# ROAMO — الموقع الكامل

نسخة 24 سبتمبر 2026. تشمل الكود، الصور، الخطوط وملفات التحميل، وإصلاح المسافة بين «التفاصيل الصغيرة».

## النشر على GitHub وVercel
1. فك ضغط الملف. ارفع محتوياته إلى جذر مستودع GitHub جديد (يمكن أن يكون Private). ارفع مجلد dist وملف vercel.json كما هما، وليس ملف ZIP نفسه.
2. في Vercel اختر Add New → Project ثم استورد المستودع.
3. Framework Preset: Other. Root Directory: جذر المستودع. Output Directory: dist. Build Command: فارغ. لا تحتاج Environment Variables أو تثبيت حزم.
4. اضغط Deploy. ملف vercel.json يحدد مجلد النشر مسبقًا.
5. افتح رابط الإنتاج في نافذة خاصة للتأكد من وصول الزوار دون تسجيل دخول. إذا كانت حماية الإنتاج مفعلة في حسابك، ألغِ حماية تسجيل الدخول لبيئة Production من Settings → Deployment Protection.

## ربط roamo.omdastudios.art
1. داخل مشروع Vercel افتح Settings → Domains وأضف roamo.omdastudios.art.
2. افتح لوحة DNS التي تدير سجلات omdastudios.art.
3. أضف سجل CNAME: الاسم roamo، والقيمة هي الهدف الذي يعرضه Vercel لهذا المشروع تحديدًا. TTL: Auto أو القيمة الافتراضية.
4. لا تغيّر سجلات @ أو www أو البريد ولا تحتاج إلى نقل Nameservers.
5. انتظر ظهور Valid Configuration وتفعيل HTTPS في Vercel. إذا طلب سجل TXT للتحقق من الملكية، أضف القيمة المعروضة حرفيًا.

## التعديل والتحديث
- dist/index.html: النصوص وأقسام الموقع وروابط التحميل.
- dist/style.css: الألوان والخطوط والتنسيقات المتجاوبة.
- dist/script.js: التفاعلات والحركة.
- dist/assets/: صور وشعارات وخطوط الموقع.
- dist/downloads/: الملفات التي ينزلها الزوار.
- بعد استيراد المشروع، دفع التغييرات إلى فرع الإنتاج في GitHub ينشر التحديث عبر Vercel.
- تحديث أصول العلامة يدوي: استبدل الملف المعتمد وحدّث رابطه عند تغيير الاسم. هذه النسخة لا تتصل تلقائيًا بمصدر الملفات.

الموقع static مستقل؛ لا يحتاج ChatGPT أو خادم خلفي أو مفاتيح API. الملفات الأصلية القابلة للتحرير هي HTML وCSS وJavaScript.

مراجع:
https://vercel.com/docs/project-configuration/vercel-json
https://vercel.com/docs/domains/working-with-domains/add-a-domain
