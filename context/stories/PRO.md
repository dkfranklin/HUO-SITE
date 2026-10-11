---
type: story
status: draft
created: 2026-10-10
owners: [Noggie, JP]
area: PRO
---

## PRO · Profiles

### PRO-01 Set up my creative profile (M2)
- AC1 Required: display name, at least one creative type, Columbus area (Columbus / other Ohio / other). Optional: title, bio, skill tags, Instagram, website, rate range. `unit` `e2e`
- AC2 Skill tags are multi-select from a list and allow custom tags. `unit`
- AC3 I can upload up to 12 portfolio images (JPEG, PNG or HEIC, resized server-side, max 10 MB each) and reorder them. `e2e`
- AC4 I can add links to video work (YouTube, Vimeo, Instagram). `unit`

### PRO-02 Add model details and a comp card (M2)
As a model, I want my measurements and headshots on my profile because that's what businesses book from.
- AC1 Model fields appear only if Model is one of my creative types: height, bust, waist, hips, shoe, eyes, hair. Height is required for models (same rule as the talent call). `unit` `db`
- AC2 I can upload up to 4 headshots and 1 full-length shot. `e2e`
- AC3 My comp card view shows those images and measurements in one shareable screen. `e2e`

### PRO-03 Set up my business profile (M2)
- AC1 Required: business name, business type, Columbus area. Optional: logo, about, website, Instagram, contact person. `unit` `e2e`
- AC2 A business profile shows its open gigs. `e2e`

### PRO-04 View someone's profile (M2)
- AC1 Any signed-in user can view any creative or business profile. `db` `e2e`
- AC2 A business viewing a creative sees "Invite to gig" (see APP-04). `e2e`
- AC3 A profile shows completed projects as a count and list ("Worked with Elevate Creative"), without pay amounts. `db` `e2e`

### PRO-05 Edit my profile (M2)
- AC1 Every field from PRO-01 to PRO-03 can be edited, and changes show immediately. `e2e`
