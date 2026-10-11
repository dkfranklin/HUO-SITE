---
type: domain
status: draft
created: 2026-10-10
owners: [Noggie, JP]
---

# Glossary and voice

Use these words in code, the database, and anything a user reads. When a word here conflicts with older docs or Rob's prototype (`job`, `casting`, `proposal`, `consumer`), this file wins.

## Voice

Huo talks like the Columbus creative scene, not like a staffing agency. That means professional but human, and it uses the words creatives actually use. **"Gig" is the word.** Don't swap it for "opportunity", "job" or "engagement" to sound formal. "Collab" is fine for unpaid or trade work. Keep the editorial confidence of the brand: short sentences, no exclamation-mark hype.

## Terms

| Term | Means | In code | Don't say |
| --- | --- | --- | --- |
| **Creative** | Someone who provides creative talent or services: model, photographer, videographer, stylist, hair and makeup artist, designer, and so on | `creative` account type, `creative_profiles` | talent (fine in marketing, not in UI), freelancer, worker |
| **Business** | Someone who needs creative work: a production company, a brand, a shop, an agency | `business` account type, `business_profiles` | client (except on an invoice later), employer, customer |
| **Gig** | A public post from a business describing work, open to applicants. Includes paid shoots, castings, campaigns and retainers | `gigs` | job, opportunity, listing, posting, casting (casting is a gig *type*) |
| **Collab** | A gig with no cash pay (trade, credit, portfolio) | `gigs.pay_type = 'collab'` | unpaid job |
| **Apply** | A creative raising their hand for a gig | `applications` | submit, bid |
| **Invite** | A business asking a specific creative to a gig ("Invite to gig") | `applications.source = 'invite'` | |
| **Select** | The business picking an applicant. It asks "Start project?" | `applications.status = 'selected'` | hire (hire is the outcome, not the button) |
| **Huo Project** / **project** | The private working relationship created when a business selects a creative. Always one business, one creative | `projects` | booking, contract, job |
| **Stage** | Where a project is: Scheduled → In progress → Delivered → Completed | `projects.stage` | status (reserved for gigs and applications) |
| **Agreed pay** | What the business and creative agreed the gig pays | `projects.agreed_pay_cents`, `pay_type` | rate (fine in copy), price |
| **Complete** | Both sides confirming the work is done. This is the "hired" record (D-009) | `projects.completed_at` | close out |
| **Filled** | A gig whose hires are all made. It stops taking applicants | `gigs.status = 'filled'` | closed (closed means cancelled with no hire) |
| **Portfolio** | A creative's work samples on their profile | `portfolio_items` | posts, feed |
| **Comp card** | A model's card with headshots and measurements | `model_details`, `media` | |
| **Team** | JP, Noggie and anyone else running Huo | `team_members` | admin (fine in code comments) |
| **Talent call** | The Pre-Beta 1 signup form on the website | `talent_call_submissions` | |

## Gig types (Beta 1)

Shoot, casting, event, campaign, content, retainer, other. Businesses pick one. Each gig also names the creative types it needs (model, photographer, videographer, designer, stylist, hair and makeup, other), using the same list as the talent call (`hair_makeup` in code).

## Example copy

- Empty state for a business: "No gigs yet. Post your first gig and we'll get it in front of Columbus creatives."
- Apply button: "Apply"; once applied: "Applied". Withdraw: "Withdraw application".
- Select confirmation: "Select Maya for this gig? This starts a Huo Project with them."
- Completion prompt: "Did this gig get done? Confirm so it's on both your records."
