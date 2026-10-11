---
type: story
status: draft
created: 2026-10-10
owners: [Noggie, JP]
area: ACC
---

## ACC · Access and accounts

### ACC-01 Enter a beta invite code (M1)
As a V, I want to enter my invite code so I can get into the beta.
- AC1 A valid, unused code moves me to sign up. `e2e`
- AC2 An invalid or used-up code shows "That code isn't valid. Check with whoever sent it." and doesn't let me continue. `unit` `e2e`
- AC3 Codes can be single-use or multi-use with a cap, and the team can create and revoke them. `db`
- AC4 Imported talent-call signups skip the code: their email is pre-approved. `db`

### ACC-02 Sign up and sign in with email (M1)
As a V, I want to sign up with my email and a one-time code so I don't need a password.
- AC1 I enter name, email and (optional) phone. I get a 6-digit code by email and land signed in once I enter it. `e2e`
- AC2 A wrong or expired code shows an error and lets me resend after 30 seconds. `e2e`
- AC3 Returning users sign in the same way and land where they left off. `e2e`
- AC4 Sessions survive closing and reopening the app. `e2e`

### ACC-03 Choose account type (M1)
As a new user, I want to say whether I'm a creative, a business, or both.
- AC1 I can pick Creative, Business, or both. At least one is required. `unit`
- AC2 Picking both creates both profiles on one account, and I can switch which one I'm acting as from my profile. `db` `e2e`
- AC3 I can add the other type later from settings. `e2e`

### ACC-04 Claim an imported profile (M1)
As a C or B who filled out the talent call or hire form, I want my answers already in my profile when I sign up.
- AC1 Signing up with the same email as a submission prefills my profile from it (name, creative types, Instagram, portfolio link, model fields, or business details). `db` `e2e`
- AC2 I see "We brought over what you told us on the talent call. Check it's right." and can edit everything. `e2e`
- AC3 The submission is marked `imported` and isn't imported twice. `db`

### ACC-05 Delete my account (M5)
As a user, I want to delete my account from settings (App Store rule 5.1.1(v)).
- AC1 Delete asks me to confirm, then removes my profile, portfolio, media and auth user. `db` `e2e`
- AC2 Projects I was on stay on the other person's record with my name replaced by "Former Huo member". `db`
