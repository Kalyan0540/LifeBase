---
type: concept
---

# Run and Save Flow

The Run button and Save button are coupled. A user must run the cross-tab before Save becomes available.

## Run-Before-Save Rule

The Save button is **disabled** until the cross-tab has been run. If the user hovers over Save without having run, a tooltip appears:

> "Please run the cross-tab before saving."

This makes the required sequence explicit in the UI rather than letting the user reach a save-then-discover-run state.

## What Triggers the Run Button Being Enabled

Eg: When the user adds a new variable to the column or row, the Run button becomes enabled and the Save button becomes disabled — because the cross-tab is not yet run with the new configuration.

## Confirmation Dialogues

There are two distinct states when the user tries to leave without completing the run-and-save flow:

**State 1 — Not run, then clicks back or reload:**
A new dialogue appears with two options:
- Run and save
- Discard (without saving)

**State 2 — Run but not saved, then clicks back:**
The existing confirmation dialogue appears: "Changes are not saved. Do you want to save?"

The two dialogues are intentionally different because the user's state is different — in State 1 the cross-tab is in an unrun, unsaved state; in State 2 the run has completed but the save step was skipped.

## Rejected Alternative

Auto-run on Save was considered and rejected. See [[Run Before Save]].

---

*Sources: [[Enlyta Discussion]]*
*Updated: 2026-05-20*
