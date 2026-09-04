# Exercise 03 — Leading vs. Lagging Metric Drill

**Estimated time:** 2 hours
**Chapter link:** [`05-leading-vs-lagging-and-the-gtm-one-pager.md`](../05-leading-vs-lagging-and-the-gtm-one-pager.md)
**Prerequisite reading:** [Amplitude — North Star Playbook](https://amplitude.com/north-star) (skim the leading-vs-lagging section, ~20 min); [Sean Ellis and Morgan Brown — *Hacking Growth*](https://www.hackinggrowth.com/) (Chapter on north-star + inputs; ~30 min if you have the book, otherwise skim any Sean Ellis interview on the topic); [Winning by Design — writing on lagging vs. leading indicators](https://winningbydesign.com/) (search their blog / blueprints, ~15 min)

## Problem statement

Chapter 5's central discipline is that leading indicators live on the weekly and lagging indicators live on the monthly — because you *manage* leading indicators (they change *before* the outcome) and *react* to lagging ones (they describe an outcome that already happened). Getting this classification wrong is not cosmetic — it produces the pathology where a founder discovers on the third week of February that January's opportunity-creation rate collapsed in the second week of January, six weeks after the leak was diagnosable and fixable.

This exercise trains the classification muscle. You will:

1. Classify a list of 25 mixed GTM metrics as leading, lagging, or composite, and place each on the weekly, monthly, or "neither / defers up" cadence.
2. Take a broken "one dashboard" that mixes both cadences and rebuild it into the correct weekly + monthly split.
3. Diagnose two case snippets where an operator missed a leading signal because they were only reading the lagging one, and prescribe the specific leading indicator that would have caught it.

The exercise is short and mechanical on purpose — the classification is the point, and by the end you should be able to look at any GTM number and place it on the correct cadence without hesitation.

## Requirements

Deliver a folder `exercise-03/` with:

- `part-a-classification.md` — the 25-metric classification table.
- `part-b-dashboard-rebuild.md` — the broken dashboard split into weekly + monthly.
- `part-c-case-diagnoses.md` — the two case-snippet diagnoses.
- Optionally: a short reflection paragraph at the bottom of Part C.

### Part A — Classify 25 GTM metrics (40 min)

For each of the metrics below, produce a table row with four fields:

- **Metric.**
- **Leading / Lagging / Composite.** (Composite = a rollup of both, e.g., magic number.)
- **Cadence.** Weekly / monthly / quarterly / "defers up" (fundraising view, per Chapter 1's five-defers-up list).
- **One-line justification.** Why the classification and cadence.

The 25 metrics:

1. Opportunities created this week
2. Closed-won ARR (month)
3. Median inbound-MQL response time
4. GRR (T12M)
5. Magic number (net-new ARR ÷ prior-quarter S&M)
6. Demos held (this week)
7. Cohort W12 retention (latest cohort)
8. Pipeline coverage vs. quota multiplier
9. NRR (T12M)
10. AE quota attainment (Q3 forecast)
11. Rule of 40 (annual)
12. CAC (blended, month)
13. Multi-year LTV under a discount rate
14. Proposal-to-Close conversion rate (T6M baseline)
15. Number of active accounts touched by founder outbound (last 7 days)
16. Burn multiple (quarter)
17. Payback period (per channel, gross-margin adjusted)
18. Stalled deals count (no touch ≥14 days)
19. Discovery → Demo conversion rate (this month vs. baseline)
20. Total open pipeline $ARR (as of Monday)
21. Public-comparables valuation multiple
22. Involuntary-churn %  of total churn (T3M)
23. Net-new ARR (month)
24. Number of MQLs delivered by paid this week
25. Sales efficiency (New ARR ÷ S&M, same-period)

For each metric, if the correct verdict is *"belongs on the weekly one-pager"* say so; if *"belongs on the monthly one-pager"* say so; if *"defers up to `startup-finance-fundraising-curriculum`"* say so. A small number should go on the quarterly board pack only (a trailing-3-month rollup of a monthly number) — call those out too.

### Part B — Rebuild the broken dashboard (45 min)

Below is a synthetic "GTM Dashboard" that a Series-A B2B SaaS founder built and reads once a week on Monday. It contains 12 metrics on one page.

> **StackFlow — GTM Dashboard (as read every Monday):**
>
> 1. Total ARR: $4.2M
> 2. Closed-won ARR this week: $18k
> 3. Net-new ARR (month-to-date): $87k
> 4. Blended CAC (T3M): $9,400
> 5. Per-channel CAC (last-completed month): outbound $7,100 / paid $12,800 / SEO $8,600
> 6. NRR (T12M): 118%
> 7. GRR (T12M): 82%
> 8. Cohort W12 retention (Q1 cohort): 68%
> 9. Magic number (T3M): 1.4
> 10. AE (Priya) forecast (Q3): 89% committed, 108% best-case
> 11. Pipeline coverage vs. Q3 quota: 4.8× (required for historic conv: 6.1×)
> 12. Number of demos held this week: 6 (target: ≥8)

Deliver `part-b-dashboard-rebuild.md` that:

1. **Names the failure mode.** One sentence: what specific pathology does "one dashboard read once a week" produce, per Chapter 5?
2. **Classifies each of the 12 metrics** into weekly, monthly, or "neither / defers up."
3. **Rebuilds a weekly one-pager** for StackFlow using only the metrics on the weekly cadence, plus any Chapter 5 template sections that are missing from the founder's dashboard (activity, per-rep breakdowns, per-channel opportunity creation, one-focus line). Where the founder's dashboard is missing a required section, name what should be there and, if you can plausibly infer, populate it; otherwise mark as `[gap — needs instrumentation]`.
4. **Rebuilds a monthly one-pager** for StackFlow using only the metrics on the monthly cadence, plus any Chapter 5 template sections that are missing (LTV / payback / LTV/CAC, sales efficiency, funnel conversion, retention segment split, headline read, one priority). Same gap-marking discipline.
5. **Names what's leftover.** Any of the 12 metrics that belongs on neither (e.g., something that defers up), with the reason.

**Constraint:** the rebuild must reproduce the Chapter 5 templates faithfully. If the founder's dashboard has no per-channel LTV, the monthly rebuild names the gap; do not silently drop the requirement.

### Part C — Case-snippet diagnoses (30 min)

Two short case snippets. For each, produce a one-paragraph diagnosis that:

- Names the specific *leading indicator* the operator was not watching.
- Names the specific *lagging indicator* they were watching that made them discover the problem too late.
- Prescribes the specific one-pager section (Chapter 5 template) that would have surfaced the leading signal.

**Case 1 — The disappeared paid channel.**

> Reviewer.io's founder Alex has been publishing a monthly one-pager since January that includes per-channel CAC for the last completed month. On July 3, 2026, Alex publishes the June 2026 monthly and notices: paid LTV/CAC has dropped to 0.78×, CAC has spiked to $13,122 (up from $9,800 in May), and only 9 logos closed from paid vs. 14 the prior month. In the retrospective, Alex discovers that in *the second week of May* the paid campaign's landing page had a broken CTA (mis-linked form) that was silently dropping ~60% of submitted MQLs. The bug was in production for six weeks before Alex saw the downstream CAC / logo-count damage.

**Case 2 — The stalled expansion motion.**

> A mid-market SaaS founder reads a monthly one-pager with NRR (T12M) at 118% and reports it healthy to the board every quarter. In Q3 2026, NRR drops to 108%. Diagnosis reveals that in *mid-Q2*, the Head of CS quietly stopped running the mod-109 Chapter 3 QBR-plus-expansion-conversation cadence with the top-50 mid-market accounts (because two accounts had complained about "too much CS attention"). The expansion pipeline dried up in Q2; the NRR read did not catch it until Q3 numbers rolled up.

For each case, the diagnosis paragraph should name (a) the specific leading indicator missing, (b) the specific lagging indicator that caught the problem too late, and (c) the specific section of the weekly one-pager or monthly one-pager that would have surfaced the leading signal earlier. Reference Chapter 5's template sections by name.

### Reflection (10 min, at the bottom of Part C)

One short closing paragraph:

- Of the 25 metrics in Part A, which was hardest to classify and why? (Common candidates: pipeline coverage, forecast committed, involuntary-churn %.)
- In your own book, which leading indicator do you currently *not* track that this exercise convinced you to add?
- Which lagging indicator do you currently over-weight relative to the leading equivalent, and what is the cost of that over-weighting in weeks-of-late-discovery?

## Starter guidance

- The Chapter 5 test for leading vs. lagging is simple: does the number *change before* the outcome it predicts? Opportunities created this week change before next month's closed-won ARR — leading. CAC describes spend and acquisition that have already happened — lagging.
- Composite numbers (magic number, sales efficiency, burn multiple, LTV/CAC) are rollups of both. Treat them as lagging for cadence purposes — they belong on the monthly.
- The five "defers up" categories from Chapter 1 are: multi-year LTV under a discount rate; payback sensitivity across scenarios; projected multi-quarter runway; public-comparables valuation multiples; Rule of 40. If a metric on the list matches one of these, mark "defers up."
- Some metrics are technically operator-relevant but at the quarterly rather than monthly cadence — the board-pack extension. Call these out with "monthly rollup, board-pack read."
- For Part B, do not accept the founder's dashboard on its own terms. The exercise's point is to rebuild to the Chapter 5 discipline; if a required section is missing from the founder's dashboard, name the gap.
- For Part C, the leading indicator in Case 1 is the *weekly* MQL count from paid (Chapter 5 weekly template section 1). In Case 2, it is the *weekly* count of QBRs held / expansion conversations held with the top-50 accounts (a mod-109 Chapter 3 input tracked on the weekly). The lagging-only pathology is the whole point; naming the specific weekly instrument is the remedy.

## Acceptance criteria

Your submission is complete when:

- [ ] Part A has all 25 metrics classified with cadence and one-line justification.
- [ ] Part A correctly places all pure-activity metrics (opportunities created, demos held, MQL response time, accounts touched, MQLs delivered, stalled deals) on the weekly cadence.
- [ ] Part A correctly places all CAC / LTV / payback / retention / NRR / magic number / burn multiple / sales efficiency / funnel-conversion metrics on the monthly cadence.
- [ ] Part A correctly places the multi-year LTV under discount rate, public-comparables valuation multiple, and Rule of 40 as "defers up" (or "board-pack-only" for Rule of 40 if you prefer).
- [ ] Part B names the "one dashboard read once a week" pathology explicitly.
- [ ] Part B's weekly rebuild follows the Chapter 5 five-section template, includes activity per-rep, per-channel opportunity creation, and a one-focus line — with `[gap]` marks where the founder's dashboard is missing data.
- [ ] Part B's monthly rebuild follows the Chapter 5 seven-section template, includes per-channel CAC / LTV / LTV/CAC, retention segment split, funnel conversion vs. baseline, headline read, and one falsifiable priority — with `[gap]` marks as needed.
- [ ] Part C's Case 1 diagnosis names weekly MQL-count-from-paid (or equivalent) as the leading indicator and cites the Chapter 5 weekly template section that would have surfaced it.
- [ ] Part C's Case 2 diagnosis names weekly count-of-expansion-conversations (or equivalent) as the leading indicator and cites the specific weekly-instrument the founder was missing.
- [ ] Reflection names a hardest-to-classify metric, a leading indicator to add, and a lagging indicator over-weighted with a cost in weeks.

## Common ways this exercise goes wrong

- **Classifying pipeline coverage as lagging.** Pipeline coverage is a *pipeline-state* number as of a point in time; it changes as opportunities are created and closed. Weekly.
- **Classifying magic number as leading.** Magic number is a ratio of lagging numbers (net-new ARR and prior-quarter S&M). Lagging composite; monthly.
- **Classifying Rule of 40 as monthly.** Rule of 40 is a lagging composite of two lagging numbers (growth + margin), both already on the monthly. Board-pack rollup or defers up; not the monthly one-pager.
- **Missing the "defers up" bucket.** Multi-year LTV under discount rate is not a monthly-one-pager number. Chapter 1's boundary; enforce.
- **Rebuilding the dashboard as one page with a "leading" section and a "lagging" section.** Chapter 5 is unambiguous: two cadences, two artifacts. Not one artifact with two sections.
- **Dropping required Chapter 5 template sections because "the founder didn't have them."** The exercise is to rebuild to the discipline; if the founder is missing sections, name the gaps, do not silently drop them.
- **Case 1 diagnosis blaming the founder for "not checking paid weekly."** The failure mode is structural — the founder's dashboard had no weekly section for paid-channel MQL count. Name the structural gap, not just the personal miss.
- **Case 2 diagnosis proposing a lagging fix (raise NRR alert threshold to catch it faster).** The remedy is a leading instrument (weekly count of expansion conversations), not a tighter lagging read.
- **Skipping the reflection.** The reflection is where the classification muscle transfers to your own book; it is the load-bearing paragraph of the exercise.
