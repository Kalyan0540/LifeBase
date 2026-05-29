---
type: source
source_title: "The RIGHT Way to Deploy A Claude AI Website + FREE Database (Nobody Explains This)"
source_url: "https://www.youtube.com/watch?v=MQk8xyZEKYg&list=WL&index=17"
raw_path: "raw/knowledge/technology/ai/The RIGHT Way to Deploy A Claude AI Website + FREE Database (Nobody Explains This).md"
created: 2026-05-28
updated: 2026-05-28
---

# The RIGHT Way to Deploy a Claude AI Website + Free Database

A YouTube tutorial (Darrel Wilson) walking through how to take a website built with Claude from local development to a live domain, with continuous deployment and an optional free database. The value is the end-to-end plumbing that most "build a site with AI" tutorials skip.

## Local setup

- Build the site with Claude (the desktop app + Claude Code). Instruct it to use **Next.js** — a clean, widely-used framework that deploys well.
- Install **Node.js** (to run JavaScript locally) and **Git** (for version control / local hosting).
- Preview via localhost or the Claude app's built-in preview while iterating.

## Push to GitHub

- Have Claude initialise a Git repository and commit everything.
- Create a GitHub repo, set the Git identity for the repo, and link/push using the standard "push an existing repository" commands. The project now lives in GitHub, ready for a host to fetch.

## Connect a domain (Hostinger)

- Hostinger is chosen specifically because it has a **Node.js app installer** that fetches the GitHub repo and auto-deploys to a live domain.
- Pick a plan (12 months qualifies for a free domain), register the domain, then under "deploy Node.js web app" connect GitHub, select the repo, confirm the detected Next.js framework, and deploy.
- **Continuous deployment:** changes pushed to GitHub are pulled and reflected on the live site automatically — but only when you instruct a push, so a bad edit won't go live by accident.
- Extras available: SSL, malware protection, CDN, and business email forwarding on the domain.

## Connect a database (Supabase, optional)

- Create a free project at supabase.com (this provisions a hosted Postgres database).
- Add Supabase as a connector in Claude (Settings → Connectors → browse → Supabase → authorize), and set tool permissions to "always allow" for read and write/delete to avoid repeated prompts.
- Use Supabase's **MCP** connect option (client = Claude Code) to install the agent commands, then instruct Claude to integrate Supabase to make the Next.js app dynamic — no auth, allow all users to submit forms — providing the required client library and the environment variables for local testing (added to the `.env` file).
- Verify locally via Supabase's table editor (test leads appear), then commit and push to the main branch.
- **Production:** adjust `.gitignore` to allow the production environment file, add the two production variables from Supabase, commit and push so Hostinger can talk to Supabase. Hostinger acts as the middle layer keeping Claude, GitHub, and Supabase in sync.
- Debugging: if a deployment fails, open it in Hostinger to read the error, paste the error back to Claude to self-correct, and force a merge to the main branch if changes landed on a side branch.

## Connections

A hands-on counterpart to the conceptual AI material in this wiki — where [[Generative AI UX Design]] covers *how* an AI app should behave, this covers the practical deployment pipeline (Claude → GitHub → Hostinger → Supabase).

## Links

- [[Deploying AI-Generated Websites]] — the workflow concept distilled from this source
