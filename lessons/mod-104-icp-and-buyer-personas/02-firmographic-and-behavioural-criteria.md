# Firmographic and Behavioural Criteria — The Two Layers of a Scoreable ICP

## Motivation

Chapter 1 fixed the operating bar: the ICP must be scoreable on a first call by a first sales hire. This chapter is the criteria-authoring instrument that lifts the ICP to that bar.

The most common shape of a broken ICP is a *purely firmographic* filter — "50-200 employees, B2B SaaS, Series A or later, US-based." It is scoreable (yes / no on each field), it is filterable in LinkedIn Sales Navigator, and it is completely useless: two companies inside that filter can have identical firmographics and radically different fit. One has an engineering leader who reports throughput to the board every month; the other has never measured throughput. One is deploying to production 20× a day with a Slack-heavy async culture; the other ships a quarterly release from a Jira board. The two look identical to a firmographic scorecard and behave completely differently in a sales cycle.

The remedy is a **two-layer** ICP: firmographic criteria (Layer 1 — the company as a Crunchbase / LinkedIn / ZoomInfo entity) and behavioural criteria (Layer 2 — how the company operates). Both layers are scoreable; both are load-bearing; neither works without the other. This chapter names the criteria types in each layer, the scoring rules, and the discipline that keeps the criteria bounded.

The failure mode this chapter exists to catch: **the founder writes a ten-line firmographic filter, ships it, and every deal that passes the filter still needs an hour of live-conversation qualifying because the firmographic filter does not predict fit.** The remedy is not a longer firmographic list; it is the behavioural layer.

## Core concepts

### Layer 1 — firmographic criteria (the company as a database entity)

Firmographics are the attributes of the company that show up in a third-party data source without a conversation. They are what a demand-gen team filters on to build an outbound list, and what an AE can pre-qualify from a LinkedIn profile before a call is even booked.

The canonical firmographic dimensions:

- **Employee count band.** The single most-load-bearing firmographic. 1-10, 10-50, 50-200, 200-1000, 1000-5000, 5000+ — pick the bands that map to *your product's whole-product surface*. A product that requires ≥ 20 engineers to see value should not have a band starting at 1-10; a product priced $500/month should not have a band starting at 5000+.
- **Revenue / ARR band.** Complementary to employee count. In modern software companies revenue-per-employee varies 10× between engineering-heavy startups and services-heavy consultancies, so both bands together carry more signal than either alone. If you sell to public companies, revenue is often the cleaner axis (10-K disclosures); to private companies, employee count via LinkedIn is the more reliably-observable axis.
- **Industry / vertical.** GICS or NAICS codes are the standard third-party taxonomies; most sales-data providers use variants of them. At SEED the industry filter is often a specific sub-vertical inside a larger one — "cybersecurity" is too broad; "identity and access management vendors selling to CISOs at 500+-employee companies" is a filter. Chapter 6's beachhead discipline is what narrows the industry filter.
- **Geography.** Country / region / metro. Load-bearing when the product has a geographic constraint (data residency, language, currency, regulation) or when the sales motion requires travel (field-sales enterprise motions). For a global SaaS product with an inside-sales motion, geography may be a low-weight filter or absent from the ICP.
- **Company stage / funding.** For B2B-SaaS-selling-to-startups products, the funding stage is often the sharpest signal — a Series-A startup has $10M+ in the bank and a mandate to spend it on growth; a bootstrapped company at similar headcount has a different budget posture. Sources: Crunchbase, PitchBook.
- **Technology graph.** Which technologies the company runs on — cloud provider (AWS / GCP / Azure), source-code host (GitHub / GitLab), authentication (Okta / Google Workspace / Microsoft Entra), CRM (Salesforce / HubSpot), data warehouse (Snowflake / BigQuery / Databricks), observability (Datadog / New Relic). Load-bearing when your product integrates natively with a specific stack. Data sources: BuiltWith, HG Insights, Wappalyzer, or scraped from public engineering blogs.
- **Growth signals.** Recent funding, hiring velocity (LinkedIn "we're hiring" tags), executive hires (a new VP Eng often opens a 90-day evaluation window for engineering tools). Data sources: LinkedIn, PitchBook, hiring-tracker services.

The **bounded discipline**: pick the smallest set of firmographic dimensions that separates strong fits from weak fits. Six is a common ceiling. A twelve-dimension firmographic filter is a research document, not a first-call instrument.

The **scoreable discipline**: each dimension resolves to a specific value or range. Not "growth-stage"; "Series A through Series C, or bootstrapped at ≥ $5M ARR." Not "modern cloud stack"; "≥ 80% workloads on AWS or GCP." A dimension you cannot resolve to a value from a third-party lookup does not belong in the firmographic layer — it belongs in the behavioural layer.

### Layer 2 — behavioural criteria (how the company operates)

Behavioural criteria are the attributes of *how the company works* that are not observable from Crunchbase but are surfaced within a five-to-ten-minute discovery conversation. They are the layer that separates two firmographically-identical companies into "will close in three weeks" and "will die in the last stage."

The behavioural dimensions cluster into four types:

- **Workflow presence.** The company has an existing workflow the product plugs into or replaces. "Runs a weekly pipeline review with the exec team"; "engineering manager runs a Monday stand-up around PR-cycle metrics"; "sales team logs every call in the CRM within 24 hours." A product whose value is "makes the weekly pipeline review faster" needs the weekly pipeline review to *exist* in the target company; if it doesn't, the value proposition has no host workflow.
- **Metric ownership.** A specific person owns a specific metric that the product moves. "The VP Eng has a board-facing engineering-throughput KPI"; "the head of support has a first-response-time OKR"; "the CFO has a specific gross-margin target". Metric ownership is the strongest single behavioural predictor of urgency — a metric-owner has a personal stake in moving the number, and will run the buying process; a company without a metric owner will nod at the demo and never close.
- **Buying-motion posture.** How the company buys software. "Departmental budget authority for tools ≤ $50k without procurement review"; "engineering leadership has a self-serve budget"; "any purchase above $10k requires a formal RFP." Load-bearing when your ACV crosses a buying-authority threshold. A $30k ACV product sold into a company with a $10k RFP threshold has *just been informed* the sales cycle is doubling.
- **Technical maturity / prerequisite behaviour.** The company already exhibits behaviour that suggests the value will be legible. "Runs post-incident reviews as a discipline" for an incident-response product; "has a dedicated data platform team" for a data-tooling product; "measures cohort retention monthly" for an analytics product. A company that does not exhibit the prerequisite behaviour typically will not adopt the product even if firmographic fit is perfect — the value has no legibility.

The **scoring discipline**: each behavioural criterion resolves to a specific question that surfaces the answer within a five-to-ten-minute discovery conversation. Not "the company is mature"; "on the first discovery call, ask 'how does your engineering leader currently measure cycle time?' — if the answer is a specific metric with a specific owner, score 1; if the answer is a version of 'we should be doing that,' score 0."

The **calibration discipline**: the specific behavioural criteria come from your mod-101 discovery corpus and mod-102 Sean Ellis "very disappointed" cohort. The behaviours the strongest-fit customers *already exhibited* before adopting the product are the behavioural criteria that predict fit in new prospects. If the top decile of your customers all ran a weekly PR-cycle review before signing, the weekly PR-cycle review is a behavioural criterion. Behavioural criteria you invent from first principles without corpus grounding are almost always wrong.

### Weighting — not every criterion is equal

Both layers score each criterion; not every criterion is worth the same. A common weighting:

- **Must-have (weight = disqualifying).** Failing this criterion is a full disqualification. Chapter 3 develops the disqualifier discipline; the ICP scorecard reserves 2-4 slots for must-haves that hard-fail the deal.
- **Should-have (weight = 2 or 3).** Strong fit signal. Ideally the prospect has all of these; missing one is not a full disqualification but knocks the fit score down materially.
- **Nice-to-have (weight = 1).** Positive signal but not load-bearing. Presence contributes to a "very strong fit" score but absence does not disqualify.

A scored ICP with 6-8 criteria and honest weights produces a total-score band the AE can act on. A typical bandsplit:

- **Score ≥ 80% of max, zero must-have failures:** in — full sales cycle.
- **Score 50-80%, zero must-have failures:** in-with-caveat — sales cycle proceeds with the specific gap named as a known risk.
- **Score < 50%, or ≥ 1 must-have failure:** out — discovery ends with a "this is not a fit" call, next steps are (a) refer to a peer, (b) put on "revisit in 12 months," or (c) close-lost with a clean reason code.

The weighted-scorecard shape is what makes the ICP an *operating instrument* rather than a paragraph. The number is not sacred — 78% vs 82% is a rounding error — but the honesty is: an AE staring at a 45% score with a must-have miss should not be spending another hour on the deal.

### The two-layer separation is what makes the ICP filterable *and* predictive

A common shortcut founders take is to fold everything into one big list and score them equally. The result is an ICP that *scores* things (so it looks operational) but does not *filter* things (because there is no observable-from-database subset to build an outbound list against).

The separation matters for a specific reason: **the firmographic layer builds the top-of-funnel list; the behavioural layer scores that list in-conversation.** Demand-gen (mod-108) needs the firmographic layer to construct a target list from Sales Navigator, buy an intent-data cut, or brief an outbound SDR. Sales (mod-105) needs the behavioural layer to score the list-derived leads once conversations start. Fold them together and you get a scorecard that neither side can use as intended.

A useful test: **can your demand-gen owner build a Sales Navigator list from Layer 1 alone, without asking the founder any clarifying questions?** If yes, Layer 1 is correctly authored. **Can your AE score Layer 2 in a 20-minute discovery call, without extra research?** If yes, Layer 2 is correctly authored.

### Where each criterion type comes from — provenance discipline

Every criterion on the scorecard should have a provenance line answering *why this criterion is on the list*. The three legitimate provenances:

1. **From the mod-102 PMF cohort.** "80% of the ≥ 40% cohort share this criterion; ≤ 20% of the < 40% cohort do." The strongest form of provenance — the criterion is empirically calibrated to fit.
2. **From the mod-101 discovery corpus.** "Named as the trigger by 6+ of the 15 buyer interviews; named as the blocker by 2+ interviews on the losing side." Weaker than PMF calibration but still empirical.
3. **From a structural product constraint.** "Product requires SSO integration; must-have is 'company enforces SSO across engineering tools' because unenforced-SSO companies will not adopt." Provenance is the product surface, not customer data — legitimate but should be a small minority of criteria.

Criteria without any of these three provenances — founder intuition, "everyone in our category has this on their ICP," "it feels like the right filter" — are almost always wrong and are the source of the aspirational-ICP failure Chapter 1 warned about. If a criterion has no provenance, the exercise is either to source it (by re-interviewing three customers) or to drop it.

### The bounded-count discipline

The single most-under-enforced constraint on ICP criteria is *count*. Six to eight scoreable criteria across both layers is the working ceiling. Ten is a stretched artifact. Twelve is not an ICP; it is a research questionnaire.

The reason is operational: an AE on a discovery call cannot hold twelve criteria in their head *and* run a natural conversation. What happens instead is that the AE mentally collapses the twelve into three or four they can remember, and the other eight are ignored. The scorecard is theatre.

Bounding the count forces the authoring discipline. Which of these twelve actually separates strong fits from weak fits? Which are correlated with each other (drop the redundant one)? Which are actually a Chapter 3 disqualifier and belong in a different section of the artifact? Which are behaviors that show up only for closed customers, not for prospects (drop — they are lagging, not leading)? The bounded-count constraint is what pushes the author to the small, load-bearing set.

## Concrete example — Loomly's two-layer ICP

Returning to Loomly's SEED ICP from Chapter 1, laid out in two layers with weights and provenances:

### Layer 1 — firmographic criteria

| # | Criterion | Value / range | Weight | Provenance |
|---|---|---|---|---|
| F1 | Employee count | 50-150 (engineering) or 100-400 (total) | Must-have | Below 50 eng: no scale problem yet; above 150: enterprise motion required, whole-product gap |
| F2 | Industry | B2B SaaS — devtools, observability, developer-productivity, security-tooling sub-verticals | Must-have | mod-103 beachhead selection |
| F3 | Primary source-code host | GitHub (Cloud or Enterprise Cloud) | Must-have | Product is GitHub-native; GitLab / Bitbucket not shipped |
| F4 | Working model | Distributed or hybrid (≥ 40% remote) | Should-have (weight 3) | mod-102 PMF cohort: 90% of ≥ 40% cohort was distributed |
| F5 | Funding stage | Series A through Series C, or bootstrapped ≥ $5M ARR | Should-have (weight 2) | Buying-authority proxy; ACV of $12k/yr requires this bracket |
| F6 | Geography | US, Canada, UK, EU (English-speaking sales motion) | Nice-to-have (weight 1) | Sales motion is English; localisation not shipped |

Six criteria. Every one is filterable in Sales Navigator or LinkedIn + a technology-graph provider. Every one has a stated provenance. Demand-gen can build the outbound list from this table alone.

### Layer 2 — behavioural criteria

| # | Criterion | Discovery question | Weight | Provenance |
|---|---|---|---|---|
| B1 | Engineering-throughput metric ownership | "Does your VP Eng or CTO have a board-facing throughput or cycle-time metric they report?" | Must-have | mod-102 cohort: 100% of very-disappointed had this |
| B2 | Existing PR-review workflow | "How does your team currently handle stalled PRs? Slack pings? A weekly review? An engineering manager who chases?" | Should-have (weight 3) | mod-101 corpus: named by 8/12 problem interviews |
| B3 | Deploys ≥ 1× per week to production | "How often do you deploy to production? Continuously? Weekly? Monthly?" | Should-have (weight 2) | Product only creates urgency for teams deploying often |
| B4 | Engineering-tool budget owned by VP Eng or CTO (not procurement-gated below $25k) | "For tools in this budget range — say $10-25k a year — does that go through engineering leadership or does procurement own the process?" | Should-have (weight 2) | ACV positioning: buying-motion posture |
| B5 | Prior engineering-productivity tool adoption | "What developer-productivity tools have you adopted in the last 12 months?" | Nice-to-have (weight 1) | Behavioural predictor: tool-adopting teams re-adopt |

Five behavioural criteria. Each has a specific discovery question that surfaces the answer in 90 seconds or less. Total ICP score: 11 criteria across both layers, weighted; a fully-hit deal scores 20 points; the in / in-with-caveat / out bands sit at 16+ / 10-15 / < 10.

An AE can carry this on one page. Chapter 7's shipping artifact is the format that fits it there.

### Contrast — the same product with only Layer 1

If Loomly had stopped at the firmographic layer, the ICP would let through:

- A 100-engineer B2B SaaS devtools company using GitHub, distributed, Series B — *whose engineering leader has never measured cycle time*. Layer 1 passes; Layer 2's B1 must-have fails. The AE would spend three weeks in demo/pilot before discovering the buyer has no metric to move. Deal dies at "let me think about it."
- A 100-engineer B2B SaaS devtools company using GitHub, distributed, Series B — *that deploys quarterly*. Layer 1 passes; Layer 2's B3 should-have (weight 2) fails; B1 may fail too. The value proposition ("cycle-time reduction") is not legible to a team whose cycles are already 90 days long.

Both of these firms would look identical to a Layer-1-only ICP. Both would be full sales cycles that died late. The behavioural layer is what catches them before the AE spends the cycle.

## Common failure patterns

- **Layer 1-only ICP.** Filterable, unpredictive. Two firms with identical firmographics behave completely differently. Add the behavioural layer or accept a low close rate.
- **Layer 2-only ICP.** Predictive, unfilterable. Demand-gen cannot build a list from "engineering managers who report cycle-time metrics" because that data is not in any database. Both layers, not one.
- **Behavioural criteria authored from founder intuition.** If the behavioural criteria are not sourced from the mod-102 PMF cohort or mod-101 discovery corpus, they are almost certainly wrong. Provenance discipline is what keeps this honest.
- **Behavioural criterion that can only be verified post-close.** "Team uses the product 5× per week" is a *retention* signal, not a prospect signal — the AE cannot ask about it on a discovery call. Leading vs lagging discipline: behavioural criteria must be observable *before* purchase, not after.
- **Twelve-criterion scorecard.** The AE mentally collapses to three; the other nine are decorative. Bound to 6-8; force the authoring discipline.
- **Weightless scoring.** Every criterion counts the same; a must-have miss weighs the same as a nice-to-have miss. Result: the deal-killing gaps get lost in the aggregate score. Weight the criteria, and mark 2-4 as disqualifying must-haves (Chapter 3).
- **Discovery-question missing on behavioural criteria.** Each behavioural criterion needs the *exact question* the AE will ask to score it. Without the question, the AE improvises, the phrasing differs deal to deal, and scoring is inconsistent.
- **Firmographic filter that excludes the current customer base.** Sanity check: run the ICP against your current 20 best-fit customers. If any of them fail Layer 1's must-haves, the ICP is broken (or those customers were misfits) — pause and reconcile.

## Summary

- A scoreable ICP has **two layers**: firmographic criteria (Layer 1 — the company as a database entity, filterable in Sales Navigator) and behavioural criteria (Layer 2 — how the company operates, surfaced in a 5-10-minute discovery conversation).
- **Layer 1** dimensions are typically: employee count, revenue / ARR, industry / vertical, geography, funding stage, technology graph, growth signals. Six or fewer.
- **Layer 2** clusters into: workflow presence, metric ownership, buying-motion posture, technical maturity / prerequisite behaviour. Each criterion has a *specific discovery question* the AE can ask.
- **Weight** the criteria: must-have (disqualifying), should-have (2-3), nice-to-have (1). Score bands at ≥ 80% (in), 50-80% (in-with-caveat), < 50% or must-have miss (out).
- **Provenance** every criterion: mod-102 PMF cohort, mod-101 discovery corpus, or structural product constraint. Founder-intuition criteria are the source of most aspirational ICPs.
- **Bounded count** — 6-8 criteria across both layers is the ceiling. A twelve-criterion scorecard is theatre; the AE mentally collapses to three.
- **The two-layer separation** is what makes the ICP simultaneously filterable (demand-gen builds a list from Layer 1) and predictive (sales scores the list in Layer 2). Folding them into one list breaks both use-cases.
- Chapter 3 develops the **disqualification checklist** — the must-have criteria that hard-fail the deal — as a first-class section of the scorecard, not an afterthought.
