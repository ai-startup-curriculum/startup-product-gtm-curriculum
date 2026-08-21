# GRR vs NRR — Two Numbers, Two Verdicts

## Motivation

Chapter 1 established that cohort retention is the customer-level ground truth. This chapter introduces the two *revenue-level* roll-ups the board pack, the fundraising memo, and every SaaS underwriter reads first: **gross revenue retention (GRR)** and **net revenue retention (NRR)**.

Founders routinely conflate the two, quote NRR without GRR (or vice versa), or report a headline number that mixes downgrades and upgrades in a way that hides the real story. The result is a metric that a Series-B underwriter cannot use — and a founder who cannot see what is actually happening in the book of business. GRR tells you the **floor**: how much of last year's revenue would you keep if no customer ever upgraded. NRR tells you the **whole**: how much of last year's revenue you kept after upgrades net downgrades net churn. **Both matter, and they must be reported together** — reporting only one is the SaaS-metrics equivalent of reporting only revenue without margin.

This chapter fixes the definitions, walks the calculation on a small worked book, names the benchmark bands, and unpacks the failure modes founders trip on when they compute either number in a way an outside underwriter would reject.

## Core concepts

### Definitions — the exact formulas

Both metrics measure **year-over-year revenue retention on a fixed customer cohort**. The cohort is the set of customers who existed at the start of the measurement period; both formulas compare *that cohort's revenue today* to *that cohort's revenue a year ago*. New customers acquired during the period are **excluded** from both. Getting the cohort right is 80% of the work.

**Gross Revenue Retention (GRR).**

```
GRR = (Starting ARR − Downgrade ARR − Churned ARR) / Starting ARR
```

- **Starting ARR** — the annualised recurring revenue of the cohort at the start of the period.
- **Downgrade ARR** — the revenue lost from customers still in the cohort who downgraded (fewer seats, cheaper tier, reduced usage commit).
- **Churned ARR** — the revenue lost from customers in the cohort who cancelled entirely.
- **GRR is capped at 100%.** Expansion is excluded. GRR isolates the *churn floor* — how much you would retain if no customer ever grew.

**Net Revenue Retention (NRR).**

```
NRR = (Starting ARR − Downgrade ARR − Churned ARR + Expansion ARR) / Starting ARR
```

- **Expansion ARR** — additional revenue from customers still in the cohort: seat expansion, tier upgrade, usage upsell, cross-sell into an adjacent product surface.
- **NRR is not capped.** A cohort that expanded aggressively can produce NRR well above 100% — the definition of a "negative churn" motion where the average customer contributes more revenue this year than last, before any new logos are counted.

**The identity worth memorising:** `NRR = GRR + Expansion Rate`, where `Expansion Rate = Expansion ARR / Starting ARR`. This makes visible why the two numbers must be reported together — an NRR of 120% means very different things at GRR=95% (small churn, strong expansion — a healthy motion) versus GRR=70% (heavy churn, huge expansion masking it — a motion that is quietly falling apart).

The definitions above are the working consensus in the practitioner and investor literature ([David Skok — "SaaS Metrics 2.0"](https://www.forentrepreneurs.com/saas-metrics-2/); [OpenView — Expansion SaaS Benchmarks](https://openviewpartners.com/expansion-saas-benchmarks/); [Bessemer — State of the Cloud](https://www.bvp.com/atlas); [SaaStr — NRR benchmarks writeups](https://www.saastr.com/); [KeyBanc — SaaS Survey](https://www.key.com/businesses-institutions/industry-expertise/key-technology-group.html)). The formulas above are the versions an outside underwriter will use to reconstruct your numbers from your billing system; if you produce a "GRR" that differs from this, you have to explain the difference.

### The load-bearing choice — customer cohort vs. dollar cohort

The definitions above are **dollar-cohorted** (starting ARR is the denominator). Some teams alternatively report **customer-cohorted** logo-retention numbers — what fraction of the starting logo count is still paying. These are related but distinct:

- **Logo retention** (also called customer retention or account retention): `Retained Customers / Starting Customers`. A small customer and a large customer count equally.
- **Dollar retention (GRR/NRR)**: dollar-weighted. A single large customer's downgrade can move the number by many points; the loss of a small customer barely nudges it.

**Both are load-bearing at different reads.** Logo retention is what you read in the customer-success stand-up ("we lost three of forty accounts this quarter"). Dollar retention is what the board pack and the fundraise memo require. A book with strong logo retention and weak GRR is losing large accounts and keeping small ones — a specific and diagnosable failure mode.

Common convention: **report GRR and NRR (dollar-weighted) as the headline numbers; keep logo retention as an internal operating metric.** The mismatch is a routine misread if the two are quoted interchangeably.

### The Series-A benchmark — why NRR ≥ 100% is the modern bar

The single most widely-cited benchmark in the modern SaaS underwriting canon is **NRR ≥ 100% at Series-A / Series-B**. The reason it is the bar and not, say, 90%, is arithmetic.

An **NRR of 100%** means the same cohort produces the same revenue this year as last year — before any new logos. Every dollar of new-logo ARR is *net-new revenue*, not covering for churn. Growth compounds cleanly.

An **NRR of 90%** means the same cohort shrinks 10% year-over-year. To grow the topline at all, new-logo ARR has to cover the 10% cohort shrinkage *before* producing any growth. The team is running on an acquisition treadmill.

An **NRR of 120%** means the same cohort *grows* 20% year-over-year. New-logo ARR compounds on top. This is the "negative churn" motion; growth is exponential in a way an NRR ≤ 100% motion cannot be.

The Series-A benchmark of ≥ 100% has appeared in **OpenView's SaaS benchmarks**, **Bessemer's Cloud Index** commentary, **KeyBanc's SaaS Survey**, **SaaStr writeups**, and **Bain / Meritech investor education**. Practitioner-benchmark ranges typically cited (with the caveat that they shift year-over-year and by ARR band):

- **NRR ≥ 100%** — the modern working threshold for a scalable SaaS motion at Series-A.
- **NRR ≥ 110%** — mid-range for a healthy usage-based or seat-expansion motion at Series-B.
- **NRR ≥ 120%** — best-in-class for public SaaS at scale; often cited as the Snowflake / Datadog / Twilio band during their pre-IPO growth phase.
- **GRR ≥ 85%** — working threshold for SMB motions.
- **GRR ≥ 90%** — working threshold for mid-market motions.
- **GRR ≥ 95%** — working threshold for enterprise motions.

<!-- needs-research: pin specific NRR/GRR bands by ARR tier and motion type to the current OpenView / KeyBanc / Bessemer surveys; the specific quantitative thresholds shift year-over-year and the numbers above are working practitioner ranges rather than a single-source benchmark. -->

Read benchmarks as *directional*, not as verdicts. The right calibration is against the **specific ARR band, motion type, and segment mix** of your book. A pre-Series-A team with strong PMF in mid-market and no enterprise motion cannot benchmark against a public enterprise SaaS's NRR; a company with a seat-heavy PLG motion will look very different from one with usage-metered infrastructure billing.

### Worked calculation — a small book, all four movements

Start of period (year 0), fixed cohort of five customers:

| Customer | Starting ARR (Y0) | End ARR (Y1) | Movement |
|---|---|---|---|
| Acme  | $120,000 | $150,000 | +$30k expansion (seat upsell) |
| Beta  |  $80,000 |  $60,000 | −$20k downgrade (dropped a tier) |
| Gamma | $150,000 | $150,000 | flat |
| Delta |  $60,000 |       $0 | churned entirely |
| Epsilon | $40,000 |  $70,000 | +$30k expansion (usage-based upgrade) |
| **Total** | **$450,000** | **$430,000** | |

Movements decomposed:

- **Starting ARR** = $450,000.
- **Churned ARR** = $60,000 (Delta).
- **Downgrade ARR** = $20,000 (Beta).
- **Expansion ARR** = $60,000 ($30k Acme + $30k Epsilon).

**GRR** = (450,000 − 20,000 − 60,000) / 450,000 = 370,000 / 450,000 = **82.2%**.

**NRR** = (450,000 − 20,000 − 60,000 + 60,000) / 450,000 = 430,000 / 450,000 = **95.6%**.

Two things fall out of the numbers you would not see if you reported only one:

- **GRR of 82.2% is weak for an enterprise motion** (the benchmark band above is ≥ 95%). This book is bleeding revenue at the floor.
- **NRR of 95.6% is masked by strong expansion** — $60k of expansion is doing heavy lifting to compensate for $80k of downgrade + churn. If the expansion motion stalls for even one quarter, NRR falls to the mid-80s.

The read this book demands is *"expansion is compensating for churn; investigate why we are losing 18% of Starting ARR through the floor before we lose the expansion motion too."* The single number "NRR = 95.6%" hides that. Reporting both is the whole point.

### The four movements the book must decompose

To produce defensible GRR and NRR, the billing system (or manual roll-up) has to decompose every ARR change in the cohort into exactly one of four buckets:

- **New ARR** — new logo acquisition. Excluded from GRR and NRR (both are cohort-locked).
- **Expansion ARR** — additional revenue from a customer already in the cohort. Seat additions, tier upgrades, usage-based upsell, cross-sell into an adjacent product line.
- **Downgrade ARR** — revenue lost from a customer still in the cohort. Seat removals, tier downgrades, reduced usage commits.
- **Churned ARR** — revenue lost from a customer who left the cohort entirely.

Two edge cases founders trip on:

- **Renewals with price change.** A customer who renews at a higher price (contract escalation or repricing) is expansion; a customer who renews at a lower price (negotiated down) is downgrade. Not "renewed" as a neutral bucket.
- **Multi-year contracts.** Report on **ARR** (annualised) or **committed MRR × 12**, not on billed revenue in period. A three-year contract's ARR is contract value ÷ contract years, not the cash paid in year one.

The decomposition must be *complete* — every dollar of change is in exactly one bucket. Any "misc adjustments" bucket you cannot classify is a leak in the metric; over time, it drifts to hide the very churn or expansion the metric is meant to expose.

### Segmentation — cohort-level and revenue-band-level

Chapter 1's segmentation discipline persists here. Company-wide NRR and GRR hide segment-level facts that dominate the operating decision.

At minimum, decompose GRR and NRR by:

- **ARR tier / customer size.** Enterprise vs. mid-market vs. SMB. Enterprise books usually retain and expand far better; SMB books usually churn heavily and expand modestly. A company-wide NRR of 105% can be 130% in enterprise and 88% in SMB — a decision-critical split for both product and GTM investment.
- **Cohort year of acquisition.** The 2023 cohort's NRR through today vs. the 2024 cohort's NRR through today. A degradation is a durability signal on the *newer* acquisitions (compare with Chapter 1's cohort-over-cohort read).
- **Product / SKU.** For multi-product companies, per-SKU retention isolates whether the composite number is being carried by one strong product line and dragged by another weak one.
- **Segment / vertical.** For companies with multi-segment ICPs, retention often varies wildly across verticals — one strong-fit vertical can carry an aggregate that reads as mediocre.

The specific cut that matters most depends on the business. **Any headline NRR / GRR that is not decomposed at least one level down from the aggregate is not defensible in a Series-A / B diligence process.** The underwriter will decompose it for you; do the work first.

### Failure modes — where GRR and NRR quietly lie

- **Cohort drift.** The "starting cohort" quietly changes between periods — someone excludes churned accounts from the starting count, or includes accounts that were added mid-year. The number reads better than the truth. Lock the cohort at period start and never adjust it.
- **Reporting NRR without GRR.** A book at NRR=115% and GRR=75% is very different from NRR=115% and GRR=98%. Underwriters read both; report both.
- **Expansion attributed to the wrong period.** Expansion from a customer who upgraded in month 11 of the prior year sometimes gets counted in the current year to flatter the number. Attribution rule: expansion is dated by the effective start of the new ARR level.
- **Downgrade booked as churn (or vice versa).** A customer who reduces seats and then cancels three months later can be booked as "churn = full starting ARR" or as "downgrade + subsequent churn." The dollar total is the same; the diagnosis is not. Pick a convention and enforce it.
- **Multi-year contract paper vs. ARR.** A $600k three-year deal recognised as $600k of "new ARR" in year one inflates every downstream metric. It is $200k ARR for three years.
- **Involuntary churn treated as voluntary (or ignored).** Chapter 6 unpacks this. Payment-failure churn is a metric that a dunning programme can move by several percentage points; if you fold it into the same "churned ARR" bucket as intentional cancellation, you lose the diagnosis.
- **Currency and pricing-model changes not normalised.** A price change or currency conversion mid-cohort produces artificial expansion / downgrade. Normalise before computing.

Every one of these failure modes is exactly the sort of thing a Series-B partner and their diligence firm will find in the second week of a fundraise, and each one lands as an investor-side reason to renegotiate terms or pull. The mitigations are cheap to run in-house on a monthly cadence; the cost of the failure at a fundraise is not.

## Concrete example — the code-review-tool one year later

Return to the code-review-tool from Chapter 1. The team has 240 mid-market teams paying, with a per-seat metric and a "premium security" cross-sell tier introduced six months ago.

**Cohort locked at 2025-01-01:** 108 mid-market teams, $2.16M ARR.

**Year-end 2025 status of the same 108 teams:**

| Movement | # of teams | ARR delta |
|---|---|---|
| Renewed flat | 71 | $0 |
| Expanded (seats added) | 22 | +$580k |
| Expanded (security cross-sell) | 8 | +$120k |
| Downgraded (seats removed) | 6 | −$180k |
| Churned | 9 | −$300k |
| **Net movement** | **108** | **+$220k** |

Compute:

- **Starting ARR** = $2,160,000.
- **Churned ARR** = $300,000.
- **Downgrade ARR** = $180,000.
- **Expansion ARR** = $700,000 ($580k seat + $120k cross-sell).
- **GRR** = (2,160,000 − 180,000 − 300,000) / 2,160,000 = 1,680,000 / 2,160,000 = **77.8%**.
- **NRR** = (2,160,000 − 180,000 − 300,000 + 700,000) / 2,160,000 = 2,380,000 / 2,160,000 = **110.2%**.

**Read.**

- **NRR of 110% clears the Series-A bar.** Investable topline.
- **GRR of 77.8% is weak — below the mid-market ≥ 90% band.** The book is losing 22% of Starting ARR through the floor every year.
- **Expansion is doing heavy lifting.** $700k of expansion is compensating for $480k of downgrade + churn. If the expansion motion stalls even for one quarter, NRR collapses to the mid-80s.

**The verdict is legible in the decomposed numbers, not the headline.** Chapter 6 (churn diagnosis) is the next-quarter work — the team has to find out whether the 9 churned teams are voluntary (product mismatch → Chapter 6 exit surveys → route to product roadmap) or involuntary (payment failure → dunning programme). The mid-quarter 6 downgrades are the mod-102-Chapter-4 "leaky curve at the top" landing in the revenue book. Chapter 3's expansion motion is the reason the number reads as investable — but it is compensating, not compounding on a healthy floor.

Compare with a competing team that reports **NRR = 108% and GRR = 96%**. Same headline NRR band; entirely different underlying book. That team is compounding on a healthy floor; this team is compensating for a leaky one. The board pack has to say so.

## Common failure patterns

- **"NRR is 115%, we're great."** GRR unknown or unreported. See failure modes above.
- **Cohort not locked.** Starting ARR redefined mid-period; the number is not comparable to prior periods and not defensible in diligence.
- **Every movement in a single "renewal" bucket.** No decomposition, no diagnosis.
- **Multi-year contracts booked as year-one ARR.** Every downstream ratio inflated.
- **Expansion counted from new logos.** New logos are excluded from the cohort. Expansion is only from customers who were in the cohort at period start.
- **Involuntary churn silently included in voluntary.** Chapter 6 unpacks the fix.
- **Logo retention quoted as if it were revenue retention.** Small vs. large customer weighting missed.
- **Currency / pricing changes not normalised.** Artificial expansion / downgrade.
- **Aggregate-only, no segment decomposition.** Enterprise cohort strong, SMB cohort collapsing; the mid-tier number hides both facts.

## Summary

- **GRR is the churn floor** — Starting ARR minus downgrade minus churn, over Starting ARR. Capped at 100%.
- **NRR adds expansion** — GRR plus Expansion ARR / Starting ARR. Not capped. NRR ≥ 100% at Series-A is the modern working benchmark.
- **Report both together.** NRR without GRR hides whether a book is compounding on a healthy floor or compensating for a leaky one.
- **Lock the cohort at period start.** New logos are excluded from both metrics; the four movements (new, expansion, downgrade, churn) must fully decompose every ARR change in the cohort.
- **Segment the roll-up.** Aggregate NRR/GRR hides ARR-tier, cohort-year, and product-line facts that dominate operating decisions.
- **Common failure modes are metric-integrity failures** — cohort drift, undecomposed movements, involuntary-churn folded into voluntary, multi-year paper as year-one ARR. Each is diligence-visible; fix them in-house first.
- **The Chapter 3 expansion motion is what puts the "N" in NRR** — it is the specific programme that keeps NRR above GRR (and above 100%) even when the churn floor is imperfect.
