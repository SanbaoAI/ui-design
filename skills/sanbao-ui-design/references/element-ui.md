# Element UI / Element Plus Branch

Use this branch for web admin, SaaS, CRM, dashboards, back-office tools, and interfaces that should use Element UI or Element Plus component semantics.

## Design Priorities

- Prefer Element Plus for new Vue 3 prototypes; use Element UI vocabulary when the user explicitly targets legacy Vue 2.
- Design operational screens for scanning, filtering, editing, comparing, and repeated daily use.
- Keep layouts dense but calm: clear navigation, strong alignment, compact tables, predictable forms, and restrained color.
- Avoid marketing-page composition, oversized decorative heroes, and purely illustrative dashboards unless the user explicitly asks for a public landing page.
- Use component semantics that map cleanly to Element components.

## Component Vocabulary

Prefer these components and patterns:

- Structure: `el-container`, `el-aside`, `el-header`, `el-main`, `el-menu`, `el-breadcrumb`.
- Data display: `el-table`, `el-table-column`, `el-tag`, `el-progress`, `el-statistic`, `el-empty`, `el-skeleton`.
- Filtering and input: `el-form`, `el-form-item`, `el-input`, `el-select`, `el-date-picker`, `el-cascader`, `el-checkbox`, `el-radio`, `el-switch`, `el-slider`.
- Actions: `el-button`, `el-button-group`, `el-dropdown`, `el-popconfirm`.
- Navigation: `el-tabs`, `el-pagination`, `el-steps`.
- Overlays: `el-dialog`, `el-drawer`, `el-popover`, `el-tooltip`, `el-message`, `el-notification`.
- Feedback: `el-alert`, `el-result`, loading states, validation states.

Use icons from the Element Plus icon set when available. Avoid unrelated icon packs unless the existing project already uses them.

## Image Prompt Guidance

For design images, create one multi-screen or multi-state web design board. Include:

- "Element Plus admin interface" or "Element UI dashboard"
- "multi-page product design board"
- The specific business domain and data objects
- Component names such as table, filter form, drawer, dialog, tabs, pagination, status tags
- 7-10 labeled desktop pages or states that cover the product loop, including second-level detail/create/edit/review states
- Realistic row data and empty/loading/error states when relevant

Avoid mobile-native phrasing such as "SwiftUI", "iOS tab bar", "SF Symbols", or "native iPhone app" unless the user asks for a comparison.

For new admin or SaaS concepts, do not generate only a dashboard. Include the pages or states needed for repeated work. A typical Element Plus board may include:

- First-level: Overview or dashboard
- First-level: List page with filters
- First-level: Analytics or history page
- First-level: Settings, roles, or configuration page when relevant
- Second-level: Detail page or side drawer
- Second-level: Create form
- Second-level: Edit form
- Second-level: Review, approval, confirmation, or batch action state

## HTML Mockup Guidance

For runnable web prototypes:

- Use Element Plus directly when a Vue setup is appropriate.
- If building static HTML only, mirror Element component structure and class naming clearly enough for implementation handoff.
- Implement the full approved page set, not just the dashboard.
- Include realistic table widths, filter bars, pagination, dialogs or drawers, and form validation states when relevant.
- Keep cards for repeated items or framed tools only; do not wrap entire page sections inside decorative cards.
- Use restrained color accents and clear status semantics rather than a one-note palette.

## Handoff Notes

When delivering Element UI work, identify:

- Whether the target is Element UI or Element Plus.
- The Vue version assumption if code is generated.
- The primary components used.
- Any states represented in the mockup, such as loading, empty, selected row, validation error, or drawer open.
