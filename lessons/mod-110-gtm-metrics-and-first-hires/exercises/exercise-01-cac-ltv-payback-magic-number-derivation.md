# Exercise 01 — CAC / LTV / Payback / Magic Number Derivation

**Estimated time:** 3 hours
**Chapter link:** [`02-cac-fully-loaded-and-per-channel.md`](../02-cac-fully-loaded-and-per-channel.md), [`03-ltv-payback-and-ltv-cac-ratio.md`](../03-ltv-payback-and-ltv-cac-ratio.md), [`04-magic-number-sales-efficiency-and-funnel-conversion.md`](../04-magic-number-sales-efficiency-and-funnel-conversion.md)
**Prerequisite reading:** [David Skok — "SaaS Metrics 2.0"](https://www.forentrepreneurs.com/saas-metrics-2/) (~30 min); [David Skok — "LTV: What It Is and How to Calculate It"](https://www.forentrepreneurs.com/ltv/) (~15 min); [OpenView — Expansion SaaS Benchmarks (most recent)](https://openviewpartners.com/expansion-saas-benchmarks/) (skim, ~20 min); [David Sacks — "The Burn Multiple"](https://sacks.substack.com/) (~10 min)

## Problem statement

Chapters 2–4 fixed the operator's four core efficiency numbers — CAC (fully-loaded, per-channel), LTV (cohort-based, gross-margin-adjusted), payback (in months, gross-margin-adjusted), and magic number (net-new ARR × 4 ÷ prior-quarter S&M) — and the composite (LTV/CAC ratio) that the underwriter reads first. This exercise makes you *compute all four correctly on a real (or realistic) book*, spot the failure modes founders trip on, and produce the per-channel decomposition an outside underwriter would demand.

You will:

1. Derive CAC, LTV, payback, LTV/CAC, and magic number by hand on a provided book that contains every Chapter 2–4 failure mode (founder-time excluded, blended-media-only, expansion in denominator, naïve LTV, uncapped horizon, gross-margin forgotten, same-period magic number). Fix each and produce the correct numbers.
2. Compute the same numbers for a real (or realistic hypothetical) book of your own — per-channel, per-segment, benchmarked, and read against the applicable benchmark bands.
3. Read the numbers against the benchmark bands and produce the one-paragraph verdict that would appear in section 7 of the monthly one-pager (Chapter 5 template).

The exercise trains the metric integrity a Series-B underwriter will demand — the exact decomposition, the exact segmentation, the exact benchmark call-out.

## Requirements

Deliver a folder `exercise-01/` with:

- `part-a-provided-book-fix.md` — the correction pass on the provided book, including a table of "what the founder reported" vs. "what the numbers should be after fix" and the specific failure mode each fix addresses.
- `part-b-your-book-derivation.md` — the CAC / LTV / payback / LTV/CAC / magic number derivation for a chosen startup, in the shape of monthly one-pager sections 2–4.
- Optionally: a spreadsheet with the per-channel decomposition (linkable from either write-up).

### Part A — Fix a broken efficiency report (75 min)

Below is a synthetic Series-A SaaS company's efficiency summary as reported by the founder to the board. Each number contains one or more Chapter 2–4 failure modes; your job is to identify each and produce the correct numbers.

**The founder's summary as reported:**

> "Q2 2026 efficiency snapshot:
> - CAC = $4,200 (marketing spend / new logos)
> - LTV = $84,000 (ARPU $1,400/mo × 60-mo average customer life)
> - LTV/CAC = 20× — best-in-class
> - Payback = 3 months
> - Magic number = 1.8 (same-quarter S&M-to-ARR)"

**The underlying detail:**

*Company context.* Mid-market B2B SaaS. ARPU $1,400/mo (ACV $16,800). Gross margin 74%. Two active sales channels (founder outbound + first AE) plus one paid channel (LinkedIn) plus SEO / content. Founder spent ~55% of time selling in Q2. First AE (hired Q1 2026) fully-loaded at $260k/yr. Marketing manager fully-loaded at $200k/yr. Head of CS at $220k (25% attributed to expansion sales, per Chapter 2). Founder opportunity-cost comp $450k/yr fully-loaded.

*Q2 2026 spend detail (fully-loaded):*

| Line item | Q2 cost |
|---|---|
| Founder selling time (55% × $450k / 4) | $61,875 |
| First AE ($260k / 4) | $65,000 |
| Marketing manager ($200k / 4) | $50,000 |
| Head of CS (25% attribution × $220k / 4) | $13,750 |
| LinkedIn ads | $84,000 |
| SEO / content freelancer | $18,000 |
| CRM + sales engagement + call intelligence | $13,500 |
| Data (ZoomInfo, Sales Nav) | $8,500 |
| Sponsorship of one conference | $22,000 |
| **Total fully-loaded S&M (Q2)** | **$336,625** |

Founder's numerator: $84,000 (LinkedIn) + $18,000 (SEO) + $22,000 (event) = $124,000 (marketing-only).

*Q2 2026 new-logo detail:*

| Channel | New logos (Q2) | Notes |
|---|---|---|
| Founder outbound | 11 | ACV $18,200 average |
| First AE outbound | 9 | ACV $17,100 average |
| Paid (LinkedIn) | 7 | ACV $15,400 average |
| SEO / content | 4 | ACV $17,900 average |
| Event | 1 | ACV $28,000 |
| **Total** | **32** | Blended ACV $17,100 |

Founder's denominator: 32 new logos + 8 expansion accounts = **40 "new-logo equivalents"**.

*LTV numerator:* Founder used ARPU $1,400/mo × 60-mo life = $84,000. Ignored gross margin. Used "60-month life" from a rule-of-thumb (not a cohort read; not verified against the mod-109 retention floor, which for this company is 89% monthly for the outbound cohort and 82% monthly for the paid cohort).

*Q1 2026 S&M spend (for magic-number denominator):* $285,000 fully-loaded.
*Q2 2026 net-new ARR:* $198,000 (new-logo ARR $547k + expansion $84k − downgrade $63k − churn $370k; the $370k churn line is 60% involuntary and the founder has not remediated it per the mod-109 Chapter 6 discipline).

**Structure your Part A write-up as:**

1. **Per-line failure-mode identification.** Table with rows for each of CAC, LTV, LTV/CAC, payback, magic number showing (reported number) → (correct number) → (failure modes at play).
2. **Corrected fully-loaded CAC.** Both blended and per-channel. Include founder-time. Exclude expansion from the denominator.
3. **Corrected cohort-based LTV.** Per-channel, using the mod-109 retention floors, gross-margin-adjusted, capped at 36 months.
4. **Corrected payback.** Per-channel, gross-margin-adjusted.
5. **Corrected LTV/CAC.** Per-channel; blended.
6. **Corrected magic number.** Using prior-quarter S&M; using net-new ARR (not gross); note the burn multiple as an additional read.
7. **Benchmark reads.** Per-channel numbers against the applicable mid-market benchmark bands.
8. **Verdict.** One paragraph — which channels are investable, which are not, what the operator decision is.

### Part B — Derive the efficiency numbers for a real (or realistic hypothetical) book (75 min)

Pick a startup — yours, one you know well, or the code-review-tool example from the chapters.

Deliver `part-b-your-book-derivation.md` in the shape of monthly one-pager sections 2–4:

1. **CAC section.** Fully-loaded S&M numerator (documented, per line item), new-logo denominator, blended and per-channel decomposition. Trend vs. prior 3 months if available.
2. **LTV / payback / LTV/CAC section.** Per-channel, cohort-based (link the mod-109 retention floor read), gross-margin-adjusted, capped 36 months. Trend if available.
3. **Efficiency ratios section.** Magic number (net, prior-quarter S&M), sales efficiency, burn multiple. Trend if available.
4. **Benchmark reads.** Per-channel numbers against the applicable benchmark bands for the ARR band and motion type. Cite the source of the benchmark.
5. **Verdict.** One paragraph — which channels are investable, which are not, what the operator decision this month is.

Length: 1–2 pages. Do not exceed 2. Mark hypothetical numbers as such and justify plausibility against the Chapter 2–4 benchmark ranges.

### Part C — Reflection (30 min)

A short closing paragraph:

- Of the Chapter 2–4 failure modes, which do you think would be most likely to slip through in your own book if you did not do the exercise? Why?
- Which piece of the numerator (CAC) or denominator (LTV) is hardest to get right for your specific business, and what instrumentation would make it easier?
- If a Series-B underwriter read your Part B write-up cold, what one question would you push on hardest? (Channel decomposition hidden? Founder-time excluded? Uncapped LTV? Same-period magic number?)

## Starter guidance

- Chapter 2's fully-loaded formula is the operating manual. Read the "formula" and "founder-time trap" sections end to end before starting Part A.
- Chapter 3's cohort-based LTV formula (Form 1, floor-based, capped at 36 months) is the recommended operator form. Use it.
- Chapter 4's magic-number formula (net, prior-quarter S&M) is the recommended operator form. Do not use the same-period, gross-only shortcut.
- For Part A, the failure modes to look for include (but are not limited to): founder-time excluded (biggest hidden cost); blended-media-only in the CAC numerator; expansion in the CAC denominator; naïve LTV with blended monthly churn; LTV without gross-margin adjustment; uncapped LTV horizon; magic number using same-period S&M instead of prior-quarter; magic number using gross ARR instead of net; involuntary churn not separated in the retention read that feeds LTV.
- For Part B, per-channel decomposition is 80% of the exercise. If your book is small enough that per-channel does not have enough logos for statistical significance, use "primary-source" categorisation and mark low-N channels as provisional.
- If hypothetical, use plausible-for-your-segment numbers. A per-seat SMB motion producing LTV/CAC = 12× on paid is not plausible; an enterprise multi-threaded motion with a 4-month payback is not plausible. Cross-check against Chapter 3's benchmark ranges.
- Do not skip the burn multiple. It is one number; it belongs on the one-pager; it is often the number the board asks about first.

## Acceptance criteria

Your submission is complete when:

- [ ] Part A identifies the specific failure mode(s) in every line of the founder's summary.
- [ ] Part A's corrected CAC is materially higher than the founder's $4,200 (the fully-loaded numerator and the new-logo-only denominator both push the number up).
- [ ] Part A's corrected LTV is materially lower than the founder's $84,000 (gross-margin adjustment, cohort-based-retention, and 36-month cap all push it down).
- [ ] Part A's corrected LTV/CAC is nowhere near the founder's 20×; it reveals the per-channel spread including a paid channel that is likely below the 3× working bar.
- [ ] Part A's corrected magic number uses prior-quarter S&M and net-new ARR; it is not 1.8.
- [ ] Part A includes per-channel decomposition (at least four channels).
- [ ] Part A's verdict paragraph names which channels are investable, which are not, and what the operator decision is.
- [ ] Part B has fully-loaded CAC numerator (with founder-time), per-channel decomposition, cohort-based LTV per channel, gross-margin-adjusted payback per channel, magic number (net + prior-quarter), and burn multiple.
- [ ] Part B's benchmark reads cite the specific source (OpenView, KeyBanc, Bessemer, SaaStr — with vintage year).
- [ ] Part B's verdict paragraph names channels-to-defund, channels-to-invest, and the operator decision.
- [ ] Part C reflection names a likely-to-slip failure mode, an instrumentation gap, and a hostile-underwriter question.

## Common ways this exercise goes wrong

- **Founder-time silently excluded in the corrected numerator.** The biggest single miss in Chapter 2. If your Part A corrected CAC does not include founder-time (either opportunity-cost or actual-comp), you have not applied Chapter 2's core discipline.
- **Blended CAC without per-channel decomposition.** Chapter 2's whole point. A per-channel table is a hard acceptance criterion.
- **LTV computed with naïve formula and blended monthly churn.** Chapter 3's whole point. Use cohort-based with the mod-109 retention floor.
- **LTV without gross-margin adjustment.** 20–40% overstatement. Cite gross-margin dollars.
- **Uncapped LTV horizon.** A 60-month or infinite-horizon LTV without a cap is a fundraising-view number, not an operator number. Cap at 36 months.
- **Magic number using same-period S&M.** Use prior-quarter — the causal timing dictates the lag.
- **Magic number using gross ARR.** Retention masks acquisition. Use net.
- **Payback in revenue terms, not gross-margin terms.** A 3-month revenue-payback is a 4-month gross-margin payback at 75%. Use gross-margin.
- **Benchmark citation without vintage.** "OpenView benchmark" without the year is not defensible; the numbers shift year-over-year.
- **Verdict without per-channel routing.** The whole payoff of the exercise is per-channel operator decision. Aggregate verdicts are not usable.
