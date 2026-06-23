---
type: source
source_title: "Hidden vs. Disabled In UX"
source_url: "https://www.smashingmagazine.com/2024/05/hidden-vs-disabled-ux/"
raw_path: "raw/knowledge/product-and-design/design/Hidden vs. Disabled In UX.md"
created: 2026-06-18
updated: 2026-06-18
---

# Hidden vs. Disabled In UX

Smashing Magazine article on when UI features should be hidden, disabled, read-only, or left enabled with feedback.

## Core Idea

Both hidden and disabled controls can confuse users. Hiding can hurt discoverability. Disabling without explanation can frustrate users.

The article's practical rule:

- Disable a control when the user should know the feature exists but cannot use it yet.
- Hide a control when the value or action is irrelevant, unavailable to that user, or impossible in the current context.
- Do not hide important buttons or key filters by default when users expect them to persist.

## Decision Roadmap

Ask: will this user ever be able to interact with this element?

If yes, disabled or read-only states are usually better. This fits temporary restrictions, incompatible filter states, relevant-but-not-editable values, and actions that are not ready yet.

If no, hide the element. This fits permissions, access controls, safety/security restrictions, inaccessible admin controls, and functionality that should appear only once a condition is met.

## Disabled State Guidance

Disabled controls can help users learn the interface, understand feature availability, or see the benefits of an upgrade.

But disabled controls need explanation:

- why the control is disabled
- how to make it available
- whether the state is temporary or permanent

The article suggests alternatives to plain disabled buttons, including enabled buttons with explanatory feedback, read-only states, better empty states, hide/reveal accordions, error messages, and user customization.

## Layout Stability

Showing and hiding controls can create layout shifts. If a UI lets users switch between hidden and visible states, it should avoid disruptive shifts.

Layout stability is useful, but it should not be the only reason to show unavailable controls. The stronger question is whether the action is meaningful and learnable for the user in that context.

## Design System Examples

The article points to design system examples from Carbon, Unity, Vaadin, SAP, Motif, and Emplifi to show how hidden, disabled, and read-only states are handled in production systems.

## Related Concept

- [[Action Visibility in UX]]

---

*Raw source: [[Hidden vs. Disabled In UX]]*
*Updated: 2026-06-18*
