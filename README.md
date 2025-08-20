# Manga-Script-Generator
.generat script youtub
كيفية تشغيل مشروع Manga Script Generator
نظرة عامة
هذا المشروع هو تطبيق Python يحول مقاطع فيديو YouTube إلى سيناريوهات مانجا باستخدام الذكاء الاصطناعي. يتضمن واجهة مستخدم رسومية ويدعم تنزيل مقاطع الفيديو وتحويلها إلى صور ونصوص.

المتطلبات الأساسية
1. تثبيت Python
تأكد من تثبيت Python 3.8 أو إصدار أحدث على نظامك
تحقق من التثبيت عبر الأمر: python --version أو python3 --version
2. تثبيت FFmpeg
يجب تثبيت FFmpeg لمعالجة الفيديو والصوت
للنظام Windows: قم بتنزيل FFmpeg من الموقع الرسمي وقم بإضافته إلى متغير البيئة PATH
للأنظمة الأخرى: استخدم مدير الحزم (مثل apt، brew، إلخ)
خطوات التثبيت والتشغيل
1. استنساخ المشروع
git clone <رابط_المشروع>
cd manga-script-generator

bash


2. إنشاء بيئة افتراضية (موصى به)
python -m venv venv
# Windows:
venv\Scripts\activate
# Linux/Mac:
source venv/bin/activate

bash


3. تثبيت المتطلبات
pip install -r requirements.txt

bash


4. إعداد ملف البيئة
انسخ ملف .env.example إلى ملف جديد باسم .env وقم بتعديل القيم حسب الحاجة:

cp .env.example .env

bash


5. تشغيل التطبيق
python run.py

bash


المشكلات المحتملة أثناء التنزيل والتثبيت
1. أخطاء في تثبيت المتطلبات
رسالة الخطأ: "Could not find a version that satisfies the requirement"

الحل: تأكد من أنك تستخدم Python 3.8 أو إصدار أحدث، وقم بتحديث pip:

pip install --upgrade pip

bash


رسالة الخطأ: "Microsoft Visual C++ 14.0 is required"

الحل: قم بتثبيت Microsoft C++ Build Tools أو Visual Studio مع دعم C++

2. مشاكل في تثبيت FFmpeg
رسالة الخطأ: "ffmpeg not found" أو "command not found"
الحل: تأكد من تثبيت FFmpeg وإضافته إلى متغير البيئة PATH بشكل صحيح
3. أخطاء في تنزيل YouTube
رسالة الخطأ: "Video unavailable" أو "Age restricted"

الحل: تأكد من أن رابط الفيديو صحيح وغير مقيد بحسب العمر، وقم بتحديث مكتبة pytube:

pip install --upgrade pytube

bash


رسالة الخطأ: "Too Many Requests"

الحل: انتظر بعض الوقت ثم حاول مرة أخرى، أو استخدم VPN لتغيير عنوان IP

4. مشاكل في استخدام Google Gemini API
رسالة الخطأ: "API key not set" أو "Invalid API key"
الحل: تأكد من الحصول على مفتاح API من Google Gemini وإضافته إلى ملف .env
5. أخطاء في معالجة الصور
رسالة الخطأ: "No module named 'PIL'"
الحل: قم بتثبيت مكتبة Pillow:
pip install Pillow

bash


6. أخطاء في تشغيل التطبيق
رسالة الخطأ: "ModuleNotFoundError"
الحل: تأكد من تثبيت جميع المتطلبات المدرجة في ملف requirements.txt
استخدام التطبيق
1. الواجهة الرئيسية
بعد تشغيل التطبيق، افتح المتصفح وانتقل إلى العنوان:

http://localhost:5000

txt


2. إدخال رابط YouTube
أدخل رابط فيديو YouTube الذي ترغب في تحويله إلى سيناريو مانجا.

3. معالجة الفيديو
انتظر حتى يتم تنزيل الفيديو ومعالجته إلى صور وتقطيعها.

4. إنشاء السيناريو
استخدم واجهة المستخدم لإنشاء السيناريو بناءً على الصور المقطعة.

ملاحظات إضافية
تأكد من وجود مساحة كافية على القرص لتخزين الفيديوهات والصور
قد يستغرق معالجة الفيديوهات الطويلة وقتًا أطول
احفظ ملفات السيناريو المُنشأة في مجلد data/scripts/
يمكن تعديل إعدادات التطبيق في ملف .env حسب الحاجة
إيقاف التطبيق
لإيقاف التطبيق، اضغط على Ctrl+C في نافذة الأوامر حيث يعمل التطبيق.
