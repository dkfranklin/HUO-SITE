---
type: eval-plan
status: draft
created: 2026-10-10
owners: [Noggie, JP]
---

# Testing and evals

Two different questions, two different tools:

- **Tests** answer: *does the code do exactly what we wrote down?* They're deterministic. The same input always gives the same pass or fail. They run on every PR.
- **Evals** answer: *did we get what we actually asked for?* They grade an output against a rubric, usually with a model as the grader, because "does this screen match the story and sound like Huo" isn't a yes/no a unit test can check. They give a score, and we track it over time.

Because AI agents will write most of the code, we need both: tests stop regressions, evals catch an agent that made the tests pass but built the wrong thing.

## Tests

| Layer | Tool | What it covers | Runs |
| --- | --- | --- | --- |
| Unit | Jest + React Native Testing Library | Validation, formatting, state machines, components in isolation | Every PR |
| Database | Supabase CLI + pgTAP | Every RLS policy, every state-change function (for example, "a creative can't read another creative's project", "a gig goes filled when its last hire is selected") | Every PR, against a local Supabase |
| End-to-end, web | Playwright against the Expo web build | Story flows (sign up, post gig, apply, select, complete) | Every PR |
| End-to-end, mobile | Maestro flows on a simulator | The same flows on iOS and Android | Before each milestone demo and release |
| Manual | Checklist in the PR | Only what can't be automated (push arrives on a real phone, camera upload) | When touched |

**Rules for implementers:**
1. Every acceptance criterion in [README.md](../context/stories/README.md) gets at least one test, named with its ID, for example `test("PRJ-03 AC2: completes only when both confirm")`. A script checks every AC ID appears in a test, which gives us coverage by story instead of by line.
2. Write the failing test first, then the code.
3. RLS policies never ship without a pgTAP test that proves both the allowed and the denied case.
4. Seed data comes from JP's real placements (names anonymized), so tests look like Huo's real gigs.

## Evals

### 1. Build evals: did the agent build the story? (start in M1)

After an implementer agent finishes a plan, a grader model reviews the PR with:
- the story and its acceptance criteria,
- the plan,
- the diff and the test results,
- screenshots of the affected screens (from Playwright).

It scores against a fixed rubric and returns JSON:

| Criterion | Pass means |
| --- | --- |
| AC coverage | Every AC is implemented and has a test that exercises it, not a stub |
| Scope | No changes outside the files and behavior the plan named. No surprise features |
| Data rules | Schema changes are migrations, RLS is on, policies are tested |
| Design | Uses design tokens and core components; matches the screen reference |
| Voice | User-facing copy follows [glossary.md](../context/domain/glossary.md): says "gig", not "job" or "opportunity"; no hype |
| Docs | The milestone checklist and any changed doc are updated |

A PR merges only with green tests **and** an eval score at or above the bar (start at 5 of 6 with AC coverage required, then raise it). Results go in an `evals/results/` log, so we can see whether the agents and plans are getting better or worse across milestones. That trend is the learning piece: if Scope fails often, the plans are too vague; if Voice fails often, the glossary isn't in the agent's context.

### 2. Copy evals: does it sound like Huo? (start in M2)

A small set of cases: every user-facing string file, plus the push and email templates. The grader checks each string against the glossary and voice rules. It's cheap to run and catches "opportunities" creeping back in.

### 3. Spec evals: are the stories good enough to build from? (M0, now)

Before a milestone starts, a grader checks each story in it: is every AC testable, unambiguous and inside scope? Weak stories get fixed before an agent burns hours guessing.

### How to run them

Start with a plain script (`evals/run.ts`) that calls the Claude API with the rubric and the inputs and writes JSON results. Each eval is a folder with `cases/`, `rubric.md` and `expected.json` where there's a known answer. Once that works, a framework like promptfoo can take over the running and the reports. Each eval also gets a few **known-bad** cases (a PR that skips an AC, copy that says "job") to prove the grader actually catches failures. An eval that never fails proves nothing.

## Definition of done (per story)

1. Every AC has a passing test with its ID in the name.
2. CI is green: lint, types, unit, db, web e2e.
3. The build eval passes.
4. Screenshots are attached to the PR for any screen change.
5. The milestone checklist in 06 is ticked.
