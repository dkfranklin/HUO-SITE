---
type: story
status: draft
created: 2026-10-10
owners: [Noggie, JP]
area: PLT
---

## PLT · Platform (no user-facing story, but required)

- **PLT-01** Expo app builds for iOS, Android and web from one codebase, with EAS builds to TestFlight and Play internal testing. (M1)
- **PLT-02** Supabase migrations are the only source of the schema. Every table has row-level security on and a test. (M1)
- **PLT-03** Sentry error tracking and PostHog analytics, with the events listed in [README.md](../../evals/README.md). (M1)
- **PLT-04** CI runs lint, type-check, unit, db and web e2e tests on every PR. (M1)
- **PLT-05** Design tokens and core components from Rob's files, which every screen uses. (M2)
