---
type: concept
---

# Persona Bots Overview

Persona Bots is a separate AI web app where users speak with predefined synthetic personas.

It is not the same as the existing chatbot:

- the chatbot answers data queries from a data set
- Persona Bots answer from the perspective of a selected persona
- responses should sound like a human perspective, not a table or metric output
- one persona answers at a time in the current scope

## Why It Exists

The product is driven by client demand and by the opportunity to productize available data sets.

For internal data sets like Cogent investor data, users can subscribe to a model and ask follow-up questions without running new fieldwork. This helps when a survey has already ended and the user wants to ask a synthetic representative more questions.

The product also fits the industry interest in synthetic data.

## Data And Persona Model

Personas are predefined before development starts.

Each respondent in the data set is tagged to a persona. When a user selects a persona, the system uses only the rows or responses from that persona group, calculates the relevant scores, compares where needed, and then generates a personified response.

Personas should be:

- distinct from each other
- broad enough to cover most of the useful population
- not so narrow that the sample size becomes too small

The expected range is roughly 4 to 7 personas per data set. Current early client work is expected to land around 4 to 6 personas.

Users cannot create their own personas in the near-term scope.

## Product Shape

Persona Bots is planned as a separate web app, not a widget inside Enlyta or Catalyst.

Initial internal access can come from an AI Hub tile. AI Hub handles SSO and authorization, then redirects users to the Persona Bots app and should pass the user's email address downstream for logging and feedback capture.

Client-facing access may later require its own login page, but authentication pages are not part of the current UX scope.

The product should support future client-specific configuration, including colors, fonts, logos, and brand guidelines.

## Current And Future Scope

Current scope:

- standalone web app
- desktop-first experience
- predefined persona selection
- one persona selected at a time
- temporary on-screen state only; caching/history is not a current focus
- design can be different from existing chatbot or platform UI

Forward-looking scope:

- contextual conversation
- switching between personas
- comparing responses from multiple personas
- tabular or visual comparison across personas
- client-facing login and branding configuration

---

*Sources: [[Persona Bots - Scoping Discussion-2026-06-08 -Meeting Recording]], [[Alignment On Persona Bots UIUX-2026-06-16-Meeting Recording]]*
*Updated: 2026-06-17*
