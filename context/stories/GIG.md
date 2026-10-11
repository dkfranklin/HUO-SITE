---
type: story
status: draft
created: 2026-10-10
owners: [Noggie, JP]
area: GIG
---

## GIG · Gigs

### GIG-01 Post a gig (M3)
As a B, I want to post a gig so Columbus creatives can apply.
- AC1 Fields: title, gig type, creative types needed, description, date(s) or "flexible", location (address or "remote"), pay type (flat, hourly, day rate, collab), pay amount (required unless collab), number of hires (default 1), deliverables, requirements, usage/rights (optional), application deadline (optional). `unit` `e2e`
- AC2 Posting makes the gig `open` and visible in browse. `db` `e2e`
- AC3 I can save as a draft. `e2e`
- AC4 Posting is free and unlimited (MVP Scope). `db`

### GIG-02 Edit, close or reopen my gig (M3)
- AC1 I can edit an open gig. Applicants get notified when date, pay or location change. `e2e`
- AC2 I can close a gig without hiring. It disappears from browse and applicants are told it closed. `db` `e2e`
- AC3 A gig becomes `filled` automatically when all its hires have projects (see PRJ-01). `db`

### GIG-03 Browse and search gigs (M3)
As a C, I want to find gigs that fit me.
- AC1 Browse lists open gigs, newest first, with gigs matching my creative types on top. `db` `e2e`
- AC2 I can search by text and filter by creative type, gig type, pay type and date. `db` `e2e`
- AC3 Closed, filled and past-deadline gigs never show. `db`

### GIG-04 Search creatives (M3)
As a B, I want to find a specific kind of creative.
- AC1 I can search creatives by text and filter by creative type, skill tag and area, and for models by height range. `db` `e2e`
- AC2 Results show name, creative types, a portfolio thumbnail and completed-project count. `e2e`

### GIG-05 View a gig (M3)
- AC1 Gig detail shows all GIG-01 fields, the business's name and logo, and how many have applied. `e2e`
- AC2 A creative sees Apply, Applied or Invited. The owner sees Manage applicants. `e2e`
