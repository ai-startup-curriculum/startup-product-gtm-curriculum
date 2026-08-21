# Exercise 03 — Retention Curve Read and Critique

**Estimated time:** 3 hours
**Chapter link:** [`04-retention-curves.md`](../04-retention-curves.md)
**Prerequisite reading:** [Brian Balfour — "The Never Ending Road to Product/Market Fit"](https://brianbalfour.com/essays/product-market-fit) (~20 min); [Amplitude — "The Amplitude Guide to Retention"](https://amplitude.com/blog/product-retention) (~30 min); [Andrew Chen — "The Power User Curve"](https://andrewchen.com/power-user-curve/) (~15 min)

## Problem statement

Chapter 4 gave you the vocabulary. This exercise makes you *use it against real numbers*. You will:

1. Read four provided retention curves and diagnose each — cadence appropriateness, "active" definition critique, segment split necessity, flattening / decay / smile / frown / cliff, verdict.
2. Assemble a retention read for a real (or realistic hypothetical) startup — cohort correctly, segment correctly, plot correctly, write the one-paragraph verdict that would appear in the Chapter 7 scorecard's section 2.

The exercise trains the eye. A founder who can look at a cohort chart and *see* the shape — as opposed to reading the aggregate number — is much harder to fool.

## Requirements

Deliver a folder `exercise-03/` with:

- `part-a-provided-curves.md` — critiques of the four provided curves below.
- `part-b-your-retention-read.md` — a full retention read for a chosen startup, in the shape of scorecard section 2.
- Optionally: `part-b-cohort-chart.png` or an ASCII-art rendering if you want to include the visual in the read.

### Part A — Critique the four provided curves (60 min)

Below are four retention datasets. For each, produce a critique in this structure:

1. **What cadence is used?** Is it appropriate for the described product? If not, what should it be?
2. **What is "active" here?** Is it a good proxy for value received? If not, what would be?
3. **Does the pooled read tell you the right story, or does it hide a segment split?** If it hides one, describe what segmentation you would add.
4. **What shape is this curve?** (flattening, decay-to-zero, smile, frown, cliff.)
5. **Verdict.** One of: PMF signature in this segment, no-PMF signature, likely-PMF-hidden-by-mis-aggregation, insufficient data.
6. **What would you do next?** One-sentence route.

**Curve 1 — a WAU B2B code-review tool, pooled across all cohorts:**

```
W0: 100%
W1: 68%
W2: 51%
W3: 40%
W4: 33%
W6: 27%
W8: 24%
W12: 22%
```

(A footnote: the same team's mid-market segment retains at W12=70% and their small-team segment retains at W12=1%.)

**Curve 2 — a consumer mobile note-taking app, DAU cadence, active = "opened the app":**

```
D0: 100%
D1: 42%
D3: 28%
D7: 21%
D14: 18%
D30: 15%
D60: 14%
D90: 14%
```

(Product docs say most users only expect to open the app 1–2× per week.)

**Curve 3 — a monthly invoicing tool, MAU cadence, active = "sent ≥1 invoice":**

```
M0: 100%
M1: 74%
M2: 70%
M3: 68%
M4: 66%
M6: 65%
M9: 68%
M12: 71%
```

(The pool includes both trial and paid users; the tool has a 14-day free trial then a required paid conversion.)

**Curve 4 — a self-serve SaaS analytics product, WAU cadence, active = "logged in":**

```
W0: 100%
W1: 55%
W2: 40%
W3: 32%
W4: 27%
W6: 22%
W8: 20%
W12: 19%
```

(No segmentation available. The product is used by both individual contributors — who log in daily — and executives — who look at the dashboard weekly. Login = active is the only defined event.)

For each: full critique, one to two paragraphs.

### Part B — Retention read for a real (or realistic hypothetical) startup (90 min)

Pick a startup — yours, one you know well, or the running code-review-tool example from Chapters 3–4.

Deliver `part-b-your-retention-read.md` in the shape of scorecard section 2:

1. **Cadence and rationale.** Which cadence you picked (DAU/WAU/MAU) and one paragraph on why it matches your ICP usage pattern.
2. **"Active" definition and rationale.** The specific product event you chose, and one sentence on why it corresponds to value received rather than login.
3. **Cohort scheme.** How you cohort (by signup week? activation week?), how many cohorts you include, and how far back the earliest cohort extends.
4. **Segments plotted.** Enumerate the segments you break out (minimum three per Chapter 4's segment-first discipline). For each, state the segment definition and the n.
5. **Curves.** Actual retention numbers per segment (real if you have them, plausibly reasoned if hypothetical). At minimum W0, W1, W4, and W12 (or D or M equivalents). Delivered as a table or ASCII sparkline or plot.
6. **Verdict.** Per Chapter 4's five shapes — what shape is each segment? What does the aggregate look like and what does it hide?
7. **Chapter 6 route.** For each segment where a Chapter 6 mode fires from the retention shape alone, name the mode and the routing module.

Length: 1–2 pages. Do not exceed 2. If you do not have real data, mark clearly at the top that the numbers are hypothetical and justify their plausibility.

### Part C — Reflection (30 min)

A short closing paragraph:

- Which of your Part A critiques was hardest to make and why?
- Which shape did you find yourself under-recognising (people default to seeing decay-to-zero as PMF failure and miss the smile; people default to seeing flat as PMF and miss the frown)?
- If your Part B startup segment produced a PMF-signature curve, what would you *not* do next per Chapter 4's "leaky curve is a PMF failure, not a marketing failure" rule? Name the specific temptation you would resist.

## Starter guidance

- Chapter 4 is the operating manual. The three curves (PMF/no-PMF/smile) at the top of the "reading the curve" section are the shapes you should be able to name on sight.
- For Part A Curve 4 the "login = active" definition is the trap. Diagnose it explicitly; the answer to "what shape is this" is "the shape produced by a poor active definition; the true curve could be very different."
- If you use real product data, use whatever analytics you have (Amplitude, Mixpanel, Heap, Postgres). If your product data doesn't have cohort tooling built in, the [Mixpanel retention docs](https://docs.mixpanel.com/docs/reports/retention) and [Amplitude guide](https://amplitude.com/blog/product-retention) both show the SQL / query patterns.
- For hypothetical numbers in Part B, choose plausible-for-your-segment values. A W12 of 90% on a consumer freemium mobile app is not plausible; a W12 of 5% on a B2B enterprise tool is not plausible. Chapter 4's benchmarks are your sanity-check.
- The smile curve is real but rare in month-3 windows. If you spot a smile in your data, verify it is not a computation artifact (e.g. denominator narrowing because you only have data for old cohorts).
- Do not defend a shape you do not see. If the segment breakdown flattens the mid-market curve at 65% and the small-team curve is decay, resist writing "aggregate is flattening" — write "aggregate is misleading; mid-market is flattening at 65%, small-team is decay."

## Acceptance criteria

Your submission is complete when:

- [ ] Part A has full six-field critiques of all four provided curves.
- [ ] The Curve 2 critique catches the DAU-on-a-weekly-product mismatch and prescribes WAU.
- [ ] The Curve 4 critique catches "login = active" and prescribes a real value event.
- [ ] The Curve 1 critique acknowledges the pooled shape and prescribes segmentation, and can now be read as PMF-in-mid-market masked by pool.
- [ ] The Curve 3 critique catches the trial-vs-paid pooling and the emerging smile in months 9–12.
- [ ] Part B is in scorecard-section-2 shape with cadence + rationale, active event, cohort scheme, ≥3 segments plotted, per-segment shape verdicts, and per-segment Chapter 6 routing where a mode fires.
- [ ] Part C reflection names a hard call, a shape you under-recognised, and a specific "leaky curve is not a marketing problem" temptation you would resist.

## Common ways this exercise goes wrong

- **Reading the pooled Curve 1 as a legitimate flattening.** It is not — the mid-market segment is the flattening and the small-team segment is decay; the pooled 22% floor is an artifact.
- **Missing the DAU/weekly mismatch in Curve 2.** The 15% D30 looks catastrophic on a DAU curve; measured as WAU, the same underlying behaviour could easily be W4=45%. Cadence matters.
- **Ignoring the smile in Curve 3.** The uptick at months 9–12 is the signature of a monthly-workflow product where users deepen their usage; missing it means missing the strongest read available.
- **Accepting Curve 4's "logged in" definition.** Even if the numbers look bad, the diagnosis has to name the definitional problem first, not the shape.
- **Segments named but not defined.** "Enterprise vs. SMB" is not a segment definition; "Enterprise = ≥500 employees on annual contracts" is.
- **Part B numbers that violate benchmark sanity.** Chapter 4's benchmarks are approximate; producing numbers that would be impossible in the segment (99% W52 on a consumer freemium product) invalidates the read.
- **No routing in Part B.** The whole payoff of the exercise is that the retention shape routes to a module. A read without routing is a chart, not a decision.
