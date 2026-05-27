# How to Use LifeBase

This file is for you, not for the LLM processing workflow.

## What Goes Where

Use `raw/knowledge/inbox/` for new articles, videos, essays, research, and learning material that should become part of the durable knowledge wiki.

After processing, the LLM moves each knowledge source from `raw/knowledge/inbox/` into the right topic folder under `raw/knowledge/`, then creates or updates the matching wiki pages. Moving the raw file is not enough by itself; it must still be processed into `wiki/`.

Keep the first level under `raw/knowledge/` broad and easy to scan: examples are `product-and-design/`, `technology/`, `health-and-wellness/`, `finance/`, and `mental-models/`. More specific folders should live inside those broad shelves only when there are enough files to justify them.

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

`raw/` is where messy source material lands. New knowledge starts in `raw/knowledge/inbox/`; processed knowledge sources live in broad topic folders under `raw/knowledge/`, with optional subfolders only when a folder becomes crowded.

`wiki/` is durable knowledge.

`work/` is operational product memory. Each sub-product has an Index, a Tasks file, and `Concepts/`, `Decisions/`, `Patterns/` folders. Start from `work/Work Index.md`.

`thoughts/` is personal idea memory. Start from `thoughts/Thoughts Index.md`.

The LLM should read indexes first, then product/topic pages, then raw notes only when needed.
