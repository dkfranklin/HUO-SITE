---
type: story
status: draft
created: 2026-10-10
owners: [Noggie, JP]
area: APP
---

## APP · Applications and invites

### APP-01 Apply to a gig (M3)
- AC1 I can apply with an optional note (up to 500 characters). My profile goes with it. `e2e`
- AC2 I can't apply twice to the same gig, or to my own gig. `db`
- AC3 The business is notified (see NOT-01). `e2e`

### APP-02 Withdraw an application (M3)
- AC1 I can withdraw until I'm selected. The business sees it as withdrawn. `db` `e2e`

### APP-03 Review applicants (M3)
As a B, I want one place to compare everyone who applied.
- AC1 My gig dashboard lists applicants with name, creative types, thumbnail, note and applied date. `e2e`
- AC2 I can open each applicant's profile and comp card. `e2e`
- AC3 I can mark an applicant "Shortlist" or "Not a fit". "Not a fit" sends them a polite notice only when the gig is filled or closed. `db` `e2e`
- AC4 Only the gig owner can see its applicants. `db`

### APP-04 Invite a creative to a gig (M3)
As a B, I want to invite someone whose work I like instead of waiting (business plan "Invite to Project").
- AC1 From a creative's profile I pick one of my open gigs and send an invite with an optional note. `e2e`
- AC2 The creative sees the invite and can accept (it becomes an application) or decline. `db` `e2e`
