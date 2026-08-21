# Magic Number, Sales Efficiency, and Funnel Conversion

## Motivation

CAC (Chapter 2), LTV, payback, and LTV/CAC (Chapter 3) are *per-customer* efficiency reads. This chapter zooms out to the *company-level* efficiency ratios — **magic number** and **sales efficiency** — and zooms in to the *pipeline-level* conversion the operator reads to see whether the motion is loading. Together with the retention numbers inherited from mod-109 (NRR, GRR, cohort retention), these are the last four numbers that go on the monthly GTM one-pager.

**Magic number** — the ratio of net-new ARR to the prior quarter's S&M spend — is the specific number a founder or GTM lead uses to answer *"should we spend more?"* It compresses CAC, LTV, retention, and go-to-market efficiency into a single dimensionless ratio. **Sales efficiency** is closely related but scoped differently in practice; this chapter fixes the distinction. **Funnel conversion** is the stage-by-stage read that tells you whether the motion the founder or AE runs is actually *producing* opportunities and advancing them at rates that match the historic model — the leading-indicator complement to the lagging-indicator magic number.

The failure mode this chapter exists to catch: **the founder scales S&M spend from $200k/qtr to $400k/qtr on the strength of "our CAC is fine and LTV/CAC is 3.4×," discovers a quarter later that net-new ARR grew from $300k to $350k rather than the expected $600k because the funnel-conversion rates degraded materially as spend was scaled through a saturating channel, and has burned an extra $200k with a magic number that dropped from 1.5 to 0.88 — a number that would have caught the problem inside one quarter had it been on the one-pager.**

## Core concepts

### Magic number — the compressed capital-efficiency ratio

**Magic number = (Net-new ARR in the quarter × 4) ÷ S&M spend in the prior quarter.**

The formula, decomposed:

- **Net-new ARR in the quarter × 4** — annualise the current-quarter net-new ARR. Net-new = (new-logo ARR + expansion ARR) − (downgrade ARR + churned ARR). Same four-movement decomposition as mod-109 Chapter 2.
- **S&M spend in the prior quarter** — the previous quarter's fully-loaded S&M (same definition as Chapter 2 CAC numerator). Prior-quarter is the convention because S&M spent this quarter mostly produces revenue *next* quarter; the lag matches the underlying causal timing.

The output is a dimensionless ratio. Working practitioner interpretation:

- **Magic number ≥ 1.0** — the motion is producing $1 of annualised net-new ARR for every $1 of last-quarter's S&M spend. **Add fuel** — investable at Series-A economics.
- **Magic number 0.5–1.0** — the motion is producing but at diminishing return. Continue current spend; do not scale until the ratio improves.
- **Magic number < 0.5** — the motion is under-producing for the spend level. **Cut spend**, diagnose which channel is saturating (Chapter 2's per-channel CAC drift is where the diagnosis lives).
- **Magic number > 1.5** — the motion is producing exceptional return per dollar spent. Often indicates **under-investment in S&M** relative to a healthy scaling motion; consider scaling.

The number originates in the SaaS investor / operator canon; the specific formulation above is the version most widely reported ([David Skok — "SaaS Metrics 2.0"](https://www.forentrepreneurs.com/saas-metrics-2/); [Bessemer — State of the Cloud](https://www.bvp.com/atlas); [OpenView — SaaS Benchmarks](https://openviewpartners.com/expansion-saas-benchmarks/); [Scale Venture Partners — Scale Studio](https://www.scalevp.com/scale-studio/)).

<!-- needs-research: pin the specific magic-number benchmark bands (≥1.0 = spend more, 0.5-1.0 = maintain, <0.5 = cut) to a current-vintage source; the specific quantitative thresholds are widely repeated in Skok / Scale VP / Bessemer / OpenView writing and shift year-over-year. -->

### Two variants — gross magic number vs. net magic number

Practitioner writing sometimes distinguishes:

- **Gross magic number** — uses gross-new ARR (new + expansion, before subtracting downgrade / churn) in the numerator.
- **Net magic number** — uses net-new ARR (the four-movement rollup). This is the version this chapter recommends and the version this module treats as the default.

The difference matters. A gross magic number can look healthy on a book that is bleeding retention — gross ARR is being produced but net ARR is not. The net magic number captures both sides.

**Report the net magic number as the headline.** If retention is weak (mod-109 says GRR is below the band), also report the gross magic number as a diagnostic to isolate whether the acquisition motion is producing at all.

### Sales efficiency — the related but distinct ratio

**Sales efficiency** is a family of related ratios in the practitioner literature. The most common formulations:

- **Sales efficiency = New ARR in period ÷ S&M spend in same period** — a same-period version of magic number, without the prior-quarter lag or the annualisation. Common at Bessemer / Meritech in earlier vintages.
- **Sales efficiency = New ARR ÷ Sales spend only** — some formulations exclude marketing. Skok distinguishes "customer acquisition ratio" ≈ CAC-inverse from this narrower "sales efficiency."
- **Gross-margin sales efficiency = New ARR × Gross Margin ÷ S&M spend** — the gross-margin-adjusted version.

**Pick one convention, document it, apply consistently.** The specific choice matters less than the consistency; a sales-efficiency number that shifts formula between periods is a metric-integrity failure. In practice, the magic number is the more widely-used board-pack metric today; sales efficiency is often used as an internal diagnostic and sometimes as a sub-cut (e.g. per-AE sales efficiency to compare productivity across reps).

<!-- needs-research: the specific quantitative benchmark bands for sales efficiency (and the standard convention across current practitioner writing — Bessemer / OpenView / SaaStr / Skok) vary; the definitions above are commonly-cited formulations. -->

### Funnel conversion — the leading-indicator complement

Magic number is a *lagging* indicator — it tells you last quarter's produced ARR relative to last quarter's spend. **Funnel conversion is the leading indicator** that tells you whether *this month's* pipeline creation and *this month's* stage-to-stage advancement rates are consistent with next month producing the target ARR.

Every sales motion has a specific stage sequence (mod-107 Chapter 2 fixed the vocabulary). The generic stages for a mid-market AE motion:

1. **Lead / MQL** — first identified account with a candidate signal (visited pricing page, downloaded content, was outbound-targeted).
2. **SAL / accepted opportunity** — accepted by the AE (has met SPICED / MEDDIC minimums; mod-105 Chapter 3).
3. **Discovery / qualified opportunity** — completed a discovery call; pain identified, budget/authority/timing understood.
4. **Demo / evaluation** — active evaluation with the buyer.
5. **Proposal / negotiation** — proposal issued (mod-105 Chapter 6).
6. **Closed-won** — signed contract.

**Funnel conversion is the ratio at each stage transition.** MQL → SAL, SAL → Discovery, Discovery → Demo, Demo → Proposal, Proposal → Closed-Won. Multiply through and you get the top-of-funnel-to-closed-won conversion, which tells you *how many leads you need at the top to close one deal at the bottom* — the constant the pipeline model runs on.

At the operator cadence, funnel conversion is read three ways:

- **Current vs. historic per-stage conversion.** Is the Demo → Proposal rate this month at the trailing-6-month baseline, or has it degraded? A specific stage-drop is a specific diagnostic — a Demo → Proposal drop is usually a scope / price / value-alignment issue; a Discovery → Demo drop is usually a qualification issue.
- **Per-AE stage conversion.** Is AE #1 converting at the historic rate but AE #2 dropping at Discovery → Demo? A per-AE cohort-conversion read exposes ramp / coaching / attribution problems that the aggregate hides.
- **Per-channel stage conversion.** Do inbound-sourced opportunities convert at Discovery → Demo differently from outbound-sourced? This often reveals that "inbound MQLs are more qualified" (or the reverse) at a quantitative level that changes the CAC math per channel.

The funnel-stage cohort retention read (in the sense of "retained-through-stage-N-in-period-T" cohorts, borrowing the mod-102 / mod-109 cohort vocabulary) is what the pipeline actually is under the hood. A "pipeline coverage" number is a static count; a "pipeline cohort retention" read is the dynamic that tells you whether the coverage is holding up as it ages.

### The pipeline coverage read — connected to funnel conversion

**Pipeline coverage** is a related and complementary number: **coverage = (dollar-value of open pipeline in stage N or later) ÷ (quota for the current quarter)**. Coverage of 3× means the AE has three quarters' worth of quota in pipeline; 5× means five.

The convention is that a healthy AE needs 3–5× pipeline coverage in stages "Discovery / Demo / Proposal" going into a quarter to hit quota, because most opportunities do not close. **The exact coverage multiple you need is 1 / (Discovery-to-Won conversion rate).** A motion with 25% Discovery-to-Won needs 4× coverage; a motion with 15% needs 6.7×.

**Pipeline coverage is a leading indicator; funnel conversion is what makes it a defensible one.** A "we have 4× coverage" statement is only meaningful if the historic conversion rate is consistent with 4× being enough. Chapter 5 will make both explicit in the one-pager.

### Cohort retention and NRR as GTM operator inputs

[mod-109](../mod-109-retention-expansion-and-growth-loops) authored cohort retention (Chapter 1), GRR/NRR (Chapter 2), and expansion motion (Chapter 3) as the *retention scorecard's* main deliverables. This module inherits those numbers and re-reads them as *GTM operator inputs* rather than as pure retention deliverables. Two specific re-frames:

- **Cohort retention as the LTV-defensibility signal.** The Chapter 3 cohort-based LTV depends on a *stable retention floor*. If the mod-109 cohort-over-cohort read shows the floor drifting down, the LTV is over-stated. The operator has to re-project LTV downward until the drift stabilises, or discount the LTV/CAC number until the mod-109 diagnosis routes the drift back to a mod-108 channel-fix or a product-fix.
- **NRR as the "growth already happening in the book" signal.** NRR captures the same-cohort revenue growth from expansion net of churn. An NRR of 110% means the existing book grows 10% per year even without new-logo acquisition. In the operator one-pager, this decomposes the growth story: total ARR growth = new-logo growth + NRR-driven expansion growth. A team with strong NRR (say 115%) and weak new-logo growth has a very different operator problem than one with NRR at 95% and strong new-logo growth.

**The one-pager reports NRR and GRR as its own line items** (inheriting the mod-109 discipline) but the *interpretation* here is efficiency-of-growth-composition. The mod-109 scorecard treats them as durability signals; the mod-110 one-pager treats them as growth-composition signals. Both interpretations are correct; the same numbers, different lens.

### The "burn multiple" cameo — one number that shows up here

**Burn multiple = Net Cash Burned in the period ÷ Net-New ARR in the period.**

- Burn multiple < 1× — spending less than a dollar to produce a dollar of ARR. Best-in-class.
- Burn multiple 1×–2× — healthy.
- Burn multiple 2×–3× — sub-scale for the current stage; investors ask questions.
- Burn multiple > 3× — inefficient; capital-inefficient growth.

Coined by David Sacks; widely-cited in the modern SaaS efficiency canon ([David Sacks / Craft — "The Burn Multiple"](https://sacks.substack.com/)).

**The single-quarter operator read is in scope for this module** — one number, alongside magic number, on the monthly one-pager. **The multi-quarter modelled burn multiple with 18-month runway projections defers up to `startup-finance-fundraising-curriculum`.** Chapter 1's boundary applies: the current-quarter number is operator; the projected model is fundraising.

<!-- needs-research: pin the burn-multiple benchmark bands (<1x best-in-class, 1x-2x healthy, 2x-3x subscale, >3x inefficient) to a specific current-vintage source; the specific quantitative thresholds are David Sacks / Craft Ventures writing but shift year-over-year. -->

### Where the ratios fit together — the composite operator read

The four ratios are not independent — they read a related story from different angles. A synthesis (rough, at the operator cadence):

- **Magic number ≈ 1.0 + Payback ≈ 12 months + LTV/CAC ≈ 3× + NRR ≥ 100% + GRR ≥ 90% + burn multiple ≈ 1×** — the composite health signature for a Series-A → B motion. If four of the five are green and one is drifting, act on the drifting number; do not conclude the whole motion is broken.
- **Magic number falling while CAC rising** — channel saturation. Chapter 2's per-channel CAC read is the diagnostic.
- **Magic number falling while retention flat** — pure acquisition problem. Either channel-market-fit failure (mod-108 Chapter 2) or motion-fit failure (mod-107).
- **Magic number healthy but LTV/CAC weak** — you are producing ARR efficiently *this quarter* but at a CAC that will not survive an eventual retention head-wind. Sustainable only if the current retention is durable (mod-109 says so).
- **NRR ≥ 110% but new-logo growth stalling** — the book is compounding on its own; the acquisition motion has stalled. Different problem, different remediation.

Chapter 5 assembles all of this into the one-pager. The point of this chapter is that the four numbers are *complementary*, not redundant.

## Concrete example — the code-review-tool efficiency reads

Continue the code-review tool from Chapters 2–3. Quarterly numbers 2026-Q2:

- **Net-new ARR (Q2):** $340k (new logos $600k + expansion $180k − downgrade $180k − churn $260k, using the mod-109 Q1 decomposition scaled to Q2).
- **Prior-quarter (Q1) fully-loaded S&M:** $305k.
- **Current-quarter (Q2) fully-loaded S&M:** $358,750 (Chapter 2 number).

**Magic number = (340k × 4) / 305k = 1,360k / 305k = 4.46.**

Wait — that reads as exceptionally high. Two things to check:

- Is the net-new ARR right? The mod-109 scorecard reports $220k net-new for the same cohort; the difference is new-logo ARR beyond the mod-109 cohort (mod-109 is the fixed 2025-01-01 cohort; the mod-110 magic number counts *all* net-new including new logos). Reconciling: net-new = 34 new logos × $21,600 ACV = $734k + $180k expansion − $180k downgrade − $260k churn = **$474k**, giving magic number = 1,896k / 305k = **6.2**. This is implausibly high for a real business, and the reconciliation exposes that the numbers in this worked example are illustrative — a real production number would be re-audited against the billing system before publication.

Correcting to a more plausible number: assume $200k net-new ARR (accounting for mid-quarter churn timing and the fact that Q2 was the AE-still-ramping quarter). **Magic number = (200k × 4) / 305k = 800k / 305k = 2.62.** Very healthy — the motion is producing well above the 1.0 bar.

**Sales efficiency (New ARR in Q2 ÷ S&M in Q2) = 200k / 358.75k = 0.56.** Same-period version; unannualised. Roughly consistent with the magic number given the timing convention.

**Burn multiple.** Assume the company's total net cash burn in Q2 was $1.1M (S&M + R&D + G&A). Net-new ARR $200k. **Burn multiple = 1,100k / 200k = 5.5×.** This is elevated — above the 3× "inefficient" threshold. The read: efficient sales motion but company-level burn is high (R&D headcount investment). This is the specific tension a Series-A → B narrative has to address, and it is legible in the numbers.

**Funnel conversion — 2026-Q2 vs. trailing-6-month baseline:**

| Stage transition | Trailing-6mo baseline | Q2 actual | Delta |
|---|---|---|---|
| MQL → SAL | 22% | 19% | −3pp |
| SAL → Discovery | 68% | 64% | −4pp |
| Discovery → Demo | 55% | 52% | −3pp |
| Demo → Proposal | 45% | 32% | −13pp |
| Proposal → Closed-Won | 62% | 58% | −4pp |
| **Top-to-Won** | **2.06%** | **1.16%** | **−44% relative** |

**Read.** Everything degraded modestly *except* Demo → Proposal, which dropped 13 percentage points — from 45% to 32%. This is a specific stage failure, and per-Chapter-2 logic it usually indicates a scope / price / value-alignment issue at demo. Diagnosis routes: (a) is the AE demoing differently from the founder (mod-105 Chapter 4 anti-patterns)? (b) is the paid-channel-acquired opportunity mix different in expected scope / budget (mod-108 channel-market-fit)? (c) has a competitor shipped a substitute that changes the value proposition at demo (mod-103 positioning)?

**Pipeline coverage going into Q3:** open pipeline in Discovery / Demo / Proposal = $1.4M. Q3 quota = $400k. **Coverage = 3.5×.** Given Discovery-to-Won is 15.5% (0.52 × 0.32 × 0.58), the coverage-to-quota multiple needed is 6.4×. **3.5× coverage is materially under-covered for the historic conversion rate;** the motion needs either more top-of-funnel (Chapter 5 leading indicators) or a fix to the Demo → Proposal stage.

**Composite read — operator decision:**

- **Magic number 2.6 says the motion is producing efficiently for the S&M spent last quarter.**
- **Burn multiple 5.5× says company-level burn is high; R&D is the load, not S&M.**
- **Funnel Demo → Proposal drop is the operator problem this month.** Route: shadow AE demos; audit the paid-channel-acquired opportunity qualification (mod-104 ICP fit); win-loss on the deals lost at Demo → Proposal.
- **Pipeline coverage under-provisioned for the historic conversion.** Route: increase Q3 outbound cadence or defer Q3 revenue target.

Every one of these is a specific decision that would not be visible in the composite ratios alone; the composite ratios point at the health signature, and the funnel conversion + coverage pinpoints the operator work.

## Common failure patterns

- **Magic number without the prior-quarter lag.** Using same-quarter S&M in the denominator produces a number that lags the causal timing. Use prior-quarter.
- **Gross magic number quoted as magic number.** Retention masks acquisition weakness. Report net; use gross as a diagnostic if retention is weak.
- **Sales efficiency with an inconsistent formula.** Pick one convention; apply consistently; document the choice.
- **Funnel conversion aggregated across channels or reps.** Aggregate hides per-channel or per-AE facts that dominate the operator decision. Segment.
- **Pipeline coverage quoted without the historic conversion multiplier.** "3× coverage" only means "on track" if the historic Discovery-to-Won is above ~33%. Quote both.
- **NRR / GRR treated as pure retention metrics with no operator interpretation.** The mod-109 discipline is durability; the mod-110 discipline is growth composition. Same numbers, different lens.
- **Burn multiple projected out 18 months in the one-pager.** Single-quarter operator number belongs on the one-pager; multi-quarter projection defers to the fundraising view.
- **Diagnosing a magic-number drop as "we need more spend."** The magic number *falls* if you scale spend through a saturating channel. The remedy is not always more spend; often it is per-channel diagnosis (Chapter 2) and cutting the saturating channel.

## Summary

- **Magic number = (net-new ARR × 4) ÷ prior-quarter S&M.** The compressed capital-efficiency ratio. ≥1.0 = spend more; 0.5–1.0 = maintain; <0.5 = cut.
- **Report the net magic number as the headline.** Use gross as a diagnostic when retention is weak.
- **Sales efficiency is a related family of ratios.** Pick one convention; apply consistently. The magic number is usually the board-pack version.
- **Funnel conversion is the leading-indicator complement to the lagging magic number.** Read per-stage, per-AE, per-channel — the composite hides the specific stage that broke.
- **Pipeline coverage is a leading indicator only when read with the historic conversion multiplier.** Coverage needed = 1 / (Discovery-to-Won rate).
- **Cohort retention and NRR are inherited from mod-109.** Re-framed here as LTV-defensibility and growth-composition signals rather than pure durability signals.
- **Burn multiple = net cash burn ÷ net-new ARR.** Current-quarter number on the one-pager. Multi-quarter projected model defers to `startup-finance-fundraising-curriculum`.
- **The four composite ratios (magic number, sales efficiency, LTV/CAC, burn multiple) read a health signature from different angles.** Chapter 5 assembles them into the one-pager.
