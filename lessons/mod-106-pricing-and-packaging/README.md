# mod-106 — Pricing and Packaging

**Stage:** SEED
**Pillar:** GTM
**Hours:** 22 (6 lecture chapters + 6 exercises + 1 lab)
**Track:** [Startup Product & GTM](../../CURRICULUM.md)

> *The metric is the strategy. The number tests.*

## What this module trains

Author a defensible pricing pack — one primary pricing **metric**, three **tiers**, one **anchor price** per tier, one **supported experiment** for the next quarter — starting from **willingness-to-pay research** (Van Westendorp, Gabor-Granger, Max-Diff), anchored to a **value derivation** against the buyer's economic outcome, packaged in a **good / better / best** structure with an anchor tier, a hidden premium tier, and a stripped anchor, and evolved through **cohort-tracked price experiments** with pre-committed guardrails and an explicit grandfathering policy.

The failure mode the module exists to catch: **the founder either picks a price by intuition ("$99 sounds right"), by cost-plus markup, or by competitor-sticker copy — locking in an unowned number that leaks ARPU quarter after quarter — or she runs pricing "experiments" as guerrilla changes without cohort tracking, without guardrails, and without a policy for existing customers, producing revenue movement that is un-decodable and grandfathering chaos that costs the finance team quarters of reconciliation.**

## Learning objectives

- Run willingness-to-pay research — Van Westendorp price-sensitivity meter, Gabor-Granger, and Max-Diff feature preference — and know the trade-offs (what each measures, sample-size requirements, common misreads).
- Design value-based pricing anchored to the buyer's economic outcome (ROI, hours saved, seats replaced), not cost-plus markup or competitor sticker.
- Design good / better / best packaging — three tiers with an **anchor tier** (the one buyers should pick), a **hidden premium tier** (raises the ceiling), and a **stripped anchor** (protects the middle from a price war).
- Distinguish **pricing metric** (per seat / transaction / GB / message / workflow-run — the strategic choice) from **price point** (the number attached to it — the test).
- Run price experiments at startup scale — first-conversation pricing, plan-tier switches, geographical / segment variants, grandfathering policies — and know why cohort-level tracking beats snapshot ARR after a price change.
- Ship a pricing + packaging pack — one primary metric, three tiers, one anchor price per tier, one supported experiment for the next quarter.
- Recognise the boundary — GTM depth on pricing lives here; deep unit-economics modelling that feeds fundraising financials defers up to [`startup-finance-fundraising-curriculum`](https://github.com/ai-startup-curriculum/startup-finance-fundraising-curriculum).

## Chapters

Read the chapters in order. Each one is focused enough for a single sitting; together they walk the derivation-and-shipping motion end-to-end.

| # | Chapter | Objective |
|---|---|---|
| 1 | [Willingness-to-Pay Research](01-willingness-to-pay-research.md) | Van Westendorp PSM, Gabor-Granger, Max-Diff — trade-offs, sample-size discipline, common misreads |
| 2 | [Value-Based Pricing](02-value-based-pricing.md) | Value equation from the buyer's economic outcome; 10-25% capture ratio; five-step derivation |
| 3 | [Good / Better / Best Packaging](03-good-better-best-packaging.md) | Three-tier structure; anchor / ceiling raiser / stripped protector; tier-composition worksheet |
| 4 | [Pricing Metric vs. Price Point](04-pricing-metric-vs-price-point.md) | Four metric families (seat / usage / outcome / hybrid); four-alignment-test worksheet |
| 5 | [Price Experiments and Grandfathering](05-price-experiments-and-grandfathering.md) | Four experiment types; cohort-level tracking; guardrails; grandfathering policies |
| 6 | [Shipping the Pricing Pack](06-shipping-the-pricing-pack.md) | Seven required sections; one-page summary; operating cadence; three-audience test |

## Exercises

Sequenced to build the pack from raw research to shippable artifact. Solutions are authored in the paired solutions repo and are not part of this file set.

| # | Exercise | Hours | Depends on |
|---|---|---|---|
| 1 | [Van Westendorp + Gabor-Granger drill](exercises/exercise-01-van-westendorp-and-gabor-granger-drill.md) | 3 | Chapter 1 |
| 2 | [Value-based pricing derivation](exercises/exercise-02-value-based-pricing-derivation.md) | 3 | Chapter 2; mod-104 personas |
| 3 | [Good / better / best packaging authoring](exercises/exercise-03-good-better-best-packaging-authoring.md) | 3 | Chapters 2, 3 |
| 4 | [Pricing metric vs. price point drill](exercises/exercise-04-pricing-metric-vs-price-point-drill.md) | 2 | Chapters 2, 4 |
| 5 | [Price experiment design + guardrails](exercises/exercise-05-price-experiment-design-and-guardrails.md) | 3 | Chapter 5; Exercises 2, 3 |
| 6 | [Grandfathering and migration policy drill](exercises/exercise-06-grandfathering-and-migration-policy-drill.md) | 2 | Chapter 5 |

## Lab

The module's ship deliverable — **publish a pricing + packaging pack for one startup** — one primary metric, three tiers, one anchor price per tier, one supported experiment for the next quarter, plus WTP research summary, value derivation, grandfathering policy, and operating cadence. The lab picks up from Exercises 1-6 and assembles the shippable pack per Chapter 6. See [`.aicg/curriculum-plan.json`](../../.aicg/curriculum-plan.json) for the lab spec. The lab is authored in a follow-on content cycle.

## Quiz

One quiz covers the module. See [`.aicg/curriculum-plan.json`](../../.aicg/curriculum-plan.json). Authored in a follow-on content cycle.

## Resources

See [`resources.md`](resources.md) for the citable references this module is grounded in — the WTP-research canon (Van Westendorp, Gabor & Granger, Louviere), the value-based-pricing canon (Nagle & Müller, Ramanujam & Tacke), the packaging-and-choice-psychology canon (Simonson & Tversky), and the practitioner writing on B2B SaaS pricing.

## How this module connects to the rest of the track

- **Depends on ← [mod-101](../mod-101-customer-discovery-and-problem-validation), [mod-102](../mod-102-pmf-signal-and-measurement), [mod-103](../mod-103-positioning-and-messaging), [mod-104](../mod-104-icp-and-buyer-personas), [mod-105](../mod-105-founder-led-sales).** WTP research is only meaningful when respondents match the mod-104 ICP; the value equation is only defensible when the outcome is a mod-104-persona-owned KPI; packaging is only right when the tiers match mod-103 positioning; price experiments only produce readable cohort signal when the sales motion (mod-105) is stable; and value-based pricing only lands when the mod-103 positioning has already moved the buyer's category reference class.
- **Feeds → [mod-107](../mod-107-sales-motion-design).** The pricing metric (Chapter 4) constrains the sales motion — per-seat aligns with SDR-AE inside sales, per-usage aligns with PLG, per-outcome aligns with enterprise MEDDPICC. The tier composition (Chapter 3) sets the anchor for the negotiation the enterprise motion runs.
- **Feeds → [mod-109](../mod-109-retention-expansion-and-growth-loops).** The pricing metric is the axis of expansion — per-seat expands with headcount, per-usage expands with activity, per-tier expands with upsell. NRR ≥ 100% requires the pricing metric to have a natural expansion vector.
- **Feeds → [mod-110](../mod-110-gtm-metrics-and-first-hires).** The pack's per-tier ARPU is one of the inputs to the CAC / payback / LTV benchmarks the GTM one-pager tracks.
- **Feeds → [`project-101-first-thirty-paying-customers`](../../projects/project-101-first-thirty-paying-customers).** The pricing pack is the applied artifact — the reference the founder quotes from in every one of the first thirty deals.
- **Defers up → [`startup-finance-fundraising-curriculum`](https://github.com/ai-startup-curriculum/startup-finance-fundraising-curriculum).** Deep unit-economics modelling (LTV with discount rates, cohort DCF, gross margin by tier, contribution margin optimisation, valuation-multiple analysis for the fundraising narrative) is out of scope; the pack's cohort-tracking outputs feed that model but do not replace it.

## Prerequisites and out-of-scope references

- **Prerequisite:** [`startup-foundations`](https://github.com/ai-startup-curriculum/startup-foundations) (level 10) — the startup-as-a-system mental model, the dependency graph, the stages, the founder's operating loop.
- **Prerequisite in-track:** mod-101 (discovery corpus), mod-102 (PMF cohort characteristics), mod-103 (positioning + narrative), mod-104 (ICP scorecard + personas), mod-105 (founder-led sales motion). Running mod-106 without these produces pricing derived from founder intuition rather than empirical inputs.
- **Not in scope, linked out:** deep unit-economics modelling for fundraising ([`startup-finance-fundraising-curriculum`](https://github.com/ai-startup-curriculum/startup-finance-fundraising-curriculum)); feature prioritisation / roadmap / product-analytics tooling ([`cpo-curriculum`](https://github.com/ai-startup-curriculum/cpo-curriculum)); GTM-org comp / IC-plan structures ([`startup-operations-governance-curriculum`](https://github.com/ai-startup-curriculum/startup-operations-governance-curriculum)).

---

*Return to [track overview](../../CURRICULUM.md) or [track README](../../README.md).*
