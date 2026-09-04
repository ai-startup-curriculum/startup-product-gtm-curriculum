# Exercise 06 — Motion Mismatch Diagnosis Teardown

**Estimated time:** 3 hours
**Chapter link:** [`06-motion-mismatch-diagnosis.md`](../06-motion-mismatch-diagnosis.md)
**Prerequisite:** Chapter 6 read end-to-end; a real or reconstructed GTM situation with observable symptoms — either your own startup at seed-through-Series-B, a public case study of a company that pivoted its motion (e.g., a documented enterprise-to-PLG or PLG-to-enterprise transition), or a hypothetical scenario built by degrading a healthy motion (e.g., "what would Loomly's mid-market SDR-AE motion look like if we forced it onto a $6K bottoms-up developer product"). Chapters 1-5 read; Exercises 01 and 05 useful as inputs but not strictly required.

## Problem statement

Chapter 6 named the four canonical motion mismatches — enterprise ceremony on a self-serve product, self-serve on a $100K contract, mid-market SDR-AE on a bottoms-up developer product, sub-scale CAC / payback on any motion — and named the failure mode: founders reach for in-motion levers (hire another SDR, coach the AE, buy a better cadence tool) when the actual diagnosis is a mismatch, wasting another quarter of runway on the wrong motion.

This exercise trains you to **run the full five-step teardown** — locate the actual motion on the Chapter 1 matrix; read the Chapter 5 CRM signals honestly; score the three symptom families quantitatively; match to a canonical mismatch (or rule them out); prescribe the fix, the pack change, and the sequencing — on a specific case, and to communicate the diagnosis to the four audiences the pivot requires.

The failure mode this exercise exists to catch: **the founder runs a "diagnosis" that is really a list of complaints ("SDRs aren't performing," "the market is soft"), skips the matrix location step, doesn't cite CRM numbers, and prescribes a fix that is either an in-motion tweak masquerading as strategy or a pivot in the wrong direction — because the teardown was never structurally run**.

## Requirements

Deliver a folder `exercise-06/` with three files:

- `part-a-case-and-symptom-scoring.md` — the case description with quantitative symptom scoring across the three families.
- `part-b-teardown-and-prescription.md` — the five-step teardown; the matched mismatch; the prescribed fix.
- `part-c-communication-plan.md` — the four-audience communication (team / board / customers / market).

### Part A — Case description and symptom scoring (75 min)

Deliver `part-a-case-and-symptom-scoring.md`.

**A1 — Case selection and source (10 min).** Name the case and label the source honestly:

- **Own startup (real, current situation)** — preferred; the teardown produces immediately-usable output.
- **Own startup (historical retro)** — a decision made 6-18 months ago, retro'd now with the discipline. Useful for pattern-recognition.
- **Public case study** — a documented company pivot (e.g., HubSpot's early motion evolution, a well-known PLG-to-enterprise transition). Cite the source URL.
- **Constructed scenario** — a hypothetical built from your own ICP + ACV combined with a plausible-but-mismatched motion (e.g., "if I forced enterprise MEDDPICC onto our $6K mid-market deals, what would break?"). Label clearly as constructed; the exercise is a mechanics demonstration.

**A2 — Motion-as-installed (15 min).** Describe the current motion in the shape Chapter 1's matrix requires:

- **ICP band and behavioural signature** — firmographic band, buyer/user/champion split, self-service willingness (with evidence).
- **ACV band and pricing pack** — anchor tier ACV, pricing metric, tier structure.
- **Motion installed** — primary motion + any layers (per Exercise 01's brief format).
- **Team allocated to the motion** — SDR count, AE count, SE count, sales-assist reps, CS, growth engineers. Include OTE ballparks.
- **Tooling installed** — CRM, cadence tool, product analytics, billing.
- **Time since motion installed** — months / quarters. This matters for the differential rule (Chapter 6): two consecutive quarters of no-movement escalates in-motion problems to mismatch teardowns.

**A3 — Symptom family scoring — Family A: unit-economic (15 min).** Report the specific numbers with sources:

- **CAC per closed customer** — blended, over the last 6-12 months. Cite the calculation (sales team cost + tooling + marketing spend ÷ closed customers).
- **CAC payback (months)** — CAC ÷ (monthly gross margin per customer). Compare to Chapter 6's benchmarks: ≤ 6 months (self-serve), ≤ 12 months (mid-market), ≤ 18-24 months (enterprise).
- **Blended gross margin** after full sales-team cost allocation.
- **Payback vs. median retention** — is payback shorter than the median customer's retention window?
- **Trend** — is CAC climbing, flat, or falling QoQ; is payback stretching or compressing?

Grade Family A: healthy / borderline / broken.

**A4 — Symptom family scoring — Family B: funnel-shape (15 min).** Report the specific numbers per stage per Chapter 5's CRM discipline:

- **Top-of-funnel volume** (sign-ups if PLG; booked meetings if SDR-AE; qualified opportunities if enterprise).
- **Conversion at each stage boundary** — sign-up → activation, activation → PQL, PQL → paid (PLG); booked → held, held → opp, opp → close (SDR-AE); Discovery → Evaluation → Proposal → Negotiation → Close (enterprise).
- **Stage-specific pipeline health** — which stage has the deepest leak? What is the median cycle time at each stage vs. the working benchmark?
- **Compare to Chapter 3 / Chapter 5 benchmarks** — note where numbers sit inside the healthy range, at the edge, or clearly outside.

Grade Family B: healthy / borderline / broken. If broken, identify the specific stage.

**A5 — Symptom family scoring — Family C: team-and-narrative (10 min).** Report the qualitative signals:

- **Sales team dynamics** — turnover, ramp attainment, quota attainment %, morale signals.
- **Founder time on selling** — hours/week; is the founder still closing deals well past the mod-105 hand-off point?
- **Buyer language vs. vendor pitch language** — are buyers asking for things the pitch doesn't discuss? Is the pitch describing things buyers don't ask about?
- **Investor update language** — is the founder hedging ("still tuning," "green shoots," "conversion improving from low base") in a way that suggests the motion cannot yet be described positively without qualification?
- **Champion / user community sentiment** (PLG) — are champions going silent post-hand-off? Is the free-tier community enthusiastic while the paid funnel is quiet?

Grade Family C: healthy / borderline / broken.

**A6 — Cross-family summary (10 min).** In one line per family:

```
Family A (unit-economic): {grade}, primary evidence: {one-line}
Family B (funnel-shape): {grade}, primary evidence: {one-line}
Family C (team-and-narrative): {grade}, primary evidence: {one-line}
Cross-family cluster: {number of families broken or borderline; note whether this is a single-family in-motion signal or a cross-family mismatch signal per Chapter 6's differential rule}
```

### Part B — Teardown and prescription (60 min)

Deliver `part-b-teardown-and-prescription.md`.

**B1 — Step 1: Matrix location and gap (10 min).** Chapter 6's first step. Compare:

- **What ICP + ACV combination is the current motion designed for?** (E.g., "SDR-AE inside sales is designed for mid-market $10-100K ACV with buyer-committee complexity.")
- **What ICP + ACV combination is the pipeline actually selling to?** (E.g., "the pipeline is 80% bottoms-up developer sign-ups at implied $6-8K ACV.")
- **Do they match?** If yes, in-motion diagnosis expected. If no, mismatch expected.

**B2 — Step 2: Read the CRM signals honestly (10 min).** Chapter 6's second step. If Chapter 5's discipline has been installed (Exercise 05), the CRM tells you:

- Which stage is the pipeline leaking at?
- Which artifact is systematically missing?
- Which MEDDPICC / SPICED letter is systematically red?

If the CRM has not been run with Chapter 5 discipline, the teardown pauses here until it has been (Exercise 05 is a prerequisite in that case; note it).

**B3 — Step 3: Score the symptom family cluster (5 min).** Import Part A's Family A / B / C grades and cross-family summary. Chapter 6's rule: cross-family cluster (2+ families broken) is usually a mismatch; single-family broken is usually in-motion.

**B4 — Step 4: Match to a canonical mismatch (or rule them out) (15 min).** Test the symptom cluster against each of Chapter 6's four canonical mismatches:

- **Mismatch 1 — Enterprise ceremony on a self-serve product** — does the symptom pattern fit? What in Family A / B / C is consistent with it?
- **Mismatch 2 — Self-serve on a $100K contract** — does it fit?
- **Mismatch 3 — Mid-market SDR-AE on a bottoms-up developer product** — does it fit?
- **Mismatch 4 — Sub-scale CAC / payback on any motion** — does it fit?

Note whether a **compound mismatch** applies (Chapter 6's compound patterns: 1+4, 2+4, 3+2). If no mismatch fits, name the in-motion diagnosis explicitly and exit with an in-motion prescription (hiring / tooling / discipline change).

**B5 — Step 5: Prescription and sequencing (20 min).** Author the prescription in the shape Chapter 6 requires:

- **New motion** (or continued current motion with defined adjustments if in-motion). Reference Chapter 2 / 3 / 4 for the specific motion design.
- **Pack change** (mod-106) — what pricing / tier / metric changes are needed to support the new motion. Chapter 6's rule: motion + pack are joint decisions.
- **ICP re-scoping** (mod-104) — is the primary ICP being changed, narrowed, or expanded?
- **Team changes** — which roles become wrong, which roles become required. Specific hires and specific reassignments.
- **Sequencing** — what to stop first (e.g., "freeze new SDR outbound"); what to keep running while the new motion ramps (e.g., "AE continues serving PQL-triggered accounts"); what to start (e.g., "ship the free tier and activation instrumentation; hire growth engineer at month 2"); expected timeline to see the numbers move (Chapter 6's default: 60-90 days to first signal, 2 quarters for full evaluation).
- **Success criteria** — the specific numbers that would tell you the pivot worked, at 90 / 180 / 365 days.

### Part C — Four-audience communication plan (45 min)

Deliver `part-c-communication-plan.md`. Chapter 6 names the four audiences a motion pivot needs to be communicated to, each with a different tone and level of detail.

**C1 — Team-facing communication (15 min).** Draft the message to the team (sales team + adjacent — customer success, product marketing, growth). Chapter 6's rule: over-communicate to the team; blame-free; explicit about who's role changes and how.

Structure:

```
# Team announcement — {date}

## What we learned
{2-3 sentences on the diagnosis — motion mismatch named honestly, not spun}

## What we're changing
- {The new motion, in one sentence}
- {The pack change, in one sentence}
- {The team-role changes — who does what now}

## What each person's role becomes
- {Person / role 1}: {new responsibility or continued responsibility}
- {Person / role 2}: {new responsibility}
- {Any role being sunset — say it plainly, with the offboarding / transition plan}

## Timeline
- {What happens this week}
- {What happens by end of quarter}
- {When we re-evaluate}

## What we're not changing
- {Elements of the existing motion that continue}
- {Product roadmap, positioning, or other things the team might worry are affected}

## Questions
- {Where to ask; standing office hours or channel}
```

**C2 — Board-facing communication (10 min).** Draft the board memo (or the appendix in the next board update). Chapter 6's rule: named honestly; framed as diagnosis-driven; the teardown is the evidence; the plan is the ask.

Structure:

```
# Board update appendix — {product} motion review — {date}

## Summary
{2-3 sentences: diagnosis + prescription}

## Teardown
- Matrix location: {gap}
- CRM signals: {leaking stage}
- Symptom cluster: {families broken}
- Matched mismatch: {which one, or in-motion diagnosis}

## Prescription
- New motion + pack change + role changes: {compressed}
- Sequencing: {compressed}
- Expected timeline to signal: {60-90 days for first, 2 quarters for full}

## Ask
- Runway impact: {any cash-burn change}
- Expectation reset on next quarter's numbers: {be specific}
- Hiring changes requiring board / investor sign-off: {any}
```

**C3 — Customer-facing communication (10 min).** Draft the message to the affected customers (existing customers on a pack being replaced; customers whose rep is changing; customers whose contract terms shift). Chapter 6's rule: proactive; migration story per mod-106 Chapter 5's grandfathering discipline; silence produces churn a five-minute email would prevent.

If no customer-facing communication is needed (the pivot is upstream of the customer), state that explicitly and note why.

**C4 — Market-facing communication (10 min).** Name the surfaces the pivot changes:

- **Pricing page** — does it need to be rewritten? By when?
- **Positioning / homepage** — does the primary buyer message change?
- **Pitch deck** — does the outbound pitch and inbound demo deck need refresh?
- **Public statements** — does the founder need to update a Twitter thread, blog post, or podcast talking point where the old motion was publicly discussed?

For each surface: what changes, who owns the update, target date.

## Starter guidance

- **The differential rule is the whole game.** Chapter 6's core question: is this in-motion execution or a mismatch? The rule: cross-family symptom cluster + no in-motion knob moving the numbers over 2 quarters = mismatch. Single-family broken + specific stage / discipline root cause = in-motion. Get this call right and the prescription follows; get it wrong and you either over-pivot (destroying a fixable motion) or under-pivot (staying on a broken one).
- **Score symptoms quantitatively, not adjectivally.** "CAC is high" is a complaint; "CAC payback is 22 months vs. mid-market benchmark of ≤ 12" is a symptom. Every Family A number has a $ or a month attached; every Family B number has a % or a count attached; every Family C signal has a specific behavior or quote attached.
- **Chapter 5's CRM discipline is a prerequisite.** If your CRM has not been run with artifact-per-stage discipline, your Family B numbers are noise and the teardown at Step 2 stalls. Exercise 05 first, then Exercise 06.
- **Compound mismatches unstack.** Chapter 6's compound patterns (1+4, 2+4, 3+2) are diagnosed by naming each mismatch separately and sequencing the fixes. Attempting to fix all mismatches simultaneously is the pivot-form of Chapter 1's *run-all-three-motions-simultaneously* trap.
- **The pack change is part of the prescription, always.** Chapter 6's discipline: motion + pack are joint decisions. A pivot to PLG without a per-seat / per-usage pack that supports self-serve checkout will fail for pack reasons that look like new-motion failure. A pivot to enterprise without an enterprise tier will fail similarly. Prescribe pack changes explicitly.
- **Sequencing is what makes the pivot land.** "Kill the old motion, start the new motion" produces a whipsaw quarter with no revenue. Chapter 6's discipline: freeze the old motion's expansion; keep the current pipeline running through close; ship the new motion in parallel; kill the old motion on a defined date after the new one has demonstrated signal.
- **Team communication is over-communicated; board communication is briefly-communicated.** The mistake Chapter 6 names: founders brief the board in detail (because they're worried about investors) and hand-wave to the team (because it's awkward). The opposite is correct — the team needs the detailed explanation because their roles change; the board mostly needs to know that the diagnosis was disciplined and the plan is sound.
- **Named honestly, not spun.** The team-facing announcement should not say "we're pivoting to unlock a new opportunity" if the actual diagnosis is "we installed the wrong motion 12 months ago and are correcting the mistake." Language that spins the pivot into a positive-only narrative loses the trust of the team members who can see the reality; language that names the mistake directly (blame-free but honest) preserves trust.
- **Success criteria are specific, not aspirational.** "The pivot works if we grow revenue" is not a success criterion. "The pivot works if the new self-serve funnel produces 200 paid accounts at $180 average CAC by month 6" is a success criterion. Chapter 6's rule: name the number that would falsify the diagnosis.
- **If the diagnosis is in-motion, say so.** Not every teardown produces a mismatch. If Family A is healthy and Family C is healthy and only Family B is broken at one specific stage, the diagnosis is in-motion (hire a role, tune a bar, coach an AE). Don't manufacture a mismatch to feel decisive; the honest in-motion diagnosis is often the right answer.
- **The teardown is *cheap* relative to the alternative.** One week of founder time to run the teardown. The alternative — another quarter of tuning the wrong motion — is millions of dollars in wasted runway. The exercise's ROI is measured in quarters saved.

## Acceptance criteria

Your submission is complete when:

- [ ] Part A names the case with source label (real / retro / public / constructed).
- [ ] Part A describes the motion-as-installed with ICP, ACV, motion + layers, team allocation, tooling, time since installed.
- [ ] Part A scores Family A (unit-economic) with CAC, payback, gross margin, payback-vs-retention, trend, and a healthy / borderline / broken grade.
- [ ] Part A scores Family B (funnel-shape) with per-stage volume + conversion + cycle time, comparison to benchmarks, and a healthy / borderline / broken grade.
- [ ] Part A scores Family C (team-and-narrative) with sales-team dynamics, founder-time-on-selling, buyer-vs-pitch language, investor-update hedging, community sentiment, and a healthy / borderline / broken grade.
- [ ] Part A ends with a cross-family summary line naming whether the cluster indicates in-motion or mismatch.
- [ ] Part B runs Step 1 (matrix location gap), Step 2 (CRM signal read), Step 3 (import Part A scoring), Step 4 (match to canonical mismatch or rule out), Step 5 (prescription + sequencing).
- [ ] Part B's Step 4 tests all four canonical mismatches explicitly (not just the one the founder was already leaning toward).
- [ ] Part B's Step 5 prescription includes new motion + pack change + ICP re-scoping (if any) + team changes + sequencing + success criteria at 90 / 180 / 365 days.
- [ ] Part C provides team / board / customer / market communication drafts — each in the given structure.
- [ ] Part C's team message names role changes plainly (including any role sunsetting) with the offboarding / transition plan.
- [ ] Part C's board memo compresses to fit an appendix (2 pages max) with teardown + prescription + ask.
- [ ] If no customer-facing or market-facing communication is needed, Part C states so explicitly with reason.
- [ ] Any factual claim (a benchmark, a public-company pivot detail, a competitor's motion) that is not from Chapter 6's cited sources or your own data is flagged `<!-- needs-research: ... -->` rather than invented.
- [ ] Constructed / hypothetical elements are labelled clearly; the teardown output is treated as mechanics demonstration rather than fielded diagnosis.

## Common ways this exercise goes wrong

- **Skip-the-matrix-step trap.** Part B starts at Step 3 or Step 4 without Step 1's matrix location check. Diagnosis becomes "the numbers are bad" without naming *what the motion was designed for* vs. *what the pipeline is actually selling to*. Fix: Step 1 first; if the matrix locations match, the diagnosis is in-motion; if they don't, the diagnosis is a mismatch.
- **Adjectival-symptom-scoring trap.** Part A grades Family A "not great" and Family C "concerning." Grades are non-actionable. Fix: every grade cites a specific number with a source; every "broken" grade names the specific gap vs. benchmark.
- **Mismatch-shopping trap.** Founder wants the diagnosis to be Mismatch 2 (enterprise gap) because it justifies hiring the enterprise AE she wanted anyway. Fix: Step 4 tests all four canonical mismatches; the diagnosis is what the cluster fits, not what the founder prefers.
- **In-motion-masquerading-as-mismatch trap.** Family B is broken at one specific stage (Discovery → Evaluation conversion is 15% vs. benchmark 40%) but Family A and C are healthy. Founder pivots the motion. Actual diagnosis was a bad first AE hire; new motion also fails because the hire is still bad. Fix: single-family broken usually = in-motion; check the differential rule before pivoting.
- **Mismatch-masquerading-as-in-motion trap.** Founder tunes SDR cadence templates for two quarters against a motion that fundamentally does not fit the ICP; conversion never moves. Founder concludes the SDR needs more coaching. Fix: two-consecutive-quarter rule — if in-motion fixes have not moved the numbers over 2 quarters, escalate to a mismatch teardown.
- **Pack-change-forgotten trap.** Part B prescribes a new motion but not the pack change that supports it. New motion runs against the old pack; fails for pack reasons. Fix: Step 5 explicitly names the pack change per Chapter 6's rule.
- **Simultaneous-pivots trap.** Part B prescribes changing the motion, the pack, the ICP, and the team simultaneously. Each pivot has 60-90 days of setup; simultaneous pivots produce whipsaw. Fix: sequence the pivots; name what happens first, second, third.
- **Team-communication-vague trap.** Part C's team announcement says "we're evolving our GTM approach" without naming role changes. Team senses risk; quiet resignations follow. Fix: name role changes plainly; blame-free but explicit.
- **Board-communication-detailed-while-team-communication-vague trap.** Founder writes a 4-page board memo and a 1-paragraph team note. Team feels blindsided; board feels micromanaged. Fix: over-communicate to team, briefly to board with teardown + plan + ask.
- **Success-criteria-aspirational trap.** Part B's success criteria are "revenue grows" or "conversion improves." No numbers, no dates. Fix: specific numbers at specific milestones; the criteria are what would falsify the diagnosis if not met.
- **Customer-communication-skipped trap.** Pivot affects existing customers (pack change, rep change, contract shift) but Part C skips customer communication. Silent grandfathering / rep-swap produces churn. Fix: proactive migration story per mod-106 Chapter 5.
- **Market-surfaces-forgotten trap.** Pricing page and pitch deck are not updated for 3 months post-pivot. New buyers see the old positioning. Fix: C4 names every affected surface with owner and target date.
- **Never-schedule-the-re-teardown trap.** Exercise 06 is run once and the founder assumes the diagnosis is durable. Six months later the market has moved and a new mismatch is developing. Fix: schedule the next teardown per Chapter 6's cadence (quarterly at seed, monthly at Series A); the teardown is a reading practice, not a one-time event.
- **Constructed-case-without-transferable-lesson trap.** Constructed / hypothetical scenario is worked through but the mechanics are not tied back to what the founder would do in her own situation. Fix: constructed cases should end with a "what this means for my own motion" paragraph — the transferable lesson.
