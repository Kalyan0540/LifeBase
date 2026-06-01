---
type: concept
sources:
  - "[[LLM Wiki — Karpathy]]"
  - "[[Karpathy's LLM Wiki Goes Further Than Everyone Realised]]"
created: 2026-05-07
updated: 2026-06-01
---

# LLM Wiki Architecture

The three-layer architecture behind the [[Persistent Knowledge Base]] pattern described in [[LLM Wiki — Karpathy]]. This wiki is an implementation of it.

The same architecture can also be used as an operating layer for business workflows and agents: raw work inputs, structured wiki/JSON memory, and schema/skill files that tell agents exactly where to retrieve context. See [[Karpathy's LLM Wiki Goes Further Than Everyone Realised]] and [[AI-First Business Systems]].

## Layer 1 — Raw sources

Immutable source documents. Articles, papers, transcripts, images, data files. The LLM reads from them but never modifies them. Source of truth.

Location: `raw/`, with domain-specific attachments in `raw/knowledge/assets/`, `raw/work/assets/`, and `raw/thoughts/assets/`.

## Layer 2 — The wiki

LLM-generated markdown pages. Summaries, entity pages, concept pages, comparisons, synthesis, query results. The LLM owns this layer entirely — creates pages, updates them, maintains cross-references.

Location: `wiki/` and subdirectories.

## Layer 3 — The schema

A config document (here: `AGENTS.md`) that tells the LLM how the wiki is structured, what conventions to follow, and what workflows to run for each operation. Co-evolved by the human and LLM over time.

## Navigation files

- **index.md** — small top-level map for the whole LifeBase vault.
- **Wiki Index.md** — content-oriented catalog for durable knowledge. LLM reads it first for wiki queries.
- **Wiki Log.md** — append-only chronological record for wiki operations.

## Operations

- **Ingest** — read source → create/update pages → update wiki index → append wiki log entry
- **Query** — read the relevant index → read relevant pages → synthesise → optionally file result
- **Lint** — scan for orphans, contradictions, stale content, missing cross-refs

## Related pages

- [[LLM Wiki — Karpathy]]
- [[Persistent Knowledge Base]]
- [[Obsidian]]
