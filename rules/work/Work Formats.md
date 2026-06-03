# Work Formats

Use this file only when creating or updating work pages or tasks.

## Concept Page

```yaml
---
type: concept
---
```

Footer:

```md
---

*Sources: [[Source Page]]*
*Updated: YYYY-MM-DD*
```

## Decision Page

```yaml
---
type: decision
status: accepted
---
```

Allowed statuses: `accepted`, `inferred`, `superseded`, `proposed`.

Footer:

```md
---

*Sources: [[Source Page]]*
*Updated: YYYY-MM-DD*
```

If a decision comes from pasted user input and no source file exists yet, first create a processed source note in `raw/work/processed/` containing the input. Link the decision footer to that processed source page, not to a generic source label.

## Pattern Page

```yaml
---
type: pattern
tags: [ProductA, ProductB]
---
```

Tags use parent product names exactly, such as `Catalyst`, `Enlyta`, or `AI`.

Footer:

```md
---

*Applies to: Catalyst - AI Summarisation · Enlyta - Cross Tabs*
*Sources: [[Source Page]]*
*Updated: YYYY-MM-DD*
```

## Task Format

Visible task text contains the action and useful links. Trailing inline metadata uses backticks:

```md
- [ ] Update filter journeys for the confirmation dialogue. `P0` `TASK-YYYY-MM-DD-001`
```

Inline tokens:

- `P0` / `P1` / `P2` / `P3` - priority
- `TASK-YYYY-MM-DD-NNN` - task ID
- `completed YYYY-MM-DD` - completion date for checked items

Use a `<details>` block only when a task needs longer notes that would clutter the line.

If a source task has explicit subtasks, keep them as indented checklist items below the parent task. Do not merge subtask text into the parent task.

## Task Dashboard

In `work/tasks/Work Tasks.md`, group tasks under headings that link directly to the sub-product index.

```md
### [[Cross Tabs - Index|Cross Tabs]]

- [ ] Render Table designs. `P0` `TASK-2026-05-18-007`
```

Task wording should not repeat the product name when the heading already provides the product context.
