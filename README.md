# SANS SEC450 — Blue Team Fundamentals: Study Notes

[![Read online](https://img.shields.io/badge/Read%20online-Blue%20Team%20Notes-2747c9?logo=bookstack&logoColor=white)](https://ammaryasser28.github.io/?t=sec450) ![Blue Team](https://img.shields.io/badge/Blue%20Team-informational) ![SOC](https://img.shields.io/badge/SOC-informational) ![Status](https://img.shields.io/badge/Status-In%20Progress-yellow)

My personal study notes for **SANS SEC450: Blue Team Fundamentals — Security Operations and Analysis**, rewritten in my own words to make each topic easier to revise. The focus is on what a SOC analyst does day to day: understanding alerts, reading logs, analyzing network traffic, and investigating suspicious hosts and files.

📖 **Read it online:** every note in this repo is on [Blue Team Notes](https://ammaryasser28.github.io/?t=sec450), with interactive diagrams, search across all four courses, and progress tracking.

> 🌐 **Language:** the notes are written in Arabic (Egyptian dialect), with every technical term and command kept in English. Each note also has a full English version: switch to **EN** at the top of [the site](https://ammaryasser28.github.io/?t=sec450&lang=en).

> **Status:** in progress. Sections 450.1–450.3 are complete; 450.4 and 450.5 are being written.

## What's Covered

- SOC structure, the alert-to-incident lifecycle, SIEM, automation, and incident management systems
- Network traffic analysis for DNS, HTTP(S), and SMTP, including common attacks and how they look on the wire
- Windows and Linux logging, log collection, parsing, and normalization
- Key Windows Event IDs for investigations (logons 4624/4625, RunAs 4648, services 7045/4697, scheduled tasks 4698, account and group changes, PowerShell, Kerberos)
- Endpoint attack tactics and identifying and handling suspicious files

## Contents (23 notes)

### 450.1 - Blue Team Tools and Operation

- [Defensible Network Concepts](450.1%20-%20Blue%20Team%20Tools%20and%20Operation%20/Defensible%20Network%20Concepts.md)
- [Events, Alerts, Anomalies, and Incidents](450.1%20-%20Blue%20Team%20Tools%20and%20Operation%20/Events%2C%20Alerts%2C%20Anomalies%2C%20and%20Incidents.md)
- [Incident Management Systems](450.1%20-%20Blue%20Team%20Tools%20and%20Operation%20/Incident%20Management%20Systems.md)
- [Know Your Enemy](450.1%20-%20Blue%20Team%20Tools%20and%20Operation%20/Know%20Your%20Enemy.md)
- [SIEM and Automation](450.1%20-%20Blue%20Team%20Tools%20and%20Operation%20/SIEM%20and%20Automation.md)
- [SOC Overview](450.1%20-%20Blue%20Team%20Tools%20and%20Operation%20/SOC%20Overview.md)
- [Threat Intelligence Platforms](450.1%20-%20Blue%20Team%20Tools%20and%20Operation%20/Threat%20Intelligence%20Platforms.md)

### 450.2 - Understanding Your Network

- [Additional Network Protocols](450.2%20-%20Understanding%20Your%20Network/Additional%20Network%20Protocols.md)
- [Network Architecture](450.2%20-%20Understanding%20Your%20Network/Network%20Architecture.md)
- [Traffic Capture and Analysis](450.2%20-%20Understanding%20Your%20Network/Traffic%20Capture%20and%20Analysis.md)
- [Understanding SMTP and Email](450.2%20-%20Understanding%20Your%20Network/Understanding%20SMTP%20and%20Email.md)
- [DNS › DNS Analysis and Attacks](450.2%20-%20Understanding%20Your%20Network/DNS/DNS%20Analysis%20and%20Attacks.md)
- [DNS › Understanding DNS](450.2%20-%20Understanding%20Your%20Network/DNS/Understanding%20DNS.md)
- [HTTP › HTTP(S) Analysis and Attacks](450.2%20-%20Understanding%20Your%20Network/HTTP/HTTP%28S%29%20Analysis%20and%20Attacks.md)
- [HTTP › Understanding HTTP](450.2%20-%20Understanding%20Your%20Network/HTTP/Understanding%20HTTP.md)

### 450.3 - Understanding Hosts, Logs, and Files

- [Endpoint Attack Tactics](450.3%20-%20Understanding%20Hosts%2C%20Logs%2C%20and%20Files/Endpoint%20Attack%20Tactics.md)
- [Endpoint Defense In Depth](450.3%20-%20Understanding%20Hosts%2C%20Logs%2C%20and%20Files/Endpoint%20Defense%20In%20Depth.md)
- [File Contents and Identification](450.3%20-%20Understanding%20Hosts%2C%20Logs%2C%20and%20Files/File%20Contents%20and%20Identification.md)
- [How Linux Logging Works](450.3%20-%20Understanding%20Hosts%2C%20Logs%2C%20and%20Files/How%20Linux%20Logging%20Works.md)
- [How Windows Logging Works](450.3%20-%20Understanding%20Hosts%2C%20Logs%2C%20and%20Files/How%20Windows%20Logging%20Works.md)
- [Identifying and Handling Suspicious Files](450.3%20-%20Understanding%20Hosts%2C%20Logs%2C%20and%20Files/Identifying%20and%20Handling%20Suspicious%20Files.md)
- [Interpreting Important Events](450.3%20-%20Understanding%20Hosts%2C%20Logs%2C%20and%20Files/Interpreting%20Important%20Events.md)
- [Log Collection, Parsing, and Normalization](450.3%20-%20Understanding%20Hosts%2C%20Logs%2C%20and%20Files/Log%20Collection%2C%20Parsing%2C%20and%20Normalization.md)

> **Note:** these are independent study notes written in my own words. They are not official SANS material and do not reproduce course content.

---

**Author:** Bn Yasser — SOC Analyst  
[LinkedIn](https://www.linkedin.com/in/bn-yasser-424bb4215/) · [GitHub](https://github.com/ammaryasser28)

⭐ If these notes help you, consider giving the repo a star.
