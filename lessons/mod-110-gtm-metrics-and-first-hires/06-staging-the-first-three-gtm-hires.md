# Staging the First Three GTM Hires — Triggers and the Over-Hire Trap

## Motivation

The numbers from Chapters 2–5 have a specific downstream use: they *time* the first GTM hires. A founder who reads the one-pager well but hires the first AE at the wrong moment burns twelve months and one senior GTM salary. A founder who reads the one-pager well and hires the first AE at the right moment turns a founder-led motion into a scalable one. **The one-pager is the trigger mechanism; this chapter is the sequence it triggers.**

Two things this chapter fixes. First, the **default staging sequence** — founder-led sales through PMF; then the first AE; then the first product-marketer or demand-gen lead; then the first sales manager only after ≥3 AEs. The sequence is not arbitrary — each hire depends on specific artifacts and specific GTM signals produced by the prior stage. Second, the **over-hire trap** — the specific pathology of hiring a VP Sales to invent a motion the founder never validated, or standing up an SDR team to feed an AE motion that has no repeatable AE. Chapter 7 will assemble both into the ship deliverable; this chapter fixes the logic.

The failure mode this chapter exists to catch: **the founder closes the Series-A, hires a VP Sales and two SDRs and three AEs in the first quarter post-raise, discovers eighteen months later that the VP Sales inherited a motion the founder had never made repeatable, the SDRs are feeding AEs who cannot close because the founder's script has not been documented and cannot be transferred, and $2.4M has been spent on GTM salaries producing $600k of net-new ARR — and the VP Sales is being fired for a problem that was structural, not personal.**

The remedy: a **staged first-hire plan** with specific GTM signal triggers per hire, an explicit "not yet" call on hires whose pre-conditions are not met, and an over-hire-anti-pattern check on every hire under consideration.

## Core concepts

### The default staging sequence — five stages, four hires

The default sequence for a mid-market B2B SaaS at SEED → Series-A. Consumer / PLG / enterprise-first motions have variants (noted at the end); the mid-market case is the canonical one.

- **Stage 0 — Founder-led sales through PMF.** The founder is the salesperson. No dedicated GTM hires yet. The trigger to *end* stage 0 is the [mod-102](../mod-102-pmf-signal-and-measurement/) PMF verdict landing green in a specific ICP segment *and* the [mod-105](../mod-105-founder-led-sales/) readiness signals landing — repeatable script, repeatable win-loss pattern, founder-becoming-the-bottleneck. This is Chapter 6 of mod-105.
- **Stage 1 — First AE.** The first Account Executive is hired to take over the sales motion the founder has proven repeatable. The trigger is stage 0 signals green. Hire criteria (below) prioritise founder-adjacent operators who can execute a known script over senior "hunters" who expect to invent a motion.
- **Stage 2 — First product-marketing or demand-generation lead.** The next hire is *not* another AE. It is a product marketer (if the constraint is positioning / messaging / demand quality) or a demand-gen lead (if the constraint is top-of-funnel volume). The trigger is the first AE closing at target *and* a specific one-pager signal that the constraint has shifted from "the AE motion works?" to "the top of the funnel is thin / mis-qualified."
- **Stage 3 — Second and third AEs.** Additional AEs are hired to scale the motion the first AE has now demonstrated *is transferable* to a non-founder-adjacent seller. The trigger is the first AE hitting quota for at least two consecutive quarters *and* PMM or DG demonstrably loading the top of funnel.
- **Stage 4 — First sales manager.** Only when there are ≥3 AEs (some conventions say ≥4) does a first sales manager get hired. The trigger is the AE team being big enough that managing them is a full-time job the founder cannot continue to hold.

**The order is not arbitrary.** Each stage produces the artifact the next stage needs. Skipping a stage or hiring out of order is the specific pathology this chapter catalogues.

References the sequence is grounded in: Pete Kazanjy's [*Founding Sales*](https://foundingsales.com/) (the definitive practitioner treatment of the founder-led → first-AE transition); Mark Roberge's [*The Sales Acceleration Formula*](https://www.markroberge.com/) (HubSpot's early sales hiring playbook, particularly on the founder-to-first-AE handoff and the science of scaling); Jason Lemkin's SaaStr writing on when to hire the first VP Sales ([SaaStr — When to hire your first VP Sales](https://www.saastr.com/)); Winning by Design's blueprints on GTM hire sequencing ([Winning by Design — Blueprints](https://winningbydesign.com/)).

### The trigger criteria per hire — the specific one-pager signals

Every hire has a **trigger criterion** — a specific, checkable pre-condition (usually a set of one-pager numbers plus an artifact from a prior module) that qualifies the hire. If the trigger is not met, the hire waits. The whole point of the operator one-pager (Chapter 5) is that these triggers are visible in the numbers monthly.

**First AE — trigger criteria (all must be met):**

- **mod-102 PMF scorecard is green** in at least one ICP segment. The Sean Ellis 40% or a comparable pull-signal in the specific segment.
- **mod-105 readiness signals** — the founder can produce a repeatable script (mod-105 Chapter 3–5 fixed the vocabulary); win-loss patterns are repeatable (the reasons the founder wins and loses are consistent across the last N deals, not one-offs); the founder is the bottleneck (specific deals are being lost because the founder cannot spend enough time on them).
- **Payback per channel** for the founder-outbound channel is at or below the mid-market working bar (≤12–18 months depending on ACV band).
- **mod-104 ICP scorecard is codified** — the AE needs a written ICP to disqualify against; the founder cannot rely on her intuitive read.
- **The mod-107 sales motion is designed** and documented at least to Chapter 2 of mod-107 (stages, exit criteria per stage, discovery-call script). The AE needs a motion to run, not one to invent.

**First AE — hire criteria (who to hire):**

- **Founder-adjacent operator, not a "hunter."** The first AE is someone who can run a documented script under founder mentorship, iterate the script with feedback, and produce data that improves the script. Not someone who needs to invent a motion or expects a fully-built machine to plug into.
- **2–5 years of relevant SaaS sales experience.** Enough to know the mechanics; not so senior that they expect infrastructure. Roberge's *Sales Acceleration Formula* argues for hiring against a specific competency profile (curiosity, coachability, work ethic, prior success, intelligence); the specific profile depends on the motion.
- **Compensation calibrated to founder-adjacent expectations.** Comp mechanics (base / variable / OTE / accelerators / ramp) is a deep topic that defers sideways to `startup-operations-governance-curriculum`. This module's boundary: **know the specific *number* — total OTE fully-loaded — that goes on the CAC line in Chapter 2** and know that the first AE typically ramps to full productivity in 3–6 months.

**First product-marketer or demand-gen lead — trigger criteria:**

- **First AE closing at target for ≥1 quarter.** Not two quarters yet (that triggers the *second AE*, below); just one quarter of hitting quota, which qualifies the motion as transferable.
- **The one-pager signal has shifted.** The bottleneck has moved from "the AE motion works?" (a mod-105 / mod-107 question) to "the top of funnel is thin or mis-qualified" (a mod-108 / mod-103 question). Specifically, one of the following is landing on the monthly one-pager:
  - **Pipeline coverage systematically below the required multiplier** even as the AE closes what she has → the constraint is *volume of qualified opportunities*, which is a demand-gen hire.
  - **Funnel Discovery → Demo dropping** on inbound-sourced opportunities → the constraint is *qualification of MQLs*, which is often a demand-gen + PMM hire (the inbound message is bringing in the wrong audience; positioning needs a fix).
  - **Funnel Demo → Proposal dropping** → the constraint is *value alignment at demo*, which is a product-marketing hire (positioning / demo narrative / competitive teardown are the fixes; mod-103 territory).
  - **Win-loss reasons showing "we didn't understand the differentiation"** in the exit surveys → PMM hire; the positioning has not landed.

**Which one — PMM or DG — depends on the specific signal.** A team with thin volume but healthy qualification hires DG first; a team with plenty of volume but poor conversion at Discovery or Demo hires PMM first. Both eventually get hired; the sequence depends on which the numbers say is the tighter constraint.

**Second and third AEs — trigger criteria:**

- **First AE hitting quota for ≥2 consecutive quarters.** This is the specific evidence that the motion is *transferable* to a non-founder-adjacent seller. A single quarter can be an outlier; two consecutive quarters is a pattern.
- **PMM or DG demonstrably loading the top of funnel** at a rate that supports 2–3 AE quotas' worth of pipeline coverage. The math: if each AE needs 5× coverage, three AEs need $15× the aggregate quota in pipeline; the DG or PMM has to be producing it.
- **Sales-motion documentation** at [mod-107](../mod-107-sales-motion-design/) depth — playbook, discovery script, demo checklist, proposal template, competitive teardown, objection handling. The second AE learns from documentation and coaching, not from watching the founder.
- **A functioning ramp process** — a written 60/90/120-day onboarding plan for a new AE, calibrated against the first AE's actual ramp. The first AE ramped in the founder's shadow; subsequent AEs ramp in an increasingly-structured process.

**First sales manager — trigger criteria:**

- **≥3 AEs** (some conventions say ≥4). Fewer than three does not justify a dedicated manager; the founder can 1:1 with two or three AEs herself.
- **The AE team is diverse enough** that a single generalist coach cannot serve them all — different segments, different geographies, different specialisations.
- **The founder's time is bottlenecked on management, not selling.** If the founder is spending >20 hours a week in AE 1:1s, coaching, deal review, pipeline reviews, and hiring, the founder is functionally the sales manager and the role has to be delegated.
- **Reliable enough month-over-month numbers** that the incoming manager can be held to a specific performance bar and can hold AEs to one.

The first sales manager hire is where the boundary with `startup-operations-governance-curriculum` lives — the *staging* of the hire (this module) vs. the *hiring / onboarding / management-system depth* of the hire (that curriculum).

### The over-hire trap — three specific failure patterns

Chapter 7 unpacks the wrong-first-hire diagnosis in depth. This section names the three specific patterns to anticipate.

**Pattern 1 — VP Sales before PMF.** The founder closes a seed round, decides to "hire a real sales leader to build the team," and recruits a VP Sales from a company one or two stages further along. The VP arrives with expectations of a working motion to scale, an SDR team to feed, a marketing engine to lean on, and a founder who will hand off the sales function. **None of that is present.** The founder is still selling; PMF is still being validated in one segment; the script is still in the founder's head; the CRM is a spreadsheet. The VP spends 6–12 months trying to invent the motion the founder never validated, burns their credibility on hires who cannot succeed because the underlying motion is unproven, and typically leaves (or is fired) within 12–18 months. **The team is worse off:** a senior GTM leader is now in the market with a "did not work out" line on their CV; the founder is out $250–350k in comp; the team is 12–18 months behind where it would have been had the founder run stage 0 to completion.

Lemkin's SaaStr writing is unambiguous on this: **do not hire a VP Sales before you have PMF and a repeatable motion.** The specific quote often paraphrased: *"if you're the CEO and you can't sell your own product, no VP Sales can save you."* The pattern is one of the most-catalogued in the practitioner canon; every generation of founders re-discovers it.

**Pattern 2 — SDR team before AE motion works.** The founder decides to "scale outbound" by hiring 2–4 SDRs before hiring an AE, on the reasoning that "SDRs are cheaper and let the founder focus on closing." The SDRs load the top of funnel — but the AE-to-close motion has not been built yet, so the founder is still the one closing every deal, and the SDRs' output overwhelms the founder's closing capacity. Alternatively, the founder hires an SDR to feed an AE motion that has *no repeatable AE* — the SDRs load the funnel, the AE cannot close the opportunities the SDRs generate (because the motion is not yet fit for a non-founder), and the pipeline conversion drops to a level where the SDR cost is not recoverable.

**The right sequence is AE first, then SDR.** The AE demonstrates the motion works with SDR-generated leads before the SDR headcount is scaled. Winning by Design's blueprints on GTM hire sequencing make this explicit; Kazanjy's *Founding Sales* Chapter on the first-AE-then-SDR sequence is another reference.

**Pattern 3 — First AE hired against a founder script that has not been documented.** The founder hires the first AE, but the sales script, discovery approach, demo, proposal, and objection-handling are all in the founder's head — never written down. The AE arrives, is expected to "shadow the founder" and pick it up; ramps for six months producing nothing; and either quits or is let go. **The founder concludes "the AE was the wrong hire" when in fact the founder-artifact hand-off never happened.** The specific mod-105 Chapter 6 deliverables — repeatable script, discovery template, demo checklist, proposal template, next-step email templates — are the artifacts the first AE needs to learn from. If they do not exist as written documents, the hire is set up to fail.

The remedy is not to hire slower; it is to complete the mod-105 documentation *before* hiring the first AE.

### Consumer / PLG / enterprise-first variants

The default sequence is calibrated to mid-market B2B SaaS with an AE-led sales motion. Adjacent motions have variants:

- **Consumer / prosumer / low-touch PLG.** The "first AE" hire often does not happen at all; the first GTM hire is often a growth marketer or a product-led-growth product manager. The trigger equivalent to "founder can produce a repeatable script" is "the self-serve funnel converts at a rate that is a defensible growth engine." The `[cpo-curriculum]` treats the PLG-first hire staging in depth.
- **Enterprise-first (very high ACV, multi-threaded).** The first hire may be a full sales-cycle AE with enterprise-selling experience *earlier* than the mid-market cadence would suggest, because the ACVs are high enough to justify a $300k+ OTE from earlier. But the same *trigger* still applies — the founder must have proven the motion is repeatable in at least one enterprise land before hiring an AE to run it. The mistake is common in enterprise motions where founders think "the deals are too big for a first-year AE" and hire a senior AE they cannot mentor because they themselves have not yet proven the motion.
- **Pure PLG with paid layer on top.** Often the first hire is a demand-gen lead responsible for the paid funnel *before* the first AE, because the leading indicator that matters is self-serve activation and paid CAC, not AE productivity. But the demand-gen hire still requires the mod-102 PMF scorecard to be green — otherwise the paid loop scales an un-durable product.

The **principle** — trigger criteria before hire — is invariant. The **sequence** varies with motion type.

### The "not yet" call — explicit deferral

The most operationally-important discipline in this chapter is the willingness to say **"not yet"** to a hire the numbers do not qualify. Founder-pressure is real — the board wants growth; the runway needs to compound; the founder is exhausted from selling — and the temptation to hire someone senior *now* to relieve the pressure is the specific pathology this chapter warns against.

The plan (Chapter 7 will make this explicit) should contain **as many "not yet" calls as it does affirmative hires.** For each hire under consideration:

- **What is the trigger criterion?** (Which one-pager numbers, which artifacts.)
- **What is the current state on each criterion?** (Met / not met / partially met.)
- **If not met, what has to change and by when?** (Which one-pager number needs to move; which artifact needs to be produced; which mod-102 / mod-105 / mod-107 / mod-108 upstream work is unfinished.)
- **What is the review cadence?** (Monthly? Quarterly? What triggers a re-read?)

The "not yet" is not a delay of the plan; it is *part* of the plan. A plan without "not yet" calls is a hire-everyone plan and is the specific artifact the over-hire trap produces.

### The boundary with `startup-operations-governance-curriculum`

Named explicitly to avoid confusion:

- **In scope (this module):** the *staging* — which hire when, based on which GTM signal from the one-pager, with which trigger criteria.
- **Out of scope (defers to `startup-operations-governance-curriculum`):** the *hire execution depth* — job description authoring, sourcing / interview loops, offer construction and negotiation, comp mechanics (base / variable / OTE / accelerators / clawbacks / equity), ramp-plan authoring, on-target-earnings design at company scale, sales-comp-plan mechanics, performance-management systems, quota-setting methodology, territory design, sales-ops function build-out, CS-ops function build-out, RevOps hiring.

Everything on the second list is a legitimate and important body of work. It lives in the operations / governance curriculum because it is a cross-role competency (the same offer-construction discipline applies to hiring an engineer or a designer), and because its depth would double this module's page count for a marginal gain in operating value.

The **staging logic** — the module's actual contribution — is what tells you *whether to hire now*. The **hire mechanics** — deferred — is what tells you *how to hire well when you do*.

## Concrete example — the code-review-tool 12-month first-hire staging plan

Continue the code-review tool from Chapters 2–5. As of 2026-08-21:

- Founder Alex Reyes is the only executive-level GTM person.
- First AE (Priya) hired 2026-Q1; ramped; ended Q2 at 82% of quota (below 100% but consistent with a ramping AE); Q3 forecast to hit 95–105% of quota.
- Head of CS (Jordan) hired 2026-Q1 to run the mod-109 retention motion.
- No dedicated PMM. No dedicated DG. Marketing Manager (Sam) handles both at a low bar.
- No SDRs, no second AE.
- Series-A closed for $6M in 2026-Q1; 18 months of runway remaining.

**Chapter 5 monthly one-pager (June 2026) key signals:**

- First AE (Priya) at 82% of Q2 quota; forecast 95–105% Q3.
- Funnel Demo → Proposal dropped 13pp in June (a specific stage failure isolated to paid-channel-sourced opportunities).
- Paid channel LTV/CAC = 0.78×; per-channel CAC drifting up; mod-108 channel-market-fit audit in flight.
- SEO / content channel showing modest but improving CAC efficiency (compounding channel candidate).
- Retention (from mod-109): outbound-cohort GRR healthy; paid-cohort GRR weak; NRR clears bar via expansion.
- Pipeline coverage 3.5× (short of the 6.4× required for historic conversion).

**12-month staging plan (2026-Q3 through 2027-Q2):**

**Hire #1 (candidate) — First DG (Demand Generation) or PMM hire.** Target date: 2026-Q4.
- **Trigger criteria:**
  - AE at 100% of quota for at least 1 quarter (Q3 forecast is 95–105%; needs to land at ≥100% before triggering the DG hire).
  - The one-pager signal that the constraint is top-of-funnel (currently: pipeline coverage 3.5× vs. 6.4× required → yes, volume constraint).
  - Paid channel decision made (defund vs. re-configure) so the DG hire is not walking into an unresolved channel problem.
- **Current state:** Q3 forecast met and AE at quota → Q4 hire greenlit. Otherwise, defer to 2027-Q1.
- **Which — DG or PMM?** The signal is volume constraint (pipeline coverage short), not conversion constraint (Discovery/Demo conversion is only modestly off baseline). **DG hire first;** PMM defers to 2027-Q1 or later.

**Hire #2 (candidate) — Second AE.** Target date: 2027-Q1.
- **Trigger criteria:**
  - First AE (Priya) at ≥100% quota for **2 consecutive quarters** (Q3 + Q4).
  - DG or PMM demonstrably loading the top of funnel — pipeline coverage rising toward 5–6× on the new hire's efforts.
  - Sales motion documentation complete at mod-107 depth — Priya has co-authored a playbook, discovery script, demo checklist, proposal template that a next AE can learn from.
  - Written 60/90/120-day ramp process for a new AE, calibrated against Priya's actual ramp.
- **Current state:** None of the four criteria met yet. **"Not yet."** Re-read after Q4 numbers land in January 2027.

**Hire #3 (candidate) — First PMM.** Target date: 2027-Q1 or Q2.
- **Trigger criteria:**
  - Volume constraint solved by the DG hire — pipeline coverage back to healthy level.
  - Conversion constraint emerging: Discovery/Demo/Proposal conversion below baseline systematically (not currently — the current gap is paid-channel-specific and will resolve with the paid decision).
  - Positioning gap surfacing in win-loss (mod-103 territory) — win-loss reasons showing "did not understand the differentiation" or competitive losses to a specific competitor at rate.
- **Current state:** No conversion constraint yet; no systematic positioning gap. **"Not yet."** Re-read after the DG hire's first quarter of impact.

**Hire #4 (candidate) — Third AE, First SDR.** Target date: 2027-Q2 or later.
- **Trigger criteria:**
  - Second AE ramped and at quota (would be Q2 2027 at earliest).
  - The founder still bottlenecked on close (implying the motion demands additional AE capacity, not additional demand).
  - SDR hire is coupled to the second AE succeeding: the SDR feeds the second AE, not the first (who has proven she can produce her own pipeline).
- **Current state:** Contingent on Hires #1 and #2 landing. **"Not yet."** Re-read after Second AE's first quarter.

**Explicit deferrals (things not on the plan):**

- **VP Sales.** Deferred indefinitely; no trigger criteria met (repeatable motion at ≥3 AEs is nowhere close). **"Not for at least 18 months, and only after a second and third AE both hit quota."**
- **RevOps hire.** Deferred until there is enough tooling and process complexity to justify — target 2027-Q2 or later.
- **Sales enablement hire.** Deferred until second AE onboarding has produced enough operational learning to codify — target 2027-Q3+ or later.

**Board narrative accompanying the plan:**

> The plan spends approximately $180k in fully-loaded GTM salary over the next 12 months (one DG hire in Q4 2026, contingent on AE Q3 numbers landing). The alternative — hiring a VP Sales and a second AE and two SDRs in Q4 as some board members have suggested — would spend approximately $850k in fully-loaded GTM salary against a motion that has not yet demonstrated it can support a second AE (per the one-pager). The recommended plan defers the additional spend until the trigger criteria are met, and reads them monthly from the operator one-pager.

This is the artifact the founder brings to the board. It is defensible against a "we should hire faster" pressure because every deferral is tied to a specific numerical trigger, and the trigger is on the one-pager the board is already looking at.

## Common failure patterns

- **VP Sales before PMF.** Pattern 1. The single most-catalogued over-hire failure in the SaaS canon.
- **SDR team before AE motion works.** Pattern 2. The "cheaper hires first" pathology.
- **First AE hired against an undocumented founder script.** Pattern 3. The AE is set up to fail because the artifact hand-off is impossible.
- **Second AE hired before the first has hit quota for two quarters.** One quarter of success can be an outlier; two consecutive quarters is a pattern. Scaling on one is a bet, not a plan.
- **PMM hired when the constraint is volume.** DG is the fix. Wrong hire; expensive delay.
- **DG hired when the constraint is qualification.** PMM is the fix (or upstream positioning work). Wrong hire; the volume that follows will convert poorly.
- **Sales manager hired at ≤2 AEs.** No management leverage; the manager becomes a senior IC with no team.
- **Skipping the "not yet" call.** A plan with only affirmative hires and no explicit deferrals is a hire-everyone plan; it produces the over-hire trap.
- **Trigger criteria without a review cadence.** "We'll hire when the AE hits quota" without specifying "monthly re-read" leaves the trigger buried in the founder's head; the one-pager review is what surfaces it.
- **Confusing staging with hire mechanics.** The staging (this module) says whether to hire now; the mechanics (`startup-operations-governance-curriculum`) says how to hire well. Neither substitutes for the other.

## Summary

- **Default staging sequence: founder-led → first AE → first PMM or DG → second and third AEs → first sales manager.** The order is not arbitrary; each hire's pre-conditions are produced by the prior stage.
- **First AE trigger:** mod-102 PMF green + mod-105 readiness signals + payback in-band + mod-104 ICP codified + mod-107 motion documented.
- **First PMM or DG trigger:** first AE at quota for ≥1 quarter *and* the one-pager signal has shifted to a top-of-funnel constraint. DG for volume; PMM for qualification.
- **Second and third AE trigger:** first AE at quota for ≥2 consecutive quarters + PMM/DG loading the top + motion documentation at mod-107 depth + written ramp process.
- **First sales manager trigger:** ≥3 AEs + team diverse enough that a single coach cannot serve all + founder time bottlenecked on management, not selling.
- **The over-hire trap has three patterns.** VP Sales before PMF (most catastrophic); SDR team before AE motion works; first AE hired against an undocumented founder script.
- **The "not yet" call is part of the plan.** A staging plan without explicit deferrals is a hire-everyone plan and produces the trap.
- **Consumer / PLG / enterprise-first motions vary the sequence.** The principle (trigger criteria first) is invariant; the specific hires and their order change with motion type.
- **The boundary with `startup-operations-governance-curriculum` is deliberate.** Staging logic lives here; hire mechanics lives there.
