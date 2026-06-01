---
type: source
source_title: "Karpathy's LLM Wiki Goes Further Than Everyone Realised"
source_url: "https://www.youtube.com/watch?v=ijBJVzxSBRA&t=96s"
raw_path: "raw/knowledge/technology/ai/Karpathy's LLM Wiki Goes Further Than Everyone Realised.md"
created: 2026-06-01
updated: 2026-06-01
---

# Karpathy's LLM Wiki Goes Further Than Everyone Realised

Adam Goodyer applies the LLM Wiki pattern beyond personal notes and into an AI agency operating system. The key move is the same three-layer structure: raw source material, structured wiki/JSON summaries, and schema/rule files that tell agents where to look.

## Core Argument

The LLM Wiki pattern is not only for Obsidian knowledge bases. It can become the memory and navigation layer for an AI-first business system.

Instead of letting agents search everything every time, the system stores:

- raw client inputs, meetings, emails, and media
- structured outputs such as audit JSON, process maps, or storyboards
- schema and skill files that explain how to retrieve and use the right slice of context

This creates controlled context injection. The agent gets the relevant structured memory instead of bloating the context window with raw material.

## Agency Audit Example

The agency audit workflow collects raw material from meeting transcripts, client emails, calls/messages, and client materials.

The structured wiki layer then extracts operational facts such as:

- who performs a task
- who is responsible
- how long it takes
- how often it happens
- what tools are used
- pain points and possible optimisations

That structured data can later power cost-waste calculations, opportunity identification, and client recommendations.

## Video Editor Example

The same structure is used for a video pipeline:

- ingest raw video
- transcribe and analyse audio
- create proxies/clips
- build a structured storyboard
- let Remotion consume the storyboard and assets

The storyboard becomes a wiki-like representation of the final video: transcript segments, motion graphics, zooms, and timing.

## Structure Beats RAG

The speaker argues this is lighter than vector-database RAG for many production workflows. The benefit is not semantic search; it is explicit organisation.

Well-labeled folders, YAML/JSON, skill files, and schemas make it possible to filter context deterministically and keep the agent from wasting work rediscovering structure.

## Key Takeaways

- LLM-wiki-style memory can coordinate many agents or business workflows.
- Raw data should be preserved, but agents should usually work from structured summaries.
- Schema/rule files are part of the product; they tell agents what exists and where to find it.
- Per-agent memory files can accumulate operational knowledge over time.
- The main payoff is lower context bloat and more reliable retrieval.

---

*Concepts: [[AI-First Business Systems]] · [[LLM Wiki Architecture]] · [[Persistent Knowledge Base]]*
*Updated: 2026-06-01*
