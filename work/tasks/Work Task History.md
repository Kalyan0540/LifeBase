# Task History

Append-only chronological history of task creation, status changes, and completions.

---

## 2026-05-18

Work task history initialized.

Removed three inferred Cross Tabs tasks because the source notes did not explicitly mark them as tasks or todos. Going forward, tasks are created only from explicit checkboxes, todos, action items, or direct user instruction.

Added one explicit Cross Tabs task requested by the user:

- Complete the decision making on new variable creation for Cross Tabs: text output, number output, and variable output.
  - ID: TASK-2026-05-18-001
  - Product: [[Cross Tabs - Index]]

Added 6 tasks from unchecked items on the user's work task board screenshot. Three new product folders created (Enlyta Design System, Catalyst AI Summarisation, AI Product):

- Update filter journeys for the confirmation dialogue.
  - ID: TASK-2026-05-18-002
  - Priority: P0
  - Product: [[Cross Tabs - Index]]

- Crosstab prototype demo recording.
  - ID: TASK-2026-05-18-003
  - Priority: P2
  - Product: [[Cross Tabs - Index]]

- Design system colour tokens.
  - ID: TASK-2026-05-18-004
  - Priority: P2
  - Product: [[Enlyta Design System - Index]]

- Summarisation backend flag turn on/off for member side.
  - ID: TASK-2026-05-18-005
  - Priority: P2
  - Product: [[Catalyst AI Summarisation - Index]]

- Claude skills quick demo recording.
  - ID: TASK-2026-05-18-006
  - Priority: P3
  - Product: [[AI Product - Index]]

- Render Table designs.
  - ID: TASK-2026-05-18-007
  - Priority: P0
  - Product: [[Cross Tabs - Index]]

## 2026-05-19

Reorganised `work/products/` into a parent → sub-product hierarchy based on user instruction.

- **Enlyta** is now the parent for Cross Tabs and Design System.
- **Catalyst** is now the parent for AI Summarisation.
- **AI** is now the parent product (renamed from "AI Product").

Folder moves and renames:

- `products/Cross Tabs/` → `products/Enlyta/Cross Tabs/`
- `products/Enlyta Design System/` → `products/Enlyta/Design System/` (renamed to Design System)
- `products/Catalyst AI Summarisation/` → `products/Catalyst/AI Summarisation/` (renamed to AI Summarisation)
- `products/AI Product/` → `products/AI/AI/` (renamed to AI)

Created three new parent index pages: `Enlyta - Index.md`, `Catalyst - Index.md`, `AI - Index.md`.

Updated all sub-product frontmatter to include `parent` field. Updated `AGENTS.md` vault map, `AGENTS - Work.md` structure and task rules, `Work Index.md`, and `Work Tasks.md` to reflect the new hierarchy.

Completed: Render Table designs.
  - ID: TASK-2026-05-18-007
  - Priority: P0
  - Product: [[Cross Tabs - Index]]
  - Completed: 2026-05-19

## 2026-05-20

Added 6 tasks from two new raw work inbox files.

Cross Tabs — from `Today's meeting notes.md`:

- User journey for Run-before-Save flow; add Save button tooltip.
  - ID: TASK-2026-05-20-001
  - Priority: P0
  - Product: [[Cross Tabs - Index]]

- Design confirmation dialogue for when user clicks back/reload without running.
  - ID: TASK-2026-05-20-002
  - Priority: P0
  - Product: [[Cross Tabs - Index]]

- Update variable creation flows in UI per new scope decisions; cover edge cases when switching output type after setup.
  - ID: TASK-2026-05-20-003
  - Product: [[Cross Tabs - Index]]

AI Summarisation — from `Today's meeting notes.md` (Catalyst section; routed to AI Summarisation as only current Catalyst sub-product):

- Warning message for deleting bucketing if a summary is already generated.
  - ID: TASK-2026-05-20-004
  - Product: [[AI Summarisation - Index]]

- Update button text to "Reset to default" instead of "Reset".
  - ID: TASK-2026-05-20-005
  - Product: [[AI Summarisation - Index]]

- Provide Dominique the links to updated copy design, dialogue layout, and selection interaction in profile fields.
  - ID: TASK-2026-05-20-006
  - Product: [[AI Summarisation - Index]]

Resolved triage — 3 Common Components bucketing tasks duplicated into both Cross Tabs and AI Summarisation per user instruction:

- Confirm with Pradnya on bucketing flow difference between Catalyst and Enlyta.
  - ID: TASK-2026-05-20-007 (Cross Tabs) / TASK-2026-05-20-010 (AI Summarisation)

- Add validation that bucket names should not be the same.
  - ID: TASK-2026-05-20-008 (Cross Tabs) / TASK-2026-05-20-011 (AI Summarisation)

- Create loading state for N size in bucketing.
  - ID: TASK-2026-05-20-009 (Cross Tabs) / TASK-2026-05-20-012 (AI Summarisation)

## 2026-05-21

Priority and status updates across Cross Tabs and AI Summarisation per user review.

**Cross Tabs — priority changes:**
- TASK-2026-05-18-002 (Update filter journeys for the confirmation dialogue): P0 → P2
- TASK-2026-05-20-003 (Update variable creation flows in UI): no priority → P1
- TASK-2026-05-20-007 (Confirm with Pradnya on bucketing flow): no priority → P0
- TASK-2026-05-20-008 (Add validation that bucket names should not be the same): no priority → P0

**Cross Tabs — status changes:**
- TASK-2026-05-18-001 (Complete the decision making on new variable creation): marked completed 2026-05-21
- TASK-2026-05-18-003 (Crosstab prototype demo recording): moved to Blocked/On Hold
- TASK-2026-05-20-009 (Create loading state for N size in bucketing): removed from Cross Tabs (kept in AI Summarisation only)

**AI Summarisation — priority changes:**
- TASK-2026-05-20-004 (Warning message for deleting bucketing): no priority → P0
- TASK-2026-05-20-005 (Update button text to "Reset to default"): no priority → P0
- TASK-2026-05-20-006 (Provide Dominique the links): no priority → P0
- TASK-2026-05-20-010 (Confirm with Pradnya on bucketing flow): no priority → P0
- TASK-2026-05-20-011 (Add validation that bucket names should not be the same): no priority → P0
- TASK-2026-05-20-012 (Create loading state for N size in bucketing): no priority → P0

## 2026-05-22

Processed `raw/work/inbox/2026-05-21 Priority Tasks.md`.

**Cross Tabs — completed:**
- TASK-2026-05-20-001 (User journey for Run-before-Save flow; add Save button tooltip): completed 2026-05-21
- TASK-2026-05-20-002 (Design confirmation dialogue for back/reload without running): completed 2026-05-21
- TASK-2026-05-20-007 (Confirm with Pradnya on bucketing flow difference): completed 2026-05-21
- TASK-2026-05-20-008 (Add validation that bucket names should not be the same): completed 2026-05-21

**Cross Tabs — priority change:**
- TASK-2026-05-20-003 (Update variable creation flows in UI): P1 → P2

**Cross Tabs — new task:**
- Update table designs: update all screenshots and check links in Jira.
  - ID: TASK-2026-05-21-001
  - Priority: P0
  - Product: [[Cross Tabs - Index]]
  - Note: Parent task "Update table designs" has two sub-items completed (bucketed indication for column variable; Mean and SD table view); this task covers the remaining open sub-item.

**AI Summarisation — completed:**
- TASK-2026-05-20-004 (Warning message for deleting bucketing if a summary is already generated): completed 2026-05-21
- TASK-2026-05-20-005 (Update button text to "Reset to default"): completed 2026-05-21
- TASK-2026-05-20-010 (Confirm with Pradnya on bucketing flow difference): completed 2026-05-21
- TASK-2026-05-20-011 (Add validation that bucket names should not be the same): completed 2026-05-21
- TASK-2026-05-20-012 (Create loading state for N size in bucketing): completed 2026-05-21
