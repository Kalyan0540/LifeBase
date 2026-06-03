---
type: decision
status: accepted
---

# Custom Variable Edit Synchronisation

Custom variable edits sync automatically for everyone using that variable.

## Decision

When a custom variable is modified, the changes are synchronised automatically. Cross Tabs will not copy the filter pattern where editing a public saved filter creates a draft or duplicate of the original saved filter to preserve its previous state for other users.

Duplicate and use at the custom variable level is deferred until after MVP.

Any custom variable can be further bucketed.

## Contrast With Filters

For filters, when a filter creator modifies a public saved filter that is already used by other users, the system creates a draft by duplicating the original filter. That draft keeps the previous state before the filter was modified.

For custom variables, the decision is different: edits are synchronised automatically instead of keeping a previous-state duplicate.

---

*Sources: [[2026-06-03 Cross Tabs Task and Decision Updates]]*
*Updated: 2026-06-04*
