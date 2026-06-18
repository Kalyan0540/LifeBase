---
type: decision
status: accepted
---

# Filter Actions Disabled Instead of Hidden

For Crosstabs filters, keep `Clear date range`, `Filter details`, and `Clear filter` visible in a disabled state when there is no selected date range or filter.

Do not hide these actions just because there is currently nothing to clear or inspect.

## Context

The question was whether unavailable filter actions should be hidden or disabled when no selected filter is available.

The captured screenshots show:

- Empty state: date range and filter selectors are available, while `Clear date range`, `Filter details`, and `Clear filter` are visible but disabled.
- Active filter state: after selecting `AUM 10`, `Filter details` and `Clear filter` become active.

The team discussed the tradeoff with Pradnya and Mahesh. The agreed preference is disabled rather than hidden for these actions.

## Reasoning

These actions are part of the expected filter workflow. Keeping them visible helps users learn where the actions live and keeps the interface predictable.

In this case, the actions are not permanently unavailable. They are inactive because there is no selected object or value to operate on yet.

Layout stability is a supporting benefit, but not the main reason for the decision. The stronger reason is workflow visibility and helping users understand what becomes possible later.

The note also references the external UX guidance that important workflow actions can stay visible when users will be able to use them later, while irrelevant or permission-restricted actions should be hidden.

## Guidance

- Show persistent workflow actions disabled when the user can use them later in the same workflow.
- Hide actions only when they are irrelevant, unavailable to the user, or tied to an object that does not exist.
- If a disabled state is used, the reason should be obvious or easy to explain.

Related work-level pattern: [[patterns/Action Visibility by Workflow Relevance|Action Visibility by Workflow Relevance]].

---

*Sources: [[UX UI Pattern & Decision]]*
*Updated: 2026-06-18*
