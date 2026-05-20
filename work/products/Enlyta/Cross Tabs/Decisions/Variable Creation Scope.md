---
type: decision
status: accepted
---

# Variable Creation Scope

Two related decisions that narrow the scope and change the structure of custom variable creation for the initial release.

## Decision 1 — Output Type Is Set at Variable Level

The "Set Output To" setting is configured at the variable level, not at the individual value level.

**Reasoning:** Setting output type per value was logically inconsistent — a single variable could end up with text output for some values and numeric output for others. This makes no sense as a data model. Errors would only surface at the end, not upfront.

**UI impact:** The output type selector moves from the per-value row to the variable-level settings.

## Decision 2 — Variable Output Type Is Deferred

Only numeric and text are supported as output types in the initial release. Variable output (copying values dynamically from another variable) is deferred to a post-initial-release milestone.

**Reasoning:** Variable output is a separable capability. Shipping text and numeric first keeps the initial scope manageable without blocking the core use cases.

---

*Sources: [[Enlyta Discussion]]*
*Updated: 2026-05-20*
