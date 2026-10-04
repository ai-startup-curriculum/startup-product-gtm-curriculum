# Exercise 06 — Paid Guardrails and Attribution Drill

**Estimated time:** 3 hours
**Chapter link:** [`06-paid-acquisition-at-pre-series-a.md`](../06-paid-acquisition-at-pre-series-a.md)
**Prerequisite:** Chapter 6 read end-to-end; Exercise 02 completed (a channel-market-fit four-gate diagnosis you can extend to paid); a mod-106 pricing pack (ACV band + gross margin + payback envelope); a mod-102 PMF signal read (needed to decide whether paid can scale past learning-motion budget); a mod-104 ICP scorecard; Exercise 01 completed (the portfolio decision — paid is either the primary, the experimental, or on the dated "not now" list with a trigger). If any upstream input is not yet in a defensible state, use a labelled `PLACEHOLDER` per Chapter 1's placeholder discipline.

## Problem statement

Chapter 6 named paid as the **fastest channel to measure and the most dangerous channel to scale before PMF**. It identified the three surface families (search / social / retargeting), the three spend guardrails (total-budget ceiling / per-channel test floor / payback-period stopcock), the three paid-specific attribution risks (platform-reported-vs-CRM, last-touch over-crediting, branded-search leakage), the **pre-PMF trap** (buying a growth curve the product cannot retain), the small-experiment discipline (one channel, one hypothesis, one stop criteria, one four-gate diagnosis, one write-up), and the three-question surface-choice sequence.

The failure mode: the founder, under board-deck or fundraise pressure, turns on paid at $20-30K/month before PMF signal has fired or retention parity has been proven; the top-of-funnel metric looks like progress for two quarters; cohort retention arrives 60-180 days later; CAC : LTV inverts; runway consumed. Or the mirror failure: the founder refuses to run paid on principle; two years later a competitor has captured 40% of the branded-search real estate and recovery requires a much larger budget.

This exercise trains you to **design the paid programme the way it actually works at pre-Series-A** — size the spend guardrails against your actual pricing and PMF state, pick one paid experiment per the three-question surface-choice sequence, author the paid-attribution plan with the three honesty extensions wired in, write the pre-PMF go/no-go gate, draft the small-experiment design (hypothesis, stop criteria, four-gate diagnosis checkpoints, write-up template), and run a reconstruction audit of a hypothetical paid-attributed cohort to practise the attribution-truthfulness discipline.

The failure mode this exercise exists to catch: **the founder writes "we're spending $15K/month on Google + LinkedIn + Meta + retargeting" without guardrails, without a hypothesis, without a stop criterion, and without the attribution extensions — and six months later cannot defend whether paid worked, is working, or will keep working.**

## Requirements

Deliver a folder `exercise-06/` with five files:

- `part-a-guardrails-and-pmf-gate.md` — the three spend guardrails sized to your pricing + PMF state + the pre-PMF go/no-go gate.
- `part-b-surface-choice.md` — the three-question surface-choice sequence applied to your startup + the first paid experiment pick.
- `part-c-experiment-design.md` — the one-paid-experiment design (hypothesis / stop criteria / setup / four-gate checkpoints).
- `part-d-attribution-plan.md` — the paid-specific attribution plan (platform-vs-CRM; first-touch + last-touch; branded-search separation; audit template).
- `part-e-reconstruction-audit.md` — the attribution reconstruction drill on 10 hypothetical paid-attributed deals.

### Part A — Guardrails and PMF gate (30 min)

Deliver `part-a-guardrails-and-pmf-gate.md`.

**A1 — Total-budget ceiling (10 min).** Chapter 6's Guardrail 1: paid spend at pre-Series-A should not exceed **10-25% of gross-margin-adjusted new revenue** on a rolling 6-month basis, with an absolute hard ceiling in the **$5-25K/month range** during the learning phase. Compute your ceiling.

- **Inputs.** From mod-106: ACV, gross margin %, monthly new ARR (actual if available; forecast if pre-launch). From Exercise 01: the stage you are in (pre-PMF / post-PMF / Series-A-raising).
- **Arithmetic.** `rolling-6-mo new ARR × gross-margin% × 0.10` and `rolling-6-mo new ARR × gross-margin% × 0.25` → the ceiling range. Compare to the absolute $5-25K/month corridor; take the lower of the two bounds. Show the arithmetic.
- **Output.** Your monthly paid-budget ceiling, in dollars, for the learning phase.
- **Adjustment for pre-PMF stage.** If mod-102 PMF signal has not fired (<40% "very disappointed" on target ICP), set the ceiling at the floor of the range ($3-5K/month total across all paid) — the three exceptions in A3 are the only paid programmes allowed.

**A2 — Per-channel test floor (5 min).** Chapter 6's Guardrail 2: a paid experiment on a specific channel needs **≥ $3-5K of spend + ≥ 50 conversion events over 4-8 weeks** to produce a defensible signal. Below the floor the CAC number is noise.

- Compute: at your ACV + expected conversion-rate assumption, what spend and what time window produces ≥ 50 conversion events on your target surface? Show the arithmetic.
- Output: the floor budget and the test window length for the one surface Part B will pick.

**A3 — Payback-period stopcock (5 min).** Chapter 6's Guardrail 3: a paid channel that has run past its time-to-signal (≥3-6 months + ≥50 closed deals) and cannot demonstrate payback **≤ 18 months** on the acquired cohort should be paused, not scaled.

- Compute: at your ACV, gross margin, and current CAC assumption, what is the payback period? Show the arithmetic.
- Output: the maximum defensible CAC for your paid programme (the number above which the payback would exceed 18 months). This is the stopcock number. If the campaign's observed CAC drifts above it for 2 consecutive months, the campaign pauses pending a four-gate re-diagnosis.

**A4 — Pre-PMF go/no-go gate (10 min).** The load-bearing section of Part A. Chapter 6's rule: do not scale paid past the small-experiment budget until **all three conditions** are met: (a) mod-102 PMF signal fires at ~40% "very disappointed" on target ICP; (b) organically-acquired cohort has demonstrated retention parity or better against non-paid benchmarks; (c) paid-cohort 90-day retention (from the small paid test) is within 10 pp of organic-cohort 90-day retention.

Write your gate:

- **Condition (a) status.** Current mod-102 reading. If not yet measured, say so and schedule the measurement before paid spend scales.
- **Condition (b) status.** Organic cohort retention vs. non-paid benchmarks. If retention has not yet been characterised (common pre-PMF), the gate is red by default.
- **Condition (c) status.** Paid-cohort 90-day retention vs. organic — not measurable until the paid test cohort has 90 days of tenure. Schedule the measurement for 90 days after the test's first conversion event.
- **Current gate state.** All three green = scale allowed; any one red = stay at learning-motion budget; any one amber = extend the test window and re-diagnose.
- **Exceptions.** Chapter 6 names two: **(i) branded-defence** (always defensible, separate from acquisition-CAC); **(ii) a tightly-scoped ICP-validation test** (≤$5K over 4-6 weeks, learning-exercise shape). Specify whether either exception applies to your Q+1 paid plan.

### Part B — Surface choice (30 min)

Deliver `part-b-surface-choice.md`. Chapter 6's three-question surface-choice sequence.

**B1 — Where is the ICP reachable through paid targeting? (10 min).** For each of the three surface families, score fit on 0-3:

- **Search (Google / Bing / Reddit search ads).** Does the ICP use recognisable transactional queries ("best X for Y", "X vs Y", "X pricing", "X alternatives")? Does the ICP already have a problem-recognition behaviour that paid search can serve? Branded-defence candidate? Enumerate the specific query clusters you would bid on.
- **Social (LinkedIn / Meta / X / Reddit / YouTube).** Is the ICP concentrated enough on one platform to be targetable at defensible precision? What is the targetable audience size at the specific job-title + firmographic filter level? If LinkedIn: is the ICP VP-level or Director-level in companies at the firmographic tier?
- **Retargeting.** Does the site have ≥ 5,000 monthly unique first-party visitors to build a defensible retargeting pool? If no, retargeting is deferred until inbound traffic accumulates.

Score each 0-3 on fit. The highest-scoring family is the first paid experiment candidate.

**B2 — What does the CAC math support? (10 min).** From Part A's arithmetic:

- Your ACV band + gross margin → max defensible CAC → the surface families whose typical CAC ranges fit inside the envelope.
- **$99-499/month self-serve:** CAC ceiling $200-800; usually only Google search on transactional queries + specific look-alike social works at this envelope.
- **$10-30K/year mid-market SaaS:** CAC ceiling $3-9K; supports LinkedIn Ads targeted at VP/Director + Google Ads transactional.
- **$100K+/year enterprise:** CAC ceiling $25K+; account-based advertising + targeted display + search; often better served by partnerships + events than paid.

Match your ACV band to the surface candidates. Eliminate any that would exceed the stopcock number from Part A3.

**B3 — What does the downstream funnel need? (5 min).** Chapter 6's third question: paid produces top-of-funnel that has to be converted through the same downstream funnel the other channels feed. If the demo-conversion stage is broken, more leads will not fix it. Audit:

- Is the mod-105 discovery script producing acceptable advance rates on inbound-generated meetings? (If no, fix the funnel first.)
- Does the pricing pack (mod-106) support the sign-up experience the paid ad would promise? (If a paid ad is going to promise self-serve but the pricing is contact-sales-only, the paid programme will burn out on refund-and-abandon.)
- Is the sales motion (mod-107) resourced to handle an additional 2-5× top-of-funnel volume this surface would produce? (If no, defer scaling until the motion is ready.)

Any red answer here defers paid; the funnel is upstream of the surface choice.

**B4 — Pick the first paid experiment (5 min).** From B1-B3, name the one surface + one hypothesis you will run the small-experiment design against in Part C. Second-ranked candidate noted as the sequential-next experiment if the first fails or produces inconclusive results.

### Part C — Experiment design (45 min)

Deliver `part-c-experiment-design.md`. Chapter 6's small-experiment discipline has four elements: hypothesis + stop criteria + four-gate diagnosis + write-up.

**C1 — Written hypothesis (10 min).** Chapter 6's rule: the hypothesis is written down *before* the test starts, in the shape *"{surface} on {targeting} will produce {outcome} at a CPA below ${Y} over {N} weeks."* Write yours:

- **Surface.** The specific family + sub-surface from Part B4 (e.g., "LinkedIn Ads sponsored content"; "Google Ads on transactional queries"; "branded-defence on Google").
- **Targeting.** The specific targeting criteria (job titles + firmographic filters for LinkedIn; keyword cluster + match type for Google; look-alike audience seed + size for Meta).
- **Outcome.** The specific conversion event the campaign is optimising for (ICP-fit sign-ups; demo requests; MQLs; downloads of a gated resource). Must be a defined action, not a vague "awareness" or "engagement".
- **CPA target (Y).** The maximum CPA that would still fit inside the stopcock from Part A3. If observed CPA exceeds Y for 2 consecutive weeks, the stop criterion fires.
- **Test window (N weeks).** 4-8 weeks per Chapter 6. Specify a start date and an end date.

**C2 — Stop criteria (10 min).** Write the specific triggers that end the experiment early. From Chapter 6:

- **CPA trigger.** CPA stays above the Y target for 2 consecutive weeks → pause and diagnose.
- **Volume trigger.** Conversion volume below 20/week for 3 consecutive weeks → the surface is not producing enough signal; pause.
- **Budget trigger.** Spend hits the total-budget ceiling from Part A1 before the window closes → pause and reassess.
- **Quality trigger.** Gate 1 (ICP-fit lead quality) scored at the 2-week checkpoint is below 60% → the targeting is wrong; pause and tighten before continuing.
- **PMF-gate trigger.** The Part A4 pre-PMF gate goes red mid-experiment (e.g., retention data arrives showing paid-cohort 90-day retention is 20pp below organic) → pause scaling discussion; experiment stays at learning-motion budget.

Each trigger has a specific action (pause / tighten / reassess), not a vague "we'll look at it".

**C3 — Setup specifics (10 min).** Write the specific setup the experiment will launch with:

- **Campaign structure.** Name of the campaign, ad group / ad set structure, number of creative variants, bidding strategy (manual CPC / automated / target-CPA), bid or max-CPC ceiling.
- **Daily / weekly / total budget.** Must respect the Part A1 ceiling and the Part A2 floor.
- **Creative.** 3-5 variants. Specify: image / video / copy source (first-party vs. LLM-generated), the hook (positioning statement from mod-103), the CTA, the landing page URL. From Chapter 6's Amendment 3: distinctive first-party creative outperforms LLM-generated variants.
- **Landing page.** The conversion surface — pillar page, pricing page, dedicated LP, gated resource. Form fields: email + "how did you hear about us?" + role + company at minimum.
- **UTM template.** `utm_source={platform}, utm_medium={paid_search / paid_social / retargeting}, utm_campaign={experiment_name}, utm_content={variant}`. Must be consistent to let Part D's attribution plan work.

**C4 — Four-gate diagnosis checkpoints (10 min).** Chapter 2's four-gate diagnosis + Chapter 6's paid-specific extensions. Specify when each gate is read:

- **Gate 1 — ICP-fit lead quality.** Read at **week 2** and **week 6**. Measurement: ICP-fit score of the conversion cohort against the mod-104 scorecard (buyer / user / champion split; firmographic fit). Target: ≥80% green at week 6.
- **Gate 2 — unit economics.** Read at **week 6** and **week 12**. Measurement: fully-loaded CAC (ad spend + founder time + tooling + landing-page attributable production), using **CRM-computed closed revenue, not platform-reported conversions** (Chapter 6 Risk 1). Target: payback ≤ the Part A3 stopcock number.
- **Gate 3 — time-to-signal maturity.** Read at **week 12** / end of window. Measurement: ≥ 50 conversion events + ≥ Part A2 floor spend + ≥ 3-6 months (if the window has been extended). The CAC number is only defensible once this gate is green.
- **Gate 4 — attribution honesty.** Read **throughout**. Measurement: self-reported source completion rate (≥85%); CRM-vs-platform CAC variance (platform-reported should not be more than 30% below CRM-computed — if it is, something is wrong); branded-search separation (branded-defence conversions are tagged and excluded from acquisition CAC).

For each gate, specify who runs the measurement, in what tool, and what the pass / amber / red threshold is.

**C5 — Write-up template (5 min).** Chapter 6's rule: every experiment ends with a written note. Draft the one-page template:

```
# Paid Experiment Write-up — {experiment name} — {date}

## Hypothesis
{restate C1}

## Setup
{summarise C3}

## Result
- Spend: ${X}
- Conversion events: {N}
- CRM-computed CAC: ${X}
- Platform-reported CAC: ${X} (for comparison; not the primary number)
- Closed revenue (if available at window close): ${X}

## Four-gate diagnosis
- Gate 1 (ICP-fit): {green / amber / red} — {evidence}
- Gate 2 (unit economics): {green / amber / red} — {evidence}
- Gate 3 (time-to-signal): {green / amber / red} — {evidence}
- Gate 4 (attribution): {green / amber / red} — {evidence}

## Recommendation
{scale / iterate / kill / defer} — {reasoning}

## Next hypothesis (if any)
{what the result surfaced that justifies a follow-on test}

## PMF-gate status
{A4 reassessed at end-of-window}
```

### Part D — Attribution plan (30 min)

Deliver `part-d-attribution-plan.md`. Chapter 6's three paid-specific attribution risks + the audit discipline.

**D1 — Platform-vs-CRM reconciliation (10 min).** Chapter 6 Risk 1: platform-reported attribution is aspirational (observed + modelled); CRM-computed CAC on closed-won revenue is the truth. Specify:

- **Primary CAC source.** CRM report that filters opportunities by `utm_source = paid_{platform}` + `community_member = n/a (paid cohort)` and computes `(fully-loaded spend + attributable founder-time + tooling) ÷ closed-won deals in cohort`.
- **Platform number treatment.** Platform-reported CAC is a leading indicator; the dashboard shows it with a visible caveat ("platform-reported — may include modelled conversions; truth is CRM number below").
- **Reconciliation cadence.** Monthly: pull platform-reported conversion totals vs. CRM-sourced conversion totals; compute variance; if variance >30%, investigate (pixel broken? modelled conversions over-reporting? CRM mis-tagged?).

**D2 — First-touch + last-touch side-by-side (10 min).** Chapter 6 Risk 2: last-touch attribution over-credits paid on multi-touch buyer journeys. Specify:

- **Report structure.** Two reports side-by-side on every paid cohort: first-touch (which channel generated the first known contact?) and last-touch (which channel generated the final conversion event?). Difference between the two surfaces the multi-touch journeys.
- **Primary view for scale decisions.** Multi-touch (position-weighted or U-shaped) attribution — not last-touch. Chapter 6's rule: scaling decisions use multi-touch; last-touch is secondary.
- **Position-weighted formula.** Choose one: U-shaped (40% first-touch + 40% last-touch + 20% distributed to middle touches) or linear (equal distribution across touches). State which you are using and why.
- **Qualitative check.** On 10% of closed-won deals per quarter, manually reconstruct the full journey from CRM + email + self-reported source + platform reports. Compare to the attribution model's assignment. If the model consistently over-credits paid, revise the weighting.

**D3 — Branded-search separation (10 min).** Chapter 6 Risk 3: branded-search conversions get last-touch credit for customers paid did not acquire; blending them with acquisition paid inflates efficiency. Specify:

- **Branded-defence campaign tag.** `utm_campaign=brand_defence` on all branded-search ads; separate campaign structure in Google Ads (campaign name clearly tagged).
- **Reporting treatment.** Branded-defence conversions are reported in a separate line item ("branded-defence conversions saved") — never blended with the acquisition-CAC calculation.
- **Rule of thumb.** Branded-search CPC and CPA are not comparable to non-branded; the two are reported on separate lines, with separate budget line items.
- **Stop condition for branded-defence.** Chapter 6: do not stop branded-defence as a cost-cutting measure. If total paid budget is being cut, cut acquisition paid first; preserve branded-defence at 0.5-1.5% of new ARR.

### Part E — Reconstruction audit (45 min)

Deliver `part-e-reconstruction-audit.md`. Chapter 6's paid-attribution audit: once per quarter, reconstruct 10 closed-won paid-attributed deals end-to-end, and count how many were *actually* first-discovered through the paid channel.

This exercise is a drill: because you may not yet have 10 real closed-won paid-attributed deals, construct the audit on **hypothetical plausible journeys** that stress-test your Part D attribution plan.

**E1 — Construct 10 hypothetical journeys (25 min).** Build a table of 10 hypothetical deals. For each:

| # | Deal | First touch (what happened) | Second-Nth touch | Last touch | Platform-attributed to | CRM-attributed to | Actual-first discovery | Over-credit? |
|---|---|---|---|---|---|---|---|---|

Design the 10 journeys to include the common attribution risks:

- 2 deals where paid is genuinely the first touch and the correct attribution (control for over-correction).
- 2 deals where inbound (a blog post, an HN mention) was first touch and retargeting was last touch; last-touch over-credits paid.
- 2 deals where outbound (a founder cold email) was first touch and a Google search ad was last touch; last-touch over-credits paid.
- 2 deals where branded-search was last touch and the first touch was anything (community referral, HN, outbound) — classic branded-leakage.
- 1 deal where community (a Slack discussion) was first touch, a paid retargeting ad reinforced, and demo-request form was last touch; multi-touch should distribute credit.
- 1 deal where the self-reported source contradicts the platform attribution (e.g., self-report says "a colleague recommended it" but UTM says paid-social).

For each journey, name the platform-attribution assignment, the CRM-attribution assignment (per your Part D plan), and the *actual* first discovery (what the audit would reveal).

**E2 — Count the over-credits (10 min).** Chapter 6's audit threshold: **if fewer than 6 of 10 paid-attributed deals were actually first-discovered through the paid channel, the paid channel is over-credited and the effective CAC is materially higher than the dashboard reports.**

- Count your over-credits.
- If > 4 of 10, name the specific attribution-plan changes Part D needs (tighten branded-defence separation; weight first-touch more heavily; add self-reported-source as a tiebreaker).
- If ≤ 4 of 10, note which attribution risks the plan surfaces vs. misses.

**E3 — Audit cadence commitment (10 min).** Chapter 6: the audit runs once per quarter. Specify:

- The specific quarterly date (e.g., "last Friday of each quarter").
- The sample size (10 deals; if fewer than 10 closed-won paid-attributed deals in the quarter, run on all of them).
- The reviewer (founder for first 4 quarters; GTM lead after).
- The output artifact (a one-page memo appended to the quarterly review per Chapter 7 — includes over-credit count, specific journeys where attribution broke, specific plan changes).

## Starter guidance

- **Compute the arithmetic, do not estimate.** Part A's three guardrails are specific dollar numbers derived from your pricing + PMF state, not round-number estimates. "We'll spend $10K/month on paid" without the arithmetic is the pre-planning version of the pre-PMF trap. Show the arithmetic even when it feels obvious.
- **The PMF gate is the load-bearing section of Part A.** If mod-102 PMF signal has not fired, paid stays at learning-motion budget — the only exceptions are branded-defence and a tightly-scoped ICP-validation test. The gate is not advisory; it is a precondition for scaling past the small-experiment ceiling.
- **One experiment, one surface, one hypothesis.** The small-experiment discipline from Chapter 6 is not a style preference — it is the only way to produce defensible signal at seed scale. Running $500/month across five channels produces zero defensible answers. Pick one.
- **The three-question surface-choice sequence is sequential.** B1 (where is the ICP?) comes before B2 (what does CAC math support?) comes before B3 (what does the funnel need?). A surface that fails B1 is not rescued by passing B2. A surface that passes B1 and B2 but fails B3 defers; fix the funnel before scaling the paid.
- **Write the hypothesis before launching, not after.** The point of C1's written hypothesis is to make the result interpretable. If the hypothesis is written after the result, the hypothesis will be shaped to fit the result and the experiment has lost its diagnostic value.
- **CRM is truth; platform is leading indicator.** Chapter 6's Risk 1 is the most load-bearing operational discipline. Every dashboard that reports CAC should show CRM-computed primary + platform-reported secondary, with the variance visible. If you only have the platform number, you have a number that is 20-50% optimistic.
- **Branded-defence always, acquisition paid gated.** Even at pre-PMF, bidding on your own brand terms is defensible — it protects the brand-search close that the other channels generate. Blending its efficiency into the acquisition-CAC calculation is attribution self-deception. Separate campaigns, separate line items, separate budgets.
- **Distinctive first-party creative beats LLM-generated variants.** Chapter 6's Amendment 3 is operational, not aesthetic. In the AI-creative era, the auction fills with plausible-generic variants that all look the same; distinctive creative (real founder video, specific first-party claims, authentic customer quotes) breaks out. Budget creative accordingly.
- **The audit is the discipline, not a one-off.** Part E is a drill; the real audit runs once per quarter against real deals. If the quarterly audit never runs, Part D's attribution plan is a theory that was never tested, and the paid-CAC number drifts away from truth over time.
- **Paid does not create value; it converts value the product economics support.** If retention is weak, pricing is wrong, or the ICP is misdefined, paid will accelerate the deficit — not fix it. The pre-PMF gate exists because this failure is mathematically inevitable, not a judgement call.
- **Rejecting paid without a test is as diagnostic-invisible as scaling without guardrails.** Chapter 6's second failure mode is the founder who refuses to run paid on principle. The small-experiment design is the defensible answer — a $3-5K / 4-8 week test on one surface produces a yes/no answer on whether paid works for the ICP, without committing runway to a programme.

## Acceptance criteria

Your submission is complete when:

- [ ] Part A computes the three guardrails as specific dollar numbers (total-budget ceiling, per-channel test floor, payback stopcock) with arithmetic shown.
- [ ] Part A writes the pre-PMF go/no-go gate with current status on all three conditions, the exceptions, and the current overall gate state (green / amber / red).
- [ ] Part B scores the three surface families against question 1 (ICP reachability), eliminates candidates against question 2 (CAC math), and gates against question 3 (funnel readiness).
- [ ] Part B picks one surface + hypothesis as the first paid experiment and names the sequential-next candidate.
- [ ] Part C writes the hypothesis in the specific *"{surface} on {targeting} will produce {outcome} at a CPA below ${Y} over {N} weeks"* shape.
- [ ] Part C writes 5 specific stop criteria (CPA / volume / budget / quality / PMF-gate) each with a specific action.
- [ ] Part C writes the setup specifics (campaign structure, budget, creative variants, landing page, UTM template).
- [ ] Part C schedules four-gate diagnosis checkpoints with specific weeks, measurement sources, and thresholds.
- [ ] Part C drafts the write-up template in the structured format.
- [ ] Part D specifies the CRM-vs-platform reconciliation (primary source, caveat treatment, monthly reconciliation).
- [ ] Part D specifies first-touch + last-touch + multi-touch (position-weighted or U-shaped) with the formula.
- [ ] Part D specifies branded-search separation (campaign tag, reporting treatment, stop condition that protects branded-defence from cost-cutting).
- [ ] Part E constructs 10 hypothetical journeys covering the five Chapter 6 attribution risks, with platform-attribution / CRM-attribution / actual-first-discovery / over-credit flag for each.
- [ ] Part E counts the over-credits against the ≤ 4-of-10 threshold and names specific attribution-plan changes if the threshold is exceeded.
- [ ] Part E commits the audit cadence (date, sample size, reviewer, output artifact appended to Chapter 7 quarterly review).
- [ ] Any factual claim (a specific CAC benchmark, a specific platform CPC, a specific retention delta) that is not cited to Chapter 6 or a practitioner reference is flagged `<!-- needs-research: ... -->`.

## Common ways this exercise goes wrong

- **No-arithmetic trap.** Part A1 writes "we'll spend $10K/month on paid" without computing the 10-25% of gross-margin-adjusted new revenue arithmetic. The number is a feel, not a bound. Fix: show the computation; if $10K exceeds the 25% ceiling, the ceiling binds.
- **Skip-the-PMF-gate trap.** Part A4 is written but all three conditions are glossed as "we'll figure that out". Six weeks later, paid is scaling with no PMF signal in place. Fix: Part A4 is the load-bearing section; if any condition is red, paid stays at the learning-motion budget without exception (except branded-defence + ICP-validation test).
- **Four-surfaces-at-$500-each trap.** Part B picks "a bit of Google, a bit of LinkedIn, a bit of Meta, a bit of Reddit" with $500/month each. Per Chapter 6's Guardrail 2, none hits the test-floor; none produces defensible signal. Fix: one surface, $3-5K/month, 4-8 weeks.
- **Hypothesis-after-the-result trap.** Part C1 is left vague ("we'll see what happens with LinkedIn") and the hypothesis is written after the result arrives, shaped to the result. The experiment has lost diagnostic value. Fix: hypothesis written before launch, specific CPA target Y specified in advance.
- **No-stop-criteria trap.** Part C2 reads "we'll pause if things aren't working" without specific thresholds. Six months later, paid is still running with mediocre results and no clear stop decision. Fix: 5 specific triggers each with a specific action.
- **Platform-CAC-as-truth trap.** Part D1 reports CAC from Meta Ads Manager or Google Ads only. CRM-computed CAC is 40% higher. Scaling decisions are made against the optimistic number. Fix: CRM is primary; platform is secondary; variance monitored monthly.
- **Last-touch-only trap.** Part D2 reports only last-touch attribution. Retargeting gets credit for inbound-generated conversions; founder scales retargeting; the actual-performing channel is under-credited and under-invested. Fix: first-touch + last-touch side-by-side; multi-touch primary for scaling decisions.
- **Blended-paid-CAC trap.** Part D3 reports one paid-CAC number blending branded-defence (near-zero-CAC self-serve returns) with acquisition paid. Branded is $30; acquisition is $420; blended looks like $180. Scaling decisions treat blended as acquisition. Fix: separate line items, separate budgets, never blend.
- **Audit-is-theoretical trap.** Part E's 10 journeys are all "paid first touch, paid last touch, deal closed" — the drill doesn't stress-test the attribution plan. Fix: deliberately construct journeys covering the five Chapter 6 risks (inbound-first-paid-last; outbound-first-paid-last; branded-search-last; multi-touch; self-report-contradicts-platform).
- **Audit-cadence-not-committed trap.** Part E3 is left blank or the audit date is "we'll run it eventually". Attribution plan drifts; CAC-truth and CAC-reported diverge over quarters. Fix: specific quarterly date, specific sample size, specific reviewer, specific output artifact filed with the Chapter 7 quarterly review.
- **Reject-paid-on-principle trap.** Exercise concludes "we're a dev-tools company, paid is irrelevant" without running any experiment, including branded-defence. Two years later a competitor captures branded-search traffic. Fix: Chapter 6's second failure mode — the small-experiment discipline is the defensible answer; a $3-5K, 4-8-week test on one surface produces the yes/no.
- **Buy-the-growth-curve trap.** The exercise is written just before a fundraise; the paid budget is sized to produce impressive top-of-funnel numbers for the pitch deck, not to answer a learning question. Cohort retention arrives 60-180 days after the round closes; CAC : LTV inverts; runway consumed. Fix: fundraise narrative is grounded in retention-adjusted growth, not gross top-of-funnel; paid budget sized to the Part A guardrails, not the deck.
- **AI-creative-race-to-the-bottom trap.** Part C3 lists "40 LLM-generated image variants" as the creative plan; every competitor is doing the same; auction fills with plausible-generic variants; conversion rate collapses. Fix: distinctive first-party creative (founder voice, real customer imagery, specific claims) in a smaller variant count.
- **Kill-branded-defence-in-cost-cutting trap.** The exercise flags branded-defence as the first thing to cut if runway tightens. Chapter 6's rule: branded-defence is a permanent 0.5-1.5% of new ARR cost; cut acquisition paid first. Fix: branded-defence has stop-condition protection in Part D3.
- **Skip-the-write-up trap.** Part C5's write-up template is drafted but no commitment is made to actually run it at window close. Experiment ends; founder moves on; the learning does not accumulate. Fix: write-up is the artifact that turns paid from ad accounts into a learning programme; schedule the write-up appointment at window close before launching the campaign.
