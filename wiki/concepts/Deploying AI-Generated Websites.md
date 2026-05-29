---
type: concept
sources:
  - "[[The RIGHT Way to Deploy a Claude AI Website + Free Database]]"
created: 2026-05-28
updated: 2026-05-28
---

# Deploying AI-Generated Websites

A practical pipeline for taking a website built with an AI coding tool (Claude / Claude Code) from local development to a live, database-backed site with continuous deployment. The throughline: connect a few standard services so edits flow automatically from the AI to the live site.

## The pipeline

```
Claude (build) → GitHub (version control) → Hostinger (host + domain) → Supabase (database)
```

## Stage 1 — Build locally

Build with Claude and instruct it to use **Next.js** (clean code, deploys well). Install **Node.js** (run JS locally) and **Git** (version control). Preview via localhost or the Claude app preview while iterating.

## Stage 2 — Push to GitHub

Have Claude initialise a Git repo and commit. Create a GitHub repo, set the repo's Git identity, and push using the standard "push an existing repository" commands.

## Stage 3 — Host on a domain (Hostinger)

Hostinger is chosen for its **Node.js app installer**, which fetches the repo and auto-deploys. Pick a plan (12 months → free domain), connect GitHub, select the repo, confirm the detected Next.js framework, and deploy. **Continuous deployment:** pushes are reflected live automatically, but only when you instruct a push — so mistakes don't auto-publish. Extras: SSL, malware protection, CDN, business email.

## Stage 4 — Add a database (Supabase, optional)

Create a free Supabase project (hosted Postgres). Add Supabase as a Claude connector and set read + write/delete tool permissions to "always allow." Use Supabase's **MCP** connect flow (client = Claude Code) to install agent commands, then instruct Claude to integrate Supabase, supplying the client library and the env vars (in `.env`) for local testing. Verify locally in Supabase's table editor, then commit/push. For production: allow the production env file in `.gitignore`, add the two production variables, commit and push. Hostinger acts as the middle layer keeping Claude, GitHub, and Supabase in sync.

## Debugging tip

If a Hostinger deployment fails, open it to read the error, paste the error back to Claude to self-correct, and force a merge to the main branch if changes landed on a side branch.

## Related pages

- [[The RIGHT Way to Deploy a Claude AI Website + Free Database]]
- [[Generative AI UX Design]] — the behaviour/UX layer over apps built this way
