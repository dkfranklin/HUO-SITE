---
type: outcome
status: draft
created: 2026-10-10
owners: [Noggie, JP]
id: O-001
roadmap: ../roadmaps/beta-1.md
---

# O-001: Beta 1 runs the gig loop

## Why Beta 1 exists

Pre-Beta 1 proved the loop by hand. From JP's tracker (*Pre-BETA Huo Connections*, 10/10): 10 creatives connected with 4 Columbus businesses. 9 gigs are complete and $5,500 has been paid to creatives. A videographer collab with Sole Classic is in progress. JP and Rob did every match through texts, calls and a spreadsheet.

Beta 1 puts that loop into an app, so it runs without JP in the middle of every message, and so every hire leaves a record.

## The outcome

> A Columbus business can post a gig, find or hear from the right creatives, pick one, and run the work to completion inside Huo. Both sides end up with a record of who did what, for how much. JP can see all of it.

## Success measures for Beta 1

The business plan's exit bar is the target. The numbers in brackets are proposed and still need team sign-off.

| Measure | Target | How we measure it |
| --- | --- | --- |
| Core flows stable | Post gig, apply, message, start project and complete project all work with no critical bugs for 2 straight weeks | Sentry crash-free sessions ≥ 99%; zero open P0 bugs |
| Gigs actually run through the app | [≥ 10 projects completed in the first 6 weeks of beta] | `projects.status = 'completed'` |
| Organic use | [≥ 50% of gigs posted by businesses without JP doing it for them] | `gigs.created_by` is not a team member |
| Creatives get hired | [≥ 30% of active creatives on at least one project] | Distinct creatives on projects / creatives active in 30 days |
| Pre-Beta 1 cohort arrives | [≥ 60% of imported signups claim their profile] | Imported profiles with a confirmed login |
| Repeat bookings | [≥ 1 business books the same creative twice] | Projects grouped by business and creative pair |

## In scope (Beta 1)

These come from D-009 and MVP Scope, adjusted to the business plan's language:

- **Two account types:** Creative and Business. One person can be both (multi-select, as in the business plan §3.1).
- **Invite-only access** through a beta invite code (business plan §3.2). See open question Q3.
- **Profiles:** creatives have a portfolio, skill tags and model fields (measurements, headshots, comp card), because models are first class (D-009). Businesses have a basic profile.
- **The gig loop:** post a gig, browse and search, apply, invite a creative, select, then the Huo Project runs through its stages to Completed.
- **Huo Project as the container** for every hire from day one (business plan §4). In Beta 1 it holds the gig details, the agreed pay, stages, messages and history. The contract, invoice and payment parts are *not* built yet. The Project records the agreed pay and has both sides confirm completion, which is D-009's "mark as hired" hook. See Q1.
- **Messaging** tied to an application or project.
- **Notifications:** push and email.
- **Trust and safety:** report, block, terms acceptance, account deletion (App Store requirement).
- **Team tools:** the /team page for JP (signups, contacted/matched, CSV, suggest-a-change), growing into a view of every gig and project.
- **Import** of the CTA signups so Beta 1 doesn't launch empty.

## Out of scope (Beta 1)

- Money moving through Huo: contracts, invoices, payments and transaction fees (D-009; business plan says these switch on at Public Launch).
- Huo Pro and Business Pro (Beta 2).
- Consumer and Talent Agency accounts (business plan §9).
- The portfolio and community feeds, likes, comments and the saved tab (D-009; see Q2).
- Build a team, find collaborators, ask the community.
- Referral codes (Beta 2 growth mechanism).
- Stalled-project automation (thresholds still open; Beta 1 shows stalled projects to the team instead).
- Public App Store launch. Beta runs on TestFlight, Play internal testing and the web.

## Constraints

- **Stack:** Expo (iOS, Android, web from one codebase), expo-router, Supabase (Postgres, Auth, Storage, Realtime), EAS builds, Sentry, PostHog (D-003, MVP Scope).
- **Capacity:** about 10 hrs/wk from Noggie, AI-assisted. Target closed beta around late March 2027.
- **Brand:** editorial, minimalist and bold. Pink HUO wordmark on black. The business plan's pink is #FF3C75; the CTA site uses #E02A62 for text contrast. Which one is the app token is Q6.
