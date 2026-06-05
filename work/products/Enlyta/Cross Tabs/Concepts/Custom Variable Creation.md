---
type: concept
---

# Custom Variable Creation

Custom variables let users derive a new variable from existing survey variables without overwriting the original. The mental model is rule-based:

```text
IF condition matches
THEN assign output
```

Each rule defines a condition and a value to assign. The system adds a new column alongside the original variable; both remain available for analysis.

The current confirmed scope uses one output type: string. Earlier exploration covered text, number, and variable output modes; those pages remain useful for history and examples, but the active design scope should follow the string-only decision.

In Cross Tabs, the output value is used as a column name / column label. This was clarified for the difference between text and number output: both can appear as table labels, and number output does not by itself enable numeric calculations. See [[Custom Variable Output as Column Name]].

**Scope for initial release:** only string output is in scope. See [[String-Only Custom Variable Output]].

**Reason for one output type:** custom variable outputs are mostly used as column or row labels in the table. Since number and text output do not create different table behaviours, separate output types do not add value.

**Output type history:** the earlier decision set output type at the variable level, not at the individual value level. The latest scope removes the need to choose between text and numeric output for the initial design. See [[Variable Creation Scope]].

## Shared Behaviour

These behaviours apply across all three output modes.

**Original variables are preserved.** Creating a custom variable adds a new derived column. The original variable still exists and is still usable in crosstabs, filters, and charts.

**First-match-wins.** When multiple rules match the same row, the system applies the first matching rule. Mentioned explicitly in the text-output source. It appears to apply across all output modes, but is not yet explicitly confirmed for number or variable output.

**No-match behaviour.** If no rule matches a row, the system may return:

- blank
- missing
- uncategorized
- null

Final no-match behaviour is open.

## Historical Output Modes

Earlier output-mode exploration has its own detail page.

- [[Custom Variable - Text Output]] — Fixed text labels; behaves as a categorical variable. Used for segmentation and readable groups.
- [[Custom Variable - Number Output]] — Superseded for the current release scope. Earlier notes explored fixed numeric-looking labels as numeric-coded categories in count crosstabs.
- [[Custom Variable - Variable Output]] — Deferred. Earlier notes explored copying values dynamically from another variable.

## Output Type Comparison

|   | Text Output | Number Output | Variable Output |
|---|---|---|---|
| Assigns | Fixed text label | Fixed numeric-looking label | Value from another variable |
| Used for | Segmentation, readable groups | Numeric-coded column labels / score buckets | Combining split variables |
| Example | `Young Adult` | `100` | `Apple` (copied from Mobile Brand) |

## Open Threads

- Confirm rule precedence (first-match-wins) explicitly across all three output modes.
- Confirm no-match behaviour (blank vs. missing vs. "Uncategorized" vs. null).

---

*Sources: [[Custom Variable Creation - Text Output]] · [[Custom Variable Creation - Number Output]] · [[Custom Variable Creation - Variable Output]] · [[Crosstabs Decision Making]] · [[2026-06-05 Today's Note]]*
*Updated: 2026-06-05*
