# SwiftUI Native Branch

Use this branch for iOS native app screens, SwiftUI design systems, iPhone mockups, Apple-style UI, and requests for SwiftUI code.

## Design Priorities

- Design for native iOS first, not a web app squeezed into an iPhone frame.
- Use SwiftUI-native component vocabulary and iOS platform conventions.
- Use SF Symbols for icons. Prefer valid symbol concepts such as `house`, `magnifyingglass`, `bell`, `person.crop.circle`, `plus`, `chevron.right`, `square.and.arrow.up`, `heart`, `star`, `calendar`, `chart.bar`, `slider.horizontal.3`, and `gearshape`.
- Use iOS system typography, hierarchy, safe areas, navigation bars, tab bars, sheets, lists, forms, and grouped sections.
- Respect touch targets and platform spacing. Primary controls should feel tappable and not web-dense.
- Avoid arbitrary custom icon packs, web-style sidebars, browser tables, hover-only affordances, and CSS-only control inventions unless the user asks for a custom visual language.

## SwiftUI Component Vocabulary

Prefer these patterns when specifying or implementing screens:

- App structure: `NavigationStack`, `TabView`, `NavigationSplitView` when appropriate.
- Lists and forms: `List`, `Form`, `Section`, grouped rows, disclosure rows.
- Navigation and actions: `.toolbar`, `ToolbarItem`, `Menu`, `Button`, `EditButton`.
- Input controls: `TextField`, `SecureField`, `TextEditor`, `Searchable`, `Picker`, `DatePicker`, `Toggle`, `Slider`, `Stepper`.
- Presentation: `.sheet`, `.fullScreenCover`, `.popover`, `Alert`, `confirmationDialog`.
- Visual containers: `ScrollView`, `LazyVStack`, `Grid`, `LazyVGrid`, `safeAreaInset`.
- System styling: `.buttonStyle`, `.controlSize`, `.listStyle`, `.navigationTitle`, `.symbolRenderingMode`.

## Image Prompt Guidance

For design images, create one multi-screen iOS design board. Include:

- "native iOS SwiftUI app screen"
- "multi-screen product design board"
- iPhone model or viewport, such as "iPhone 15 Pro portrait"
- "SF Symbols icons"
- Specific native controls, such as "TabView bottom tab bar", "NavigationStack large title", "grouped List sections", or "native sheet"
- 7-9 labeled iPhone screens that cover the product loop, including second-level task/detail/result screens
- Real content and data relevant to the product

Avoid phrases that pull the model toward web UI, such as "landing page", "HTML dashboard", "Bootstrap", "Material UI", or "web admin".

For new mobile app ideas, do not generate only a Today, Home, or Dashboard screen. Include the screens needed to complete and repeat the user's core job. A typical SwiftUI board may include:

- First-level: Dashboard or Today
- First-level: History, list, calendar, or progress screen
- First-level: Profile, goals, or settings screen
- Second-level: Create, log, or capture flow
- Second-level: Detail screen for the core object
- Second-level: Edit or configuration screen
- Second-level: Success, summary, or active-session state
- Second-level: Settings detail when preferences materially affect the loop

## HTML Mockup Guidance

The HTML mockup should visually emulate the approved native iOS board, but label it as a visual handoff artifact. It should implement every approved screen and not use non-iOS control semantics in the design spec.

For icons in HTML:

- Prefer SF Symbols references in labels, comments, or metadata when actual SF Symbols are not locally available.
- If rendering substitute icons with a web icon library, keep names mapped to SF Symbols in the code comments or data attributes.
- Do not introduce a visual icon style that changes the meaning of the native design.

## SwiftUI Code Guidance

When generating SwiftUI code after the mockup is approved:

- Use real SwiftUI controls instead of recreating controls with rectangles whenever a native control exists.
- Keep custom drawing limited to brand-specific surfaces, charts, or illustrations.
- Use semantic view names and break large screens into small `View` structs.
- Use realistic preview data and SwiftUI previews.
- Use `Image(systemName:)` for SF Symbols.

If the approved image contains a non-native interaction, translate it to the closest native pattern and mention the translation.
