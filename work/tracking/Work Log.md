# Work Log

Append-only chronological record of work-memory operations.

Parse entries with: `grep "^## \[" "work/tracking/Work Log.md"`

---

## [2026-05-18] setup | Work memory scaffold

Created the work memory structure: `work/Work Index.md`, `work/Work Inbox Index.md`, `work/Work Tasks.md`, `work/Work Task History.md`, `work/Work Log.md`, and `work/products/`. Future work inbox processing should update product pages, task dashboards, task history, inbox index, and this log.

---

## [2026-05-18] setup | Work tracking tables and triage

Converted `work/Work Index.md`, `work/Work Inbox Index.md`, and `work/Work Tasks.md` to table-based tracking. Added `work/Work Needs Triage.md` for notes or tasks that cannot be safely assigned to a product. Recorded three Cross Tabs raw work files in the unprocessed inbox table without processing them.

---

## [2026-05-18] format | Human-readable product and task pages

Reformatted Cross Tabs product pages so headings are readable first and IDs/metadata appear beneath the content. Converted `work/Work Tasks.md` to checkbox-first format for daily review and updated `work/Work Task History.md` into a readable chronological summary. Updated `AGENTS.md` so future product memory follows this human-readable pattern.

---

## [2026-05-18] process | Cross Tabs custom variable creation

Processed three raw work inbox notes for Cross Tabs custom variable creation. Created `work/products/Cross Tabs/` with index, overview, requirements, decisions, and tasks pages; updated global work indexes and task history; marked the three inbox files as processed.

---

## [2026-05-18] correction | Removed inferred Cross Tabs tasks

Cleared three inferred Cross Tabs tasks from `work/Work Tasks.md` and `work/products/Cross Tabs/Cross Tabs - Tasks.md` because the source notes did not explicitly mark them as tasks or todos. Updated `AGENTS.md` so future tasks are created only from explicit checkboxes, todos, action items, or direct user instruction. Task wording should stay simple and source-like, with compact metadata below the readable task text.

---

## [2026-05-18] setup | Split agent rules and added explicit Cross Tabs task

Split the large root `AGENTS.md` into a router plus `AGENTS - Wiki.md`, `AGENTS - Work.md`, and `AGENTS - Thoughts.md`. Added the explicit Cross Tabs task requested by the user to `work/Work Tasks.md` and `work/products/Cross Tabs/Cross Tabs - Tasks.md`, with collapsible metadata and links to the relevant custom variable source sections.

---

## [2026-05-18] format | Visible task links

Updated the Cross Tabs decision-making task so the useful product and source links appear directly in the visible task text, while detailed IDs and traceability remain in collapsible metadata.

---

## [2026-05-18] format | Simplified task metadata

Reduced task metadata for the Cross Tabs decision-making task to only ID and updated date because the visible task text already contains the useful product and source links. Updated `AGENTS - Work.md` to prefer minimal metadata when visible task links are sufficient.

---

## [2026-05-19] restructure | Parent → sub-product hierarchy

Reorganised `work/products/` from a flat structure into a two-level parent → sub-product hierarchy based on user instruction.

Parent products created: **Enlyta**, **Catalyst**, **AI**.

- `Cross Tabs` and `Design System` are sub-products of Enlyta.
- `AI Summarisation` is a sub-product of Catalyst.
- `AI` (formerly "AI Product") is both parent and current sub-product.

Updated files: all sub-product frontmatter (`parent` field added), `AGENTS.md` vault map, `AGENTS - Work.md` structure and task rules, `Work Index.md` (parent/sub-product table), `Work Tasks.md` (grouped by `Parent › Sub-Product` headings), `Work Task History.md`.

---

## [2026-05-20] restructure | Concepts/Decisions/Patterns model + minimal metadata

Refined per-product structure based on user instruction. Each sub-product now follows: `<Sub-Product> - Index.md`, `<Sub-Product> - Tasks.md`, `Concepts/`, `Decisions/`, `Patterns/`.

Removed per sub-product: `Overview.md`, `Requirements.md`, and the standalone `Decisions.md` (split into per-decision files inside `Decisions/`).

For Cross Tabs, migrated the three custom variable creation source notes into a single concept page: `Custom Variable Creation.md` (with text/number/variable output as sections). The two prior inferred candidate decisions were folded into the concept page as open threads — they were not explicit decisions in source material.

Flattened the redundant `AI/AI/` nesting. `work/products/AI/` is now a single product folder; will become a parent index again when distinct AI sub-products emerge.

Reduced metadata significantly. Frontmatter is now minimal (`type` only on most pages; `parent` only on sub-product indexes). IDs, dates, and source links moved to a footer line at the bottom of each page. Task metadata moved from `<details>` blocks to inline backtick tokens: ``- [ ] Do thing. `P0` `TASK-...```.

Moved agent rule files into `_agents/`: `AGENTS.md`, `AGENTS - Wiki.md`, `AGENTS - Work.md`, `AGENTS - Thoughts.md`, plus `README - How to Use LifeBase.md`. Underscore prefix keeps the folder pinned at the top of the Obsidian sidebar.

Updated files: `_agents/AGENTS.md` (vault map), `_agents/AGENTS - Work.md` (full rewrite for new model), `Work Index.md`, `Work Tasks.md`, `Work Inbox Index.md`, parent indexes (`Enlyta - Index.md`, `Catalyst - Index.md`), and per sub-product Index + Tasks files.

---

## [2026-05-20] concept-detail | Split Custom Variable Creation into parent + 3 detail pages

User flagged that the initial `Custom Variable Creation` concept page over-compressed the three source notes — missing the after-crosstab tables, the expected vs. current behaviour split for Number Output, the Problem framing for Variable Output, and the misunderstanding/clarification callouts.

Split into one parent + three detail pages under `Cross Tabs/Concepts/`:

- `Custom Variable Creation.md` — overview, shared behaviour (originals preserved, first-match-wins, no-match), output type comparison, open threads
- `Custom Variable - Text Output.md` — full Text Output detail with Age Grouping example, before/after crosstabs, key terms, use cases
- `Custom Variable - Number Output.md` — full Number Output detail with NPS Scoring example, expected analytical output (Mean NPS Score table), current crosstab AFTER (count buckets), important clarification, common misunderstanding
- `Custom Variable - Variable Output.md` — full Variable Output detail with Purchased Brand example, The Problem (split crosstabs), combined result

Naming: child concept files use `Custom Variable - X Output` (drop "Creation") to disambiguate from raw source notes named `Custom Variable Creation - X Output`.

Updated `Cross Tabs - Index.md` (nested concept list) and `Work Inbox Index.md` (each raw note now maps to its detail concept + parent + tasks).

Rule reinforced: when raw material is detailed, the concept page should preserve content — reorganise and rephrase, but don't drop examples, tables, or distinct sections that aren't true duplicates. When raw material is sparse, the framework can elaborate.

---

## [2026-05-20] process | Enlyta Discussion + Today's meeting notes

Processed two new raw work inbox files.

`raw/work/processed/Enlyta Discussion.md` — Cross Tabs meeting notes. Created two concept/decision artifacts:
- `Cross Tabs/Concepts/Run and Save Flow.md` — Run-before-Save rule, tooltip behaviour, two distinct confirmation dialogues (not-run-then-back vs. run-then-back)
- `Cross Tabs/Decisions/Run Before Save.md` — explicit decision: no auto-run on save; run is mandatory before save
- `Cross Tabs/Decisions/Variable Creation Scope.md` — two decisions: (1) output type set at variable level not value level; (2) variable output deferred to post-release
- Updated `Custom Variable Creation.md` to reflect the scope decisions and add output-type-switching edge case to open threads

`raw/work/processed/Today's meeting notes.md` — checkbox tasks across three sections:
- Enlyta / Cross Tabs: 3 new tasks (TASK-2026-05-20-001–003)
- Common Components: 3 tasks routed to `Work Needs Triage` — product ownership unclear; source note itself flagged this for triage
- Catalyst: 3 new tasks routed to AI Summarisation (TASK-2026-05-20-004–006)

Updated: `Cross Tabs - Index.md`, `Cross Tabs - Tasks.md`, `AI Summarisation - Tasks.md`, `Work Tasks.md`, `Work Index.md` (task counts), `Work Inbox Index.md`, `Work Task History.md`, `Work Needs Triage.md`.

Triage resolved (same session): 3 Common Components bucketing tasks duplicated into both Cross Tabs (TASK-2026-05-20-007–009) and AI Summarisation (TASK-2026-05-20-010–012). Work Needs Triage cleared.

---

## [2026-05-20] rules | Source fidelity, splitting, and dedup principles added to AGENTS - Work

Expanded the Concepts section of `_agents/AGENTS - Work.md` with four named subsections that codify how raw notes should be processed:

- **Source Fidelity vs. Elaboration** — preserve all distinct content from detailed sources; elaborate within the framework when sources are sparse. Reader test: no missing context.
- **Do Not Infer Reasoning or Behaviour** — leave it out, or mark explicitly inferred.
- **Page Structure and Splitting** — sub-concepts default to sections; split into separate files only when the page is long AND sub-concepts are parallel and self-standing. Parent + children structure. Child-page naming convention to avoid Obsidian link collisions with raw filenames.
- **Deduplication** — consolidate literal duplicates (within a source, or across sources for shared behaviour). Never drop content for "seeming" similar.

Also expanded the **Work Inbox Processing** checklist with new steps: read the raw note fully and inventory its sections first; preserve distinct content; apply the splitting rule when warranted; tag every artifact in the Output column of `Work Inbox Index.md` by type.

---

## [2026-05-22] process | Priority tasks + 3 pattern/decision notes

Processed 4 unprocessed raw work inbox files.

**`raw/work/processed/2026-05-21 Priority Tasks.md`** — task status update file.

Cross Tabs completions (2026-05-21): TASK-2026-05-20-001, -002, -007, -008. Priority change: TASK-2026-05-20-003 P1 → P2. New task: TASK-2026-05-21-001 — Update table designs: update all screenshots and check links in Jira. `P0`

AI Summarisation completions (2026-05-21): TASK-2026-05-20-004, -005, -010, -011, -012.

Updated: `Cross Tabs - Tasks.md`, `AI Summarisation - Tasks.md`, `Work Tasks.md`, `Work Task History.md`.

**`raw/work/processed/Session-Based Destructive Confirmation Pattern.md`** — show destructive confirmation once per session, then suppress. Decision and pattern for AI Summarisation; pattern for Cross Tabs.

Created: `AI Summarisation/Decisions/Session-Based Destructive Confirmation.md`, `work/patterns/Session-Based Destructive Confirmation.md`.

**`raw/work/processed/Trigger warnings on intent, not possibility.md`** and **`raw/work/processed/Tabs vs Segemented controls vs Custom tabs.md`** — same source material (text identical). Show warnings only on destructive intent, not on entering edit mode. Decision and pattern for AI Summarisation; pattern for Cross Tabs. Note: Tabs file contains two embedded images that were not processed in this pass.

Created: `AI Summarisation/Decisions/Trigger Warnings on Intent, Not Possibility.md`, `work/patterns/Trigger Warnings on Intent, Not Possibility.md`.

Updated: `Work Inbox Index.md`.

---

## [2026-05-22] restructure | Patterns to work level + work folder reorganisation

Moved patterns from product level to work level per user instruction. Reorganised `work/` into four groups.

**Pattern changes:**
- Moved pattern files from `work/products/Catalyst/Patterns/` → `work/patterns/`
- Added `tags: [Catalyst, Enlyta]` frontmatter to each pattern file for Obsidian filtering
- Deleted old product-level pattern files; feature-level `Patterns/` stubs updated to redirect
- `Work Patterns Index.md` moved into `work/patterns/Patterns Index.md`

**Folder reorganisation:**

| Before | After |
|---|---|
| `work/Work Tasks.md` | `work/tasks/Work Tasks.md` |
| `work/Work Task History.md` | `work/tasks/Work Task History.md` |
| `work/Work Inbox Index.md` | `work/tracking/Work Inbox Index.md` |
| `work/Work Needs Triage.md` | `work/tracking/Work Needs Triage.md` |
| `work/Work Log.md` | `work/tracking/Work Log.md` |
| `work/Work Patterns Index.md` | `work/patterns/Patterns Index.md` |

`work/Work Index.md` stays at root as the master entry point.

Updated: `Work Index.md`, `AGENTS.md`, `AGENTS - Work.md`, `Catalyst - Index.md`, `Enlyta - Index.md`, `AI Summarisation - Index.md`, `Cross Tabs - Index.md`, product-level Patterns stubs.

---

## [2026-05-22] fix | Ambiguous pattern links + fix agents stale lines

Fixed all Obsidian link collisions caused by decision files and pattern files sharing identical filenames.

- Decision files: both `Session-Based Destructive Confirmation` and `Trigger Warnings on Intent, Not Possibility` decision pages now use path-qualified links to their canonical pattern pages → `[[patterns/…|…]]`
- Feature index Patterns sections (AI Summarisation, Cross Tabs): pattern links path-qualified to `[[patterns/…|…]]`; decision links path-qualified to `[[Decisions/…|…]]`
- Parent index Patterns sections (Catalyst): pattern links path-qualified
- `[[Patterns Index]]` added to Folders sections in AI Summarisation - Index and Cross Tabs - Index
- `AGENTS - Work.md`: removed two stale lines ("It is fine for `Patterns/` to stay empty" and "All sub-product and product `Patterns/` folders contain redirect stubs only")

---

## [2026-05-22] process | Tabs vs Custom Tabs (image pass)

Processed the two embedded images in `raw/work/processed/Tabs vs Segemented controls vs Custom tabs.md` that were skipped on the initial pass.

Image 1 — Bucketing & Custom Logic: Pattern Comparison. A 6-criteria comparison (Mental Model, Content Change, Scalability, Discoverability, Industry Convention, User Confidence) between Segmented Controls and Tabs, concluding Tabs are the right choice for Bucketing / Custom Logic in AI Summarisation.

Image 2 — Tabs vs Custom Tabs. Defines the distinction and design rule: Tabs for mode/workflow switching; Custom Tabs for context/breakdown selection.

Created: `AI Summarisation/Concepts/Tabs vs Custom Tabs.md`, `AI Summarisation/Decisions/Tabs over Segmented Controls.md`.

Updated: `AI Summarisation - Index.md` (concept + decision added), `Work Inbox Index.md` (entry corrected).

---

## [2026-05-27] process | 2026-05-26 work notes

Processed `raw/work/processed/2026-05-26 Notes.md`.

Cross Tabs:
- Added TASK-2026-05-26-001 — For Run in Cross Tabs, add the recommendation flow and reasoning in the design along with the last discussed designs. `P0`
- Completed TASK-2026-05-21-001 — Update table designs: update all screenshots and check links in Jira. `completed 2026-05-25`

AI Summarisation:
- Completed TASK-2026-05-20-006 — Provide Dominique the links to updated copy design, dialogue layout, and selection interaction in profile fields. `completed 2026-05-25`

Activity Feed:
- Created `work/products/Catalyst/Activity Feed/` for Catalyst activity feed work.
- Added completed TASK-2026-05-26-002 — Peer review new activity feed in Catalyst for both member side and facilitator side. `P0` `completed 2026-05-25`

Updated: `Work Tasks.md`, `Cross Tabs - Tasks.md`, `AI Summarisation - Tasks.md`, `Activity Feed - Tasks.md`, `Work Index.md`, `Catalyst - Index.md`, `Work Inbox Index.md`, `Work Task History.md`.

---

## [2026-05-27] rules | Agent rules simplified and split

Replaced the `_agents/` rule folder with a root `AGENTS.md` router and focused rule files under `rules/`.

Work rules are now split by use case:
- `rules/work/Work.md` for lightweight work queries and routing.
- `rules/work/Process Work.md` for inbox processing.
- `rules/work/Work Formats.md` for exact page and task formats.

Also standardised raw asset folders under each domain and moved existing work screenshots from `raw/work/processed/assets/` to `raw/work/assets/`.

---

## [2026-06-01] process | Cross Tabs decision clarification + 29 May tasks

Processed two unprocessed work inbox files.

`raw/work/processed/Crosstabs Decision Making.md` — Cross Tabs clarification from Pradnya that custom variable output is determined as the column name. Created `Cross Tabs/Decisions/Custom Variable Output as Column Name.md` and updated `Custom Variable Creation.md` plus `Custom Variable - Number Output.md` to clarify that numeric output behaves as a column label in the current Cross Tabs flow, not as calculation support.

`raw/work/processed/29th May '26 - Tasks.md` — task board update. Completed TASK-2026-05-26-001 on 2026-05-27, updated TASK-2026-05-20-003 from P2 to P0 with remaining scope, added TASK-2026-05-29-001 for crosstabs dev design review, and updated Design System colour tokens from P2 to P1.

Moved the referenced screenshot attachment into `raw/work/assets/`.

---

## [2026-06-01] correction | Preserve subtasks under parent task

Corrected TASK-2026-05-20-003 after user feedback: restored the parent task wording and kept the 29 May checklist items as indented subtasks in both `Cross Tabs - Tasks.md` and `Work Tasks.md`.

Added a simple rule to `rules/work/Work Formats.md`: explicit source subtasks should stay as indented checklist items, not be merged into the parent task.

---

## [2026-06-03] update | Cross Tabs task completions and variable edit decision

Updated Cross Tabs task status from user notes: completed three existing subtasks under TASK-2026-05-20-003, added the completed "view mode for custom variable" subtask, and added completed task TASK-2026-06-03-001 for the crosstab demo call with new QA.

Created `Cross Tabs/Decisions/Custom Variable Edit Synchronisation.md` to record that custom variable edits sync automatically rather than creating a previous-state duplicate like public saved filters. Also recorded that duplicate and use at custom variable level is post-MVP, and any custom variable can be further bucketed.
