> **Goal of this section:**
> We'll understand that any file is fundamentally just a sequence of bytes, and we'll learn how to identify a file's type without relying on its extension, using tools such as the **file command**, **hexdump**, **magic bytes**, and **strings**. We'll also cover the concepts of Unicode and encoding and how they affect extracting strings from any file.

## Table of Contents
- [Introduction](#introduction)
- [File Content: What Is a File, Really?](#file-content-what-is-a-file-really)
- [Identifying the File Type](#identifying-the-file-type)
- [Using the file Command](#using-the-file-command)
- [Magic Bytes](#magic-bytes)
- [Nested Files](#nested-files)
- [Polyglots](#polyglots)
- [Unicode and Encoding](#unicode-and-encoding)
- [What Are Strings?](#what-are-strings)
- [A Practical Strings Example](#a-practical-strings-example)
- [Strings in Different Byte Orders and Encodings](#strings-in-different-byte-orders-and-encodings)
- [How Strings Help Us](#how-strings-help-us)
- [Summary](#Summary)

## Introduction

In this section, we'll dive into the nature of files at the byte level and learn how to analyze them to determine their type and content and extract additional information from them. Understanding files at this level is a core skill, because there are many situations where you'll need it. For example, if you get a PCAP in which an infected machine made a GET request to a certain URL and received a certain file... what is that file? And how do we know whether it's dangerous or not?

## File Content: What Is a File, Really?

At the most basic level, **a file is just a sequence of bytes**. That sequence can represent anything:

- It could be plain text, such as a PowerShell script.
- It could be a compiled program, such as an executable.

Each file type (PDF, DOCX, TXT) has unique characteristics, and the program that opens it has to interpret the byte sequence in its own way to display it on screen. Each type works in a completely different way and has different security implications.

### The hexdump Tool

If you want to see the raw bytes of any file, you can use a tool like **hexdump**. The output consists of 3 columns:

| Column | Description |
|------|--------|
| Left column | The offset from the beginning of the file |
| Middle column | The bytes represented in hex |
| Right column | The same bytes represented as ASCII characters (where possible) |

> [!NOTE]
> If you run hexdump on a random PDF file, you'll find the letters "PDF" in the first few bytes — an easy hint that we're looking at the PDF format, even if we didn't know that to begin with.

## Identifying the File Type

### The Scenario

A machine downloaded a file from `http://mystery.com/x`. What type of file is it? Is it dangerous?

After extracting the file with a tool like **Wireshark**, there are several methods you can use:

1. Run the **file** command in Linux to try to identify the type automatically.
2. Run a hexdump and look for **Magic Bytes**.
3. Examine the **Strings** for clues or nested content.
4. Run automated analysis in a **Sandbox** or **Virtual Machine** (Dynamic Analysis).

## Using the file Command

The Linux **file** command is the first quick attempt at identifying any file. This tool has a large library of known formats and can determine a file's type based on its bytes.

### Example

If you have 6 files with no extension and you run the command:

```bash
file *
```

The result might be:

| File | Type |
|------|--------|
| A, F | Windows Executable |
| B | Linux Executable |
| C | PNG Image |
| D | SVG Image |
| E | PDF File |

> [!TIP]
> If the file is just plain text, the file command will usually report it as "ASCII text". The exception is when the text is a known scripting language, such as a bash script, which may show up as "Bourne-Again shell script, ASCII text executable".

## Magic Bytes

### How Does the file Command Work?

By recognizing **Magic Bytes**, also known as the **File Signature**. Almost every file format has a standard that defines how its bytes must be organized, and one of the most important features of that structure is a **Signifier** in the first few bytes of the file that confirms its type.

### The Most Common Magic Bytes

| File Type | First Bytes (Hex) | ASCII |
|------|--------|---------|
| EXE | 4D 5A | MZ |
| ZIP, DOCX, XLSX, PPTX | 50 4B 03 04 | PK.. |
| GZ | 1F 8B | .. |
| PDF | 25 50 44 46 2D | %PDF- |
| RTF | 7B 5C 72 74 66 31 | {\rtf1 |
| PNG | 89 50 4E 47 0D 0A 1A 0A | .PNG... |

> [!IMPORTANT]
> Notice something odd: **ZIP** files have the same magic bytes as **Microsoft Office** documents (DOCX, XLSX, PPTX). That's because Office documents are actually **ZIP files**! You can change the extension, unzip it, and see the internal components the file was built from.

Not all magic bytes have a readable ASCII representation (the printable characters are in bold in the table), and in that case you'll need to use **hexdump** to identify them manually.

## Nested Files

### Why Not Rely on the file Command Alone?

The file command works well when the file is already separate, but if you're looking at a raw stream of bytes coming from a PCAP, or a file embedded inside another file, the file command **won't be able to identify it**. This is where you have to rely on your knowledge of magic bytes.

### The Nested Files Technique

Some file types (such as a Word doc or a PDF) allow additional files to be embedded inside them, and this is a common phishing technique. Tools such as **foremost**, **binwalk**, and **scalpel** are designed to search for magic bytes at **any point** inside the file, not just at the beginning, and can extract nested files automatically.

### Example

In a malicious .doc file, we might find the magic bytes of a compressed ZIP file embedded inside it. The two letters **PK** are the easiest thing to spot, followed by non-printable bytes such as `0x03` and `0x04`.

> [!TIP]
> If you're interested in going deeper into this topic for malware analysis, the SANS **FOR610: Reverse Engineering Malware** course covers it in detail.

## Polyglots

### What Makes a File Valid?

The answer is **not the name or the extension**; it **depends 100% on the bytes themselves**. If the magic bytes indicate the file is a PDF, the content follows the PDF specification, and it opens in a PDF reader, then by every measure it is a PDF file.

### But Could It Be Something Else Too?

Yes! This is what's called a **Polyglot File** — a file that is valid in more than one format at the same time. A fun example: an image posted on Twitter that is a fully working image, but if you extract it as an archive, you'll find a **multi-part RAR** archive containing Shakespeare's text inside!

> [!WARNING]
> Although using polyglots in a security context isn't common, it can be a very clever way to hide a malicious file if an attacker decides to use it. Standards can be combined so that the same byte sequence is read correctly by more than one program at the same time.

## Unicode and Encoding

### The Core Idea

Since most of the world doesn't use English ASCII characters alone, there has to be a broader character mapping. **Unicode** is the system that ultimately won, and it defines more than **1.1 million characters** as **Code Points**, with each character written as `U+` followed by a number (for example, A = U+41).

### Code Point vs. Encoding

The code point is the character's number itself, while **the encoding** is the way the code point is converted into actual bytes inside the file. Some of the most common encodings:

| Encoding | Description |
|------|--------|
| ASCII | One character = one byte; covers English characters only |
| UTF-8 | Variable length; uses the least space |
| UTF-16 | Variable length; usually uses 2 bytes per character |
| UTF-32 | Constant length; always 4 bytes per character |

### A Practical Example

The phrase "学SEC450" (学 means "study" in Kanji) can be written as 3 completely different byte sequences:

```
UTF-8  = e5ada6 53 45 43 34 35 30
UTF-16 = 5b66 0053 0045 0043 0034 0035 0030
UTF-32 = 00005b66 00000053 00000045 00000043 00000034 00000035 00000030
```

| Encoding | Representation Length | Note |
|------|--------|---------|
| UTF-8 | Variable | English characters have the same values as ASCII, but the Kanji needs more than one byte |
| UTF-16 | Fixed in this example (2 bytes per character) | All characters are represented with the same length |
| UTF-32 | Always fixed (4 bytes) | Less efficient, but easier to interpret |

> [!IMPORTANT]
> If you try to decode text written in UTF-8 using the wrong table, such as ASCII, UTF-16, or UTF-32, you'll get garbled, unreadable characters. You need to know the correct encoding to read the text properly.

## What Are Strings?

Since files are just sequences of bytes from 0 to 255 (0x0 to 0xFF in hex), encoding standards such as **ASCII** map some of those bytes to printable characters.

### Definition

A **String** is a contiguous sequence of printable characters that ends as soon as it hits a non-printable byte.

### Example

If the file contains the bytes `[00 01 02 03 74 65 73 74 04 05 06]`, the only string will be "test", because it's the only group of consecutive printable characters.

### Classification: Plaintext vs. Binary

| Type | Description | Examples |
|------|--------|---------|
| Plaintext | The entire file is printable characters, so the whole file is "one long string" | txt, vbs, ps1, js |
| Binary | Contains both printable and non-printable bytes | zip, docx, exe, jpg |

### The strings Command in Linux

It prints every contiguous sequence of printable characters in a given file by trying to decode it with different standards. Running it on a plaintext file won't give you anything useful (since the whole file is a single string), but running it on a binary file such as an executable can reveal metadata, URLs, or other important information.

## A Practical Strings Example

If you run `strings -n 10` (meaning the minimum string length is 10 characters) on a Windows executable, you'll find output like:

| Discovered String | What It Indicates |
|------|--------|
| "This program cannot be run in DOS mode" | A phrase found in every EXE file; clear evidence that the file is an executable |
| MSVBVM60.DLL | A library associated with the Microsoft Visual Basic Virtual Machine, meaning the program was built with Visual Basic |
| "REATTACKED" | An unusual string that may be unique to a specific malware family; useful for identifying similar files later |

> [!NOTE]
> A large portion of the bytes in any executable is non-printable, so no strings come out of it. Printable parts (like "MZ" at the beginning) won't appear in the output if they are shorter than the specified minimum (10 characters here).

## Strings in Different Byte Orders and Encodings

### An Important Reminder

Not all encodings are ASCII, and not every character takes exactly one byte! If you only use the default strings command, you might miss very important strings written in a different encoding.

### The -e Option of the strings Command

| Value | Meaning |
|------|--------|
| s | Single 7-bit characters (ASCII, the default) |
| S | Single 8-bit characters |
| b | 16-bit Big Endian |
| l | 16-bit Little Endian |
| B | 32-bit Big Endian |
| L | 32-bit Little Endian |

> [!TIP]
> **Little Endian** means the least significant byte comes first. If you only use ASCII mode and no strings show up, try the other encodings such as `-e l` (16-bit little endian) before giving up — the text might be UTF-16, and with ASCII you'd misinterpret it as a set of single characters separated by null bytes.

## How Strings Help Us

### Their Value for Static Analysis

Many **IOCs (Indicators of Compromise)** are ordinary printable strings. Looking at an executable's strings is an excellent way to identify:

- Files the malware might download.
- Domains or IP addresses it will communicate with.
- Affected registry keys.

> [!IMPORTANT]
> Analyzing strings without running the program is called **Static Analysis**, and it is completely safe. The alternative is **Dynamic Analysis**, which is when you actually let the program run in a sandbox or virtual machine.

### Additional Advantages

- It works well on **PCAP files, PDFs, Pictures**, and many other types, not just executables.
- It helps you easily find domains, user-agents, cookies, and URLs inside files.

### Limitations

- **It won't work on compressed files**, because compression completely changes the file's internal structure.

### Strings from Memory

There's a more advanced method that extracts strings from the memory bytes of a program that is actually running. This method is **Dynamic Analysis**, because the program has to be running.

> [!NOTE]
> If the malware is encrypted or "packed," strings may appear in memory that didn't show up in normal static analysis. If you see strings in a particular sandbox (such as hybrid-analysis) but didn't find them when you ran the strings command yourself, it's most likely because they were extracted from memory during actual execution.

## Summary 

- Any file is just a **sequence of bytes**; the extension has no real meaning in determining the type.
- Some files are "Plaintext" (all characters are printable) and some are "Binary" (they contain non-printable bytes).
- The Linux **file** command is the first quick tool for identifying a file's type.
- **Magic Bytes** (or the File Signature) are the first few bytes that determine a file's type, and you can view them with a tool like hexdump.
- Nested files require tools such as **foremost, binwalk, scalpel** to be discovered.
- **Polyglot Files** are files that are valid in more than one format at the same time.
- **Unicode** defines characters as code points, and the **Encoding** (ASCII, UTF-8, UTF-16, UTF-32) determines how they are converted into actual bytes.
- **Strings** are contiguous sequences of printable characters, and the Linux **strings** tool extracts them.
- You should try different encodings with the strings command (using `-e`) so you don't miss important evidence.
- Analyzing strings is safe **Static Analysis**, and it's very useful for identifying IOCs without running the file.

