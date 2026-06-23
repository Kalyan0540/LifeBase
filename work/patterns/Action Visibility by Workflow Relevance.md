---
type: pattern
tags: [Enlyta]
---

# Action Visibility by Workflow Relevance

Keep persistent workflow actions visible when they are temporarily unavailable. Hide actions when they are mode-specific, permission-restricted, irrelevant, or tied to an object that does not exist.

## Applies In

- [[Cross Tabs - Index|Cross Tabs]] — filter actions and saved-filter view/edit controls.

## Originating Decisions

- [[Filter Actions Disabled Instead of Hidden]]
- [[Saved Filter View and Edit Mode Controls]]

## Pattern

Use disabled state for actions that teach the workflow and can become available later in the same context.

Use hidden state for controls that should not exist for the current user, mode, or object.

## Examples

### Filter actions

When no date range or filter is selected, `Clear date range`, `Filter details`, and `Clear filter` stay visible but disabled. They become active once the related date range or filter exists.

### Saved filter controls

In saved-filter view mode, row drag and row delete are hidden because the user is reviewing or applying the filter, not editing it.

For non-creators, edit and delete controls are hidden because they are permission-restricted. The visible path is `Modify & Use`.

For creators, high-level owner actions are visible in view mode, and row-level editing controls appear only after entering edit mode.

## Guidance

- Show persistent workflow actions disabled when users can use them later and the action helps them understand the workflow.
- Hide actions that are not relevant to the current mode.
- Hide actions that the current user does not have permission to use.
- Hide actions tied to an object that does not exist.
- Make the reason for a disabled state obvious or explainable.

---

*Applies to: Enlyta - Cross Tabs*
*Sources: [[UX UI Pattern & Decision]]*
*Updated: 2026-06-18*
