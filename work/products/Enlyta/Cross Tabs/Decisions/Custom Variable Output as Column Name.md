---
type: decision
status: accepted
---

# Custom Variable Output as Column Name

For Cross Tabs, custom variable outputs should be understood as column names / column labels in the table.

This means text output and number output both behave as table labels when they are used as columns. The number output should not imply that Cross Tabs supports numeric calculations for that output.

## Context

The question was whether "set output as number" and "set output as string" are meaningfully different if both become column names. The clarification from Pradnya was that the output is being determined as the column name.

## Implication

Use language that keeps the user's mental model close to what Cross Tabs can currently do:

- the output value names the resulting column/category
- numeric-looking output can appear as a column label
- numeric calculations are not supported by this Cross Tabs flow right now

---

*Sources: [[Crosstabs Decision Making]]*
*Updated: 2026-06-01*
