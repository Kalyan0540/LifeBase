# Work Rules

Use `work/` for operational product memory: products, concepts, decisions, patterns, tasks, and history.

Raw work notes live in `raw/work/inbox/`. Attachments live in `raw/work/assets/`.

## Start Here

```text
work/Work Index.md                 master work entry point
work/tasks/Work Tasks.md           current global task dashboard
work/tasks/Work Task History.md    chronological task history
work/patterns/Patterns Index.md    cross-product pattern registry
work/tracking/Work Inbox Index.md  processing tracker
work/tracking/Work Needs Triage.md unclear product ownership
work/tracking/Work Log.md          work operation log
work/products/                     parent and sub-product memory
```

Products are organised as parent -> sub-product. A parent with only one product can stay flat until more sub-products appear.

Current map:

```text
Enlyta/
├── Cross Tabs/
└── Design System/

Catalyst/
├── AI Summarisation/
└── Activity Feed/

AI/         (flat: no sub-products yet)
```

## Retrieval Rules

Read only what the query requires. For narrow queries, do not pre-read unrelated products, concepts, decisions, patterns, or raw files.

| Query Type | Start Here | Then Read |
|---|---|---|
| Current product status | Sub-product Index | Concepts, Decisions, Tasks only if needed |
| Open tasks | `work/tasks/Work Tasks.md` | Sub-product Tasks page if needed |
| Completed tasks or history | `work/tasks/Work Task History.md` | `work/tracking/Work Log.md` if needed |
| Why was X decided | Sub-product `Decisions/` | Linked sources if needed |
| How does the product behave | Sub-product `Concepts/` | Linked sources if needed |
| What patterns exist | `work/patterns/Patterns Index.md` | Specific pattern files |
| Unclear product ownership | `work/tracking/Work Needs Triage.md` | Source note if needed |
| New inbox processing | `work/tracking/Work Inbox Index.md` | Read `rules/work/Process Work.md` |

## Core Principles

- The system is a product memory assistant, not an aggressive documentation generator.
- Keep concepts, decisions, and tasks scoped to the product or sub-product they belong to.
- Patterns live at `work/patterns/` because they can apply across products.
- Do not invent content. If something is inferred, mark it as inferred.
- If ownership is unclear, use `work/tracking/Work Needs Triage.md` instead of guessing.

