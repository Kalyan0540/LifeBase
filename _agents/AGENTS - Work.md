# LifeBase Work Agent

Rules for operational product memory: products, concepts, decisions, patterns, tasks, and history.

## Purpose

Use `work/` for product and office memory. Keep it separate from the durable knowledge wiki.

Raw work notes live in `raw/work/inbox/`. They can be messy. They do not need frontmatter.

## Structure

```text
raw/work/inbox/                    messy source notes
work/Work Index.md                 master entry point (root level)
work/patterns/                     cross-product patterns
  ├── Patterns Index.md            pattern registry table
  └── [one file per pattern]
work/tasks/                        task tracking
  ├── Work Tasks.md                daily task dashboard
  └── Work Task History.md         chronological task history
work/tracking/                     processing pipeline & ops
  ├── Work Inbox Index.md          processing tracker
  ├── Work Needs Triage.md         unclear product ownership
  └── Work Log.md                  work operation log
work/products/<Parent>/            parent products
```

Products are organised in a two-level hierarchy: **parent → sub-product**. A parent that has only one product can be flattened (no sub-product folder) until additional sub-products appear.

Each sub-product folder follows this shape:

```text
work/products/<Parent>/<Sub-Product>/
├── <Sub-Product> - Index.md     entry point + short intro
├── <Sub-Product> - Tasks.md     open / blocked / completed
├── Concepts/                    one file per concept
└── Decisions/                   one file per decision
```

Current map:

```text
Enlyta/
├── Cross Tabs/
└── Design System/

Catalyst/
└── AI Summarisation/

AI/         (flat: no sub-products yet)
```

When a new product note arrives, route it to the correct sub-product folder. If ownership is unclear, use `work/tracking/Work Needs Triage.md`.

## Core Principles

The system is a **product memory assistant**, not an aggressive documentation generator. It should evolve gradually. Do not over-structure upfront. Do not invent content. Keep concepts, decisions, and patterns scoped to the product they belong to — do not flatten into global folders.

## Concepts

Concepts are reusable product/UX/system understanding: features, workflows, behaviours, system interactions, JTBDs, product rules, UX understanding.

- Framework- and tool-agnostic where possible.
- May contain: use cases, flows, constraints, conditions, examples, edge cases.
- Multiple concept pages per product. One file per concept.
- Attach images when they exist in the source.
- Link to related concepts only when genuinely useful.

### Image Reading Rule

Before marking a raw note as processed, check for embedded images (`![[...png]]`, `![[...jpg]]`). If any exist, read each one using the Read tool — images may contain the primary content of the note (decision tables, annotated UI screenshots, comparison charts). A note is not fully processed until all its images have been read.

**Skip an image only if the user has explicitly said not to read it** (e.g. a comment in the raw note or a direct instruction). Do not skip silently or assume an image is decorative.
- Human-readable first.

### Source Fidelity vs. Elaboration

When raw source material is **detailed** — multiple examples, tables, distinct sections, callouts — preserve all distinct content. Reorganising and rephrasing are fine. Removing content is not, unless it is a literal duplicate within the source. Examples, before/after tables, and named callouts (Expected vs. Current, Common Misunderstanding, Important Clarification, etc.) should survive into the concept page.

When raw source material is **sparse**, elaborate within the framework: surface use cases, conditions, flows, and behaviours the concept implies. Add structure the source doesn't provide if it helps the reader.

**Test** — a reader of the concept page should not feel that context is missing or that a behaviour is unclear. If the source had it, the concept page should reflect it.

### Do Not Infer Reasoning or Behaviour

If a behaviour, reasoning, or claim is not in the source, either leave it out, or mark it explicitly as inferred (`*inferred from X, needs confirmation*`). Never present invented detail as if it came from source.

### Page Structure and Splitting

Sub-concepts default to **sections within a concept page**. Splitting into separate concept files is allowed only when *both* conditions hold:

- the parent page has grown long, **and**
- the sub-concepts are parallel — each has its own complete example flow and stands on its own as a concept

The split must be logical, not arbitrary. Each child page should be coherent without the parent.

When splitting, use a **parent + children** structure:

- **Parent page** — shared mental model, shared behaviour, comparison table across children, open threads, links to children
- **Child page** — full detail of one sub-concept following the source's own arc

**Child page naming.** When child concepts map to raw source notes with similar filenames, give the children slightly different names to avoid Obsidian link collisions. Example: raw `Custom Variable Creation - Text Output` → concept `Custom Variable - Text Output`.

### Deduplication

Consolidate true duplicates:

- Within a single source note, repeated tables or sections can be kept once (e.g., the same comparison table appearing twice).
- Across multiple source notes, the same shared behaviour can move to a Shared Behaviour section in the parent concept (e.g., first-match-wins mentioned in both Text and Number Output sources → state once in the parent).

Never drop content because it *seems* duplicated with something already written. Verify it is the same idea, not just similar wording. When in doubt, keep both.

### Frontmatter and Footer

Frontmatter is minimal:

```yaml
---
type: concept
---
```

Sources and date live at the bottom as a small italicised line:

```md
---

*Sources: [[Source Page 1]] · [[Source Page 2]]*
*Updated: YYYY-MM-DD*
```

## Decisions

Decisions are explicit product/design decisions — "we chose X over Y, and here is why".

- Preserve reasoning, tradeoffs, context, and usage guidance **only if explicitly present in source material**.
- Never invent reasoning. If reasoning is not in source: either omit it, or clearly label it as inferred.
- One file per decision. Multiple decision pages per product.
- Keep lightweight. Not ADR-style.
- Mark superseded decisions as `superseded` instead of deleting them.

Frontmatter:

```yaml
---
type: decision
status: accepted    # accepted | inferred | superseded | proposed
---
```

Sources and date at the bottom:

```md
---

*Sources: [[Source Page]]*
*Updated: YYYY-MM-DD*
```

If the source material does not contain explicit reasoning, prefer adding the observation to the relevant concept page instead of creating an inferred decision.

## Patterns

Patterns are recurring behaviours emerging across repeated decisions or concepts.

- Examples: *Filled buttons for primary actions*, *Confirmation dialogs before destructive changes*, *Explicit execution preferred over auto-trigger for expensive operations*.
- Patterns are **not requirements**. They describe how a product generally behaves.
- They emerge gradually. Do not force a pattern from a single example.
- Flag conflicts when new evidence contradicts an existing pattern. Note the conflict on the pattern page; do not silently overwrite.

### Pattern Location

Patterns live at the **work level** — `work/patterns/` — not at the product or sub-product level. Products and sub-products do not have their own `Patterns/` folders.

When a pattern applies to multiple products, there is **one canonical file** in `work/patterns/`. Add all applicable products to the frontmatter `tags` and the `Applies to` footer line, and update `work/patterns/Patterns Index.md`.

### Pattern Index

`work/patterns/Patterns Index.md` is the cross-product registry. Every pattern must have a row in this table. Columns: Pattern, Description, and one column per parent product (Catalyst, Enlyta, AI, etc.). The product column shows the sub-product name where the pattern is applied, or `—` if not applicable.

When adding a new pattern:
1. Create the pattern file in `work/patterns/`.
2. Add product tags to the frontmatter: `tags: [Catalyst, Enlyta]`.
3. Add a row to `work/patterns/Patterns Index.md`.
4. Update the relevant parent product Index pages (Patterns section).

### Frontmatter

```yaml
---
type: pattern
tags: [ProductA, ProductB]
---
```

Tags use the parent product name exactly (Catalyst, Enlyta, AI) for Obsidian filtering.

Pattern footer includes an `Applies to` line listing products and sub-products:

```md
---

*Applies to: Catalyst — AI Summarisation · Enlyta — Cross Tabs*
*Sources: [[Source Page]]*
*Updated: YYYY-MM-DD*
```

## Source Traceability

Every concept, decision, or pattern page links back to its sources.

Sources may include: raw notes, meeting notes, Figma discussions, chats, screenshots, transcripts.

Keep source links lightweight — a footer line, not a heavy frontmatter block.

## Metadata

Metadata is for the LLM, not the user.

- Frontmatter stays minimal — usually just `type` (plus `status` on decisions, `parent` on sub-product indexes).
- IDs and dates live at the **bottom** of the page (footer line or `<details>` block), never at the top.
- Avoid bulky frontmatter on every page.

## Writing Style

- Human-readable first, LLM-readable second.
- Use simple language close to the user's notes.
- Headings carry context; do not repeat the product name in every task or section.
- Use tables for `Work Index.md` and `Work Inbox Index.md`. Do not make product pages table-only.
- Requirements-style language belongs in concepts. There is no separate Requirements file.

## Task Rules

Create a task only when:

- the raw note has a checkbox
- the note says task, todo, to-do, or action item
- the user explicitly asks to create a task

If a follow-up is only implied, do not add it as a task. Add it as an open question or ask the user.

Task wording should be simple. Do not repeat the product name in the task line — the section heading already provides that context.

Tasks live in `<Sub-Product> - Tasks.md` per product, plus the global `Work Tasks.md` dashboard.

### Task Format

Visible task text contains the action and any useful product/source links. Trailing inline metadata uses backticks:

```md
- [ ] Update filter journeys for the confirmation dialogue. `P0` `TASK-YYYY-MM-DD-001`
```

Inline tokens (any subset, any order):

- `P0` / `P1` / `P2` / `P3` — priority
- `TASK-YYYY-MM-DD-NNN` — task ID
- `completed YYYY-MM-DD` — completion date for checked items

This replaces the older `<details>` metadata block. Use the `<details>` block only when a task needs longer notes that would otherwise clutter the line.

### Task Dashboard

In `Work Tasks.md`, group tasks under headings that hyperlink directly to the sub-product index. The heading carries product context; task lines stay plain.

```md
### [[Cross Tabs - Index|Cross Tabs]]

- [ ] Render Table designs. `P0` `TASK-2026-05-18-007`
```

Avoid:

- Trailing breadcrumbs (`— Enlyta > Cross Tabs`) — heading already provides this.
- Verbose wording.

## Checked Task Processing

When the user checks a task in `Work Tasks.md` or a product task page:

1. Treat it as completed on the next work-processing pass.
2. Move/update it under Completed with `completed YYYY-MM-DD` token.
3. Add a completion entry to `Work Task History.md`.
4. Update the related sub-product task page.
5. Preserve the task ID and source links.

## Work Inbox Processing

When processing work inbox:

1. Read `work/Work Index.md`.
2. Read `work/tracking/Work Inbox Index.md`.
3. Process only unprocessed files from `raw/work/inbox/` or pasted work content.
4. Identify the parent and sub-product. If unclear, use `work/tracking/Work Needs Triage.md`.
5. **Read the raw note fully before writing anything.** Inventory the distinct sections, examples, tables, and callouts it contains. If the note contains embedded images, read each one using the Read tool before proceeding — unless the user has explicitly marked a specific image to skip.
6. Create or update concept pages. Preserve all distinct content from the raw note. Compress only literal duplicates. Elaborate within the framework when source is sparse. Apply the splitting rule if the page grows long and the sub-concepts are logically parallel.
7. Create decision pages at the sub-product level (`<Sub-Product>/Decisions/`). Create pattern pages in `work/patterns/`. Check `work/patterns/Patterns Index.md` first — if the pattern already exists, update the index row and tags rather than creating a duplicate file. Do not invent reasoning.
8. Update explicit tasks in `work/tasks/Work Tasks.md` and the relevant sub-product Tasks file.
9. Update `work/tracking/Work Inbox Index.md` (Output column lists every artifact produced, tagged by type — concept / decision / pattern / tasks), `Work Index.md`, `work/tasks/Work Tasks.md` when needed, `work/tasks/Work Task History.md` when tasks change, `work/patterns/Patterns Index.md` when patterns change, and `work/tracking/Work Log.md`.

## Conflict Rules

- Concepts show current understanding. Update in place; flag inferred reasoning explicitly.
- Decisions preserve history. Mark old decisions as `superseded` instead of deleting them.
- Patterns flag conflicts when new behaviour contradicts an existing pattern.
- Task history is append-only.
