# How to Use LifeBase

This file is for you, not for the LLM processing workflow.

## What Goes Where

Use `raw/knowledge/` for articles, videos, essays, research, and learning material that should become part of the durable knowledge wiki.

Use `raw/work/inbox/` for messy work capture: meeting notes, todos, PRD snippets, requirements, research notes, Slack summaries, and pasted work notes.

Raw work files do not need properties/frontmatter. Plain markdown is fine.

If a work note has screenshots or images, paste/drop them directly into the note in Obsidian. With your attachment setting configured to use an `assets` subfolder under the current folder, Obsidian will place those files beside the note in an `assets/` folder and embed the links in markdown.

Use `raw/thoughts/inbox/` for personal thoughts, ideas, reflections, and loose notes that you may want to retrieve or organize later.

## How To Ask The LLM

For knowledge:

```text
Process new knowledge sources.
```

For work:

```text
Process work inbox.
```

If a note does not clearly mention a product, the LLM should place it in `work/Work Needs Triage.md` instead of guessing.

For thoughts:

```text
Process thought inbox.
```

For product queries:

```text
What is the current status of Cross Tabs?
Why did we decide X for Cross Tabs?
Show me open Cross Tabs tasks.
What did I complete on Cross Tabs last week?
```

## Mental Model

`raw/` is where messy source material lands.

`wiki/` is durable knowledge.

`work/` is operational product memory. Each sub-product has an Index, a Tasks file, and `Concepts/`, `Decisions/`, `Patterns/` folders. Start from `work/Work Index.md`.

`thoughts/` is personal idea memory. Start from `thoughts/Thoughts Index.md`.

The LLM should read indexes first, then product/topic pages, then raw notes only when needed.
