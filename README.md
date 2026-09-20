# 🎮 RAW GAME — PS4 Exploit & Jailbreak Host

<p align="center">
  <img src="photo_2026-05-31_13-18-03.jpg" alt="RAW GAME Logo" width="120" style="border-radius: 50%; box-shadow: 0 4px 20px rgba(0,0,0,0.5);" />
</p>

<p align="center">
  <b>مستضيف ثغرات وبكج جيلبريك بلايستيشن 4 فائق السرعة مع دعم كامل للكاش أوفلاين وحقن الحمولات التلقائي.</b><br>
  <i>Ultra-fast, offline-cached PS4 WebKit & Kernel Exploit Host with automated payload injection.</i>
</p>

<p align="center">
  <a href="https://github.com/raw13g/raw13g.github.io"><img src="https://img.shields.io/badge/Original%20Repo-raw13g%2Fraw13g.github.io-blue?style=for-the-badge&logo=github" alt="Original Repository"></a>
  <img src="https://img.shields.io/badge/Platform-PlayStation%204-003791?style=for-the-badge&logo=playstation" alt="Platform PS4">
  <img src="https://img.shields.io/badge/Offline-100%25%20Cached-success?style=for-the-badge" alt="Offline Ready">
  <img src="https://img.shields.io/badge/License-MIT%20%2F%20Research-green?style=for-the-badge" alt="License">
</p>

---

## 📌 نبذة عن المشروع | Overview

**RAW GAME Host** هو مستضيف ثغرات (Exploit Host) متكامل وموجّه لأجهزة **PlayStation 4**. تم تصميمه بهندسة برمجية نظيفة تعتمد على السرعة، الاستقرار العالي، وتقليل احتمالية انهيار النظام (Kernel Panic).

يقوم المستضيف باكتشاف إصدار نظام التشغيل (Firmware) تلقائياً، وإنشاء مساحة ذاكرة أولية (Memory Primitive RW) عبر ثغرة WebKit، ثم تصعيد الصلاحيات وتطبيق تصحيحات الكيرنل (Kernel Patches) المناسبة وتمرير حمولة (Payload) الـ HEN / GoldHEN تلقائياً إلى الذاكرة دون أي تدخل يدوي.

> 🌟 **المطور وصاحب المشروع الأصلي:**  
> تم تطوير ونشر هذا المشروع أساساً بواسطة المطور **[raw13g](https://github.com/raw13g)**  
> 🔗 المستودع الأصلي: [https://github.com/raw13g/raw13g.github.io](https://github.com/raw13g/raw13g.github.io)

---

## ✨ المميزات الرئيسية | Key Features

- ⚡ **تخزين مؤقت كامل (100% Offline AppCache):** بفضل ملف `cache.appcache`، يمكنك فتح المستضيف لمرة واحدة فقط وسيعمل لاحقاً بدون إنترنت نهائياً.
- 🎯 **كشف ذكي وتلقائي للإصدار (Smart FW Detection):** يقرأ الـ User-Agent ويحدد بدقة رقم التحديث العشري ويطابقه مع جدول الإزاحات (Offsets Table).
- 🛡️ **استقرار وثبات عالي (Safe Retry & Benign Miss Handling):** نظام إعادة محاولة آمن قبل لمس ذاكرة الكيرنل لتفادي الـ Panic وإعادة التشغيل الإجباري.
- 🚀 **حقن تلقائي للحمولة (Automatic Payload Delivery):** حقن وتفعيل حمولة `payload2.bin` (HEN) فور نجاح تصحيح الكيرنل.
- 🎨 **واجهة مستخدم احترافية وخفيفة:** واجهة داكنة مريحة للعين وسريعة الاستجابة بأقل استهلاك لموارد المتصفح.
- 🔍 **أدوات تصحيح متقدمة (Built-in Debugger & Logger):** يدعم خيارات سريعة عبر عنوان الرابط لعرض السجلات وتتبع خطوات الاستغلال تفصيلياً.

---

## 📊 جدول التوافق والأنظمة المدعومة | Compatibility Matrix

يحتوي ملف `ps4_offsets.js` على عناوين وإزاحات دقيقة مقاسة على الأجهزة:

| التحديث (Firmware) | حالة الدعم (Status) | تصحيح الكيرنل (Kernel Patch) | الحمولة (Payload) |
|:---:|:---:|:---:|:---:|
| **13.52** | ✅ مدعوم ومُختبر على العتاد (Hardware Proven) | `patches/1352.bin` | `payload2.bin` |
| **13.50** | ✅ مدعوم ومقاس بالكامل (Measured RVAs) | `patches/1350.bin` | `payload2.bin` |
| **13.04** | ✅ مدعوم (نفس كيرنل 13.02) | `patches/1302.bin` | `payload2.bin` |
| **13.02** | ✅ مدعوم ومُختبر على العتاد (Hardware Proven) | `patches/1302.bin` | `payload2.bin` |
| **12.50 / 12.52** | 🔬 مدمج في جدول الإزاحات (Corroborated) | `patches/1250.bin` | متاح اختياري |
| **12.00 / 12.02** | 🔬 مدمج في جدول الإزاحات (Verified Dumps) | `patches/1200.bin` | متاح اختياري |
| **11.50** | 🔬 مدمج في جدول الإزاحات (Proven Step4q) | — | متاح اختياري |
| **11.00** | 🔬 مدمج في جدول الإزاحات (Proven Step4q) | — | متاح اختياري |

> ℹ️ **ملاحظة:** الإصدارات من 13.02 حتى 13.52 مفعلة بالتشغيل التلقائي المباشر في `index.html`. بالنسبة لبقية التحديثات يمكنك تشغيلها بنقرة زر أو باستخدام معامل `?force=1`.

---

## 🕹️ طريقة الاستخدام على جهاز PS4 | How to Use

1. **إعداد المتصفح:**
   - افتح متصفح الإنترنت في جهاز PS4.
   - اضغط على زر `OPTIONS` واختر **حذف ملفات تعريف الارتباط (Clear Cookies)** و **مسح بيانات التصفح (Clear Website Data)** لضمان بدء جلسة نظيفة.
2. **زيارة الصفحة:**
   - اكتب رابط المستضيف في المتصفح، مثلاً:
     ```text
     https://raw13g.github.io
     ```
   - أو عنوان الـ IP المحلي إذا كنت تشغله عبر شبكتك المنزلية.
3. **تثبيت الكاش (Offline Cache):**
   - ستظهر لك رسالة تفيد بتنزيل وتخزين الملفات (`cached` أو `offline -- from cache`).
4. **تشغيل الجيلبريك:**
   - سيبدأ المستغل فوراً بالعمل وستظهر دائرة التحميل.
   - انتظر ثوانٍ معدودة حتى تكتمل المراحل وتتم ترقية الصلاحيات وتشغيل الـ HEN.
   - عند الانتهاء بنجاح، ستظهر لك إشعار أو رسالة تفيد بإتمام العملية ويمكنك الخروج من المتصفح والتمتع بالصلاحيات الكاملة!

---

## 🛠️ خيارات وعوامل التتبع والتشغيل المتقدمة | URL Query Parameters

يمكنك تمرير وسائط في نهاية الرابط داخل المتصفح للتحكم بسلوك المستضيف وفحص الأخطاء:

| المعامل (Parameter) | الوصف (Description) | مثال على الاستخدام |
|---|---|---|
| `?log=1` | تفعيل شاشة السجلات الكاملة بالخطوات خطوة بخطوة بدلاً من شاشة الانتظار | `jb.html?log=1` |
| `?verbose=1` | عرض التفاصيل البرمجية الكاملة للرسائل بدون تقليص النصوص | `jb.html?log=1&verbose=1` |
| `?force=1` | إجبار المستضيف على العمل حتى لو كان إصدار الجهاز غير مدرج بقائمة التفعيل المباشر | `index.html?force=1` |
| `?payload=0` | تشغيل ثغرة الكيرنل وتطبيق الباتش بدون تمرير حمولة `payload2.bin` | `jb.html?payload=0` |
| `?stop=beforedouble` | التوقف قبل مرحلة مضاعفة كائنات الذاكرة (لأغراض التطوير والفحص) | `jb.html?log=1&stop=beforedouble` |

---

## 💻 الاستضافة الذاتية والتشغيل المحلي | Self-Hosting Guide

إذا أردت استضافة الموقع بنفسك على خادم محلي، هاتف، أو خوادم GitHub:

### 1. عبر GitHub Pages (الأسهل مجاناً):
1. قم بعمل **Fork** للمستودع الأصلي: [raw13g/raw13g.github.io](https://github.com/raw13g/raw13g.github.io).
2. اذهب إلى إعدادات المستودع الخاص بك **Settings** > **Pages**.
3. اختر الفرع `main` ثم المجلد `/ (root)` واضغط **Save**.
4. سيمنحك GitHub رابطاً جاهزاً للتشغيل على جهازك مباشرة.

### 2. التشغيل محلياً عبر بايثون (Local Python Server):
قم بفتح الطرفية (Terminal / PowerShell) داخل مجلد المشروع ونفذ:
```bash
# Python 3
python -m http.server 8080
```
ثم ادخل من متصفح الـ PS4 إلى الرابط:
`http://[IP-الكمبيوتر]:8080`

### 3. التشغيل عبر Node.js:
```bash
npx serve -l 8080
```

---

## 📂 هيكلية ملفات المشروع | Project Structure

```text
├── index.html          # صفحة الترحيب، فحص التحديث، والتحقق من الكاش
├── jb.html             # واجهة تشغيل الجيلبريك وعرض حالات التحميل والسجلات
├── jb.js               # المحرك الرئيسي للاستغلال وحقن الباتشات والحمولة
├── core.js             # ثغرة الـ WebKit وبناء الـ Primitive RW
├── mem.js              # عمليات قراءة وكتابة الذاكرة وإدارتها
├── int64.js            # مكتبة التعامل مع العمليات الحسابية 64-bit في JavaScript
├── ps4_offsets.js      # جداول الإزاحات ومواقع دوال الكيرنل لكل تحديث
├── rpc_worker.js       # مشغّل خلفي للعمليات المزامنة عبر Web Workers
├── cache.appcache      # ملف المانيفست للتخزين المؤقت دون اتصال
├── payload2.bin        # حمولة الـ HEN المجهزة للإرسال
├── patches/            # تصحيحات الكيرنل المخصصة للتحديثات (1302, 1350, 1352...)
└── preview.png / logo  # الصور وشعارات الواجهة
```

---

## 🤝 حقوق المشروع والشكر والتقدير | Credits & Acknowledgements

- **صاحب المشروع والمستودع الأصلي:**
  - **[raw13g](https://github.com/raw13g)** — الرابط الأصلي: [github.com/raw13g/raw13g.github.io](https://github.com/raw13g/raw13g.github.io)
- مجتمع باحثي أمن وحماية نظام PS4 والمطورين المشاركين في توفير الإزاحات وتطوير الثغرات ومكتبات WebKit و FreeBSD Kernel Exploits.

---

## ⚠️ إخلاء مسؤولية | Disclaimer

> هذا المشروع مخصص **للأغراض التعليمية والبحثية واختبارات الأمان وحفظ المشتريات الشرعية فقط**. الاستخدام غير المصرح به أو التعديل على جهازك يقع على مسؤوليتك الخاصة بالكامل. المطورون غير مسؤولين عن أي استخدام خاطئ أو ضرر يلحق بجهازك.
