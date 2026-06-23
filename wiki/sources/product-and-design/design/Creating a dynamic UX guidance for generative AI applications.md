---
type: source
source_title: "Creating a dynamic UX: guidance for generative AI applications"
source_url: "https://learn.microsoft.com/en-us/microsoft-cloud/dev/copilot/isv/ux-guidance"
raw_path: "raw/knowledge/product-and-design/design/Creating a dynamic UX guidance for generative AI applications.md"
created: 2026-05-28
updated: 2026-05-28
---

# Creating a Dynamic UX - Guidance for Generative AI Applications

A Microsoft Learn article on designing the user experience for generative AI ("copilot") applications. It draws on Microsoft's [responsible AI principles](https://www.microsoft.com/ai/principles-and-approach) and the [HAX (Human-AI Experience) Toolkit](https://aka.ms/haxtoolkit/), and is the practical companion to the research-backed [[Guidelines for Human-AI Interaction]].

## Three UX framework variations

Choose the level of focus by how important the task is — the more important the task, the more screen real estate it deserves.

- **Immersive** — uses the entire canvas for a whole-knowledge-base focus. Best for deep analysis tied to specific data sources (e.g. AI-generated dashboards, security copilots that guide a comprehensive process).
- **Assistive** — an in-app side-bar that extends existing functionality without forcing users to switch tools. Best for ongoing support or monitoring inside an app they already work in.
- **Embedded** — a single-entry pop-up for one entity or action, giving context-aware help without permanent screen space. Best for occasional guidance (e.g. highlight code to invoke help, dive deeper into a chart).

A secondary focus can be layered in — an embedded option pairs well with an immersive or assistive copilot.

## Three foundational principles

A copilot predicts text word-by-word with no inherent understanding of truth, so the UX must set appropriate expectations.

1. **Human in control.** The human is the pilot; the copilot is a tool. Give transparency about abilities, limitations, and the data behind outputs, packaged in meaningful human controls. Language matters: write "Summarize with copilot," not "Copilot, summarize" — keep action words off the copilot so it reads as an assistant.
2. **Avoid anthropomorphizing.** Over-human framing breeds over-reliance. Give the copilot a machine voice (prefer "processing," "analyzing"; avoid "understand," "think," "feel"). First-person singular ("I") is fine and conversational; don't use plural "we/us" to stand in for the company, which lets the copilot appear to speak on its behalf. Go light on personality — the more character, the more it gets humanized.
3. **Consider direct and indirect stakeholders.** Design for everyone the output might affect, not just the primary user, with special attention to vulnerable stakeholders and unintended consequences. Useful questions: How might this output be used and shared? Who is most vulnerable? What happens if the technology fails or is misused?

## Designing across the application lifecycle

This maps onto the four phases of the [[Human-AI Interaction Guidelines]]:

- **First run / initially** — make clear what the system *can* do and *how well* it can do it. Studies show users prefer being shown capabilities and starter suggestions.
- **During interaction** — match relevant social norms; mitigate social biases.
- **When it's wrong** — support efficient correction; make it clear why the system did what it did.
- **Over time** — encourage granular feedback; provide global controls over what the system monitors and how it behaves.

## Collaborative UX

Because copilots can fabricate, the antidote is a tight input→output feedback loop that lets users steer toward their goals.

**Input design:** provide suggestions and affordances (large input boxes, character counters, promptbooks) to get users going; encourage detail by splitting one prompt into several fields; allow tone and other customization; support multimodal and multilingual input.

**Output design:**

- Show inputs and outputs together so users link output quality to input choices.
- Keep a history of prompts and outputs so users can experiment without losing earlier (sometimes better) results.
- **Add appropriate friction** — a deliberate counter to the usual "remove all friction" instinct. Slow users down at save/share/copy/paste moments so they take ownership and accountability for AI-generated content; attach AI disclaimers.
- Encourage fact-checking via citations and direct quotes that point to the exact source location; this also nudges the model toward grounded rather than fabricated answers.
- Let users edit outputs (reinforces the pilot/assistant relationship).
- Withhold outputs when necessary — sometimes no answer beats an inappropriate one. For harmful topics (self-harm, elections) Microsoft recommends predefined experiences rather than a blunt disengage.
- Let users rate, correct, and comment on outputs, and show how feedback improves the experience.

## Connections

This is an applied design layer over the [[Human-AI Interaction Guidelines]] research. The "add appropriate friction" idea is a deliberate inversion of frictionless-design dogma and contrasts interestingly with the [[Hook Model]]'s drive to minimise friction in the action step.

## Links

- [[Generative AI UX Design]] — the concept page distilled from this source
- [[Human-AI Interaction Guidelines]] — the research foundation this article builds on
- [[Guidelines for Human-AI Interaction]] — the source page for those guidelines
