SOC Overview — فهم الأساس الذي يقوم عليه كل شيء

📌 فهرس المحتوى

لماذا نبدأ من هنا؟
مكونات SOC الثلاثة: People, Process, Technology
الأربعة أسئلة التي تحدد مهمتك
SOC Charter — الوثيقة التي تعطيك الصلاحية
Risk Appetite — حدود الأمان التي تقررها المؤسسة
حين تتعارض الأمان مع الواقع
Accepting the Risk — قبول الخطر كقرار إداري
Blue Team Truths — الحقيقتان اللتان لا بد من قبولهما
الهيكل التنظيمي للـ SOC
Tiered vs Tierless SOC — أيهما أفضل؟
كيف يعمل الـ SOC من الداخل
المعلومات الحيوية التي يجب أن تكون دائماً أمامك
وثائق الـ SOC التي يجب أن تعرفها
Metrics — كيف يُقاس أداؤك
Key Takeaways


لماذا نبدأ من هنا؟ {#why-start-here}
ليه المحلل الجديد في SOC يحتاج يفهم كيف يُبنى الـ SOC قبل ما يبدأ يشتغل؟
لأن كثيراً من المحللين يدخلون الـ SOC ولا يعرفون إجابة لسؤال بسيط: لماذا نحن هنا؟
يشتغلون على الـ alerts، يعملون triage، يفتحون tickets — لكن بدون فهم الصورة الكبيرة. وهذا يصنع محللاً يتبع خطوات من غير ما يفكر.
الوحدة دي مش عن الأدوات. دي عن الإطار الذهني اللي لازم يكون عندك قبل ما تلمس أي أداة.

مكونات SOC الثلاثة {#three-pillars}
ببساطة، أي SOC يقوم على ثلاث ركائز:
People — Process — Technology
وده مش مجرد كلام نظري. لو أي ركيزة اتكسرت، الـ SOC بيبقى أقل كفاءة أو بيفشل خالص.
الناس — People
أهم عنصر على الإطلاق. المحللون، الـ leads، الـ engineers — هم القلب. مفيش technology أو process تقدر تعوض فريق فاشل أو غير مدرَّب أو غير سعيد.

[!warning]
لو المحلل قدر يُستبدل بأوتوماشن — فده مش محلل، ده كان يعمل شغل الأوتوماشن أصلاً. المحلل الحقيقي يعمل analysis، مش تكليك.

العملية — Process
هي التتالي المنظم للمهام اللي توصلنا للنتيجة المطلوبة. الـ process بتحدد: إيه اللي لازم يتعمل؟ بأي ترتيب؟ ومين المسؤول؟
بدون process، حتى أحسن فريق هيشتغل بشكل عشوائي.
التقنية — Technology
هي المُمكِّن. بتخلي الـ process أسرع وأكثر دقة. لكنها مش بديل للناس — هي تضخيم لقدراتهم.
#mermaid-rmr{font-family:inherit;font-size:16px;fill:#E5E5E5;}@keyframes edge-animation-frame{from{stroke-dashoffset:0;}}@keyframes dash{to{stroke-dashoffset:0;}}#mermaid-rmr .edge-animation-slow{stroke-dasharray:9,5!important;stroke-dashoffset:900;animation:dash 50s linear infinite;stroke-linecap:round;}#mermaid-rmr .edge-animation-fast{stroke-dasharray:9,5!important;stroke-dashoffset:900;animation:dash 20s linear infinite;stroke-linecap:round;}#mermaid-rmr .error-icon{fill:#CC785C;}#mermaid-rmr .error-text{fill:#3387a3;stroke:#3387a3;}#mermaid-rmr .edge-thickness-normal{stroke-width:1px;}#mermaid-rmr .edge-thickness-thick{stroke-width:3.5px;}#mermaid-rmr .edge-pattern-solid{stroke-dasharray:0;}#mermaid-rmr .edge-thickness-invisible{stroke-width:0;fill:none;}#mermaid-rmr .edge-pattern-dashed{stroke-dasharray:3;}#mermaid-rmr .edge-pattern-dotted{stroke-dasharray:2;}#mermaid-rmr .marker{fill:#A1A1A1;stroke:#A1A1A1;}#mermaid-rmr .marker.cross{stroke:#A1A1A1;}#mermaid-rmr svg{font-family:inherit;font-size:16px;}#mermaid-rmr p{margin:0;}#mermaid-rmr .label{font-family:inherit;color:#E5E5E5;}#mermaid-rmr .cluster-label text{fill:#3387a3;}#mermaid-rmr .cluster-label span{color:#3387a3;}#mermaid-rmr .cluster-label span p{background-color:transparent;}#mermaid-rmr .label text,#mermaid-rmr span{fill:#E5E5E5;color:#E5E5E5;}#mermaid-rmr .node rect,#mermaid-rmr .node circle,#mermaid-rmr .node ellipse,#mermaid-rmr .node polygon,#mermaid-rmr .node path{fill:transparent;stroke:#A1A1A1;stroke-width:1px;}#mermaid-rmr .rough-node .label text,#mermaid-rmr .node .label text,#mermaid-rmr .image-shape .label,#mermaid-rmr .icon-shape .label{text-anchor:middle;}#mermaid-rmr .node .katex path{fill:#000;stroke:#000;stroke-width:1px;}#mermaid-rmr .rough-node .label,#mermaid-rmr .node .label,#mermaid-rmr .image-shape .label,#mermaid-rmr .icon-shape .label{text-align:center;}#mermaid-rmr .node.clickable{cursor:pointer;}#mermaid-rmr .root .anchor path{fill:#A1A1A1!important;stroke-width:0;stroke:#A1A1A1;}#mermaid-rmr .arrowheadPath{fill:#0b0b0b;}#mermaid-rmr .edgePath .path{stroke:#A1A1A1;stroke-width:2.0px;}#mermaid-rmr .flowchart-link{stroke:#A1A1A1;fill:none;}#mermaid-rmr .edgeLabel{background-color:transparent;text-align:center;}#mermaid-rmr .edgeLabel p{background-color:transparent;}#mermaid-rmr .edgeLabel rect{opacity:0.5;background-color:transparent;fill:transparent;}#mermaid-rmr .labelBkg{background-color:rgba(0, 0, 0, 0.5);}#mermaid-rmr .cluster rect{fill:#CC785C;stroke:hsl(15, 12.3364485981%, 48.0392156863%);stroke-width:1px;}#mermaid-rmr .cluster text{fill:#3387a3;}#mermaid-rmr .cluster span{color:#3387a3;}#mermaid-rmr div.mermaidTooltip{position:absolute;text-align:center;max-width:200px;padding:2px;font-family:inherit;font-size:12px;background:#CC785C;border:1px solid hsl(15, 12.3364485981%, 48.0392156863%);border-radius:2px;pointer-events:none;z-index:100;}#mermaid-rmr .flowchartTitleText{text-anchor:middle;font-size:18px;fill:#E5E5E5;}#mermaid-rmr rect.text{fill:none;stroke-width:0;}#mermaid-rmr .icon-shape,#mermaid-rmr .image-shape{background-color:transparent;text-align:center;}#mermaid-rmr .icon-shape p,#mermaid-rmr .image-shape p{background-color:transparent;padding:2px;}#mermaid-rmr .icon-shape rect,#mermaid-rmr .image-shape rect{opacity:0.5;background-color:transparent;fill:transparent;}#mermaid-rmr .label-icon{display:inline-block;height:1em;overflow:visible;vertical-align:-0.125em;}#mermaid-rmr .node .label-icon path{fill:currentColor;stroke:revert;stroke-width:revert;}#mermaid-rmr :root{--mermaid-font-family:inherit;}PeopleSOCProcessTechnologyDetected & Remediated Incidents

الأربعة أسئلة التي تحدد مهمتك {#four-questions}
قبل ما تبني SOC أو تقيّم الـ SOC اللي شغّال فيه، في أربع أسئلة أساسية لازم تكون عندك إجابة واضحة عليهم:
السؤالما يعنيه في الواقعWhat are we trying to protect?إيه الأصول الحساسة؟ البيانات، الأنظمة، الخدماتWhat are the threats?مين المهاجم المحتمل؟ إيه التكتيكات المتوقعة؟How do we detect them?إيه مصادر البيانات؟ إيه الـ analytics اللازمة؟How will we respond?إيه الـ playbooks؟ مين المسؤول؟

[!info]
الإجابات دي مش ثابتة. التهديدات بتتغير، الفريق بيتغير، والمؤسسة بتتطور. المراجعة الدورية ضرورية.


SOC Charter — الوثيقة التي تعطيك الصلاحية {#charter}
تخيل إنك محلل في SOC وبدأت تعمل حاجة معينة، وجه مدير من قسم تاني وقالك "إنتو ليه بتراقبوا نظامنا ده؟ ده مش شغلتكم!"
هنا بييجي دور الـ SOC Charter.
الـ Charter هو الوثيقة الرسمية اللي بتوضح:

مين الـ SOC بيحمي؟ (Constituency served)
إيه الخدمات اللي بيقدمها؟ (Services)
إيه نطاق عمله؟ (Scope of work)
إيه رسالته العليا؟ (Mission statement)

الـ Charter بيحمي الـ SOC قانونياً وإدارياً ويعطيه سلطة التصرف.
Steering Committee
مش كفاية تكتب Charter مرة وتسيبه. المؤسسة بتتغير، التهديدات بتتغير. الـ Steering Committee هو الاجتماع الدوري مع أصحاب المصلحة في المؤسسة اللي بيضمن إن الـ SOC دايماً متوافق مع أولويات الشركة.

Risk Appetite — حدود الأمان التي تقررها المؤسسة {#risk-appetite}
هنا في سؤال ينبغي لكل محلل أن يسأله عن المؤسسة التي يعمل فيها: ما المستوى الذي هي مستعدة لقبوله من الخطر؟
مش كل المؤسسات نفسها:

حكومة / عسكري → Risk appetite منخفض جداً → ضوابط صارمة جداً
Startup ناشئة → Risk appetite مرتفع → أولوية السرعة على الأمان


[!info]
المؤسسة مش موجودة عشان تكون secure. هي موجودة عشان تحقق قيمة. الأمان هو وسيلة لحماية تلك القيمة، مش هدف في حد ذاته.

Risk Appetite Statement
بعض المؤسسات بيكتبوا وثيقة رسمية اسمها Risk Appetite Statement بتوضح فيها بالضبط مستوى المخاطرة المقبول. لو موجودة في مؤسستك — اقرأها.
دورك كمحلل مش تفرض مستوى أمان لا تريده المؤسسة، بل توضح للإدارة الخطر الحقيقي وتساعدهم يتخذوا قرار واعي.

حين تتعارض الأمان مع الواقع {#reality-check}

[!warning]
من أصعب اللحظات في حياة محلل SOC أو Security Engineer هي لما يكتشف إن "الحل الصح" مستحيل تطبيقه في الواقع.

المثال من المصدر واضح جداً: تخيل إن في جهاز يعمل بنظام Windows XP، مسؤول عن خط إنتاج حيوي في شركة أدوية. لا يمكن تحديثه، لا يمكن إضافة برامج عليه، وهو يستخدم FTP غير مشفر. كيف تؤمّنه؟
الإجابة الخاطئة: "لا تستخدموه."
الإجابة الصحيحة: ابحث عن Compensating Controls خارجية — جدران حماية خارجية، فلترة الشبكة، WAF — وراقب ما يمكن مراقبته.
الفكرة هنا: الأمان المثالي نادراً ما يكون ممكناً. الأمان الممكن هو ما تسعى إليه.

Accepting the Risk — قبول الخطر كقرار إداري {#accepting-risk}
لو وضحت للإدارة كل المخاطر وقدمت كل التوصيات، وقرروا عدم التصرف — مش دايماً هدا كارثة.
Risk Acceptance هو قرار إداري مقبول، شريطة أنه قرار واعٍ. دورك هو:

توثيق التوصية
توضيح الخطر بدقة
ترك القرار لمن يملكه


[!info]
ده مش تخلٍّ عن المسؤولية. ده احترام لحدود دورك وضمان إن قرار القبول مكتوب وموثق، مش شفهي.


Blue Team Truths — الحقيقتان اللتان لا بد من قبولهما {#blue-team-truths}
الحقيقة الأولى: Compromise Will Happen
مش لو، لما.
الفكرة مش إن نمنع كل اختراق — ده غير واقعي. الفكرة إن نضمن إن أي اختراق:

يُكتشف بسرعة
يُحتوى قبل ما يكمل مهمته
تأثيره يكون أقل ما يمكن

المحاور مش اللي يمنع المهاجم من الدخول فقط — ده مهم. المحاور أكثر هو اللي يضمن إن المهاجم لو دخل، ما يقدرش يكمل.
الحقيقة الثانية: شركتك مش موجودة عشان تكون Secure
الـ SOC هو وظيفة Loss Prevention — زي حراس أمن المتجر بالضبط. متجر بيفتش كل زبون قبل يدخل مش هيفلس من السرقة، هيفلس من الفلوس.
التوازن بين الأمان والإنتاجية هو الفن الحقيقي للـ Blue Team.

الهيكل التنظيمي للـ SOC {#org-structure}
#mermaid-rms{font-family:inherit;font-size:16px;fill:#E5E5E5;}@keyframes edge-animation-frame{from{stroke-dashoffset:0;}}@keyframes dash{to{stroke-dashoffset:0;}}#mermaid-rms .edge-animation-slow{stroke-dasharray:9,5!important;stroke-dashoffset:900;animation:dash 50s linear infinite;stroke-linecap:round;}#mermaid-rms .edge-animation-fast{stroke-dasharray:9,5!important;stroke-dashoffset:900;animation:dash 20s linear infinite;stroke-linecap:round;}#mermaid-rms .error-icon{fill:#CC785C;}#mermaid-rms .error-text{fill:#3387a3;stroke:#3387a3;}#mermaid-rms .edge-thickness-normal{stroke-width:1px;}#mermaid-rms .edge-thickness-thick{stroke-width:3.5px;}#mermaid-rms .edge-pattern-solid{stroke-dasharray:0;}#mermaid-rms .edge-thickness-invisible{stroke-width:0;fill:none;}#mermaid-rms .edge-pattern-dashed{stroke-dasharray:3;}#mermaid-rms .edge-pattern-dotted{stroke-dasharray:2;}#mermaid-rms .marker{fill:#A1A1A1;stroke:#A1A1A1;}#mermaid-rms .marker.cross{stroke:#A1A1A1;}#mermaid-rms svg{font-family:inherit;font-size:16px;}#mermaid-rms p{margin:0;}#mermaid-rms .label{font-family:inherit;color:#E5E5E5;}#mermaid-rms .cluster-label text{fill:#3387a3;}#mermaid-rms .cluster-label span{color:#3387a3;}#mermaid-rms .cluster-label span p{background-color:transparent;}#mermaid-rms .label text,#mermaid-rms span{fill:#E5E5E5;color:#E5E5E5;}#mermaid-rms .node rect,#mermaid-rms .node circle,#mermaid-rms .node ellipse,#mermaid-rms .node polygon,#mermaid-rms .node path{fill:transparent;stroke:#A1A1A1;stroke-width:1px;}#mermaid-rms .rough-node .label text,#mermaid-rms .node .label text,#mermaid-rms .image-shape .label,#mermaid-rms .icon-shape .label{text-anchor:middle;}#mermaid-rms .node .katex path{fill:#000;stroke:#000;stroke-width:1px;}#mermaid-rms .rough-node .label,#mermaid-rms .node .label,#mermaid-rms .image-shape .label,#mermaid-rms .icon-shape .label{text-align:center;}#mermaid-rms .node.clickable{cursor:pointer;}#mermaid-rms .root .anchor path{fill:#A1A1A1!important;stroke-width:0;stroke:#A1A1A1;}#mermaid-rms .arrowheadPath{fill:#0b0b0b;}#mermaid-rms .edgePath .path{stroke:#A1A1A1;stroke-width:2.0px;}#mermaid-rms .flowchart-link{stroke:#A1A1A1;fill:none;}#mermaid-rms .edgeLabel{background-color:transparent;text-align:center;}#mermaid-rms .edgeLabel p{background-color:transparent;}#mermaid-rms .edgeLabel rect{opacity:0.5;background-color:transparent;fill:transparent;}#mermaid-rms .labelBkg{background-color:rgba(0, 0, 0, 0.5);}#mermaid-rms .cluster rect{fill:#CC785C;stroke:hsl(15, 12.3364485981%, 48.0392156863%);stroke-width:1px;}#mermaid-rms .cluster text{fill:#3387a3;}#mermaid-rms .cluster span{color:#3387a3;}#mermaid-rms div.mermaidTooltip{position:absolute;text-align:center;max-width:200px;padding:2px;font-family:inherit;font-size:12px;background:#CC785C;border:1px solid hsl(15, 12.3364485981%, 48.0392156863%);border-radius:2px;pointer-events:none;z-index:100;}#mermaid-rms .flowchartTitleText{text-anchor:middle;font-size:18px;fill:#E5E5E5;}#mermaid-rms rect.text{fill:none;stroke-width:0;}#mermaid-rms .icon-shape,#mermaid-rms .image-shape{background-color:transparent;text-align:center;}#mermaid-rms .icon-shape p,#mermaid-rms .image-shape p{background-color:transparent;padding:2px;}#mermaid-rms .icon-shape rect,#mermaid-rms .image-shape rect{opacity:0.5;background-color:transparent;fill:transparent;}#mermaid-rms .label-icon{display:inline-block;height:1em;overflow:visible;vertical-align:-0.125em;}#mermaid-rms .node .label-icon path{fill:currentColor;stroke:revert;stroke-width:revert;}#mermaid-rms :root{--mermaid-font-family:inherit;}SOC LeadCore TeamSOC-AdjacentTier 1 AnalystsTier 2-3 / SMEsDetection EngineeringIncident ResponseEngineering & InfraThreat IntelligenceForensicsVuln ManagementPen Testing / Red Team

[!info]
مفيش هيكل واحد صح لكل المؤسسات. الهيكل الصح هو اللي يضمن التواصل والكفاءة. لو الـ org chart بيمنع التعاون — وقت لمراجعته.


Tiered vs Tierless SOC — أيهما أفضل؟ {#tiers}
Tiered SOC
كل محلل عنده مستوى ومهام محددة:
Tierالمهام الأساسيةTier 1Initial triage, alert review, ticket generationTier 2Attack scoping, deeper analysis, remediation supportTier 3Deep analysis, methodology development, threat hunting
ميزة: مسار واضح للترقي، عمليات منتظمة.
عيب: قد يصبح مقيداً جداً ويسبب frustration وارتفاع معدل الاستقالات.
Tierless SOC
الكل يعمل على كل شيء، لكن بمستويات مختلفة من الاستقلالية.
ميزة: تعلم أسرع، انخراط أعلى، retention أفضل.
عيب: يتطلب نضجاً وعياً ذاتياً بالحدود من كل عضو.

[!warning]
الـ Tierless مش فوضى. هو يتطلب إن كل شخص يعرف حدوده ويطلب مساعدة لما يحتاجها.

لا يوجد نموذج أفضل — كل نموذج محسَّن لشيء مختلف.

كيف يعمل الـ SOC من الداخل {#soc-functions}
الدورة الأساسية
#mermaid-rmt{font-family:inherit;font-size:16px;fill:#E5E5E5;}@keyframes edge-animation-frame{from{stroke-dashoffset:0;}}@keyframes dash{to{stroke-dashoffset:0;}}#mermaid-rmt .edge-animation-slow{stroke-dasharray:9,5!important;stroke-dashoffset:900;animation:dash 50s linear infinite;stroke-linecap:round;}#mermaid-rmt .edge-animation-fast{stroke-dasharray:9,5!important;stroke-dashoffset:900;animation:dash 20s linear infinite;stroke-linecap:round;}#mermaid-rmt .error-icon{fill:#CC785C;}#mermaid-rmt .error-text{fill:#3387a3;stroke:#3387a3;}#mermaid-rmt .edge-thickness-normal{stroke-width:1px;}#mermaid-rmt .edge-thickness-thick{stroke-width:3.5px;}#mermaid-rmt .edge-pattern-solid{stroke-dasharray:0;}#mermaid-rmt .edge-thickness-invisible{stroke-width:0;fill:none;}#mermaid-rmt .edge-pattern-dashed{stroke-dasharray:3;}#mermaid-rmt .edge-pattern-dotted{stroke-dasharray:2;}#mermaid-rmt .marker{fill:#A1A1A1;stroke:#A1A1A1;}#mermaid-rmt .marker.cross{stroke:#A1A1A1;}#mermaid-rmt svg{font-family:inherit;font-size:16px;}#mermaid-rmt p{margin:0;}#mermaid-rmt .label{font-family:inherit;color:#E5E5E5;}#mermaid-rmt .cluster-label text{fill:#3387a3;}#mermaid-rmt .cluster-label span{color:#3387a3;}#mermaid-rmt .cluster-label span p{background-color:transparent;}#mermaid-rmt .label text,#mermaid-rmt span{fill:#E5E5E5;color:#E5E5E5;}#mermaid-rmt .node rect,#mermaid-rmt .node circle,#mermaid-rmt .node ellipse,#mermaid-rmt .node polygon,#mermaid-rmt .node path{fill:transparent;stroke:#A1A1A1;stroke-width:1px;}#mermaid-rmt .rough-node .label text,#mermaid-rmt .node .label text,#mermaid-rmt .image-shape .label,#mermaid-rmt .icon-shape .label{text-anchor:middle;}#mermaid-rmt .node .katex path{fill:#000;stroke:#000;stroke-width:1px;}#mermaid-rmt .rough-node .label,#mermaid-rmt .node .label,#mermaid-rmt .image-shape .label,#mermaid-rmt .icon-shape .label{text-align:center;}#mermaid-rmt .node.clickable{cursor:pointer;}#mermaid-rmt .root .anchor path{fill:#A1A1A1!important;stroke-width:0;stroke:#A1A1A1;}#mermaid-rmt .arrowheadPath{fill:#0b0b0b;}#mermaid-rmt .edgePath .path{stroke:#A1A1A1;stroke-width:2.0px;}#mermaid-rmt .flowchart-link{stroke:#A1A1A1;fill:none;}#mermaid-rmt .edgeLabel{background-color:transparent;text-align:center;}#mermaid-rmt .edgeLabel p{background-color:transparent;}#mermaid-rmt .edgeLabel rect{opacity:0.5;background-color:transparent;fill:transparent;}#mermaid-rmt .labelBkg{background-color:rgba(0, 0, 0, 0.5);}#mermaid-rmt .cluster rect{fill:#CC785C;stroke:hsl(15, 12.3364485981%, 48.0392156863%);stroke-width:1px;}#mermaid-rmt .cluster text{fill:#3387a3;}#mermaid-rmt .cluster span{color:#3387a3;}#mermaid-rmt div.mermaidTooltip{position:absolute;text-align:center;max-width:200px;padding:2px;font-family:inherit;font-size:12px;background:#CC785C;border:1px solid hsl(15, 12.3364485981%, 48.0392156863%);border-radius:2px;pointer-events:none;z-index:100;}#mermaid-rmt .flowchartTitleText{text-anchor:middle;font-size:18px;fill:#E5E5E5;}#mermaid-rmt rect.text{fill:none;stroke-width:0;}#mermaid-rmt .icon-shape,#mermaid-rmt .image-shape{background-color:transparent;text-align:center;}#mermaid-rmt .icon-shape p,#mermaid-rmt .image-shape p{background-color:transparent;padding:2px;}#mermaid-rmt .icon-shape rect,#mermaid-rmt .image-shape rect{opacity:0.5;background-color:transparent;fill:transparent;}#mermaid-rmt .label-icon{display:inline-block;height:1em;overflow:visible;vertical-align:-0.125em;}#mermaid-rmt .node .label-icon path{fill:currentColor;stroke:revert;stroke-width:revert;}#mermaid-rmt :root{--mermaid-font-family:inherit;}CollectionDetectionTriageInvestigationIncident ResponseContinuous Improvement
Collection — جمع البيانات
جمع كل الـ logs والـ events من الشبكة، الـ endpoints، والـ cloud. لو البيانات مش موجودة — مش هتشوف الهجوم.
Detection — الاكتشاف
من بين آلاف الـ events، نطلع اللي يستحق التحقيق. بيتعمل عن طريق rules، analytics، وـ threat intel.
Triage — الترتيب حسب الأهمية
مش كل الـ alerts تساوي بعض. المحلل لازم يحدد: إيه الأخطر؟ إيه اللي يحتاج تدخل دلوقتي؟
Investigation — التحقيق
هل ده هجوم حقيقي؟ لو أيه — إيه حجمه؟ إيه تأثيره؟
Incident Response — الاستجابة
احتواء، استئصال، استعادة، وتوثيق.

وظائف Core vs Auxiliary
Core SOCAuxiliary / SpecialtyData CollectionThreat IntelligenceDetectionForensicsTriage & InvestigationVulnerability ManagementIncident ResponsePenetration Testing / Red Team
The SOC as a System
الفكرة الجوهرية: الـ SOC هو نظام له inputs وoutputs.
Input: ما حدث في البيئة + كيف تبدو الهجمات
Output: حوادث مُكتشفة ومحتواة ومعالجة

[!danger]
"Garbage in, garbage out" — لو بياناتك رديئة أو ناقصة، detection أيًا كان جودة أدواتك ستكون محدودة.


المعلومات الحيوية التي يجب أن تكون دائماً أمامك {#critical-info}
من أكثر الأخطاء الشائعة في SOC: محلل يبحث عن log ومش لاقيه ويستنتج إن الحادثة ما صرتش — لأنه ما يعرفش إن اللوج ده ما بيتجمعش أصلاً.
الـ SOC لازم يكون عنده:

Network Diagram — مبسط لكن يوضح تدفق الحركة
Points of Visibility — فين الـ taps، الـ span ports، الـ PCAP collectors
Log Flow Diagram — اللوجات مجية منين وبتروح فين
Incident Response Plan — إيه الخطوات لما حاجة غلط
Communication Plan — مين اللي لازم تتصل بيه ومتى
Critical Assets List — إيه الأنظمة والبيانات الأهم


[!danger]
لو مش عندك هذه الوثائق — ابدأ بإنشائها قبل أي شيء آخر. التحقيق بدون خريطة شبكة ولا خطة استجابة يعني تضييع وقت ثمين وقت الأزمة.


وثائق الـ SOC التي يجب أن تعرفها {#documents}
في SOC، هتواجه أنواع مختلفة من الوثائق، ومهم تفرق بينهم:
النوعالغرضإلزامي؟Policy"ماذا يجب أن يُفعل" — اتجاه عام✅ نعمStandard"كيف يُفعل" — تفاصيل إضافية✅ نعمProcedureخطوات تفصيلية لمهمة محددة✅ نعمGuidelineتوصيات وأفضل الممارسات❌ اختياريBaselineقائمة إعدادات محددة جداً — مثل CIS Benchmarks✅ غالباًPlaybook / Use Caseخطوات SOC المحددة للتحقيق في نوع حادثة✅ في SOC

[!info]
الـ Playbook في SOC هو أداة التناسق — يضمن إن كل المحللين يتعاملوا مع نفس نوع الحادثة بنفس المنهجية، بغض النظر عن خبرتهم.


Metrics — كيف يُقاس أداؤك {#metrics}
هنا في حقيقة مؤلمة: أنت ستُحكم عليك بالأرقام التي تنتجها — حتى لو كانت تلك الأرقام لا تعكس الواقع.
لذا من المهم جداً إن تعرف إيه اللي يصنع Metric جيد:

مرتبط بهدف — مش مجرد رقم سهل القياس
قابل للتصرف بناءً عليه — في threshold واضح ونتيجة محددة
قابل للتكرار — لو اتنين قاسوه، هيطلعوا نفس الرقم
يتحدث بشكل متكرر وآلي — مش بيكلّف ساعات من العمل اليدوي


[!warning]
السؤال المهم: "لو الـ metric ده بقى أحسن — هل الأمان اتحسن فعلاً؟" لو الإجابة "مش بالضرورة" — فهذا مؤشر خاطئ.

مثال: "عدد الـ tickets المغلقة" مش بالضرورة مؤشر جيد، لأنه يمكن تحسينه بإغلاق tickets بشكل سطحي.

Key Takeaways {#key-takeaways}

الـ SOC يقوم على ثلاث ركائز: People, Process, Technology — أي خلل في واحدة يؤثر على الكل
الـ SOC Charter هو الوثيقة التي تعطي الـ SOC صلاحية العمل وتحدد نطاقه
Risk Appetite يحدده البيزنس، مش الـ SOC — دورك التوضيح والتوصية، مش الفرض
الاختراق سيحدث — السؤال هو مدى سرعة الاكتشاف وحجم الضرر
الـ SOC هو نظام: بيانات جيدة + threat intel = اكتشاف أفضل
فرّق بين Core SOC وAuxiliary Functions — وافهم إين أنت فيهم
الـ Metrics الغلط تضر أكثر مما تنفع — تحداها لو مش واقعية
Tiered و Tierless ليسا صواباً أو خطأً — كل منهما محسّن لسياق مختلف
