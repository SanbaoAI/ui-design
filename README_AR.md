# ui-design

[English](./README_EN.md) | [中文](./README.md) | العربية

Sanbao UI Design هي مجموعة من مهارات (Skills) تصميم المنتجات وواجهات المستخدم الخاصة بـ Codex. لا تنتقل مباشرة من فكرة غامضة إلى صورة مصممة، بل تبدأ بتوضيح متطلبات المنتج أولاً، ثم توليد لوحة تصميم متعددة الصفحات، ولا تنتقل إلى إنشاء HTML عالي الدقة إلا بعد موافقة المستخدم على التصميم.

## المهارات (Skills)

يحتوي هذا المستودع على مهارتين متكاملتين:

- `sanbao-product-manager`: مهارة إدارة المنتج. توضح positioning المنتج، والمستخدمين المستهدفين، والتدفقات الأساسية، والصفحات من المستوى الأول والثاني، ونطاق MVP، والحالات الحدية، ومعايير القبول.
- `sanbao-ui-design`: مهارة تصميم واجهات المستخدم والتسليم. تولد لوحات تصميم متعددة الصفحات بأسلوب iOS SwiftUI أو Element UI بعد تأكيد خطة المنتج، ثم تنتج نماذج HTML عالية الدقة بعد موافقة المستخدم على التصميم.

التدفق الموصى به:

```text
فكرة المنتج
-> sanbao-product-manager يوضح المتطلبات
-> المستخدم يؤكد خطة المنتج
-> sanbao-ui-design يولد لوحة تصميم واجهة المستخدم
-> المستخدم يؤكد لوحة التصميم
-> توليد HTML عالي الدقة للتسليم
```

## هيكل الدليل

```text
.
├── README.md
├── README_EN.md
├── README_AR.md
├── skills/
│   ├── sanbao-product-manager/
│   │   ├── SKILL.md
│   │   ├── agents/
│   │   │   └── openai.yaml
│   │   └── references/
│   │       ├── requirements.md
│   │       ├── product-loop.md
│   │       ├── page-architecture.md
│   │       └── ui-brief.md
│   └── sanbao-ui-design/
│       ├── SKILL.md
│       ├── agents/
│       │   └── openai.yaml
│       └── references/
│           ├── mockup-core.md
│           ├── swiftui.md
│           └── element-ui.md
└── examples/
    └── fitness-checkin/
        ├── index.html
        ├── styles.css
        ├── assets/
        │   └── fitness-checkin-design-board.png
        └── screenshots/
            └── fitness-checkin-html.png
```

## مثال

مشروع نموذجي: تطبيق iOS خفيف لتسجيل حضور اللياقة البدنية.

اتجاه المنتج:

- موجه لمستخدمي اللياقة البدنية اليوميين، وليس لتدريب القوة المعقد.
- تسجيل حضور يومي مع نوع التمرين والمدة والشدة وتتبع المزاج.
- سجل التقويم والتقدم الأسبوعي والأهداف الشخصية وإعدادات التذكير.
- يستخدم لغة iOS SwiftUI الأصلية.

الصفحات:

- `Today`
- `Check In`
- `Check-in Result`
- `Calendar`
- `Activity Detail`
- `Progress`
- `Profile`
- `Goal Settings`

الملفات:

- [examples/fitness-checkin/index.html](./examples/fitness-checkin/index.html): نموذج HTML عالي الدقة
- [examples/fitness-checkin/styles.css](./examples/fitness-checkin/styles.css): أنماط الصفحة
- [examples/fitness-checkin/assets/fitness-checkin-design-board.png](./examples/fitness-checkin/assets/fitness-checkin-design-board.png): لوحة التصميم الأصلية
- [examples/fitness-checkin/screenshots/fitness-checkin-html.png](./examples/fitness-checkin/screenshots/fitness-checkin-html.png): لقطة شاشة نموذج HTML

### نموذج HTML

![Fitness check-in HTML mockup](./examples/fitness-checkin/screenshots/fitness-checkin-html.png)

### لوحة التصميم

![Fitness check-in design board](./examples/fitness-checkin/assets/fitness-checkin-design-board.png)

## طريقة الاستخدام

انسخ المهارات إلى دليل مهارات Codex الخاص بك:

```bash
cp -R skills/sanbao-product-manager ~/.codex/skills/
cp -R skills/sanbao-ui-design ~/.codex/skills/
```

ابدأ بتوضيح المنتج:

```text
Use $sanbao-product-manager to clarify this app idea into a product plan before UI design.
```

بعد تأكيد خطة المنتج، انتقل إلى تصميم واجهة المستخدم:

```text
Use $sanbao-ui-design to generate a pure iOS SwiftUI multi-screen design board from this confirmed product plan.
```

بعد تأكيد لوحة التصميم، قم بتوليد HTML:

```text
Generate a high-fidelity HTML mockup based on this design board.
```

معاينة المثال:

```bash
open examples/fitness-checkin/index.html
```

ملاحظة: يتطلب `sanbao-ui-design` تأكيد لوحة التصميم قبل توليد HTML. لن ينتقل من فكرة غامضة مباشرة إلى صفحة عالية الدقة.
