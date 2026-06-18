---
type: concept
sources:
  - "[[Hidden vs. Disabled In UX]]"
created: 2026-06-18
updated: 2026-06-18
---

# Action Visibility in UX

Action visibility is the choice between showing, disabling, hiding, or making controls read-only based on user relevance, permissions, state, and workflow learning.

## Rule Of Thumb

Show or disable actions when they help users understand what exists and can become available later.

Hide actions when they are irrelevant, permission-restricted, unsafe to expose, or tied to a condition or object that does not exist.

## Disable When

- The user can use the action later.
- The action is part of a persistent workflow.
- The current restriction is temporary.
- A value is relevant but not editable.
- The interface should teach users that a feature exists.

Disabled controls should explain why they are disabled and how to re-enable them.

## Hide When

- The user will never be able to use the action.
- The action is permission-restricted.
- The control is only relevant in another mode or after another condition is met.
- Showing the action would add noise or imply a capability the user does not have.

## Alternatives

Plain disabled buttons are not always the best answer. Alternatives include:

- enabled controls that explain the issue after interaction
- read-only states
- empty states
- progressive reveal
- accordions for unavailable options
- clearer validation or error messages
- user preferences to hide unavailable options

## Related Work Pattern

The work memory has a Crosstabs-specific application of this concept: [[patterns/Action Visibility by Workflow Relevance|Action Visibility by Workflow Relevance]].

---

*Sources: [[Hidden vs. Disabled In UX]]*
*Updated: 2026-06-18*
