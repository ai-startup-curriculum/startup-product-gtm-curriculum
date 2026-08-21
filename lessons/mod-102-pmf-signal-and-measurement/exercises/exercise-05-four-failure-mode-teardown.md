# Exercise 05 — Four-Failure-Mode Teardown

**Estimated time:** 3 hours
**Chapter link:** [`06-four-pmf-failure-modes.md`](../06-four-pmf-failure-modes.md)
**Prerequisite:** Exercises 02 and 03 complete; Exercise 04 helpful but not required

## Problem statement

Chapter 6 named four failure modes — **wrong market, wrong product, wrong distribution, wrong price** — and a diagnostic tree that routes each to a specific downstream module. This exercise makes you run the tree.

You will:

1. Teardown **four provided case sketches**, one per failure mode, and prove which mode is firing with a specific evidence trail.
2. Teardown **your own startup** (or a real public one), producing a per-segment failure-mode verdict and the downstream-module route.

The exercise's whole payoff is the routing. A team that can diagnose the mode can spend the next quarter on the right work; a team that cannot spins.

## Requirements

Deliver a folder `exercise-05/` with:

- `part-a-provided-cases.md` — the four case teardowns.
- `part-b-my-startup-teardown.md` — the per-segment failure-mode read for your chosen startup.
- `part-c-routing-plan.md` — the actionable next-quarter plan derived from part B.

### Part A — Teardown four provided cases (75 min)

For each of the four case sketches below, deliver a teardown in this shape:

1. **Restate the evidence.** Bullet the observations from the case.
2. **Run the diagnostic tree.** Show your work through Chapter 6's Q1 → Q2 → Q3, naming the branch you take at each step and why.
3. **Verdict.** Which of Modes 1 / 2 / 3 / 4 fires? Or does no mode fire?
4. **Route.** Which downstream module owns the fix? Cite the module and the specific artifact / exercise in that module that would apply.
5. **What the founder should *stop* doing.** The specific work that the wrong mode-diagnosis would justify but that would be counterproductive given the correct diagnosis.

#### Case 1 — the "we just need more marketing" team

> A team building a scheduling tool for dental practices has been at it for 14 months. The Sean Ellis survey against 220 active dentists (defined as ≥1 appointment scheduled in the tool in the past 30 days) came back at **48% "very disappointed"** — the highest they've ever seen. Free-text is convergent: *"finally a scheduler that understands recall reminders."* Retention on the mid-size-practice segment (5–15 chairs) flattens at 82% at M6. Total active practices in that segment: 26. The team acquired all 26 through the founder's personal network of dental-school-classmate spouses. The founder wants to hire two AEs and a marketer next quarter.

#### Case 2 — the "we're rebuilding everything" team

> A team building a project-management tool for construction subcontractors ran the Sean Ellis on 340 active users (defined as ≥1 project created in the past 14 days) and got **9% very-disappointed aggregate**. Segment splits: general contractors 12%, subcontractors 8%, sole traders 6%. No segment above 15%. Retention on every segment decays: pooled W12 is 6%. Free-text on "who benefits most" is all over the map — 20 different roles named, none more than twice. Free-text on "main benefit" is thin — many "not sure" and "the interface is nice" answers. The team is rewriting the app in React Native with a new design system, believing the current UI is the problem.

#### Case 3 — the "our conversion sucks" team

> A team building a Notion-like doc tool for engineering teams ran the Sean Ellis on 4,200 active users of the free tier (defined as ≥3 docs created in past 14 days) and got **43% very-disappointed**. Retention on the free tier flattens beautifully at 61% W12. The paid conversion rate is **6%** — most users hit the paywall (10 docs per workspace on free) and never upgrade. Paid users (n=210) retain at 95% M12 and have Sean Ellis 71% VD. Free-text on "how to improve" from the free tier is dominated by *"$20/user/month is too expensive for our seven-person team"* and *"we'd pay but there's no team plan under 20 seats"*. Founder wants to do a Product Hunt relaunch to get more free users.

#### Case 4 — the "we're going enterprise" team

> A team building an analytics tool for growth marketers ran the Sean Ellis on 180 active users (defined as ≥1 report opened in past 7 days). Aggregate came back **31%**; the small-team segment (2–10 marketers) is **56%**; the enterprise segment (dedicated growth teams inside 500+ headcount companies) is **7%**. Retention: small-team WAU flattens at 55% W12; enterprise WAU decays to 8% W12 with a specific cliff after the pilot period. Free-text from enterprise: *"we love the concept but you don't have SSO, SCIM, audit logs, or per-team RBAC — our security team will not approve rollout."* Founder is considering shifting the whole roadmap to enterprise because "the ACVs are higher."

### Part B — Teardown your own startup or a real one (60 min)

Pick a startup — yours, one you know well, or the running code-review-tool example from the chapters. If you completed Exercises 02–04 against this startup, you already have most of the raw data.

Deliver `part-b-my-startup-teardown.md`:

1. **The evidence.** Bullet-point summary of the Sean Ellis segment splits (Exercise 02 or reconstructed), the retention curves (Exercise 03), and any other artifacts (conversion-to-paid rate if applicable, distribution channel concentration).
2. **Per-segment diagnostic-tree walk.** For each ICP segment you have data on, run Chapter 6's Q1 → Q2 → Q3, name the branches, and produce a per-segment verdict.
3. **Per-segment verdict table.**

| Segment | Sean Ellis VD | Retention shape | Mode | Route |
|---|---|---|---|---|

4. **One-paragraph founder-facing summary.** Written as if you were the founder writing to a board — one paragraph that names the segment-by-segment routing decision and the single most consequential next action. Do not soften; Chapter 7's opinionated-not-neutral rule applies.

### Part C — Routing plan (45 min)

Deliver `part-c-routing-plan.md`. This is the *action* the diagnosis produces.

For each segment × mode verdict from Part B, name:

- **The specific downstream module** the fix routes to (with a link).
- **The specific artifact in that module** you would run next (e.g., "mod-106 Van Westendorp WTP study on the free-tier cohort", "mod-108 channel-market-fit spike on three candidate acquisition channels", "mod-101 re-discovery cycle against sub-segment X").
- **The owner and rough timeline** (who, by when).
- **The "do not do" list.** The specific work you will *not* do next quarter because it would fit a wrong mode diagnosis (e.g., "we will not hire an AE — Mode 3 for the mid-market segment, distribution work first before sales-scale work").

Deliver as a table:

| Segment | Verdict (mode / route) | Next artifact | Owner / date | What we will NOT do |
|---|---|---|---|---|

Plus a one-paragraph closing note on the **one-mode-at-a-time** rule from Chapter 6: if you diagnosed two modes stacked on the same segment (e.g., wrong-product AND wrong-distribution), commit to fixing the lower-numbered mode first and defer the higher-numbered work; state the specific deferral explicitly.

## Starter guidance

- Chapter 6's diagnostic tree is the operating instrument. Every verdict must show its work through the tree.
- The four cases in Part A are designed to make each mode diagnosable from evidence alone — but each also contains a founder impulse that would be the wrong response. Half the exercise is diagnosing the mode; the other half is naming what the founder should *stop* doing.
- Case 1 is the archetypal wrong-distribution misdiagnosis (mode 3) — the team has real PMF in a small pool; hiring AEs before fixing distribution scales the wrong end. Do not let the "48% VD" fool you into thinking Marketing is the answer.
- Case 2 is wrong-market (mode 1) or a very deep wrong-product (mode 2). The rewrite instinct is wrong; the diagnosis is *discovery*, not engineering.
- Case 3 is textbook wrong-price / packaging (mode 4). The free tier is PMF; the paid tier is a pricing / packaging problem, not a marketing problem.
- Case 4 is wrong-product for the enterprise segment (mode 2) — the segment names specific missing features. The move is *not* to shift the roadmap to enterprise wholesale; the small-team segment is where PMF holds today. Enterprise is a segment to park until the specific product-shape gaps close.
- For Part B, if your startup has genuinely no evidence yet, use the running code-review-tool example from the chapters — the chapter examples are complete enough to run this teardown end-to-end.
- Part C's "what we will NOT do" list is where founders find it hardest to write. Naming the wrong response explicitly is what makes the routing binding.

## Acceptance criteria

Your submission is complete when:

- [ ] Part A has all four case teardowns with the five-field structure (evidence / tree walk / verdict / route / stop-doing).
- [ ] Case 1 verdict is Mode 3 (wrong-distribution) with route to mod-108, and explicitly names hiring AEs as the wrong response.
- [ ] Case 2 verdict is Mode 1 or Mode 2 (with a defended distinction) with route to mod-101, and explicitly names the React Native rewrite as the wrong response.
- [ ] Case 3 verdict is Mode 4 (wrong-price / packaging) with route to mod-106, and explicitly names the Product Hunt relaunch as the wrong response.
- [ ] Case 4 verdict is Mode 2 for enterprise segment (with small-team no-mode-fires) with route to mod-101 re-audit for enterprise features, and explicitly names the "shift the whole roadmap to enterprise" impulse as the wrong response.
- [ ] Part B produces a per-segment mode verdict table with a diagnostic-tree walk and an opinionated founder-facing summary.
- [ ] Part C's routing plan names the specific module, artifact, owner, date, and "will NOT do" per segment — and, if two modes stack on a segment, names the deferral explicitly.

## Common ways this exercise goes wrong

- **Diagnosing Mode 1 for every low-scoring case.** The tree exists to distinguish Mode 1 from Modes 2/3/4. If you find yourself always answering "wrong market", you are skipping the sub-segment reads.
- **Verdicts without evidence trails.** "It's Mode 3" without walking the tree is not a diagnosis. Show the Q1 / Q2 / Q3 branches.
- **Not routing to a specific module.** "This is wrong-distribution" without naming mod-108 leaves the diagnosis unactionable.
- **Softening the "stop doing" list in Part C.** Founders write "we will consider deprioritising X." That is not a commitment. Write "we will not hire the AE this quarter — Mode 3, distribution work first."
- **Reading Case 1 as Mode 4 (wrong price) because the pool is small.** The pool is small because of distribution, not price. Users who found the tool love it and pay for it (implicit in the "hire two AEs" plan); the constraint is that too few users find the tool.
- **Reading Case 4 as "shift to enterprise" because ACVs are higher.** The enterprise segment has no PMF today; shifting the roadmap wholesale abandons the small-team segment where PMF holds. The correct route is mod-101 re-audit for enterprise features while continuing to serve the small-team segment.
- **No one-mode-at-a-time discipline in Part C.** Fixing distribution while product is still leaky scales the leak; fixing price while distribution is broken means nobody encounters the new price. Order matters; the routing plan must reflect it.
