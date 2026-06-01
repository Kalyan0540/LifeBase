---
type: concept
sources:
  - "[[How I Vibe Coded a Recipe App using Claude Code]]"
created: 2026-06-01
updated: 2026-06-01
---

# AI-Assisted App Building

AI-assisted app building is a workflow where a person guides research, product definition, design generation, implementation, testing, and launch preparation through AI tools.

The strongest version is not "ask AI to build an app" in one step. It is a staged workflow:

1. Study a validated reference product.
2. Ask the agent for a feature/page breakdown.
3. Generate high-fidelity UI from the breakdown and visual references.
4. Implement from the generated design files.
5. Wire backend, AI calls, storage, and subscriptions.
6. Test on a real device.
7. Prepare for app store and marketing.

## Practical Principles

- Plan features before generating UI.
- Use visual references when asking for design.
- Keep API keys off the client app.
- Test primary workflows on a real device.
- Treat marketing and distribution as part of the product workflow, not a later afterthought.

## Common Stack

- Expo React Native for mobile apps
- TypeScript for implementation
- Node/Express backend for protected API calls
- OpenAI API for AI features
- Supabase for database
- RevenueCat for subscriptions
- Expo Go for early device testing
