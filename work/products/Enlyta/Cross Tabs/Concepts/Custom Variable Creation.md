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

There are three output modes — text, number, and variable. The rule model is shared; only the kind of output assigned differs.

In Cross Tabs, the output value is used as a column name / column label. This was clarified for the difference between text and number output: both can appear as table labels, and number output does not by itself enable numeric calculations. See [[Custom Variable Output as Column Name]].

**Scope for initial release:** only text and numeric output are in scope. Variable output is deferred to a post-release milestone. See [[Variable Creation Scope]].

**Output type is set at variable level:** the "Set Output To" selector applies to the whole variable, not to individual values. A variable cannot mix output types across its values. See [[Variable Creation Scope]].

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

## Output Modes

Each mode has its own detail page.

- [[Custom Variable - Text Output]] — Fixed text labels; behaves as a categorical variable. Used for segmentation and readable groups.
- [[Custom Variable - Number Output]] — Fixed numeric-looking labels; behaves as numeric-coded categories in count crosstabs. Metric aggregation (mean / sum / average / score) is not part of the current Cross Tabs flow.
- [[Custom Variable - Variable Output]] — Copies values dynamically from another variable. Used to combine values split across multiple source variables into one analysis variable.

## Output Type Comparison

|   | Text Output | Number Output | Variable Output |
|---|---|---|---|
| Assigns | Fixed text label | Fixed numeric-looking label | Value from another variable |
| Used for | Segmentation, readable groups | Numeric-coded column labels / score buckets | Combining split variables |
| Example | `Young Adult` | `100` | `Apple` (copied from Mobile Brand) |

## Open Threads

- Confirm rule precedence (first-match-wins) explicitly across all three output modes.
- Confirm no-match behaviour (blank vs. missing vs. "Uncategorized" vs. null).
- Edge cases when user switches output type between text and numeric after partial setup.

---

*Sources: [[Custom Variable Creation - Text Output]] · [[Custom Variable Creation - Number Output]] · [[Custom Variable Creation - Variable Output]] · [[Crosstabs Decision Making]]*
*Updated: 2026-06-01*
