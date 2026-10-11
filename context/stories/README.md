---
type: story-index
status: draft
created: 2026-10-10
owners: [Noggie, JP]
---

# User stories

Each story has an ID that plans, branches, tests and evals refer to. Acceptance criteria (AC) are written so each one maps to at least one automated test. **Test** says the cheapest layer that proves it: `unit`, `db` (SQL and row-level security tests), `e2e` (driving the app), or `manual` (checked by a person; keep these rare). **M** is the milestone in [beta-1.md](../roadmaps/beta-1.md).

Roles: **C** = creative, **B** = business, **T** = team (JP, Noggie), **V** = visitor without an account.

## Areas

| Area | File |
| --- | --- |
| Access and accounts | [ACC.md](ACC.md) |
| Profiles | [PRO.md](PRO.md) |
| Gigs | [GIG.md](GIG.md) |
| Applications and invites | [APP.md](APP.md) |
| Huo Projects | [PRJ.md](PRJ.md) |
| Messages | [MSG.md](MSG.md) |
| Notifications | [NOT.md](NOT.md) |
| Trust and safety | [SAF.md](SAF.md) |
| Team tools | [TEAM.md](TEAM.md) |
| Platform (no user-facing story, but required) | [PLT.md](PLT.md) |

Each story gets one GitHub issue, titled `<ID>: <story title>` and labelled `story` plus its milestone (D-016).
