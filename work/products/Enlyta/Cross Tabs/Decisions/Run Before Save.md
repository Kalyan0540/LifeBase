---
type: decision
status: accepted
---

# Run Before Save

Do not auto-run when the user clicks Save. Run is a mandatory step before Save; the Save button stays disabled until the cross-tab has been run.

## Decision

- Save button is disabled until the cross-tab has been run.
- The system does not trigger a run automatically when the user clicks Save.
- A tooltip on the Save button communicates the requirement when the user tries to save without running.

## Reasoning

If the user intends to save and exit, the run result would not be displayed anyway, and the user would likely navigate back regardless. Requiring an explicit run keeps the state clear and makes the sequence intentional.

## Rejected Alternative

Auto-run on Save click - rejected because it hides the run step from the user and offers no visible benefit.

---

*Sources: [[Enlyta Discussion]]*
*Updated: 2026-05-20*
