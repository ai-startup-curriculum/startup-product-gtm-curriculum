# CAC — Fully-Loaded and Per-Channel

## Motivation

Ask a founder what their CAC is and you will usually get one of four numbers back — and the four are rarely within 30% of each other. Some founders quote paid-media-spend ÷ paid-signups; some quote (paid + tools) ÷ new logos; some quote everything-called-marketing ÷ new logos; a few quote a blended founder-outbound-included number that averages a $200 self-serve signup with a $40,000 enterprise-pilot land.

None of these is wrong in a moral sense, but only one of them is the number an outside underwriter will reconstruct in diligence, and none of them by itself is the number a founder can use to decide what channel to invest in next month. The operator's CAC has to be **fully-loaded** (everything actually spent to acquire, not just the visible line items) and **per-channel** (never blended across channels with materially different economics). This chapter fixes both.

The failure mode this chapter exists to catch: **a founder scales the paid channel on the strength of a blended CAC that quietly averages founder-outbound leads (which cost effectively $0 in media but hundreds of hours of founder time) with paid-acquired leads (which cost $12,000 in media each) — discovers six months later that the paid channel alone is at $18k CAC on an $850/mo ARPU product, and has to defund the channel and lay off the SDR team hired to feed it.**

## Core concepts

### The formula — and the four things that go in the numerator

**CAC = (sales spend + marketing spend, in a period) ÷ (new logos acquired in the same period)**.

The formula is simple. The interpretation is where founders diverge, and every real-world CAC computation is a set of choices about the numerator (what counts as sales and marketing spend) and the denominator (which logos count, and over what period).

The **fully-loaded numerator** includes, at minimum:

1. **Sales headcount.** Fully-loaded compensation (base + variable + benefits + payroll taxes + equity value if you are being complete) for every sales person, sales-adjacent (BDR / SDR / RevOps), and the fraction of the founder's own time spent selling. Founder-selling time is the most-often-omitted item and is often the largest.
2. **Marketing headcount.** Fully-loaded compensation for every marketer, product-marketer, content, ops.
3. **Program spend.** Ad platforms (LinkedIn, Google, Meta, publisher direct), sponsorships, events, agencies, content-production, PR, SEO tooling, ABM platforms.
4. **Sales tooling and enablement.** CRM (HubSpot, Salesforce), sales engagement (Outreach, Apollo), call intelligence (Gong, Chorus), data (ZoomInfo, LinkedIn Sales Nav), enablement platforms.

The **denominator** is the count of **new-logo customers** (not the count of new logos + expansion; expansion is `mod-109` and does not belong in the CAC denominator) acquired in the same period as the numerator. Match the period exactly — if you sum quarterly S&M spend, divide by quarterly new logos, not annualised.

The output is a **dollar-per-new-logo** number, and the interpretation depends on the ACV of that logo. A CAC of $15,000 is investable on an $80,000 ACV enterprise product and unrecoverable on a $600 ARR SMB product; the raw number carries no verdict without the ACV context.

References that anchor this treatment: [David Skok — "SaaS Metrics 2.0"](https://www.forentrepreneurs.com/saas-metrics-2/) and [David Skok — "CAC: A Spotlight on the Most Important Metric"](https://www.forentrepreneurs.com/saas-metrics-2/); [OpenView — SaaS Benchmarks](https://openviewpartners.com/expansion-saas-benchmarks/); [Jason Lemkin / SaaStr — CAC benchmarks archives](https://www.saastr.com/); [KeyBanc — SaaS Survey](https://www.key.com/businesses-institutions/industry-expertise/key-technology-group.html).

### The founder-time trap — the biggest missing line item

The largest omitted cost in a naïve CAC computation is almost always **the founder's own selling time.** At PRE-SEED / SEED, the founder is often the only salesperson, and her time has to be counted or the CAC number is fictitiously low.

There are two defensible ways to count founder-time in CAC. Pick one; document it; be consistent:

- **Opportunity-cost salary.** Assign the founder a market-rate salary for a comparable head-of-sales role (say $200k base + $200k variable + benefits = ~$450k fully-loaded), pro-rate by the fraction of her time spent selling, and include in the numerator. This is the version an outside underwriter will use.
- **Actual comp + equity.** Use the founder's actual paid compensation, plus a per-year equity accrual. This tends to under-count because founders are notoriously undercompensated relative to market; it is defensible only if paired with an explicit note that CAC will *rise* the moment the founder is replaced with a market-comp AE.

Either is defensible; **quietly excluding founder-time is not.** A CAC number that excludes founder-time and is then used to justify "we can hire an AE at $180k base and CAC will not move" is quantitatively wrong at the arithmetic level. The AE's comp does not add to the CAC; it *replaces* the founder-time that was previously implicit. If founder-time was implicitly $0, replacing it with an AE at $200k adds $200k of visible cost with no offsetting cost reduction.

Pete Kazanjy's [*Founding Sales*](https://foundingsales.com/) treats this trap explicitly. Every founder-led-sales handoff to the first AE (Chapter 6) has to model the transition against a *founder-time-included* CAC baseline, not the naïve one.

### Fully-loaded vs. blended-media CAC — a worked pair

Startup with three GTM channels at Series-A. One-quarter spend and new-logo counts:

| Line item | Quarterly cost |
|---|---|
| Founder selling time (60% of $450k fully-loaded ÷ 4) | $67,500 |
| First AE fully-loaded ($240k / 4) | $60,000 |
| Marketing manager fully-loaded ($200k / 4) | $50,000 |
| LinkedIn ads (paid channel) | $90,000 |
| SEO / content freelancer | $18,000 |
| CRM + sales tooling (HubSpot + Outreach + Gong) | $12,000 |
| Data (ZoomInfo, Apollo, LinkedIn Sales Nav) | $9,000 |
| Sponsorship of one industry event | $25,000 |
| **Total quarterly S&M spend (fully-loaded)** | **$331,500** |

New logos acquired that quarter: 42.

**Fully-loaded CAC = $331,500 / 42 = $7,893.**

**Blended-media-only CAC (a common founder shortcut) = ($90,000 + $18,000 + $25,000) / 42 = $3,167.**

A **2.5× difference** between the two computations. The fully-loaded number is the number an outside underwriter will use; the blended-media-only number is the number that leads the founder to conclude "our CAC is great, let's spend more on paid." The moment the founder tries to *scale* on the media-only number, she discovers that scaling paid does not proportionally reduce the founder-time and sales-headcount lines, and the fully-loaded CAC does not fall the way the media-only number would predict.

**Report the fully-loaded number as the headline.** Report the media-only number only as a diagnostic (see per-channel below), and only ever alongside the fully-loaded headline.

### The per-channel decomposition — where the operator decision lives

A single headline CAC hides which channel to defund and which to double. The operator CAC is always decomposed **per channel**, where "channel" means one of the acquisition-source primitives from [mod-108](../mod-108-demand-generation-and-channels): founder outbound, first-AE outbound, paid search, paid social (LinkedIn / Meta), SEO / content, partnerships, community, events, referral.

For each channel, compute a channel-specific CAC:

- **Numerator (channel-specific):** the sales and marketing spend attributable to that channel. This is where the exercise gets sticky — some costs are unambiguously channel-specific (LinkedIn ad spend is 100% LinkedIn); some are partially attributable (the AE's time is split across outbound, inbound-response, and closing; RevOps supports all channels); some are joint costs (CRM, data platforms) that get allocated pro-rata to touched-logo count or to volume.
- **Denominator (channel-specific):** new logos where that channel was the primary source. Multi-touch attribution is a rabbit hole; at the operator cadence, primary-touch (or first-touch, if the CRM captures it) is defensible. Document the rule and be consistent.

Return to the worked example. Suppose the 42 new logos decompose as: **18 from founder outbound, 12 from first-AE outbound, 8 from LinkedIn ads, 3 from SEO / content, 1 from the event.** Approximate channel-specific fully-loaded CAC:

| Channel | Attributable spend | New logos | Channel CAC |
|---|---|---|---|
| Founder outbound | $67,500 (founder time) + $9,000 (data) × 0.5 + $6,000 (tooling) × 0.3 | 18 | ~$4,200 |
| First-AE outbound | $60,000 (AE) + $9,000 × 0.3 + $6,000 × 0.3 | 12 | ~$5,375 |
| Paid (LinkedIn) | $90,000 + $50,000 × 0.4 (mkt time) + $6,000 × 0.2 | 8 | ~$14,050 |
| SEO / content | $18,000 + $50,000 × 0.4 + $6,000 × 0.1 | 3 | ~$12,867 |
| Event | $25,000 + $50,000 × 0.2 + $6,000 × 0.1 | 1 | ~$35,600 |

*(These allocations are illustrative; the actual attribution rule needs to be documented and enforced consistently.)*

**The blended $7,893 hid an order-of-magnitude spread across channels.** Founder outbound is producing at $4.2k CAC; paid is producing at $14k CAC; the event produced one logo at $35.6k CAC. On an ACV of $12,000, the founder-outbound channel is highly investable; the paid channel is a losing motion; the event was an experiment that produced one logo and does not repeat.

**This is what the per-channel decomposition is for.** The operator decision — where to spend next month's incremental dollar — is not visible in the blended number and is obvious in the per-channel table.

### The two-part discipline — channel-market fit ⇒ CAC ⇒ decision

Chapter 2 of [mod-108](../mod-108-demand-generation-and-channels) taught you to run channel-market-fit diagnosis before scaling any channel. Per-channel CAC is what makes that diagnosis quantitative at the operator cadence.

- **Channel-market fit failing → per-channel CAC rising with spend.** The channel is not scaling on its own economics; you are spending more to acquire the marginal customer. Defund or diagnose.
- **Channel-market fit holding → per-channel CAC flat or falling with spend.** The channel is scaling on its own economics; the marginal customer costs the same (or less) than the average. Invest.
- **Channel producing at ~10× the price of another channel with equal LTV** → obvious re-allocation opportunity.
- **Channel producing at 3× the price of another channel but higher-LTV segment** → not obvious; requires the LTV/CAC read of Chapter 3, per-channel.

The per-channel CAC is a *diagnostic* for the mod-108 channel-market-fit read, and a *decision input* for the "where does the next dollar of S&M spend go?" allocation problem. Both matter.

### The three sub-flavours of CAC — CAC, Paid CAC, Blended CAC

Practitioner writing (Skok, OpenView, First Round) sometimes distinguishes three flavours of CAC. Know the vocabulary:

- **CAC (fully-loaded, all-in).** The formula above. The headline number. Reported per-channel and blended-across-channels.
- **Paid CAC.** Cost per new logo *from paid channels only* — paid channel spend ÷ paid-channel new logos. Distinct from "blended-media-only CAC" in the worked pair above; that was media-cost-only ÷ *all* logos, which is nonsensical. Paid CAC is a legitimate diagnostic — it isolates the paid engine's economics from the founder-outbound / organic contributions.
- **Blended CAC.** The all-channels-averaged fully-loaded number. Useful for company-level trend, useless for channel allocation decisions.

The rule: report **fully-loaded per-channel** as the operating number; report **fully-loaded blended** as a summary; report **paid CAC** as a diagnostic on the paid engine. Never report **blended-media-only** because it averages the visible cost of paid across all logos, most of which came from channels with different economics.

### Benchmarks by ARR band and motion type

There is no single "SaaS CAC benchmark." The applicable benchmark depends on the ARR band (SMB / mid-market / enterprise), the motion type (PLG / SMB self-serve / mid-market AE / enterprise multi-threaded), and the vintage of the report. Practitioner ranges commonly cited (as directional, not verdicts):

- **PLG self-serve (SMB, low ACV).** CAC often in the low hundreds to low thousands of dollars per logo; the LTV/CAC test is what qualifies whether the number is investable at a specific ACV.
- **SMB inside sales (ACV $2k–$15k).** CAC often in the $2k–$10k range; payback under 12 months is the working bar.
- **Mid-market AE (ACV $15k–$100k).** CAC often in the $8k–$40k range; payback under 18 months is the working bar.
- **Enterprise multi-threaded (ACV $100k+).** CAC often in the $50k–$300k range; payback under 24 months is the working bar; multi-year contract paper is common.

<!-- needs-research: pin specific CAC benchmark ranges by ARR band and motion type to the current OpenView / KeyBanc / SaaStr / Bessemer surveys; the ranges above are commonly-cited directional practitioner numbers and specific quantitative thresholds shift year-over-year. Reference: OpenView Expansion SaaS Benchmarks, KeyBanc SaaS Survey, Bessemer State of the Cloud. -->

Read benchmarks as directional. The load-bearing number is your per-channel CAC vs. your per-channel LTV (Chapter 3), read against the payback bar for your specific motion type. The benchmark bands are a sanity check on whether the specific numbers are in-band or so far out that something is likely mis-measured.

### The metric-integrity checklist

Before publishing a CAC number in the monthly one-pager, run the checklist:

1. **Fully-loaded numerator.** Sales headcount + marketing headcount + program spend + tooling + founder-time. Nothing missing.
2. **Same period on both sides.** Quarterly spend / quarterly new logos; monthly spend / monthly new logos. Not "quarterly spend / annualised logos."
3. **New logos only in denominator.** Expansion excluded (it belongs in NRR / mod-109), not in CAC.
4. **Per-channel decomposition.** At least the top three channels; the "other" bucket documented, not silent.
5. **Founder-time counted.** Either opportunity-cost salary or actual-comp-plus-equity — pick one and document.
6. **Attribution rule documented.** Primary-touch, first-touch, or a specific multi-touch model. Consistent across periods.
7. **Reconcilable to Stripe + payroll + ad platform.** Every line item traces to a system of record; a hostile question ("where did the $50k paid line come from?") has a same-day answer.
8. **Trend visible.** Trailing-3-month or trailing-6-month CAC alongside the current-quarter number. A CAC that is drifting up quarter-over-quarter is the signal Chapter 3 will read against payback.

## Concrete example — the code-review-tool CAC decomposition at Series-A

Return to the code-review tool from mod-109 Chapter 7. 240 mid-market teams paying, four active channels, ARPU $1,800/mo (ACV $21,600), Series-A funded, one first AE + one Head of CS + one marketing manager + the founder still actively selling.

Quarter under analysis: 2026-Q2.

**Numerator (fully-loaded S&M for the quarter):**

| Line item | Cost |
|---|---|
| Founder selling time (50% of $450k opportunity cost / 4) | $56,250 |
| First AE fully-loaded ($260k / 4) | $65,000 |
| Marketing manager fully-loaded ($200k / 4) | $50,000 |
| Head of CS (25% attributed to expansion sales / new-logo close support) | $17,500 |
| LinkedIn ads | $96,000 |
| SEO / content freelancer | $22,000 |
| CRM + sales engagement + call intelligence | $14,500 |
| Data (ZoomInfo, LinkedIn Sales Nav) | $9,500 |
| Sponsorship of DevTools Summit 2026 | $28,000 |
| **Total quarterly S&M (fully-loaded)** | **$358,750** |

New logos acquired 2026-Q2: 34.

**Blended fully-loaded CAC = $358,750 / 34 = $10,551.**

**Per-channel decomposition (with primary-touch attribution):**

| Channel | New logos | Attributable spend (approx) | Channel CAC |
|---|---|---|---|
| Founder outbound | 12 | $56,250 (founder) + $6,300 (tooling / data allocation) | ~$5,213 |
| AE outbound | 8 | $65,000 (AE) + $4,200 (tooling / data allocation) | ~$8,650 |
| Paid (LinkedIn) | 9 | $96,000 + $20,000 (mkt allocation) + $2,100 (tooling) | ~$13,122 |
| SEO / content | 4 | $22,000 + $17,500 (mkt allocation) + $1,050 (tooling) | ~$10,138 |
| Event (DevTools Summit) | 1 | $28,000 + $8,500 (mkt allocation) + $525 (tooling) | ~$37,025 |

**Read.**

- **Blended $10.5k hides an order-of-magnitude spread.** Founder outbound at $5.2k, paid at $13.1k, event at $37k.
- **Paid channel is above the mid-market working payback band on an ACV of $21.6k** (Chapter 3 will do the payback arithmetic; roughly, $13.1k CAC on $1,800/mo ARPU × 0.78 gross margin = 9.3-month payback, which is inside the band, but see below).
- **CAC has drifted from the Q1 2026 fully-loaded number of $8,900 up to $10,551 — a 19% quarter-over-quarter rise.** The drift is concentrated in the paid channel, whose CAC went from $9,800 (Q1) to $13,100 (Q2) as spend was scaled from $70k → $96k. **This is the mod-108 Chapter 2 channel-market-fit failure landing quantitatively in the CAC number.** The channel is not scaling on its own economics.
- **Founder outbound and AE outbound are producing at healthy channel CAC** — the mid-market outbound cohort from mod-109 Chapter 1 is still fit-holding, and per-channel CAC confirms it in a different instrument.

**Operator decision this quarter (fed into Chapter 5's monthly one-pager):**

- **Cap paid channel spend at Q1 level** ($70k/quarter) pending the mod-108 channel-market-fit audit; do not scale further until the CAC-vs-spend curve flattens or falls.
- **Continue funding founder outbound and AE outbound at current levels.** These are the fit-holding channels.
- **Do not repeat DevTools Summit.** $37k CAC on one logo is not investable at this ACV; the one deal was serendipitous.
- **Re-fund the SEO / content programme.** $10.1k CAC on 4 logos is in-band; the channel is scaling and content compounds — invest more.

This is what the per-channel fully-loaded CAC produces that the blended number cannot: a per-channel decision, with the specific dollar amount to change per channel, defensible against a hostile question.

## Common failure patterns

- **Blended-media-only CAC.** Media cost / all logos — averages the visible cost of paid across logos that mostly came from other channels. Nonsensical and flatters the number.
- **Founder-time silently excluded.** The largest single omission in most SEED-stage CAC computations. Chapter 6 will show why this trap collides with the first-AE hire decision.
- **Expansion in the denominator.** Expansion is `mod-109` NRR / GRR; it does not go in the CAC denominator. If you include it, both CAC and LTV get double-counted downstream.
- **CAC computed over one period and divided by logos from a different period.** Match the periods exactly.
- **Attribution rule undocumented.** "Primary-touch" and "first-touch" and "multi-touch weighted" all produce different numbers. Pick one, document, be consistent.
- **A single CAC without per-channel decomposition.** Cannot inform a channel allocation decision. Chapter 5 will reject a one-pager with only a blended CAC.
- **CAC quoted against the wrong benchmark band.** A mid-market motion's CAC compared to a public enterprise SaaS benchmark tells you nothing. Match ARR band and motion type.
- **CAC drift not tracked.** A rising CAC quarter-over-quarter is the specific signal that a channel has saturated. If you only report the point-in-time number without the trend, you miss the signal.

## Summary

- **CAC is (fully-loaded S&M spend) ÷ (new logos acquired in the same period).** Fully-loaded includes headcount, program spend, tooling, and founder-time.
- **Founder-time is the biggest missing line item at SEED / Series-A.** Count it as opportunity-cost salary or actual-comp-plus-equity; document the choice; do not silently exclude.
- **Per-channel decomposition is where the operator decision lives.** Blended CAC is a summary; per-channel CAC is a decision input. Report both, headline the per-channel table.
- **Three flavours in the vocabulary.** Fully-loaded (headline), Paid CAC (paid-only diagnostic), Blended CAC (summary). Never blended-media-only.
- **Benchmarks are per ARR band and per motion type.** Read as directional; the load-bearing test is per-channel CAC vs. per-channel LTV against the payback bar for the specific motion.
- **The metric-integrity checklist is eight items.** Run it before publishing.
- **CAC drift is a leading signal of channel saturation.** Track the trailing-3 or trailing-6-month CAC alongside the current-quarter number; a rising CAC is the mod-108 channel-market-fit failure landing in the operator dashboard.
