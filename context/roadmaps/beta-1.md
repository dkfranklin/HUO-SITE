---
type: roadmap
status: draft
created: 2026-10-10
owners: [Noggie, JP]
---

# Milestones

Same phases as Notion *MVP Scope & Timeline*, at about 10 hrs/wk. A milestone is done when every story in it meets its acceptance criteria with passing tests, the milestone's evals pass, and the demo works on a real phone. Re-plan hours at the end of each one.

Each milestone breaks into **plans**: one plan per story or small group of stories, written so an implementer agent can pick it up cold. A plan says the goal, the files it may touch, the tests to write first, and the eval it must pass. Plans get written at the start of each milestone, not all up front, so they reflect what we learned.

| M | Name | Dates (target) | Stories | Exit demo |
| --- | --- | --- | --- | --- |
| **M0** | Ready to build | now → Oct 18 | – | Repo laid out for agents. These docs reviewed by Noggie and JP and moved into the repo. Data model agreed. Q1–Q6 answered. CI running on an empty Expo app |
| **M1** | Foundation | Oct 19 → Nov 15 | ACC-01..04, TEAM-01, TEAM-03, PLT-01..04 | On a real phone: enter an invite code, sign up with an email code, pick Creative, see your talent-call answers prefilled. JP signs into the team page and sees signups |
| **M2** | Profiles | Nov 16 → Dec 13 | PRO-01..05, PLT-05 | A model sets up a full profile with headshots and comp card. A business sets up its profile. Both look like Rob's design |
| **M3** | Gig loop | Dec 14 → Jan 31 | GIG-01..05, APP-01..04, PRJ-01..05, TEAM-02, TEAM-04 | A business posts a gig; a creative finds and applies; another is invited; the business selects one; the project goes Scheduled → Completed with both confirming; the gig shows Filled. JP sees it all on the team page. *(Includes a holiday week off.)* |
| **M4** | Conversations | Feb 1 → Feb 28 | MSG-01, MSG-02, NOT-01 | The same loop with messages and push or email at each step |
| **M5** | Trust and ship | Mar 1 → Mar 28 | SAF-01..03, ACC-05 | Report, block and delete account work. TestFlight, Play internal and web are live. Bug bash done |
| **Beta** | Closed beta | ~Apr 1, 2027 | – | Pre-Beta 1 creatives and the 4 businesses from JP's sheet are invited |

The beta date moved about a week later than the Notion page's late-March target, because M0 runs to Oct 18. If real hours average 7 a week, expect beta around May.

## Story to milestone checklist

Implementers tick these off in the repo version of this file, so anyone can see where things stand.

- M1: ACC-01 · ACC-02 · ACC-03 · ACC-04 · TEAM-01 · TEAM-03 · PLT-01 · PLT-02 · PLT-03 · PLT-04
- M2: PRO-01 · PRO-02 · PRO-03 · PRO-04 · PRO-05 · PLT-05
- M3: GIG-01 · GIG-02 · GIG-03 · GIG-04 · GIG-05 · APP-01 · APP-02 · APP-03 · APP-04 · PRJ-01 · PRJ-02 · PRJ-03 · PRJ-04 · PRJ-05 · TEAM-02 · TEAM-04
- M4: MSG-01 · MSG-02 · NOT-01
- M5: SAF-01 · SAF-02 · SAF-03 · ACC-05

## Things that can move the dates

- **Messaging:** Supabase Realtime by hand vs. a hosted chat service (Stream). Stream saves 1–2 weeks and costs money after its free tier.
- **Web build:** if web slows mobile down, ship web after beta. The team page is web-only either way.
- **Answers to Q1 and Q2:** if the team wants the feed or the contract module in Beta 1, M3 grows by weeks.
