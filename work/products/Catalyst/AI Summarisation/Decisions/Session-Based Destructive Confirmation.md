---
type: decision
status: accepted
---

# Session-Based Destructive Confirmation

For AI Summarisation, show a destructive-action confirmation dialog once per session, then suppress it for subsequent similar actions in the same session.

## What Was Decided

When a user performs a destructive action (e.g. deleting a bucket that is already used in a generated summary), show a confirmation dialog. Once the user has confirmed, do not show the confirmation again for similar destructive actions within the same session.

## Reasoning

- Repeated confirmations create confirmation fatigue and interrupt workflow.
- A single confirmation establishes awareness; subsequent confirmations add no new information.
- Users are assumed to understand the consequence after the first acknowledgement.
- The session boundary keeps the scope tight — a new session resets the suppression.

## Constraints

This pattern applies when the destructive action is recoverable or the cost of repeating it is moderate. It is not appropriate when actions are irreversible, affect multiple users simultaneously, or could cause significant data loss.

See [[patterns/Session-Based Destructive Confirmation|Session-Based Destructive Confirmation]] (pattern) for full behaviour and usage guidance.

---

*Sources: [[raw/work/processed/Session-Based Destructive Confirmation Pattern.md]]*
*Updated: 2026-05-22*
