# CRM Stages and Qualification Artifacts — No Gut-Feel Advancement

## Motivation

A CRM is only as good as the discipline the sales team runs against it. A CRM with clean stages, honest forecasting, and MEDDPICC or SPICED artifacts attached to every opportunity is a diagnostic instrument — the founder can look at the pipeline and see *where* deals are getting stuck, *which* qualification letter is unaddressed at each stage, *why* the forecast is under or over. A CRM with vibes-based stage advancement — "the deal feels close," "the champion is really excited," "let's move it to Proposal" — is a graveyard for deals that never had qualification and a forecast the founder cannot trust.

The failure mode this chapter exists to catch: **the sales team advances deals through the CRM stages on gut feel — a deal moves to Discovery because the SDR booked a meeting, to Proposal because the AE sent a slide deck, to Negotiation because the buyer replied "let's chat about pricing" — with no artifact attached at any stage, no MEDDPICC letter marked green, no defensible reason the deal is at 60% probability vs. 30%. The founder can't tell the difference between a healthy $500K deal and an air-pocket $500K deal until close date, when the healthy one closes and the air-pocket one slips a quarter.**

This chapter builds the stage-with-artifact discipline. It defines a working CRM stage model that maps to both the mid-market SDR-AE motion (Chapter 3, SPICED-based) and the enterprise motion (Chapter 4, MEDDPICC-based); it defines the artifact each stage transition requires; it defines the stage-exit criteria that turn a stage transition into a defensible event rather than a mood; and it develops the pipeline-hygiene practice that makes the CRM a diagnostic rather than a scoreboard.

The result is a CRM the founder can look at on a Friday afternoon and know, with confidence, what will close this quarter and what won't — because every deal's forecast is grounded in a specific artifact for every stage it has passed through.

## Core concepts

### Why the CRM stage model matters

A CRM stage is a *checkpoint on the buying process*. The name of the stage matters less than the fact that (a) the stages are the same for every deal in the pipeline, (b) each stage has a defined exit criterion, and (c) advancement between stages requires a specific artifact. Without those three properties, the CRM becomes an opinion aggregator — every AE has her own definition of "Discovery," every stage means something different to the sales manager than to the AE, and the pipeline dashboard is un-diagnosable.

The three most-common failure modes for CRM stage models:

- **Too few stages** — a two-stage model (Open / Closed) tells you nothing about where deals are stuck.
- **Too many stages** — a 12-stage model (Contacted / Engaged / Interested / Meeting Set / Discovery / Qualified / Demo / POC / Business Case / Proposal / Negotiation / Verbal / Signed) creates so many transitions that AEs skip stages or backfill retroactively; the model becomes theatrical rather than diagnostic.
- **Stages defined by activity, not by buyer commitment** — "Sent Proposal" is an activity the vendor did; "Buyer Verified Business Case" is a state the buyer has entered. Activity-based stages are un-diagnosable because the vendor did the activity regardless of whether the buyer actually moved.

The working practitioner default (Kazanjy, Roberge, McMahon, Winning by Design) is **5-7 stages** with buyer-commitment-based exit criteria and required artifacts. This chapter develops the 6-stage default.

### The 6-stage working model

The working model this module uses — appropriate for both mid-market SDR-AE and enterprise motions, with different artifacts at each stage — is:

```
+---------+     +--------+     +----------+     +---------+     +-----------+     +------+
|1 Prospect| → |2 Discovery|→|3 Evaluation|→|4 Proposal|→|5 Negotiation|→|6 Close|
+---------+     +--------+     +----------+     +---------+     +-----------+     +------+
                                                                                      |
                                                                    +----------+     |
                                                                    |7 Land / CS |←--+
                                                                    +----------+
                                                                          |
                                                                    +----------+
                                                                    |Closed Lost |
                                                                    +----------+
```

Each stage is defined by:

- **Entry criterion** — what makes a deal eligible to enter the stage.
- **Exit criterion** — what makes a deal ready to advance to the next stage.
- **Required artifact** — the document / event / signal that must be attached to the opportunity as evidence of stage-exit.
- **MEDDPICC or SPICED coverage** — which letters must be green (or explicitly acknowledged as red-with-mitigation) to exit.
- **Forecast probability** — the working probability the deal closes this quarter given it is at this stage.

Working probabilities are calibrated per-team by looking at historical conversion — the numbers below are practitioner defaults from Winning by Design and McMahon; every team should tune to its own conversion data:

| Stage | Working probability |
|---|---|
| 1 Prospect | 5-10% |
| 2 Discovery | 15-25% |
| 3 Evaluation | 30-40% |
| 4 Proposal | 50-60% |
| 5 Negotiation | 70-80% |
| 6 Close | 90%+ |

A team that reports 60% probability at Discovery has either wildly optimistic culture, or a Discovery bar so tight it functions as Evaluation. The probabilities are a diagnostic — mismatched to actual conversion, they signal a bar-setting problem.

### Stage 1 — Prospect

- **Entry criterion**: Target-account list includes the account; SDR (or founder-as-SDR) has begun cadence execution, OR PQL has fired from a PLG signal (Chapter 2), OR inbound reply has been received from marketing content.
- **Exit criterion**: Buyer (or buyer-adjacent contact) has replied positively AND a discovery meeting is scheduled with a calendar-confirmed attendee.
- **Required artifact**: Meeting invite in calendar, accepted by the buyer.
- **SPICED/MEDDPICC coverage**: Prospect-stage MEDDPICC hypothesis written from public information — likely Economic buyer, likely Champion candidates, obvious Competition, first-pass Metrics estimate.
- **Working probability**: 5-10%.

**Diagnostic signal**: a Prospect-stage that stays open for > 90 days with no meeting scheduled is nurture, not pipeline — move to a separate nurture stage and stop counting toward pipeline coverage.

### Stage 2 — Discovery

- **Entry criterion**: Discovery meeting scheduled (or held); qualification is beginning.
- **Exit criterion**: SPICED coverage complete for mid-market (Situation, Pain, Impact, Critical event, Decision); or MEDDIC Champion + Identify Pain + first-pass Metrics for enterprise. Buyer has confirmed enough interest to invest time in a technical evaluation or a formal demo.
- **Required artifact**: **Discovery-notes document** attached to the opportunity, with SPICED (or MEDDIC) letters filled in, including named individuals for champion, buyer, and (if MEDDIC) economic buyer.
- **SPICED/MEDDPICC coverage**: SPICED for mid-market; for enterprise, MEDDIC Champion, Identify Pain, Metrics (first-pass), Economic buyer (identified by name, not yet met).
- **Working probability**: 15-25%.

**Diagnostic signal**: a Discovery-stage that has been open > 45 days without a written discovery-notes artifact is not actually at Discovery; either the meeting never happened, or the AE didn't run discovery. Either way, the deal is back at Prospect until the artifact exists.

### Stage 3 — Evaluation

- **Entry criterion**: Buyer has agreed to a technical evaluation, a POC / pilot, or a formal product demo with the buying committee.
- **Exit criterion**: Technical evaluation complete with a defensible outcome; buyer has moved from "interested" to "planning how to buy." For enterprise: MEDDIC Decision Criteria surfaced against the actual RFP / eval scorecard; Metrics document refined with POC data; Competition mapped explicitly.
- **Required artifact**: **Evaluation summary** — POC results doc (if paid pilot), technical-eval scorecard, or demo-feedback notes. For enterprise: MEDDPICC coverage doc updated with Decision Criteria, refined Metrics, Competition mapping.
- **SPICED/MEDDPICC coverage**: SPICED complete + Decision-process first-pass (mid-market); MEDDIC Decision Criteria + Decision Process + Metrics refined + Competition mapped (enterprise).
- **Working probability**: 30-40%.

**Diagnostic signal**: an Evaluation-stage deal that has no POC outcome, no evaluation scorecard, or no completed demo cycle after 60 days is either an air-pocket (buyer disengaged) or a POC-as-permanent-free-trial pattern (Chapter 4). Escalate the diagnosis.

### Stage 4 — Proposal

- **Entry criterion**: Buyer has requested a proposal, or the AE has proposed sending one and the buyer has agreed.
- **Exit criterion**: Proposal sent, buyer has reviewed, and buyer has entered a negotiation posture (redlining terms, negotiating price, asking about contract length or payment schedule). For enterprise: Economic Buyer has been met and has signed off on the ROI story.
- **Required artifact**: **Proposal document** (Loomly-format proposal or Google Doc), sent-date logged, with a specific price, specific term, specific delivery / onboarding scope. For enterprise: Economic-buyer meeting notes; ROI document co-authored with champion.
- **SPICED/MEDDPICC coverage**: SPICED + Decision-process (mid-market); MEDDPICC with all letters at least yellow (Metrics green, Economic Buyer green, Champion green + trained, Decision Criteria green, Decision Process green, Identify Pain green, Paper Process at least mapped, Competition mapped).
- **Working probability**: 50-60%.

**Diagnostic signal**: a Proposal-stage deal that has been open > 45 days (mid-market) or > 90 days (enterprise) without a redline or a specific counter-proposal has stalled. Escalate; likely a MEDDPICC letter went red (usually Champion inactivity or Economic Buyer absence).

### Stage 5 — Negotiation

- **Entry criterion**: Buyer has begun negotiating specific terms (price, contract length, payment schedule, MSA redlines, security terms, DPA terms) with the specific intent to sign after negotiation completes.
- **Exit criterion**: All commercial and legal terms agreed; contract ready for signature; only the paper-execution step remains.
- **Required artifact**: **Negotiated terms document** — either a redlined MSA / SOW or a term sheet capturing the specific negotiated points. For enterprise: Paper-process map showing all remaining steps (procurement approval, legal countersign, executive sign-off, e-signature routing) with expected completion date per step.
- **SPICED/MEDDPICC coverage**: All letters green; Paper Process actively being worked; Competition explicitly resolved (no last-standing alternative pulling the deal).
- **Working probability**: 70-80%.

**Diagnostic signal**: a Negotiation-stage deal that has been in the same state > 30 days (mid-market) or > 60 days (enterprise) is usually stuck on a specific term. Escalate to sales manager or founder; often requires executive-level negotiation to unstick.

### Stage 6 — Close

- **Entry criterion**: Contract sent for signature; all terms agreed; e-signature routing initiated.
- **Exit criterion**: Contract countersigned by both parties; deal booked.
- **Required artifact**: **Signed contract** (or executed order form); PO if procurement path requires; deal booked in the billing system.
- **SPICED/MEDDPICC coverage**: All letters green; deal moves to Land / CS on countersign.
- **Working probability**: 90%+ once entered.

**Diagnostic signal**: a Close-stage deal that has been open > 14 days (mid-market) or > 45 days (enterprise) without countersign is usually stuck on a signature-level detail — a specific stakeholder is out of office, the buyer's e-signature routing is broken, or a paper-process step wasn't fully complete. Follow up daily.

### Stage 7 (post-close) — Land / CS

- **Entry criterion**: Contract countersigned; deal moves to Customer Success for onboarding.
- **Exit criterion**: Customer has activated (usually defined as PLG activation event for PLG-adjacent products, or completion of onboarding milestones for enterprise) and is on the retention track (mod-109).
- **Required artifact**: Onboarding plan; CS hand-off document from AE (including MEDDPICC coverage, champion notes, expansion hypothesis).
- **Working probability**: 100% (this is booked revenue).

The Land / CS stage is where mod-109's retention and expansion motion begins.

### Closed Lost

Any deal that fails to advance in a defined time-box (or is explicitly disqualified) moves to **Closed Lost** with a **loss-reason code**. Loss codes matter for win/loss analysis (mod-105 Chapter 6 develops this at the founder scale; mod-110 develops the org-scale version). Working loss-code taxonomy:

- **Lost to competitor** (name the specific competitor).
- **Lost to in-house build**.
- **Lost to "do nothing" / no decision**.
- **Lost on price**.
- **Lost on feature gap** (name the specific missing feature).
- **Lost on security / compliance gap** (name the specific gap).
- **Lost on timing** (deal deferred to next fiscal cycle; may re-enter as Prospect).
- **Lost on champion departure** (champion left the company).
- **Lost on Economic buyer veto** (name the objection).

A close-lost deal without a loss code is worse than a close-lost deal with one — the pipeline loses the diagnostic signal.

### Threading MEDDPICC through the stages — the artifact-per-stage discipline

The stage model above is generic; the artifact-per-stage discipline is what makes it MEDDPICC-native. For an enterprise deal, the CRM opportunity has a **MEDDPICC coverage panel** — a set of 8 fields (M, E, D, D, I, C, P, C) — each of which can be marked:

- **Green** — evidence exists; documented on the opportunity.
- **Yellow** — partially covered; evidence exists but has a gap.
- **Red** — no coverage; deal cannot advance until addressed.

Stage-exit criteria then map to specific letter states:

- **Discovery → Evaluation**: Champion GREEN, Identify Pain GREEN, Metrics YELLOW+, Economic Buyer YELLOW+ (identified by name).
- **Evaluation → Proposal**: Decision Criteria GREEN, Decision Process GREEN, Metrics GREEN, Competition YELLOW+ (mapped).
- **Proposal → Negotiation**: Economic Buyer GREEN (met), Champion GREEN (trained), all MEDDIC letters GREEN, Paper Process YELLOW+, Competition GREEN.
- **Negotiation → Close**: All 8 letters GREEN.

The MEDDPICC panel is not a compliance exercise — it is a diagnostic tool. When a deal is stuck, the panel tells you *which letter* is red; the coaching or intervention targets that letter specifically.

For mid-market SPICED deals, the panel is simpler — SPICED with 5 letters (Situation, Pain, Impact, Critical Event, Decision) — and the stage-exit criteria are correspondingly lighter. The principle is the same: named letters, named artifacts, defined exit criteria.

### The stage-exit checklist — how to run advancement in practice

At the weekly pipeline review (mid-market) or the weekly one-on-one deal review (enterprise), the AE walks each open deal through the stage-exit checklist:

1. **Which stage is the deal in?**
2. **Which MEDDPICC/SPICED letters are green, yellow, red?**
3. **What is the required artifact for advancement to the next stage — and is it attached to the opportunity?**
4. **What is blocking advancement — a specific letter red, a specific artifact missing, a specific stakeholder unresponsive?**
5. **What is the next-step action, with owner and due date, to unblock?**
6. **Is the forecast probability defensible given the actual state?**

This is not a five-minute exercise per deal at enterprise scale — a $500K deal deserves 10-15 minutes per pipeline review, sometimes 30 minutes in a dedicated deal review. Mid-market deals get 2-3 minutes each. The rhythm allocates time based on ACV.

The output of the pipeline review is a *committed forecast* — the AE (or founder) states, on the call, which deals are committed to close this quarter, which are best-case, which are pipeline, which are omitted. The commit is against the same categories mod-105 Chapter 6 develops for founder-scale forecasting: Commit / Best Case / Pipeline / Omit.

### Pipeline hygiene — the once-a-week discipline

CRMs decay. Every week, deals get stale, forecasts get optimistic, MEDDPICC letters get out of sync with reality. The **pipeline hygiene** discipline is the weekly (or daily, at scale) practice of keeping the CRM honest:

- **Stale-deal audit** — any deal that hasn't had activity (call, email, meeting) in > 14 days (mid-market) or > 21 days (enterprise) is flagged. Either the AE takes an action to revive, or the deal drops back a stage / to nurture / to Closed Lost.
- **Forecast reconciliation** — Commit + Best Case deals against actual quota; if the Commit is < 60% of quota, the pipeline coverage below is insufficient and the AE / SDR needs to increase top-of-funnel activity.
- **MEDDPICC-panel refresh** — any deal above $50K has its MEDDPICC panel reviewed weekly; letters that were green last week but the champion has gone silent might be yellow this week; downgrade honestly.
- **Loss-reason coding** — any Closed Lost from the previous week has its loss reason coded before Monday's pipeline review; the sales manager scans the loss reasons for patterns.
- **Stage-integrity audit** — a random sample of 5 opportunities per week are audited: does the actual state of the deal match the stage the CRM says it's in? Systematic drift (deals at Proposal without proposals sent) triggers stage-hygiene coaching.

Pipeline hygiene is a *cost* the sales team pays every week. The alternative — a decaying CRM — is an *asymmetric loss*: the founder / sales manager cannot forecast, cannot diagnose, cannot coach. The cost of hygiene is much less than the cost of a mis-forecast quarter.

### CRM tooling — what to use at each stage

The CRM tooling recommendation aligns with the SDR-AE motion in Chapter 3:

- **Seed / early Series A** (founder-led + first AE): **HubSpot** or **Attio** or **Close**. HubSpot is the modern default for early-stage teams — free tier is usable, mid-tier is affordable, and the ecosystem of integrations is deep. Attio is a strong choice for teams that want a modern data-model-first CRM. Close is an inside-sales-optimised alternative.
- **Series A / B** (multiple AEs, mid-market motion): **HubSpot** for teams starting with it; **Salesforce** for teams growing into enterprise-adjacent deals or expected to enterprise-scale.
- **Enterprise scale**: **Salesforce** is the practitioner default; the enterprise stack (Sales Cloud + Service Cloud + Marketing Cloud + Data Cloud) is over-configured for < $10M ARR teams but load-bearing above.

Whichever tool, the discipline is the same — the stages, artifacts, MEDDPICC panels, and pipeline hygiene are what matter. A perfectly-configured Salesforce with no discipline is worse than a barely-configured HubSpot with rigorous discipline. Tooling amplifies discipline; it does not create it.

### Common patterns of gut-feel advancement

The failure this chapter exists to catch is *gut-feel stage advancement* — deals moving through stages without artifacts, without MEDDPICC coverage, without defensible reasons. The most-common patterns:

- **"Feels like a Proposal now."** AE moves a deal from Discovery to Proposal because "the buyer seems engaged." No discovery-notes doc; no MEDDIC coverage; no proposal was ever sent because the deal wasn't ready. The forecast probability jumps from 25% to 55%; the founder's forecast is now over-stated.
- **"Champion is really excited."** AE moves a deal to Negotiation because the champion texted an enthusiastic message. No economic-buyer meeting; no ROI document; no paper process mapped. Deal close-losts at "our CFO said no" three weeks later.
- **"They asked about pricing."** AE moves a deal to Proposal because the buyer asked what things cost. Buyer was doing casual research; deal never advances past a first email exchange.
- **"POC is going well."** AE moves a deal to Proposal because the POC has been running for two weeks. POC has no defined success criteria; buyer hasn't committed to a decision meeting; deal is in perpetual pilot.
- **"They said end-of-quarter."** AE forecasts a deal at Commit for the quarter because the champion mentioned "we'd like to do this by end of quarter." No procurement engagement, no legal engagement, no signature routing. Deal slips.
- **"We know them."** AE keeps a Closed Lost deal in the pipeline because "we've known them for years" and it "might come back." Pipeline coverage is inflated; forecasting is un-realistic.

The remedy in every case is the same: **the artifact is either attached or the deal moves back**. A Proposal-stage deal without a proposal document reverts to Evaluation; a Negotiation-stage deal without a negotiated-terms document reverts to Proposal; a Commit forecast without paper-process mapping downgrades to Best Case.

## Concrete example — Loomly's CRM stage set-up

Loomly's CRM at Series A is HubSpot (chosen at seed and grown into). The team has one enterprise AE + one mid-market AE + two SDRs + one sales-assist rep (feeding from the PLG top-of-funnel per Chapter 2). Six-stage model with SPICED discipline for mid-market and MEDDPICC discipline for enterprise:

**Custom fields on the opportunity object:**

- **Motion**: PLG / Mid-Market / Enterprise (categorical). Determines which qualification panel is required.
- **SPICED Panel** (5 fields, Green/Yellow/Red): Situation, Pain, Impact, Critical Event, Decision. Required for Mid-Market opps.
- **MEDDPICC Panel** (8 fields, Green/Yellow/Red): Metrics, Economic Buyer, Decision Criteria, Decision Process, Identify Pain, Champion, Paper Process, Competition. Required for Enterprise opps.
- **Champion Name**: text field. Required at Discovery-exit.
- **Economic Buyer Name**: text field. Required at Discovery-exit (Enterprise) or Proposal-exit (Mid-Market).
- **Critical Event / Close Date**: date. Forecasted close date; required at Evaluation-exit.
- **ACV**: numeric. Rolls up to pipeline dashboards.
- **Loss Reason**: dropdown (using the taxonomy above). Required for Closed Lost.

**Required artifacts per stage:**

- **Discovery → Evaluation**: SPICED coverage doc attached (Google Doc link on opportunity). For enterprise: MEDDIC coverage doc with named Champion and Economic Buyer.
- **Evaluation → Proposal**: POC results doc or demo-feedback notes. For enterprise: MEDDPICC coverage doc with Decision Criteria + Competition mapping.
- **Proposal → Negotiation**: Proposal doc + Economic-buyer meeting notes (enterprise).
- **Negotiation → Close**: Negotiated terms doc + Paper Process map (enterprise).
- **Close → Land**: Signed contract + CS hand-off doc.

**Stage automation**: HubSpot workflow blocks stage advancement if the required artifact field is empty on Enterprise opps > $100K. AEs can override with a note, but the override is flagged in the weekly review.

**Pipeline review cadence:**

- **Daily** (5-10 min): each AE reviews own pipeline for stalled deals, hygiene issues, forecast changes.
- **Weekly Monday standup** (15 min mid-market, 30 min enterprise): each AE walks through Commit + Best Case deals; MEDDPICC/SPICED panel reviewed; forecast committed.
- **Weekly Friday forecast** (30 min): sales manager (or founder) rolls up team forecast; commits are named; slippage risks are called out.
- **Monthly deal review** (60 min): top 10 open enterprise opps and any open opp > $500K walked through in detail; MEDDPICC gaps addressed; specific interventions assigned.
- **Quarterly win/loss retro** (90 min): closed-won and closed-lost from the quarter reviewed; loss-reason patterns identified; process changes proposed.

**Diagnostic use of the CRM**: at the end of Q3, the mid-market AE's pipeline shows 40% of Evaluation-stage opportunities stuck > 60 days. Diagnosis: the AE has been running Evaluations without paid pilots, so buyers have no commitment to advance. Prescription: introduce paid pilots for all enterprise-adjacent Evaluation-stage deals; keep evaluation as demo-only for pure mid-market deals; track pilot-to-Proposal conversion separately.

**Diagnostic use for the enterprise AE**: a $600K opportunity has been at Proposal for 90 days. MEDDPICC panel review: Economic Buyer is YELLOW (never met, only heard about). Prescription: AE + founder together request a 30-minute meeting with the Economic Buyer; if the meeting doesn't happen within 3 weeks, the deal is downgraded from Best Case to Pipeline (the forecast probability drops from 55% to 30%).

The CRM's discipline is what makes both diagnoses possible. Without stage-exit artifacts and MEDDPICC panels, both deals would be at "60% probability" indefinitely, contributing to a forecast the founder could not trust.

## Common failure patterns

- **Stage-advance-on-vibes trap.** AE advances deals because the deal "feels" further along. No artifact, no MEDDPICC coverage. Forecast becomes fiction. Fix: artifact required for stage advancement; automation blocks skipped artifacts.
- **Skipped-stage trap.** AE moves an opportunity directly from Discovery to Negotiation because "there's no need for a formal proposal — they're ready." No evaluation, no proposal doc, no Economic Buyer meeting. Deal close-losts at the last minute on a term that would have surfaced at Proposal stage. Fix: stages are not skippable; every deal passes through every stage; skipping is a hygiene violation.
- **MEDDPICC-panel-as-decoration trap.** Panel fields exist but AEs mark everything green regardless of actual coverage. Panel is theatrical, not diagnostic. Fix: manager reviews random-sample panels weekly; downgrade any letter without evidence; coaching moment.
- **Stage-model-too-granular trap.** Team creates 12 stages to capture every nuance; AEs skip stages or backfill retroactively; forecasts across teams don't align because different AEs interpret stages differently. Fix: 5-7 stages max; buyer-commitment-based, not activity-based.
- **Stage-model-too-loose trap.** Team has 3 stages (Open / Working / Closed); pipeline dashboard tells you nothing about where deals are stuck. Fix: 5-7 stages minimum; each with defined exit criteria.
- **Stale-deal-accumulation trap.** Team never audits stale deals; pipeline grows to 4× actual pipeline; forecast coverage looks great; actual close rate is 8%. Fix: weekly stale-deal audit; deals with no activity > 14/21 days go back a stage or to Closed Lost.
- **Forecast-probability-mismatch trap.** Team uses default HubSpot / Salesforce forecast probabilities (10% / 40% / 60% / 90%); actual close rates at each stage are (20% / 25% / 35% / 55%). Forecast is systematically wrong. Fix: calibrate probabilities against historical conversion; update quarterly.
- **Loss-reason-blank trap.** Closed Lost deals close without a loss reason; win/loss analysis has no data. Fix: loss reason required; workflow blocks Closed Lost without one; sales manager reviews loss-reason patterns monthly.
- **No-pipeline-review trap.** Team never runs a pipeline review; each AE forecasts privately; manager rolls up numbers without diagnosis. Slippage is a surprise every quarter. Fix: weekly pipeline review with committed forecast on the call.
- **CRM-not-source-of-truth trap.** AEs keep pipeline in personal spreadsheets, in Slack DMs, in memory. CRM is out of date. Fix: CRM is the source of truth; if it's not in the CRM, it's not in the pipeline; sales manager only forecasts from CRM.
- **Proposal-as-lead-magnet trap.** AE moves deals to Proposal stage to send a proposal document to see if the buyer engages; buyer never engages; deal stalls at Proposal. Fix: Proposal stage requires buyer having *asked for* or *agreed to* a proposal after Evaluation is complete; not a stage the AE moves the buyer through unilaterally.
- **Ignored-negotiation-terms-doc trap.** Negotiation stage advances without a written terms doc; disagreements about what was agreed surface at Close. Fix: negotiated-terms doc required for Negotiation → Close.
- **Perpetual-Prospect trap.** Deals sit in Prospect stage for 6+ months because "the SDR is still working on it." Nurture masquerading as pipeline; pipeline coverage looks inflated. Fix: 90-day cap on Prospect stage; move to nurture or Closed Lost.
- **Not-reviewing-slippage trap.** Deals slip a quarter without diagnosis; team just moves the close date. Fix: slippage triggers a MEDDPICC-panel review; the specific letter that was red gets named; coaching addresses it.
- **Tooling-overreach trap.** Team invests months configuring Salesforce with custom objects, workflows, and validation rules before the motion is stable. Configuration outlasts the motion; team ends up working around the tool. Fix: minimum-viable CRM configuration first; add complexity as the motion earns it.

## Summary

- The CRM is a **diagnostic instrument** — clean stages + honest forecasts + MEDDPICC/SPICED artifacts per opportunity = a pipeline the founder can trust. Vibes-based CRM = pipeline debt with no diagnosis.
- **Stage model**: 5-7 stages, buyer-commitment-based, defined entry / exit criteria, required artifact per stage. The working default: **Prospect → Discovery → Evaluation → Proposal → Negotiation → Close → Land / CS + Closed Lost with loss code**.
- Each stage has (a) an **entry criterion**, (b) an **exit criterion**, (c) a **required artifact**, (d) the **MEDDPICC/SPICED letters that must be green** to exit, (e) a **working forecast probability** calibrated against team-specific historical conversion.
- **MEDDPICC panel** — 8 fields on the enterprise opportunity, each marked Green / Yellow / Red. Stage-exit criteria map to specific letter states. The panel is a diagnostic — when a deal is stuck, the panel tells you which letter to work.
- **Mid-market motions** use a lighter **SPICED panel** (5 fields) with less-heavyweight artifact requirements. The stages are the same; the required artifacts scale with ACV.
- **Pipeline hygiene** is a weekly discipline — stale-deal audit, forecast reconciliation, MEDDPICC-panel refresh, loss-reason coding, stage-integrity audit. The cost of hygiene is much less than the cost of a mis-forecast quarter.
- **Pipeline review cadence** — daily hygiene (5-10 min per AE), weekly team standup with committed forecast, weekly Friday forecast roll-up, monthly deal review for top opps, quarterly win/loss retro. Rhythm scales with ACV — enterprise motions require more coordination time than mid-market.
- **Forecast categories** — Commit / Best Case / Pipeline / Omit — with a committed forecast made on the pipeline call, not in a dashboard cell.
- **Loss-reason codes** — a defined taxonomy (lost to competitor / in-house build / do-nothing / price / feature gap / security gap / timing / champion departure / EB veto). Loss patterns feed the win/loss retro; missing loss codes rob the team of the diagnostic.
- **Tooling**: HubSpot / Attio / Close at seed; HubSpot / Salesforce at Series A/B; Salesforce at enterprise scale. The **discipline** (stages + artifacts + panels + hygiene) matters more than the tool.
- **Common failure modes** — stage-advance-on-vibes, skipped-stage, MEDDPICC-panel-as-decoration, stale-deal-accumulation, forecast-probability-mismatch, loss-reason-blank, no-pipeline-review — are all fixable at the process level once the artifact-per-stage discipline is enforced.
- Chapter 6 develops the **motion mismatch diagnosis** — how to read the CRM signals to detect when the motion itself is wrong for the market, not just when the discipline has slipped.
