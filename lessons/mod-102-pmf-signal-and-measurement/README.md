# mod-102 — PMF Signal and Measurement

**Stage:** PRE-SEED
**Pillar:** GTM
**Hours:** 20 (7 lecture chapters + 5 exercises + 1 lab)
**Track:** [Startup Product & GTM](../../CURRICULUM.md)

> *Retention curves that flatten, not launch spikes that decay.*

## What this module trains

Distinguish **anecdotal traction** — one loud customer, a launch spike, a design-partner deal, a viral tweet — from **product-market fit** — retention curves that flatten and pull-based demand. Run the **Sean Ellis "very disappointed"** survey properly against active users, read cohort retention curves as the primary durability signal, and reproduce the **Superhuman iteration engine** as a PMF *engine* rather than a one-shot measurement. Diagnose the **four PMF failure modes** — wrong market, wrong product, wrong distribution, wrong price — and route each to the right downstream module.

The failure mode this module exists to catch: **the founder points at one enthusiastic customer, one launch-week signup spike, or one viral tweet and declares PMF; the retention curve is flat at 15% by week 4; nine months later the market has moved on and the team is out of runway.**

## Learning objectives

- Distinguish anecdotal traction from product-market fit — one loud customer, a launch spike, a design-partner deal, or a viral tweet is not PMF; retention curves that flatten and pull-based demand are.
- Run the Sean Ellis "how would you feel if you could no longer use this product?" survey properly — sample selection (active users only, not all signups), the 40% "very disappointed" threshold as a working PMF signal, and the sub-40% diagnostic questions (who is it for, what is the main benefit, what to improve).
- Read a retention curve — daily / weekly / monthly cohort retention, flattening as the PMF signature, the smiling / frowning curve interpretation — and know why a leaky curve is a PMF failure, not a marketing failure.
- Reproduce the Superhuman iteration engine — cohort the 40% "very disappointed" users, identify the main benefit they cite, harden that benefit, address the "somewhat disappointed" cohort's top blockers, re-run the survey — and use it as a PMF *engine*, not a one-shot measurement.
- Diagnose the four PMF failure modes — wrong market (no one wants it), wrong product (they want it but not this), wrong distribution (they want it but never see it), wrong price (they want it but can't afford it) — and route each to the right module downstream.
- Ship a PMF scorecard for a real (or hypothetical) startup — retention curve, Sean Ellis result, main-benefit statement, top blocker cohort, one hypothesis for the next iteration.

## Chapters

Read in order. Each chapter is focused enough to sit in one working session; together they walk the module's operating model end-to-end.

| # | Chapter | Objective |
|---|---|---|
| 1 | [What Product-Market Fit Means](01-what-pmf-means.md) | Andreessen / Rachleff vocabulary; PMF as a strong-pull system state, not a milestone |
| 2 | [Anecdotal Traction vs. Product-Market Fit](02-anecdotal-traction-vs-pmf.md) | Launch spikes, loud customers, viral tweets, design-partner LOIs — what each is and is not evidence of |
| 3 | [The Sean Ellis Survey — Run It Properly](03-sean-ellis-survey.md) | Sample selection, the 40% threshold, the four diagnostic questions, common misreads |
| 4 | [Reading a Cohort Retention Curve](04-retention-curves.md) | DAU / WAU / MAU cohort curves, the flattening signature, smile vs. frown interpretation |
| 5 | [The Superhuman Iteration Engine](05-superhuman-iteration-engine.md) | Rahul Vohra's engine — cohort the very-disappointed, harden the main benefit, unblock the somewhat-disappointed, re-run |
| 6 | [The Four PMF Failure Modes](06-four-pmf-failure-modes.md) | Wrong market / wrong product / wrong distribution / wrong price — how to tell them apart and route to the right module |
| 7 | [Shipping the PMF Scorecard](07-pmf-scorecard.md) | The one-page scorecard; the falsifiable next-iteration hypothesis; how the scorecard feeds mod-103 / 104 / 106 / 108 / 109 |

## Exercises

Sequenced to build the PMF scorecard from raw diagnostic through iteration engine. Solutions are authored in the paired solutions repo and are not part of this file set.

| # | Exercise | Hours | Depends on |
|---|---|---|---|
| 1 | [PMF vs. traction diagnostic](exercises/exercise-01-pmf-vs-traction-diagnostic.md) | 2 | Chapters 1, 2 |
| 2 | [Sean Ellis survey authoring](exercises/exercise-02-sean-ellis-survey-authoring.md) | 2 | Chapter 3 |
| 3 | [Retention curve read and critique](exercises/exercise-03-retention-curve-read-and-critique.md) | 3 | Chapter 4 |
| 4 | [Superhuman iteration engine drill](exercises/exercise-04-superhuman-iteration-engine-drill.md) | 4 | Exercises 2, 3; Chapter 5 |
| 5 | [Four-failure-mode teardown](exercises/exercise-05-four-failure-mode-teardown.md) | 3 | Exercises 2, 3; Chapter 6 |

## Lab

The module's ship deliverable — **publish a PMF scorecard for one startup** — packages the Sean Ellis result, the cohort retention read, the main-benefit statement, the top blocker cohort, and one falsifiable hypothesis for the next iteration into the Chapter 7 one-page format. The lab picks up from Exercises 04 and 05. See [`.aicg/curriculum-plan.json`](../../.aicg/curriculum-plan.json) for the lab spec (`lab-01-publish-a-pmf-scorecard-for-one-startup`, 6h). The lab is authored in a follow-on content cycle and is not in this file set.

## Quiz

One quiz covers the module. See [`.aicg/curriculum-plan.json`](../../.aicg/curriculum-plan.json). Authored in a follow-on content cycle.

## Resources

See [`resources.md`](resources.md) for the citable references this module is grounded in — Andreessen, Rachleff, Ellis, Vohra, Balfour, and the retention / cohort-analytics canon.

## How this module connects to the rest of the track

- **Fed by ← [mod-101](../mod-101-customer-discovery-and-problem-validation)** — the three testable hypotheses in the discovery report become the input to this module's PMF instruments. Without a discovery report, the Sean Ellis "who is this for" and "main benefit" diagnostics have nothing to compare against.
- **Feeds → [mod-103](../mod-103-positioning-and-messaging)** — the **main-benefit statement** from the very-disappointed cohort is the raw material for the Dunford value / best-for-characteristics components; positioning that ignores the surveyed main benefit is founder invention.
- **Feeds → [mod-104](../mod-104-icp-and-buyer-personas)** — the **who-is-this-for** answer from the very-disappointed cohort sharpens the firmographic + behavioural ICP; disqualifiers from the "not disappointed" cohort feed the ICP disqualification checklist.
- **Feeds → [mod-106](../mod-106-pricing-and-packaging)** — a "wrong price" PMF diagnosis routes directly into Van Westendorp / Gabor-Granger work; a scorecard that shows willingness-to-pay collapse but strong retention is a pricing problem, not a product problem.
- **Feeds → [mod-108](../mod-108-demand-generation-and-channels)** — a "wrong distribution" diagnosis routes to channel-market-fit work; retention proves the product works and the failure is at the top of the funnel.
- **Feeds → [mod-109](../mod-109-retention-expansion-and-growth-loops)** — cohort retention reading is deepened here into NRR / GRR / growth-loops after PMF holds; this module teaches the *diagnostic* read, mod-109 teaches the *durability* read.
- **Feeds → [`project-103-pmf-and-retention-scorecard`](../../projects/project-103-pmf-and-retention-scorecard)** — the module's scorecard is the seed artifact for the project.

## Prerequisites and out-of-scope references

- **Prerequisite:** [mod-101](../mod-101-customer-discovery-and-problem-validation) — the discovery corpus, JTBD outcomes, and the three testable hypotheses that the PMF instruments in this module are designed to falsify.
- **Prerequisite (implicit):** [`startup-foundations`](https://github.com/ai-startup-curriculum/startup-foundations) (level 10) — the startup-as-a-search-for-a-business-model mental model, the founder-numbers slice (runway, burn, growth read), and the default-alive / default-dead framing. Never re-taught here.
- **Not in scope, linked out:** deep growth-loops, NRR / GRR benchmarking, and expansion-motion design belong to [mod-109](../mod-109-retention-expansion-and-growth-loops); cohort financial modelling / LTV discount-rate math defers up to [`startup-finance-fundraising-curriculum`](https://github.com/ai-startup-curriculum/startup-finance-fundraising-curriculum); product-analytics tooling depth (Amplitude / Mixpanel / Heap configuration) defers sideways to [`cpo-curriculum`](https://github.com/ai-startup-curriculum/cpo-curriculum).

---

*Return to [track overview](../../CURRICULUM.md) or [track README](../../README.md).*
