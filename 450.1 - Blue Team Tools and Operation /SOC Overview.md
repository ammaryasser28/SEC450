 Overview — نظرة عامة على مركز عمليات الأمن

هدف الوحدة
فهم البنية الأساسية لـ SOC (Security Operations Center)، من مكوناته الثلاثة، إلى هيكله التنظيمي، إلى وظائفه الجوهرية، ومفهوم قياس الأداء.

فهرس المحتويات

مكونات الـ SOC الثلاثة
مهمة الـ SOC — الأسئلة الأربعة
توافق الـ SOC مع المؤسسة
Risk Appetite — مستوى تقبّل المخاطر
حقيقتان لا يتجاهلهما الـ Blue Team
الهيكل التنظيمي للـ SOC
Tiered vs Tierless SOC
وظائف الـ SOC من البداية للنهاية
وثائق يجب أن يعرفها كل محلل
SOC Metrics — قياس الأداء
الخلاصة


1. مكونات الـ SOC الثلاثة
People, Process, Technology — هذا الثلاثي هو أساس أي SOC ناجح.
(تبسيط الفكرة)
تخيل مطعمًا: الطباخون هم الـ People، الوصفات هي الـ Process، والمعدات هي الـ Technology. بدون أي واحد منهم، لن يخرج طبق جيد.

People — الناس
هم قلب الـ SOC. بدون فريق متفاعل ومدرّب، لا شيء يعمل. اختيار الأشخاص المناسبين يمكن أن يصنع الفرق أو يكسر الفريق بأكمله.
Process — العمليات
تحدد ماذا يفعل الناس وكيف يفعلونه. العملية الجيدة تضمن الاتساق والكفاءة.
Technology — التكنولوجيا
تُمكّن العمليات وتضاعف قدرة الفريق. لكن التكنولوجيا ليست بديلًا عن الإنسان — هي أداة تجعله أفضل.

الفكرة هنا: إذا كانت التكنولوجيا قادرة على استبدال المحلل بالكامل، فهذا يعني أن المحلل كان يؤدي مهامًا آلية — وليس تحليلًا حقيقيًا.


2. مهمة الـ SOC — الأسئلة الأربعة
قبل بناء أي SOC، يجب الإجابة على هذه الأسئلة:
السؤالالهدفما الذي نحمي؟تحديد الأصول الحرجةما هي التهديدات؟فهم طبيعة المهاجمينكيف نكتشفها؟بناء قدرات الكشفكيف نستجيب؟تجهيز خطط الاستجابة
ببساطة: كلما كانت إجاباتك أكثر تفصيلًا، كانت قدرتك على الدفاع أعلى. السؤال الأول وحده لا يكفي — يجب تحديد أي بيانات، أين تُخزَّن، ومن يصل إليها.

3. توافق الـ SOC مع المؤسسة
SOC Charter
وثيقة تُعرِّف صلاحيات الـ SOC وحدوده ومهمته العليا. تُحدد:

من يخدم الـ SOC (Constituency)
ما الخدمات التي يقدمها
نطاق عمله

هذه الوثيقة تُشرِّع عمل الفريق وتضمن أن الجميع على نفس الصفحة.

Steering Committee
اجتماعات دورية مع أصحاب المصلحة من الأعمال، تضمن أن الـ SOC يخدم احتياجات المؤسسة الفعلية وليس ما يراه الفريق التقني فقط.

4. Risk Appetite — مستوى تقبّل المخاطر
Risk Appetite هو مقدار المخاطرة التي تقبل بها المؤسسة.
(تبسيط الفكرة)
مثل قيادة السيارة: بعض الناس يقودون ببطء شديد (risk-averse)، وبعضهم بسرعة عالية (high risk tolerance). مهمتك كـ Blue Team أن تفهم كيف تقود مؤسستك.

نوع المؤسسةمستوى تقبّل المخاطرأمثلة على الضبطحكومة / جيشمنخفض جدًاZero Trust، عزل تام، سياسات مشددةشركة ناشئةمرتفعأدوات أساسية، مراقبة بسيطة
دورك كمحلل: تفهم هذا المستوى وتعمل ضمنه — وإذا رأيت خطرًا غير محسوب، تبلغ الإدارة.

Risk Appetite في الواقع
أحيانًا تجد نفسك أمام جهاز يعمل بـ Windows XP يُشغّل خط إنتاج حيوي ولا يمكن تعديله. الحل ليس رفض استخدامه — بل إيجاد Compensating Controls خارجية كأجهزة فحص الشبكة وجدران الحماية الخارجية.

5. حقيقتان لا يتجاهلهما الـ Blue Team
الحقيقة الأولى: الاختراق سيحدث
لا يوجد دفاع مثالي. السؤال ليس "هل سنُخترق؟" بل "متى نكتشف الاختراق وكيف نحدّ من تأثيره؟"

النتيجة الجيدة: المهاجم يدخل، يُكتشف مبكرًا، لا يصل لهدفه
النتيجة السيئة: المهاجم يدخل، يبقى أشهرًا، يسرق البيانات، يُعلن الخرق

هدف الـ Blue Team: الكشف المبكر + تقليل الأضرار.

الحقيقة الثانية: المؤسسة لا تعيش لتكون آمنة فقط
الأمن هو وظيفة "منع الخسارة" مثل حارس الأمن في المتجر. لا يمكنك تفتيش كل عميل عند الدخول — ستُفلس المتجر. التوازن بين الأمن والإنتاجية ضرورة.

6. الهيكل التنظيمي للـ SOC
#mermaid-rut{font-family:inherit;font-size:16px;fill:#E5E5E5;}@keyframes edge-animation-frame{from{stroke-dashoffset:0;}}@keyframes dash{to{stroke-dashoffset:0;}}#mermaid-rut .edge-animation-slow{stroke-dasharray:9,5!important;stroke-dashoffset:900;animation:dash 50s linear infinite;stroke-linecap:round;}#mermaid-rut .edge-animation-fast{stroke-dasharray:9,5!important;stroke-dashoffset:900;animation:dash 20s linear infinite;stroke-linecap:round;}#mermaid-rut .error-icon{fill:#CC785C;}#mermaid-rut .error-text{fill:#3387a3;stroke:#3387a3;}#mermaid-rut .edge-thickness-normal{stroke-width:1px;}#mermaid-rut .edge-thickness-thick{stroke-width:3.5px;}#mermaid-rut .edge-pattern-solid{stroke-dasharray:0;}#mermaid-rut .edge-thickness-invisible{stroke-width:0;fill:none;}#mermaid-rut .edge-pattern-dashed{stroke-dasharray:3;}#mermaid-rut .edge-pattern-dotted{stroke-dasharray:2;}#mermaid-rut .marker{fill:#A1A1A1;stroke:#A1A1A1;}#mermaid-rut .marker.cross{stroke:#A1A1A1;}#mermaid-rut svg{font-family:inherit;font-size:16px;}#mermaid-rut p{margin:0;}#mermaid-rut .label{font-family:inherit;color:#E5E5E5;}#mermaid-rut .cluster-label text{fill:#3387a3;}#mermaid-rut .cluster-label span{color:#3387a3;}#mermaid-rut .cluster-label span p{background-color:transparent;}#mermaid-rut .label text,#mermaid-rut span{fill:#E5E5E5;color:#E5E5E5;}#mermaid-rut .node rect,#mermaid-rut .node circle,#mermaid-rut .node ellipse,#mermaid-rut .node polygon,#mermaid-rut .node path{fill:transparent;stroke:#A1A1A1;stroke-width:1px;}#mermaid-rut .rough-node .label text,#mermaid-rut .node .label text,#mermaid-rut .image-shape .label,#mermaid-rut .icon-shape .label{text-anchor:middle;}#mermaid-rut .node .katex path{fill:#000;stroke:#000;stroke-width:1px;}#mermaid-rut .rough-node .label,#mermaid-rut .node .label,#mermaid-rut .image-shape .label,#mermaid-rut .icon-shape .label{text-align:center;}#mermaid-rut .node.clickable{cursor:pointer;}#mermaid-rut .root .anchor path{fill:#A1A1A1!important;stroke-width:0;stroke:#A1A1A1;}#mermaid-rut .arrowheadPath{fill:#0b0b0b;}#mermaid-rut .edgePath .path{stroke:#A1A1A1;stroke-width:2.0px;}#mermaid-rut .flowchart-link{stroke:#A1A1A1;fill:none;}#mermaid-rut .edgeLabel{background-color:transparent;text-align:center;}#mermaid-rut .edgeLabel p{background-color:transparent;}#mermaid-rut .edgeLabel rect{opacity:0.5;background-color:transparent;fill:transparent;}#mermaid-rut .labelBkg{background-color:rgba(0, 0, 0, 0.5);}#mermaid-rut .cluster rect{fill:#CC785C;stroke:hsl(15, 12.3364485981%, 48.0392156863%);stroke-width:1px;}#mermaid-rut .cluster text{fill:#3387a3;}#mermaid-rut .cluster span{color:#3387a3;}#mermaid-rut div.mermaidTooltip{position:absolute;text-align:center;max-width:200px;padding:2px;font-family:inherit;font-size:12px;background:#CC785C;border:1px solid hsl(15, 12.3364485981%, 48.0392156863%);border-radius:2px;pointer-events:none;z-index:100;}#mermaid-rut .flowchartTitleText{text-anchor:middle;font-size:18px;fill:#E5E5E5;}#mermaid-rut rect.text{fill:none;stroke-width:0;}#mermaid-rut .icon-shape,#mermaid-rut .image-shape{background-color:transparent;text-align:center;}#mermaid-rut .icon-shape p,#mermaid-rut .image-shape p{background-color:transparent;padding:2px;}#mermaid-rut .icon-shape rect,#mermaid-rut .image-shape rect{opacity:0.5;background-color:transparent;fill:transparent;}#mermaid-rut .label-icon{display:inline-block;height:1em;overflow:visible;vertical-align:-0.125em;}#mermaid-rut .node .label-icon path{fill:currentColor;stroke:revert;stroke-width:revert;}#mermaid-rut :root{--mermaid-font-family:inherit;}SOC LeadAnalysts Tier1/2/3Detection EngineeringIncident ResponseEngineering & InfraSOC-AdjacentThreat IntelligenceForensicsVuln ManagementRed Team
لا يوجد هيكل "صحيح" واحد — كل مؤسسة تختار ما يناسب احتياجاتها وحجمها.

7. Tiered vs Tierless SOC
المعيارTiered SOCTierless SOCالهيكلTier 1 → 2 → 3الجميع يعمل معًاالمرونةمحدودةعاليةالتعلمبطيء (قيود)سريع (حرية)الاتساقعالٍيحتاج انضباطًا ذاتيًاخطر الاستنزافمرتفع (بسبب الملل)أقل
ببساطة: لا نموذج أفضل بشكل مطلق — كل منهما يُحسِّن جانبًا مختلفًا.

8. وظائف الـ SOC من البداية للنهاية
#mermaid-ruu{font-family:inherit;font-size:16px;fill:#E5E5E5;}@keyframes edge-animation-frame{from{stroke-dashoffset:0;}}@keyframes dash{to{stroke-dashoffset:0;}}#mermaid-ruu .edge-animation-slow{stroke-dasharray:9,5!important;stroke-dashoffset:900;animation:dash 50s linear infinite;stroke-linecap:round;}#mermaid-ruu .edge-animation-fast{stroke-dasharray:9,5!important;stroke-dashoffset:900;animation:dash 20s linear infinite;stroke-linecap:round;}#mermaid-ruu .error-icon{fill:#CC785C;}#mermaid-ruu .error-text{fill:#3387a3;stroke:#3387a3;}#mermaid-ruu .edge-thickness-normal{stroke-width:1px;}#mermaid-ruu .edge-thickness-thick{stroke-width:3.5px;}#mermaid-ruu .edge-pattern-solid{stroke-dasharray:0;}#mermaid-ruu .edge-thickness-invisible{stroke-width:0;fill:none;}#mermaid-ruu .edge-pattern-dashed{stroke-dasharray:3;}#mermaid-ruu .edge-pattern-dotted{stroke-dasharray:2;}#mermaid-ruu .marker{fill:#A1A1A1;stroke:#A1A1A1;}#mermaid-ruu .marker.cross{stroke:#A1A1A1;}#mermaid-ruu svg{font-family:inherit;font-size:16px;}#mermaid-ruu p{margin:0;}#mermaid-ruu .label{font-family:inherit;color:#E5E5E5;}#mermaid-ruu .cluster-label text{fill:#3387a3;}#mermaid-ruu .cluster-label span{color:#3387a3;}#mermaid-ruu .cluster-label span p{background-color:transparent;}#mermaid-ruu .label text,#mermaid-ruu span{fill:#E5E5E5;color:#E5E5E5;}#mermaid-ruu .node rect,#mermaid-ruu .node circle,#mermaid-ruu .node ellipse,#mermaid-ruu .node polygon,#mermaid-ruu .node path{fill:transparent;stroke:#A1A1A1;stroke-width:1px;}#mermaid-ruu .rough-node .label text,#mermaid-ruu .node .label text,#mermaid-ruu .image-shape .label,#mermaid-ruu .icon-shape .label{text-anchor:middle;}#mermaid-ruu .node .katex path{fill:#000;stroke:#000;stroke-width:1px;}#mermaid-ruu .rough-node .label,#mermaid-ruu .node .label,#mermaid-ruu .image-shape .label,#mermaid-ruu .icon-shape .label{text-align:center;}#mermaid-ruu .node.clickable{cursor:pointer;}#mermaid-ruu .root .anchor path{fill:#A1A1A1!important;stroke-width:0;stroke:#A1A1A1;}#mermaid-ruu .arrowheadPath{fill:#0b0b0b;}#mermaid-ruu .edgePath .path{stroke:#A1A1A1;stroke-width:2.0px;}#mermaid-ruu .flowchart-link{stroke:#A1A1A1;fill:none;}#mermaid-ruu .edgeLabel{background-color:transparent;text-align:center;}#mermaid-ruu .edgeLabel p{background-color:transparent;}#mermaid-ruu .edgeLabel rect{opacity:0.5;background-color:transparent;fill:transparent;}#mermaid-ruu .labelBkg{background-color:rgba(0, 0, 0, 0.5);}#mermaid-ruu .cluster rect{fill:#CC785C;stroke:hsl(15, 12.3364485981%, 48.0392156863%);stroke-width:1px;}#mermaid-ruu .cluster text{fill:#3387a3;}#mermaid-ruu .cluster span{color:#3387a3;}#mermaid-ruu div.mermaidTooltip{position:absolute;text-align:center;max-width:200px;padding:2px;font-family:inherit;font-size:12px;background:#CC785C;border:1px solid hsl(15, 12.3364485981%, 48.0392156863%);border-radius:2px;pointer-events:none;z-index:100;}#mermaid-ruu .flowchartTitleText{text-anchor:middle;font-size:18px;fill:#E5E5E5;}#mermaid-ruu rect.text{fill:none;stroke-width:0;}#mermaid-ruu .icon-shape,#mermaid-ruu .image-shape{background-color:transparent;text-align:center;}#mermaid-ruu .icon-shape p,#mermaid-ruu .image-shape p{background-color:transparent;padding:2px;}#mermaid-ruu .icon-shape rect,#mermaid-ruu .image-shape rect{opacity:0.5;background-color:transparent;fill:transparent;}#mermaid-ruu .label-icon{display:inline-block;height:1em;overflow:visible;vertical-align:-0.125em;}#mermaid-ruu .node .label-icon path{fill:currentColor;stroke:revert;stroke-width:revert;}#mermaid-ruu :root{--mermaid-font-family:inherit;}CollectionDetectionTriageInvestigationIncident ResponseContinuous Improvement
الوظيفةالوصفCollectionجمع البيانات الأمنية من الشبكة والأجهزةDetectionتحديد الأنشطة المشبوهة من البياناتTriageترتيب التنبيهات حسب الأولوية والخطورةInvestigationالتحقيق في التنبيه لتأكيده أو رفضهIncident Responseالاحتواء والاستئصال والتعافي

الوظائف المساندة (Auxiliary)

Threat Intelligence: جمع معلومات عن المهاجمين لتعزيز الكشف
Forensics: تحليل ما حدث بعد الاختراق بتفصيل عميق
Self-Assessment: فحص الثغرات، Red Teaming، مراقبة الإعدادات


9. وثائق يجب أن يعرفها كل محلل
الوثيقةالصفةالهدفPolicyإلزاميةتحدد "ماذا" يجب فعلهStandardإلزاميةتحدد "كيف" وبأي قدرProcedureإلزاميةخطوات تفصيلية لتنفيذ المهمةGuidelineاختياريةتوصيات وأفضل الممارساتBaselineمرجعيةقائمة إعدادات تفصيلية (مثل CIS Benchmarks)Playbook / Use Caseتشغيليةقواعد كشف + خطوات استجابة خاصة بالـ SOC

10. SOC Metrics — قياس الأداء
Metrics هي الأرقام التي تُقاس بها فعالية الـ SOC.
الفكرة هنا: مجرد أن رقمًا يمكن قياسه لا يعني أنه مفيد.
خصائص الـ Metric الجيد:

مشتق من هدف حقيقي — وليس رقمًا لأجل الرقم
قابل للتنفيذ — يوجد حد واضح للتدخل عنده
محدد وقابل للتكرار — شخصان مختلفان يصلان لنفس النتيجة
يُجمَع تلقائيًا وبشكل متكرر — لا يضيف عبئًا يدويًا


اسأل نفسك دائمًا: "إذا تحسّن هذا الرقم، هل الأمن فعلًا تحسّن؟"


11. الخلاصة

Key Takeaways

الـ SOC يقوم على ثلاثة ركائز: People, Process, Technology — لا يمكن الاستغناء عن أي منها
مهمة الـ SOC تبدأ بالإجابة على أربعة أسئلة جوهرية: ماذا نحمي، من يهاجمنا، كيف نكشف، كيف نستجيب
SOC Charter يُشرّع عمل الفريق، وSteering Committee يضمن توافقه مع الأعمال
Risk Appetite يختلف من مؤسسة لأخرى — مهمة الـ Blue Team العمل ضمنه وليس ضده
الاختراق سيحدث — الهدف هو الكشف المبكر وتقليل الأضرار
لا يوجد هيكل تنظيمي "أفضل" للـ SOC — كل نموذج يُحسِّن جانبًا مختلفًا
الـ Metrics الجيدة مرتبطة بأهداف حقيقية وقابلة للتنفيذ — وليست مجرد أرقام
