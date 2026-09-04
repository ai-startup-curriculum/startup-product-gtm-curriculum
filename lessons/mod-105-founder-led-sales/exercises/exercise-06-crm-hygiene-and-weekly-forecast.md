# Exercise 06 — CRM Hygiene and Weekly Forecast

**Estimated time:** 3 hours
**Chapter link:** [`07-crm-hygiene-and-weekly-forecast.md`](../07-crm-hygiene-and-weekly-forecast.md)
**Prerequisite:** Chapter 7 read end-to-end; Exercises 02-05 (real or role-played deals exist to file); a chosen CRM tool (HubSpot Free, Attio, Pipedrive, Salesforce, or a Google Sheet — see Chapter 7).

## Problem statement

Chapter 7 named the connective tissue that turns 20-30 individual deals into a legible operating instrument: five load-bearing fields per opportunity, written stage exit criteria, a 45-minute weekly review with a six-part agenda, a Commit / Best-case / Pipeline honest forecast, and 8-12 win/loss reason codes that feed monthly ICP / pricing / product loops.

This exercise trains you to **stand up the actual CRM instrument** (populate the five fields on 8-12 real or working-sample opportunities), **write the stage exit criteria specific to your product**, **run one honest weekly forecast walk with a documented commit-vs-best-case-vs-pipeline classification**, and **install the reason-code list** with your product's specific variations. The output is a working CRM (not a design doc for one) plus a first weekly-forecast artifact the founder can defend.

The failure mode this exercise exists to catch: **the founder reads Chapter 7, buys HubSpot, adds 30 custom fields, populates none of them, forecasts by intuition anyway, and produces the same un-diagnosable pipeline the discipline was supposed to fix. The tool is not the discipline; the discipline is.**

## Requirements

Deliver a folder `exercise-06/` with:

- `part-a-crm-setup.md` — the chosen tool, the five-field schema, the reason-code list, the stage exit criteria.
- `part-b-populated-pipeline.md` — 8-12 opportunities filed against the schema, all fields populated honestly.
- `part-c-weekly-forecast-walk.md` — the six-part weekly review agenda run against Part B, with the Commit / Best-case / Pipeline classification and a defensible number.

### Part A — CRM setup (60 min)

Deliver `part-a-crm-setup.md`.

**A1 — Tool choice + rationale (10 min).** Name your chosen CRM and cite the fit-to-scale rationale from Chapter 7. If you are using a Google Sheet, include the exact column headers. If you are using HubSpot / Attio / Pipedrive / Salesforce, screenshot the deal-pipeline view or paste an export of the pipeline schema. The tool choice is not strategic; the discipline is — but the tool has to actually exist and be accessible for the pipeline population in Part B to be real.

**A2 — The five load-bearing fields (10 min).** Define each field in your chosen tool:

- `Stage` — the enum of 9 values (Prospect, Outreach, Discovery, Demo, Proposal, Close, Closed-Won, Closed-Lost, Nurture).
- `Next step + due date` — the free-text next action + the date field.
- `Dollar value (ACV or TCV)` — currency field, no TBD placeholders allowed.
- `Close date` — date field.
- `Reason code (on close)` — enum from the list in A4.

Include any tool-specific configuration notes (e.g., HubSpot pipeline stages, Attio object types, or spreadsheet formulas).

**A3 — The stage exit criteria (25 min).** Author the specific entry and exit criteria per stage, populated to your product. Follow Chapter 7's table shape:

```
Stage: {name}
Entry criterion: {what puts a deal in this stage}
Advance-to-next-stage exit criterion: {what specifically must be true — evidence-based, not vibe}
Regress-or-lose criterion: {what puts the deal back a stage or close-lost}
```

Cover all six operational stages. The point is that a colleague reading the criteria could apply them to a deal you have never described to them and reach the same stage designation you would — the transferability test from Chapter 8.

**A4 — The 8-12 reason-code list (15 min).** Populate Chapter 7's list, adjusting the wording for your product:

- **Won reasons (5 codes):** `PAIN_URGENT`, `ROI_CLEAR`, `CHAMPION_STRONG`, `COMPETITIVE_WIN`, `REFERRAL`.
- **Lost reasons (7 codes):** `NOT_ICP`, `NO_BUDGET`, `NO_URGENCY`, `FEATURE_GAP`, `LOST_TO_COMPETITOR`, `LOST_TO_STATUS_QUO`, `PROCESS_STALL`.

For each code, add:
- A one-sentence definition specific to your product.
- The specific *feedback loop* it feeds (mod-104 ICP drift, mod-106 pricing, product roadmap).

Add up to 2 product-specific codes if the standard 12 miss something load-bearing. Do not exceed 14 total — the discipline is aggregation, not enumeration.

### Part B — Populate the pipeline (75 min)

Deliver `part-b-populated-pipeline.md`. Populate 8-12 opportunities in your chosen tool with all five fields honestly filled.

If you have a real pipeline, use it. If not, use opportunities from Exercises 02-05 (role-played discovery calls, role-played demos) — extended with fabricated but plausible details as needed. Note fabricated deals with `<!-- needs-research -->`.

**Coverage requirements.** The 8-12 opportunities must span:

- All six operational stages (Prospect through Close) — at least 1 per stage.
- The ACV band from Exercise 03 — some SPICED-band, some MEDDIC-band, ideally at least 1 MEDDPICC-band.
- At least 2 opportunities in Nurture (with dated reactivation triggers).
- At least 1 recent Closed-Won and 1 recent Closed-Lost (with reason codes filled).

**The population honesty test.** For every field, ask: is this the real value, or the aspirational value? The exercise's whole point is honest state. A deal with a `Next step: TBD` or a `Dollar value: TBD` is a hygiene failure — either it has to be populated with a real value now, or the deal is not really open.

Include a per-deal one-paragraph note explaining any unusual value (e.g., "this deal has a very-long Close date because the buyer is post-planning-cycle").

### Part C — The weekly forecast walk (45 min)

Deliver `part-c-weekly-forecast-walk.md`. Run the six-part 45-minute review from Chapter 7 against Part B.

**C1 — No-next-step audit (5 min in the exercise).** List all Part-B deals with no next-step or a next-step past the due-date. For each, resolve: booked new step (with date) or close-losted (with reason).

**C2 — Stage-regression audit (5 min).** List any deal whose exit criterion (from Part A) was not met in the last week. Regress those deals to the earlier stage in Part B, and document the regression.

**C3 — Forecast walk (15 min).** For every deal in Proposal or Close, walk it one at a time and classify Commit / Best-case / Pipeline. Format:

```
Deal: {ID} — {name} — ${value}
Stage: {current}
Close date: {current}
Close-plan status: {which step, on time / slipped}
Biggest risk: {what could break}
Classification: Commit / Best-case / Pipeline
Rationale: {one sentence — "I would defend this to the board because..."}
```

Sum the Commit + Best-case totals; compare against your quarter target (real or invented for the exercise). Name whether you are on-plan or short.

**C4 — Stalled-deal review (5 min).** For every deal whose close date has slipped once or twice in Part B, name the specific "what has to change to unstick this?" — or close-lost if the third slip is imminent.

**C5 — Pipeline-coverage check (5 min).** Compute total open pipeline (Discovery + Demo + Proposal + Close). Compare against next-quarter target × 3x. If below 3x, name the specific front-of-funnel action for this week (increase outbound volume, run a webinar, kick off a referral push).

**C6 — Reason-code review (5 min).** For every Closed-Lost in Part B (real or in the last-week window), walk the reason codes. Which cluster? Does the cluster suggest a specific mod-104 ICP scorecard edit, a mod-106 pricing move, or a product roadmap change?

**C7 — The commit number (5 min).** Write the specific dollar number you would report to the board / co-founder / investor as "this is what we will hit this quarter" — with the one-paragraph defense.

## Starter guidance

- **Choose the smallest tool that works.** A Google Sheet with six columns is sufficient through the first 15-30 deals. Attio or HubSpot Free is fine. Salesforce is overkill at SEED and the customisation cost outweighs the discipline benefit. The tool is not strategic; the discipline is.
- **Populate `TBD` on nothing.** Every deal has a specific stage, a specific next-step, a specific dollar value, a specific close date. If you cannot populate one honestly, either the deal is not really open or the discipline has already broken.
- **The stage exit criteria are the transferability test.** Chapter 8's substitution test starts here. A colleague reading Part A's criteria should be able to independently classify a deal you have never described to them.
- **The forecast walk is where honesty gets tested.** Every deal in Commit is a deal you would defend to the board. If you are calling 12 of 12 open deals Commit, either you have an unusual pipeline (rare) or you are optimism-inflating. Chapter 7's honest classification is one-per-deal, defensible.
- **The no-next-step audit is done live.** Not deferred. If Part C reports "3 deals in the no-next-step column that I'll handle next week," the exercise's discipline-installation half is skipped. Resolve now.
- **Regression is healthy, not a failure.** A deal that has been in Proposal for 6 weeks with no signed proposal moves back to Demo. Honest state is the discipline; leaving deals in a favourable stage because it feels warm is the specific bias to catch.
- **The reason-code cluster is the monthly feedback loop.** Even in this one-week exercise, name the codes that clustered — the discipline of pattern-reading is what makes the codes useful.
- **The commit number is a bet.** Write it, own it, defend it. The exercise's final artifact — one number, one paragraph — is the muscle memory the weekly cadence builds over time.
- **The 45-minute time-box matters.** In real life the review is 45 minutes. This exercise's review is a similar time-box. If you cannot walk the pipeline in 45 minutes, either the pipeline is too big for a founder-scale motion or the schema is too heavy.

## Acceptance criteria

Your submission is complete when:

- [ ] Part A names a specific chosen tool with the fit-to-scale rationale and the schema captured (screenshot, export, or Google Sheet header row).
- [ ] Part A defines the five load-bearing fields with tool-specific configuration notes.
- [ ] Part A contains stage entry and exit criteria for all six operational stages.
- [ ] Part A contains the 8-12 (up to 14) reason-code list with one-sentence definitions and named feedback loops per code.
- [ ] Part B contains 8-12 opportunities populated in the actual tool (not just written on paper) with all five fields honestly filled.
- [ ] Coverage requirements met: all six operational stages, ACV band spans SPICED / MEDDIC / MEDDPICC, at least 2 in Nurture, at least 1 recent Closed-Won and 1 recent Closed-Lost with reason codes.
- [ ] No `TBD` values on any field; fabricated deals flagged `needs-research`.
- [ ] Part C — no-next-step audit resolved live during the exercise (new steps booked or close-losted with reasons filed).
- [ ] Part C — stage-regression audit performed, any regressed deals documented.
- [ ] Part C — forecast walk performed with a per-deal Commit / Best-case / Pipeline classification and a rationale sentence.
- [ ] Part C — pipeline-coverage check computed, front-of-funnel action named if coverage is below 3x.
- [ ] Part C — reason-code cluster named, specific mod-104 / mod-106 / product feedback identified if applicable.
- [ ] Part C — final Commit number written with one-paragraph defense.
- [ ] The full review walk fits into a 45-minute time-box.

## Common ways this exercise goes wrong

- **The over-configured-CRM trap.** Founder installs Salesforce and configures 30 custom fields. Populates 4. Fix: five load-bearing fields, done well; add fields only when a specific question makes them worth the maintenance cost.
- **The tool-with-no-discipline trap.** Beautiful HubSpot install; every deal has `Next step: TBD`. Fix: discipline is the point; tool is the substrate.
- **The TBD-fields trap.** Deals with `Dollar value: TBD` or `Close date: TBD`. Forecast is uncomputable. Fix: no TBDs; if you cannot populate, the deal is not really open.
- **The vague-next-step trap.** `Next step: follow up`. Fix: specific action, specific date, per Chapter 5's discipline.
- **The all-Commit forecast trap.** Every deal in Proposal or Close is classified Commit. Number is fiction. Fix: one-per-deal defensible classification; Chapter 7's Commit-accuracy calibration is the long-term instrument.
- **The stage-inflation trap.** Deals in Proposal that never had a real proposal sent. Fix: exit criteria applied honestly; deals regress when criteria not met.
- **The no-close-losts trap.** Every deal is open; nothing is close-losted. Fix: Chapter 5's 30-50% qualified-out rate is healthy; some deals close-lost every week.
- **The no-reason-codes-on-close trap.** Closed-Lost deals with `Reason code: blank`. Pattern un-diagnosable. Fix: reason code stamped same-day on close; enforced in the exit criterion.
- **The 40-reason-codes trap.** Founder adds a new reason code for every close-lost variation. Aggregate pattern lost. Fix: 8-12 codes maximum; nuance goes in a free-text comment field.
- **The forecast-in-Slack trap.** The Commit number lives in a Slack DM to the co-founder; not in the CRM. Not reproducible next week. Fix: forecast lives in the CRM (or the spreadsheet); export to a weekly document for the co-founder / board.
- **The no-pipeline-coverage-check trap.** Founder focuses on this-quarter deals; next-quarter pipeline is invisible. Miss shows up 8 weeks later. Fix: coverage math weekly.
- **The reason-code-doesnt-feed-back trap.** Reason codes stamped but never rolled up. Same product-gap code fires 5 times; roadmap never sees it. Fix: monthly reason-code rollup feeds mod-104 / mod-106 / product.
- **The forecast-walk-skipped trap.** Founder walks the pipeline in 12 minutes because the deals feel obvious. No classification rigor. Fix: 15-minute forecast walk with per-deal rationale, even for the "obvious" ones.
- **The 45-minute-time-box-blown trap.** Review takes 90 minutes because the pipeline is over-populated or the schema is too heavy. Fix: compress the pipeline or the schema; the founder-scale discipline is 45 minutes.
- **The one-time-not-recurring trap.** The exercise runs once; the weekly cadence never installs. Fix: schedule the same 45-minute slot next Monday and every Monday thereafter.
