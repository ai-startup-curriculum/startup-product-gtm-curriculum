# Exercise 05 — Magic Moment and Activation Programme Authoring

**Estimated time:** 3 hours
**Chapter link:** [`05-magic-moment-and-activation.md`](../05-magic-moment-and-activation.md)
**Prerequisite reading:** [Andrew Chen — "The Power User Curve"](https://andrewchen.com/power-user-curve/) (~15 min); [Andrew Chen — "New data shows losing 80% of mobile users is normal"](https://andrewchen.com/new-data-shows-why-losing-80-of-your-mobile-users-is-normal-and-that-the-best-apps-do-much-better/) (~15 min); [Lenny Rachitsky — "What is 'aha' and how do you find it"](https://www.lennysnewsletter.com/) (search "aha moment"; ~30 min); [Amplitude — North Star Playbook](https://amplitude.com/north-star) (skim, ~30 min); [Reforge — writing on activation and onboarding](https://www.reforge.com/blog) (search "activation"; ~20 min); [Wes Bush — *Product-Led Growth*](https://productled.com/book) (Chapter on onboarding, ~30 min)

## Problem statement

Chapter 5 said the magic moment is *found empirically, not guessed*, and named the three-part definition (action + count + window). This exercise walks you through the empirical method against a provided cohort dataset, then makes you author an activation programme around the winning triple.

You will:

1. Run the empirical magic-moment method on a provided cohort dataset — enumerate candidate triples, split the cohort, measure retention lift, and pick the winning triple with the cleanest causal story.
2. Author an activation programme around the winning triple — onboarding flow, empty-state design, triggered nudges, human-touch touchpoint — with the activation-rate cohort chart as the instrument.
3. Repeat both for a real (or realistic hypothetical) startup of your own, in the shape of scorecard section 6.

The exercise trains the discipline that turns a *"users don't stick around"* handwave into a specific triple, a designed programme, and a measurable activation rate.

## Requirements

Deliver a folder `exercise-05/` with:

- `part-a-empirical-diagnosis.md` — the empirical magic-moment analysis on the provided dataset.
- `part-b-activation-programme.md` — the activation programme designed around Part A's winning triple.
- `part-c-your-startup.md` — the magic-moment + activation programme for a chosen startup, in scorecard-section-6 shape.

### Part A — Run the empirical method on a provided dataset (60 min)

Below is a synthetic cohort dataset for **"Threadline"** — a synthetic B2B project-management tool. A team signs up; users within the team take various actions; the team is either still active at W12 or has churned.

**Team-level cohort:** 200 teams that signed up in 2025-Q4. W12 retention across all teams = **38%**.

For each team, four early-window actions are tracked:

| Action | Description |
|---|---|
| **A.** Invited-teammates-in-7d | Number of teammates invited (and accepted) within 7 days of signup |
| **B.** Created-tasks-in-7d | Number of tasks created within 7 days of signup |
| **C.** Integrated-Slack-in-7d | Whether the team connected the Slack integration within 7 days (yes/no) |
| **D.** Assigned-tasks-across-members-in-14d | Number of task assignments where the assigner and assignee are different users, within 14 days |

The retention split by candidate triple has been pre-computed (this represents a warehouse query you would ordinarily write). The candidate table:

| # | Candidate triple | Teams crossed | W12 retention (crossed) | Teams did not cross | W12 retention (did not cross) | Lift |
|---|---|---|---|---|---|---|
| 1 | A ≥ 2 invited in 7d | 84 | 61% | 116 | 21% | 2.9× |
| 2 | A ≥ 5 invited in 7d | 26 | 73% | 174 | 33% | 2.2× |
| 3 | B ≥ 10 tasks in 7d | 121 | 44% | 79 | 29% | 1.5× |
| 4 | B ≥ 30 tasks in 7d | 44 | 66% | 156 | 30% | 2.2× |
| 5 | C = yes (Slack in 7d) | 63 | 57% | 137 | 29% | 2.0× |
| 6 | D ≥ 5 cross-assignments in 14d | 71 | 68% | 129 | 22% | 3.1× |
| 7 | D ≥ 10 cross-assignments in 14d | 39 | 74% | 161 | 29% | 2.6× |
| 8 | A ≥ 2 AND D ≥ 5 in 14d | 58 | 72% | 142 | 24% | 3.0× |

Contextual notes:

- The team's stated hypothesis walking into the analysis was *"Slack integration is the aha moment — teams that connect Slack stick around."*
- Threadline's product is collaborative task management. The value scales with cross-assignment (multiple people doing coordinated work), not with solo task creation.
- Every user who invited a teammate did so via an explicit in-product "invite" action; the invited teammate had to accept and log in for the invitation to count.

Deliver `part-a-empirical-diagnosis.md` with:

1. **Candidate ranking.** Rank all 8 candidates by lift; note the top 3.
2. **Causal-story sanity check.** For each of the top 3, is the action a plausible *cause* of retention, or is it a *correlate* of engagement? Use Chapter 5's causal-story test.
3. **Winning triple.** Name the specific triple and one paragraph justifying why (largest sustained lift + cleanest causal story).
4. **Rejected favourite.** State whether the team's stated hypothesis (Slack integration) survives — and explain why or why not.
5. **Segmentation flag.** One sentence noting whether you would want to run the analysis segmented by ICP tier (SMB / mid-market / enterprise) before shipping the activation programme, and why.

### Part B — Author the activation programme around the winning triple (60 min)

Deliver `part-b-activation-programme.md` with the Chapter 5 four-block structure plus the activation-rate cohort chart plan:

1. **Onboarding flow.** A specific first-run flow that funnels the team to the winning action. Not a feature tour; a narrow path. Describe screen-by-screen (3–7 screens) and the "does not end until X happens" gate.
2. **Empty-state design.** For each product surface a new team hits before crossing the threshold, the specific empty-state affordance that invites the winning action.
3. **Triggered nudges.** The nudge fires (in-product modal / email / Slack) on close-to-threshold signals only. Cadence-throttled. Name the specific signals and the specific nudges.
4. **Human-touch activation.** For enterprise-tier teams (define "enterprise" — e.g., ≥ 25 seats or opted into an enterprise trial), the activation call within 3–7 days with a scripted outcome.
5. **Activation-rate cohort chart.** The instrument. State the exact numerator, denominator, cohort cadence, and the baseline (current activation rate) + target (activation rate after two quarters of iteration).
6. **Segmentation.** If Part A flagged that the moment likely differs by ICP tier, note the programme adaptation (or the additional analysis to run before shipping).
7. **Re-diagnosis cadence.** The scheduled two-quarterly re-run of the empirical method, with the specific trigger events (major feature ship, ICP shift, competitive change) that would trigger an ad-hoc re-run.

### Part C — Your startup's magic moment + activation programme (60 min)

Pick a startup — yours, one you know well, or a variant of the code-review-tool from Chapter 5 (choose a *different* winning triple than the chapter's, or invent a different candidate list, so you are not copying the worked example).

Deliver `part-c-your-startup.md` in the shape of scorecard section 6:

1. **Empirical method — abbreviated.** List the candidate actions you would enumerate. State which you would compute against which windows. Where real data is available, run the split and produce the table. Where data is not available, name the specific instrumentation you would add and the specific query you would run.
2. **Winning triple.** Named as (action, count, window). Retention lift with source.
3. **Activation programme.** The four building blocks (onboarding, empty state, nudges, human touch) scoped to your ACV band. Enterprise motions get more human touch; PLG SMB motions get more in-product automation.
4. **Activation-rate cohort chart.** Numerator, denominator, cohort cadence, baseline, target. Two-quarter target justified against a plausible programme-iteration rate.
5. **Segmentation.** ICP-tier segmentation as required.
6. **Re-diagnosis cadence.** With trigger events.
7. **Distinction from north-star.** One sentence naming the company-level north-star metric and one sentence explaining how the magic moment is the *user-level* version — Chapter 5's non-conflation rule.

Length: 1–2 pages. Do not exceed 2. Mark hypothetical numbers and justify against Chapter 5's guidance that a magic moment produces at least ~2× retention lift.

### Part D — Reflection (15 min)

A short closing paragraph:

- Which of the Part A candidates were "correlate not cause" and would have led to a wrong-headed activation programme if picked?
- For your Part C startup, what is the single instrumentation gap most likely to prevent you from computing the winning triple, and what would it take to close?
- If your Part C activation programme's activation rate is flat six months after ship, what does that tell you — and which of Chapter 5's four building blocks would you re-open first?

## Starter guidance

- The Chapter 5 causal-story test is the load-bearing filter. "Team changed the workspace name" might correlate with retention (only engaged teams do it), but changing the name does not *create* value; it is a proxy for engagement, not a magic moment.
- In Part A, the largest-lift candidate is candidate 6 (D ≥ 5 cross-assignments in 14d, 3.1×). The team's stated hypothesis (Slack integration, 2.0×) is real but weaker and is arguably a *correlate* — teams that integrate Slack are already committed enough to configure it, which may make it a signal of engagement rather than a causal driver.
- Cross-assignment (D) is the collaborative behaviour Threadline was built for. That is the Chapter 5 causal story: users who did the thing the product exists to enable retain more.
- Candidate 8 (composite A + D) has a lift of 3.0× but adds design complexity; a single-action triple is easier to onboard and easier to instrument. Prefer the simpler triple unless the composite meaningfully outperforms.
- For Part B, the onboarding flow must produce the winning action, not describe it. If a user can complete onboarding without cross-assigning a task, the onboarding does not enforce the magic moment.
- The activation-rate cohort chart is not the same as the retention curve. Retention is the lagging indicator; activation rate is the leading one. Chapter 5's separate-instruments rule.
- For Part C, if you cannot state the winning triple as (action, count, window), you have not finished the empirical method — pick a starting hypothesis and name the analysis you would run.
- Do not confuse activation with the north-star metric. The north-star is "messages sent per active user" at company level; the magic moment is "team sends ≥ 5 messages within 3 days" at cohort level. Both matter; do not conflate.

## Acceptance criteria

Your submission is complete when:

- [ ] Part A ranks all 8 candidates by lift and names the top 3.
- [ ] Part A applies the causal-story test to each of the top 3 and distinguishes correlate from cause.
- [ ] Part A picks candidate 6 (or a defensible alternative — most likely candidate 6 or the composite 8) as the winning triple, with a paragraph justifying the choice.
- [ ] Part A explicitly addresses the team's stated Slack hypothesis and explains why it is (or is not) the winning triple.
- [ ] Part A flags whether an ICP-segmented re-analysis is warranted.
- [ ] Part B specifies an onboarding flow that gates completion on the winning action, not on a feature tour.
- [ ] Part B specifies empty-state designs for the specific surfaces a new team hits.
- [ ] Part B's triggered nudges fire on close-to-threshold signals, not on schedule for everyone.
- [ ] Part B specifies an activation-rate cohort chart with numerator / denominator / cadence / baseline / target.
- [ ] Part C runs the empirical method (real data or named instrumentation gap) and produces a specific winning triple with retention lift.
- [ ] Part C's programme is scoped to the ACV band (more in-product automation for PLG; more human touch for enterprise).
- [ ] Part C distinguishes the magic moment from the company-level north-star metric.
- [ ] Part D reflection names the correlate-not-cause traps, an instrumentation gap, and a building-block to re-open on programme underperformance.

## Common ways this exercise goes wrong

- **Picking the highest-lift candidate without the causal-story check.** Chapter 5's core discipline. Lift alone can be a proxy for engagement.
- **Confirming the team's stated hypothesis without running the empirical method.** Chapter 5's opening rule: do not guess the moment.
- **Feature-tour onboarding that doesn't produce the winning action.** A tour is not activation.
- **Empty state that says "No data" with no next action.** Retention dies here (Chapter 5).
- **Nudges fired on day 1 for everyone, cadence-untargeted.** Signal-untargeted nudges are noise.
- **Human-touch call scheduled as "how can we help".** That is a discovery call, not an activation call. Script the outcome.
- **Conflating activation rate with retention rate.** Two distinct instruments per Chapter 5.
- **Not segmenting by ICP tier when the segments plausibly have different moments.** SMB and enterprise often need different activation programmes.
- **No re-diagnosis cadence.** The magic moment drifts as the product and ICP change. Chapter 5's shelf-life rule.
- **Conflating the magic moment with the north-star metric.** User-level vs. company-level. Chapter 5's non-conflation rule.
- **In Part C, no plausibility check against the ≥ 2× retention-lift practitioner benchmark.** A "magic moment" that lifts retention by 5% is not a magic moment; it is a small effect.
