---
type: story
status: draft
created: 2026-10-10
owners: [Noggie, JP]
area: PRJ
---

## PRJ · Huo Projects

### PRJ-01 Select a creative and start a project (M3)
- AC1 On an applicant, "Select" asks "Select [name] for this gig? This starts a Huo Project with them." Confirming creates the project. `e2e`
- AC2 The project copies the gig's title, dates, location, deliverables and pay, so nothing is typed twice. `db`
- AC3 Business and creative can both edit the agreed pay before the project starts, and the other person sees the change. `db` `e2e`
- AC4 A multi-hire gig creates one project per selected creative. Each is private to that business and creative. `db`
- AC5 Only the two participants (and the team) can read a project. `db`

### PRJ-02 Move a project through its stages (M3)
- AC1 Stages are Scheduled → In progress → Delivered → Completed. Either participant can move it forward. `db` `e2e`
- AC2 Each stage change is timestamped and shown as a timeline on the project. `db` `e2e`
- AC3 Optional milestones can be added inside In progress (for example Editing or Revisions). `e2e`

### PRJ-03 Confirm the gig is done (M3)
This is the "mark as hired" record (D-009) and the hook for invoicing and fees later.
- AC1 When the project is Delivered, both sides get "Did this gig get done?" with the agreed pay shown. `e2e`
- AC2 It becomes Completed only when both confirm. The final pay amount is saved. `db`
- AC3 If one side says it didn't happen, the project is flagged for the team. `db` `e2e`
- AC4 Completion adds the project to both profiles' history (PRO-04 AC3). `db`

### PRJ-04 See my projects (M3)
- AC1 A Projects list shows active projects first, then completed, for whichever account type I'm acting as. `e2e`

### PRJ-05 Cancel a project (M3)
- AC1 Either side can cancel before Completed with a reason. The other side is notified and the team can see the reason. `db` `e2e`
- AC2 Cancelling reopens a filled gig if it has open hire slots. `db`
