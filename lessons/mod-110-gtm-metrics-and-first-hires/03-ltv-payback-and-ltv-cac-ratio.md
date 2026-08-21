# LTV, Payback, and the LTV/CAC Ratio

## Motivation

CAC (Chapter 2) tells you the price of a customer. **LTV tells you the value.** The ratio of the two — LTV / CAC — is the single most-quoted composite in SaaS underwriting and the most-often-mis-computed number on a founder's spreadsheet. **Payback period** — the months to recover CAC at gross-margin dollars — is the same relationship expressed at the operating cadence and is the number the founder actually uses to decide whether next month's spend is affordable.

The tension this chapter fixes: it is very easy to compute a comfortable-looking LTV using the wrong denominator (blended monthly churn) and the wrong numerator (blended monthly ARPU), get a big number, divide by CAC, and conclude the motion is investable. It is much harder — and much more informative — to compute a **cohort-based LTV** using the [mod-109](../mod-109-retention-expansion-and-growth-loops) retention floor and gross-margin-adjusted ARPU, and read that against a **per-channel CAC** from Chapter 2.

The failure mode this chapter exists to catch: **a founder reports LTV = $52,000, CAC = $8,000, LTV/CAC = 6.5×, and scales the paid channel and the AE team on the strength of that ratio — discovers a year later that the LTV was blended-ARR-÷-blended-monthly-churn (mathematically comfortable, operationally meaningless), the actual cohort-based LTV for the paid channel is $14,000 (because paid-acquired cohorts retain 40% worse), the per-channel LTV/CAC for the paid channel is 1.0×, and the growth she funded burned $2M with nothing durable to show.**

## Core concepts

### The naïve LTV formula and why to abandon it at Series-A

The introductory textbook LTV formula is:

```
LTV_naive = ARPU × Gross Margin / Monthly Churn Rate
```

At SEED, when you have three months of data and a small book, this formula is defensible as a *directional* number. At SERIES-A, when you have enough cohort data to read a retention floor and enough revenue data to segment by ARR tier and acquisition channel, the naïve formula silently averages away the specific facts that matter.

Three specific ways the naïve formula lies:

1. **"Monthly churn rate" is usually blended.** A monthly logo churn of 3% might be 1% in the enterprise cohort and 6% in the SMB cohort. The blended LTV under a 3% churn is a number that describes no cohort accurately — every LTV/CAC decision made against it is a decision against a fictional customer.
2. **ARPU is usually blended.** ARPU averaged across an $8,000 ACV SMB customer and a $120,000 ACV enterprise customer is a number nobody actually pays.
3. **Retention is often not steady-state.** The naïve formula assumes a constant monthly churn extending indefinitely. Real cohorts have a steep-then-flat retention curve — most of the churn happens early, then the retained cohort holds for years. Applying a "monthly churn" pulled from the churn happening in month 1 across a decade of "expected" LTV mis-projects both directions.

David Skok, Balfour, and the OpenView / SaaStr practitioner canon converge on the recommendation: **at Series-A, replace the naïve LTV with a cohort-based LTV.** ([Skok — "SaaS Metrics 2.0"](https://www.forentrepreneurs.com/saas-metrics-2/); [Skok — "LTV: What It Is and How to Calculate It"](https://www.forentrepreneurs.com/ltv/); [Balfour — "Retention is King"](https://brianbalfour.com/essays/retention-engagement-growth)).

### The cohort-based LTV — the operator version

**Cohort-based LTV** integrates the actual retention curve of a specific cohort (segmented by ICP tier and acquisition channel), applied to the gross-margin-adjusted revenue per surviving customer, summed over the relevant horizon.

The formula (operator version):

```
LTV_cohort = Σ (Revenue_per_customer_in_period_t × Gross Margin × Survival_Rate_in_period_t)
             for t = 0 to horizon
```

At the operator cadence, you almost always simplify to one of two forms:

**Form 1 — Floor-based LTV (the recommended operator form).** Once the retention curve flattens (mod-109 Chapter 1), the survival rate settles at a floor. Approximate LTV as:

```
LTV_floor = ARPU_of_cohort × Gross Margin / (1 - Retention_Floor)
```

Where `Retention_Floor` is the per-period survival rate from the mod-109 durability read. Equivalent to the naïve formula but with two upgrades: ARPU is *cohort-specific* (not blended), and the retention denominator is the *floor of the curve* (not the blended monthly churn dominated by early-period drop-off).

**Form 2 — Sum-of-cohort-revenue (the discipline version).** If you have enough data, integrate the actual cohort curve period-by-period out to a chosen horizon (24, 36, 48 months). Sum the surviving-cohort revenue in each period. This is what a Series-B underwriter will do in diligence.

At the weekly / monthly one-pager cadence, Form 1 is enough. Form 2 belongs in the quarterly board pack or the fundraise model. Chapter 5 will fix which form goes in which artifact.

### The horizon question — where the fundraising view leaks in

The naïve formula (and Form 1 above) implicitly extends to infinity — a monthly churn of 2% implies a 50-month average life, integrated indefinitely. At the operator cadence, this is usually fine because the arithmetic dominates the horizon question — the discount rate from cost-of-capital only matters after year 3 or so, and the operator LTV is mostly determined by the first 24 months of cohort revenue.

**A common practitioner discipline: cap the LTV at a 36- or 48-month horizon** even in Form 1, because (a) it produces a more conservative number that survives a fundraise sceptic's push-back, and (b) it removes the ambiguity about "what discount rate did you use?" that the fundraising view is going to want to talk about. Skok explicitly recommends the horizon cap in his working writing.

The DCF-style LTV — with an explicit discount rate, terminal value, and multi-scenario sensitivity — is the fundraising view. Defers up to `startup-finance-fundraising-curriculum`. Do not put it in the monthly one-pager.

### Payback period — the operator's LTV

**Payback period is the number of months of gross-margin revenue required to recover CAC.**

```
Payback (months) = CAC / (ARPU_monthly × Gross Margin)
```

Read a specific example. CAC = $10,000. ARPU = $1,000/month. Gross margin = 80%. Payback = $10,000 / ($1,000 × 0.80) = **12.5 months.**

Payback is the *operator's* LTV because it is denominated in the currency that matters at the operator cadence: **months of runway.** A payback of 12 months means the CAC dollars spent this quarter come back as gross-margin dollars four quarters from now; a payback of 30 months means they come back after eight quarters, which is often longer than the funding runway. The founder who can quote payback and does not immediately know LTV/CAC is often making better operating decisions than the founder who quotes LTV/CAC but has to look up payback.

**The gross-margin adjustment is load-bearing.** A CAC of $10,000 on $1,000/mo ARPU without the gross-margin adjustment is a "10-month payback" — which is *revenue-payback*, not the operator number. The revenue is not what pays back the CAC dollars; the *gross-margin dollars* do. Every payback quote in the one-pager is gross-margin-adjusted or the ratio is misleading.

### The payback benchmark bands — by motion type

Practitioner working ranges, cited directionally:

- **PLG self-serve.** Payback often 6–12 months; the shorter the better; net payback (payback net of retention-driven ARR growth) is sometimes the working number.
- **SMB inside sales.** Payback under 12 months is the working bar.
- **Mid-market AE.** Payback under 18 months is the working bar.
- **Enterprise multi-threaded.** Payback under 24 months is the working bar; some multi-year contract businesses tolerate 30 months.

<!-- needs-research: pin specific payback benchmark bands by ARR band and motion type to the current OpenView / KeyBanc / Bessemer / SaaStr surveys; the ranges above are commonly-cited directional practitioner numbers and shift year-over-year. -->

The point at which payback becomes a hard problem is when it exceeds the effective *funding runway* — a 24-month payback on an 18-month cash runway means the CAC dollars spent this quarter are not going to come back before the next fundraise, which forces the raise to happen against S&M-heavy P&L. Not necessarily wrong, but a specific narrative choice.

### The LTV / CAC ratio — the composite the underwriter reads first

```
LTV/CAC = LTV_cohort / CAC (fully-loaded, matched channel)
```

The ratio is the composite that appears at the top of every Series-A / Series-B pitch's efficiency section. Practitioner working thresholds:

- **LTV/CAC ≥ 3× is the working bar for an investable SaaS motion.** Below 3× the motion is often not scalable at Series-B economics.
- **LTV/CAC ≥ 5× starts to look best-in-class**, though very high LTV/CAC (say 8× or 10×) sometimes indicates under-investment in acquisition — you are leaving growth on the table.
- **LTV/CAC < 1×** is unrecoverable — you are burning money on every customer.

<!-- needs-research: LTV/CAC bar of ≥3x is a widely-cited working threshold across Skok, OpenView, Bessemer, SaaStr — pin to a specific current-vintage source rather than folk knowledge; the specific quantitative threshold may shift with the funding environment. -->

The load-bearing discipline: **compute LTV/CAC per channel, not blended.** A blended LTV/CAC of 3.5× can be 6× in the founder-outbound channel and 1.2× in the paid channel. Chapter 2 argued this for CAC; the same argument holds for LTV/CAC, because CAC is one of the two inputs. Chapter 5 will require the per-channel LTV/CAC table in the monthly one-pager.

### The LTV/CAC ↔ Payback relationship

The two numbers are not independent — they are two views of the same relationship. The identity:

```
Payback (months) = 12 / Annual Revenue Per Customer × CAC / Gross Margin
LTV/CAC (steady-state, no discounting) = 1 / (Monthly Churn Rate × Payback Months / 12)
```

Roughly, **LTV/CAC ≈ 1 / (Churn × Payback in years)**. A motion with 12-month payback and 2% monthly churn has LTV/CAC ≈ 4.2×; a motion with 24-month payback and 3% monthly churn has LTV/CAC ≈ 1.4×.

**This is why the two numbers move together in the one-pager and why fixing one usually fixes the other.** A CAC-reduction that cuts payback from 24 to 12 months roughly doubles LTV/CAC at constant churn; a retention improvement that halves monthly churn also roughly doubles LTV/CAC at constant payback. The mod-109 "retention dominates CAC/LTV arithmetic" argument (Chapter 1 of mod-109) lives here — churn is the coefficient that determines whether growth compounds.

### Worked example — floor-based LTV, per-channel, gross-margin-adjusted

Two channels of a Series-A mid-market SaaS. ARPU (ACV / 12) is $1,800/month. Gross margin is 78%.

**Channel A — founder outbound.**

- Retention floor (mod-109 read): 92% monthly (i.e. 8% monthly churn on this cohort).
- Fully-loaded per-channel CAC (Chapter 2 read): $5,200.
- LTV (floor-based, capped at 36 months):
  - Approximate: $1,800 × 0.78 / 0.08 = **$17,550 uncapped**.
  - Sum-of-cohort at 36 months: roughly $1,800 × 0.78 × sum(0.92^0 + 0.92^1 + ... + 0.92^35) ≈ $1,800 × 0.78 × 11.94 ≈ **$16,760 capped**.
- Payback: $5,200 / ($1,800 × 0.78) = **3.7 months**.
- LTV/CAC (capped): $16,760 / $5,200 = **3.2×**.

**Channel B — paid (LinkedIn).**

- Retention floor: 87% monthly (13% monthly churn — the mod-109 Chapter 1 leaky-cohort argument for this channel).
- Fully-loaded per-channel CAC: $13,100.
- LTV (floor-based, capped at 36 months):
  - Approximate: $1,800 × 0.78 / 0.13 = **$10,800 uncapped**.
  - Sum-of-cohort at 36 months: $1,800 × 0.78 × sum(0.87^0 + ... + 0.87^35) ≈ $1,800 × 0.78 × 7.30 ≈ **$10,246 capped**.
- Payback: $13,100 / ($1,800 × 0.78) = **9.3 months**.
- LTV/CAC (capped): $10,246 / $13,100 = **0.78×**.

**Read:**

- **Blended-across-channels LTV/CAC would be ~2.1× — below the 3× working bar but not egregiously so.** Founders read this and often conclude "we need to work on efficiency."
- **Per-channel LTV/CAC reveals a very different picture.** Founder outbound at 3.2× is at the working bar; paid at 0.78× is **losing money on every paid-acquired customer** even before considering the leaky floor.
- **Payback per channel says the same thing in operator currency.** Founder outbound recovers CAC in under 4 months (working); paid recovers CAC in over 9 months but on a cohort that leaks — a fraction of paid-acquired customers will churn before recovering their CAC.
- **The operator decision falls out of the table:** stop scaling paid until the mod-108 channel-market-fit audit either improves the retention floor or reduces the CAC materially.

This is what per-channel LTV/CAC does that the blended number cannot. It is also what cohort-based LTV does that the naïve LTV cannot.

### The negative-margin trap and the horizon trap

Two subtler failure modes worth flagging:

- **Negative-gross-margin ARPU.** A company that is selling below cost (subsidised free tier, heavily-discounted anchor pricing, unit-economics-negative infrastructure product) has an LTV that is *literally negative* at the gross-margin level. No CAC produces recovery. The naïve formula hides this — divide by monthly churn and you get a big positive number as long as ARPU × gross margin is positive. **Always compute gross-margin dollars per customer per month first;** if that is negative or near-zero, LTV analysis is not the tool — [mod-106](../mod-106-pricing-and-packaging) pricing rework is.
- **The retention floor is not yet knowable.** For a young cohort (a few weeks or months old), the retention curve has not flattened yet. Extrapolating a floor from three data points produces a highly speculative LTV. If your cohorts are all young, mark LTV as "provisional" and report **payback** as the primary efficiency number — payback is a same-month observable, not a projection.

### Segment mixing — where LTV/CAC ratios hide the real business

Same rule as mod-109 Chapter 1: an aggregate LTV/CAC hides segment-level facts that dominate operating decisions.

- **Enterprise vs. mid-market vs. SMB.** Enterprise typically has higher CAC and much higher LTV; SMB the reverse. A blended LTV/CAC of 3.5× can be 6× in enterprise and 1.4× in SMB. Reporting only the blended number hides the "we should stop selling to SMB" or "we should double down on enterprise" decision.
- **Cohort year / vintage.** LTV improves as retention curves lengthen and more real data replaces projection; CAC often rises as easy channels saturate. A 2023-cohort LTV/CAC is not the 2025-cohort LTV/CAC.
- **Channel — the Chapter 2 argument, repeated.** A per-channel LTV/CAC is the operator-decision-relevant number. A blended is a summary.

**A monthly one-pager that reports LTV/CAC as a single number without per-channel and per-segment cuts fails the operator-view discipline.** Chapter 5 will enforce this in the template.

## Concrete example — the code-review-tool LTV / Payback / LTV/CAC

Continue the code-review tool from Chapter 2. ARPU $1,800/mo (ACV $21,600), gross margin 78%, four channels active.

From mod-109 Chapter 1 retention read: mid-market outbound-acquired cohort retention floor ≈ 92% monthly; paid-acquired cohort retention floor ≈ 87% monthly; enterprise pilots retention floor ≈ 82% (with a much higher initial drop).

Per-channel LTV (floor-based, 36-month cap), payback, LTV/CAC:

| Channel | CAC | Floor | LTV (capped) | Payback (mo) | LTV/CAC |
|---|---|---|---|---|---|
| Founder outbound | $5,213 | 92% mo | $16,760 | 3.7 | 3.2× |
| AE outbound | $8,650 | 92% mo | $16,760 | 6.2 | 1.94× |
| Paid (LinkedIn) | $13,122 | 87% mo | $10,246 | 9.3 | 0.78× |
| SEO / content | $10,138 | 90% mo | $13,900 | 7.2 | 1.37× |
| Event | $37,025 | (single logo, no floor read) | n/a | n/a | (n/a — one-shot) |

Weighted / blended: LTV ≈ $14,200; CAC $10,551; blended LTV/CAC ≈ 1.35×; blended payback ≈ 7.5 months.

**Read against benchmarks (mid-market motion):**

- **Blended LTV/CAC of 1.35× is far below the 3× working bar.** The Series-A investors will read this hard.
- **Founder outbound is at the working bar (3.2×) and healthy.**
- **AE outbound is below the bar (1.94×) but note the AE only just finished ramp; the CAC is fully-loaded against the newly-hired AE's still-low volume. The projected steady-state per-AE CAC (year-two of AE) is roughly $6,200, which produces LTV/CAC ≈ 2.7×.** A specific note the founder must make: the AE-cohort LTV/CAC is projected to improve, and the timeline for that projection is what triggers or delays the second AE hire (Chapter 6).
- **Paid at 0.78× is unrecoverable and the channel must be defunded or fixed.**
- **SEO / content at 1.37× is investable if the CAC comes down as the compounding content channel scales;** re-fund modestly and re-read next quarter.
- **Blended payback of 7.5 months is inside the mid-market ≤ 18-month band** — but the blended payback averages the 3.7-month founder-outbound channel with the 9.3-month paid channel. Per-channel is the read.

**Operator decision this month (Chapter 5 will collect these into the one-pager):**

- Defund paid channel to Q1 spend levels ($70k/qtr) pending the mod-108 channel-market-fit audit.
- Continue AE cohort with explicit "AE-cohort LTV/CAC re-read in Q4 2026 with steady-state CAC" callout.
- Re-fund SEO / content programme (invest more into the compounding channel).
- **Ratio between the founder-outbound LTV/CAC (3.2×) and the paid LTV/CAC (0.78×) is the specific quantitative reason to change the channel mix.** Chapter 5 will make this explicit in the one-pager.

## Common failure patterns

- **Naïve LTV with blended monthly churn.** The formula that flatters. Use cohort-based; use the floor from mod-109; segment by channel and ICP tier.
- **LTV without gross-margin adjustment.** Revenue-LTV overstates by 20–40%. Gross-margin dollars are what pays back CAC.
- **Uncapped horizon.** An infinite horizon LTV under a 2% monthly churn is not a defensible number in diligence. Cap at 36 or 48 months.
- **Blended LTV/CAC as the headline.** Per-channel is the operator-decision-relevant read. Blended is a summary.
- **Payback quoted in revenue terms, not gross-margin.** A 10-month revenue-payback is a 12.5-month gross-margin payback at 80% margin. Report gross-margin payback.
- **Payback ignored in favour of LTV/CAC.** LTV/CAC is the composite; payback is the operator-runway number. Report both.
- **LTV computed on a young cohort with no floor.** Extrapolating a floor from three data points is speculative. Mark as provisional; lean on payback until the floor lands.
- **Negative-gross-margin ARPU hidden inside a positive LTV.** Compute the gross-margin dollars first. If negative, pricing rework (mod-106) is the tool, not LTV analysis.
- **Channel-agnostic LTV/CAC in the monthly one-pager.** Chapter 5 will not accept it.

## Summary

- **Replace the naïve LTV formula with cohort-based LTV at Series-A.** ARPU is cohort-specific, gross-margin adjusted; the retention denominator is the mod-109 floor, not blended monthly churn.
- **Payback in months is the operator's LTV.** CAC / (monthly ARPU × gross margin). The number the founder uses to decide "can we afford next month's spend."
- **LTV / CAC ≥ 3× is the working bar for an investable SaaS motion.** Below 3× the motion is often not scalable at Series-B economics.
- **Compute LTV, payback, and LTV/CAC per channel.** The blended is a summary; the per-channel is the operator decision.
- **Cap LTV at 36 or 48 months for the operator read.** DCF-style discount-rate LTV is the fundraising view; defers up.
- **Payback and LTV/CAC are two views of the same relationship.** LTV/CAC ≈ 1 / (Churn × Payback in years). Fix one and the other moves.
- **Retention dominates the arithmetic.** A doubling of churn halves LTV; no CAC reduction compensates. This is the mod-109 leaky-bucket claim landing in the operator dashboard.
- **Watch the negative-gross-margin trap and the not-yet-flattened cohort trap.** Both invalidate LTV; both are common at SEED / Series-A.
