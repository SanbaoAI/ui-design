# ui-design

[English](./README_EN.md) | [العربية](./README_AR.md) | 中文

Sanbao UI Design 是一组给 Codex 使用的产品与 UI 设计 Skill。它的目标不是直接从一句模糊需求跳到出图，而是先把产品需求梳理清楚，再生成多页面 UI 设计图，并在用户确认后继续生成高保真 HTML handoff。

## Skill 功能

这个仓库包含两个配套 Skill：

- `sanbao-product-manager`：产品经理前置 Skill。负责梳理产品定位、目标用户、核心流程、一级/二级页面、MVP 范围、边界状态和验收标准。
- `sanbao-ui-design`：UI 设计 handoff Skill。负责在产品方案确认后生成 iOS SwiftUI 或 Element UI 风格的多页面设计图，并在用户确认设计图后继续生成 HTML 高保真 mockup。

推荐流程：

```text
产品想法
-> sanbao-product-manager 梳理需求
-> 用户确认产品方案
-> sanbao-ui-design 生成 UI 设计图
-> 用户确认设计图
-> 生成 HTML 高保真 handoff
```

## 目录结构

```text
.
├── README.md
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

## 生成示例

示例项目：轻量综合健身打卡 iOS App。

产品方向：

- 面向日常健身用户，不做复杂力量训练记录。
- 支持每日健身打卡、运动类型、时长、强度、心情记录。
- 支持日历历史、周进度、个人目标和提醒设置。
- 使用 iOS SwiftUI 原生视觉语言。

示例页面：

- `Today`
- `Check In`
- `Check-in Result`
- `Calendar`
- `Activity Detail`
- `Progress`
- `Profile`
- `Goal Settings`

示例文件：

- [examples/fitness-checkin/index.html](./examples/fitness-checkin/index.html)：高保真 HTML mockup
- [examples/fitness-checkin/styles.css](./examples/fitness-checkin/styles.css)：页面样式
- [examples/fitness-checkin/assets/fitness-checkin-design-board.png](./examples/fitness-checkin/assets/fitness-checkin-design-board.png)：原始设计图
- [examples/fitness-checkin/screenshots/fitness-checkin-html.png](./examples/fitness-checkin/screenshots/fitness-checkin-html.png)：HTML 效果图

### HTML 效果图

![Fitness check-in HTML mockup](./examples/fitness-checkin/screenshots/fitness-checkin-html.png)

### 原始设计图

![Fitness check-in design board](./examples/fitness-checkin/assets/fitness-checkin-design-board.png)

## 怎么使用

把 Skill 复制到 Codex 的 Skill 目录：

```bash
cp -R skills/sanbao-product-manager ~/.codex/skills/
cp -R skills/sanbao-ui-design ~/.codex/skills/
```

先做产品梳理：

```text
Use $sanbao-product-manager to clarify this app idea into a product plan before UI design.
```

产品方案确认后，再做 UI 设计：

```text
Use $sanbao-ui-design to generate a pure iOS SwiftUI multi-screen design board from this confirmed product plan.
```

设计图确认后，再生成 HTML：

```text
按这个设计图生成 HTML 高保真 mockup。
```

预览示例：

```bash
open examples/fitness-checkin/index.html
```

注意：`sanbao-ui-design` 会要求先确认设计图，再生成 HTML。它不会把一个模糊想法直接跳到高保真页面。
