# How to Use LifeBase

This file is for you, not for the LLM processing workflow.

## What Goes Where

Use `raw/knowledge/inbox/` for new articles, videos, essays, research, PDFs, and learning material that should become part of the durable knowledge wiki.

Use `raw/work/inbox/` for messy work capture: meeting notes, todos, PRD snippets, requirements, research notes, Slack summaries, PDFs, and pasted work notes.

Use `raw/thoughts/inbox/` for personal thoughts, ideas, reflections, and loose notes.

Attachments should live in the matching domain assets folder:

```text
raw/knowledge/assets/
raw/work/assets/
raw/thoughts/assets/
```

## How To Ask The LLM

```text
Process new knowledge sources.
Process work inbox.
Process thought inbox.
Show me open Cross Tabs tasks.
Why did we decide X for Cross Tabs?
```

## Mental Model

`AGENTS.md` is the router. The detailed rules live in `rules/`.

`raw/` is where source material lands.

`wiki/` is durable knowledge.

`work/` is operational product memory.

`thoughts/` is personal idea memory.

