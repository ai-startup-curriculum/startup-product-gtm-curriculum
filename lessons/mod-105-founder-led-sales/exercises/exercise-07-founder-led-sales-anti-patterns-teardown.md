# Exercise 07 — Founder-Led-Sales Anti-Patterns Teardown

**Estimated time:** 3 hours
**Chapter link:** [`06-proposal-close-and-founder-led-sales-anti-patterns.md`](../06-proposal-close-and-founder-led-sales-anti-patterns.md)
**Prerequisite:** Chapter 6 read end-to-end; Exercise 06 (CRM + weekly forecast) so a populated pipeline exists to teardown against; a working mod-104 ICP scorecard (ACV band, disqualifier list) and a mod-106 pricing anchor (or a reasonable interim rate).

## Problem statement

Chapter 6 named the four highest-cost founder-led-sales anti-patterns — the moments where the founder's unbounded authority stops being a superpower and starts being a liability:

- **Deep-discounting to close** a wobbly deal, training the pipeline to expect the discount and degrading renewals.
- **Feature-promising** to unstick a stalled proposal, distorting the roadmap and setting up a trust-collapse if the promise ships late.
- **Taking non-ICP deals** to hit a revenue number, absorbing 3-5x CSM cost, 2-3x churn, and product-pull distortion of the roadmap.
- **Saying yes to unsupported scope** — custom integration, bespoke SLA, data-residency arrangement, non-standard legal term — creating ongoing operational cost that outlasts the deal.

Each has a specific pressure dynamic (runway, quarter-end, board meeting), a specific rehearsed "say-no" script, and a specific *healthy alternative* that keeps the deal open on the right terms (multi-year for cash, logo for reference, priced exception for custom scope).

This exercise trains you to **teardown your own pipeline for anti-pattern incidents and near-incidents**, **author the rate card + discount ladder + exception log** that converts "let me see what I can do" pricing into a defensible instrument, **rehearse the four say-no scripts out loud until they are muscle memory**, and **install the monthly exception-review loop** that catches the three "one-time" 40% discounts before they become the new default. The output is a working anti-patterns pack — not a reflection, an *instrument* — that ships into the first-AE hand-off pack.

The failure mode this exercise exists to catch: **the founder reads Chapter 6, agrees the anti-patterns are real, nods at the say-no scripts, continues to grant un-coded discounts under quarter-end pressure, promises features in the demo to save stalling deals, closes non-ICP deals when the forecast is short, and ships a "pack" to the first AE that reads clean on paper and silently absorbs the exceptions that are degrading the economics.** Anti-pattern recognition without a rate-card + exception-log + rehearsed-script discipline is understanding without discipline — the chapter is read but the behaviour is unchanged.

## Requirements

Deliver a folder `exercise-07/` with:

- `part-a-rate-card-and-exception-log.md` — the written rate card, the discretion ladder, the healthy-discount patterns, and the exception-log schema.
- `part-b-anti-pattern-teardown.md` — a teardown of 4-6 real or role-played incidents / near-incidents from the pipeline (Exercise 06), one per anti-pattern.
- `part-c-say-no-rehearsal.md` — the four say-no scripts personalised to your product, rehearsed, and recorded (text or audio) with the awkwardness-ranking.
- `part-d-monthly-exception-review.md` — the monthly review cadence that catches drift before it becomes the new default.

### Part A — Author the rate card + discount ladder + exception log (60 min)

Deliver `part-a-rate-card-and-exception-log.md`.

**A1 — The rate card (20 min).** A written, internal document (not customer-facing). For each product tier in your packaging, name:

- Tier name and target ICP band.
- Standard annual contract value (ACV).
- Standard contract length (12 months default at SEED).
- Standard payment terms (annual up-front vs. quarterly vs. monthly) and standard billing cadence.
- Standard auto-renewal notice period (60-day default per Chapter 6).
- Standard SLA level (match operational capability; do not promise 99.99% if the vendor cannot operate it).
- Standard liability cap (1x-2x annual fees — hold the line).

If you do not yet have a settled rate card from mod-106, use your current best interim prices and flag `<!-- needs-research: pin against mod-106 pricing pack -->`. The point is a *written* anchor, not a perfect one.

**A2 — The discretion ladder (15 min).** Who has authority to grant what discount, against what coded reason. Follow Chapter 6's shape, adjusted for a one-founder (or founder + co-founder) org:

| Discount band | Who approves | Coded reasons permitted | Documentation required |
|---|---|---|---|
| 0% (list price) | Any seller | n/a | None |
| 1-10% | Founder | PROMO, MULTIYEAR, LOGO | CRM note |
| 11-20% | Founder + co-founder review | MULTIYEAR, LOGO | CRM note + exception-log entry |
| 21-30% | Co-founder sign-off | LOGO (anchor), MULTIYEAR (36+ mo) | Written rationale + exception-log |
| > 30% | Deliberate exception | Named strategic reason only | Board-visible exception-log entry |

Adjust the bands and the gate structure to your reality. The point is that *every* non-list-price deal has a coded reason and a documented approval path. "Let me see what I can do" is not an entry in the ladder.

**A3 — The three healthy-discount patterns (10 min).** Chapter 6 names three patterns of discounting that are strategically sound and should be pre-authorised:

- **Multi-year for cash certainty.** Specify your bands (e.g., 10-15% off 24 months, 15-20% off 36 months) and the cash-timing rationale.
- **Logo / reference for asymmetric value.** Define what qualifies as a logo in your ICP, the discount offered, and the *reference commitments* embedded in the contract (case study, 2-3 references per quarter, logo-usage rights). Price the reference commitment.
- **Time-bounded promotional launch.** Define the specific launch window, the discount, and the hard end date. Note the pattern-degradation risk if used every quarter.

For each, write the *coded-reason label* exactly as it will appear in the CRM reason-code field (MULTIYEAR, LOGO, PROMO), consistent with Exercise 06 Part A4.

**A4 — The exception-log schema (15 min).** The exception log is the instrument that catches "one-time" exceptions before they become the new default. Author the specific schema (spreadsheet columns or CRM fields):

| Date | Deal | ACV | Standard price | Exception granted | Coded reason | Rationale (1-2 sentences) | Approver | Review flag |
|---|---|---|---|---|---|---|---|---|

Include the specific entry criterion ("any discount > 10% or any scope / term outside standard"), the storage location (same CRM, separate sheet, shared doc), and the monthly-review rollup rule (Part D).

### Part B — The anti-pattern teardown (75 min)

Deliver `part-b-anti-pattern-teardown.md`. Pull 4-6 incidents from your pipeline (Exercise 06) — real or role-played — one per anti-pattern. If your current pipeline does not contain all four patterns, construct a role-played scenario against the Exercise 06 schema and flag `<!-- needs-research -->`.

For each incident, document the teardown using this template:

```
──────────────────────────────────────────────────────────
Incident: {Deal ID} — {customer name or role-play label}
Anti-pattern: {deep-discount / feature-promise / non-ICP / custom-scope}
Pressure context: {quarter-end / runway / board meeting / champion ask}
──────────────────────────────────────────────────────────

1. THE MOMENT
   {2-3 sentences on what the buyer asked for and what the founder was tempted to grant}

2. WHAT HAPPENED (or would have happened)
   {Decision taken + outcome if known; if a near-miss, the counterfactual}

3. THE SIX-MONTH COST
   {The specific downstream cost per Chapter 6 — pipeline-training effect for
    discounts; roadmap distortion for feature-promises; CSM cost + churn + product-
    pull for non-ICP; ongoing operational cost for custom-scope. Name a dollar
    estimate where possible, flagged as estimate.}

4. THE RATE-CARD / DISCIPLINE BREAK
   {Which rule in Part A was violated or almost violated? Which coded reason
    would have been required? Was there a healthy alternative available?}

5. THE HEALTHY ALTERNATIVE
   {The specific different path from Chapter 6 — multi-year instead of deep-
    discount, honest disqualification instead of feature-promise, close-lost +
    partner-referral instead of non-ICP close, priced-exception instead of
    free-custom-scope.}

6. THE SCRIPT THAT SHOULD HAVE RUN
   {Quote the Part C say-no script verbatim, personalised to this incident. If
    the script needs sharpening for this case, note the sharpening.}

7. THE PATTERN SIGNAL
   {What does this incident, aggregated with others of the same shape, tell you
    about ICP (mod-104), pricing (mod-106), product roadmap, or forecast
    honesty (Chapter 7)?}

8. CRM / EXCEPTION-LOG ACTION
   {If a real decision: file the exception-log entry retroactively. If a near-
    miss: file a "near-miss" entry so the pattern surfaces at the monthly review.}
──────────────────────────────────────────────────────────
```

**Coverage requirements.** At least one incident per anti-pattern (4 minimum). At least 2 of the 4-6 should be *real* incidents from your pipeline rather than fully role-played — the chapter's discipline installs through recognising your own near-misses, not through analysing hypotheticals. Flag any role-played incident `<!-- needs-research -->`.

**Honesty test.** For every real incident where the founder *did* grant the exception (not just was tempted), the teardown must say so without flinching. The exercise's whole discipline-installation half runs on honest incident analysis, not reputation management. If every incident in Part B is a "near-miss I resisted," the honesty discipline has already broken.

### Part C — The four say-no scripts, personalised and rehearsed (30 min)

Deliver `part-c-say-no-rehearsal.md`. Chapter 6 provides a canonical version of each script. Personalise the language to your product, your tier structure, your ICP, and your coded-reason labels.

For each of the four, deliver:

```
Anti-pattern: {name}
Buyer line that triggers: {typical phrasing — "can you do 25% off?" / "if you
                           could ship X by Q2 we'd sign" / "we're a different
                           kind of company but we'd love to try it" / "we need
                           it hosted in Frankfurt only"}

Your say-no script (3-5 sentences):
{the exact language — not a paraphrase, not a sketch}

The alternative-offered (1-2 sentences):
{the healthy yes-shape that keeps the deal open — multi-year, honest disqual
 + referral, priced exception, etc.}

The coded reason (if the alternative is taken):
{the specific reason-code label from Part A — MULTIYEAR, LOGO, PROMO, PRICED-
 EXCEPTION, HONEST-DISQUAL, etc.}

Fallback if the buyer pushes further:
{the second-level language — hold the line, name the precedent cost, or
 close-lost cleanly}
```

Author one for each of:

1. **Deep-discount refusal** (Chapter 6's canonical line: "below [rate-card floor], we'd be treating our other customers unfairly and setting a precedent I'd have to honor. Would multi-year work for you, or should we look at a different tier?").
2. **Feature-promise refusal** (Chapter 6's canonical line: "that feature is on our roadmap but not in the next 6 months. Rather than promise a ship date I won't hit, let me suggest two options: sign now for current scope and I'll flag your account when we do ship it; or hold off and I'll reach back out when it's shipping.").
3. **Non-ICP-deal refusal** (Chapter 6's canonical line: "being honest — I don't think we're the right fit for what you're trying to do. We're built specifically for [ICP]; your team is different in [specific way]. Rather than sell you something you'd probably regret in 6 months, I'd point you at [alternative].").
4. **Custom-scope refusal** (Chapter 6's canonical line: "that custom [integration / deployment / SLA] is possible but outside our standard scope. To do it we'd need to add [X% / $Y one-time / different tier]; the ongoing cost is real.").

**Rehearsal check (10 min).** Read each script out loud twice. Record either (a) the audio to a file in the folder, or (b) a self-rating note on *delivery smoothness* per script on a 1-5 scale.

Then rank the four by **awkwardness-under-pressure** — which one would you most-likely abandon on a real call if the buyer pushed back twice? That is your rehearsal target. Note it explicitly:

```
Most-likely-to-abandon under pressure: {anti-pattern #}
Why: {one sentence — "the honest-disqualification feels harsh and I'm tempted
      to soften it when the buyer sounds eager"}
Specific rehearsal plan: {how you will drill it before the next real call —
                         3 more out-loud rehearsals this week, role-play with
                         co-founder, record and listen back}
```

### Part D — The monthly exception review (15 min)

Deliver `part-d-monthly-exception-review.md`. Author the monthly cadence that catches drift before it becomes the new default.

**D1 — The review mechanics (5 min).**

- When: specific day of the month and time-box (30-45 minutes).
- Who: founder + co-founder (or founder solo at smallest scale, with the output shared with an advisor / board member monthly).
- Input: the exception log from Part A4 for the trailing 30 days.
- Output: a one-page summary feeding mod-104 (ICP drift), mod-106 (pricing moves), and the CRM reason-code rollup (Chapter 7).

**D2 — The four review questions (10 min).** Author the specific questions you will walk, with the threshold that triggers an action:

1. **Discount concentration.** What % of closed-won deals this month carried a discount of any size? What % carried > 15%? Threshold: if > 50% of deals carried any discount OR > 20% carried > 15%, the rate card has drifted and a mod-106 pricing-pack conversation is overdue.
2. **Coded-reason distribution.** Of the discounts granted, what % were MULTIYEAR vs. LOGO vs. PROMO vs. uncoded-exception? Threshold: if > 20% are uncoded exceptions, the discretion ladder (A2) is being bypassed and the gate has broken.
3. **Feature-promise log.** How many deals this month closed on the back of a product-roadmap commitment with a date? For each, is the ship date tracked in the roadmap, with ownership? Threshold: any uncommitted / un-dated promise logged against a signed deal is a trust-collapse-in-progress.
4. **Non-ICP close count.** How many deals closed outside the mod-104 ICP (any disqualifier triggered but overridden)? Threshold: any single non-ICP close requires a one-paragraph written justification. More than 1 per month in the same disqualifier bucket is an ICP-scorecard-drift signal (feeds mod-104's drift diagnosis).
5. **Custom-scope grants.** How many commercial exceptions (SLA uplift, custom integration, data-residency, bespoke legal term) were granted this month? For each, is the ongoing operational cost estimated and the pricing premium (if any) applied? Threshold: any unpriced custom-scope grant is an entry for the ops / engineering backlog with a dated cost estimate.

**D3 — The feedback-loop map (5 min).** Draw the specific loop from the exception log to the upstream artifacts:

- Rate-card drift → mod-106 pricing pack revision.
- Non-ICP cluster → mod-104 ICP scorecard revision + disqualifier-list refinement.
- Feature-promise log → product roadmap commitment tracking.
- Custom-scope grants → pricing of exceptions + engineering backlog visibility.
- All of the above → Chapter 8's first-hire readiness check (the pack has to be *characterised*, not just populated).

## Starter guidance

- **The rate card is written, not spoken.** A rate card that lives in the founder's head is not a rate card. Write it, timestamp it, store it where the first AE will inherit it. Even if numbers change, the shape persists.
- **"Let me see what I can do" is a pattern-identifier.** Any time you hear yourself say that language, you are in the moment Chapter 6 is designed to catch. The rate card + say-no script is what replaces the phrase.
- **Code every exception.** An uncoded exception is a future precedent you cannot defend. If the discount does not fit MULTIYEAR / LOGO / PROMO / PRICED-EXCEPTION, it should probably not happen — or it should be filed as a deliberate strategic exception with named rationale.
- **The exception-log is not punitive.** It is characterisation. The point is not to shame the founder for discounting — it is to make the pattern legible so the pricing / packaging feedback loop runs.
- **Honest disqualification is the hardest script.** Most founders rank it most-likely-to-abandon under pressure. The reason is empathy — the buyer is eager, the quarter is short, the number feels within reach. The script's job is to make the honest conversation sayable. Rehearse it twice as much as the others.
- **The healthy-discount patterns are not a loophole.** MULTIYEAR, LOGO, and PROMO are strategic patterns; they are not permission to grant 20% off every deal with a MULTIYEAR label and a 13-month contract. If every deal is MULTIYEAR, the rate card is already the discounted price.
- **Role-play incidents must be marked.** The exercise builds the muscle through real incidents; role-plays are the fallback. Any incident that is role-played gets a `<!-- needs-research -->` flag so the retrospective is honest about the sample.
- **The monthly review is a 30-45 minute standing meeting.** If it is not calendared, it will not happen, and the exception log becomes a graveyard. Install the cadence before Part D is "done."
- **The feedback loop is what makes the pack worth building.** An exception log that nobody reads is a diary. An exception log that feeds mod-104 (ICP), mod-106 (pricing), and roadmap is an operating instrument.
- **The say-no scripts are muscle memory, not reference material.** You will not open a Google doc on a buyer call. The scripts are rehearsed until they are available in the moment. If you cannot deliver them out loud smoothly in Part C's rehearsal check, they will not be available in the real call.
- **The alternative-offered line is what keeps the deal open.** Every refusal is paired with a legitimate yes-shape. "No, but" closes more deals than "no, period."

## Acceptance criteria

Your submission is complete when:

- [ ] Part A contains a written rate card with tier, standard ACV, contract length, payment terms, auto-renewal, SLA, and liability cap for every product tier.
- [ ] Part A contains the discretion ladder with discount bands, approver, permitted coded reasons, and documentation requirements per band.
- [ ] Part A names the three healthy-discount patterns (MULTIYEAR, LOGO, PROMO) with specific bands, reference-commitment pricing (for LOGO), and end-date discipline (for PROMO).
- [ ] Part A defines the exception-log schema with the entry criterion, storage location, and monthly-review rollup rule.
- [ ] Part B contains 4-6 incident teardowns, at least one per anti-pattern, with the eight-section template completed per incident.
- [ ] At least 2 of the Part B incidents are real pipeline incidents (not fully role-played); any role-played incident is flagged `needs-research`.
- [ ] At least one Part B incident where the founder *did* grant the exception is documented honestly, not reframed as a near-miss.
- [ ] Each Part B incident names a six-month cost estimate (dollar figure or specific operational consequence), the discipline break, the healthy alternative, the say-no script, and the pattern signal to upstream artifacts.
- [ ] Part C contains all four say-no scripts, personalised to your product, with the trigger line, the script, the alternative-offered, the coded reason, and the fallback.
- [ ] Part C includes an out-loud rehearsal evidence — either a recorded audio file in the folder, or a self-rating note on delivery smoothness per script.
- [ ] Part C names the most-likely-to-abandon script with a one-sentence why and a specific rehearsal plan.
- [ ] Part D contains the monthly review cadence (day / time-box / attendees / input / output).
- [ ] Part D contains the four (five, including custom-scope) review questions with specific thresholds that trigger upstream action.
- [ ] Part D contains the feedback-loop map linking the exception log to mod-104, mod-106, product roadmap, and Chapter 7's reason-code rollup.
- [ ] The monthly review is calendared (not just documented) — a specific first-review date is named.

## Common ways this exercise goes wrong

- **The rate-card-in-the-founders-head trap.** Part A is written aspirationally; the actual pricing is still "it depends." Fix: write the current real prices, flag `needs-research` if un-settled, make the first AE's inheritance path explicit.
- **The ladder-with-no-gates trap.** Discretion ladder has bands but no coded-reason restrictions and no documentation requirement. Founder self-approves everything. Fix: every band has a required coded reason and a required documentation step; the > 20% band requires a second set of eyes.
- **The healthy-pattern-as-loophole trap.** Founder relabels every deep discount as MULTIYEAR with a 13-month contract. Rate card is already the discounted price. Fix: MULTIYEAR requires 24+ months real; audit at monthly review.
- **The sanitised-teardown trap.** Every Part B incident is a near-miss the founder resisted. No real discounts, no real feature-promises. Fix: honesty is the exercise's point; include at least one real exception that was granted.
- **The role-play-only-pack trap.** All 4-6 incidents are hypotheticals. No muscle built against real pattern recognition. Fix: 2+ real incidents from Exercise 06 pipeline; role-play fills gaps.
- **The six-month-cost-handwaved trap.** "Could be bad" without a number or specific consequence. Pattern-signal has no weight. Fix: name a dollar estimate or a specific operational cost (headcount hour, roadmap slip, customer-support ticket volume).
- **The script-paraphrased trap.** Part C scripts are summaries, not deliverable sentences. Under pressure, nothing to say. Fix: full sentences, out-loud rehearsed, 3-5 sentences per script.
- **The no-alternative-offered trap.** Scripts refuse but do not offer a healthy yes-shape. Buyer feels blocked; deal close-losts unnecessarily. Fix: every refusal paired with a specific alternative, coded reason labelled.
- **The silent-rehearsal trap.** Founder claims to have rehearsed in their head. Under real pressure, the delivery is not smooth. Fix: out-loud rehearsal with audio recording or an honest self-rating per script.
- **The exception-log-is-a-graveyard trap.** Entries filed; monthly review skipped. Patterns never roll up. Fix: calendar the first monthly review before Part D is marked done; name the attendees and the output format.
- **The feedback-loop-breaks-at-mod-104 trap.** Non-ICP cluster surfaces at the review but no mod-104 action is taken. ICP drift continues. Fix: the review's output includes specific proposed scorecard / disqualifier edits; mod-104 updates on a defined cadence.
- **The uncoded-exception-tolerance trap.** 25% of exceptions have no coded reason. Monthly review flags it; founder shrugs. Fix: the > 20% uncoded threshold is a hard trigger — the next 30 days require every exception coded or escalated.
- **The ladder-ignored-at-quarter-end trap.** Rate card and ladder apply all quarter until the last week; then everything is 30% off. Fix: the ladder tightens at quarter-end, not loosens — the pressure moment is exactly when the discipline is most load-bearing.
- **The ICP-override-with-no-justification trap.** Non-ICP deals close with "it felt like a good fit" as the rationale. Pattern un-decodable; mod-104 drift invisible. Fix: every non-ICP close has a one-paragraph written justification; more than 1 in the same disqualifier bucket per month is a scorecard-edit signal.
- **The custom-scope-grant-without-ops-cost trap.** Custom SLA, data-residency, or integration granted without an engineering / ops estimate. Discovery of the cost comes months later. Fix: dated ops-cost estimate attached at the moment the grant is made; feeds the engineering backlog same-day.
- **The feature-promise-with-no-roadmap-tracking trap.** Deal closes on "we'll ship X by Q2." X is not in the roadmap. Q2 arrives; customer churns. Fix: any ship-date promise logged against a signed deal is added to the roadmap tracker same-day; monthly review audits.
- **The pack-authored-not-used trap.** Rate card + exception log + say-no scripts live in a folder; the founder's actual negotiations do not reference them. Fix: the pack is the operating instrument, not a diary — Chapter 7's weekly review and this exercise's monthly review are what install it.
- **The one-time-not-recurring trap.** Exercise completed once; discipline never installs. Monthly review slot never calendared. Fix: the next monthly review date is on the calendar before the exercise is marked complete; the discipline-installation half is what makes the pack real.
