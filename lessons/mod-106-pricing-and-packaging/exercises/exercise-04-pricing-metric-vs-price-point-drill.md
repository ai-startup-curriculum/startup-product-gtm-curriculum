# Exercise 04 — Pricing Metric vs. Price Point Drill

**Estimated time:** 2 hours
**Chapter link:** [`04-pricing-metric-vs-price-point.md`](../04-pricing-metric-vs-price-point.md)
**Prerequisite:** Chapters 2 and 4 read end-to-end; Exercise 02's value equation and anchor price; Exercise 03's tier composition (or an equivalent three-tier structure); the mod-104 buyer / user / champion personas and the mod-107 planned sales motion (or a working assumption about it).

## Problem statement

Chapter 4 named the failure modes: copying the category leader's metric ("Slack charges per seat, so we will"); optimising the price point while the underlying metric is misaligned; picking usage without the metering infrastructure to bill it; picking outcome pricing without the attribution story; failing to align the metric with the sales motion; bloating the pricing metric with add-on line items. The remedy is a structured **metric-selection worksheet** — 4-5 candidate metrics evaluated against the four alignment tests, plus the derivation from the value equation, plus the sales-motion fit — that produces one primary metric with a written defence.

This exercise trains you to **evaluate at least four candidate pricing metrics against Chapter 4's four alignment tests, pick one primary metric, and author the metric-decision block** in the shape Chapter 6's pack requires. The output is the pricing-metric decision that goes into the pricing pack (Chapter 6 Section 2) and drives the pricing-page calculator design.

The failure mode this exercise exists to catch: **the founder picks the metric in 30 seconds ("everyone in our category charges per seat") and never runs the four-test worksheet. Two years later the metric is wrong, the customer's growth curve doesn't move it, and changing the metric requires rebuilding metering, contracts, and sales training simultaneously.**

## Requirements

Deliver a folder `exercise-04/` with:

- `part-a-candidate-metrics.md` — 4-5 candidate metrics enumerated with the derivation-from-value-equation reasoning.
- `part-b-four-test-worksheet.md` — every candidate scored against the four alignment tests + the sales-motion fit test.
- `part-c-metric-decision-block.md` — the metric decision + calculator design + failure-signal list in the shape Chapter 6 Section 2 requires.

### Part A — Enumerate candidate metrics (30 min)

Deliver `part-a-candidate-metrics.md`.

**A1 — Start from the value equation (10 min).** Restate Exercise 02's value equation in this shape:

```
Value = (baseline metric − improved metric) × cost per unit × frequency
```

Identify the **frequency variable** — the variable that determines "how much value the customer gets per unit of time." Common frequency variables per Chapter 4's derivation:

- PRs / year → per-repo (proxy).
- Queries / month → per-query.
- Deals / quarter → per-seller.
- Messages / month → per-message.
- Model inferences / month → per-inference / per-token.
- Incidents / quarter → per-monitored-service.

The frequency variable is the **first candidate** metric.

**A2 — List 4-5 candidate metrics (15 min).** Enumerate at least four candidate pricing metrics. Include:

- **The frequency-variable metric** from A1 (the value-equation-derived candidate).
- **The category-leader metric** (whatever the dominant competitor charges on — sanity check, but do not pick just because they do).
- **A per-seat / per-user variant** (if not already included).
- **A per-outcome variant** (even if you'll reject it, evaluate).
- **A hybrid** (per-seat base + per-usage overage, or per-tier base + per-metric expansion) — often the honest answer for mature B2B products with multi-persona buyers.

For each candidate, write two sentences: *what you charge for* and *the standard example* (a well-known product using this metric — no need to invent).

**A3 — Category / competitor context (5 min).** For each candidate, briefly note the observed use in your category — which competitors or adjacent-category vendors charge along this axis, and what price points they charge. If you don't know, flag `<!-- needs-research: competitor pricing on {metric} -->` rather than invent.

### Part B — The four-test alignment worksheet (60 min)

Deliver `part-b-four-test-worksheet.md`.

Score every candidate from Part A against Chapter 4's four alignment tests plus a sales-motion-fit test. Use a matrix:

```
Test                    | Candidate 1 | Candidate 2 | Candidate 3 | Candidate 4 | Candidate 5
------------------------|-------------|-------------|-------------|-------------|-------------
T1 — Value scaling      | pass/partial/fail + evidence
T2 — Growth vector      | ...
T3 — Estimability       | ...
T4 — Incentive align.   | ...
T5 — Sales-motion fit   | ...
```

Score each cell with:

- **pass / partial / fail.**
- **One-sentence evidence** — the specific reason the metric passes or fails this test for your product.

**B1 — Test 1: value scaling (10 min).** If the customer's value doubles, does the customer's bill approximately double under this metric? Cite the value equation from A1 as the reference. A metric that leaves the bill flat when value doubles fails; a metric that inflates the bill when value is flat also fails.

**B2 — Test 2: growth vector match (10 min).** As the customer's business grows, does the metric grow with it organically? What is the customer's natural growth vector in your ICP (headcount / repos / usage / accounts / transactions), and does the metric track it? A metric that requires a sales conversation for every increment is a metric that caps expansion.

**B3 — Test 3: estimability (10 min).** Can the buyer estimate her monthly bill within 15 minutes of understanding the metric, using inputs she knows off the top of her head? Per-seat is trivially estimable; per-event is often not. If not estimable, deals stall at the "how much will it cost me" step.

**B4 — Test 4: incentive alignment (10 min).** Does the metric reward the vendor for the customer *using the product more* (aligned) or for *minimising usage to control the bill* (misaligned)? Per-seat is aligned (customer's success = more users = more revenue); per-event can be mis-aligned (customer's success may involve reducing events); per-outcome is aligned when attribution works.

**B5 — Test 5: sales-motion fit (10 min).** Does the metric match the mod-107 planned sales motion?

- **PLG:** wants a metric a self-serve buyer can estimate and adopt without a sales conversation. Usually per-user, per-usage, per-workspace.
- **SDR-AE inside sales:** wants a metric with a clear "seats × price" story for the negotiation. Usually per-seat or per-seat + usage hybrid.
- **Enterprise MEDDPICC:** wants a metric that can be bounded with an annual commitment (dollar minimum) even if usage-based underneath. Pure per-event pricing at enterprise scale terrifies CFOs.

**B6 — Score summary + short-list (10 min).** Aggregate the scores. A metric passing all 5 tests is a strong candidate. Passing 4 with 1 mitigatable failure (e.g. per-usage failing estimability, mitigated by a calculator) is workable. Failing 2+ tests is usually the wrong metric; move it to the "rejected" list.

Short-list 1-2 candidates as your finalists. Name the reason the short-list survived and the reason each rejected candidate did not.

### Part C — Metric decision block + calculator + failure signals (30 min)

Deliver `part-c-metric-decision-block.md` in the shape of Chapter 6 Section 2:

**C1 — Primary pricing metric decision (10 min).** One sentence naming the metric: "{product} charges per {unit} per {period}, billed {annually/monthly}." Followed by:

- **The four-test defence** — one paragraph summarising why the metric passes each test (compress from Part B).
- **The alternative-metrics-rejected note** — one paragraph naming what you evaluated and why each rejected candidate lost.
- **The metric-vs-value derivation** — one sentence linking the metric to the frequency variable in the value equation.

**C2 — Pricing-page calculator design (10 min).** For any metric more complex than per-seat, sketch the pricing-page calculator (Chapter 4's estimability instrument). Cover:

- **Inputs** — 2-4 fields the buyer knows off the top of her head (headcount, repos, monthly transactions).
- **Output** — per-tier monthly / annual bill projection with the tier the buyer's inputs land in highlighted.
- **Overage handling** — how the calculator handles inputs above the middle-tier's bracket (project the upgrade cost, show the delta).
- **Annual / monthly toggle** — show both, with the annual discount visible.

If your metric is per-seat and needs no calculator, write "no calculator required; per-seat pricing displayed directly on the pricing page" and skip the calculator design — but note this in C2 explicitly so the reader knows it was considered.

**C3 — Failure-signal watchlist (10 min).** From Chapter 4's list of signals that "the metric is wrong," pick the specific signals you'll watch for over the next 6-12 months and how you'll measure each:

- **Bill-surprise churn** — measured by exit-interview data or churn-reason tagging in the CRM (mod-105 Chapter 7).
- **Anti-usage optimisation** — measured by CS call notes tagged "help me use less" or similar.
- **Bill-flat / value-growing** — measured by customer telemetry vs. billing data.
- **Sales cycles dying at estimation** — measured by close-lost reasons tagged "cost unclear / estimation."
- **Champion-vs-CFO fights** — measured by deal-stage stall time in procurement.
- **Every enterprise deal has a "custom" clause on the metric** — measured by contract-review notes.

For each signal you commit to watching, name the specific measurement source and the threshold at which the pack revision (Chapter 6 quarterly) considers a metric change.

## Starter guidance

- **The metric is the strategic choice; the number tests.** Chapter 4's central point. Spend 90% of your time on this exercise on Parts A / B; the number belongs to Exercises 02, 03, and 05.
- **Start from the value equation, not from the category leader.** The category leader may have made her choice at a different stage / motion / product-shape than yours. The value-equation frequency variable is a first-principles anchor.
- **Estimability failures are the most common deal-killer.** If the buyer cannot get to a bill estimate in 15 minutes, the deal stalls. Per-event pricing without a calculator is Chapter 4's classic estimability failure — usually mitigable, but has to be designed.
- **Incentive alignment failures are the most damaging long-term.** A metric that makes your customer's success = your revenue misalignment is a churn generator. Per-event is the canonical example: customer wants to reduce noise, vendor wants more events. If a metric fails Test 4 hard, evaluate a hybrid that fixes the alignment.
- **Per-outcome is beautiful in theory and brittle in practice.** Attribution is the hard part; unless you have a category norm for outcome measurement (some parts of marketing, some parts of financial services), rejecting per-outcome at seed and revisiting at Series C is the working default.
- **A hybrid metric is often the honest answer for mid-market / enterprise.** Chapter 4's Family 4 (seat + usage) captures the reliability of subscription with the expansion of usage. If your evaluation ends with two finalists that each fail a different test, a hybrid usually wins.
- **The sales-motion fit test is the tiebreaker.** Two metrics that pass Tests 1-4 equally will often diverge on Test 5. A PLG product cannot use a metric that requires a sales conversation to explain; an enterprise product cannot use a metric that gives CFOs unbounded quotes.
- **The calculator is not optional for any non-seat metric.** Chapter 4 is explicit: without a calculator, the metric fails Test 3 in practice regardless of how well it passes on paper. Sketch it in Part C2 even if you'll build it later.
- **The failure-signal watchlist is what turns a static metric decision into an operating one.** Chapter 6's quarterly review examines whether the metric is still working; the watchlist is the input. Without it, the metric survives on inertia.
- **Do not bloat the pricing metric with add-on line items.** Chapter 4's failure mode: base metric plus 3 add-ons plus 2 overage rules = a 5-line quote the buyer can't parse. One primary metric per product; at most one usage overage; the rest belongs to the tier composition, not the metric.
- **The metric decision is the least reversible pricing choice.** Changing it is a multi-quarter project. Pick with the same care you'd pick a co-founder; document the reasoning with the same care.

## Acceptance criteria

Your submission is complete when:

- [ ] Part A restates the Exercise 02 value equation and identifies the frequency variable.
- [ ] Part A enumerates 4-5 candidate metrics including the value-equation-derived candidate, the category-leader candidate, a per-seat variant, a per-outcome variant, and a hybrid.
- [ ] Each candidate has two sentences (what you charge for + standard example) and a note on category / competitor use (or `needs-research` flag).
- [ ] Part B scores every candidate against 5 tests (T1-T4 from Chapter 4 + T5 sales-motion fit) with pass / partial / fail + one-sentence evidence per cell.
- [ ] Part B ends with a short-list of 1-2 finalists and a written reason each rejected candidate lost.
- [ ] Part C1 states the primary pricing metric in one sentence and includes the four-test defence, the rejected-alternatives paragraph, and the metric-to-value-derivation link.
- [ ] Part C2 sketches the pricing-page calculator (inputs / output / overage / annual-monthly toggle) or explicitly states no calculator is required with a defence.
- [ ] Part C3 names 3+ specific failure signals from Chapter 4's list, the measurement source for each, and the threshold at which a pack revision considers a metric change.
- [ ] The metric decision is one *primary* metric, not a bloated stack of add-ons. At most one usage overage is included.
- [ ] Any competitor pricing referenced without a source is flagged `<!-- needs-research: ... -->` rather than invented.

## Common ways this exercise goes wrong

- **The copy-the-category-leader trap.** Founder picks per-seat because Slack does. Fix: run the four tests against your value equation and your ICP's growth vector; the leader's choice may fail your Test 1 or Test 2.
- **The skip-the-four-tests trap.** Founder writes a one-paragraph justification without scoring against T1-T4. Fix: fill in the matrix in Part B; every cell has to have pass / partial / fail + evidence.
- **The per-outcome-because-it-sounds-good trap.** Founder picks per-outcome without an attribution story. Every customer disputes the outcome count. Fix: evaluate per-outcome honestly against T3 (estimability) and T4 (attribution feasibility); reject at seed unless attribution is a solved problem in the category.
- **The per-event-without-calculator trap.** Founder picks per-event and ships without a calculator. Every buyer bounces at "how much will this cost me." Fix: Part C2's calculator design is required for non-seat metrics.
- **The hybrid-that's-actually-five-line-items trap.** Founder picks per-seat + per-event + per-integration + per-workspace + priority-support-add-on. Buyer's quote has 5 lines, each a negotiation. Fix: one primary metric; at most one overage; the rest is tier composition (Exercise 03).
- **The metric-decoupled-from-value-equation trap.** Founder picks a metric that has no relationship to the frequency variable in the value equation. Bills and value diverge over time. Fix: Part A1's frequency-variable identification is the anchor.
- **The metric-that-terrifies-CFO trap.** Enterprise-motion product with pure per-event pricing; every enterprise CFO rejects the unbounded quote. Fix: T5's sales-motion fit test; hybrid with annual commitment floor mitigates.
- **The metric-that-fails-Test-3-but-founder-hopes-it-works-out trap.** Estimability failure without a calculator plan. Fix: either design the calculator (C2) or pick a different metric.
- **The Test-4-hand-wave trap.** Founder claims Test 4 passes with "our customers love us." Fix: name the specific incentive alignment — does the customer's success increase the metric she pays on, or decrease it?
- **The no-failure-signal-watchlist trap.** Metric decision lands with no monitoring. Two years later the metric has drifted and no one noticed. Fix: Part C3's specific signals + measurement sources + thresholds.
- **The metric-decision-that-forgets-mod-107 trap.** Metric picked in isolation from sales motion. Later mod-107 planning realises the motion is wrong for the metric. Fix: T5's sales-motion fit is not optional; either the metric or the motion has to give.
- **The revisit-metric-in-a-year trap.** Founder assumes the seed-stage metric is fine forever. Fix: quarterly pack review (Chapter 6) examines the metric against C3's signals; annual review re-runs the four tests.
