---
type: decision
id: D-016
status: accepted
created: 2026-10-11
owners: [Noggie]
source: "Noggie, project thread \"Next steps after JP update\", 2026-10-11"
---

# D-016: Agent-first repo layout in huo-app/huo-app

## Decision

`huo-app/huo-app` is the single home for Huo's build: context, records, rules and code in one repo. It follows the layout in `CLAUDE.md` (modeled on Noggie's workbench agentic-context repo): `context/` for what we're building and why, `specs/`, `evals/`, `design/`, `apps/app` (Expo), `apps/site` (the CTA site), and `supabase/`. Work flows Roadmap → Outcome → Plan → Story → Spec → PR.

Noggie's three calls on the proposal:

1. **The repo is the source of truth for decisions.** New decisions are added here as `D-###` files. The Notion Decision Log keeps a one-line row per decision that links to the file, because JP reads Notion.
2. **One GitHub issue per story.** Each story ID in `context/stories/` gets an issue; plans link to their issues and PRs close them.
3. **The CTA site keeps deploying from Noggie's fork** (`dkfranklin/HUO-APP`) on Noggie's Vercel Hobby account until Huo has a Vercel team. Until then, site changes are pushed to both repos.

## Why

One app and one builder. Agents get the context and the code in one checkout, and every level of work has one place to live. Vercel Hobby can't deploy from a private org repo, so the site stays on the fork for now.

## Consequences

- Supersedes the Notion Decision Log as the record; rows D1–D15 were imported as D-001 to D-015.
- Open items stay open, not decided: Notion P8 (revenue timing) and the questions in `context/briefs/2026-10-10_open-questions.md`.
