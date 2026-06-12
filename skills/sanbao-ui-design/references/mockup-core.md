# Shared Product-To-Mockup Workflow

## Intake

Start by analyzing the product, not by drawing one screen. Collect or infer the details needed to define a usable product loop:

- Product or feature type
- Target user and primary job
- Platform branch: SwiftUI, Element UI, or both
- Visual direction if supplied: serious, playful, premium, utility, editorial, data-dense, etc.
- Required content, states, and brand constraints
- Core object being created, tracked, reviewed, or managed
- Primary user loop: entry, action, feedback, history, and return
- First-level navigation destinations
- Second-level task, detail, edit, confirmation, result, and settings screens

If the user is vague, make conservative assumptions and proceed with a small but complete product loop instead of blocking.

If `$sanbao-product-manager` is available and the user has not already confirmed a product plan, run that product-management workflow before generating any design image.

## Stage 0: Product Analysis

Before generating any image, provide a concise analysis with:

- Product goal: what the product helps the user accomplish.
- Target user: who uses it and in what situation.
- Core loop: the repeatable flow that makes the product useful.
- First-level pages: the main navigation destinations.
- Second-level pages: the task, detail, edit, confirmation, result, and configuration screens required to complete the loop.
- Page inventory: the minimum complete set of screens needed for that loop.
- Key data: the realistic content, metrics, entities, and states shown in the UI.
- Platform choice: SwiftUI, Element UI, or both.

For a new app concept, do not design only a homepage. Choose enough pages to make the product feel closed-loop.

Minimum closed-loop means the fewest screens that make the product usable from start to finish. It does not mean only first-level pages or only tab destinations. A valid loop must include enough second-level depth for the user to create, inspect, edit, confirm, and review the core object.

Closed-loop page coverage usually includes:

- Entry or dashboard page.
- Create, capture, or log page.
- Detail page for the core object.
- Editing or configuration page for the core object when users must adjust inputs.
- Confirmation, summary, or result page after the main action.
- History, progress, list, or analytics page.
- Profile, settings, or preference page when it materially affects the loop.
- Empty, success, or in-progress state when important to understand the product.

For very small tools, 4-5 screens can be enough if at least one second-level task/detail page is present. For normal mobile apps, prefer 7-9 screens: 3-4 first-level pages plus 3-5 second-level task/detail/result pages. For admin systems, prefer 7-10 screens covering list, filter, detail, create/edit, review, batch action, and settings/permissions when relevant.

Before image generation, reject shallow inventories that contain only Home, Search, Progress, Profile, Dashboard, or similar first-level pages. Add the missing second-level pages.

Show the analysis to the user before or together with the image prompt. If assumptions are significant, name them briefly.

## Stage 1: Design Image

Generate a raster UI design board first unless the user has already supplied an approved visual. The image should show all core screens on one canvas, not a single homepage, marketing hero, or abstract mood board.

The board should be structured as a product design presentation:

- Multiple device frames or page artboards in one image.
- Each page labeled with a short screen name.
- First-level and second-level screens visibly mixed in the board.
- A visible left-to-right or top-to-bottom product flow.
- Consistent component system, typography, spacing, and icon style across pages.
- Realistic data that demonstrates the product loop.

For mobile apps, show 7-9 iPhone screens by default unless the product is extremely simple. For Element UI admin tools, show 7-10 desktop page states or panels in one board.

When writing the image prompt:

- Specify the target device or viewport.
- Specify the component system and its visual language.
- Include realistic content and data.
- Name every screen that should appear on the board.
- Mark each screen as first-level or second-level in the planning notes, even if the image labels stay short.
- Describe how the screens form a closed product loop.
- Avoid decorative-only composition.
- Avoid UI controls that conflict with the selected platform reference.

After generating the image board, stop. Ask the user whether to approve it, revise it, add/remove pages, or generate another direction.

## Confirmation Gate

Proceed to HTML only when the user clearly confirms the design board or provides an already-approved image. Examples of sufficient confirmation include:

- "确认"
- "继续"
- "按这个生成 HTML"
- "这个可以"
- "Use this design"
- "Approved"

If the user asks for revisions, revise the image/spec first and keep the gate closed.

## Stage 2: HTML Mockup

After confirmation, build a high-fidelity HTML mockup that visually matches the approved design board while respecting the selected platform branch.

HTML requirements:

- Use stable responsive dimensions for fixed-format surfaces such as iPhone frames, tables, toolbars, tab bars, and controls.
- Keep text inside its container at mobile and desktop sizes.
- Use real content instead of placeholder filler where possible.
- Use icons consistent with the selected platform.
- Implement the full approved page set, not just the first screen.
- Preserve the product loop in navigation and visible state transitions.
- Avoid nested cards and decorative page-section cards.
- Avoid large marketing heroes unless the requested product is a landing page.
- Keep the mockup usable as a handoff artifact: organized DOM, readable CSS, and named sections.

Verification:

- Run a local preview when needed.
- Capture browser screenshots for the target viewport(s).
- Check for text overflow, overlapping controls, blank images, missing icons, and layout drift.
- Iterate until the screenshot matches the approved intent closely enough for handoff.

## Deliverables

Provide the user with the generated files and a short note describing:

- The approved source design board used.
- The page set implemented.
- The HTML or app entry point.
- Screenshot path(s).
- Any Figma handoff assets or next-step instructions.

## Figma Handoff Reality

Do not promise direct `.fig` generation from HTML. A local script can help with:

- Exporting screenshots.
- Exporting SVG or PDF.
- Packaging images and CSS tokens.
- Producing JSON or metadata for a Figma plugin.

A reliable Figma conversion needs one of these:

- A Figma import plugin that reads the live HTML page.
- A custom Figma plugin that constructs nodes from a structured spec.
- A Figma API or MCP integration exposed to Codex.

When no Figma integration is available, provide the cleanest import path: HTML preview plus PNG/SVG/PDF assets and concise import instructions.
