# Product Loop

## Definition

A complete product loop lets the user enter the product, perform the core action, receive feedback, review history or progress, and return with a reason to repeat the action.

Minimum closed-loop does not mean the fewest top-level pages. It means the fewest screens required for the user to complete the job end to end.

## Define The Core Object

Name the object the product is organized around:

- Fitness app: workout, exercise, set, goal, body metric.
- CRM: lead, account, opportunity, task, note.
- Course product: lesson, plan, assignment, progress record.
- Finance tool: transaction, budget, account, report.

Every important page should create, inspect, modify, summarize, or organize one of these objects.

## Flow Template

Describe the main flow:

1. Entry: where the user starts.
2. Intent selection: what they choose to do.
3. Creation or action: what they create, log, edit, buy, review, or complete.
4. Feedback: what confirms progress or outcome.
5. Detail and correction: how they inspect or fix the result.
6. History or analytics: how they understand progress over time.
7. Configuration: what preferences or goals affect future loops.

## States

Include states that materially affect design:

- Empty state.
- In-progress state.
- Success or completion state.
- Error or validation state.
- Permission or integration state.
- Loading state for data-heavy systems.

Do not overproduce states, but include the ones needed to make the flow credible.

## Acceptance Criteria

Write practical criteria:

- A user can complete the core action without leaving the product.
- A user can review what happened after the action.
- A user can change key inputs or settings that affect the next loop.
- The UI has enough data to demonstrate real usage, not only placeholders.
