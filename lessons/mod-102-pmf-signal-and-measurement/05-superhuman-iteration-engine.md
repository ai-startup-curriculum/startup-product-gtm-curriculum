# The Superhuman Iteration Engine

## Motivation

Chapters 3 and 4 gave you two instruments — a survey score and a retention curve. On their own, they answer *"do we have PMF?"* On their own, they do not answer *"if we don't, what do we do about it?"*

Rahul Vohra of Superhuman published the operating loop that turns those instruments into a **PMF engine** — a repeatable iteration cycle that moves the survey score from below the 40% threshold toward and past it. The move is small — four steps, run on a cadence — and its power comes from *targeting the right cohort with the right work*. This chapter reproduces the engine, names the four steps, and shows why it is a PMF engine, not a one-shot measurement.

The source is Rahul Vohra's own First Round Review essay, "How Superhuman Built an Engine to Find Product/Market Fit" ([First Round Review, 2018](https://review.firstround.com/how-superhuman-built-an-engine-to-find-product-market-fit/)). Read it end-to-end; this chapter is the operating condensation, not a replacement.

## Core concepts

### The Superhuman starting position — 22% and the choice not to pivot

In late 2017, Superhuman was well-funded, well-known, and well-liked, but by their own reading pre-PMF. Vohra reports they ran the Sean Ellis survey and got **22% "very disappointed"** — clearly below the 40% threshold. Three doors were open at that moment:

1. **Declare victory anyway** — plenty of loud fans, media coverage, a waitlist. Some teams call this PMF and start scaling.
2. **Pivot** — the score is under 40%; the product must be wrong; rewrite from scratch.
3. **Iterate** — treat the score as a *diagnostic* rather than a verdict, and build a system that raises it.

Vohra chose 3, and the essay documents the engine they built to run door 3 systematically. Twelve months later they were at **58% "very disappointed"** — from pre-PMF to strong PMF in a single segment, without a pivot.

The insight worth naming up front: **the survey score is a state variable, not a grade.** Below 40% is not a fail; it is a starting position. The question is *what specific move raises it?* That is what the engine answers.

### Step 1 — cohort the "very disappointed" users

Take the very-disappointed responses from the Sean Ellis survey. Do not average across all respondents. **Cohort exactly the users who answered "very disappointed"** and read that cohort separately from the rest.

Two questions this cohort answers:

- **Who are they?** Read their free-text on "who would benefit most" and cross-reference against user metadata (role, company size, industry). The cluster you find *is* your PMF ICP — the segment for which the value hypothesis is currently proven. Superhuman found their very-disappointed cohort was heavily concentrated in specific roles (founders, executives, business developers, salespeople) and specific behaviours (heavy email volume, high-context users).
- **Why are they there?** Read their free-text on "main benefit". This produces the modal main-benefit statement — the compressed value experience the cohort actually receives in their own words.

The output of Step 1 is not a percentage. It is **a segment definition (who) plus a benefit statement (what).** Both feed forward.

### Step 2 — identify the main benefit and harden it

Take the modal main-benefit statement from Step 1 and ask: **what fraction of our roadmap is currently making that benefit stronger?**

For Superhuman, the very-disappointed cohort's modal main benefit was **speed** — users described the product as enabling them to "keep inbox zero", "get through email faster", "spend less time in email" — dozens of variants of the same underlying value. The team then audited the roadmap: which items make the product perceptibly *faster*? Which items are neutral? Which items risk slowing it down?

They hardened around the cohort's main benefit — invested the roadmap in things that made speed more true, more visible, and more differentiated versus the alternatives set (competitive alternatives from Dunford / mod-103 language). Anything that pulled roadmap capacity away from the main benefit — even useful features — got deprioritised or cut.

The move here is counterintuitive. The natural founder instinct is to work on what the *dissatisfied* users complain about. The Superhuman move is to first **make the thing your fans love, love-able-r**. If speed is the main benefit, do not spend the quarter building a shared inbox because "somewhat-disappointed" users asked for one. That work happens in Step 3.

### Step 3 — cohort the "somewhat disappointed" and address the top blockers

Now switch cohorts. Read the "somewhat-disappointed" responses separately.

Two questions this cohort answers:

- **What is stopping them from being very-disappointed?** Read their "how to improve" free-text carefully. These are the users who *see the value* — that is why they are not "not disappointed" — but who *cannot fully commit* because of specific missing pieces. Their blocker list is the highest-leverage roadmap.
- **Are they in-ICP or out-of-ICP?** Cross-reference against the segment definition from Step 1. Somewhat-disappointed users who look like the very-disappointed segment on other dimensions are the ones whose blockers matter most — they are one blocker removed from crossing the line.

The move: sort the somewhat-disappointed's blockers by (a) how many users cite each blocker and (b) whether those users match the very-disappointed ICP. Ship the top blockers first. Superhuman built shared inboxes, mobile, and Windows/Linux support in this cadence — items that were repeatedly named as blockers by users who otherwise matched the very-disappointed segment.

Critically: **do not build for blockers cited only by "not-disappointed" users.** Those users are not close to the boundary; unblocking them will not move the score, and the work costs roadmap capacity that could have made a boundary-crossing user cross.

### Step 4 — re-run the survey

After the roadmap moves from Steps 2 and 3 ship, **re-run the same survey with the same wording against the same active-user filter.** Compare segment-to-segment against the previous run.

You are looking for two moves:

- **The very-disappointed segment grows.** Somewhat-disappointed users have crossed into very-disappointed as their blockers cleared.
- **The main-benefit statements sharpen.** More users describe the modal benefit in tighter language; the free-text convergence is a leading indicator of positioning strength.

If the score moves, the engine is working — cohort the new very-disappointed set, re-harden the main benefit, address the new top blockers, re-run. If the score does not move, the diagnostic is: either the wrong blockers were fixed (Step 3 misread which somewhat-disappointed users were in-ICP), or the main benefit was correctly identified but weakly hardened (Step 2 shipped speed features that were not perceptible to users), or the segment definition itself is off (Step 1 clustered on the wrong dimension). Iterate one of the three and re-run.

### Why this is an engine, not a measurement

The naming is the payoff. Most teams treat Sean Ellis as a snapshot: "we're at 22% — bad" or "we're at 45% — good." Vohra's move is to treat the survey as the **evaluation function of a search algorithm**:

- Every run produces a score (the objective function value) and a diagnostic (the free-text) that tells you which direction to move.
- Every roadmap cycle is one step of the search.
- The engine converges when the score stabilises above threshold — at which point PMF is established and the engine's job becomes durability (mod-109) rather than discovery.

The engine is powerful because it **removes the founder from the loop**. Roadmap decisions get grounded in the very-disappointed cohort's main benefit and the somewhat-disappointed cohort's blockers, not in the loudest customer's requests or the founder's taste. Every decision has a defended cohort behind it.

### Cadence — quarterly is the working default

Vohra's cadence for the engine at Superhuman was roughly **quarterly** — one full loop (survey → very-disappointed read → main-benefit hardening + somewhat-disappointed unblocking → re-survey) per quarter. That is a working default for a PRE-SEED / SEED team with a shipping cadence of days-to-weeks and a stable-enough surface area for the survey to be re-run against comparable users.

Do not run it monthly — the roadmap has not moved enough for the score to change. Do not run it annually — the surface area drifts too much for the diagnostic to be actionable. Quarterly is where you get one meaningful comparison per iteration.

### What the engine assumes — and where it breaks

Two assumptions the engine rests on:

- **You have enough active users to survey.** The engine requires ≥30 responses in the very-disappointed bucket to read cleanly. At 20% survey response rate, that means ≥150 active users. If you have 15 active users, run mod-101 discovery further before trying to run this engine.
- **The main benefit is *coherent enough to name*.** If very-disappointed users write ten completely different main-benefit statements, you do not yet have a segment — you have ten segments with n=1 each. Sharpen the ICP first.

Where the engine breaks: **wrong-market cases** (Chapter 6). If your product has no viable segment at all, the engine will run one cycle and the score will not move. That is a Chapter 6 diagnostic to re-run, not an engine to keep spinning. Vohra's engine is for the case where a real segment exists and needs to be found — not for the case where no segment exists yet.

## Concrete example — the code-review-tool runs the engine

Return to the code-review-tool at 25% aggregate very-disappointed (Chapter 3), with mid-market at 56%, small-teams at 13%, enterprise at 9%.

**Step 1 — cohort the very-disappointed.** 22 users answered very-disappointed. 20 of 22 are in the mid-market segment. Segment definition: engineering managers at 50–200-eng distributed teams with reviewers across ≥3 time zones. Modal main-benefit statement (from 15/22 free-texts): *"knowing exactly who to nudge without becoming the nag."* Secondary main benefit (7/22): *"seeing which reviews are stalled at a glance."*

**Step 2 — harden the main benefit.** Audit the next-quarter roadmap. Of 14 planned features, 3 make the "who to nudge" experience faster/clearer (auto-reassign with confidence signal, one-click escalate, per-time-zone reviewer preference); 4 are neutral (billing improvements, admin panel); 2 make it *worse* (a new "digest" that would compete with the direct escalation UX). Reprioritise: cut the digest, promote the three main-benefit features, ship them first. All roadmap capacity aligns with the very-disappointed cohort's benefit.

**Step 3 — cohort the somewhat-disappointed.** 30 users answered somewhat-disappointed. Cross-check ICP: 18 are mid-market (in-ICP), 8 are small-team (out-of-ICP for now), 4 are enterprise (out-of-ICP for now). Look only at the 18 in-ICP somewhat-disappointeds. Top three blockers in their "how to improve": (a) GitHub Enterprise support, (b) per-team ownership rules, (c) less-noisy default digest. Add these three to the roadmap immediately after the main-benefit hardening ships.

**Step 4 — re-run the survey next quarter.** Same wording, same active filter, same segments. If mid-market very-disappointed moves from 56% → 65%, the engine is working: main-benefit hardening + top-blocker unblocking crossed 3 more mid-market users into very-disappointed. Read the new free-text; the modal benefit will have sharpened; the new somewhat-disappointed cohort's blockers are the next cycle's roadmap.

Do not touch the small-teams or enterprise segments this cycle — Chapter 6 will route them separately (small-teams likely wrong-market, enterprise likely wrong-product-shape for that segment). The engine is running against the segment where PMF is closest to landing.

## Common failure patterns

- **Building for "not disappointed" complaints.** Those users are furthest from crossing the line. Their blockers cost roadmap capacity that could have moved a boundary-crossing user.
- **Averaging main-benefit statements across all respondents.** The very-disappointed cohort's benefit is *different* from the somewhat-disappointed cohort's benefit. Cohort first, read separately.
- **Skipping Step 2 (main-benefit hardening) and going straight to Step 3 (unblocking).** Founders find the blocker list more actionable. But unblocking without hardening makes a broader product that no one loves; the score does not move. Do Step 2 first.
- **Running the engine without segmenting.** The main-benefit statement is often segment-specific. A single "mainly speed" cluster can hide "speed for founders" vs. "speed for salespeople" — the latter cares about different features (multi-account, templates) than the former (keyboard shortcuts, snoozes). Segment.
- **Treating one bad cycle as a pivot signal.** Sometimes a cycle does not move the score because you fixed the wrong blockers. Diagnose Step 1 or Step 3, adjust, and re-run — do not pivot the whole product on one flat cycle.
- **Ignoring the engine after PMF is achieved.** Chapter 1's system-state framing: PMF drifts. Cutting the engine after crossing 40% is how you find yourself back at 35% eighteen months later.

## Summary

- Superhuman's engine turns the Sean Ellis survey from a snapshot into a **four-step iteration loop**: cohort the very-disappointed → harden their main benefit → unblock in-ICP somewhat-disappointed → re-survey.
- Below 40% is a **starting position**, not a verdict; the engine is what raises the score.
- **Segment first.** The very-disappointed cohort's segment definition and main-benefit statement are the ICP and positioning inputs; every roadmap decision downstream is grounded in them.
- **Unblock somewhat-disappointed users who match the very-disappointed ICP** — those are the users closest to crossing the boundary. Do not build for out-of-ICP complaints.
- Run the engine on a **quarterly cadence**; monthly is too fast (roadmap has not moved), annual is too slow (surface area drifts).
- The engine assumes a real segment exists to be found. If wrong-market (Chapter 6), the engine will spin without moving; that is a different diagnosis, not a different iteration.
