---
type: source
source_title: "Going Unitless in Figma"
source_url: "https://www.designsystemscollective.com/going-unitless-in-figma-a-workaround-f1bc1cee399d"
raw_path: "raw/knowledge/product-and-design/design/Going Unitless in Figma - Text Line-heights & letter-spacing.md"
created: 2026-07-13
updated: 2026-07-13
---

# Going Unitless in Figma

Design Systems Collective article about working around Figma's lack of unitless or percentage typography variables for line-height and letter-spacing.

The article's core workaround: store the calculated pixel values Figma requires, then use each variable's Code Syntax field so developers see the intended semantic token.

## Problem

Figma text styles can show percentage line-height, but number variables only store fixed values. That creates a design-to-code gap when the implementation token should be unitless, such as `line-height: 1.5`.

Without a workaround, teams usually choose between leaving line-height undocumented, using a pixel value that may be implemented literally, or repeatedly adding annotations.

## Workaround

1. Calculate each font-size and line-height combination needed by the typography system.
2. Create number variables for the calculated pixel values.
3. Scope the variables to text properties so they do not appear in unrelated dropdowns.
4. Set Code Syntax for each variable to the implementation token developers should use.
5. Apply the variables in text styles.
6. Test Dev Mode before rollout.

## Scaling Notes

- Start with the combinations the type system actually uses.
- Duplicate a correctly scoped and documented variable to speed up repetitive setup.
- Avoid relying on modes for this workaround because the Code Syntax field does not change by mode.
- Use a bulk syntax tool when many variables need Code Syntax updates.

## Letter-Spacing

Letter-spacing has the same gap. The article suggests using variable descriptions as a fallback when Dev Mode does not expose the converted value clearly enough.

## Durable Notes

- This expands [[Figma Variables]] from colour variables into typography handoff.
- The central design-system pattern is to separate design-tool representation from implementation representation.
- Documentation is part of the system because future maintainers need to know why the line-height variables are organized by calculated pixel values.

## Links

- [[Unitless Typography Tokens in Figma]]
- [[Figma Variables]]
- [[Colour Token Architecture]]
