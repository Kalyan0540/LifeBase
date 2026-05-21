# LifeBase Agent Router

Read this file first. Then read the specific agent rule file for the kind of request the user is making.

Agent rule files live in `_agents/` alongside this file.

## Routing

- Knowledge/wiki request: read `_agents/AGENTS - Wiki.md`
- Work/product/task request: read `_agents/AGENTS - Work.md`
- Thoughts/ideas request: read `_agents/AGENTS - Thoughts.md`

If the request crosses areas, read all relevant rule files. Keep these systems separate unless the user explicitly asks to connect or promote material between them.

## Vault Map

```text
LifeBase/
├── _agents/
│   ├── AGENTS.md
│   ├── AGENTS - Wiki.md
│   ├── AGENTS - Work.md
│   ├── AGENTS - Thoughts.md
│   └── README - How to Use LifeBase.md
├── index.md
├── log.md
├── raw/
│   ├── knowledge/
│   ├── work/inbox/
│   ├── thoughts/inbox/
│   └── assets/
├── wiki/
├── work/
│   ├── Work Index.md              ← master entry point (stays at root)
│   ├── patterns/                  ← work-level patterns (cross-product)
│   │   ├── Patterns Index.md
│   │   └── [one file per pattern]
│   ├── tasks/                     ← task tracking
│   │   ├── Work Tasks.md
│   │   └── Work Task History.md
│   ├── tracking/                  ← processing pipeline & ops
│   │   ├── Work Inbox Index.md
│   │   ├── Work Needs Triage.md
│   │   └── Work Log.md
│   └── products/
│       ├── Enlyta/
│       │   ├── Enlyta - Index.md
│       │   ├── Cross Tabs/
│       │   │   ├── Cross Tabs - Index.md
│       │   │   ├── Cross Tabs - Tasks.md
│       │   │   ├── Concepts/
│       │   │   └── Decisions/
│       │   └── Design System/
│       │       ├── Design System - Index.md
│       │       ├── Design System - Tasks.md
│       │       ├── Concepts/
│       │       └── Decisions/
│       ├── Catalyst/
│       │   ├── Catalyst - Index.md
│       │   └── AI Summarisation/
│       │       ├── AI Summarisation - Index.md
│       │       ├── AI Summarisation - Tasks.md
│       │       ├── Concepts/
│       │       └── Decisions/
│       └── AI/
│           ├── AI - Index.md
│           ├── AI - Tasks.md
│           ├── Concepts/
│           └── Decisions/
└── thoughts/
```

## Global Rules

- Do not process `_agents/README - How to Use LifeBase.md`.
- Do not process anything in `duplicates/`.
- Do not process files with `duplicate` in the filename.
- Do not process files named `_README.md` inside `Concepts/`, `Decisions/`, or `Patterns/` folders — they are placeholder markers.
- Existing captured files in `raw/` are source material. Do not edit their contents unless the user explicitly asks.
- `index.md` is only the top-level map. Detailed work indexing belongs in `work/Work Index.md`; detailed thoughts indexing belongs in `thoughts/Thoughts Index.md` and so on.
- Keep language simple and close to the user's notes.
- Obsidian resolves links by filename. Page filenames should match the visible link text exactly.
- Metadata is for the LLM, not the user. Keep frontmatter minimal. Put IDs, dates, and source links at the bottom of the page.
