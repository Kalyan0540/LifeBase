---
type: decision
status: accepted
---

# String-Only Custom Variable Output

For Cross Tabs custom variable creation, the confirmed scope is to use one output type: string.

## Context

In the weekly PM sync, Kristina and the team confirmed that designs should use only one output type. The note describes this as "a string output type."

## Reasoning

Number and string output types are not used directly in the table. They are mostly used as column or row labels. Because both output types end up serving the same label role, keeping number and text as separate output types does not add value.

## Impact

- Update the custom variable creation designs to use only one string output type.
- The earlier initial-release scope of supporting both text and numeric output is superseded.
- Variable output remains out of scope unless a later decision reopens it.

---

*Sources: [[2026-06-05 Today's Note]]*
*Updated: 2026-06-05*
