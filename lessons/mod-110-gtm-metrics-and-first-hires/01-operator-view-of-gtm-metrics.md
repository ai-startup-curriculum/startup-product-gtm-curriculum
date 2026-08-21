# The Operator View of GTM Metrics

## Motivation

By the time a founder reaches this module the numbers are already piling up. CAC, LTV, payback, magic number, sales efficiency, funnel conversion, cohort retention, NRR, GRR, burn multiple, ARR, growth rate, quick ratio — each with three or four common definitions, each with a benchmark quoted from a different report on a different vintage. It is easy to end up with a spreadsheet full of numbers that nobody can defend, and a founder who can quote the numbers to a board but cannot use them on Monday morning to decide anything.

This module opens by naming the distinction that lets the rest of the module stay small. There are two very different reads of the same GTM numbers:

- **The operator view.** The founder / GTM lead reads these numbers on a weekly and monthly cadence to *run the business* — decide what to invest in next week, which channel to defund, whether the funnel is loading, whether the AE is on ramp, whether it is time to make the next hire. The reads are current-week or last-month; the decisions are same-week or same-month; the audience is internal.
- **The fundraising / capital-allocation view.** The same underlying data, modelled as multi-year projections for a fundraise, with LTV discount-rate math, CAC-payback sensitivity analysis under multiple scenarios, and a narrative that packages the numbers for a Series-A / Series-B partner. The reads are quarterly or annually; the decisions are 12-to-24-month resource-allocation; the audience is external (investors, board).

**This module owns the operator view. The fundraising / capital-allocation view defers up to [`startup-finance-fundraising-curriculum`](https://github.com/ai-startup-curriculum/startup-finance-fundraising-curriculum).** Both are load-bearing at different times; conflating them is the specific mistake that produces the "board deck full of numbers the founder cannot defend on Monday morning" pathology.

This chapter fixes that boundary, lays out the four operating cadences the numbers get read on, and enumerates the specific set of numbers the module will teach in the following chapters — with a one-line justification of why each is in scope.

## Core concepts

### The operator view — three questions the numbers must answer

At the SERIES-A boundary the founder is asking three questions of the GTM numbers every week and every month. Not five, not ten. Three.

- **Is the motion working?** Is the funnel loading enough opportunities? Are the opportunities converting at the historic conversion rate? Is the AE on ramp? Is the paid channel producing at plan? Is retention holding?
- **Is the motion efficient?** Is each dollar of S&M spend producing enough net-new ARR? Is CAC in a payback band the business can sustain? Is LTV/CAC above the bar an outside investor will read as investable?
- **Is the motion ready to scale?** Is the founder still the bottleneck on close, on demo, on onboarding? Are the pre-conditions for the first (or next) GTM hire in place? Which specific number, if it moved, would trigger the next hire?

Every number this module teaches is instrumented against one of these three questions. If a number does not answer one of the three at the operator cadence, it defers up to the fundraising view. The three questions are the filter that keeps the operator dashboard small.

### The operating cadences — Monday, month-end, quarter-end, fundraise

The same underlying data gets read at four cadences. The reads are different; the audiences are different; the decisions are different.

- **Monday morning (weekly).** Activity, pipeline, and short-cycle conversion. The founder or GTM lead reads a **weekly one-pager** — new opportunities created last week, meetings held, proposals sent, closed-won, closed-lost, current-week forecast committed vs. best-case, per-AE pipeline coverage. Every number is a *leading indicator* — activity and pipeline creation this week is next month's revenue. Chapter 5 authors the weekly one-pager.
- **Month-end (monthly).** Revenue, retention, CAC, payback, sales efficiency. The founder reads a **monthly one-pager** — MRR / ARR closed and net-new, per-segment retention, per-channel CAC, blended CAC, payback, magic number, sales efficiency. Every number is a *lagging indicator* — it describes what happened, not what is loading. Chapter 5 authors the monthly one-pager.
- **Quarter-end (board pack).** The monthly one-pager assembled into a quarterly view with the trailing-3-month trend, the year-over-year comparison, the benchmark call-out, and one paragraph of narrative for each of the three operator questions. The audience is the board and (implicitly) any incoming Series-B partner. Chapter 7 assembles the board-pack GTM section.
- **Fundraise (Series-A / Series-B pitch).** The same numbers modelled forward as multi-year projections, with the LTV discount-rate math, the CAC-payback sensitivity analysis under multiple scenarios, and the narrative that packages the numbers for the target investor. **This is out of scope for the module.** The fundraising treatment defers up to `startup-finance-fundraising-curriculum`.

The four cadences build on each other. A weekly one-pager that has been maintained honestly for six months produces a monthly one-pager for free; six monthly one-pagers produce a quarterly board pack for free; four quarterly board packs produce a fundraise data room for free. **The failure mode is not "we lack the fundraising model"; it is "we skipped the weekly one-pager and are trying to reconstruct twelve months of data three days before the pitch."**

### The specific numbers in scope

The following numbers are what "GTM operator metrics" means at the SERIES-A boundary in the modern SaaS canon. Each is treated in one of the next four chapters.

- **CAC — Customer Acquisition Cost.** Fully-loaded (all S&M spend, not just paid media) and per-channel (never blended across founder-outbound and paid). Chapter 2.
- **LTV — Lifetime Value.** Cohort-based on the retention floor from [mod-109](../mod-109-retention-expansion-and-growth-loops), not the blended-ARR shortcut. Gross-margin adjusted. Chapter 3.
- **Payback period.** Months to recover CAC at gross-margin dollars. The single most operator-relevant efficiency number at the working cadence. Chapter 3.
- **LTV / CAC ratio.** The composite the Series-B underwriter reads first. Chapter 3.
- **Magic number.** Net-new ARR ÷ prior-quarter S&M spend. The capital-efficiency number that translates directly to "should we spend more?" Chapter 4.
- **Sales efficiency.** Closely related to magic number; several definitions in the practitioner literature; Chapter 4 fixes one.
- **Funnel conversion.** Stage-by-stage conversion rates through the pipeline the mod-107 motion produces — with the stage-cohort-retention read that lets you see whether the motion is working. Chapter 4.
- **Cohort retention.** The mod-109 durability instrument, re-read as an operator input rather than a durability signal. Chapter 4 references and re-frames.
- **NRR.** The mod-109 revenue-level durability roll-up, re-read at the operator cadence. Chapter 4 references and re-frames.

Deliberately **out of scope** for this module (and named here so the reader does not go looking):

- **CAC discount-rate LTV models.** Multi-year DCF-style LTV with cost-of-capital adjustments. Defers up to `startup-finance-fundraising-curriculum`.
- **Cohort-financial-modelling under multiple scenarios.** Base / bear / bull projections. Defers up.
- **Burn multiple as a modelled scenario over 18 months.** The single-quarter operator read is here (Chapter 4 briefly); the multi-scenario modelled read defers up.
- **Sales-team comp mechanics.** Quota construction, on-target-earnings design, spiff programmes, ramp models — the *hiring / comp / IC-plan* depth defers sideways to `startup-operations-governance-curriculum`. This module owns the *staging* (which hire when).
- **Product analytics (Amplitude / Mixpanel / Heap) configuration depth.** Defers sideways to `cpo-curriculum`.

### Why "operator view" is a discipline, not a shortcut

It is tempting to read "the operator view" as the beginner version of the fundraising view — the numbers the founder does in her head before the CFO does them properly for the pitch. It is not. The operator view is a **specific discipline** with its own failure modes, its own cadence, and its own bar for defensibility.

- **The bar for the operator view is same-week decision usefulness.** A number that cannot inform a decision this week is not an operator number. It is a fundraising number that got included in the weekly by mistake.
- **The bar for the operator view is per-segment, per-channel decomposition.** A blended, aggregate number is not operator-relevant even if it is directionally correct; the operator needs to know which channel to defund and which segment is drifting.
- **The bar for the operator view is honest, not flattering.** A monthly one-pager that presents the strongest cohort's NRR as the headline hides the operating decisions the weakest cohort demands. This is Chapter 5's discipline in detail.
- **The bar for the operator view is defensible against a hostile question.** "Where did that CAC number come from?" must have a same-day answer sourced from the actual system of record (Stripe, HubSpot, Salesforce, the ad platforms) — not an assertion from memory.

The fundraising view can be lossy about any of these; the operator view cannot. This is why the founder who runs a strong weekly / monthly one-pager for a year has a much easier fundraise than the founder who tried to construct one from memory in the week before the pitch. The operator discipline is what makes the fundraising view legible.

### The relationship to the mod-102 / mod-109 scorecards

This module's GTM one-pager is not a replacement for the [mod-102 PMF scorecard](../mod-102-pmf-signal-and-measurement/) or the [mod-109 retention + expansion scorecard](../mod-109-retention-expansion-and-growth-loops/). It is a third artifact that assumes both.

- The **mod-102 PMF scorecard** tells you whether PMF is real in the ICP segment, and is authored on a quarterly cadence.
- The **mod-109 retention + expansion scorecard** tells you whether that PMF is *durable*, and is authored on a monthly cadence.
- The **mod-110 GTM one-pager** tells you whether the acquisition / conversion / retention motion, taken together, is *investable at Series-A / Series-B economics*, and is authored on a weekly (activity) and monthly (efficiency) cadence.

`project-103-pmf-and-retention-scorecard` packages all three into one integrated set of anchor artifacts. The three answer complementary questions; skipping any one of them leaves a gap the underwriter will find.

### The boundary named explicitly — five things that defer up

Read this list. If any of the following shows up in your weekly / monthly one-pager, you have leaked the fundraising view into the operator view and you need to move it out.

- **A multi-year LTV under a discount rate.** The operator LTV is a cohort read against the current retention floor, gross-margin adjusted. The DCF-style multi-year LTV is a fundraise-model artifact.
- **A payback sensitivity analysis under three CAC scenarios.** The operator payback is one number, the current one, benchmarked. The scenario analysis is a fundraise-model artifact.
- **A burn multiple with a projected 18-month runway model.** The operator burn multiple is the current quarter's number, read against the current runway. The projected runway model is a fundraise-model artifact.
- **A public-comparables valuation-multiple mapping.** Operator numbers do not compare to Snowflake's revenue multiples. Fundraise decks sometimes do.
- **A "Rule of 40" score.** This is a legitimate SaaS metric, but at the operator cadence it is a lagging composite of two numbers (growth + margin) both of which are already in the monthly one-pager. It belongs in the board pack or fundraise; it does not add operator signal.

Each of these is a good and useful artifact at the appropriate cadence. Each is a distraction at the operator cadence. Chapter 5 enforces this in the one-pager template.

## Concrete example — the code-review-tool operator dashboard

Return to the mid-market code-review tool from [mod-109](../mod-109-retention-expansion-and-growth-loops). The team has closed a $6M Series-A on the strength of the mid-market outbound cohort, is now 18 months in, and has three GTM channels operating (founder outbound, first AE outbound, paid LinkedIn), one paid content programme, and a Head of CS running the expansion motion.

**Before this module, the founder's "dashboard" is a Slack channel `#numbers` where various people post various things.**

The founder posts CAC once a month, computed as "everything we spent on marketing and sales divided by number of new logos." The Head of CS posts NRR once a quarter. The first AE posts closed-won weekly. The board deck once a quarter has a slide titled "Metrics" with seven numbers on it, three of which were computed differently from last quarter and nobody remembers why.

**After this module, the founder maintains two artifacts on two cadences.**

- The **weekly one-pager** (published every Monday): last-week meetings held per rep, opportunities created per channel, opportunities advanced by stage, proposals sent, closed-won and closed-lost with reasons, current-quarter forecast committed vs. best-case, per-AE pipeline coverage. Reads in five minutes. Answers "is the motion working this week?"
- The **monthly one-pager** (published on the 3rd of each month for the prior month): closed MRR/ARR, net-new MRR/ARR, per-channel CAC (fully-loaded), blended CAC, per-segment cohort retention W12 delta vs. prior month, GRR, NRR, LTV, LTV/CAC, payback period, magic number, sales efficiency, funnel-stage conversion rates. Each with the benchmark band call-out. Reads in ten minutes. Answers "is the motion efficient? Is the motion ready to scale?"

**The board pack (quarterly) is the monthly one-pager assembled into a trailing-3-month view with year-over-year comparison and one paragraph per operator-question narrative.** No new data collection. No new numbers.

**The Series-A pitch that raised the $6M was not built from any of these.** It was built by the founder and a hired CFO consultant, over three months, using the operator dashboard as raw input and the deep DCF-style LTV / CAC-payback-sensitivity / burn-multiple-projection modelling from the CFO. That work — the fundraising view — defers up to `startup-finance-fundraising-curriculum`.

The point of the boundary is that the operator dashboard is what the founder maintains continuously; the fundraise model is what a specialist builds every 18–24 months on top of it. Both are load-bearing at their appropriate cadence. Neither substitutes for the other.

## Common failure patterns

- **Twenty numbers on the dashboard.** If it is not one of the numbers in the "in scope" list above, and it does not answer one of the three operator questions, it does not go on the operator dashboard.
- **A single "SaaS benchmarks" page in the appendix.** The benchmarks are per-ARR-band and per-motion-type. A single benchmark applied to every number produces a misleading verdict on at least half of them.
- **Blended CAC as the headline CAC.** The blended CAC of a business with three channels averaging out to $9k tells you nothing about which channel to defund. Chapter 2's whole point.
- **Blended-ARR-divided-by-blended-churn LTV.** The number is easy to compute and quantitatively wrong at the operator cadence. Chapter 3's whole point.
- **"NRR is 115%" as the headline retention number without GRR.** [mod-109 Chapter 2](../mod-109-retention-expansion-and-growth-loops/02-grr-vs-nrr.md) said this already; if the mod-109 scorecard is honest, the mod-110 one-pager stays honest by inheritance.
- **Board pack numbers not reconcilable to the operator dashboard.** A quarterly "CAC = $6,400" that cannot be reconstructed from three months of the weekly / monthly one-pager is a metric-integrity failure. The board will read it as such if they look.
- **Leaking the fundraising view into the operator view.** Multi-year LTV, payback sensitivity analysis, projected 18-month runway modelling — all belong in the fundraising view. Chapter 5 will enforce this in the one-pager template.
- **Skipping the weekly cadence "because we're too small."** The weekly one-pager is 20 minutes of the founder's time per week and is the specific instrument that catches the funnel loading problem early. Skipping it is why founders discover in month 5 that the funnel dried up in month 2.

## Summary

- **The module owns the operator view of GTM metrics.** The fundraising / capital-allocation deep view defers up to `startup-finance-fundraising-curriculum`.
- **The operator view answers three questions weekly and monthly.** Is the motion working? Is the motion efficient? Is the motion ready to scale?
- **Four cadences on the same data.** Weekly (activity, leading), monthly (efficiency, lagging), quarterly (board pack, trend), fundraise (multi-year model, out of scope).
- **The specific numbers in scope.** CAC (Chapter 2), LTV / payback / LTV/CAC (Chapter 3), magic number / sales efficiency / funnel conversion / cohort retention / NRR (Chapter 4). Everything else defers up or sideways.
- **The operator view is a discipline, not a shortcut.** Same-week decision usefulness, per-segment / per-channel decomposition, honest not flattering, defensible against a hostile question.
- **The GTM one-pager assumes the mod-102 PMF scorecard and the mod-109 retention scorecard.** All three answer complementary questions; `project-103` packages the set.
- **Five things that defer up.** Multi-year LTV under discount rate, payback sensitivity analysis, projected 18-month runway modelling, public-comparables valuation mapping, Rule-of-40 composite. Each is legitimate at its own cadence; each is a distraction at the operator cadence.
