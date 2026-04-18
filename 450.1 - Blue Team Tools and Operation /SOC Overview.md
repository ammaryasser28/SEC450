Module 2: SOC Overview — نظرة عامة على مركز عمليات الأمنهدف الوحدةبنهاية هذه الوحدة، ستكون قادراً على:

وصف المكونات الأساسية الثلاثة لأي SOC فعّال
تحديد مهمة الفريق الأزرق وربطها بأهداف المنظمة
التمييز بين نماذج هيكلة الفريق (Tiered vs Tierless)
فهم تدفق العمليات من الجمع حتى الاستجابة للحوادث
قياس فاعلية الـ SOC من خلال مقاييس صحيحة
فهرس المحتويات
المكونات الأساسية: People, Process, Technology
تحديد المهمة: الأسئلة الأربعة الجوهرية
محاذاة الـ SOC مع المنظمة
شهية المخاطر والتوازن الأمني
هياكل الفريق: Tiered vs Tierless
وظائف الـ SOC من الجمع إلى الاستجابة
المستندات التشغيلية
قياس الأداء: SOC Metrics
الرسم التوضيحي Mermaid
عقلية المحلل وعقلية المهاجم
ملاحظات الامتحان
الملخص
1. المكونات الأساسية للـ SOCأي SOC (Security Operations Center) يرتكز على ثلاثة مكونات لا غنى عنها، وغياب أيٍّ منها يعني فشل المنظومة بالكامل:┌─────────────────────────────────────┐
│           SOC = People              │
│              + Process              │
│              + Technology           │
└─────────────────────────────────────┘المكوّنالتعريفالدور في الـ SOCPeople (الأشخاص)المحللون، المهندسون، القادةالقلب النابض — لا يمكن استبدالهم بالأتمتةProcess (العمليات)تسلسل منظّم للمهاميحدد ماذا وكيف يعمل الفريقTechnology (التكنولوجيا)الأدوات والبرمجيات والأجهزةمُضاعِف للقوة — لا بديل عن الإنسان
نقطة حرجة: التكنولوجيا ليست بديلاً عن الإنسان. إذا كان المحلل قابلاً للاستبدال بأداة، فهو كان يقوم بعمل تكراري كان يجب أتمتته من البداية.
2. تحديد المهمة: الأسئلة الأربعة الجوهريةلبناء أو تقييم أي SOC Mission، استخدم هذه الأسئلة الأربعة من كتاب Crafting the Infosec Playbook:┌──────────────────────────────────────────────────────┐
│  1. What are we trying to PROTECT?  (ماذا نحمي؟)    │
│  2. What are the THREATS?           (ما التهديدات؟)  │
│  3. How do we DETECT them?          (كيف نكتشف؟)     │
│  4. How will we RESPOND?            (كيف نستجيب؟)    │
└──────────────────────────────────────────────────────┘هذه الأسئلة ليست لمرة واحدة — يجب مراجعتها دورياً لأن التهديدات والمنظمات تتغير باستمرار.3. محاذاة الـ SOC مع المنظمةSOC Charter (ميثاق الـ SOC)الـ Charter هو المستند التأسيسي الذي يمنح الفريق الأزرق الصلاحية للعمل. يجب أن يتضمن:
الفئات المخدومة (Constituency Served)
نطاق العمل (Scope of Work)
الخدمات المقدمة (Services Delivered)
بيان المهمة (Mission Statement)
الهيكل التنظيمي (Organizational Structure)
Steering Committee (لجنة التوجيه)اجتماع دوري مع أصحاب المصلحة الرئيسيين لضمان:

محاذاة الـ SOC مع أهداف الأعمال
تحديد مخاوف المخاطر المؤسسية
قياس مدى تحقيق الـ SOC لتوقعات الإدارة
4. شهية المخاطر والتوازن الأمنيRisk Appetite (شهية المخاطر)[لا أمان] ←───────────────────────────→ [أمان مشدّد]
  Startup                            Government/Militaryنوع المنظمةمستوى الشهية للمخاطرنماذج الضوابطحكومة/عسكريمنخفض جداًApplication Control, Zero Trust, Air-gapمؤسسة ماليةمنخفضEDR/XDR, Strict Email Policiesشركة ناشئةمرتفعBasic AV, Default Loggingالحقيقتان الأساسيتان للفريق الأزرقBlue Team Truth #1: الاختراق سيحدث حتماً. السؤال ليس هل بل كيف ستؤثر النتيجة؟Blue Team Truth #2: الشركة لا توجد لتكون آمنة فقط — الأمن هو وظيفة منع الخسائر، وليس الهدف الأول.مثال واقعي: معضلة Risk Appetite
سيناريو: جهاز كمبيوتر يعمل بـ Windows XP في خط إنتاج اللقاحات — لا يمكن تعديله، يحتاج FTP للخارج، ويستضيف صفحة ويب.
الإجابة الخاطئة: "لا يجب استخدامه"
الإجابة الصحيحة: Compensating Controls — فحص المحتوى الشبكي، تقييد المنافذ، Web Application Firewall على الصعيد الخارجي.
5. هياكل الفريقالنموذج الطبقي (Tiered SOC)المستوىالمهامالخصائصTier 1Triage أولي، فتح تذاكرمهام محددة، قيود على الأدواتTier 2تحليل موسّع، تحديد نطاق الهجومحرية أكبر، دعم تكتيكيTier 3تحليل عميق، Threat Hunting، بناء منهجياتخبراء متخصصون، مشاركة استراتيجيةالنموذج اللاطبقي (Tierless SOC)الجميع يعمل معاً → الجميع مسؤول → الجميع يتعلم أسرعالمعيارTieredTierlessالهيكلمحدد وواضحمرن وتعاونيالتعلمبطيء، مقيّدسريع، شاملالاحتفاظ بالموظفينضعيف (إحباط)أفضل (انخراط)الكفاءةعاليةمتوسطة6. وظائف الـ SOC: من الجمع إلى الاستجابةالعمليات الأساسية (Core SOC Activities)Collection → Detection → Triage → Investigation → Incident Response
     ↑_____________________Continuous Improvement_____________________↑الوظيفةالوصفمن يقوم بهاData Collectionجمع البيانات من الشبكة والأجهزةEngineers, SensorsDetectionاكتشاف السلوك المشبوهIDS, SIEM, AVTriage & Investigationتأكيد التنبيهات وترتيب أولوياتهاSOC AnalystsIncident Responseالاحتواء والاستئصال والاستردادIR Team / CSIRTالقدرات الإضافية (Auxiliary Capabilities)الوظيفةالدورThreat Intelligenceتعزيز الكشف، فهم المهاجمينForensicsالتحقيق العميق في الحوادثSelf-AssessmentVuln Management, Red Team, Pentesting7. المستندات التشغيلية للمحللPolicies (إلزامي، عام)
    ↓
Standards (إلزامي، محدد)
    ↓
Procedures (خطوات تفصيلية)
    ↓
Guidelines (اختياري، أفضل الممارسات)
    ↓
Baselines (قوائم إعدادات محددة - CIS Benchmarks)
    ↓
Playbooks/Use Cases (خاصة بالـ SOC)النوعالإلزاميةالمستوىPolicyإلزاميعام جداًStandardإلزاميكيف/كمProcedureإلزاميخطوة بخطوةGuidelineاختياريأفضل الممارساتBaselineمرجعCIS BenchmarksPlaybookSOC خاصمنطق الكشف والاستجابة8. مقاييس الـ SOC (SOC Metrics)خصائص المقياس الجيد┌─────────────────────────────────────────────────┐
│  مقياس جيد يجب أن يكون:                        │
│  ✅ مشتق من القمة (Top-Down Derived)            │
│  ✅ قابل للتنفيذ (Actionable)                  │
│  ✅ محدد وقابل للتكرار (Well-Defined/Repeatable)│
│  ✅ محدّث تلقائياً (Automated/Frequent)         │
└─────────────────────────────────────────────────┘السؤال النقدي للمحلل
إذا تحسّن هذا المقياس، هل يعني ذلك فعلاً أن الأمن تحسّن؟
9. الرسم التوضيحي: تدفق الـ SOC#mermaid-r28s{font-family:inherit;font-size:16px;fill:#E5E5E5;}@keyframes edge-animation-frame{from{stroke-dashoffset:0;}}@keyframes dash{to{stroke-dashoffset:0;}}#mermaid-r28s .edge-animation-slow{stroke-dasharray:9,5!important;stroke-dashoffset:900;animation:dash 50s linear infinite;stroke-linecap:round;}#mermaid-r28s .edge-animation-fast{stroke-dasharray:9,5!important;stroke-dashoffset:900;animation:dash 20s linear infinite;stroke-linecap:round;}#mermaid-r28s .error-icon{fill:#CC785C;}#mermaid-r28s .error-text{fill:#3387a3;stroke:#3387a3;}#mermaid-r28s .edge-thickness-normal{stroke-width:1px;}#mermaid-r28s .edge-thickness-thick{stroke-width:3.5px;}#mermaid-r28s .edge-pattern-solid{stroke-dasharray:0;}#mermaid-r28s .edge-thickness-invisible{stroke-width:0;fill:none;}#mermaid-r28s .edge-pattern-dashed{stroke-dasharray:3;}#mermaid-r28s .edge-pattern-dotted{stroke-dasharray:2;}#mermaid-r28s .marker{fill:#A1A1A1;stroke:#A1A1A1;}#mermaid-r28s .marker.cross{stroke:#A1A1A1;}#mermaid-r28s svg{font-family:inherit;font-size:16px;}#mermaid-r28s p{margin:0;}#mermaid-r28s .label{font-family:inherit;color:#E5E5E5;}#mermaid-r28s .cluster-label text{fill:#3387a3;}#mermaid-r28s .cluster-label span{color:#3387a3;}#mermaid-r28s .cluster-label span p{background-color:transparent;}#mermaid-r28s .label text,#mermaid-r28s span{fill:#E5E5E5;color:#E5E5E5;}#mermaid-r28s .node rect,#mermaid-r28s .node circle,#mermaid-r28s .node ellipse,#mermaid-r28s .node polygon,#mermaid-r28s .node path{fill:transparent;stroke:#A1A1A1;stroke-width:1px;}#mermaid-r28s .rough-node .label text,#mermaid-r28s .node .label text,#mermaid-r28s .image-shape .label,#mermaid-r28s .icon-shape .label{text-anchor:middle;}#mermaid-r28s .node .katex path{fill:#000;stroke:#000;stroke-width:1px;}#mermaid-r28s .rough-node .label,#mermaid-r28s .node .label,#mermaid-r28s .image-shape .label,#mermaid-r28s .icon-shape .label{text-align:center;}#mermaid-r28s .node.clickable{cursor:pointer;}#mermaid-r28s .root .anchor path{fill:#A1A1A1!important;stroke-width:0;stroke:#A1A1A1;}#mermaid-r28s .arrowheadPath{fill:#0b0b0b;}#mermaid-r28s .edgePath .path{stroke:#A1A1A1;stroke-width:2.0px;}#mermaid-r28s .flowchart-link{stroke:#A1A1A1;fill:none;}#mermaid-r28s .edgeLabel{background-color:transparent;text-align:center;}#mermaid-r28s .edgeLabel p{background-color:transparent;}#mermaid-r28s .edgeLabel rect{opacity:0.5;background-color:transparent;fill:transparent;}#mermaid-r28s .labelBkg{background-color:rgba(0, 0, 0, 0.5);}#mermaid-r28s .cluster rect{fill:#CC785C;stroke:hsl(15, 12.3364485981%, 48.0392156863%);stroke-width:1px;}#mermaid-r28s .cluster text{fill:#3387a3;}#mermaid-r28s .cluster span{color:#3387a3;}#mermaid-r28s div.mermaidTooltip{position:absolute;text-align:center;max-width:200px;padding:2px;font-family:inherit;font-size:12px;background:#CC785C;border:1px solid hsl(15, 12.3364485981%, 48.0392156863%);border-radius:2px;pointer-events:none;z-index:100;}#mermaid-r28s .flowchartTitleText{text-anchor:middle;font-size:18px;fill:#E5E5E5;}#mermaid-r28s rect.text{fill:none;stroke-width:0;}#mermaid-r28s .icon-shape,#mermaid-r28s .image-shape{background-color:transparent;text-align:center;}#mermaid-r28s .icon-shape p,#mermaid-r28s .image-shape p{background-color:transparent;padding:2px;}#mermaid-r28s .icon-shape rect,#mermaid-r28s .image-shape rect{opacity:0.5;background-color:transparent;fill:transparent;}#mermaid-r28s .label-icon{display:inline-block;height:1em;overflow:visible;vertical-align:-0.125em;}#mermaid-r28s .node .label-icon path{fill:currentColor;stroke:revert;stroke-width:revert;}#mermaid-r28s :root{--mermaid-font-family:inherit;}NoYesEvents & Logs(Network + Endpoint)Data Collection Layer(SIEM, NetFlow, EDR)Detection Engine(IDS / SIEM Analytics / AV)Alert Queue(Triage Pending)Tier 1 Analyst(Initial Triage)True Positive?Close / False Positive(Tune Rule)Tier 2/3 Investigation(Deep Dive)Incident Response(Contain, Eradicate, Recover)Lessons Learned(Continuous Improvement)Threat IntelligenceRed Team / PentestingForensics10. عقلية المحلل والمهاجمDetection Mindset (عقلية الكشف)ماذا تبحث في الـ SIEM؟spl# مثال Splunk: كشف الأنشطة غير الطبيعية
index=security_logs
| stats count by src_ip, dest_port
| where count > 100
| sort -count
ابحث عن Anomalies في بيانات التدفق (NetFlow) لاكتشاف Lateral Movement
راقب Failed Logins المتكررة لاكتشاف Brute Force
تتبع New Processes لاكتشاف التنفيذ غير المصرح به
Attack Mindset (عقلية المهاجم — MITRE ATT&CK)تكتيك المهاجمMITRE TIDكيف يخترق الـ SOC دفاعاتكInitial AccessT1566 (Phishing)إذا لم تكن هناك رقابة على البريدDiscoveryT1082 (System Info Discovery)أوامر نظام مدمجة — صعب الكشفLateral MovementT1021 (Remote Services)ينجح في الشبكات المسطحة (Flat Networks)ExfiltrationT1048 (Exfil over Alt Protocol)يستغل الثغرات في قواعد جدار الحماية الصادرةCommon Pitfalls (الأخطاء الشائعة)
❌ Alert Fatigue: كثرة التنبيهات تجعل المحللين يتجاهلون الحقيقية
❌ الاعتماد على التكنولوجيا فقط: لا يوجد أداة تحل محل التحليل البشري
❌ غياب الـ Baseline: بدون معرفة "الطبيعي"، لا يمكنك اكتشاف "غير الطبيعي"
❌ مقاييس وهمية: قياس عدد التذاكر المغلقة لا يعكس التحسن الأمني الحقيقي
11. ملاحظات الامتحان
🔑 Key Notes

الـ SOC Charter = مستند يمنح الصلاحية ويحدد النطاق — معتمد من الإدارة
الـ Steering Committee = آلية محاذاة مستمرة مع أهداف الأعمال
Risk Appetite يتغير مع تغيير القيادة أو نضج المنظمة
الـ Playbook هو أكثر الوثائق خصوصية للـ SOC — يحتوي منطق الكشف والاستجابة
Tier 3 ≠ مجرد ترقية — هو دور متخصص في Hunting والتحليل العميق


🎯 Exam Strategy
في الامتحان، إذا سُئلت عن هيكل الـ SOC، ركّز على:

الفرق بين Core Functions (Collection, Detection, Triage, IR) وAuxiliary (TI, Forensics, Red Team)
الفرق بين Tiered (كفاءة + إحباط محتمل) وTierless (انخراط + فوضى محتملة)
معادلة المقياس الجيد: Goal-Aligned + Actionable + Repeatable + Automated
