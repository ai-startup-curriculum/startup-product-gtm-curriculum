# Exercise 01 — Cohort Retention Curve Read (Durability)

**Estimated time:** 3 hours
**Chapter link:** [`01-cohort-retention-as-pmf-durability.md`](../01-cohort-retention-as-pmf-durability.md)
**Prerequisite reading:** [Brian Balfour — "The Never Ending Road to Product/Market Fit"](https://brianbalfour.com/essays/product-market-fit) (~20 min); [Brian Balfour — "Retention is King"](https://brianbalfour.com/essays/retention-engagement-growth) (~20 min); [Amplitude — "The Amplitude Guide to Retention"](https://amplitude.com/blog/product-retention) (~30 min); [David Skok — "SaaS Metrics 2.0"](https://www.forentrepreneurs.com/saas-metrics-2/) (skim, ~20 min)

## Problem statement

mod-102 Chapter 4 taught you to read a cohort retention curve as a *diagnostic*. This exercise makes you read the same instrument as a *durability* signal — the ongoing monthly-cadence read that catches PMF drift in the newest cohort before the aggregate ARR line reflects it.

You will:

1. Read three provided cohort-over-cohort datasets and diagnose each — where the floor is drifting, which segmentation cut most likely explains the drift, and what the CAC / LTV consequence would be if the drift continues.
2. Build a durability read for a real (or realistic hypothetical) startup — cohort-over-cohort W12 (or Mn / Dk) plot, at least one root-cause segmentation cut, and the leaky-bucket arithmetic showing what the drift is costing.

The exercise trains the durability eye — the ability to see PMF loss landing in the newest cohort before the aggregate reveals it, and to state the CAC/LTV consequence in numbers a founder cannot dismiss.

## Requirements

Deliver a folder `exercise-01/` with:

- `part-a-provided-cohort-drift.md` — critiques of the three provided cohort-over-cohort datasets.
- `part-b-your-durability-read.md` — a full durability read for a chosen startup, in the shape of scorecard section 1.
- Optionally: `part-b-cohort-chart.png` or an ASCII rendering.

### Part A — Diagnose three provided cohort-over-cohort datasets (75 min)

For each dataset, produce a diagnosis in this structure:

1. **What does the cohort-over-cohort plot show?** (Flat / drifting down / drifting up / stepped / noisy.)
2. **What is the most likely root-cause cut?** (ICP tier / acquisition channel / product version / seasonal / segment mix shift.)
3. **What is the CAC / LTV consequence** if the drift continues at the observed rate for the next 4 quarters? Use the Chapter 1 arithmetic — express LTV, LTV/CAC, and monthly-churn-implied change.
4. **What would you segment on next** to confirm the root cause?
5. **What action would you route to?** One sentence, naming the module or programme (mod-108 channel-market fit, mod-104 ICP audit, Chapter 3 expansion motion investment, Chapter 5 activation programme, Chapter 6 dunning, etc.).

**Dataset 1 — a mid-market B2B SaaS, WAU, W12 retention by monthly cohort:**

```
Cohort start   n     W12 retention
2025-01        86       72%
2025-02        92       71%
2025-03        95       73%
2025-04       108       70%
2025-05       112       68%
2025-06       124       65%
2025-07       138       60%
2025-08       152       58%
```

Contextual note: the team scaled paid acquisition (LinkedIn Ads) from $8k/mo in 2025-03 to $32k/mo by 2025-08. No product-version changes shipped in the window. ARPU ≈ $1,800/mo; gross margin 78%; blended CAC ≈ $9,000 in 2025-01 and ≈ $11,500 in 2025-08.

**Dataset 2 — a consumer mobile productivity app, DAU, D30 retention by weekly cohort:**

```
Cohort start   n         D30 retention
2026-W01     11,200        18%
2026-W02      9,800        19%
2026-W03     10,400        22%
2026-W04     44,700        11%
2026-W05     51,200        10%
2026-W06     22,900        14%
2026-W07     18,300        16%
2026-W08     16,500        17%
```

Contextual note: 2026-W04 and W05 saw a viral moment (Product Hunt + a large TikTok mention). No product-version changes; no paid acquisition ramp.

**Dataset 3 — a mid-market vertical SaaS, MAU, M6 retention by monthly cohort:**

```
Cohort start   n     M6 retention
2024-Q3-01    42      88%
2024-Q3-02    48      87%
2024-Q3-03    51      86%
2024-Q4-01    56      85%
2024-Q4-02    62      84%
2024-Q4-03    58      74%   <-- step
2025-Q1-01    64      73%
2025-Q1-02    68      75%
2025-Q1-03    71      74%
```

Contextual note: an integration API endpoint the product depended on was deprecated by an upstream vendor in the second week of 2024-Q4-03; the team scrambled a fix but users saw a broken import flow for ~3 weeks. No ICP or channel shifts.

For each: full five-field diagnosis, one to two paragraphs.

### Part B — Durability read for a real (or realistic hypothetical) startup (90 min)

Pick a startup — yours, one you know well, or the running code-review-tool from the chapter.

Deliver `part-b-your-durability-read.md` in the shape of scorecard section 1:

1. **Cadence + rationale.** DAU / WAU / MAU and one sentence on why (per mod-102 Chapter 4).
2. **"Active" event.** The specific value-received action.
3. **Segmentation cuts.** Minimum three (ICP tier, acquisition channel, one other). For each, state the definition and the n.
4. **Cohort tables per segment.** W0, W1, W4, W12 (or D or M equivalents). Real if available; realistic hypothetical if not.
5. **Cohort-over-cohort roll-up plot.** The W12 (or equivalent) value sequenced by cohort date, at least 6 cohorts. This is the durability instrument.
6. **Drift verdict.** For each segment: floor holding / drifting / stepped. If drifting, root-cause hypothesis (channel mix, product change, ICP shift, seasonality).
7. **CAC / LTV consequence.** For the primary segment: compute LTV, LTV/CAC, and payback for the current floor and for the projected floor 4 quarters out if drift continues. Use the Chapter 1 arithmetic.
8. **Route.** One line naming the next action per drifting segment.

Length: 1–2 pages. Do not exceed 2. If hypothetical, mark clearly at the top and justify the plausibility of the numbers (Chapter 4 mod-102 benchmark ranges are the sanity-check).

### Part C — Reflection (15 min)

A short closing paragraph:

- Which dataset was hardest to root-cause and why?
- Which segmentation cut do you most often *not* have available in your own product data, and what would it take to instrument?
- If your Part B startup's cohort-over-cohort trend showed material drift, what founder-side conversation does the CAC / LTV arithmetic force that "let's fix retention later" would allow you to avoid?

## Starter guidance

- The cohort-over-cohort plot is what makes this a durability exercise vs. a diagnostic one. If you find yourself charting one long retention curve, you have gone back to mod-102 — pivot to the cohort-over-cohort roll-up.
- Dataset 1 is a channel-mix story. Dataset 2 is a viral-acquisition-cohort-fit story. Dataset 3 is a product-event story. Each requires a different remediation.
- The CAC / LTV arithmetic in Chapter 1 is the whole point of the drift verdict. A drift from 72% → 58% W12 is a specific dollar consequence; compute it. That number ends the "we'll fix it later" conversation.
- For Part B, if you cannot get product data with cohort tooling built in, the SQL patterns in the [Mixpanel retention docs](https://docs.mixpanel.com/docs/reports/retention) and [Amplitude guide](https://amplitude.com/blog/product-retention) work over any event table.
- If your startup is early enough that you do not have 6 cohorts yet, use realistic hypothetical numbers and mark clearly. The instrumentation and reasoning shape are the deliverable.
- Do not defend a segmentation cut you cannot instrument. If your product data does not distinguish acquisition channels at the cohort level, name that as a gap in the appendix rather than fabricating the split.

## Acceptance criteria

Your submission is complete when:

- [ ] Part A has full five-field diagnoses of all three provided datasets.
- [ ] Dataset 1's diagnosis names the paid-channel scale-up as the likely root cause and computes the CAC/LTV consequence with numbers.
- [ ] Dataset 2's diagnosis identifies the viral-moment cohorts (W04 / W05) as a different acquisition-mix cohort with lower fit, and recognises that the trend has partially reverted post-viral.
- [ ] Dataset 3's diagnosis identifies the integration-API deprecation as the root cause of the step, not a durability drift, and prescribes a product/eng route not a growth route.
- [ ] Part B is in scorecard-section-1 shape with cadence + rationale, active event, ≥3 segmentation cuts, per-segment cohort tables, a cohort-over-cohort roll-up plot, per-segment drift verdicts, CAC / LTV arithmetic on the primary segment, and per-segment routing.
- [ ] Part C reflection names the hardest root-cause, an instrumentation gap, and a specific "leaky curve is not a marketing problem" founder-conversation the arithmetic forces.

## Common ways this exercise goes wrong

- **Reading one aggregate curve.** The whole point of the durability read is cohort-over-cohort. If you charted one curve, you did the mod-102 exercise, not this one.
- **Missing the channel-mix story in Dataset 1.** The floor drop coincides with paid-channel scale-up. If you diagnose product regression, you have missed the cut.
- **Missing the viral-cohort acquisition-fit story in Dataset 2.** The W04/W05 cohorts are 4× larger than baseline and 40–50% lower in retention — classic viral-acquisition-cohort story.
- **Missing the product-event story in Dataset 3.** The step is instantaneous, not gradual — durability drift is gradual. Instantaneous steps are product/eng events.
- **Skipping the CAC / LTV arithmetic.** The dollar consequence is the whole point of the durability read for a founder. If you report "the floor is drifting" without the dollar-cost read, you have not made the case.
- **Part B numbers that violate benchmark sanity.** A 95% W52 retention on a consumer freemium app is not plausible; a 3% W12 on an enterprise SaaS is not plausible. mod-102 Chapter 4's benchmark ranges are the sanity-check.
- **No routing in Part B.** The whole payoff of the exercise is per-segment routing. Without it, you produced a chart, not a decision.
