# Exercise 05 — CRM Stages with a Qualification Artifact per Stage

**Estimated time:** 3 hours
**Chapter link:** [`05-crm-stages-and-qualification-artifacts.md`](../05-crm-stages-and-qualification-artifacts.md)
**Prerequisite:** Chapter 5 read end-to-end; a specific CRM in use (HubSpot / Salesforce / Attio / Close) or a plausible commitment to one; Exercise 01's motion brief (or an equivalent motion decision) — the stage model differs slightly for SDR-AE vs. enterprise vs. stacked PLG-plus-sales-assist. If you have never configured a CRM before, you may write the spec as a *configuration plan* rather than actually configuring in a tool — the discipline is the same.

## Problem statement

Chapter 5 named CRM discipline as the load-bearing infrastructure for any sales motion: 5-7 buyer-commitment-based stages, defined entry / exit criteria, a required artifact per stage, MEDDPICC or SPICED coverage panels per opportunity, calibrated forecast probabilities, weekly pipeline hygiene. The failure mode: the sales team advances deals through the CRM on gut feel — a deal moves to Discovery because the SDR booked a meeting, to Proposal because the AE sent a slide deck, to Negotiation because the buyer replied "let's chat about pricing" — with no artifact attached at any stage. The founder can't tell a healthy $500K deal from an air-pocket $500K deal until close date.

This exercise trains you to **design and configure the CRM stage set for your motion**, with entry / exit criteria and required artifacts per stage, and to run the pipeline-hygiene rituals against a sample pipeline to see what the discipline catches. The output is a runnable CRM configuration (or a configuration spec if you're not yet in a tool) plus a sample-pipeline audit that demonstrates the diagnostic in action.

The failure mode this exercise exists to catch: **the founder installs a CRM with default stages ("Lead / Opportunity / Proposal / Negotiation / Closed Won / Closed Lost") and default probabilities (10% / 25% / 50% / 75%), populates it with opportunities, and reports the pipeline forecast to the board — never noticing that the stages don't match her actual buying process, that the probabilities don't match her actual conversion rates, and that no artifact is required for any advancement**.

## Requirements

Deliver a folder `exercise-05/` with three files:

- `part-a-stage-configuration.md` — the stage set, entry / exit criteria, required artifacts, forecast probabilities.
- `part-b-panel-and-fields.md` — the MEDDPICC / SPICED panel spec, custom fields, and automation rules.
- `part-c-sample-pipeline-audit.md` — a walkthrough of 5-10 sample opportunities using the discipline; what the audit catches.

### Part A — Stage configuration (75 min)

Deliver `part-a-stage-configuration.md`.

**A1 — Stage set (10 min).** Adopt Chapter 5's working 6-stage model, or adapt to your motion:

```
Prospect → Discovery → Evaluation → Proposal → Negotiation → Close → Land / CS
                                                                     ↘
                                                              Closed Lost (with loss reason)
```

If you adapt, name each stage change and the rationale (e.g., "adding a POC stage between Evaluation and Proposal because our motion always paid-pilots"). Do not add stages > 8 total (Chapter 5's *stage-model-too-granular* trap). Do not reduce below 5 (Chapter 5's *stage-model-too-loose* trap).

**A2 — Per-stage spec (40 min).** For each stage, write:

```
## Stage {N} — {Name}

**Entry criterion**: {what makes a deal eligible to enter this stage}

**Exit criterion**: {what makes a deal ready to advance}

**Required artifact**: {the specific document / meeting / signal that must be attached to the opportunity as evidence of stage-exit}

**MEDDPICC / SPICED coverage required**: {which letters must be at least Yellow (or Green) to exit}

**Working forecast probability**: {%} — {calibration note: is this Chapter 5's default, or tuned against your historical conversion?}

**Diagnostic signal**: {a stage-specific pattern that indicates the deal is stalled and should be flagged}
```

Repeat for all stages including Closed Lost (with the loss-reason taxonomy from Chapter 5).

**A3 — Forecast probability calibration (15 min).** Chapter 5's default probabilities:

| Stage | Working probability |
|---|---|
| Prospect | 5-10% |
| Discovery | 15-25% |
| Evaluation | 30-40% |
| Proposal | 50-60% |
| Negotiation | 70-80% |
| Close | 90%+ |

If you have historical close data (from mod-105 founder-led sales or from an existing sales team), compute the actual close rate at each stage from your data and compare to the defaults. Report the gap. If actual close rates diverge materially, use *your* numbers, not Chapter 5's defaults — the default is a starting point, not the answer.

If you don't have historical data yet, use Chapter 5's defaults but note the plan to recalibrate at 30-90 days of pipeline history.

**A4 — Motion-aware probability differentiation (10 min).** If your motion is stacked (PLG + sales-assist + enterprise per Chapter 1's layer concept), note whether you need per-motion probability curves. A PLG PQL-triggered sales-assist opportunity typically closes at a higher rate than a cold-outbound SDR-AE opportunity at the same stage. Adjust the forecast probability by Motion type in the CRM (Chapter 5's Motion custom field is where this hangs).

### Part B — MEDDPICC / SPICED panel and custom fields (60 min)

Deliver `part-b-panel-and-fields.md`.

**B1 — Panel spec (20 min).** For each motion type your CRM will serve (mid-market SDR-AE / enterprise / PLG-triggered sales-assist), name the qualification-panel fields:

- **SPICED panel** (5 fields, Green / Yellow / Red): Situation, Pain, Impact, Critical Event, Decision. Applied to mid-market opportunities.
- **MEDDPICC panel** (8 fields, Green / Yellow / Red): Metrics, Economic Buyer, Decision Criteria, Decision Process, Identify Pain, Champion, Paper Process, Competition. Applied to enterprise opportunities.

Which motion uses which panel is set by the Motion custom field. Author the mapping explicitly.

**B2 — Custom fields (15 min).** Enumerate the custom fields on the opportunity object beyond the panels:

- **Motion** (categorical: PLG / Mid-Market / Enterprise). Determines panel and probability curve.
- **Champion Name** (text). Required at Discovery-exit.
- **Economic Buyer Name** (text). Required at Discovery-exit (Enterprise) or Proposal-exit (Mid-Market).
- **Critical Event / Close Date** (date). Required at Evaluation-exit.
- **ACV** (numeric). For pipeline rollups.
- **Loss Reason** (dropdown, using Chapter 5's taxonomy). Required for Closed Lost.
- Additional fields specific to your motion (e.g., "PLG source signal" for PLG-triggered opps; "POC status" for enterprise opps).

For each field: name, type, when it becomes required, default value, and validation rule (if any).

**B3 — Automation rules (15 min).** Chapter 5 names automation as blocking stage advancement when a required artifact is missing (with an override mechanism that is flagged). Author the automation rules:

- **Rule 1 — Stage-advance guard**: block stage advancement if the required artifact field is empty on Enterprise opps > $100K. Override permitted with a manager-visible note.
- **Rule 2 — Stale-deal flag**: opportunities with no activity in > 14 days (mid-market) or > 21 days (enterprise) are flagged for the weekly pipeline review.
- **Rule 3 — Loss-reason enforcement**: Closed Lost cannot be saved without a Loss Reason.
- **Rule 4 — Forecast-category discipline**: opportunities in Commit or Best Case for > 60 days (mid-market) or > 90 days (enterprise) auto-flag for downgrade review.
- Additional rules specific to your motion.

For each rule: trigger condition, action taken, notification recipients.

**B4 — Tooling choice and configuration reality (10 min).** Name the CRM tool your spec targets (HubSpot / Salesforce / Attio / Close). Note:

- What's natively supported (out of the box).
- What requires configuration or a plugin.
- What is manual-discipline-only (the tool cannot enforce; the sales team's culture has to).

Chapter 5's rule: the tool matters less than the discipline. Do not over-configure the CRM before the motion is validated (Chapter 5's *tooling-overreach* trap).

### Part C — Sample pipeline audit (45 min)

Deliver `part-c-sample-pipeline-audit.md`.

**C1 — Sample opportunities (10 min).** Enumerate 5-10 sample opportunities. Use real ones from your pipeline where possible; otherwise construct plausible cases from your discovery corpus or from Exercises 03 / 04.

For each opportunity, list:

- Opportunity name and rough deal shape (ACV, motion, stage-as-marked-in-CRM).
- Current MEDDPICC / SPICED grades (from Exercise 04 if applicable, or by fresh assessment).
- Required artifacts per stage: which are attached, which are missing.
- Last activity date.

**C2 — Audit walkthrough (25 min).** For each opportunity, apply the discipline:

- **Stage-integrity check** — does the actual state of the deal match the stage the CRM says it's in? If not, downgrade or flag.
- **Artifact check** — are the artifacts required for the current stage attached? If not, downgrade to the last stage where artifacts were complete.
- **Panel check** — do the MEDDPICC / SPICED grades honestly support the current stage per Chapter 5's stage-exit letter requirements? If not, downgrade the panel first, then the stage.
- **Stale-deal check** — has the deal had activity in the last 14/21 days? If not, flag and either revive or move to nurture / Closed Lost.
- **Forecast-probability check** — does the assigned probability match the actual state? If Best Case + Commit combined coverage is < 60% of quota, the pipeline is under-covered.

Report the diagnostic output per opportunity in a table:

| Opp | CRM Stage | Actual Stage | Artifacts | Panel Honest? | Stale? | Forecast Action |
|---|---|---|---|---|---|---|
| Acme Corp | Proposal | Discovery (proposal never sent) | Missing | No (M yellow, EB red) | Yes (18d) | Downgrade to Discovery; downgrade Best Case → Pipeline |
| ... | ... | ... | ... | ... | ... | ... |

**C3 — Diagnostic summary (10 min).** After the walkthrough, summarise what the audit caught:

- How many deals were at the wrong stage?
- How many were missing artifacts?
- How many had inflated panel grades?
- How many were stale?
- What is the net forecast change (Commit / Best Case / Pipeline / Omit)?

Name any pattern that spans multiple deals — e.g., "3 of 8 deals were in Proposal without an EB meeting; the AE has a pattern of skipping the EB step." Patterns that repeat across deals are coaching moments (Chapter 5's stage-integrity audit and Chapter 6's mismatch-diagnosis territory).

## Starter guidance

- **The stage set is a *system*, not a set of independent choices.** Every stage's exit criterion is the next stage's entry criterion. Every artifact requirement compounds — a deal at Proposal must have all Discovery + Evaluation artifacts already attached. Design the set as a whole; do not tune stages in isolation.
- **Buyer-commitment-based, not vendor-activity-based.** "Sent Proposal" is a vendor activity. "Buyer Verified Business Case" is a buyer commitment. Chapter 5 is explicit: activity-based stages are un-diagnosable because the vendor did the activity regardless of whether the buyer moved. Every exit criterion should describe *what the buyer has done*, not what the vendor has done.
- **Required artifacts are load-bearing.** The whole discipline hangs on the artifact — the discovery-notes doc, the evaluation summary, the proposal document, the negotiated-terms doc, the signed contract. If a stage has no required artifact, stage advancement becomes vibes-based. Every stage has a required artifact.
- **Forecast probabilities are *calibrated*, not assigned.** Chapter 5's defaults are starting points. Your actual close rate at each stage might diverge (a leaky Evaluation stage; a tight Discovery bar). Use your data if you have it; use the defaults if you don't and note the plan to recalibrate.
- **Motion-differentiation is real.** A PLG-triggered sales-assist opportunity at "Discovery" is meaningfully different from a cold-outbound SDR-AE opportunity at "Discovery" — the PLG one has already demonstrated intent. Do not use the same probability curve for both. Chapter 5's Motion field is the mechanism.
- **Automation should be enabling, not punitive.** Block stage advancement without artifacts, yes — but with an override mechanism that is visible in the weekly review. The goal is enforcement of discipline, not bureaucracy. If AEs are working around the automation, the rules are too tight or the artifacts are unclear.
- **The pipeline audit is where the discipline pays off.** A CRM with clean discipline is a diagnostic instrument. A CRM without discipline is a decorated spreadsheet. The audit in Part C is what turns "we configured the CRM" into "we can trust the forecast."
- **Downgrading is discipline, not shame.** If Part C's audit downgrades 30% of your Commit to Best Case or Pipeline, that is the CRM doing its job — surfacing the truth. The mistake is not the downgrade; the mistake is having called Commit those deals in the first place.
- **Loss-reason taxonomy is what turns lost deals into learning.** Chapter 5's loss codes (competitor / in-house build / do-nothing / price / feature gap / security gap / timing / champion departure / EB veto) are the primary input to Chapter 6's mismatch diagnosis. A Closed Lost without a loss reason is data you don't have.
- **Do not skip Closed Lost with a "we'll figure it out later" attitude.** Loss-reason patterns are the single most-diagnostic signal for a motion mismatch (Chapter 6). Enforce loss-reason coding on save.
- **Stale-deal audit is weekly, not quarterly.** Deals decay fast. A 14-day-stale mid-market deal or a 21-day-stale enterprise deal is a signal — either the AE re-engages or the deal drops back a stage / to nurture / to Closed Lost. Weekly hygiene keeps the pipeline honest; monthly hygiene lets bad pipeline compound.
- **Do not conflate the tool with the discipline.** A perfectly-configured Salesforce with no discipline is worse than a barely-configured HubSpot with rigorous discipline. Chapter 5 is explicit. If you're at seed, use HubSpot or Attio or Close and focus 90% of the effort on the discipline, not the configuration.

## Acceptance criteria

Your submission is complete when:

- [ ] Part A names a 5-7 stage set (Chapter 5's default or an adapted set with rationale for changes).
- [ ] Part A provides per-stage spec (entry / exit / required artifact / MEDDPICC or SPICED coverage / forecast probability / diagnostic signal) for every stage including Closed Lost.
- [ ] Part A reports forecast-probability calibration — either your historical close rates by stage or an explicit adoption of Chapter 5's defaults with a plan to recalibrate.
- [ ] Part A addresses motion-aware probability differentiation if your motion is stacked (PLG + SDR-AE + enterprise).
- [ ] Part B names the qualification panel(s) — SPICED for mid-market, MEDDPICC for enterprise — with the mapping to motion type.
- [ ] Part B enumerates custom fields (Motion, Champion Name, Economic Buyer Name, Critical Event / Close Date, ACV, Loss Reason, plus motion-specific fields) with type, required-at criteria, defaults, and validation.
- [ ] Part B authors 4+ automation rules (stage-advance guard, stale-deal flag, loss-reason enforcement, forecast-category discipline, plus motion-specific).
- [ ] Part B names the target CRM tool and honestly notes what's native, what needs configuration, and what is manual-discipline-only.
- [ ] Part C enumerates 5-10 sample opportunities with real or plausible detail, including current CRM stage, MEDDPICC / SPICED grades, artifact status, and last activity.
- [ ] Part C runs the audit walkthrough per opportunity (stage-integrity / artifact / panel / stale-deal / forecast checks) and reports the diagnostic action per opportunity in a table.
- [ ] Part C's diagnostic summary reports net forecast change (Commit / Best Case / Pipeline / Omit) and names any pattern spanning multiple deals.
- [ ] Any factual claim about a benchmark, a CRM feature, or a competitor's practice that is not from Chapter 5's cited sources or your own data is flagged `<!-- needs-research: ... -->` rather than invented.
- [ ] Sample opportunities that are constructed rather than real are labelled as such; the audit results on constructed opportunities are treated as mechanics demonstrations, not fielded findings.

## Common ways this exercise goes wrong

- **Default-stages trap.** Part A adopts HubSpot / Salesforce default stages ("Lead / Opportunity / Proposal / Closed Won") without adapting to the buyer's commitment journey. Stages are vendor-activity-based; discipline fails immediately. Fix: rewrite stages as buyer-commitment-based per Chapter 5.
- **Too-many-stages trap.** Part A adds 12 stages to capture every nuance. AEs skip stages or backfill retroactively. Fix: 5-7 stages maximum; the ones you keep have real buyer-commitment differentiation.
- **No-artifact-per-stage trap.** Part A names stages but doesn't specify the required artifact for stage exit. Vibes-based advancement is preserved. Fix: every stage exit requires a specific document / meeting / signal, named in the spec.
- **Default-probabilities trap.** Part A uses HubSpot's or Salesforce's default probabilities (10% / 25% / 50% / 75%) without calibrating to your actual conversion. Forecast is systematically wrong. Fix: A3 calibration against historical data, or explicit adoption of Chapter 5's defaults with a plan to recalibrate.
- **Panel-decoration trap.** Part B specifies the MEDDPICC / SPICED panel fields but no rule for how they get marked or reviewed. Panels become "always Green" fields that carry no signal. Fix: name the review cadence and the grading discipline; consider the "manager audits random 5 per week" habit from Chapter 5.
- **Automation-over-reach trap.** Part B's rules are so tight that AEs cannot advance any deal without a manager override. Bureaucracy replaces discipline. Fix: automation blocks obvious violations (missing critical field) but allows override with visibility; the goal is enforcement of the pattern, not punitive control.
- **Automation-under-reach trap.** Part B has no automation at all; every rule is "AE will remember." Nobody remembers. Fix: minimum viable automation — stage-advance guard for large deals, loss-reason enforcement, stale-deal flag.
- **Loss-reason-optional trap.** Loss Reason is a field but not required on save. Closed Lost deals close without reasons; win/loss retro has no data. Fix: workflow blocks Closed Lost without a Loss Reason.
- **Motion-single-panel trap.** Part B uses one panel (usually MEDDPICC) for all motion types. Mid-market opps get over-managed with enterprise ceremony. Fix: motion-specific panels — SPICED for mid-market, MEDDPICC for enterprise, sales-assist-light for PLG-triggered.
- **Sample-pipeline-too-optimistic trap.** Part C picks the healthiest 5 opps in the pipeline, audits them, finds nothing wrong, declares success. Fix: sample includes at least 3 opps you suspect are stale, over-graded, or wrong-stage; the audit is more useful on the messy ones.
- **Audit-without-downgrade trap.** Part C runs the audit but every problem is met with "the AE will fix it later." No forecast change; no downgrade; no coaching. Fix: each row in the audit table names the specific action (downgrade stage, downgrade forecast category, coach the AE, escalate to founder).
- **Configuration-first-motion-second trap.** Team spends 4 weeks configuring Salesforce before running a single opp through the motion. Configuration is theoretical because no discipline has been tested against real deals. Fix: minimum-viable configuration; ship the motion; add configuration as bottlenecks appear.
- **Never-recalibrate-probabilities trap.** Initial probabilities are set; never revisited even after 6 months of actual data. Forecast drift compounds. Fix: quarterly recalibration; if actual close rate at Discovery is 32% but the CRM says 20%, update the number.
- **No-cross-deal-pattern-diagnosis trap.** Part C reports per-opp findings but doesn't identify patterns spanning multiple deals ("3/8 opps at Proposal without an EB meeting"). Patterns are the coaching signal; individual findings are just cleanup. Fix: C3's pattern summary is required; patterns feed the Chapter 6 mismatch teardown.
