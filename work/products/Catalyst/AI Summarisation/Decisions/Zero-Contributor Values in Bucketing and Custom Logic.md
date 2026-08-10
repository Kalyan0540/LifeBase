---
type: decision
status: accepted
---

# Zero-Contributor Values in Bucketing and Custom Logic

## Decision

In Bucketing and Custom Logic, keep values available even when they currently have 0 contributors/respondents.

Show a clear indication that the value currently has 0 respondents. Continue disabling those values only at the final selection stage where they cannot contribute to the current analysis.

## Reasoning

- Bucketing, custom variable creation, and custom logic are intentionally decoupled from final variable selection.
- A user may be creating a custom variable for future use, so a value having 0 contributors in the current dataset does not necessarily mean it should be unavailable for configuration.
- Applying a hard disable rule consistently becomes difficult in Custom Logic, where conditions may include values that currently have no contributors.
- Disabling or hiding these values during creation could make the creation logic inconsistent or overly restrictive.

## UI Guidance

- Indicate that a selected profile has no current respondents.
- The message can be dismissible so users can read it and recover modal space.
- Show the message at session level when the user adds a profile field with no current respondents.

---

*Sources: [[Catalyst AI Summary - No responses bucketing handling]]*
*Updated: 2026-07-14*
