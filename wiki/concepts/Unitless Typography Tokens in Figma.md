---
type: concept
sources:
  - "[[Going Unitless in Figma - Text Line-heights & letter-spacing]]"
created: 2026-07-13
updated: 2026-07-13
---

# Unitless Typography Tokens in Figma

Unitless typography tokens in Figma are a workaround for making design files support implementation-friendly line-height and letter-spacing tokens even when Figma stores fixed pixel values.

## Problem

CSS line-height often uses unitless values, such as `1.5`, because they scale cleanly with font size. Figma variables cannot directly store that as a text-style line-height token, so the design file can drift away from implementation semantics.

## Workaround

Store calculated pixel values in Figma variables and use Code Syntax to show the semantic implementation token in Dev Mode.

Example structure:

- font size: `16px`
- intended line-height: `1.5`
- Figma variable value: `24px`
- Code Syntax: implementation token such as `var(--lh-normal)`

## Operating Rules

- Create only the font-size and line-height combinations the typography system actually uses.
- Scope variables to text properties only.
- Use Code Syntax for developer-facing token names.
- Use descriptions for letter-spacing when Dev Mode does not expose enough context.
- Document the workaround in the design system because the variable names may encode calculated values instead of pure semantic names.

## Design-System Implication

This follows the same principle as [[Colour Token Architecture]]: the implementation token is the stable contract, while the design tool may need an internal representation that serves Figma's constraints.

## Links

- [[Going Unitless in Figma - Text Line-heights & letter-spacing]]
- [[Figma Variables]]
- [[Colour Token Architecture]]
