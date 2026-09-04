# Exercise 02 — Value-Based Pricing Derivation

**Estimated time:** 3 hours
**Chapter link:** [`02-value-based-pricing.md`](../02-value-based-pricing.md)
**Prerequisite:** Chapter 2 read end-to-end; a mod-104 buyer / user / champion persona for at least one ICP segment; Exercise 01's WTP findings memo (or a placeholder if WTP research is not yet fielded); a way to reach 3-5 real ICP-matched buyers for the attribution sanity check.

## Problem statement

Chapter 2 named the failure modes: cost-plus pricing dressed up as value-based; competitor-sticker pricing dressed up as value-based; picking the wrong (unownable) outcome; inflating the equation to the theoretical maximum; treating one buyer's number as the segment's; skipping the "value slide" the buyer walks out with. The remedy is a five-step derivation — name the outcome, write the equation, compute the range, choose the capture ratio, cross-check — that produces a **defensible per-segment value worksheet** the founder can point at in a sales conversation and a board update.

This exercise trains you to **derive value-based pricing for one ICP segment end-to-end**, produce the one-page value slide the buyer walks out of the demo with, resolve the gap between the value ceiling and the stated-WTP ceiling (from Exercise 01), and pressure-test the derivation against 3-5 real buyers so the numbers are not a private founder exercise. The output is the anchor price for the middle tier of Exercise 03 and the value slide for the mod-105 demo.

The failure mode this exercise exists to catch: **the founder writes a value equation on a whiteboard, computes a big number, sets a price at 10% of that number, calls it "value-based," and never shows the equation to a real buyer or reconciles it with the stated-WTP curve. The pricing lands unmoored from both the buyer's economics and the buyer's stated ceiling.**

## Requirements

Deliver a folder `exercise-02/` with:

- `part-a-value-worksheet.md` — the five-step derivation for one ICP segment.
- `part-b-value-slide.md` — the one-page buyer-value slide the AE / founder shows in the demo.
- `part-c-attribution-and-gap-resolution.md` — the attribution defence, the 3-5 buyer sanity check, and the value-vs-WTP gap resolution.

### Part A — The five-step value worksheet (75 min)

Deliver `part-a-value-worksheet.md`. Pick **one ICP segment** (from mod-104) — usually the beachhead segment. Do not attempt to derive across all segments in one worksheet; per-segment is the discipline.

**A1 — Name the economic outcome (10 min).** Which single buyer-owned, dollar-denominated, attributable outcome is your product changing? Cover:

- **The outcome in one phrase** — "PR review cycle time," "time-to-first-response," "attributed pipeline," "incidents mitigated per quarter."
- **The persona who owns it** — the specific mod-104 persona whose scorecard this KPI rolls into. Name the person (or role), their manager, and the metric it rolls into at their manager's level. If you cannot name the roll-up chain (persona → manager → manager's manager KPI), the outcome is not buyer-owned; go back to mod-104.
- **How the persona currently reports on it** — dashboard, weekly review, quarterly business review, ad-hoc? If she doesn't currently report it, the value story does not survive a discovery call.
- **Alternative outcomes considered and rejected** — list at least 2 outcomes you *could* have picked and explain why they're weaker (usually because they fail one of the three tests: buyer-owned, dollar-denominated, attributable).

**A2 — Write the value equation (15 min).** Pick **one primary equation** from Chapter 2's six templates (hours × rate, seats × cost, incidents × cost, cycle × cost-of-delay, revenue × attribution, risk × probability × severity), and name **1-2 supporting cross-checks** (usually another equation that gives an independent estimate against the same outcome).

Write the equation with named inputs. Example:

```
Value = (baseline cycle time − improved cycle time) × cost per day of delay × active PRs / year
```

For each input, name:

- **The source** — "buyer's own dashboard," "DORA 2023 State of DevOps report," "Loomly customer aggregate telemetry across 8 customers," "IDC benchmark." If the source is your own telemetry, note the N and the recency.
- **The conservative-case value** — the low end of the plausible range.
- **The likely-case value** — the mid-plausible value you would defend to a CFO.
- **The theoretical-max value** — the highest value the input could take (which you will NOT use in the final derivation, but which is worth naming so you can point at what you're deliberately not claiming).

**A3 — Compute the per-customer annual value (15 min).** Plug the conservative-case and likely-case inputs into the primary equation to get:

- **Conservative annual value per customer** — the range you would defend to a skeptical CFO.
- **Likely annual value per customer** — the value you would use in the buyer's internal justification.

Also plug the cross-check equations and report their independent estimates. If two equations disagree by > 2×, name why (usually one input is fragile) — do not average them; pick the primary and use the cross-checks as sanity.

**A4 — Choose the value-capture ratio (10 min).** Given the category dynamics (commodity vs. differentiated), the current stage (adoption-seeking vs. ARPU-optimising), the packaging plans, and the competitor sticker anchor, pick a target capture ratio in the 10-25% band (Chapter 2). Justify:

- **The category-dynamics factor** — commodity → low capture; differentiated → higher.
- **The stage factor** — early-stage seeking adoption → low; growth-stage → higher.
- **The positioning factor** — has mod-103 moved the buyer's reference class or not? If not, capture is capped by the category reference.
- **The pick** — one number (or narrow range) with a defence you'd stake to.

Multiply by the **conservative** annual value to get the value-derived anchor price.

**A5 — Cross-check against WTP + competitor + live sales reactions (25 min).** The anchor price from A4 has to be:

- **Inside the [PMC, PME] band** from Exercise 01. If above PME, note the narrative work required to move the buyer's reference class. If below PMC, revisit — you may be under-anchored.
- **Within [0.5×, 2×] of the competitor-sticker reference.** Pick 3-5 named competitors (or adjacent-category anchors); list their published prices; note where your anchor lands. Outside the 0.5-2× band is a positioning move, not a pricing move.
- **Consistent with live-sales-call reactions.** From mod-105's discovery calls, name specific buyers who have heard a similar anchor and what their reaction was (score against the 1-5 ordinal scale from Chapter 5). If you haven't yet quoted the anchor to live buyers, note it explicitly as a gap.
- **Resolvable per Chapter 2's rule** — if value ceiling and WTP disagree by ≤ 2×, price at the value-band low end. 3× or more, price closer to WTP with a positioning-work plan. ≈, price middle. Value < WTP → re-examine the equation.

Produce the final anchor price for the middle tier. This is the number Exercise 03 uses.

### Part B — The buyer-value slide (30 min)

Deliver `part-b-value-slide.md`. Author the one-page slide the buyer walks out of the demo with (Chapter 2's four-element layout). This slide is what the mod-105 AE shows in the demo; it is not the private founder derivation.

Structure (one screen, no scrolling):

```
─────────────────────────────────────────────────────────────
{PRODUCT} FOR {BUYER'S TEAM}                    {date}
─────────────────────────────────────────────────────────────

Your team's KPI: {named outcome, in the buyer's language}

Where you are today: {baseline number, with source}
                    (industry benchmark: {benchmark})

Where similar teams get to: {improved number, with source
                             — usually your own customer data}
                             = {computed value in $ / year}

What {product} costs: {anchor price in $ / year}
Your team keeps:      {value − price} = {% of value}

Method: {one-sentence description of the equation used}
Conservative-case defence: {conservative number and inputs — 
                            the version the buyer takes to her CFO}
─────────────────────────────────────────────────────────────
```

Rules:

- One page. Buyer scans in 60 seconds.
- The named outcome is in **the buyer's language**, not internal product jargon.
- All numbers cite their source (buyer's dashboard, customer aggregate, third-party benchmark).
- The ratio (buyer's kept share) is calculated and displayed — not "great ROI" but "your team keeps 90% of the value."
- The **conservative-case** version is included below the fold — this is the version the buyer's CFO will interrogate; give her the answer up front.
- No product feature list; this is a value slide, not a capabilities slide.

### Part C — Attribution defence, buyer sanity check, gap resolution (45 min)

Deliver `part-c-attribution-and-gap-resolution.md`.

**C1 — Attribution defence (15 min).** Chapter 2's Failure 1: the buyer doesn't believe the attribution. For your specific outcome, write:

- **Why the outcome could be attributed to something else** — name the top 2-3 alternative causes a skeptical buyer would raise ("we adopted Kubernetes at the same time," "we hired 5 engineers," "the season is different").
- **The attribution mechanism** — how would you (and the buyer, jointly) measure that the change is attributable to your product? Before / during / after, pilot vs. non-pilot cohorts, buyer-as-her-own-control, control-team baseline?
- **The proof-point plan** — if you don't yet have proof points, what specific 3-5 customer references or case studies would you author, in what timeframe? Flag `<!-- needs-research: authorised customer stories -->` where relevant.
- **The attribution-discount ratio** — if attribution is genuinely weak (< 100% attributable to your product), the value math has to be discounted proportionally. State the discount you're applying (e.g., "we discount the value equation by 40% to account for confounding causes"). If you're not discounting, defend why.

**C2 — Live buyer sanity check (20 min).** Take the value slide from Part B to **3-5 real ICP buyers** (existing customers, warm prospects from the mod-105 pipeline, mod-101 discovery-corpus respondents willing to re-engage). Record for each:

- **Buyer name / role.** Verify ICP-match.
- **Reaction to the outcome named** — do they own the KPI? Is it named the same way in their world?
- **Reaction to the baseline number** — is it plausible for their situation? Higher, lower?
- **Reaction to the improvement number** — do they believe similar teams see this?
- **Reaction to the ratio slide** — do they feel the kept-value share is compelling? Fair? Too low? (A buyer saying "wait, only 10% for you? that's cheap" is a signal your capture ratio is low.)
- **Attribution objection raised** — did they raise any of the alternative-cause objections from C1?

Summarise the 3-5 reactions. Any pattern (all buyers reject one input; all disagree on the ratio; two disagree on the outcome name) is a signal to revise the worksheet.

If you cannot reach 3-5 real buyers this week, do the exercise against 3-5 mod-101 corpus respondents from memory + written notes, and label it "corpus-derived, not live-tested" in the deliverable. Real-buyer testing is preferred; corpus is acceptable when live is unavailable.

**C3 — Value-vs-WTP gap resolution (10 min).** From Exercise 01's WTP curve and Part A's value ceiling, compute the ratio (value ceiling / WTP ceiling) and apply Chapter 2's resolution rule:

- **≤ 2× gap:** price at the low end of the value band, lead with the value slide, expect longer sales cycles.
- **3× or more:** price closer to WTP, use value as narrative, name the case-study accumulation plan to close the gap over 6-12 months.
- **≈ equal:** price middle, high confidence.
- **Value < WTP:** re-check the equation; the buyer knows something you haven't translated into the spreadsheet.

Write the resolution as one paragraph: "the ratio is Xx, so we're pricing at $Y (position relative to WTP band), and our plan to close the gap is Z."

## Starter guidance

- **The outcome is the whole game.** Nine of ten failed value-based-pricing derivations pick the wrong outcome (unownable, un-dollar-denominated, or un-attributable). Spend real time on Part A1. If the persona doesn't already report the metric to her manager, the value story dies in the sales conversation regardless of how tight the equation is.
- **Pick a single primary equation.** Chapter 2 lists six templates; you pick one. The cross-checks are sanity checks, not co-primary equations. Buyers can hold one equation in their head; two is too many.
- **Report ranges, not points.** Every input has uncertainty; report a conservative case and a likely case. A single-number value ("$640K") pretends precision that does not exist and gets picked apart by any CFO worth her title.
- **Anchor on the buyer's language.** If the buyer calls it "cycle time" and your slide says "development velocity," the slide has already lost. Read your buyer-value slide out loud, imagining you're the mod-104 persona; if any phrase requires internal translation, rewrite in the buyer's phrase.
- **The conservative case is the load-bearing number.** Buyers-CFOs demand defensibility; the conservative case is the number they can walk into a budget conversation with. The likely case is what the buyer uses to justify to herself.
- **The capture ratio is a strategic choice, not a formula.** 10-25% is a band; the specific pick reflects category dynamics, stage, and positioning. Write the two-sentence justification in A4; a picked-ratio without justification is intuition.
- **Show the ratio, not just the price.** "Your team keeps 88% of the value" beats "our price is $12K" every time. The ratio is the buyer's win frame; the price alone is a transaction frame.
- **The attribution defence is where most sales cycles die.** If C1 has weak answers ("we don't have proof points yet, hoping the buyer trusts us"), the entire derivation is fragile. Author the proof-point plan even if you can't ship it today.
- **The 3-5 buyer sanity check is where the exercise becomes real.** A value slide that has never been shown to a buyer is a founder document. If you can't reach 3-5 this week, corpus-derived is acceptable, but real-buyer testing has to happen before the derivation is used in a live sales conversation.
- **The value-vs-WTP gap is a positioning statement, not a pricing bug.** A 5× gap doesn't mean the value equation is wrong; it means the buyer's category reference class hasn't yet moved (mod-103). Name the case-study accumulation plan (C3) as the closure mechanism.
- **Do not price against your value ceiling on day one.** Chapter 2's resolution rule is explicit: when value ≥ 3× WTP, price closer to WTP. Charging at the value ceiling immediately loses the deal; pricing at WTP + a moderate premium wins the deal and starts the multi-quarter narrative work.
- **Do not derive across all segments in one worksheet.** The value equation for enterprise is different from mid-market is different from SMB. Pick one segment per worksheet; run the exercise again per additional segment.

## Acceptance criteria

Your submission is complete when:

- [ ] Part A names one ICP segment and derives the value equation for that segment specifically.
- [ ] Part A1 names the outcome, the persona who owns it, the roll-up KPI chain, how the persona currently reports on it, and at least 2 alternative outcomes considered and rejected.
- [ ] Part A2 picks one primary equation from Chapter 2's six templates, names 1-2 supporting cross-checks, and cites the source + conservative + likely + theoretical-max for every input.
- [ ] Part A3 computes conservative-case and likely-case annual value with the primary equation, plus independent estimates from the cross-checks; disagreements > 2× are explained.
- [ ] Part A4 picks a capture ratio in the 10-25% band with a written justification citing category / stage / positioning factors.
- [ ] Part A5 cross-checks the anchor against Exercise 01's WTP band, 3-5 named competitors' published prices, and mod-105 live-sales reactions (or flags the missing live data explicitly).
- [ ] Part B is a one-page slide in the four-element shape (outcome, baseline, improvement, ratio) with every number sourced.
- [ ] Part B's outcome is stated in the buyer's language, not internal product jargon.
- [ ] Part B includes the conservative-case defence below the fold (the CFO-facing version).
- [ ] Part C1 names the top 2-3 alternative attribution causes, the attribution mechanism, the proof-point plan (or `needs-research` flag), and any attribution-discount applied to the equation.
- [ ] Part C2 records 3-5 buyer reactions (or corpus-derived reactions with the label) covering outcome / baseline / improvement / ratio / attribution objection.
- [ ] Part C3 computes the value-vs-WTP ratio and applies Chapter 2's resolution rule with a one-paragraph resolution statement including the pricing position and the gap-closure plan.
- [ ] Any input that cannot be sourced from your data, customer telemetry, a named third-party benchmark, or a live buyer is flagged `<!-- needs-research: ... -->` — no invented numbers.

## Common ways this exercise goes wrong

- **The unownable-outcome trap.** Founder picks "developer joy" or "team velocity" — no persona has a KPI on it. Fix: mod-104 persona check; if the metric doesn't roll into the manager's dashboard, pick another outcome.
- **The theoretical-maximum trap.** Founder plugs the best-case number into every input and gets a $10M "value ceiling." Fix: conservative + likely; save theoretical-max for context, do not use it in the derivation.
- **The single-buyer-anecdote trap.** Founder cites one customer's outcome ("Acme saved $500K") as if it were the segment. Fix: aggregate across 3-8 customers when possible, use range not point, and be explicit about the sample.
- **The ratio-without-defence trap.** Founder picks 30% capture "because we're a great product." Fix: capture > 25% requires a monopoly narrative or defensible switching cost; A4's justification has to name the specific factor.
- **The no-live-buyer trap.** The value slide has never been shown to a real ICP buyer. Fix: Part C2 with 3-5 buyers (or corpus-labelled if you cannot); before-use, live testing is required.
- **The value-slide-as-features-list trap.** Slide has a product feature list where the value math should be. Fix: no features on the value slide; features live in the capabilities section of the demo.
- **The kept-share-off-the-slide trap.** Slide names the price and the value separately; buyer has to compute the ratio herself. Fix: display the ratio explicitly ("your team keeps X% of the value we create").
- **The value-priced-immediately trap.** Founder computes a $50K/year value ceiling and prices at $50K on day one, ignoring the WTP ceiling of $10K. Fix: apply the resolution rule from Chapter 2; expected close rate at day-one value pricing is ~0%.
- **The one-derivation-across-all-segments trap.** Enterprise, mid-market, and SMB are averaged into one number. Fix: per-segment worksheets; run the exercise again per segment.
- **The attribution-hand-wave trap.** C1's proof-point plan is "we'll get customers to say nice things eventually." Fix: named 3-5 case-study candidates, target timeframe, `needs-research` flag if authorisation is missing.
- **The gap-not-named trap.** Value and WTP disagree by 5×; C3 is silent. Fix: apply Chapter 2's resolution rule explicitly; name the positioning work that closes the gap.
- **The value-slide-that-has-14-numbers trap.** Buyer cannot scan; loses interest. Fix: one page, 4 numbers, 1 ratio, one method sentence. Deep detail lives in Part A worksheet.
- **The derivation-that-does-not-produce-an-anchor trap.** Part A ends with "the value ceiling is $X-$Y range." Fix: the exercise produces one specific anchor price for the middle tier (Exercise 03 consumes it); a range is fine but the point stake has to be picked.
