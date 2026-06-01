---
type: concept
sources:
  - "[[Karpathy's LLM Wiki Goes Further Than Everyone Realised]]"
created: 2026-06-01
updated: 2026-06-01
---

# AI-First Business Systems

An AI-first business system uses agents, skills, structured memory, and integrations to run repeatable business workflows.

The important idea is that agents need more than prompts. They need an organised operating environment:

- raw inputs from real work
- structured summaries and JSON/YAML stores
- schema or rule files explaining where things live
- workflow-specific skills
- per-agent memory that accumulates over time

## Why It Matters

As the number of projects, clients, agents, or workflows grows, raw context becomes too large for the agent to inspect from scratch. A structured wiki layer gives the agent a map.

This makes the agent's work more reliable because it can retrieve the right context directly instead of guessing which files matter.

## Common Structure

```text
raw inputs -> structured wiki/memory -> schema + skills for agent retrieval
```

The same pattern can apply to client audits, video editing, content production, software delivery, or internal operations.
