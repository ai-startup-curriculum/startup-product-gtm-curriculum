# Job Requirements — Startup Product & GTM

**Role level:** 30 (deep functional pillar — Startup family)
**Track:** `startup-product-gtm-curriculum`
**Research window:** 2026-05-23 → 2026-08-21 (last 90 days)
**Today:** 2026-08-21
**Live postings sampled this cycle:** 0 — see *Status* below

This file documents the requirements catalog used to seed the Startup Product & GTM curriculum. Raw normalised data lives in [`.aicg/job-requirements.json`](.aicg/job-requirements.json); the planned curriculum lives in [`.aicg/curriculum-plan.json`](.aicg/curriculum-plan.json).

## Status — bootstrap session, live postings deferred

Startup Product & GTM covers the **customer-facing branch** of the startup dependency graph — Customer Discovery → PMF → Positioning → ICP → Founder-Led Sales → Pricing → Sales Motion → Demand Gen → Retention & Expansion → GTM Metrics & First Hires — from IDEA-stage problem validation through the Series-A boundary of the revenue motion. Unlike a single-title role, the equivalent live-market postings span several hireable titles. The live cycle should backfill from:

- **Founding-team GTM titles:** *Founding Go-to-Market Lead*, *Founding GTM*, *Founding Sales*, *Founding AE*, *Founding Product Marketer* — pre-seed → seed startups, usually <10 headcount.
- **Head-of GTM titles:** *Head of GTM*, *Head of Growth*, *Head of Product Marketing*, *Head of Demand Generation* — seed → Series-A companies, usually 10-40 headcount.
- **Motion-specific specialist titles:** *PLG Lead*, *Growth Engineer* (GTM-oriented, not infra), *Product Marketing Manager (early-stage)*.
- **Founder / CEO adjacency:** *Chief of Staff to CEO* at pre-Series-A companies where the CoS runs GTM operations alongside the founder — filter for CoS postings that explicitly name GTM ownership.

Postings for **senior sales / marketing operator titles that assume PMF and an established revenue team of ≥8** (*VP Sales*, *CRO*, *VP Product Marketing at scale*, *VP Demand Gen*) should defer *up* — those belong to a future `startup-revenue-scaling-curriculum` or to `founder-ceo-curriculum` for CEO-level board-facing positioning, not to this pillar.

In this bootstrap cycle the required WebSearch / WebFetch tools were not granted, so the 25-in-window posting sample could not be pulled. The `postings` array is empty by design and every `requirement_themes[].frequency` is recorded as `"needs-research"` until the live cycle backfills it. This document instead grounds the requirements catalog in **authoritative public references** that publish what an early-stage GTM operator is expected to know at the *pillar* level:

- **Customer discovery + PMF canon** — [Steve Blank — *The Four Steps to the Epiphany*](https://web.stanford.edu/group/e145/cgi-bin/spring/upload/handouts/Four_Steps.pdf), [*The Startup Owner's Manual* companion overview](https://steveblank.com/2020/03/03/the-startup-owners-manual-1-a-step-by-step-guide-for-building-a-successful-company/), [Rob Fitzpatrick — *The Mom Test*](https://www.momtestbook.com/), [Anthony Ulwick / Strategyn — Jobs-to-be-Done (Outcome-Driven Innovation)](https://strategyn.com/jobs-to-be-done/), [Clayton Christensen — 'Know Your Customers' Jobs to Be Done' (HBR)](https://hbr.org/2016/09/know-your-customers-jobs-to-be-done), [Sean Ellis — The PMF Survey](https://www.startuprocket.com/articles/how-to-measure-product-market-fit-with-the-sean-ellis-survey), and [Rahul Vohra — 'How Superhuman Built an Engine to Find PMF' (First Round Review)](https://review.firstround.com/how-superhuman-built-an-engine-to-find-product-market-fit/).
- **Positioning + narrative canon** — [April Dunford — *Obviously Awesome*](https://www.aprildunford.com/obviously-awesome), [Andy Raskin — 'The Greatest Sales Deck I've Ever Seen'](https://medium.com/the-mission/the-greatest-sales-deck-ive-ever-seen-4f4ef3391ba0), and [Geoffrey Moore — *Crossing the Chasm* (companion)](https://www.mckinsey.com/industries/technology-media-and-telecommunications/our-insights/crossing-the-chasm-a-conversation-with-geoffrey-moore).
- **Founder-led sales + motion canon** — [Pete Kazanjy — *Founding Sales*](https://www.foundingsales.com/), [Aaron Ross — *Predictable Revenue*](https://predictablerevenue.com/blog/what-is-outbound-sales), [Winning by Design — SPICED framework](https://winningbydesign.com/frameworks/), [MEDDIC / MEDDPICC (canonical overview)](https://www.meddicacademy.com/what-is-meddic/), [Jason Lemkin — SaaStr](https://www.saastr.com/), and [Paul Graham — 'Do Things That Don't Scale'](https://paulgraham.com/ds.html).
- **Pricing canon** — [Patrick Campbell / ProfitWell / Price Intelligently](https://www.priceintelligently.com/blog).
- **PLG canon** — [Wes Bush — *Product-Led Growth*](https://www.productled.com/blog), [OpenView Partners — PLG Index & Benchmarks](https://openviewpartners.com/product-led-growth/).
- **Growth loops + retention canon** — [Brian Balfour / Reforge — Growth Loops](https://www.reforge.com/blog/growth-loops), [Andrew Chen — Growth essays](https://andrewchen.com/essays/), [Dave McClure — Startup Metrics for Pirates (AARRR)](https://500hats.typepad.com/500blogs/2007/09/startup-metrics.html), and [Amplitude — The North Star Metric](https://amplitude.com/blog/product-north-star-metric).
- **Demand gen canon** — [HubSpot — Inbound Methodology](https://www.hubspot.com/inbound-marketing).
- **Metrics + benchmarks** — [David Skok — SaaS Metrics 2.0](https://www.forentrepreneurs.com/saas-metrics-2/), [OpenView SaaS Benchmarks](https://openviewpartners.com/saas-benchmarks-report/), [First Round Review](https://review.firstround.com/), [Y Combinator Library](https://www.ycombinator.com/library), and [Paul Graham — 'Startup = Growth'](https://paulgraham.com/growth.html).

Every requirement below cites at least one such reference, and every requirement is shaped so posting-frequency evidence can be added underneath it without restructure.

## Methodology

1. Sourced the canonical GTM-operator task domains at the *pillar* level from the public references catalogued in [`.aicg/job-requirements.json`](.aicg/job-requirements.json) `authoritative_references` — the discovery / PMF canon (Blank, Fitzpatrick, Ulwick, Christensen, Ellis, Vohra), the positioning canon (Dunford, Raskin, Moore), the founder-led sales canon (Kazanjy, SaaStr, Winning by Design, MEDDIC), the pricing canon (Price Intelligently), the PLG canon (Bush, OpenView), the growth-loops canon (Balfour, Chen), and the metrics canon (Skok, OpenView benchmarks, Amplitude).
2. Anchored the taxonomy against the three-axis model authored in [`startup-foundations`](https://github.com/ai-startup-curriculum/startup-foundations) — the [dependency graph](https://github.com/ai-startup-curriculum/startup-foundations/blob/main/FUNCTIONAL_CURRICULA.md) (customer-facing branch owned by this repo), the [stage ladder](https://github.com/ai-startup-curriculum/startup-foundations/blob/main/STARTUP_STAGES.md) (IDEA → PRE-SEED → SEED → SERIES-A), and the founder's operating loop (never re-taught here).
3. Applied the **ownership rule** — this repo owns the customer-facing branch depth from IDEA through the Series-A boundary. Everything else defers:
   - *Down* to [`startup-foundations`](https://github.com/ai-startup-curriculum/startup-foundations) (level 10) for the mental model, the graph, the stages, the founder's operating loop, and the founder-numbers slice (runway, burn, growth read, default alive / default dead).
   - *Sideways* to [`cpo-curriculum`](https://github.com/ai-startup-curriculum/cpo-curriculum) for product-management depth (feature prioritisation, roadmap discipline, product-ops, product-analytics tooling).
   - *Sideways* to [`startup-finance-fundraising-curriculum`](https://github.com/ai-startup-curriculum/startup-finance-fundraising-curriculum) for unit-economics deep-dive beyond the GTM operator view (cohort financial modelling, capital-allocation frameworks, LTV discount-rate math, Series-A fundraising narratives).
   - *Sideways* to [`startup-operations-governance-curriculum`](https://github.com/ai-startup-curriculum/startup-operations-governance-curriculum) for GTM-org hiring / comp / IC-plan / management depth (quota carrying-rep comp structures, sales-comp legal, employment contracts).
   - *Up* to [`founder-ceo-curriculum`](https://github.com/ai-startup-curriculum/founder-ceo-curriculum) and [`cpo-curriculum`](https://github.com/ai-startup-curriculum/cpo-curriculum) — role-pathway repos that reference this curriculum rather than re-authoring it.
4. Sized each module against the level-30 depth target (~280–310h total across modules + projects), stage-tagged per [`STARTUP_STAGES.md`](https://github.com/ai-startup-curriculum/startup-foundations/blob/main/STARTUP_STAGES.md) — mod-101 → IDEA, mod-102 → PRE-SEED, mod-103–108 → SEED, mod-109–110 → SEED / SERIES-A.
5. Flagged every theme's frequency as `needs-research` so the first live research cycle can populate the number without restructuring the catalog.

## Requirement themes → curriculum ownership

The table below lists each requirement theme, its posting frequency this cycle (all `needs-research` — see *Status* above), its planned owner per the ownership rule, and the curriculum coverage path.

| # | Theme | Freq | Owner track | Coverage |
|---|---|---|---|---|
| 1 | Run customer-discovery interviews that produce information rather than compliments — Mom-Test discipline, problem / solution / product interviews, JTBD outcome interviews | <!-- needs-research --> | `startup-product-gtm` (this) | [`mod-101-customer-discovery-and-problem-validation`](lessons/mod-101-customer-discovery-and-problem-validation) |
| 2 | Measure product-market fit empirically — Sean Ellis 40% survey, retention-curve flattening, cohort behaviour, the Superhuman iteration engine | <!-- needs-research --> | `startup-product-gtm` | [`mod-102-pmf-signal-and-measurement`](lessons/mod-102-pmf-signal-and-measurement) |
| 3 | Ship a defensible positioning statement using the April Dunford five-component frame + a strategic-narrative deck in the Andy Raskin shape | <!-- needs-research --> | `startup-product-gtm` | [`mod-103-positioning-and-messaging`](lessons/mod-103-positioning-and-messaging) |
| 4 | Define an ICP precise enough for a first sales hire to qualify in / out on the first call — beachhead segment selection, buyer vs. user personas, disqualification checklist | <!-- needs-research --> | `startup-product-gtm` | [`mod-104-icp-and-buyer-personas`](lessons/mod-104-icp-and-buyer-personas) |
| 5 | Run a founder-led sales motion end-to-end per Kazanjy — discovery-call script, next-step discipline, CRM hygiene, closing the first 20-30 paying customers by hand, and the tell-tale signs it is time for the first sales hire | <!-- needs-research --> | `startup-product-gtm` | [`mod-105-founder-led-sales`](lessons/mod-105-founder-led-sales) |
| 6 | Design pricing and packaging using willingness-to-pay research, value-based pricing, good/better/best plan structure, and price-experimentation cadence | <!-- needs-research --> | `startup-product-gtm` | [`mod-106-pricing-and-packaging`](lessons/mod-106-pricing-and-packaging) |
| 7 | Match the sales motion to the ICP + ACV combination — PLG / self-serve, SDR-AE inside-sales, or enterprise MEDDPICC — and thread the qualification framework (SPICED / MEDDIC / MEDDPICC) through the funnel | <!-- needs-research --> | `startup-product-gtm` | [`mod-107-sales-motion-design`](lessons/mod-107-sales-motion-design) |
| 8 | Pick one primary + one experimental demand-generation channel per stage (founder-led outbound, inbound content + SEO, community, paid, partnerships) and diagnose channel-market fit before scaling spend | <!-- needs-research --> | `startup-product-gtm` | [`mod-108-demand-generation-and-channels`](lessons/mod-108-demand-generation-and-channels) |
| 9 | Design for retention and expansion as first-order — cohort retention curves, NRR / GRR, expansion motions, growth loops instead of a leaky funnel | <!-- needs-research --> | `startup-product-gtm` | [`mod-109-retention-expansion-and-growth-loops`](lessons/mod-109-retention-expansion-and-growth-loops) |
| 10 | Read the GTM operator numbers — CAC, LTV, payback, magic number, sales efficiency, funnel conversion, cohort retention, NRR — against OpenView / SaaStr benchmarks, and stage the first three GTM hires without over-hiring ahead of PMF | <!-- needs-research --> | `startup-product-gtm` | [`mod-110-gtm-metrics-and-first-hires`](lessons/mod-110-gtm-metrics-and-first-hires) |
| 11 | Startup-as-a-system mental model — graph, stages, founder's operating loop, founder-numbers slice — every learner arrives with this installed | <!-- needs-research --> | `startup-foundations` | Linked out — prerequisite; this track never re-teaches. See [`PREREQUISITES.md`](PREREQUISITES.md). |
| 12 | Product-management depth — feature prioritisation, roadmap discipline, product-ops, product-analytics tooling — the *how* of shipping product, distinct from the *what* of finding a market | <!-- needs-research --> | `cpo-curriculum` | Linked out (mod-102 and mod-109 name the sideways boundary) |
| 13 | Unit-economics deep-dive beyond the GTM operator view — cohort financial modelling, capital-allocation frameworks, LTV discount-rate math, fundraising narratives that turn GTM traction into a Series-A pitch | <!-- needs-research --> | `startup-finance-fundraising-curriculum` | Linked out (mod-106 and mod-110 hand off) |
| 14 | Hiring / comp / IC-plan / management depth for the GTM org — quota carrying-rep comp structures, sales-comp legal, employment contracts | <!-- needs-research --> | `startup-operations-governance-curriculum` | Linked out (mod-110 hands off the *staging* logic keeps here; the *comp* structures defer) |

## Emerging themes — below curriculum threshold this cycle

None captured this cycle. The scaffold pass does not sample live postings and therefore does not produce below-threshold signal. The first live research cycle will populate `emerging_themes_below_threshold` in [`.aicg/job-requirements.json`](.aicg/job-requirements.json) once postings backfill.

## Posting evidence

0 in-window postings sampled 2026-05-23 → 2026-08-21 (scaffold cycle — WebSearch / WebFetch not granted). See [`.aicg/job-requirements.json`](.aicg/job-requirements.json) `research_status.needs_research_note` for the exact sampling contract the next cycle should honour, and this document's *Status* section for the equivalent-title buckets the next cycle should draw from.

<!-- needs-research: backfill 25+ live in-window postings on the first cycle where WebSearch / WebFetch is exercised — fan out across (a) Founding-GTM / Founding-Sales / Founding-Product-Marketer postings on YC Work at a Startup and Wellfound / AngelList Talent for pre-seed → seed startups (<10 headcount); (b) Head-of-GTM / Head-of-Growth / Head-of-Product-Marketing / Head-of-Demand-Gen postings at seed → Series-A companies (10-40 headcount); (c) PLG Lead and Product Marketing Manager (early-stage) motion-specialist postings; (d) Chief-of-Staff-to-CEO postings at pre-Series-A companies with explicit GTM ownership. Filter out VP Sales / CRO / VP Marketing / VP Demand Gen postings that assume PMF and a revenue team of ≥8 — those defer up to a future startup-revenue-scaling track or to founder-ceo-curriculum. -->

## Ownership map — quick reference for the next cycle

When backfilling postings, use this ownership decision to keep this pillar from drifting into Foundations, product-management, finance, or ops territory:

- **Startup Product & GTM** (this repo, level 30) — owns Customer Discovery, PMF measurement, Positioning, ICP, Founder-Led Sales, Pricing & Packaging, Sales Motion Design (PLG / SDR-AE / Enterprise), Demand Generation, Retention & Expansion, Growth Loops, and GTM Metrics & First-Hire staging. IDEA-stage through Series-A boundary.
- **Startup Foundations** (`startup-foundations`, level 10) — the *system*, the *graph*, the *stages*, the founder's operating loop, and the founder-numbers slice (runway / burn / growth). Prerequisite. *Never* re-taught here.
- **CPO** (`cpo-curriculum`, level 30) — product-management depth (feature prioritisation, roadmap, product-ops, product-analytics tooling). Sideways peer — this pillar owns *market-facing* discovery / PMF / positioning; CPO owns *shipping-facing* prioritisation / roadmap.
- **Startup Finance & Fundraising** (`startup-finance-fundraising-curriculum`, level 20) — unit-economics deep-dive, capital allocation, fundraising, equity. Sideways — this pillar covers the *operator* view of CAC / LTV / payback / magic number as GTM instruments; the fundraising-narrative / cohort-financial-modelling depth lives there.
- **Startup Operations & Governance** (`startup-operations-governance-curriculum`, level 25) — people, legal, operations, governance. Sideways — this pillar covers the *staging* logic for the first three GTM hires (which hire when, based on what GTM signal); comp structures, sales-comp legal, and management depth live there.
- **Founder / CEO** (`founder-ceo-curriculum`, level 30) — CEO-level board-facing GTM positioning. Sideways role-pathway peer — references this curriculum for GTM depth at ~60% coverage.

## Salary evidence

Not gathered this cycle — WebSearch / WebFetch gated. On the first live cycle, the salary summary should aggregate published US ranges **per equivalent-title bucket** rather than as a single headline aggregate:

- Founding GTM / Founding Sales / Founding Product Marketer (pre-seed → seed, <10 headcount)
- Head of GTM (seed → Series-A)
- Head of Growth (seed → Series-A)
- Head of Product Marketing (seed → Series-A)
- Head of Demand Gen (seed → Series-A)
- PLG Lead (seed → Series-A)
- Chief of Staff to CEO with GTM scope (pre-Series-A)

Do not quote a headline range until the strict per-bucket sample clears **n≥8 with salary present**. Sales-comp postings often quote only OTE (on-target-earnings) or base only — the live cycle must record which was quoted and normalise before aggregating. See [`.aicg/job-requirements.json`](.aicg/job-requirements.json) `salary_summary` for the machine-readable placeholder.
