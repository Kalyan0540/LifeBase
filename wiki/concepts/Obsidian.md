---
type: concept
sources:
  - "[[LLM Wiki — Karpathy]]"
created: 2026-05-07
updated: 2026-05-27
---

# Obsidian

A local-first markdown note-taking app used as the interface for browsing this wiki. In the [[LLM Wiki — Karpathy]] pattern, Obsidian is the IDE — the LLM edits files, the human browses results in real time.

## Relevant features

- **Graph view** — visualises connections between pages. Best way to see the shape of the wiki: which pages are hubs, which are orphans.
- **Wiki links** — Obsidian-style links between notes. Used throughout this wiki for cross-references.
- **Web Clipper** — browser extension that converts web articles (including YouTube transcripts) to markdown. Primary method for getting sources into `raw/`.
- **Download attachments hotkey** — `Settings → Hotkeys → Download attachments for current file`. Saves images locally so they do not rely on external URLs. In LifeBase, use the matching domain assets folder such as `raw/knowledge/assets/` or `raw/work/assets/`.
- **Dataview plugin** — runs queries over page frontmatter. Can generate dynamic tables from tags, dates, source counts.
- **Marp plugin** — renders markdown as slide decks. Useful for generating presentations from wiki content.

## Related pages

- [[LLM Wiki Architecture]]
- [[Persistent Knowledge Base]]
- [[LLM Wiki — Karpathy]]
