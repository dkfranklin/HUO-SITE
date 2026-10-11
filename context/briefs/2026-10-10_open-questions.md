---
type: brief
status: open
created: 2026-10-10
owners: [Noggie, JP]
---

# Open questions

These came up while turning JP's business plan into buildable stories. Each has a recommendation, so the drafts assume it until the team decides. Answers become decisions in `context/decisions/` (see D-016), then this file is updated.

| # | Question | Where they disagree | Recommendation (drafts assume this) | Who decides |
| --- | --- | --- | --- | --- |
| Q1 | Is the Huo Project in Beta 1, or just "mark as hired"? | Business plan §2.2: every hire is a Huo Project from day one, with contract, invoice and payment built but switched off. D-009: no money in the app, just a "mark as hired" hook | Build the Project as the container (stages, agreed pay, both confirm, timeline, messages), but **don't build** the contract, invoice or payment parts until they're needed. Building them early and leaving them off adds weeks for code nobody uses | JP + Noggie |
| Q2 | Does Beta 1 have the feed? | Business plan §3.3: Home is a portfolio and community feed. D-009: no social feed | No feed. Home is a dashboard of gigs and projects. Portfolios live on profiles. Revisit for Beta 2 | JP |
| Q3 | Invite codes in Beta 1? | Business plan §3.2: beta invite code at launch. MVP Scope doesn't mention it | Yes, it's cheap (ACC-01) and keeps the beta closed. Imported talent-call emails skip the code | JP |
| Q4 | Can anyone DM anyone? | Business plan: DM and connect with anyone. MVP Scope: DMs tied to a gig | Threads only open from an application or invite in Beta 1. That cuts spam and moderation work. Open DMs and Connect come with the social features later | JP + Noggie |
| Q5 | Can the team read private messages? | Not covered | No, only reported messages. Say so in the terms | JP + Noggie |
| Q6 | Which pink is the app's brand token? | Business plan: #FF3C75. CTA site: #E02A62 (darker, so text on it reads better) | #FF3C75 for the logo and large color areas, #E02A62 for text and buttons that need contrast. Two tokens: `brand.pink` and `brand.pinkStrong` | Noggie (design) |
| Q7 | Phone number at signup? | Business plan: name, email, phone. MVP Scope: email OTP, no SMS | Ask for phone as optional, don't verify it. Use email codes only | Noggie |
| Q8 | How long until a project counts as stalled? | Business plan §4.5 and §10 leave it open | Beta 1 shows projects with no change in 7 days to the team, with no automated nudges. Use beta data to set real thresholds | JP |
| Q9 | Revenue timing (P8) | Still open after 10/7 | Doesn't block Beta 1. The Project already records agreed and final pay, which is what any revenue model needs. JP's business conversations (due 10/21) settle it | JP |
