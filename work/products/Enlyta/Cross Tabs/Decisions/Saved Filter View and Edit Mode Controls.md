---
type: decision
status: accepted
---

# Saved Filter View and Edit Mode Controls

In saved filters, hide row drag and row-delete controls in view mode. Show them only in edit mode.

For non-creators, hide edit and delete controls for the original filter. Show the valid path instead: `Modify & Use`.

## Context

The question was whether delete and drag controls should be hidden in saved-filter view mode and shown only in edit mode.

The source screenshots compare:

- Non-creator view: the saved filter is visible with `Modify & Use`; owner edit/delete controls are absent.
- Creator view: the creator sees high-level owner actions such as `Edit Filter` and filter-level `Delete`.
- Creator edit mode: row-level delete and drag controls appear, along with `Discard`, `Save`, visibility controls, and other editing controls.

## Reasoning

Drag and row-delete are edit-mode controls, not persistent workflow actions.

In view mode, the user is reading, reviewing, or applying the saved filter. Showing disabled row drag/delete controls in view mode would add noise and could incorrectly suggest inline manipulation is available.

For non-creators, edit and delete are permission-restricted, not temporarily unavailable. Disabled controls would communicate the wrong thing. The user should see the action they can take: `Modify & Use`.

## Behaviour

- Non-creator view: show `Modify & Use`; hide `Edit Filter`, row drag, row delete, and owner delete actions.
- Creator view mode: show high-level owner actions like `Edit Filter` and filter-level `Delete`; hide row drag/delete.
- Creator edit mode: show row drag/delete, `Discard`, `Save`, visibility toggle, and other editing controls.

Related work-level pattern: [[patterns/Action Visibility by Workflow Relevance|Action Visibility by Workflow Relevance]].

---

*Sources: [[UX UI Pattern & Decision]]*
*Updated: 2026-06-18*
