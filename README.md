# BeePlayer

منصة BeePlayer لتشغيل قوائم IPTV (M3U/M3U8) على كل الشاشات: الويب، الجوال، صناديق Android، وأجهزة التلفاز الذكية.

## مكونات المشروع

| المجلد | المنصة | التقنية المقترحة |
|---|---|---|
| `apps/web` | منصة الويب: الموقع التسويقي ولوحات المدير والموزع والعميل (beeplayer1.com) | Next.js (App Router) + API على NestJS |
| `apps/mobile` | تطبيق الجوال: Android و iOS و Apple TV | React Native (Expo) مع دعم tvOS |
| `apps/android-box` | تطبيق مخصص لصناديق Android TV / Android Box | Kotlin + Jetpack Compose for TV + Media3 ExoPlayer |
| `apps/lg-webos` | تطبيق تلفاز LG | webOS (HTML/JS) + hls.js |
| `apps/samsung-tizen` | تطبيق تلفاز Samsung | Tizen Web App (HTML/JS) + AVPlay |
| `packages/shared` | كود مشترك: عميل الـ API، تحليل M3U و EPG، الأنواع، الترجمة | TypeScript |

## المبادئ المشتركة
- واجهة خلفية واحدة (`api.beeplayer1.com`) لكل التطبيقات.
- تفعيل الجهاز بـ MAC + key، كما في بوابة العميل الحالية.
- دعم العربية (RTL) والإنجليزية في كل التطبيقات.
- تحليل M3U و EPG في `packages/shared` لتستخدمه تطبيقات الويب والجوال والتلفاز (webOS و Tizen).

## الوثائق
- [خارطة الطريق](docs/ROADMAP.md)
- [تقرير اختبار الموقع، 14 نوفمبر 2026](docs/reports/site-test-report-2026-11-14.md)

## البدء
كل تطبيق داخل `apps/` له ملف README خاص بطريقة التشغيل والبناء.
