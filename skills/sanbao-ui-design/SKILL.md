---
name: sanbao-ui-design
description: Analyze product requirements, define a closed-loop page flow with first-level and second-level screens, generate one multi-screen UI design board, and create confirmation-gated HTML mockups and Figma handoff assets for native iOS SwiftUI screens and Element UI/Element Plus web interfaces. Use when the user asks Codex to design an app, product UI, full feature flow, high-fidelity mockup, HTML/CSS handoff, Figma-importable assets, SwiftUI-native interface, or Element UI web interface. The workflow must analyze requirements and page coverage before image generation, must design all core first-level and second-level pages in one image board when starting from a product idea, and must pause for user confirmation after the design image before generating HTML unless the user supplies an already-approved design.
---

# UI Design Handoff

## Core Rule

Use a three-stage workflow:

1. Analyze the product requirement and define the smallest closed-loop page flow, including both first-level navigation pages and second-level task/detail/result pages. If the requirement is not already clear, use `$sanbao-product-manager` first.
2. Generate or refine one design image board containing all core pages in that flow.
3. Stop and ask for explicit user confirmation before creating HTML, CSS, screenshots, or Figma handoff assets.

Do not proceed from image to HTML based only on implied approval. Continue only after the user says the design is approved, confirmed, ready, or otherwise clearly asks to generate the implementation from that design.

## Workflow

1. Identify the target platform:
   - Use `references/swiftui.md` for iOS native SwiftUI screens.
   - Use `references/element-ui.md` for Element UI or Element Plus web interfaces.
   - Use both when the user asks for parallel native and web versions.
2. Read `references/mockup-core.md` for the shared product analysis, multi-screen design board, confirmation, mockup, and handoff process.
3. Summarize the product goal, target user, core jobs, first-level pages, second-level pages, and closed-loop page set before image generation.
4. Generate one design image board first when no approved visual exists. The board should include all core pages needed for the product loop, not only home or top-level tab pages.
5. Present the image board and ask the user to confirm or request changes.
6. After confirmation, generate the HTML mockup using the selected platform rules.
7. Verify the mockup with browser screenshots at the relevant viewport sizes.
8. Provide final deliverables: source image, HTML/CSS or app files, screenshot(s), and Figma handoff guidance or importable assets.

## Platform Selection

For SwiftUI requests, prioritize native iOS semantics over web styling. Use SF Symbols and SwiftUI component vocabulary in the design spec and any code. The HTML mockup is only a visual handoff artifact; it must not redefine the product as a web app.

For Element UI requests, prioritize actual Element UI or Element Plus component semantics. Use dense, operational layouts for admin, SaaS, CRM, dashboards, and internal tools.

When the user asks for a "subskill", treat SwiftUI and Element UI as platform branches within this skill. Load only the reference file needed for the current branch.

## Figma Handoff

Do not claim that a local script can reliably convert arbitrary HTML into a native `.fig` file. Figma files and node graphs are not a simple public HTML serialization target.

Acceptable handoff paths:

- Generate HTML and use a Figma import plugin such as an HTML-to-Figma plugin.
- Export SVG or PDF snapshots and import them into Figma as editable or semi-editable assets.
- If a Figma plugin, MCP tool, or Figma API integration is available, create Figma nodes through that integration.
- Generate structured design specs that a Figma plugin can consume.

If the user explicitly asks for a script, explain that a script can prepare assets or plugin input, but it should not be represented as a guaranteed HTML-to-`.fig` converter.

## References

- `references/mockup-core.md`: shared confirmation, HTML mockup, screenshot validation, and Figma handoff workflow.
- `references/swiftui.md`: iOS native design constraints, SF Symbols, SwiftUI controls, and SwiftUI code guidance.
- `references/element-ui.md`: Element UI and Element Plus design constraints, components, and web prototype guidance.
