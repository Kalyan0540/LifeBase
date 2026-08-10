---
type: concept
---

# Persona Bots Interaction Model

The user must choose a persona before asking questions. Persona selection is mandatory because the selected persona determines which tagged rows or respondents are used to answer.

## Entry

For internal users, the starting point is expected to be AI Hub:

1. User opens AI Hub.
2. User selects the Persona Bots tile.
3. User chooses the available persona bot from a dropdown.
4. User is redirected into the Persona Bots web app.

There is no separate marketing or landing page in the current product flow. The first app screen should be the core interactive experience.

## Persona Selection

The user should be able to see available personas before starting the conversation.

Possible details to show:

- name
- visual cue, avatar, image, or caricature
- short description
- background or profile details
- drivers, motivations, and tone where available

The design can use cards, buttons, a left-side profile list, a dropdown, or another pattern if it better fits the web app. The selected persona should stay visible throughout the conversation.

## Conversation

Current technical scope may be one message exchange at a time, but the design should use a chat-like structure because contextual conversation is expected to arrive sooner than multi-persona comparison.

In current scope, only one persona can answer a question. If a different persona is selected, the old persona is deselected and the new interaction starts as a separate session or new chat state.

Suggested prompts, a query box, response area, disclaimer, and start-new-session behavior can follow familiar chatbot patterns where useful.

## Guardrails

Guardrails are expected to be handled mostly by backend/code logic. If a user asks something outside the selected persona or data set, the response can still appear in the chat area. No special UX pattern is currently required beyond normal response handling.

## Design Considerations

The web app should use the available landscape screen space instead of copying the small chatbot widget form factor.

Meeting notes from July 2026 add that widget view is also part of MVP scope. Current design work should account for both widget and web/desktop views.

Bank of America needs a client-specific mockup path separate from the generic persona version. This implies that persona settings, displayed details, and feedback from the Bank of America call may need to be documented and reflected in the mockups.

Open design questions include:

- whether a top header, left rail, or both are needed
- where persona details live
- where disclaimers appear
- how to show persona identity during the conversation
- how to make the current design scalable for later comparison between personas

---

*Sources: [[Persona Bots - Scoping Discussion-2026-06-08 -Meeting Recording]], [[Alignment On Persona Bots UIUX-2026-06-16-Meeting Recording]], [[Meeting Notes - 2026-07-14]]*
*Updated: 2026-07-17*
