---
type: concept
sources:
  - "[[Creating a Dynamic UX - Guidance for Generative AI Applications]]"
created: 2026-05-28
updated: 2026-05-28
---

# Generative AI UX Design

A practical model for designing the user experience of generative AI ("copilot") features, from Microsoft's UX guidance. It rests on three things: choosing the right level of focus, grounding the design in three principles, and building a collaborative input→output loop.

## Choosing a focus framework

Rule of thumb: the more important the task, the more screen real estate it deserves.

- **Immersive** — full canvas; whole-knowledge-base focus for deep analysis tied to specific data sources.
- **Assistive** — in-app side-bar that extends existing functionality without tool-switching; good for ongoing support.
- **Embedded** — single-entry pop-up scoped to one entity/action; context-aware help with no permanent footprint.

These can be combined — embedded pairs well with immersive or assistive.

## Three foundational principles

1. **Human in control.** The user is the pilot; the copilot is a tool. Provide transparency and meaningful controls. Keep action verbs off the copilot ("Summarize with copilot," not "Copilot, summarize").
2. **Avoid anthropomorphizing.** Give it a machine voice ("processing/analyzing," not "understand/think/feel"). First-person "I" is fine; avoid "we/us" standing for the company. Go light on personality.
3. **Consider direct and indirect stakeholders.** Design for everyone the output affects, with attention to vulnerable stakeholders and unintended consequences.

## Collaborative UX (input/output design)

The core defence against fabrication is a tight feedback loop letting users steer the model.

- **Inputs:** offer suggestions and affordances (large boxes, character counters, promptbooks); encourage detail by splitting one prompt into several fields; allow tone customization; support multimodal/multilingual input.
- **Outputs:** show inputs and outputs together; keep prompt/output history; **add appropriate friction** at save/share/copy/paste so users take ownership; encourage fact-checking with citations and direct quotes; let users edit outputs; withhold outputs when an answer would be inappropriate (use predefined experiences for sensitive topics); let users rate, correct, and comment.

## Notable ideas

- **Appropriate friction is good.** A deliberate inversion of frictionless-design dogma: because copilots are probabilistic and can be wrong, slowing users at commitment points builds a correct mental model and accountability. Contrast with the [[Hook Model]], which works to minimise friction in the action step — the two reconcile by treating friction as task-dependent.
- **Set expectations honestly.** A copilot predicts text without understanding truth; the UX must communicate capabilities and error rates up front (mirrors guidelines G1–G2).

## Related pages

- [[Human-AI Interaction Guidelines]] — the research foundation; its four phases map onto this model's lifecycle advice
- [[Creating a Dynamic UX - Guidance for Generative AI Applications]]
