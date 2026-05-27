# Process Work Rules

Use this file only when processing `raw/work/inbox/` or pasted work material.

## Source Handling

A single inbox note may contain multiple unrelated items. Split it into distinct items first, then route each item to the correct product, task, decision, concept, pattern, or triage destination.

Read the raw note fully before writing anything. Preserve distinct sections, examples, tables, callouts, and explicit reasoning. Compress only literal duplicates.

If the note contains embedded images (`![[...png]]`, `![[...jpg]]`, etc.), read each image before marking the note processed unless the user explicitly says to skip it.

Work attachments should live in `raw/work/assets/`. If an inbox note refers to files in `raw/work/inbox/assets/` or another note-local assets folder, move or de-duplicate those attachments into `raw/work/assets/`, update the markdown links to the canonical asset path, and remove stale duplicate asset folders after verifying no active note references them.

PDFs are valid work sources. Read or extract the PDF before processing, and preserve important tables, screenshots, decisions, and tasks.

## Processing Steps

1. Read `work/Work Index.md`.
2. Read `work/tracking/Work Inbox Index.md`.
3. Process only unprocessed files from `raw/work/inbox/` or pasted work content.
4. Identify the parent and sub-product for each item. If unclear, use `work/tracking/Work Needs Triage.md`.
5. Create or update concepts, decisions, patterns, and tasks as needed.
6. Read `rules/work/Work Formats.md` before creating or changing page/task formats.
7. Move processed raw work files to `raw/work/processed/` after the outputs are updated.
8. Update all affected indexes, dashboards, and logs.

## Concepts

Concepts are reusable product/UX/system understanding: features, workflows, behaviours, system interactions, JTBDs, product rules, UX understanding.

- Preserve all source content that changes meaning or helps future retrieval.
- Add structure when the source is sparse, but do not invent unsupported behaviour.
- Keep sub-concepts as sections unless the page is long and the sub-concepts are parallel enough to stand alone.
- Link related concepts only when genuinely useful.

## Decisions

Decisions are explicit product/design decisions: "we chose X over Y, and here is why."

- Preserve reasoning, tradeoffs, context, and usage guidance only if present in the source.
- If reasoning is absent, prefer adding the observation to a concept page instead of creating an inferred decision.
- Mark superseded decisions as `superseded` instead of deleting them.

## Patterns

Patterns are recurring behaviours emerging across repeated decisions or concepts.

- Do not force a pattern from a single example.
- If new evidence contradicts an existing pattern, note the conflict on the pattern page.
- Check `work/patterns/Patterns Index.md` before creating a new pattern.

## Tasks

Create or update a task only when the source has a checkbox, says task/todo/action item, or the user explicitly asks.

Checked tasks in a source or task page should be treated as completed during the next processing pass. Preserve task IDs and source links.

## Update Checklist

| File | When to update |
|---|---|
| `work/tracking/Work Inbox Index.md` | Every processed raw work file |
| `work/Work Index.md` | Product status, product count, or task count changes |
| `work/tasks/Work Tasks.md` | Open/blocked/completed tasks change |
| `work/tasks/Work Task History.md` | Tasks are added, completed, or meaningfully changed |
| Sub-product Index/Tasks | That sub-product changes |
| `work/patterns/Patterns Index.md` | Patterns change |
| `work/tracking/Work Needs Triage.md` | Ownership or action is unclear |
| `work/tracking/Work Log.md` | Every work processing pass |

## Conflict Rules

- Concepts show current understanding. Update in place; flag inferred reasoning explicitly.
- Decisions preserve history. Mark old decisions as `superseded` instead of deleting them.
- Patterns flag conflicts when new behaviour contradicts an existing pattern.
- Task history is append-only.
