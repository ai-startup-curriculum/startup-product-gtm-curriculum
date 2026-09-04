# Exercise 05 — ICP Drift Diagnosis: Enforce or Revisit

**Estimated time:** 3 hours
**Chapter link:** [`07-icp-scorecard-and-drift-diagnosis.md`](../07-icp-scorecard-and-drift-diagnosis.md)
**Prerequisite:** Exercise 01 (ICP scorecard); Exercise 03 (ten scored leads); Exercise 04 (not-now list); Chapter 7 read end-to-end

## Problem statement

Chapter 7 named **ICP drift** — the specific founder-led-sales pattern where the team, chasing revenue and rationalising each individual deal, gradually accepts customers outside the original ICP until the customer base looks nothing like the artifact and no one noticed the change happen. Drift is *not* legitimate learning ("we discovered the ICP was drawn too narrow and are revising it"); drift is the *un-diagnosed*, *un-decided* dilution where nobody explicitly chose to serve the new customers and no one explicitly re-authored the ICP. By the time drift is caught post-hoc at a board meeting, correction takes 12-18 months.

Chapter 7 also specified the response protocol: five drift-detection signals monitored monthly, and — when signals fire — a four-question decision framework that separates *enforcement* (the ICP is still right; the AE has stopped enforcing) from *revisit* (the ICP has been legitimately overtaken by product / market change).

This exercise trains you to build the drift-monitoring instrument, apply it to a realistic (or real) six-month customer-history snapshot, produce a founder-facing diagnosis with the enforce-vs-revisit verdict, and — if the verdict is revisit — draft the v1.1 ICP version-bump with the discipline Chapter 7 specified (named trigger, named change, rollout communication, instrument update).

The failure mode this exercise exists to catch: **the founder discovers at the board meeting that "we're winning across five different segments and I can't tell you what our ICP is anymore," and the correction takes a year.** The monthly instrument catches drift at month 3 instead; this exercise builds the instrument.

## Requirements

Deliver a folder `exercise-05/` with:

- `part-a-drift-instrument.md` — the monthly drift-monitoring dashboard specification.
- `part-b-six-month-diagnosis.md` — the applied diagnosis on a six-month customer history.
- `part-c-response.md` — the enforce-or-revisit verdict plus either the enforcement protocol or the v1.1 ICP version-bump.

### Part A — Author the drift-monitoring instrument (60 min)

Deliver `part-a-drift-instrument.md`. Specify a five-signal monthly dashboard the founder / sales leader reviews on a fixed cadence. For each of Chapter 7's five drift signals:

- **Signal 1 — Mix of closed-won deals in the beachhead segment.** What percentage of the last 30 days' closed-won revenue was inside the yes-segment from Exercise 04? Specify: the exact query / calculation, the healthy baseline, the drift-signal threshold, the crisis threshold, the data source (CRM field / Salesforce report / Attio view).
- **Signal 2 — ICP-fit score distribution at close-won.** What is the distribution of ICP-fit percentage on last-quarter's closed-won deals, and how has it shifted month over month? Specify: the histogram bucket size, the historical baseline distribution, the drift-signal shape (median dropping? long tail growing?), the data source (CRM ICP-fit-score field).
- **Signal 3 — Close-lost reason-code rate as a fraction of pipeline.** What fraction of pipeline is close-losing against named disqualifier reason codes? Specify: the healthy baseline (~30-50% per Chapter 7), the drift-signal threshold (< 15%), the data source (CRM close-lost reason-code report).
- **Signal 4 — Discovery-call time-to-disqualifier check.** How many minutes into the first discovery call is the AE actually running the Chapter 3 disqualifier questions? Specify: how you would measure this (call recording / Gong / Chorus review; AE self-report; sampling frequency), the healthy baseline (within first 10-15 min), the drift-signal threshold (deferred to second call or absent).
- **Signal 5 — Founder-hours spent on customer escalations, per account.** Are the escalation hours per active customer rising month over month? Specify: how escalation hours are logged, the healthy baseline (~1 hr / account / month at SEED for well-fit customers), the drift-signal threshold.

For each signal, deliver the following per-signal spec:

```
Signal {N} — {name}
  Question the signal answers: {one sentence}
  Metric: {precise definition, unambiguous computation}
  Data source: {CRM field | tool | manual log | calculated from raw data + query}
  Query / calculation: {SQL, view definition, or step-by-step manual computation}
  Healthy baseline: {a specific range with the source of the baseline — historical, benchmark, or first-principles}
  Drift-signal threshold: {the specific number that fires the signal}
  Crisis threshold: {the specific number that escalates to a same-week response}
  Review cadence: {monthly on the first Monday | weekly for signal 3 | ...}
  Owner: {named person}
```

Publish a one-page **dashboard mock** — a Notion / Google Docs / spreadsheet-shaped view showing all five signals with headers, current values, deltas from last review, and colour-coded threshold banding. Text sketch is fine; the point is that the artifact is legible at a glance and takes < 5 minutes to review.

### Part B — Apply the diagnosis to a six-month customer history (60 min)

Deliver `part-b-six-month-diagnosis.md`. Take a realistic (or real) six-month customer history — either your startup's real pipeline data if available, or a plausible constructed pipeline of 25-40 deals across the two quarters. For every closed-won and close-lost deal, capture:

- Deal ID.
- Close date.
- Close-won or close-lost verdict.
- ACV (approximate is fine).
- Segment (in-beachhead per Exercise 04, or which not-now segment).
- ICP-fit score at close (per Exercise 03's scoring discipline).
- Reason code (for close-losts) or won-reason (for closed-wons — was it beachhead-motion, referral, opportunistic).
- Post-close 60-day escalation load (for closed-wons — was the account demanding, standard, or low-touch).

Apply the Part A dashboard to the history:

- **Signal 1 (beachhead mix):** compute for month 1, month 3, month 6. Chart the trend.
- **Signal 2 (ICP-fit distribution):** compute median + distribution for each quarter. Chart the shift.
- **Signal 3 (close-lost reason-code rate):** compute per month.
- **Signal 4:** if you have call-recording data, sample 5 discovery calls per month and log the minute-mark of the disqualifier check. If not, use a proxy (self-reported per AE / founder recollection) and flag the proxy status.
- **Signal 5:** compute escalation hours per active account per month from the post-close escalation load.

Publish the **six-month dashboard-in-motion** as a table:

| Signal | Month 1 | Month 2 | Month 3 | Month 4 | Month 5 | Month 6 | Trend | Firing? |
|---|---|---|---|---|---|---|---|---|

Write a **diagnosis paragraph** naming: how many of the five signals are firing at month 6, whether the pattern is monotonic drift or a specific-event shift, and — critically — whether the drift is *concentrated* in one adjacent segment (a possible unlock-tripping event, per Chapter 7) or *scattered* across many one-off segments (classic opportunistic drift).

If your six-month history is constructed rather than real, be honest about what you constructed — the exercise's value is real if the history is *plausible*, but you should not present it as evidence of a specific past pattern that did not actually happen. Flag with `<!-- constructed for exercise — not real history -->`.

### Part C — The enforce-or-revisit response (60 min)

Deliver `part-c-response.md`. Apply Chapter 7's four-question decision framework:

1. **Are the out-of-ICP customers retaining and expanding as well as the in-ICP customers?** Compute (or estimate) the retention / expansion / escalation-load differential.
2. **Are the out-of-ICP customers concentrated in one adjacent segment?** If yes, the natural read is "the second bowling pin is opening earlier than expected" — the segment may be newly-in-scope. If scattered, the drift is opportunistic.
3. **Has the whole-product surface changed?** Has any Chapter 3 disqualifier's unlock condition tripped since the ICP was authored (SSO shipped, enterprise motion staffed, SOC 2 Type II certified)? If yes, a segment that used to disqualify may legitimately now qualify.
4. **Is the AE enforcing the disqualifier checklist?** Look at Signal 3 in Part B. If close-lost reason codes have dropped below the healthy rate, the drift is an enforcement problem, not an ICP problem.

Answer each question with a specific evidence-backed paragraph — not "we think" but "the data from Part B shows X, therefore Y." From the four answers, produce the verdict: **enforcement**, **revisit**, or (occasionally) **both** (some segments enforce; one specific adjacent segment revisits).

Then deliver the response artifact for whichever verdict you reached:

**If enforcement:**

- **Enforcement action plan.** The 90-day protocol per Chapter 7:
  - Reset with the AE — re-authorise the disqualifier close-lost verdict, re-run the discovery-call sequencing training, work the pipeline review with the ICP scorecard open on-screen.
  - Close-lose the pipeline's current out-of-ICP deals on second-look re-scoring; name the specific deals (from Part B) that would be closed-lost.
  - Refuse new out-of-ICP deals for 90 days, with a specific "we don't currently serve X" script and a named referral partner where possible.
  - Reset the escalation-load meter; expected to drop 30 days after the out-of-ICP customers churn or are handed to CSM.
- **Success criteria for enforcement.** Specific numbers at day 30, 60, 90 — signals in Part A that must be back in the healthy band, in what order.
- **What to do if enforcement fails.** If day-90 signals are still firing, what is the next protocol? (Usually: revisit review with an expanded evidence base.)

**If revisit:**

- **The v1.1 ICP version bump.** Per Chapter 7's version-bump protocol:
  - **Named trigger.** What specifically prompted the revisit — product change? PMF-cohort re-analysis? beachhead-won? Not "the AE was uncomfortable"; a real triggering event.
  - **Named change, line by line.** Which criteria added / removed / modified in Layer 1, Layer 2, disqualifiers, personas, not-now list? Every diff explicit at the criterion level.
  - **Named authors and reviewers.** Owner, founder / CEO sign-off, sales-lead operational confirmation, demand-gen filterability confirmation, product roadmap-alignment confirmation.
  - **Rollout communication.** The specific communication to sales and marketing — what changed, effective date, how in-flight deals under v1.0 are handled.
  - **Instrument update checklist.** CRM fields updated, Sales Navigator filters re-run, marketing automation re-segmented, weekly review template refreshed, mod-106 pricing tiers reviewed against new ACV bands, mod-107 motion-design implications noted.
- **Publish the v1.1 one-page scorecard** — the full ICP artifact from Exercise 01 re-authored with the changes, alongside a diff-view showing v1.0 vs v1.1.
- **What is preserved vs changed.** The beachhead commitment is either preserved (the revisit expanded the ICP inside the beachhead) or expanded (the second bowling pin opened); name explicitly which.

**If both:** name the segment(s) that revisit and the discipline that enforces the rest. Do not use "both" as a hedge — if you cannot separate the enforce-set from the revisit-set at the segment level, the diagnosis is unclear and you have not applied the four-question framework hard enough.

## Starter guidance

- **The dashboard is the artifact, not the analysis.** Part A is the *specification* — the queries, thresholds, cadence, owners. If you cannot hand Part A to a data analyst / ops person and have them build the dashboard from the spec alone, tighten the spec. This is the same discipline as Layer 1 firmographic criteria — every field is filterable / computable without ambiguity.
- **Signals are correlated but not redundant.** All five signals often fire together (that is the pattern of real drift), but they measure different things. Signal 4 (discovery-call timing) catches drift *before* it shows up in Signal 1 (close-won mix); Signal 5 (escalation load) catches drift *after* it shows up in Signal 1. Keep all five; each catches a different phase.
- **The historical baseline is the hard part.** Every signal needs a healthy-baseline number. For SEED-stage startups without much history, borrow baselines from Chapter 7's stated ranges and refine as data accumulates — the point is to have *a* threshold, not the perfect threshold. Vague "seems bad" is not a signal.
- **Chapter 7's bias is enforcement first, revisit second.** Rewriting the ICP because the AE is uncomfortable saying no is the fastest way to dissolve the beachhead. Only revisit on a named triggering event — the product changed, the PMF cohort re-analysis surfaced new criteria, the beachhead has been demonstrably won. "The AE feels the ICP is too narrow" is a coaching moment, not a version bump.
- **Test the enforce-vs-revisit distinction on a hard case.** Construct (or find in your real history) a hard case where three of the five signals are firing but the concentrated-adjacent-segment condition (Question 2) is met — Chapter 7's "unlock has tripped" case. Walk through the four questions carefully; the *right* answer depends on the specific evidence.
- **The v1.1 diff is expensive; do not do it lightly.** The version-bump has to update CRM fields, Sales Navigator filters, marketing automation, the weekly review template, the AE's onboarding docs, and — often — the pricing tiers. Each of those integration points is a real cost. Revisit is a legitimate act; casual revision is expensive drift under a different name.
- **The founder-exception log from Exercise 04 is a direct input.** If the log has 15 entries in six months, the founder is drifting from the not-now list; that is drift by another route. If the log has zero entries and the pipeline is inside the beachhead, that is the discipline working. Cross-reference explicitly.
- **When constructing a plausible six-month history, span the difficulty distribution.** The history should include: at least a few obvious in-ICP wins, at least a few obvious out-of-ICP wins, at least one high-escalation customer, at least one clean-close-lost pattern that reversed to close-won-with-drift over the quarter. Uniform-story histories are easy to diagnose but do not train the muscle.
- **The response artifact is a real hand-off.** Whatever verdict you reach, the response document should be immediately actionable by the founder — not a "we could consider" write-up. Named dates, named owners, specific deals to re-review, specific communications to send.

## Acceptance criteria

Your submission is complete when:

- [ ] Part A specifies all **five drift signals** with the full per-signal template (question, metric, data source, query/calculation, healthy baseline, drift-signal threshold, crisis threshold, review cadence, owner).
- [ ] Part A includes a **one-page dashboard mock** showing all five signals in a single legible view.
- [ ] Part B applies the dashboard to a **six-month customer history** with 25-40 deals; each deal has the required fields (ID, date, verdict, ACV, segment, ICP-fit score, reason code / won-reason, escalation load).
- [ ] Part B includes the **six-month dashboard-in-motion** table with all five signals computed per month plus the trend + firing verdict.
- [ ] Part B includes the diagnosis paragraph naming the pattern (drift concentrated vs scattered; monotonic vs event-triggered) with specific evidence.
- [ ] Any constructed (rather than real) history data is explicitly flagged.
- [ ] Part C answers each of the **four decision-framework questions** with a specific evidence-backed paragraph — not "we think" but "the data from Part B shows X, therefore Y."
- [ ] Part C produces a clear verdict — **enforcement**, **revisit**, or a specific split — and delivers the corresponding artifact.
- [ ] If the verdict is enforcement: Part C names the 90-day protocol with specific deals to close-lose, specific referral scripts, specific success criteria at day 30 / 60 / 90.
- [ ] If the verdict is revisit: Part C delivers the full v1.1 version-bump — named trigger, criterion-level diff, named authors/reviewers, rollout communication, instrument update checklist, and the re-authored one-page scorecard alongside a v1.0-vs-v1.1 diff view.
- [ ] The response artifact is written as an immediately actionable hand-off — named dates, named owners, specific next steps, not a "we could consider" write-up.
- [ ] Any factual claim (numbers, escalation-hour benchmarks, retention differentials) that cannot be sourced from the actual (or plausible-constructed) history is flagged with `needs-research` rather than fabricated.
- [ ] The founder-exception log from Exercise 04 is referenced in the diagnosis (either as evidence of drift or as evidence of discipline).

## Common ways this exercise goes wrong

- **Signals defined vaguely.** "Track how many out-of-ICP deals we're closing" is not a signal specification; it is a wish. Every signal needs the precise metric, calculation, and threshold. Without those, the dashboard is decoration.
- **Missing baselines.** Every signal needs a healthy-range number. "It should be higher / lower" is not a threshold. If you lack real historical data, borrow Chapter 7's ranges and refine over time — but ship a number.
- **All five signals firing but verdict is "revisit."** The four-question framework has an enforcement bias for a reason. If enforcement has not been tried and the disqualifier check-rate (Signal 3) has cratered, the drift is an *enforcement* problem — the ICP has not been overtaken by market change; the AE has stopped enforcing. Do not revisit until enforcement has been tried and failed.
- **No signals firing but verdict is "revisit."** The AE / founder feels the ICP is limiting and rewrites it without evidence. This is the fastest way to dissolve the beachhead — a v1.1 without a triggering event teaches the team that the ICP is aspirational.
- **The v1.1 diff is a paragraph, not line-by-line criterion changes.** A version bump has to be reviewable — every criterion added, removed, or modified is a specific edit with a stated reason. A paragraph-level summary hides the drift under a story.
- **No instrument update in the v1.1 rollout.** The doc changes; the CRM fields, Sales Navigator filters, and marketing automation still enforce v1.0. The AE reads the new version; the tools still filter by the old one. Update everything or nothing.
- **Enforcement protocol without specific deals named.** "We will close-lose out-of-ICP deals" is not a protocol; naming the specific 12 deals in the current pipeline that will be closed-lost on second-look re-scoring is. The enforcement is real when it is applied to specific deals.
- **Diagnosis paragraph that describes without deciding.** "Signals are firing and it might be drift or it might be an unlock" is not a diagnosis. The point of the four-question framework is to *decide*; the exercise is not complete until a decision lands.
- **Constructed history that is too easy.** A six-month history where every closed-won is in-beachhead and every out-of-ICP deal was a close-lost trains no diagnosis muscle. Construct the history with real ambiguity — a few close-wons in an adjacent segment with mixed retention outcomes, a scatter of one-off deals, at least one high-escalation account.
- **Constructed history mis-presented as real.** If you constructed the history, flag it. The exercise's value is training the diagnosis muscle; passing off constructed evidence as real history is dishonest and — for a founder who would act on the diagnosis — dangerous.
- **Missing the founder-exception log cross-reference.** Exercise 04 shipped the log; Exercise 05 uses it. If the log has entries and the diagnosis does not reference them, the exercises are not integrated. If the log is empty, note explicitly and cite as evidence of not-now discipline.
- **Response artifact not actionable.** The response is a memo the founder can act on Monday morning — named deals, named dates, named owners, specific communications. A response that reads like a strategic-consulting recommendation ("we recommend the founder consider…") has not converted to executable work.
