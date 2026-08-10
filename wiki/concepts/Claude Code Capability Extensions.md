---
type: concept
sources:
  - "[[5 Open Source Repos That Fix 95% of Claude Code's Problems]]"
created: 2026-07-14
updated: 2026-07-14
---

# Claude Code Capability Extensions

Claude Code can be treated as a base coding agent plus specialist extensions for the workflows it does not handle well by default.

## Capability Gaps

- **Video** — transcripts miss visual context. A video skill can add selected frames alongside captions instead of sending every frame.
- **Research** — simple search is shallow, while deep-research agent swarms can be expensive. NotebookLM-style workflows can sit between those extremes for source synthesis.
- **Memory** — large repos and large document sets need maps. A graph layer can give the agent a traversable structure without becoming a full vector RAG system.
- **Design** — frontend quality benefits from visual inspection and targeted design commands, not only terminal-based code edits.
- **Token efficiency** — workflow gates can reduce overbuilding by asking whether a feature already exists, whether a library should be used, and what the smallest useful implementation is.

## Operating Principle

Do not ask one agent surface to be excellent at every modality. Add narrow tools where the workflow has a known weakness, and keep the agent responsible for routing, synthesis, and implementation judgment.

## Related

- [[AI-First Business Systems]]
- [[LLM Wiki Architecture]]
- [[Persistent Knowledge Base]]

---

*Sources: [[5 Open Source Repos That Fix 95% of Claude Code's Problems]]*
*Updated: 2026-07-14*
