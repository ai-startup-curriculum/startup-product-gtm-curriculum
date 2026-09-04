# Exercise 03 — Expansion Motion Design

**Estimated time:** 3 hours
**Chapter link:** [`03-expansion-motion-design.md`](../03-expansion-motion-design.md)
**Prerequisite reading:** [Reforge — "Growth Loops are the New Funnels"](https://www.reforge.com/blog/growth-loops) (~20 min); [Kyle Poyar / OpenView — writing on expansion motions and pricing metrics](https://openviewpartners.com/blog/) (search "expansion" and "pricing"; skim ~30 min); [Lenny Rachitsky — writeups on PLG expansion and net revenue retention](https://www.lennysnewsletter.com/) (search "expansion" / "NRR"; ~30 min); [David Skok — "SaaS Metrics 2.0"](https://www.forentrepreneurs.com/saas-metrics-2/) (re-read the expansion / NRR section, ~15 min)

## Problem statement

Chapter 3 said the loud part out loud: **expansion is a first-order revenue lever, not a customer-success afterthought.** This exercise makes you *design* the motion — pick the primitive, wire the qualifying signal to a playbook, name the owner, name the instrumentation — for a startup whose current expansion story is "our CSMs will figure it out."

You will:

1. Diagnose three provided startup vignettes and, for each, name which expansion primitive(s) their pricing metric even makes available — then design the primary motion with signal, playbook, owner, and instrumentation.
2. Design the full expansion motion for a real (or realistic hypothetical) startup of your own, in the shape of scorecard section 4 (Chapter 7).
3. Name what would have to change upstream (in mod-106 pricing or mod-107 sales motion) if the pricing metric structurally caps NRR.

The exercise trains the design discipline that produces measurable Expansion ARR — the same discipline the code-review-tool worked example in Chapter 3 walks end-to-end.

## Requirements

Deliver a folder `exercise-03/` with:

- `part-a-vignette-motion-designs.md` — motion designs for the three provided vignettes.
- `part-b-your-expansion-motion.md` — the full motion design for a chosen startup, in scorecard-section-4 shape.
- Optionally: a signal-computation SQL sketch or a CS-tool workflow diagram in an appendix.

### Part A — Design expansion motions for three provided vignettes (75 min)

For each vignette, produce a design in this structure:

1. **Primitives available (given the pricing metric).** Reference the Chapter 3 table. Name each primitive as available / not available / structurally-blocked.
2. **Primary primitive pick** with one-sentence rationale.
3. **Qualifying signals** for the primary primitive — minimum three, each computable from product-usage + CRM data.
4. **Playbook** — in-product self-serve / CSM-assisted / AE-led — with rationale tied to ACV band.
5. **Owner** — specific role, comp tied to Expansion ARR.
6. **Instrumentation** — the four data flows Chapter 3 named (product events → CRM → signal layer → trigger layer), noting anything the team does not yet have.
7. **What would have to change upstream** if the pricing metric structurally caps NRR — one sentence, named against mod-106 or mod-107.

**Vignette 1 — a horizontal SMB tool priced flat per-account.**

A no-code website builder charges $79/month flat per account regardless of pageviews, seats, or storage. There is no second product line. ARR ≈ $4M, ~4,200 accounts, NRR reported as 91%, GRR 88%. The founder wants to hit NRR ≥ 100% within two quarters and is proposing to hire two "expansion CSMs" to drive it.

**Vignette 2 — a mid-market vertical SaaS priced per-seat, with a nascent second product line.**

A revenue-operations tool for GTM teams charges $180/seat/month for the core RevOps product. Six months ago the team launched a second SKU — a "Compensation Planning" module — priced at $95/seat/month, sold as an add-on. ARR ≈ $18M, average account has ~14 seats on core, cross-sell attach rate is 8% of accounts. NRR = 108%, GRR = 89%. The Head of CS owns "expansion" but has never hit an expansion-ARR target because there isn't one. There is no PQL definition; the founder pushes for cross-sell "when they think about it."

**Vignette 3 — a usage-metered developer infrastructure product with strong retention but flat expansion.**

A vector-database-as-a-service prices per-GB stored and per-query. ARR ≈ $12M, ~800 paying customers. Retention curves are flat by Chapter 1 criteria (durable). GRR = 94%. NRR = 102% — technically above the Series-A bar but well below the 120%+ usage-metered archetype (Snowflake, Datadog). Product usage grows month-over-month at the account level, but the billing system moves accounts to a higher tier only on annual renewal, and there is no in-product surface showing consumption against tier limits. The team assumes "usage-based means expansion is automatic."

For each: full seven-field design, one to two pages.

### Part B — Design the expansion motion for a real (or realistic hypothetical) startup (75 min)

Pick a startup — yours, one you know well, or the running code-review-tool from Chapter 3 (design a *variant* that changes at least one of pricing metric, primary primitive, or ACV band so you are not copying the chapter).

Deliver `part-b-your-expansion-motion.md` in the shape of scorecard section 4:

1. **Pricing metric (from mod-106).** State the metric explicitly and cite the mod-106 decision.
2. **Primitives available and picked.** Reference the Chapter 3 table. Name the primary primitive; note the secondary if any; explicitly exclude the ones the pricing metric does not support.
3. **Qualifying signals.** Minimum three per primary primitive, each specified as a computable threshold over product-usage + CRM state.
4. **Playbook per signal.** In-product / CSM / AE with SLA on time-to-touch after signal fires.
5. **Owner.** Specific role, comp structure (base + variable tied to Expansion ARR, or SPIF, or dedicated Expansion AE role).
6. **Instrumentation.** All four Chapter 3 data flows named as either "in place" or "gap — next sprint / next quarter to close."
7. **Reporting.** How Expansion ARR appears in the monthly board pack — separately from New ARR, decomposed by primitive.
8. **Current-quarter target.** Expansion ARR $ number tied to plan.
9. **Explicit exclusion.** One sentence naming the primitive(s) you are *not* pursuing this quarter and why.

Length: 1–2 pages. Do not exceed 2. Mark hypothetical numbers as such; sanity-check target Expansion ARR against benchmark expansion rates for your motion band ([OpenView SaaS benchmarks](https://openviewpartners.com/expansion-saas-benchmarks/) is the working reference).

### Part C — Reflection (30 min)

A short closing paragraph:

- Of the three vignettes in Part A, which one's expansion problem is *not* solvable by hiring — and what upstream module (mod-106 pricing, mod-107 motion, mod-105 CS hiring) actually owns the fix?
- For your Part B startup, what is the single instrumentation gap that most blocks the motion from being measurable at scale, and what would it take to close?
- If you were the founder reading your Part B design at the next board meeting, what is the specific question the board would push on hardest? (No owner? No signal? Structural pricing cap? Comp misalignment?)

## Starter guidance

- The Chapter 3 pricing-metric-to-primitive table is the load-bearing frame. If a pricing metric does not support a primitive, do not design a motion around it — name the constraint and route the fix to mod-106.
- For Vignette 1, the honest answer includes *"NRR is structurally capped near 100% until we re-price or build a second product line — hiring expansion CSMs will not fix a structural pricing gap."* This is the point of the vignette.
- For Vignette 2, the answer is that the primitives are available; the problem is the absence of qualifying signals, an owner comp'd on the number, and forecasted expansion pipeline. All fixable at the Chapter 3 layer.
- For Vignette 3, the answer is that a usage-metered pricing metric does not produce expansion on autopilot — the *in-product surface, the tier-limit signal, the mid-cycle upgrade path* are the motion, and the team has none of it.
- For Part B, if you cannot state the qualifying signals as computable thresholds ("account is at ≥ 80% of seat cap for 2 consecutive weeks", not "account looks ready"), you have a tribal motion, not a designed one.
- Do not design a motion your instrumentation cannot support. If you do not have product-usage events in a warehouse, the qualifying-signal layer is imaginary. Name the instrumentation gap honestly rather than papering over it.
- The mod-104 champion / decision-maker mapping is a load-bearing input to the cross-sell playbook — if you propose a cross-sell motion but cannot name the buyer for the second SKU, the motion will not close.

## Acceptance criteria

Your submission is complete when:

- [ ] Part A has full seven-field motion designs for all three vignettes.
- [ ] Vignette 1's design names the flat-per-account pricing as a structural cap on NRR and routes the fix to mod-106 re-pricing or new-product-line investment — not to hiring expansion CSMs.
- [ ] Vignette 2's design specifies both a seat-expansion motion and a cross-sell motion, with distinct signals, playbooks, and owners for each, and names the missing Expansion ARR target as the ownership fix.
- [ ] Vignette 3's design specifies a usage-tier signal layer (consumption-against-cap thresholds), an in-product upgrade surface, and a mid-cycle upgrade path — not a "wait for renewal" motion.
- [ ] Part B specifies the pricing metric, the available primitives, and the picked primary — with a one-sentence exclusion of the primitives not being pursued.
- [ ] Part B has ≥ 3 computable qualifying signals per primary primitive.
- [ ] Part B names a specific owner and a comp structure tied to Expansion ARR.
- [ ] Part B enumerates the four Chapter 3 data flows and marks each in-place or gap.
- [ ] Part B has a specific current-quarter Expansion ARR target with a plausibility sanity-check.
- [ ] Part C reflection names the vignette whose fix is upstream of Chapter 3, an instrumentation gap in the Part B startup, and a likely board-question.

## Common ways this exercise goes wrong

- **Designing three primitives for one motion.** Chapter 3 said pick one primary at Series-A. If you designed seat + usage + cross-sell all as "primary", you did not read the composition guidance.
- **Signals that cannot be computed from data.** "Account is engaged" is not a signal. "Account has active users > 80% of seat cap for the past 14 days" is.
- **No owner or "everyone owns expansion."** Chapter 3's operating rule. Assign the number to a role.
- **CSM comp'd on renewals only.** The comp structure has to align with the number — if the CSM is not paid on Expansion ARR, they will not push expansion.
- **Ignoring the pricing-metric constraint.** If the pricing metric does not tick when usage grows, no in-product upgrade path can materialise expansion. Fix at mod-106, not Chapter 3.
- **Designing a self-serve upgrade modal for enterprise-tier accounts.** Enterprise buyers do not click a self-serve modal. Escalation path required per ACV band.
- **Expansion ARR buried in a "renewals" number.** Chapter 3's reporting discipline — Expansion ARR is a separate P&L line with its own pipeline and its own forecast.
- **Cross-sell managed by the same new-logo AE with no attribution.** The AE has no incentive to prioritise cross-sell over their next new-logo deal. Attribution / SPIF / dedicated Expansion AE role solves this.
- **Skipping the current-quarter Expansion ARR target.** A motion without a number is a wish.
- **Copying the code-review-tool worked example without variation.** The point of Part B is to design; if the pricing metric, primitive, and ACV band all match Chapter 3, pick a different startup.
