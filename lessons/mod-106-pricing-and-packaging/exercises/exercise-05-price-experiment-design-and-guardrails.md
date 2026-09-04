# Exercise 05 — Price Experiment Design + Guardrails

**Estimated time:** 3 hours
**Chapter link:** [`05-price-experiments-and-grandfathering.md`](../05-price-experiments-and-grandfathering.md)
**Prerequisite:** Chapter 5 read end-to-end; Exercises 02 and 03 (value derivation + tier composition — the artifacts the experiment tests); a working ability to tag customers in a CRM by signup cohort and pricing regime (or a spreadsheet stand-in); mod-105's pipeline meeting or a founder-run equivalent.

## Problem statement

Chapter 5 named the failure modes: the-price-change-that-was-actually-five-changes; snapshot-ARR reads that mask cohort effects; un-committed guardrails debated mid-experiment; leaky segment pricing; bait-and-switch experimental prices; running experiments without ICP filtering; continuous experimentation without a pack revision; not documenting the experiment. The remedy is a **single next-quarter price experiment** authored to the design-doc shape — one variable changed, pre-committed guardrails, cohort-level tracking, communication policy — plus a **counter-experiment design** that runs in parallel or sequence to verify the read.

This exercise trains you to **author the pricing-pack's Section 6 (next-quarter experiment)** in the shape Chapter 6 requires — with a real experiment picked from Chapter 5's four types, pre-committed guardrails, cohort tracking, communication policy, timeline, owner, and a documented read-plan. The output is the specific document the founder points at when the sales team asks "what are we changing next quarter?" and when the finance team asks "what should we watch?"

The failure mode this exercise exists to catch: **the founder announces "we're going to test pricing" at the weekly pipeline meeting, changes 3 things at once with no baseline recorded, reads snapshot ARR at Day 30, and either concludes the change was a wash (missing the cohort effect) or concludes it was a huge win (attributing seasonal / other-cause movement to the price change). The experiment produces no learning either way.**

## Requirements

Deliver a folder `exercise-05/` with:

- `part-a-experiment-design-doc.md` — the full experiment design in Chapter 5's shape.
- `part-b-cohort-tracking-and-guardrails.md` — the specific cohort-tracking instrumentation and the pre-committed guardrail thresholds.
- `part-c-communication-and-read-plan.md` — the customer communication policy + the read-plan + the pre-mortem.

### Part A — The experiment design doc (75 min)

Deliver `part-a-experiment-design-doc.md`.

**A1 — Pick the experiment type (10 min).** From Chapter 5's four types, pick **one**:

1. **First-conversation pricing test** — vary the anchor quoted in the mod-105 discovery call for a calibrated period; measure the ordinal-scale reaction distribution.
2. **Plan-tier switch** — change one thing (price, feature assignment, or usage bracket) in one tier for a new-signup cohort; measure the tier-mix shift.
3. **Segment / geographical variant** — introduce different pricing for enforceable segments (region, verified vertical, self-declared company size); measure segment-specific close rate + ARPU.
4. **Grandfathering / migration** — apply a specific grandfathering policy for a pricing transition (this is authored in Exercise 06; if you're running a migration experiment, Exercise 06 is the specific one; here pick a different type).

Write one paragraph naming the type, why this type (vs. the other three) is the right choice for what you need to learn this quarter, and which pack section the experiment is testing (from Exercises 02 / 03 / 04).

**A2 — Name the one variable (10 min).** Chapter 5's cardinal rule: **one variable at a time**. Name:

- **The specific thing changing.** E.g., "middle-tier price rises from $10/repo to $12/repo," or "SSO moves from premium-only to middle+premium," or "Team-tier bracket expands from 50 to 75 repos."
- **What is NOT changing.** Explicit list of things that stay constant across the experiment: metric, other tier prices, feature composition of other tiers, sales scripts, pricing-page layout except for the tested change.
- **The rationale** — one paragraph linking the variable back to the specific hypothesis (e.g., "the middle tier's price is below the WTP OPP; a 20% raise brings it to the modal acceptable point without exceeding PME").

**A3 — Baseline metrics (20 min).** Before the experiment runs, capture the current state. Cover:

- **Close rate** on the affected deal type — new-tier close rate, or overall close rate if the change affects all deals.
- **ACV / ARPU** distribution — mean, median, per-tier if applicable.
- **Sales cycle length** — mean, median.
- **30 / 60 / 90-day retention** for the last 2-3 cohorts.
- **Tier mix** — fraction landing in each tier over the last 90 days.
- **Support ticket volume** tagged "pricing" or "billing" — baseline rate.
- **Pricing-related close-lost tags** in the CRM — baseline rate.

Every baseline number needs its source (CRM query / spreadsheet cell / dashboard URL) so a reader in 6 months can reproduce the read.

**A4 — Hypothesis statement (10 min).** Write the specific hypothesis in the shape: "if we change [variable] by [amount], we expect [metric] to move by [direction] because [causal reasoning]." Include:

- **Directional prediction** — up / down / no change.
- **Magnitude prediction** — a band, not a point (e.g., "close rate drops 5-15%").
- **Time horizon** — when you expect the effect to be measurable.
- **The confidence level** — how sure you are. Chapter 5's operational discipline: directional signal not p-values, but explicit confidence framing ("we think this is more likely than not" vs. "we're 90% sure") is worth naming.

**A5 — Cohort assignment rule (15 min).** Chapter 5's cohort discipline: every customer tagged with signup cohort and pricing regime. Author:

- **The cohort tag scheme** — e.g., "cohort-Q3-2026, regime-v3.2-team-tier-12" for a customer signing in Q3 under v3.2 pricing.
- **How new customers are assigned** — publish the change on Day 1 of the experiment window; every signup within the window is in the treatment cohort.
- **How existing customers are treated** — grandfathering (Exercise 06 will formalise this; for this exercise, state the policy: full-grandfather for the duration, sunset-window, or immediate migration).
- **How the CRM / spreadsheet stores the tags** — the specific field or column, the specific values.
- **What breaks if the tag is missing** — if the sales rep forgets to tag, is the customer in treatment or control? Default should be flagged for review, not silently one or the other.

**A6 — Timeline + owner (10 min).**

- **Start date** — Day 1 of the experiment.
- **End date** — when the experiment window closes to new treatment customers.
- **Read date** — when you'll look at the results (Chapter 5: at least 2× the average sales cycle post-launch for plan-tier experiments; 1-2 weeks for first-conversation experiments).
- **Decision date** — when the pack revision (Chapter 6 quarterly) canonises or reverts the change.
- **Named owner** — one person responsible for the experiment. Not a team; one name.

### Part B — Cohort tracking + guardrails (45 min)

Deliver `part-b-cohort-tracking-and-guardrails.md`.

**B1 — Cohort tracking instrumentation (20 min).** Chapter 5's core discipline: read per-cohort, not snapshot ARR. Author the specific instrumentation:

- **The cohort table** — one row per (signup-cohort × pricing-regime) combination, columns for per-cohort ARPU, close rate, 30/60/90-day retention, count of customers, source. Include at minimum the last 2 cohorts pre-experiment as controls plus the treatment cohort.
- **The measurement cadence** — when is each column refreshed (weekly / monthly / at cohort maturity)?
- **The comparison discipline** — pre-experiment cohorts vs. treatment cohort *at the same maturity* (day 60 of treatment cohort compared to day 60 of the last control cohort, not day 60 vs. day 90). This is the classic error that makes ARPU / retention look better or worse than it is.
- **The grandfathered-cohort separation** — customers on old pricing tagged as one cohort; customers migrated to new tagged as another; new customers under new pricing as a third. Read the three separately.
- **The tool** — even a spreadsheet is fine at seed; the discipline is what matters. Name where the table lives (Google Sheet URL, Notion table, CRM report, or seed-stage `cohort-tracking.md` in the pack repo).

**B2 — Pre-committed guardrail thresholds (15 min).** Chapter 5's discipline: guardrails committed before the experiment starts. Author:

- **Close-rate floor.** "If the treatment cohort's close rate drops below [X% — typically 70-80% of baseline], revert." Name the specific X%.
- **Retention floor.** "If treatment cohort's 30-day retention drops below [Y%], investigate; below [Z%], revert."
- **Voluntary-churn spike.** "If voluntary churn in any cohort exceeds baseline by [N × ], escalate immediately."
- **Support-ticket spike.** "If pricing-related support tickets exceed baseline by [M% ] in any week, pause the experiment for review."
- **Sales-rep signal.** "If ≥ [K] AEs (or founder in founder-led-sales) raise concerns about the pricing at the weekly pipeline meeting, discuss and consider pause."
- **ICP filter.** "Every experimental deal must pass the mod-104 ICP scorecard before being included in the treatment read."

Every threshold is a specific number, not a phrase. "If close rate drops significantly" is not a guardrail; "if close rate drops below 32% (from a baseline of 42%)" is.

**B3 — Guardrail-trip response protocol (10 min).** What happens when a guardrail trips?

- **Immediate response** — pause the experiment (revert to old pricing on the pricing page and in the sales script; existing treatment customers stay on their quoted price — no bait-and-switch).
- **Investigation window** — 3-5 days to diagnose whether the trip is causal (price change), correlational (something else moved at the same time), or a data artifact.
- **Decision protocol** — who decides continue / revert / iterate? Named person from A6.
- **Communication** — how the pause / revert is communicated to sales, finance, and any impacted customers.

### Part C — Communication policy + read-plan + pre-mortem (60 min)

Deliver `part-c-communication-and-read-plan.md`.

**C1 — Customer communication policy (20 min).** Chapter 5's discipline: silent price changes are trust events. Author:

- **New-customer communication** — what does the pricing page say? What does the sales rep quote?
- **Existing-customer communication** — the specific email that goes out to existing customers if the change affects them. Content: what's changing, when, what it means for their bill at next renewal, what they can do (lock in current pricing for one term, migrate now, contact us). Include the actual draft email text.
- **Public communication** — is the change public (pricing page updated) or private (only communicated to existing / new customers)? If public, when does a blog post / community update ship?
- **Sales-team briefing** — the specific talking points AEs use in the discovery call when a buyer asks about the change ("we introduced the volume tier because customers with 100+ repos told us the flat rate felt heavy at scale" is defensible; "we're testing" is not).

Every existing customer gets an email or the equivalent; every new customer sees the updated pricing page; no one discovers the change from a discrepant invoice.

**C2 — The read-plan (20 min).** When and how you'll read the results, in explicit steps:

- **Read date 1 — early check (Day 14-30).** Guardrail-only. Any tripped guardrail forces investigation; if no guardrails tripped, do NOT make a keep/revert decision — the sample is too small.
- **Read date 2 — mid-read (Day 45-60).** Cohort-level ARPU, close rate, and retention compared to the pre-experiment cohorts at matched maturity. First directional signal.
- **Read date 3 — final read (Day 75-90, or end of quarter).** Full cohort read. Decision-ready at this point.
- **Decision at pack revision (end of quarter).** Keep / iterate / revert. The decision is written into the pack's change log with the specific baseline and treatment numbers.

For each read date, list the specific metrics you'll look at, the source (from B1's cohort table), and the read-out format (a paragraph in the weekly / monthly / quarterly meeting notes).

**C3 — Pre-mortem (20 min).** Chapter 5's implicit discipline: imagine the experiment has failed 90 days from now, and write the post-mortem *before* you launch. Cover:

- **Top 3 ways the experiment could go wrong** — the specific failure scenarios (e.g., "close rate craters because the higher price crosses PME for the mid-market segment," "cohort tag applied wrong to 40% of customers," "seasonal Q4 procurement freeze contaminates the read").
- **The signal for each failure** — what you'll observe if this scenario happens.
- **The mitigation planned before launch** — what you're doing now to reduce the probability or the impact.
- **The unmitigable risks** — the ones you can't reduce; state them explicitly so the decision to launch is informed.

The pre-mortem is 20 minutes well spent because it exposes the "we hadn't thought of that" failures while they're still cheap to fix.

## Starter guidance

- **One variable.** Chapter 5's cardinal rule. If you catch yourself designing an experiment with two knobs (change middle-tier price and add SSO to middle), split it into two sequential experiments. The compound experiment is un-decodable regardless of the read.
- **Baseline before launch, always.** A5's baseline metrics are what everything is compared against. If you launch without a baseline, you have already lost the read. Capture the baseline before Day 1, even if it means delaying launch by a week.
- **Cohort tracking is not "we track ARR."** Chapter 5's core discipline: separate per-cohort tables with matched-maturity comparisons. Snapshot ARR is the failure mode. If your instrumentation cannot produce a per-cohort table, either build the instrumentation before launching or delay the experiment.
- **Guardrails are pre-committed with specific numbers.** "If things go badly" is not a guardrail; "if close rate drops below 32%" is. Chapter 5: guardrails discovered mid-experiment are rationalisations. Write them down before Day 1.
- **The founder is the one AE at seed.** In mod-105 founder-led sales, the "sales-rep signal" guardrail is the founder's own gut. If she catches herself compressing the experimental quote or apologising in the discovery call, that's the guardrail firing.
- **The communication draft is required, not optional.** C1's existing-customer email is what turns a price change from a trust event into a trust-preserving event. Write it before launch; ship it on Day 1. Later is a trust event.
- **The read-plan has three checkpoints, not one.** Chapter 5's discipline: early check is guardrail-only; mid-read is directional; final read is decision-ready. Reading at Day 30 and deciding is the classic snapshot-ARR failure — you're seeing too little of the cohort's trajectory.
- **The pre-mortem is where the experiment gets pressure-tested.** Imagining specific failures ("cohort tagging is wrong for 40% of customers") exposes fragility while it's cheap. Skipping the pre-mortem is why "we didn't think of that" post-mortems exist.
- **This exercise pairs with Exercise 06.** Exercise 05 designs a price experiment for new customers; Exercise 06 designs the grandfathering / migration policy for existing customers when the experiment (or a full pricing revision) affects them. They are complementary — a pack revision usually needs both.
- **Do not run two experiments simultaneously.** Chapter 5's cadence: one per quarter. If you have two hypotheses, sequence them. Two overlapping experiments contaminate each other and consume the founder's attention budget.
- **Documentation is the compounding output.** The design doc + baseline + read + decision, appended to the pack's change log, is what turns 4-6 quarterly experiments into a market-tested pricing strategy vs. a series of forgotten guesses. Compress ruthlessly — the whole design doc is 3-5 pages, not 20.

## Acceptance criteria

Your submission is complete when:

- [ ] Part A picks one Chapter 5 experiment type with a written rationale for why this type is the right choice this quarter.
- [ ] Part A names one specific variable that changes, with an explicit list of what does NOT change.
- [ ] Part A captures baseline metrics (close rate, ACV, sales cycle, retention, tier mix, support ticket volume, close-lost tags) with source references for each.
- [ ] Part A includes a hypothesis statement with direction, magnitude band, time horizon, and confidence level.
- [ ] Part A specifies the cohort tag scheme, assignment rule for new customers, treatment for existing customers, and CRM / spreadsheet storage.
- [ ] Part A names start / end / read / decision dates and one named owner.
- [ ] Part B1 designs the cohort tracking table with per-cohort ARPU, close rate, retention (30/60/90) and specifies matched-maturity comparison discipline.
- [ ] Part B1 separates grandfathered / migrated / new-under-new-pricing cohorts explicitly.
- [ ] Part B2 states 5+ pre-committed guardrails with specific numeric thresholds (close-rate floor, retention floor, churn spike, support-ticket spike, sales-rep signal, ICP filter).
- [ ] Part B3 defines the guardrail-trip response protocol (pause, investigate, decide, communicate) with a named decision-maker.
- [ ] Part C1 drafts the customer communication (new-customer, existing-customer, public, sales-team briefing) including the actual existing-customer email text.
- [ ] Part C2 defines 3 read-dates (early / mid / final) with the metrics, sources, and read-out format for each.
- [ ] Part C3 lists the top 3 failure scenarios with signals and mitigations, plus any unmitigable risks.
- [ ] The design doc is 3-5 pages total (compressed), not a 20-page research report.

## Common ways this exercise goes wrong

- **The five-changes-at-once trap.** Founder changes middle-tier price, adds SSO to middle, moves entry-tier price, and switches metric — all in one launch. Result: no read attributable to any one change. Fix: A2's "one variable" rule; split compound experiments into sequential single-variable experiments.
- **The no-baseline trap.** Founder launches without capturing pre-experiment metrics. Fix: A3's baseline capture is required before Day 1; every baseline number has a source.
- **The snapshot-ARR read trap.** Founder looks at ARR at Day 30, sees flat, concludes wash. Fix: B1's per-cohort tracking with matched-maturity comparison, not aggregate ARR.
- **The un-committed guardrail trap.** "We'll see how it goes and course-correct" is not a guardrail. Fix: B2's specific numeric thresholds committed before launch.
- **The silent-price-change trap.** Existing customers discover the change on the next invoice. Trust event. Fix: C1's existing-customer email drafted and sent on Day 1.
- **The bait-and-switch trap.** Founder quotes experimental price, buyer accepts, founder tries to charge different price. Fix: any price quoted in an experiment is honoured; treatment customers get the price they were quoted at signup.
- **The off-ICP-experiment trap.** Treatment cohort includes off-ICP buyers whose reactions are noise. Fix: B2's ICP filter — every experimental deal passes the mod-104 scorecard before being included in the read.
- **The read-at-Day-30-decide-at-Day-30 trap.** Reading too early; sample too small; conclusion premature. Fix: C2's three-checkpoint read-plan; only the final read is decision-ready.
- **The no-pre-mortem trap.** Founder launches, discovers a failure mode ("we didn't think about seasonal effects"), scrambles. Fix: C3's pre-mortem exposes fragility before Day 1.
- **The undocumented-experiment trap.** Founder runs experiment, moves on. Six months later no one remembers what happened. Fix: the design doc + baseline + read + decision get appended to the pack's change log at quarterly review.
- **The two-experiments-in-parallel trap.** Founder can't decide, runs both. Cohorts contaminate. Fix: one per quarter (Chapter 5 cadence); sequence competing hypotheses.
- **The ambiguous-owner trap.** "The team owns it" — nobody owns it, nothing gets read. Fix: A6's named owner is one person, accountable for the read.
- **The guardrail-tripped-but-we-kept-going trap.** Close rate drops below the floor; founder rationalises ("but the deals were low-quality"); experiment continues. Fix: B3's response protocol enforces the pause even when the founder wants to continue.
- **The customer-communication-is-a-tweet trap.** Founder announces the change in a Slack message to sales; no email to customers; customers discover it. Fix: C1's communication policy covers every audience; existing customers get email, not tweet.
- **The read-that-cherry-picks-cohorts trap.** Founder reads the cohort where the change looked good and ignores the one where it didn't. Fix: read every cohort in B1's table; conclusion has to hold across the cohorts, not one selected one.
