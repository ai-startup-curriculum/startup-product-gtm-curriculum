# CRM Hygiene and the Weekly Forecast

## Motivation

Chapters 1-6 built the six-stage motion and the artifacts each stage produces — outreach sequence, discovery script, demo checklist, next-step email, proposal template, close plan. Individually, each artifact makes one deal legible. Collectively — across 15, 25, 40 open opportunities in flight simultaneously — the artifacts only stay legible if they are *filed against a shared operating instrument*. That instrument is the CRM.

At founder-scale the CRM is not a hundred-column enterprise Salesforce install. It is a small, disciplined set of fields — stage, next step, dollar value, close date, reason code — updated on every deal, every week, with the same rigor the founder brings to the discovery script. It can live in HubSpot, Attio, Pipedrive, Salesforce, or a Google Sheet with six columns. The tool does not matter; the hygiene does.

The failure mode this chapter exists to catch: **the founder runs the motion by intuition — she "knows" which deals are hot, "knows" which champions are wobbling, "knows" the forecast in her head — and produces a pipeline that looks fine until the quarter closes and reality diverges from her head-model by 3-5x.** The board asks "how are we going to hit?" and the founder cannot answer without a spreadsheet she reconstructs from Slack messages and calendar invites. By month three, no one — not the founder, not the co-founder, not the seed investor, not the first AE joining next month — can trust the pipeline number.

The remedy this chapter ships: **five load-bearing fields per opportunity, one weekly review meeting with a specific agenda, a commit / best-case / pipeline forecast that names probabilities honestly, and a small set of win/loss reason codes that roll into monthly ICP / pricing / product feedback loops.** The CRM discipline is the connective tissue that turns 20-30 individual deals into a legible motion the first AE can inherit (Chapter 8) and an investor can read (mod-110).

## Core concepts

### The five load-bearing fields per opportunity

Every open opportunity — and every closed one — carries five fields the founder updates weekly. Nothing else matters at founder scale.

1. **Stage.** One of six values, matching Kazanjy's stage model from Chapter 1: `Prospect`, `Outreach`, `Discovery`, `Demo`, `Proposal`, `Close`. Plus three terminal values: `Closed-Won`, `Closed-Lost`, `Nurture`. Every deal is in *exactly one* stage at *any point in time*. A deal that "isn't really in Discovery but also isn't in Demo" is a hygiene bug — the previous stage's exit criterion was not met, or the current stage's entry criterion was not confirmed. Fix the entry / exit call, not the stage-name.
2. **Next step + due date.** Not "follow up." A specific action ("send proposal v2 with redline responses") with a specific date ("2026-04-17"). Chapter 5's discipline enforced at the CRM layer. The rule from Chapter 5 — every open deal has a calendared next step in the next 14 days or it is close-losted — is the field this rule audits against.
3. **Dollar value (ACV or TCV).** The current best estimate of the deal's annual contract value (ACV) — or total contract value (TCV) for multi-year. For deals pre-proposal, the estimate is a range compressed to a mid-point ("$10-15K → $12K"). Post-proposal, it is the number on the proposal. Never a placeholder like "TBD" — a deal without a dollar estimate cannot be forecast, weighted, or ranked.
4. **Close date (or `Nurture until` date).** The specific date the deal is expected to close. Not "this quarter"; a date. For deals with a critical event (SPICED's "C"), the close date is anchored to the event; for deals without, it is anchored to the average cycle length. A deal whose close date has slipped twice in a row is a signal — investigate the underlying gate before slipping a third time.
5. **Reason code (on close only).** When a deal closes — won or lost — it is stamped with a reason code from a small controlled list (see below). The reason codes are what make weekly noise legible as a monthly pattern.

Five fields. That is the whole load-bearing schema. Every other field a CRM makes available — activity counts, email opens, deal source, campaign attribution — is optional decoration at founder scale; add them only when a specific question makes them worth the maintenance cost.

### The stage exit criteria — what puts a deal in each stage

Stage names are useless without stage *exit criteria*. Every stage's exit criterion is what the CRM discipline enforces on the weekly review; without a written exit criterion, stages become vague and the pipeline becomes fiction.

| Stage | Entry criterion | Exit criterion (advances to next stage) | Exit criterion (moves back / lost) |
|---|---|---|---|
| **Prospect** | Account added to ICP list | Named contact + persona identified + pre-outreach research complete | Removed from list (ICP miss) |
| **Outreach** | First touch sent | First meeting booked with named contact | Sequence exhausted, no reply → Closed-Lost (reason `NO_REPLY`) or move to Nurture |
| **Discovery** | First meeting scheduled | SPICED/MEDDIC coverage complete + verdict = Qualified In + demo booked on the call | Verdict = Qualified Out (reason coded) → Closed-Lost |
| **Demo** | Discovery-qualified + audience confirmed | Pain-addressing workflows shown + ROI framed + next-step booked (proposal or follow-up) | Buyer/champion/user missing at demo, OR feature-gap disqualifier fires → Closed-Lost |
| **Proposal** | Buyer + champion aligned + demo verdict positive | Proposal sent + close-plan written + redline round 1 initiated | Proposal declined or ignored for 14+ days after nudge → Closed-Lost |
| **Close** | Proposal out + redlines in flight | Signed + counter-signed + invoiced + kickoff booked → Closed-Won | Redlines stall > 30 days without owner-driven revival → Closed-Lost |

Two disciplines fall out of the exit criteria:

- **Advancing a stage requires the exit criterion to be met on the call, not "in the founder's head."** A demo that ended with "let me follow up with times" does not advance to Proposal; it stays in Demo with a next-step of "book the proposal-review call by Friday." The instinct to advance the stage because the deal *feels* hot is the specific failure mode this discipline catches.
- **Regressing a stage is a permitted, healthy move.** A Proposal-stage deal whose champion goes dark for two weeks moves *back* to Demo (or is close-losted). The regression is the honest signal; keeping the deal in Proposal because "the ACV is high and I don't want to lose it from the forecast" is the founder-optimism bias Chapter 7 exists to catch.

### The weekly review — the 45-minute meeting that runs the motion

The weekly pipeline review is a 45-minute standing meeting the founder runs with herself (until there is a first AE, at which point the AE joins). It has a specific agenda; without one, the review turns into vague deal-storytelling that consumes time without producing decisions.

The agenda, roughly:

1. **The no-next-step audit (5 min).** Filter the CRM to open deals with no next-step or a next-step past due. Every deal in that list ends the review with one of two outcomes: (a) a specific new next-step scheduled on the calendar before the review ends, or (b) close-losted with a reason. There is no third fate. This is the direct enforcement of Chapter 5's rule.
2. **The stage-regression audit (5 min).** Every deal whose exit criterion was not met last week is regressed to the earlier stage. This is the "honest CRM state" discipline — the founder resists the temptation to leave a deal in the higher stage because it feels warmer than the data supports.
3. **The forecast walk (15 min).** Every deal in `Proposal` or `Close` is walked one at a time — deal name, dollar value, current step in close plan, biggest risk, commit / best-case / omit classification (see next section). This is the source of the honest forecast.
4. **The stalled-deal review (10 min).** Every deal whose close date has slipped once or twice gets a specific "what has to change to unstick this?" conversation. Slipped twice = high-risk; slipped three times = close-lost (there is no fourth slip).
5. **The pipeline-coverage check (5 min).** How many dollars in `Discovery` + `Demo` + `Proposal` + `Close` vs. how many dollars the next 90 days needs? If coverage is below 3x quota, the front of the funnel is the bottleneck; if it is above 6x, the back-half discipline is the bottleneck. Chapter 2's outbound scoreboard is the input to this check.
6. **The reason-code review of last week's closed-lost (5 min).** Any deal closed-lost this week is walked briefly — what reason code, what pattern is it fitting into, does anything need to change on the ICP scorecard (mod-104) or the pricing pack (mod-106)?

Total: 45 minutes. Same day of the week (Monday morning is common — sets the week's priorities). Same agenda. Same fields walked. Repetition is the mechanic that makes the pipeline legible.

### The honest forecast — commit, best-case, pipeline

The single most-common founder-forecast failure is the **flat-probability forecast**: every open deal is at "70% likely" or "hot" or "committed," and the number the founder reports to the board is the sum. When the quarter closes, the founder lands at 20-40% of the number and cannot say which specific deals slipped. This is the failure Chapter 7's honest-forecast discipline exists to prevent.

The founder-scale honest forecast uses a three-band classification, borrowed from the practitioner literature (Sacks, Kellblog, McMahon):

- **Commit.** Deals the founder is willing to bet her personal credibility on for the quarter. Contract is out, redlines are in flight, close date is inside the quarter, no known blockers, champion is engaged, economic buyer is on board (for MEDDIC deals). Commit deals collectively become the number the founder reports as "we will hit this."
- **Best-case.** Deals that *could* close in the quarter but require specific things to go right — a stakeholder alignment, a security review clearing on time, a redline that could go either way. Best-case is a *stretch* forecast; the honest number is Commit, and Best-case is what the founder reports as "here is what a good quarter looks like if these five things break our way."
- **Pipeline.** Everything else that is open but not closing in the quarter. Deals in earlier stages, deals whose close date is next quarter, deals whose champion is still building the internal case. Pipeline is a *coverage* metric — it should be 3-5x the next quarter's target to sustain the motion — not a forecast for this quarter.

The classification is applied per deal, in the weekly forecast walk, with a specific "why" attached to the classification. "Acme is Commit because the CFO signed off, redlines are down to two, close plan says day 34" is a defensible classification; "Acme is Commit because I have a good feeling" is not. The Commit number that comes out of the review is what the founder should be willing to defend to a board member; if she wouldn't defend it, it is not Commit.

Two health signals fall out of the classification:

- **Commit accuracy over time.** After 4-6 quarters of running the discipline, the founder's Commit-vs-actual ratio should be 85-105%. Chronically under 70% means Commit is too optimistic (the founder is classifying Best-case deals as Commit); chronically over 120% means Commit is too conservative (the founder is under-forecasting to sandbag). Both are correctable; neither is visible without the discipline.
- **Best-case slippage.** Best-case deals that slip to next quarter are not failures — they are what "best-case" means. But if 80% of Best-case slips, either the Best-case classification is too optimistic (deals with real risk are being called Best-case rather than Pipeline) or the sales cycle is longer than the founder is modelling.

### The win/loss reason codes — a small controlled list

Every closed deal — won or lost — is stamped with a reason code from a small controlled list. The list has 8-12 codes; more and the codes lose discriminating power, fewer and patterns get flattened into a single bucket.

A working reason-code list for founder-led SaaS motion:

**Won reasons (5 codes):**

- `PAIN_URGENT` — the buyer had a critical event (SPICED's "C") that forced the decision by a date. The deal closed because the deadline was real.
- `ROI_CLEAR` — the ROI math from discovery + demo was so compelling that the deal closed on the numbers alone. Typically deals with a > 5x annualised payback.
- `CHAMPION_STRONG` — the champion drove the internal sale hard, brought the economic buyer along, defended the vendor internally. The deal closed on the champion's political capital.
- `COMPETITIVE_WIN` — the deal was actively evaluated against an incumbent or competitor, and the vendor won on a specific dimension (feature, price, integration, support).
- `REFERRAL` — the deal closed because a trusted third party (customer, investor, mutual advisor) endorsed the vendor. The referral shortened the sales cycle dramatically.

**Lost reasons (7 codes):**

- `NOT_ICP` — the deal was outside the ICP (mod-104) and never should have advanced past Discovery. Retrospectively, a scorecard failure — feedback into the ICP.
- `NO_BUDGET` — the buyer had the pain but not the budget in the current cycle. Timing-fit failure (mod-104 Chapter 5). Nurture until the budget window opens.
- `NO_URGENCY` — the pain was real but not urgent enough to force a decision. Missing critical event (SPICED's "C"). Deal drifted; may re-open when urgency arrives.
- `FEATURE_GAP` — the product does not have a feature the buyer treats as a hard requirement (SSO, on-prem, a specific integration). Whole-product-gap disqualifier (mod-104 Chapter 3). Feedback into roadmap.
- `LOST_TO_COMPETITOR` — the deal was actively evaluated and the buyer chose a competitor (or "we'll build it in-house"). The specific competitor is named; the specific reason (feature, price, incumbency) is captured in a comment.
- `LOST_TO_STATUS_QUO` — the buyer decided to do nothing. Neither the vendor nor a competitor won. Often the honest translation of "we'll revisit next year" — the pain is not urgent enough.
- `PROCESS_STALL` — the deal died in procurement / security / legal — not because the buyer changed her mind, but because the paper process (MEDDPICC's "P") outlasted the deal's political momentum. Common on enterprise deals with weak champions.

The codes are consciously kept short. A code like `LOST_TO_STATUS_QUO` is more useful than a free-text "we'll revisit later" because it aggregates — a founder who sees 40% of her losses in `LOST_TO_STATUS_QUO` has a specific problem (urgency-creation, or ICP-selection against buyers with a genuine forcing function) and a specific place to intervene (the discovery-call critical-event question).

The reasons feed into three monthly review loops:

- **`NOT_ICP` and `FEATURE_GAP`** feed the mod-104 ICP drift diagnosis. If 30% of losses are `NOT_ICP`, the outbound targeting or the inbound-qualification filter is broken.
- **`NO_BUDGET` and `NO_URGENCY`** feed the mod-104 timing-fit calibration. If half the losses are timing-fit failures, the discovery-call critical-event question needs sharpening or the ICP is being defined too loosely on timing.
- **`FEATURE_GAP`** feeds the roadmap. Three deals lost to the same missing integration in a quarter is a build decision, not a "we'll get to it later."

### The daily-hygiene minimum

Weekly reviews only work if the daily inputs are clean. The daily-hygiene minimum is small:

- **After every meaningful conversation (call, email exchange, LinkedIn thread), update the deal's `Next step` field within 2 hours.** This is the CRM half of Chapter 5's 2-hour rule. The next-step email and the CRM update are the same reflex.
- **After every stage transition (Discovery → Demo, Demo → Proposal), advance the stage in the CRM the same day.** Delayed stage transitions poison the weekly review — the founder walks a Deal-still-in-Discovery that actually already ran a demo, and the pattern is unreadable.
- **After every close (won or lost), stamp the reason code the same day and file the deal.** Reason-code assignment done a week later is done from memory and drifts toward the founder's rationalisation of the outcome, not the actual cause.

Three actions, all under 60 seconds each. Founders who skip them find that the Monday review takes 90 minutes of reconstruction instead of 45 minutes of walking clean data.

### The tool choice — HubSpot, Attio, Salesforce, or a spreadsheet

The CRM tool at founder scale is not a strategic decision. Any of the following works if the discipline is applied:

- **HubSpot Free / Starter.** The most common default at SEED — free CRM, deal-stage kanban, next-step tracking, minimal setup. Sufficient through 100 customers.
- **Attio.** Newer, opinionated, popular with SEED B2B SaaS founders in 2024-2025. Similar shape to HubSpot; better UX for founder-scale usage. <!-- needs-research: verify Attio's founder-scale positioning claim against current product docs / recent user reviews -->
- **Pipedrive.** Deal-focused CRM with a strong pipeline-stage view. Common in outbound-heavy motions.
- **Salesforce.** Overkill at SEED — the customisation cost outweighs the discipline benefit. Suitable when the first AE hire or the first RevOps hire justifies the setup. Not the founder-scale default.
- **A Google Sheet with six columns.** Fully legitimate through the first 15-30 deals. Columns: `Deal name`, `Stage`, `Next step + date`, `Dollar value`, `Close date`, `Reason code (on close)`. The tool is honest about what it is; upgrade when the manual maintenance cost exceeds a few hours per week.

The failure is not tool choice; the failure is *no discipline on any tool*. A founder with a beautiful Salesforce install and no weekly review produces worse pipeline data than a founder with a six-column spreadsheet and a Monday-morning cadence.

### The pipeline-coverage math

The pipeline-coverage check in the weekly review needs a target. The working default at founder-led scale:

- **Commit + Best-case ≥ 100% of quarter target.** If Commit is short of the number and Best-case does not bridge the gap, the quarter is at risk before it starts — front-of-funnel activity (Chapter 2 outbound + any inbound) needs to spike now.
- **Total open pipeline (all stages Discovery→Close) ≥ 3x next-quarter target.** The 3x factor accounts for the fact that most deals slip, disqualify, or lose. A pipeline coverage below 3x is a leading indicator that next quarter will miss regardless of how well this quarter closes.
- **New pipeline added per week ≥ (quarter target ÷ 12 weeks × 3x coverage factor).** If the quarter target is $360K and coverage is 3x, weekly new pipeline addition should be ~$90K. Below that, the top of the funnel is running dry.

These are working numbers. The specific ratios vary with sales-cycle length, deal-size distribution, and win rate — a 6-month enterprise cycle needs higher coverage than a 6-week SMB cycle. Chapter 8's readiness diagnostic uses the *pattern* of coverage (rising / stable / declining over 4-8 weeks) more than the absolute number.

### The forecast-to-actual reconciliation

Once per quarter, the founder walks the previous quarter's forecast against the actual outcome, deal by deal:

- Deals that were Commit and closed: expected wins. Note the timing (early / on time / late).
- Deals that were Commit and did *not* close: the highest-signal misses. What happened? Which stage stall killed them? Was the classification wrong (should have been Best-case) or was the deal legitimately Commit and something specific broke?
- Deals that were Best-case and closed: pleasant surprises. Was the classification too conservative, or was the deal genuinely stretch and something specific broke *in the vendor's favour*?
- Deals that were Best-case and did not close: the expected slippage. Fine.
- Deals that were Pipeline and closed: something moved fast. Usually a compressed cycle from an urgent buyer.

The reconciliation produces two outputs: a Commit-accuracy calibration for the founder's own forecasting judgment, and a set of specific pattern-diagnoses (e.g., "three of my Commit misses stalled in security review — I need to start security earlier next quarter") that become concrete improvements to the motion.

## Concrete example — Loomly's month-6 weekly review

Jane runs the Monday-morning pipeline review at end of month 6. Pipeline has 26 open opportunities.

**No-next-step audit (5 min).** 3 deals with no calendared next step. Two are champions who went dark 10 days ago — Jane sends "revive or close-out" emails during the review with a Friday deadline. One is a deal Jane forgot to touch after the demo — she books a follow-up on the spot for Wednesday. All 3 have next-steps by end of the audit; none close-losted this week.

**Stage-regression audit (5 min).** 1 deal is regressed. It was moved to Proposal last week; on inspection, the champion never actually agreed to the demo audience Jane needed for economic-buyer sign-off. The deal moves back to Demo, and the next-step becomes "book the economic-buyer meeting by end of week." Regression is honest; leaving the deal in Proposal would have inflated the forecast.

**Forecast walk (15 min).** 8 deals in Proposal or Close. Jane walks each one:

- Acme Observability: Close stage, $10.2K MULTIYEAR (24 mo), redlines back, close plan says signature day 34 which is next Wednesday. **Commit.** Defensible — champion strong, CFO on board, no known blockers.
- BetaBank: Proposal stage, $18K, security review in week 2 of ~3, close plan says close day 45 (end of quarter, tight). **Best-case.** If security clears by day 21, closes on plan; if it slips, moves to next quarter.
- CharlieRetail: Proposal stage, $12K, champion went silent after redline round 1, no economic-buyer contact. **Pipeline.** Not this quarter; move to nurture unless champion revives by end of week.
- ... 5 more walked similarly.

Quarter target: $180K. Commit total: $132K. Best-case total: $46K. Commit + Best-case: $178K, just barely covering. Jane notes she needs one more Best-case-to-Commit conversion by end of month, or one Pipeline-to-Best-case escalation, or the quarter will land at ~73% of number.

**Stalled-deal review (10 min).** 2 deals have slipped their close date once; 1 has slipped twice. The twice-slipped deal is DeltaData — the champion is real but the buyer is a VP who has never engaged. Jane's decision: honest email to the buyer this week — "here's where we are, is this real for your Q4?" — and if no substantive reply by Friday, close-lost with `PROCESS_STALL`. Third slip is not an option.

**Pipeline-coverage check (5 min).** Open pipeline (Discovery + Demo + Proposal + Close): $520K. Next quarter target: $180K. Coverage: 2.9x. Slightly below the 3x target — the front of the funnel needs a mild spike. Jane sets a target of 25 new outbound accounts this week vs. the 18 baseline.

**Reason-code review of last week's close-lost (5 min).** 2 deals closed-lost last week. One is `NOT_ICP` (Layer-1 miss — the account looked like a GitHub shop from the outside but ran GitLab internally; a research-quality miss more than a scorecard miss). One is `NO_URGENCY` — the buyer confirmed the pain but had no forcing function; nurtured for a Q4 re-engagement. Neither is a scorecard change trigger this week, but Jane logs both for the monthly ICP review.

Total review time: 45 minutes. Every open deal has a next step; every stalled deal has a decision; the forecast is defensible; the front-of-funnel gap is a specific action for the week; the reason-code pattern is being tracked for the monthly rollup.

By month 6, this ritual has been running for 24 weeks. Jane's Commit accuracy over the last two quarters is 91% and 96% — the discipline works. The first AE, joining in month 9, will inherit a legible pipeline and a working forecast, not a diary the founder maintains in her head.

## Common failure patterns

- **The stage-inflation trap.** Founder advances a deal to Proposal because it "feels warm" without the exit criterion being met. Two months later, half the Proposal-stage deals never had a real proposal sent. Fix: written exit criteria per stage; deals do not advance without evidence.
- **The stage-stickiness trap.** Founder refuses to regress a deal from Proposal to Demo (or from Demo to Discovery) even when the deal's actual state has slipped. Pipeline inflates; forecast decouples from reality. Fix: regression is a healthy signal; the CRM state should match the actual deal state.
- **The vague-next-step trap.** "Follow up" or "check in" in the next-step field. Every deal looks fine on paper; nothing is actually scheduled. Fix: next step is a specific action with a specific date; audit weekly.
- **The dollar-value-TBD trap.** Deals without a dollar estimate. Forecast is uncomputable; pipeline ranking is impossible. Fix: even pre-proposal deals get a mid-point range estimate.
- **The floating-close-date trap.** Deal has "close date: Q3" as a bucket, not a date. Weekly slippage cannot be diagnosed. Fix: specific date per deal, revisited weekly, slip-triggers escalation.
- **The flat-probability-forecast trap.** Every open deal is "70% likely." The forecast is the sum; it is meaningless. Fix: Commit / Best-case / Pipeline classification with a specific "why" per classification.
- **The forecast-optimism trap.** Everything is Commit. Quarter lands at 40%. Fix: Commit-accuracy calibration over 4+ quarters; deals move to Best-case unless the founder is willing to bet her personal credibility.
- **The forecast-sandbagging trap.** Founder classifies real Commit deals as Best-case to "under-promise and over-deliver." Board loses trust in the number in the other direction. Fix: honest classification either way; sandbagging is a discipline failure, not a virtue.
- **The no-reason-code trap.** Deals close-lost without a coded reason. Six months later, no pattern is visible. Fix: 8-12 reason codes, stamped same-day on close, rolled up monthly.
- **The too-many-reason-codes trap.** 40 reason codes covering every nuance. No aggregate pattern is visible because every deal is coded uniquely. Fix: 8-12 codes only; add nuance in a comment field, not in a new code.
- **The reason-code-doesnt-feed-back trap.** Reasons are stamped but never reviewed. `FEATURE_GAP` for the same missing feature fires 5 times in a quarter; product roadmap has no idea. Fix: monthly reason-code rollup feeds the ICP drift review (mod-104), the pricing review (mod-106), and the product roadmap.
- **The no-weekly-cadence trap.** Founder reviews the pipeline "when it comes up." Deals rot; forecast is a reconstruction each time. Fix: fixed day + time, 45 minutes, same agenda every week.
- **The 90-column-CRM trap.** Founder tries to run enterprise-Salesforce fields at SEED. Every field is a maintenance burden and none of them are used. Fix: five load-bearing fields, done well. Add fields when a specific question makes them worth the cost.
- **The tool-swap trap.** Founder migrates from HubSpot to Attio to Pipedrive to Salesforce over 18 months. Each migration burns a week and loses history. Fix: pick a tool, commit for 12 months, migrate only when a specific first-hire or scale event justifies it.
- **The forecast-shared-in-Slack trap.** Founder posts the forecast in a Slack DM to her co-founder or investor; there is no reproducible artifact. Fix: forecast lives in the CRM (or the spreadsheet) and is exported to a standing weekly document that the founder-plus-co-founder or founder-plus-investor read from.
- **The no-reconciliation trap.** Quarter closes; founder never reconciles Commit vs. actual. Same forecasting biases repeat quarter after quarter. Fix: one hour at end of quarter walking deal-by-deal what closed, what slipped, and what the pattern says.

## Summary

- **Five load-bearing fields per opportunity** — Stage, Next step + date, Dollar value, Close date, Reason code (on close). At founder scale, this is the whole schema; every other field is decoration.
- **Six operational stages + three terminal states** matching the six-stage motion: `Prospect`, `Outreach`, `Discovery`, `Demo`, `Proposal`, `Close`, plus `Closed-Won`, `Closed-Lost`, `Nurture`. Every deal is in exactly one at any time.
- **Written stage exit criteria** enforce honest stage transitions. Advancing requires the exit criterion met on the call; regression to an earlier stage is a healthy honest signal, not a failure.
- **The weekly review** — 45 minutes, same day / time, six-part agenda: no-next-step audit, stage-regression audit, forecast walk, stalled-deal review, pipeline-coverage check, reason-code rollup.
- **Honest forecast in three bands** — Commit (founder-credibility-bettable), Best-case (stretch, requires things to go right), Pipeline (coverage, not this quarter). Each classification carries a specific "why."
- **Commit-accuracy calibration** over 4-6 quarters — 85-105% is healthy, chronic misses in either direction diagnose specific biases (over-optimism or sandbagging).
- **8-12 win/loss reason codes** stamped same-day on every close. Codes feed monthly loops: ICP drift (mod-104), pricing (mod-106), roadmap (product). More codes destroy pattern signal; fewer flatten distinct causes.
- **Daily-hygiene minimum** — post-call next-step update within 2 hours, stage transition same-day, reason code same-day on close. Skipping these turns the weekly review into a reconstruction exercise.
- **Tool choice is not strategic** at founder scale — HubSpot, Attio, Pipedrive, Salesforce, or a six-column Google Sheet all work if the discipline is applied. Discipline > tool.
- **Pipeline-coverage math** — Commit + Best-case ≥ 100% of quarter target; total open pipeline ≥ 3x next-quarter target; new pipeline per week ≥ (target ÷ 12 × 3x). Below the ratios, the front of the funnel is the bottleneck.
- **Quarterly forecast-to-actual reconciliation** — walk every Commit deal, every Best-case, every surprise. The pattern names specific improvements (start security earlier; sharpen the critical-event question; upgrade to MEDDIC on enterprise deals).
- Chapter 8 picks up the **first-hire readiness diagnostic** — the signals that say the motion, and the pack, are ready to be handed off.
