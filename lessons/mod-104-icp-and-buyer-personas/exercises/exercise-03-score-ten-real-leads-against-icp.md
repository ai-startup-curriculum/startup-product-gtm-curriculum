# Exercise 03 — Score Ten Real Leads Against the ICP

**Estimated time:** 3 hours
**Chapter link:** [`05-icp-fit-acv-fit-timing-fit.md`](../05-icp-fit-acv-fit-timing-fit.md)
**Prerequisite:** Exercise 01 (ICP scorecard); Exercise 02 (persona section); Chapter 5 read end-to-end

## Problem statement

Chapters 1-4 built the scorecard: firmographic + behavioural criteria, disqualifiers, three personas. Chapter 5 named the three-axis routing — ICP-fit, ACV-fit, timing-fit — as the discipline that turns the scorecard from a document into a real-time operating instrument, and named the six routing verdicts (Priority 1 / Priority 2 / Nurture / Downgrade-or-Refer / Close-lost, with an "active evaluation" catch-all for late-stage inbound) that allocate the AE's calendar.

This exercise trains you to **apply the three-axis scoring to ten real leads** — five inbound, five outbound — and to produce a routing verdict for each with the specific evidence that supports the verdict. The output is a scored pipeline audit that shows *what the AE would do with each of ten specific opportunities today* and — critically — where the scorecard is ambiguous, where the discovery questions do not resolve the ambiguity, and where your judgment and the founder's would differ.

The failure mode this exercise exists to catch: **the AE scores leads on a single "vibe" axis ("solid," "meh," "hot") and cannot articulate why one solid-feeling lead closed in three weeks while another solid-feeling lead died at proposal after nine.** The three axes are independent; scoring them together loses the discriminating power of each. This exercise makes the discrimination muscle-memory.

## Requirements

Deliver a folder `exercise-03/` with:

- `part-a-lead-set.md` — the ten leads (five inbound + five outbound), sourced and briefly described.
- `part-b-scoring-worksheet.md` — the three-axis scoring for each lead with verdict + AE action.
- `part-c-calibration-report.md` — the founder-vs-AE calibration diff and the pattern diagnosis.

### Part A — Assemble the ten-lead set (45 min)

Deliver `part-a-lead-set.md`. Pick ten real (or realistic) leads for the startup from Exercise 01. Distribution: **five inbound, five outbound**. If your startup has no live pipeline, use accounts you would target next quarter for outbound and either past demo-requests or plausible-inbound sketches (labelled) for inbound.

For each lead, capture the raw material — the AE's pre-call research packet — in six fields:

- **Lead ID.** `I1` … `I5` for inbound, `O1` … `O5` for outbound.
- **Channel.** How the lead arrived (inbound: demo request, blog subscriber, referral, product-hunt sign-up; outbound: LinkedIn Sales Navigator list, cold-email sequence, event-list follow-up).
- **Company snapshot.** Employee count, revenue / ARR band if known, industry / sub-vertical, funding stage, geography, primary technology-graph fingerprint. Every field the Exercise 01 Layer 1 scorecard needs.
- **What we know about the buying context.** For inbound: what did they say in the demo-request form / referral note? For outbound: what triggering signals did the list-builder flag (recent VP hire, funding round, hiring surge, incident announcement, competitor deprecation)?
- **Named persona contacts (if known).** The specific human on the call for inbound; the intended outbound contact + LinkedIn URL for outbound. Note which persona (buyer / champion / user) they most likely fill and how confident you are.
- **Pre-call research provenance.** Sources: LinkedIn URL, company careers page, engineering blog post, funding-announcement press release, mutual-contact intro thread. Every claim in the row should be traceable.

**Deliberately span the difficulty distribution.** The ten leads should include: at least one obvious Priority 1, at least one obvious close-lost against a disqualifier, at least two ambiguous cases where two axes disagree (e.g., strong ICP-fit / weak ACV-fit, or strong ICP-fit / cold timing), at least one that fires an anti-signal from Chapter 3 without hitting a hard disqualifier. If all ten of your leads look the same, you have not stress-tested the scorecard.

Any lead that has to be fabricated because you cannot find matching real accounts should be flagged with `<!-- needs-research: verify against a real account before using in a live pipeline exercise -->`. Fabricated leads are legitimate for practice authoring; they should not be shipped as real pipeline decisions.

### Part B — Score every lead on all three axes (90 min)

Deliver `part-b-scoring-worksheet.md`. For each of the ten leads, produce a worksheet in the following shape:

```
Lead: {ID} — {one-line company description}

ICP-FIT (apply Exercise 01 scorecard)
  Layer 1 firmographic score: {N/max, %}
    F1: {value observed} → {pass/fail/partial, weight applied}
    F2: {value observed} → {pass/fail/partial, weight applied}
    ...
  Layer 2 behavioural score: {N/max, %}
    B1: {evidence — from research or planned discovery question}
    B2: ...
  Disqualifier check: {none fired | D{n} fired — {reason code}}
  Combined ICP-fit band: {strong / moderate / weak / out}

ACV-FIT (three sub-questions)
  Buyer authority at target ACV: {yes / no / unknown — plan to resolve}
  Line-item allocated in current budget cycle: {yes / no / unknown}
  ACV vs RFP threshold: {below / at-threshold / above with resource commitment}
  Combined ACV-fit band: {strong / moderate / weak}

TIMING-FIT (five signals)
  Recent triggering event: {yes — what | no}
  Named budget cycle or approval window: {yes — when | no}
  Explicit deadline / KPI tied to outcome: {yes — what | no}
  Newly-visible pain (incident, audit, churn, board question): {yes — what | no}
  Active evaluation under way: {yes — competitors named | no}
  Signal count: {N/5}
  Combined timing-fit band: {hot / warm / cold}

VERDICT: {Priority 1 | Priority 2 | Nurture | Downgrade-or-Refer | Close-lost}
  Reason code: {specific — cite the Chapter 5 verdict cell}
  Confidence: {high / medium / low — with the resolving question if low}

AE ACTION THIS WEEK
  Next step: {book discovery call | send disqualifier-check email | refer to partner | close-lost with reason | move to nurture cadence}
  Hours to invest this week: {specific — cite the per-verdict calendar budget}
  What has to be true by the next touchpoint for the verdict to hold: {specific}
```

**Every field is required.** A worksheet with "unknown" on a field is acceptable if the *plan to resolve* is named ("ask on the first discovery call"); an "unknown" without a resolution plan is the failure mode this exercise exists to catch.

At the top of Part B, publish an **inbound-vs-outbound summary table**:

| Channel | Priority 1 | Priority 2 | Nurture | Downgrade/Refer | Close-lost |
|---|---|---|---|---|---|
| Inbound (n=5) | | | | | |
| Outbound (n=5) | | | | | |

The distribution should show the Chapter 5 asymmetry: inbound self-selects for warm-to-hot timing but is filtered hard on ICP; outbound self-selects for high ICP-fit but is filtered hard on timing. If your outbound is producing three Priority 1s and your inbound is producing zero close-losts, either the leads are miscalibrated or the scoring is being generous — investigate.

### Part C — Calibration and pattern diagnosis (45 min)

Deliver `part-c-calibration-report.md`. Two halves.

**Half 1 — the founder-vs-AE calibration diff.** Either you or a second reader (ideally the founder / an experienced AE / a peer in the module cohort) scores the same ten leads independently. Produce a diff table:

| Lead | Your verdict | Second-scorer verdict | Diff | Where does the disagreement live (ICP-fit / ACV-fit / timing-fit / verdict-cell interpretation)? |
|---|---|---|---|---|

For every disagreement, write one paragraph naming *why*:

- Is the underlying scorecard criterion ambiguous?
- Is the discovery question not sharp enough to resolve the axis?
- Is the routing verdict cell being interpreted differently (e.g., "Priority 2 warm-up" vs "Nurture" for the same cold-timing outbound)?
- Is one of the scorers integrating axes into a vibe score and losing discrimination?

Every disagreement is a **feedback signal on the scorecard**, not a scoring error. If three of ten leads produce disagreements on Layer 2 criterion B2, the criterion needs sharpening; if disagreements cluster on the timing-fit "warm vs cold" boundary, the timing-fit signal definitions need tightening. Log the specific scorecard edits you would make; these feed the v1.1 revision when it becomes appropriate.

**Half 2 — the pattern diagnosis.** Write a one-page synthesis answering:

- **Where is the AE's week going?** Sum the hours-per-verdict budget across the ten leads. Which cell absorbs the majority? Is the split defensible? (If 8 of 10 leads are Priority 1, you are either mis-scoring or the pipeline is unusually rich — investigate.)
- **What does the inbound-vs-outbound split tell you about your motion?** If close-lost against ICP is 40% of inbound, you have a demand-gen targeting problem to feed back to mod-108. If close-lost against timing is 40% of outbound, your outbound is not identifying triggering events — likely a list-source or trigger-monitoring issue.
- **What are the two most-common ambiguities in the scorecard?** From the calibration diff and the "unknown" fields, name the two criteria / questions that repeatedly failed to resolve cleanly. These are the specific v1.1 edits owed to the scorecard.
- **What are your two highest-leverage next actions this week?** Not a generic "work the pipeline" — a specific "run the discovery call on I1 by Thursday; send the enterprise-waitlist referral email to O3 by Wednesday." The exercise's whole point is that the scoring converts into calendar-committed action.

## Starter guidance

- **Do the pre-call research before you score.** The temptation is to score from the lead-source metadata alone. The scorecard requires evidence — for Layer 2 criteria that the AE would surface on a call, you either need the discovery-call answer or a specific plan to get it. If most of your Layer 2 scores are "unknown, need to ask," that is honest; write down the questions you would ask on the call and score conditionally.
- **Score all three axes independently — do not read one from another.** The most common failure is inferring ACV-fit from ICP-fit ("they're a strong ICP company so they'll have budget"). Score authority, allocation, and RFP-band as three separate reads even when the answer feels obvious. The exercise exists because the "obvious" reads collapse the axes.
- **Weight the disqualifier check first.** If a disqualifier fires — a whole-product-gap, an out-of-beachhead firmographic, a procurement-gated ACV posture — the verdict is Close-lost regardless of anything else on the scorecard. Do the disqualifier check before you spend twenty minutes computing weighted percentages.
- **Be honest about the "unknown" fields.** An unknown that resolves on the first discovery call is fine; the worksheet records "unknown — resolve on call via {specific question}." An unknown that requires research you have not done is a *pre-call-research gap* — either do the research or acknowledge that the verdict is conditional. Do not fabricate an answer to make the worksheet look complete.
- **Use the actual Chapter 5 routing table.** The verdict cell is not your judgment; it is the mapping from the three-axis bands to a specific cell in the routing matrix. If your verdict does not match the cell the three bands map to, either the bands are miscalibrated or you are overriding the matrix — either is worth surfacing in Part C.
- **Look for the anti-signal set from Chapter 3.** Even leads without disqualifier hits often fire anti-signals (procurement rumblings, absent decision-maker, "just gathering info"). Log them; two firing together should downgrade the verdict even if no single one is a hard stop.
- **The calibration diff is the point of the exercise, not the scoring.** If your Part B is perfect and Part C has zero disagreements with the second scorer, either the second scorer copied your reads or the scorecard is not being stress-tested. Seek disagreement; each disagreement is a scorecard-improvement signal.
- **Stress-test the inbound-vs-outbound asymmetry.** If your outbound is scoring cold-timing across the board, the outbound triggering-event research is thin — a list built from firmographics alone without any trigger overlay will produce cold outbound. Fix the list source, not the scoring.
- **Do not spend two hours on any single lead's worksheet.** The whole point is *first-call scoring speed*. If a lead takes 45 minutes to score, the scorecard is too heavy or the AE's tacit model has not internalised it yet. Aim for ~10 minutes per lead in Part B.

## Acceptance criteria

Your submission is complete when:

- [ ] Part A contains ten leads — five inbound, five outbound — each with the six pre-call research fields, sources cited, and at least one flagged as fabricated (with `needs-research`) if any were.
- [ ] The ten leads deliberately span the difficulty distribution: at least one obvious Priority 1, at least one obvious close-lost, at least two ambiguous cases, at least one anti-signal case.
- [ ] Part B contains a full three-axis worksheet per lead with all sub-questions scored (Layer 1, Layer 2, disqualifier check, ACV-fit sub-questions, timing-fit signals), a verdict, and a specific AE action with hours-committed.
- [ ] Every "unknown" field in Part B is paired with a resolution plan (a specific discovery question or a specific research action).
- [ ] The inbound-vs-outbound summary table is present and shows a defensible distribution — the Chapter 5 asymmetry between inbound (filtered on ICP) and outbound (filtered on timing) is visible or explicitly discussed if absent.
- [ ] Part C contains a calibration diff against a second scorer (founder, peer, or independent AE), with a paragraph per disagreement naming where the ambiguity lives.
- [ ] Part C names **at least two specific scorecard edits** that would resolve the most-recurring ambiguities — the feedback signal from the calibration.
- [ ] Part C names **at least two specific next-action items with calendar-committed dates** — the exercise converts to work this week, not analysis for later.
- [ ] Any claim in the worksheets that cannot be defended from the pre-call research or a plausible discovery answer is flagged with `needs-research` rather than fabricated.
- [ ] The three-axis scores are **independent** — no lead's ACV-fit is inferred from its ICP-fit; no lead's timing-fit is inferred from the inbound-vs-outbound channel alone.

## Common ways this exercise goes wrong

- **Scoring everything as Priority 1 or Priority 2.** The AE-optimist bias: every lead is scored charitably, no one is close-lost, the pipeline still looks 3× too big. The scorecard exists to disqualify; use it.
- **Fabricated evidence for Layer 2 criteria.** The Layer 2 answer is unknowable from LinkedIn; the worksheet fills in a plausible-sounding answer instead of "unknown — resolve on call." The unknowns are honest; the fabrications are the failure.
- **Ignoring the disqualifier check.** The worksheet computes a nice weighted score and produces a Priority 2 verdict, but a disqualifier fired that the scorer overlooked. Every lead's disqualifier check is the first thing on the worksheet, not the last.
- **Collapsing ACV-fit into ICP-fit.** "They're a Series-B B2B SaaS company so they'll have the budget." The three ACV sub-questions (authority, allocation, RFP-band) each have specific answers; skipping them loses the discriminating signal.
- **Reading timing-fit off the channel.** Inbound is not automatically warm; outbound is not automatically cold. The five specific timing signals are the score; the channel-level default is a *prior*, not a substitute.
- **Fabricating the "second scorer" in Part C.** The calibration diff is not a self-diff. If no second reader is available, at minimum re-score the ten leads two weeks later cold and compare — but the disagreement is dramatically less rich than a real second scorer.
- **Anti-signals ignored.** Disqualifiers are the hard stops; anti-signals are the soft warnings. Two firing together is a downgrade. A worksheet without an anti-signal check is missing half of Chapter 3.
- **Vague AE next-action.** "Follow up with the prospect" is not an action. "Send the enterprise-waitlist referral email to O3 by Wednesday, close-lost the account in CRM with reason 'outside beachhead, waitlisted' by Friday" is an action.
- **Ten near-identical leads.** If all ten leads score in the same band, the scorecard is not being tested. Deliberately include the ambiguous cases; the whole exercise is about the discrimination.
- **Calibration diff logged but not acted on.** The point of the diff is the scorecard-edit list. If Part C names five disagreements and specifies no scorecard edits, the exercise's feedback loop is broken — go back and name the specific v1.1 edits owed.
- **Per-lead time exceeding 15 minutes.** The scorecard is meant to be scored in real time on a discovery call. If a lead takes 45 minutes to score with all research in hand, the artifact is too heavy — compress it in the Exercise 01 revision.
- **No hours-per-verdict budget.** The verdict without a calendar-committed hours-this-week number is a rating; the exercise wants a work plan. Cite the per-verdict cadence from Chapter 5 and sum across leads.
