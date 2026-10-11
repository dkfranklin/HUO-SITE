---
type: story
status: draft
created: 2026-10-10
owners: [Noggie, JP]
area: TEAM
---

## TEAM · Team tools

### TEAM-01 Team page: signups (M1)
Already planned for the CTA site (Notion task "team page"), and kept here so the app reuses it.
- AC1 Team members sign in with an email link. Only allow-listed emails get in. `db` `e2e`
- AC2 The page lists every talent-call and hire-form signup, filters by type, and downloads CSV. `e2e`
- AC3 Each signup can be marked contacted or matched. `db`
- AC4 A "Suggest a change" box tracks requests through suggested, approved, in build, done and not doing. `db`

### TEAM-02 Team page: gigs and projects (M3)
- AC1 The team sees every gig, application and project with its stage, and filters by business or creative. `db` `e2e`
- AC2 Projects that haven't changed stage in 7 days, or were flagged in PRJ-03, show as "Needs a look". `db`

### TEAM-03 Manage invite codes (M1)
- AC1 The team can create, cap and revoke invite codes and see who used each one. `db` `e2e`

### TEAM-04 Post or act on behalf of a business (M3)
Matching by hand continues in Beta 1 (D-004).
- AC1 A team member can post a gig or invite a creative for a business that has asked them to, and it's labelled "Posted by Huo for [business]". `db` `e2e`
