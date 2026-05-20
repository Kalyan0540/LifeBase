# Work Inbox Index

Tracks files in `raw/work/inbox/` so the LLM can process only new work material.

When processing a raw note, output may land in any combination of `Concepts/`, `Decisions/`, `Patterns/`, or the sub-product `Tasks` file. Annotate each linked output with its type in the Output column.

---

## Processed

| Raw File | Processed | Product | Output |
|---|---:|---|---|
| `raw/work/inbox/Custom Variable Creation - Text Output.md` | 2026-05-18 | [[Cross Tabs - Index]] | [[Custom Variable - Text Output]] (concept), [[Custom Variable Creation]] (concept), [[Cross Tabs - Tasks]] (tasks) |
| `raw/work/inbox/Custom Variable Creation - Number Output.md` | 2026-05-18 | [[Cross Tabs - Index]] | [[Custom Variable - Number Output]] (concept), [[Custom Variable Creation]] (concept), [[Cross Tabs - Tasks]] (tasks) |
| `raw/work/inbox/Custom Variable Creation - Variable Output.md` | 2026-05-18 | [[Cross Tabs - Index]] | [[Custom Variable - Variable Output]] (concept), [[Custom Variable Creation]] (concept), [[Cross Tabs - Tasks]] (tasks) |
| `raw/work/inbox/Enlyta Discussion.md` | 2026-05-20 | [[Cross Tabs - Index]] | [[Run and Save Flow]] (concept), [[Run Before Save]] (decision), [[Variable Creation Scope]] (decision), [[Custom Variable Creation]] (concept update) |
| `raw/work/inbox/Today's meeting notes.md` | 2026-05-20 | [[Cross Tabs - Index]], [[AI Summarisation - Index]], [[Work Needs Triage]] | [[Cross Tabs - Tasks]] (3 tasks: TASK-2026-05-20-001–003), [[AI Summarisation - Tasks]] (3 tasks: TASK-2026-05-20-004–006), [[Work Needs Triage]] (3 Common Components tasks) |

---

## Unprocessed

| Raw File | Added | Type | Product Guess | Status | Notes |
|---|---:|---|---|---|---|
| _No unprocessed work inbox files_ | - | - | - | - | - |



---

## Status Values

| Status | Meaning |
|---|---|
| unprocessed | Raw file has not been processed into work memory yet |
| processed | Raw file has been processed and linked to generated work pages |
| needs-triage | Product or action is unclear; item should be routed to [[Work Needs Triage]] |
