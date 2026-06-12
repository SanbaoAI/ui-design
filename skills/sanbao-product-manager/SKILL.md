---
name: sanbao-product-manager
description: Clarify app, SaaS, tool, or feature ideas into product requirements before UI design or implementation. Use when the user asks to design a product, app, feature flow, UI, prototype, PRD, MVP, information architecture, user journey, page structure, or product closure. This skill must analyze goals, users, scenarios, core objects, first-level and second-level pages, task flows, MVP scope, edge states, and acceptance criteria before any image generation or HTML mockup work begins.
---

# Sanbao Product Manager

## Core Rule

Do product thinking before design production. Do not generate UI images, HTML mockups, or implementation code until the product requirement has been clarified enough to define a complete user loop.

When the user's request is broad, infer a reasonable first version, but clearly mark assumptions and open questions. Ask only the few questions that materially change the product direction.

## Workflow

1. Read `references/requirements.md` to clarify intent, users, scenarios, and constraints.
2. Read `references/product-loop.md` to define the core object, user loop, primary flows, edge states, and product closure.
3. Read `references/page-architecture.md` to produce first-level and second-level page inventory.
4. Read `references/ui-brief.md` when handing the result to a UI design skill such as `$sanbao-ui-design`.
5. Present the PM output for user confirmation before design generation.

## Output Shape

For product design requests, produce:

- Product positioning: one sentence.
- Target users and scenarios.
- Core problem and product promise.
- Core objects and data.
- MVP scope and non-goals.
- First-level pages.
- Second-level pages.
- Key user flows.
- Edge states and empty states.
- Success metrics or acceptance criteria.
- Open questions.
- UI design brief, only after the requirement is coherent enough.

Keep the output practical and decision-oriented. Do not bury the user in theory.

## Confirmation Gate

After producing the PM output, stop and ask the user to confirm, revise, or answer the open questions. Proceed to UI design only after the user confirms the product plan or explicitly asks to continue with the current assumptions.

If the user says "先出图", "直接设计", or similar, still provide the minimum PM analysis first unless they have already supplied a clear PRD or page inventory.

## Quality Bar

A product plan is not ready for UI design if it only contains top-level tabs or generic pages such as Home, Search, Progress, and Profile. It must include the second-level task, detail, edit, confirmation, result, and settings screens needed to complete the product's main loop.

Prefer a smaller complete loop over a larger shallow product.

## References

- `references/requirements.md`: requirement clarification and assumptions.
- `references/product-loop.md`: product closure and task-flow design.
- `references/page-architecture.md`: first-level and second-level page inventory.
- `references/ui-brief.md`: handoff format for UI design.
