# Designing an Enterprise Motion — MEDDIC and MEDDPICC

## Motivation

An enterprise deal is not a mid-market deal with more zeros. The pricing pack has more zeros, yes; the ACV band jumps from $10-100K to $100K-$1M+; the cycle stretches from 4-12 weeks to 6-18 months. But the *shape* of the motion changes at every level — the deal is bought by a **buying committee** (not a single VP) that includes an economic buyer, a technical evaluator, a user, a champion, procurement, legal, security, and sometimes finance; the deal moves through **stage gates** that require named artifacts (signed NDAs, security questionnaires, ROI documents, redlined MSAs); the deal is exposed to **competition** with a specific incumbent or specific alternative vendor at each stage; and the deal is at risk of dying at a **paper-process** step no one on the vendor side has visibility into. The mid-market motion's SPICED discipline (mod-105 Chapter 3) — Situation, Pain, Impact, Critical event, Decision — is not sufficient at this scale. The framework has to upgrade.

The upgrade is **MEDDIC** — Metrics, Economic buyer, Decision criteria, Decision process, Identify pain, Champion — with the two enterprise-specific additions of **MEDDPICC** — Paper process and Competition. The framework was developed at PTC in the 1990s by Jack Napoli and sales-leadership peers, adopted across enterprise software companies through the 2000s and 2010s (BladeLogic, BMC, Ariba, etc.), and popularised in the modern SaaS era via John McMahon's *The Qualified Sales Leader* (2020), Andy Whyte's *MEDDICC: The Ultimate Guide* (2020), and the MEDDIC / MEDDPICC Academy training organisation. The framework is the operating standard for enterprise SaaS sales; a functional enterprise motion runs MEDDIC or MEDDPICC discipline through every stage of the funnel.

The failure mode this chapter exists to catch: **the founder ports the mid-market SPICED motion to enterprise deals without upgrading it — no MEDDPICC Metrics document, no explicit Economic-buyer meeting, no Decision-criteria coverage against the actual RFP, no Decision-process mapping, no paper-process forecast, no competition-mapping — and the deal enters the pipeline as a $500K opportunity, forecasted at 60% probability, and closes-lost or slips a quarter every quarter for a year because critical qualification never happened.** Or the mirror failure — the founder tries to run full enterprise MEDDPICC ceremony on a $15K mid-market deal, over-invests, and the buyer disengages under the weight of the process. Fit-to-motion is what MEDDIC discipline is calibrated for; using MEDDPICC where SPICED belongs is the same mistake in the opposite direction.

This chapter builds the enterprise motion: the MEDDIC and MEDDPICC frameworks in detail, the buying committee and its roles, the stage-gate structure that threads MEDDPICC through the CRM (developed in more instrumentation depth in Chapter 5), the sales-team roles (AE, SE, CS, sometimes an executive sponsor) that support the motion, and the operating discipline of an enterprise pipeline review.

## Core concepts

### What "enterprise" means, in motion terms

The word "enterprise" is used loosely in practitioner writing. This module fixes a working definition drawn from Chapter 1's matrix:

- **ACV threshold** — $100K/year and up. Below $100K the SDR-AE motion is typically sufficient; above $100K the buying-committee complexity typically demands MEDDIC discipline.
- **Cycle length** — 6-18 months from first meeting to signed contract. Deals under 6 months are typically mid-market complexity even if the ACV crosses the threshold; deals above 18 months usually indicate a mismatch (either an under-qualified deal or one that should have been strategic-mega-deal treatment).
- **Buying committee** — 5-15 stakeholders across at least three roles (economic buyer, technical evaluator, user, procurement, security, legal — and sometimes finance, compliance, IT, or an executive sponsor). Deals with a single buyer are not enterprise regardless of ACV.
- **Formal process** — RFP or formal evaluation process, security questionnaire, redlined MSA, procurement engagement, sometimes an executive sponsor on the buyer side. Deals without any formal process step are mid-market with a large sticker price, not enterprise.

The four criteria compound. A $150K deal to a single VP at a mid-market company is a large mid-market deal; run it on SPICED with added Economic-buyer discipline from MEDDIC. A $300K deal to a Fortune 500 buying committee with an RFP and a 12-month cycle is an enterprise deal; run it on full MEDDPICC.

### MEDDIC — the six letters

MEDDIC's six letters, in the order the framework typically covers them:

- **M — Metrics.** The specific quantitative outcomes the buyer expects the product to deliver. Not "improve productivity" but "reduce mean-time-to-resolve incidents by 40%, saving 2,000 engineer-hours per year at a fully-loaded cost of $250/hour = $500K/year." Metrics are what the champion uses to sell the deal internally; they are what the economic buyer signs off on; they are the ROI story the finance team needs to approve. A deal without Metrics has no defensible business case at the point of the sign-off meeting.
- **E — Economic buyer.** The person with veto authority over the spend. Identified by name (not role), engaged directly (ideally, meeting them at least once during the sales cycle), understood in terms of *their* KPIs and *their* decision criteria (which are usually different from the champion's). Deals that never surface the economic buyer close-lose at the final stage on "our CFO said no" — the failure was not surfacing the CFO earlier, when the ROI story could have been calibrated to her language.
- **D — Decision criteria.** The stated criteria the buyer will use to compare vendors — technical requirements (specific integrations, specific performance thresholds), security posture (SOC2, ISO27001, penetration test), commercial criteria (price, contract term, payment terms), qualitative criteria (support responsiveness, roadmap alignment). Decision criteria have to be surfaced explicitly and either met, re-negotiated, or acknowledged as a fit gap. Un-surfaced decision criteria kill deals at the eleventh hour ("we needed HIPAA and you don't have it").
- **D — Decision process.** The specific sequence of steps from "we're interested" to "signed contract" — technical evaluation, security review, procurement, legal, executive sign-off, countersign. Every step has an owner and an approximate duration. Missing the Decision-process conversation is how enterprise deals slip a quarter without anyone predicting it — the deal was "at 90%" until procurement surprised everyone with a 6-week review.
- **I — Identify pain.** The pain-sizing conversation across *multiple* stakeholders. Enterprise deals almost always have several pain articulations across the buying committee — the champion's pain (career-adjacent), the user's pain (day-to-day workflow), the economic buyer's pain (KPI / P&L), the security team's pain (compliance risk). Each pain has to be characterised and each stakeholder's pain has to map to a component of the Metrics story.
- **C — Champion.** Identified by name, coached explicitly on how to sell the deal internally, given the materials she needs (the ROI document, the case studies, the internal talking points, the objection-handling one-pager). Enterprise champions are *trained assets*, not passive interested contacts. The single most reliable predictor of an enterprise deal closing is whether a real Champion exists and has been enabled — deals with a Champion close at 3-5× the rate of deals without one.

### MEDDPICC — the enterprise upgrade

**MEDDPICC** adds two letters that become load-bearing at $250K+ ACV and formal-procurement cycles:

- **P — Paper process.** The specific contract, redline, procurement, and legal process that closes the deal — MSA (Master Services Agreement) template selection, SOW (Statement of Work) drafting, redline cycles with the buyer's legal team, procurement's approval gates, e-signature routing, countersign. Paper process is often the single longest stage of a large deal — a 6-8 week enterprise legal review is standard; complex deals stretch to 12-16 weeks. Deals under-managed on Paper process slip a quarter every time the redline surfaces a term the vendor's legal team hasn't seen.
- **C — Competition.** The incumbent solution (whatever the buyer is using today — a competitor product, an in-house build, a spreadsheet-plus-headcount workflow), the alternative vendors under evaluation (the vendors on the RFP shortlist), and the "do nothing" option (which is usually the most-common actual loss). Competition has to be characterised specifically — not "we have some competitors" but "Datadog is the incumbent, they're mid-renewal, the champion prefers us on X but the security team prefers them on Y, the CFO is anchored to Datadog's price of $Z." Un-mapped competition is how deals get out-sold at the last moment by a vendor the AE didn't know was in the room.

### The buying committee — who's in the room

Enterprise deals are bought by committees. A working taxonomy of the roles (drawn from McMahon and Whyte, with the mod-104 buyer / user / champion split extended):

- **Economic buyer** — has veto authority over the spend; typically a VP, SVP, or C-level exec depending on the deal size and the org structure. Signs the contract or authorises the signer. The deal cannot close without her explicit approval.
- **Champion** — actively wants the deal to happen and will spend political capital to make it happen. Usually the person the vendor met first; usually a director, manager, or senior individual contributor with credibility in the buyer's org. Champions have to (a) genuinely want the outcome, (b) have credibility with the economic buyer, and (c) be willing to sell internally. Missing any of the three = "interested contact," not a champion.
- **Technical evaluator** — evaluates the product against the technical decision criteria. Often a senior engineer, an architect, a technical program manager, or a technical director. The technical evaluator's approval is a gate.
- **User** — the day-to-day operator of the product post-purchase. Users can veto through implementation ("we adopted it and the team hated the UX; we're switching"); their sign-off during evaluation is common at large ACV. Users are also the primary expansion vector (mod-109) — a strong user relationship at land makes expansion likely, a weak one makes expansion impossible.
- **Procurement** — owns the vendor selection process from a commercial and contract standpoint. In large enterprises, procurement has authority to reject a deal on commercial grounds even if all technical and user stakeholders approve. Procurement engagement typically enters the process late (proposal / negotiation) but should be surfaced early so the vendor knows the commercial gates.
- **Legal** — reviews the MSA, SOW, and any redlines. Owns the paper-process stage. Legal review can stretch a deal by 6-16 weeks depending on the enterprise's contract complexity.
- **Security / IT** — evaluates the product against the security decision criteria — SOC2, ISO27001, penetration test, security questionnaire (typically a 100-300-question document; sometimes SIG or SIG Lite). Security veto is common at Fortune 500 accounts; the vendor's security package (SOC2 report, pen-test summary, DPA template, data-flow diagram) has to be ready before this stage.
- **Finance** — evaluates the ROI and the commercial terms. Sometimes the same as the economic buyer; sometimes a separate reviewer. Finance sign-off usually requires the Metrics document from MEDDIC.
- **Executive sponsor (buyer side)** — a senior exec who blesses the deal from above. Not always present; when present, the deal is on the buyer's strategic priority list rather than a discretionary purchase.
- **Blockers** — the fifth-role hidden veto (mod-105 Chapter 3). Someone at the account has a reason to say no — a competing vendor's champion, an incumbent-solution owner, a security lead with a preferred vendor, a legal advisor with a preferred template. Blockers do not appear on org charts; discovery has to surface them by asking "who else needs to weigh in?" and "any concerns from security / IT / legal / procurement?"

The vendor-side team mirrors the buyer-side committee. At enterprise ACV, the deal is worked by:

- **Enterprise AE** — owns the account and the commercial relationship.
- **Sales engineer (SE) / solutions consultant (SC)** — technical counterpart to the AE; runs technical evaluations, POCs, security questionnaires, deep-dive demos.
- **Customer success (CS)** — enters at the close and owns implementation and renewal. In some orgs, CS is present through the sales cycle as a resource the AE can bring in.
- **Executive sponsor (vendor side)** — a founder, CRO, or executive who mirrors the buyer-side executive sponsor. Presence signals the deal's importance to the vendor.
- **Legal** — vendor's legal team, works the paper process.

### Threading MEDDPICC through the funnel

The mistake mid-market motions make when moving to enterprise is running MEDDPICC as a one-off qualification exercise ("we did MEDDIC on that deal in discovery") rather than as a discipline that runs *through every stage of the funnel*. Chapter 5 develops the CRM-stage-with-artifact structure; here is the enterprise-specific shape:

- **Prospect / research (pre-first-meeting).** Account-level research: identify the likely Economic buyer, likely Champion candidates, known Decision criteria from public information (job posts, tech blog, RFP-portal listings, LinkedIn), obvious Competition (existing tools in the stack). MEDDPICC hypothesis is written before the first outreach.
- **Discovery (first meeting through fit-confirmed).** Coverage on Identify-pain, Champion (first identification), Metrics (first sizing), Economic-buyer (name and role). Coverage document written after each discovery call and updated as more stakeholders are met.
- **Technical evaluation (POC / trial).** Coverage on Decision-criteria (against the actual RFP or eval scorecard), Competition (which other vendors are in the eval), Metrics (refined against POC outcomes). SE-led; produces a technical scorecard the champion carries.
- **Business case / ROI (pre-proposal).** Coverage on Metrics (final ROI document), Economic-buyer (direct meeting to align the ROI to her KPIs), Decision-process (mapped end-to-end from here to signature). Business case document is co-authored with the champion.
- **Proposal / negotiation.** Coverage on Paper-process (MSA sent, redline expectations set), Decision-process (final approval sequence), Competition (final positioning against last-standing alternatives).
- **Legal / procurement (paper process).** Coverage on Paper-process (redline cycles, executive escalation for stuck redlines), Decision-process (procurement's specific approval path), Economic-buyer (final sign-off).
- **Close (signature).** All eight letters green; deal closes on the forecasted date or is escalated 2 weeks before the forecasted date if any letter is red.
- **Land (post-signature, pre-first-renewal).** Deal moves to CS for implementation; expansion motion begins per mod-109.

At each stage transition the CRM opportunity has to have the MEDDPICC letters that stage requires marked green (or explicitly acknowledged as red with a mitigation plan). Chapter 5 develops the artifact-per-stage discipline; this chapter names the shape.

### The enterprise-specific rhythm

Enterprise motions run on different rhythms than mid-market motions. Practitioner defaults:

- **Deal review cadence.** Weekly one-on-one between AE and sales manager (or founder if pre-VP-Sales), 30-45 min, running each open enterprise opportunity through MEDDPICC coverage. Deals under $500K may get every-other-week reviews; deals above $1M get weekly.
- **Pipeline review.** Weekly team-wide pipeline review, 45-60 min, running the top 10-20 opportunities across all AEs. Forecast is committed on the call, not in a dashboard cell.
- **Executive review.** Monthly or quarterly executive review with the founder / CEO / CRO on the top strategic deals. Any deal above a threshold (e.g., $500K or 5% of quarterly forecast) gets executive time.
- **QBR (Quarterly Business Review).** Every account (open and closed-won) gets a quarterly review — pipeline health, expansion opportunity, CS status, competitive landscape. The QBR is where deals-at-risk get surfaced and where expansion deals get sourced.

The rhythm is a coordination cost. Mid-market motions don't need it (a 15-minute Monday standup covers pipeline); enterprise motions require it (a $500K deal that slips a quarter for un-diagnosed reasons is an unacceptable outcome, and the rhythm is what makes the diagnosis possible before the slip happens).

### The SE role — and when to hire the first one

The **sales engineer** (SE) — also called solutions engineer, solutions consultant, or solutions architect — is the technical counterpart to the AE. The SE's job:

- **Deep-dive demos** — custom demos against the buyer's specific tech stack and use case. Mid-market demos can be run by the AE; enterprise demos usually require an SE.
- **Technical discovery** — the technical half of MEDDIC's Identify-pain and Decision-criteria coverage. Requires an engineer's language.
- **POC / trial execution** — configuring and running a proof-of-concept against the buyer's environment. Sometimes requires access to the buyer's infrastructure.
- **Security questionnaire response** — the 100-300-question security document that enterprise deals require. SE typically owns response; may involve the security team and legal.
- **Objection handling on technical claims** — when the competitive Competition is technical (a competitor's architecture claim, a technical requirement the vendor doesn't meet), the SE is the person who responds credibly.

**When to hire the first SE.** Standard practitioner benchmarks (Roberge, Kellogg, Sales Assembly writing on SE ratios):

- **Ratio target**: 1 SE per 2-4 AEs at enterprise ACV; 1 SE per 4-6 AEs at mid-market.
- **Hire the first SE when**: the AE is spending > 40% of her time on technical questions she can't answer without engineering help; when a security questionnaire is blocking the second enterprise deal; when a POC configuration is stalling the first enterprise opportunity.
- **Do not hire the first SE before**: the first enterprise deal has closed. The SE role's playbook is derived from the first close — hiring earlier produces a role without a defined playbook.

At seed / early Series A, the founder or CTO often plays the SE role on the first 2-3 enterprise deals, then hires the first SE once the pattern is characterised.

### The pilot / POC decision

Enterprise deals sometimes involve a **pilot** or **POC** (Proof of Concept) — a paid or free time-boxed evaluation where the buyer runs the product against their real environment for 30-90 days. Pilots are load-bearing when the deal has technical decision-criteria that can only be evaluated against the buyer's own data; they are wasted effort when the buyer has already decided and is running the pilot as a rubber-stamp exercise.

Working discipline for pilots:

- **Pilots are paid** whenever possible, at a discounted rate against a defined success criteria list. Free pilots convert 2-3× worse than paid pilots (the buyer has no commercial commitment).
- **Success criteria are written before the pilot starts** and agreed by both sides. "The pilot is successful if we detect at least 3 blocking dependency issues on Acme's monorepo in the first 30 days" is a success criterion; "the team likes it" is not.
- **The pilot has a defined end date** with a decision meeting scheduled on that date. "We'll evaluate for 60 days and see" without a scheduled decision meeting is a pilot that becomes a permanent free trial.
- **The pilot's outcome is documented** — a joint document authored by the AE + SE and reviewed with the champion, translating the success criteria into observed outcomes and their business-case implications.

Pilots badly run are the number-one reason enterprise deals stall. Pilots well run are the number-one accelerator — a successful paid pilot with documented outcomes typically closes to a full deal in 4-8 weeks after pilot end.

### Compensation and forecast discipline

Enterprise AE comp structures typically:

- **Base : variable split** of 50/50 or 60/40 (base $150-200K, variable $150-200K, OTE $300-400K for a Series-A-through-B stage enterprise AE at US benchmarks; higher for later-stage or more senior). <!-- needs-research: pin enterprise AE comp benchmarks against current Bridge Group Inside Sales report or SaaStr Enterprise Comp study rather than range estimates -->
- **Quota : OTE ratio** of 5-7× — a $350K OTE AE typically carries a $1.75-2.5M annual quota.
- **Accelerators above quota** — commission rate steps up for revenue above 100% of quota, often to 1.5-2× the base commission rate.
- **Clawbacks** — some percent of commission is held for 6-12 months and forfeited if the customer churns before the first renewal.

Forecast discipline at enterprise scale:

- **Forecast categories** — Commit (highest confidence, will close this quarter), Best Case (will close this quarter with normal execution), Pipeline (open but not forecasted this quarter), Omit (not close-able this quarter regardless).
- **Weekly forecast update** — AE reviews each deal's stage, MEDDPICC coverage, and forecast category with the sales manager. Category changes require a specific reason (a stage advanced, a MEDDPICC letter turned green, or a specific event).
- **Slippage discipline** — a deal that slips a quarter is a diagnosis moment, not just a re-forecast. Which MEDDPICC letter was red? Was it un-surfaced or was it surfaced-but-under-managed? The answer feeds coaching and process changes.

## Concrete example — Loomly's first enterprise motion

Loomly's Chapter 1 motion decision was SDR-AE-primary for mid-market. Twelve months in, one of Loomly's larger mid-market customers has been acquired by a Fortune 500 conglomerate; the buyer at the parent company reaches out with interest in deploying Loomly across 2,000 engineers globally at ~$300K ACV. This is Loomly's first enterprise deal; the mid-market motion is not sufficient.

**Step 1 — Recognise the motion shift.** Founder Jane and the first AE (mid-market-experienced but not enterprise) agree that this deal cannot be run on SPICED-only. The deal shape checks all four enterprise criteria: ACV $300K (crosses the $100K threshold), likely 9-12 month cycle, buying committee of at least Champion (VP Platform Engineering) + Economic buyer (CTO) + Technical evaluator (Head of Infrastructure) + Security (CISO) + Procurement + Legal, formal RFP-style evaluation likely.

**Step 2 — Assemble the vendor-side team.** AE is the deal owner; Jane joins as executive sponsor (she is not the SE — the deal will need a technical resource the founder alone cannot cover). Loomly does not yet have an SE; Jane's cofounder (CTO) plays the SE role on this deal explicitly to characterise the SE playbook before hiring the first SE. CS lead joins the calls from Discovery forward, mirroring the buyer's eventual expected implementation team.

**Step 3 — MEDDPICC discovery.** First discovery call is a joint call with the VP Platform Engineering (probable Champion) and the Head of Infrastructure (probable Technical evaluator). AE runs SPICED-plus, extending to MEDDIC coverage:

- **Metrics**: VP Platform describes the pain (dependency-graph incidents across 2,000 engineers = 6-8 hours/incident lost * 20 incidents/quarter = 480-640 engineer-hours/quarter at $200/hr = $384-512K/quarter, so $1.5-2M/year of engineer-time cost that Loomly could halve). This is the ROI story; AE captures it in the MEDDPICC coverage doc.
- **Economic buyer**: Confirmed as the CTO. VP Platform commits to a joint meeting with the CTO in week 3.
- **Decision criteria**: Emerging list — GitHub Enterprise Cloud + on-prem GitHub Enterprise Server support, SSO via Okta, SOC2 Type II, GDPR + FedRAMP-adjacent posture (not required but preferred), 99.9% SLA, priority support with 4-hour response, custom dependency-graph rules API.
- **Decision process**: 90-day evaluation + 60-day paper process, targeting a January close for Q1 fiscal-year budget deployment. AE maps the specific sequence: 30-day technical evaluation → 30-day POC → business case → procurement → legal → executive sign-off → countersign.
- **Identify pain**: Documented at three levels — VP Platform's pain (career-adjacent: cycle time is a scored KPI), user pain (individual engineers: Slack-chasing incidents wastes their time), CTO's pain (infrastructure reliability and cost). Three separate framings feed the Metrics story from three angles.
- **Champion**: VP Platform Engineering identified. Not yet trained; AE plans a champion-enablement meeting in week 4 with a coaching document ("here's how to sell this internally, here's the ROI one-pager, here's the objection-handling notes for the CFO and the CISO").
- **Paper process**: MSA template selection open — buyer's legal will send their preferred MSA; Loomly's legal (external counsel at this stage) reviews. Redline cycles expected to take 3-4 rounds over 6-8 weeks. AE flags the paper-process risk to Jane; Jane briefs external counsel.
- **Competition**: Buyer is currently using a custom in-house tool + a legacy vendor (Sonar Dependencies, hypothetically) that is mid-renewal. Competition Sonar is entrenched with the security team; buyer's champion prefers Loomly on UX and integration; CTO is undecided. AE builds a Competition-mapping doc: Sonar's strengths and weaknesses, Loomly's counter-positioning, expected areas of security-team resistance.

**Step 4 — Technical evaluation and POC.** Weeks 4-8: joint sessions between CTO of Loomly (playing SE), Head of Infrastructure, and 3 senior engineers at the buyer. Loomly-side documents the buyer's environment; buyer-side documents the technical decision criteria against Loomly, in-house tool, and Sonar. Week 8: paid POC begins at 200-engineer subset for 45 days at $30K flat fee, with 5 written success criteria co-authored by AE, SE, and Champion.

**Step 5 — Business case and executive alignment.** Week 12: Champion has enough POC data to build the internal business case. AE + Champion co-author the ROI document. Week 13: joint meeting with CTO (Economic buyer) — AE and Jane present the ROI, competitive positioning, and proposed terms; CTO asks about SLA, security posture, and reference customers of similar size. AE addresses each; CTO commits to Q1 close pending security and procurement.

**Step 6 — Paper process.** Weeks 14-22: buyer's legal sends MSA template; Loomly's legal redlines; 4 redline cycles over 6 weeks. Two terms escalate to Jane and buyer's CTO for executive resolution (a data-processing-addendum term and a limitation-of-liability cap). Buyer's procurement engages in week 18; commercial terms negotiated (final ACV: $280K/year, 3-year term with year-2 and year-3 uplifts, one-time onboarding fee of $20K). Security review completes week 20 (SOC2 report + pen-test summary + DPA + data-flow diagram sufficient; no additional certifications required).

**Step 7 — Close.** Week 24 (6 months from first meeting; ahead of the forecasted 9-month cycle). Contract countersigned on the forecasted date. Deal moves to CS for onboarding; expansion opportunity flagged (the parent company has 3 more subsidiaries that could adopt Loomly on the same MSA if the first deployment succeeds — mod-109 territory).

**Step 8 — Post-close diagnosis.** Jane and the AE run a retro:

- MEDDPICC coverage held all the way through — every letter was green at the stage the letter needed to be green by.
- The one stumble: Competition mapping surfaced Sonar's security-team allegiance late (week 5), which could have surfaced during Prospect research; had it surfaced in week 1, the AE could have engaged Loomly's security team with the buyer's CISO earlier.
- The SE role was played by the CTO; the pattern is now characterised enough that Loomly's first SE hire (Chapter 4 topic; likely happens in month 15-18) can inherit a playbook.
- Paper process took the longest — 8 weeks from MSA sent to signed. This matches the 6-16 week enterprise legal benchmark. Two lessons: (a) engage external counsel earlier next time; (b) prepare a Loomly-preferred MSA template that can be offered before the buyer sends their template.

The retro turns into the enterprise motion's operating playbook v1. Every subsequent enterprise deal is run on the same MEDDPICC discipline, with the retro-informed improvements. By deal #4, Loomly has hired the first SE, retained an external counsel with SaaS-contract specialisation, and shipped a Loomly-preferred MSA template that closes 60% of deals without going to the buyer's template.

## Common failure patterns

- **SPICED-on-enterprise trap.** Founder or AE runs enterprise deals on the SPICED framework alone — no explicit Metrics document, no Economic-buyer meeting, no Decision-process mapping, no Paper-process forecast, no Competition mapping. Deal enters pipeline at 60% forecast confidence and either close-losts on "our CFO said no" or slips a quarter every quarter for a year. Fix: MEDDPICC discipline threads through every stage; each letter has a stage-exit criterion.
- **Champion-without-training trap.** Champion is identified but never enabled. AE never gives the champion the ROI document, the objection-handling notes, the internal talking points, or the case-study one-pager. Champion tries to sell internally with what she remembers from the demo; deal loses when the CFO asks a question she can't answer. Fix: champion enablement is a discrete step with defined artifacts and a coaching conversation.
- **Economic-buyer-never-met trap.** Deal moves through the funnel without the AE ever meeting the Economic buyer. Champion assures the AE that the CFO will approve; the CFO turns out to have KPIs the ROI story does not address; deal close-losts. Fix: explicit Economic-buyer meeting is a stage gate; deal cannot move past a certain stage until the meeting has happened.
- **Un-mapped-competition trap.** Deal is worked as if Loomly is the only vendor in the room; competitor's presence is not characterised. At the eleventh hour the competitor's champion (in a different part of the buyer's org) blocks the deal on a term Loomly could have negotiated if surfaced earlier. Fix: Competition mapping is written at Prospect stage and updated at every stage; "who else is being evaluated?" is a required discovery question.
- **Paper-process-under-forecast trap.** AE forecasts a 6-week close time from proposal to signature; buyer's legal review takes 12 weeks; deal slips a quarter. AE has no visibility into the buyer's paper process because it was never mapped. Fix: Paper process is mapped explicitly at proposal stage — MSA template selection, expected number of redline cycles, buyer's legal-review-throughput, procurement's approval path, executive sign-off requirement, e-signature routing.
- **POC-as-permanent-free-trial trap.** POC starts without success criteria and without an end date; extends indefinitely; buyer uses the tool without paying and never commits to a full deal. Fix: paid pilots with written success criteria and a scheduled decision meeting.
- **Full-MEDDPICC-on-a-mid-market-deal trap.** AE inherits the enterprise discipline and applies it to $30K mid-market deals; buyer feels over-managed, cycle stretches to 8 months for a deal that would have closed in 6 weeks on SPICED. Fix: match framework to ACV; MEDDPICC is a Chapter 4 topic, not a universal template.
- **No-SE-when-needed trap.** Enterprise deal runs without SE support; AE tries to answer deep-technical questions she can't answer credibly; buyer's technical evaluator loses confidence; deal close-losts on "technical fit unclear." Fix: SE role covered — either by an actual SE hire, the founder / CTO on the first deals, or explicit deferral of the enterprise deal until SE resource is available.
- **Rush-the-close trap.** Deal at 90% forecast confidence; AE pushes hard on the champion to close by end of quarter; procurement and security are not yet complete; buyer's team feels pressured and slows down; deal slips two quarters. Fix: Decision-process mapping produces a defensible close date; the forecast is against that date, not against the sales team's quarterly quota pressure.
- **Solo-founder-on-a-9-month-enterprise-cycle trap.** Founder tries to run enterprise deals alone at the same time as running the mid-market motion, product development, and fundraising; enterprise deal receives 5 hours/week of attention when it needs 15-20; deal drifts. Fix: enterprise deals require dedicated capacity; either hire the enterprise AE (and support with SE and CS) or explicitly defer the enterprise motion until capacity exists.
- **Under-forecasted-paper-process-cost trap.** Founder does not budget for external legal counsel, DPA drafting, security-questionnaire response time, or MSA negotiation. Deal closes but at a lower net revenue than modelled because the paper process cost $50K in legal time. Fix: enterprise deals model in a 2-5% overhead for legal, security, and procurement — over-forecast rather than under-forecast.
- **Assuming-executive-sponsorship trap.** Champion says the deal is a "strategic priority" for the CTO; AE assumes executive-level support; CTO turns out to have never heard of Loomly. Fix: executive support is verified by direct meeting or direct communication, not by champion assertion.

## Summary

- Enterprise motion is qualitatively different from mid-market. **ACV $100K+**, **cycle 6-18 months**, **buying committee 5-15 stakeholders**, **formal process** (RFP, security questionnaire, redlined MSA, procurement, legal). SPICED alone is insufficient at this scale.
- **MEDDIC** — Metrics, Economic buyer, Decision criteria, Decision process, Identify pain, Champion — is the six-letter enterprise upgrade to SPICED. **MEDDPICC** adds **Paper process** and **Competition** for enterprise-scale (typically $250K+ and formal-procurement).
- Each letter is a **stage-exit criterion** — the deal cannot move past a certain stage until that letter is green (or explicitly acknowledged as red with a mitigation plan). Chapter 5 develops the stage-artifact structure in depth.
- The **buying committee** — Economic buyer, Champion, Technical evaluator, User, Procurement, Legal, Security, Finance, Executive sponsor, Blockers — is mirrored by the **vendor-side team** — Enterprise AE, SE, CS, Executive sponsor, Legal.
- The **enterprise-specific rhythm** — weekly one-on-one deal reviews, weekly pipeline reviews, monthly / quarterly executive reviews, QBRs — is a coordination cost mid-market motions don't need but enterprise motions require to avoid un-diagnosed slippage.
- The **SE role** enters at enterprise ACV to run technical discovery, POCs, security questionnaires, and deep-dive demos. First SE hire follows the first enterprise close; founder / CTO plays the SE role on the first 2-3 enterprise deals to characterise the playbook.
- **Pilots / POCs** are paid whenever possible, with written success criteria and a defined end date + decision meeting. Free open-ended pilots become permanent free trials.
- The **canon**: John McMahon *The Qualified Sales Leader* (2020), Andy Whyte *MEDDICC: The Ultimate Guide* (2020), MEDDIC Academy / MEDDPICC.com training organisation. All three are cited in `resources.md`.
- **Failure modes** — SPICED-on-enterprise, champion-without-training, economic-buyer-never-met, un-mapped-competition, paper-process-under-forecast, POC-as-permanent-free-trial, full-MEDDPICC-on-a-mid-market-deal, no-SE-when-needed, rush-the-close, solo-founder-on-a-9-month-cycle — are all diagnosable at the stage-gate level. If the MEDDPICC letters are honestly graded per stage, the failure has a defined letter it happened at.
- Enterprise motion is often the **top layer** in a stacked motion — PLG feeds the SDR-AE motion, SDR-AE hands off enterprise-scale deals to the enterprise motion. The layering is intentional; each layer has defined entry criteria and defined hand-off ownership.
- Chapter 5 threads MEDDIC / SPICED / MEDDPICC discipline through **every CRM stage** — no gut-feel pipeline advancement, every stage transition requires a named artifact. Chapter 6 diagnoses **motion mismatches** — what happens when the enterprise motion is applied to a mid-market deal or vice versa.
