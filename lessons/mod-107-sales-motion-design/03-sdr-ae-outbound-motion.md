# SDR-AE Outbound Inside Sales — the Predictable Revenue Motion

## Motivation

The SDR-AE inside-sales motion is the workhorse of mid-market B2B software sales. It is what a Salesforce, a HubSpot, an Okta, a Segment, a Snowflake, or a Datadog looks like from the outside — a specialised **SDR** (sales development rep) generates opportunities from a target-account list, an **AE** (account executive) runs discovery / demo / proposal / close, and the pipeline moves through defined stages against a defined qualification framework. The motion is the operating structure Aaron Ross and Marylou Tyler codified in *Predictable Revenue* (2011), refined by Mark Roberge in *The Sales Acceleration Formula* (2015), and further sharpened by John McMahon in *The Qualified Sales Leader* (2020). It is the most-taught, most-templated sales motion in modern SaaS.

That maturity is a double-edged sword. Because the SDR-AE motion has a well-known playbook, founders tend to install it on autopilot — hire an SDR, hire an AE, buy Salesforce, buy a cadence tool, follow the templates — regardless of whether the ICP + ACV combination supports it. When the motion is mismatched to the market (mod-107 Chapter 1's mismatch zones), the templates run but the pipeline does not; six months later there is no revenue and no diagnosis for why. When the motion *is* matched to the market but the founder installs the machinery too early — before the founder has personally closed the first 20-30 deals per mod-105 — the SDR and AE inherit a playbook that has not been battle-tested against real buyers, cannot answer buyer objections the founder has never heard, and grind on a target-account list nobody has yet proven will convert.

The failure mode this chapter exists to catch: **the founder installs the SDR-AE machinery (roles, tools, comp plans, cadences) before running the motion herself long enough to know what actually works — and either (a) the machinery grinds forward with false-positive pipeline that never closes, wasting a year of runway, or (b) the founder hires the SDR-AE split too late, remaining the sole seller into Series A when a repeatable motion existed 12 months earlier and revenue could have compounded on top of it.**

This chapter builds the SDR-AE motion in the shape it actually works: the SDR-AE split and what each role owns, the cadence design (channels, sequence structure, touch counts, timing), the response-rate and conversion benchmarks against which the motion is measured, the hand-off criteria between SDR and AE, and — critically — the *timing question* of when the founder is the SDR-AE-hybrid and when to hire the split. The founder-led half is developed in mod-105; this chapter picks up at the point of transition and forward.

## Core concepts

### The Predictable Revenue tradition

The operating tradition of the modern SDR-AE motion is Aaron Ross's *Predictable Revenue* (2011). Ross's insight, drawn from his time running the Salesforce outbound-sales machine in the mid-2000s, was that **the traditional AE-does-everything model breaks at scale** — the same rep who prospects the cold list, qualifies the opportunity, runs the demo, negotiates the deal, and closes the contract is doing four different jobs badly. Ross's remedy was **role specialisation** — split the prospecting job (SDR / "Cold Calling 2.0" in Ross's earlier writing) from the closing job (AE) — and instrument each side with its own quota, its own metrics, and its own tooling. The book codified the split as the *Predictable Revenue* pattern; two decades of practice have refined the specifics but not overturned the core structure.

Mark Roberge's *The Sales Acceleration Formula* (2015) — written from his time as SVP of Sales at HubSpot — adds the *how-to-hire-and-scale* discipline on top of Ross's role split. Roberge's framework: **hire the right salesperson formula, train the right sales process, generate the right demand, use the right technology.** The book's numeric rigour — target 5-6 SDRs per AE at some ratios, target-account list of ~200 accounts per AE, quota-to-OTE at 5× — is the operating benchmark set that most modern sales orgs still tune against. <!-- needs-research: pin the specific ratios and benchmarks against Roberge's book chapters or public interviews rather than the paraphrased summary version -->

John McMahon's *The Qualified Sales Leader* (2020) — written from a career running enterprise sales at PTC, Ariba, BladeLogic, and BMC — extends the discipline to the qualification framework (MEDDIC / MEDDPICC) and the sales-management practice (pipeline reviews, forecast discipline, hiring). McMahon's book is the natural upgrade path when the SDR-AE motion moves up-market from mid-market ($10-100K ACV) into enterprise ($100K+ ACV, Chapter 4).

Three books are the working canon. Every SDR-AE motion in the modern practitioner literature draws on some subset of the three. Later refinements — Winning by Design's Bowtie / SPICED framework, Trish Bertuzzi's *The Sales Development Playbook*, Josh Braun's outbound writing, LinkedIn's *State of Sales* benchmark data — build on rather than replace the tradition.

### The SDR-AE split — what each role owns

The role split is the operating heart of the motion. Each role has a defined set of activities, a defined metric it is compensated against, and a defined hand-off point to the next role.

**SDR (Sales Development Representative).** Sometimes called BDR (Business Development Representative) — same role, different name convention. The SDR owns *top-of-funnel*:

- **Prospecting** — building and maintaining the target-account list; enriching accounts with contact information (usually via Apollo, ZoomInfo, Clay, or LinkedIn Sales Navigator).
- **Outbound sequences** — running the multi-touch cadence (email + LinkedIn + phone + video) against the target-account list.
- **Response handling** — replying to positive responses, qualifying the fit, booking the discovery call.
- **Inbound lead qualification** — handling replies from marketing content (webinars, gated ebooks), qualifying whether the lead is ICP-fit and buyer-role-fit before booking the AE.
- **Hand-off** — writing up the qualification notes and handing the account to the AE at the defined hand-off bar.

Standard SDR metrics: **booked meetings per month** (30-50 booked meetings is a common mid-market target); **held meetings per month** (booked-but-showed-up meetings, which run 60-80% of booked); **meetings-that-become-opportunities** (typically 40-60% of held meetings pass the AE's qualification bar). SDR OTE is typically $60-90K (US mid-market benchmarks; varies by region and company stage). <!-- needs-research: pin SDR OTE benchmarks against current Bridge Group Inside Sales report or LinkedIn State of Sales rather than range estimates -->

**AE (Account Executive).** The AE owns *middle-and-bottom-of-funnel*:

- **Discovery calls** — SPICED (or MEDDIC / MEDDPICC for enterprise, Chapter 4) discipline against the handed-off opportunity.
- **Demos** — customised demonstrations run against the pain surfaced in discovery (mod-105 Chapter 4).
- **Proposal and negotiation** — pricing conversations, redlining, procurement navigation.
- **Close** — signature, hand-off to customer success.
- **Expansion** — some AE structures include expansion revenue in the AE's quota (a "farmer-hunter hybrid"); others split expansion to a customer-success or account-management role. mod-109 develops the expansion side.

Standard AE metrics: **annual quota** (usually 4-6× OTE for mid-market; a $150K OTE AE typically carries a $600-900K annual quota); **quota attainment** (60% is the working practitioner benchmark for a healthy mid-market team — 60% of AEs at or above 100% quota; teams below 40% attainment usually have a pipeline problem or a hiring problem or both); **win rate on qualified opportunities** (25-40% for mid-market SaaS); **average sales cycle** (4-12 weeks for mid-market; longer for enterprise). <!-- needs-research: pin AE quota attainment and cycle-time benchmarks against current SaaStr / OpenView / Bridge Group data rather than range estimates -->

The **hand-off** between SDR and AE is the single most-consequential process boundary in the motion. It is developed as its own section below.

**Optional adjacent roles** that appear in a mature SDR-AE motion:

- **Sales engineer / solutions engineer (SE / SC).** Technical support to the AE on demos and evaluations. Common at ACV > $30K or in products that require significant configuration to demo well.
- **Sales operations.** Owns CRM hygiene, dashboarding, forecast discipline, comp-plan administration. Common once a team has 5+ AEs.
- **Customer success (CS).** Owns onboarding and renewal; sometimes owns expansion. Present from day one in most SaaS orgs regardless of size.
- **Sales manager.** Manages 5-8 AEs. Appears once the AE count crosses the manageable-by-founder threshold. The wrong-first-hire pattern (mod-110 develops this) is hiring a VP Sales before the motion is repeatable.

### The ratio question — how many SDRs per AE

Standard practitioner ratios (Roberge, Trish Bertuzzi, Bridge Group):

- **Mid-market** (ACV $10-100K, 4-8 week cycles) — 1-3 SDRs per AE. An AE closing 15-25 deals a year needs enough pipeline to support the demo cadence; 2 SDRs booking 30-50 meetings each per month is typical.
- **Enterprise** (ACV $100K+, 6-18 month cycles) — 0.5-1 SDR per AE, or a named-account model where the AE also prospects a smaller list herself. Enterprise AEs need fewer meetings per year but each meeting must be higher-fit.
- **Low-mid-market** (ACV $10-25K, 2-4 week cycles) — 3-5 SDRs per AE. High volume, short cycles, higher SDR-to-AE ratio.

The ratios are working starting points, not laws. The correct ratio is the one that keeps the AE's calendar full without stuffing it — an AE with too much pipeline develops attention debt and closes at a lower rate; an AE with too little pipeline prospects herself and defeats the specialisation. Ratio-tuning is a Chapter 5 topic (the CRM funnel makes the imbalance visible).

### Cadence design — the outbound sequence

The **cadence** (also called **sequence**, **cadence**, or **rhythm** depending on the tooling) is the multi-channel, multi-touch, time-boxed script the SDR runs against each target account. Modern cadence design has converged on a few operating principles:

**Multi-channel.** No single channel wins on its own. The working default is **email + LinkedIn + phone**, with **video message** (Loom / Vidyard) as a fourth channel for higher-touch accounts. Email-only cadences see response rates 30-50% below multi-channel cadences (per Outreach.io / SalesLoft published benchmark reports). <!-- needs-research: pin response-rate uplift for multi-channel vs. single-channel against current Outreach, SalesLoft, or Gong benchmark reports -->

**Multi-touch.** A functioning outbound cadence has **8-14 touches** over 3-6 weeks. Fewer than 8 touches under-invests (buyer misses the outreach in a busy inbox); more than 14 touches over-invests (fatigue; risk of being blocked). The distribution of touches across channels typically:

- ~5-7 emails, one per week or slightly more frequent, with variance in subject line, opening, and CTA.
- ~2-3 LinkedIn touches — connection request, direct message, InMail, engagement on posts.
- ~1-3 phone calls — targeted at the buyer's role, with voicemail scripts.
- ~1 video or personalised asset — high-effort, low-frequency, high-conversion.

**Personalisation gradient.** Modern practice differentiates three levels:

- **Level 1 — segment-personalised.** Same email template with the account name inserted. Response rate 1-2% (LinkedIn Sales Solutions benchmark). Appropriate for the top-of-list prospecting layer.
- **Level 2 — trigger-personalised.** Template plus a one-sentence reference to a recent event (funding round, executive hire, product launch, LinkedIn post). Response rate 3-5%. Appropriate for the middle of the target-account list.
- **Level 3 — deeply-personalised.** Custom email referencing specific product usage, specific job posts, specific technical content the buyer wrote. Response rate 8-15%. Appropriate only for the top-of-list ICP-fit tier.

An efficient cadence tiers accounts by fit and applies the personalisation level accordingly — Level 3 to the top 50 accounts, Level 2 to the next 200, Level 1 to the long tail. Level-3-everywhere is unaffordable at scale; Level-1-everywhere caps response rate at the segment-personalised floor.

**Timing discipline.** Cadence tools (Outreach.io, SalesLoft, Apollo, Woodpecker, Instantly) schedule touches at configurable intervals. Working practice:

- Space touches **2-4 days apart** at the front of the cadence, tightening slightly near the end.
- Send at times consistent with the buyer's timezone — mid-morning weekdays for most B2B buyers; avoid Friday afternoons and Monday mornings.
- Skip touches on holidays and known-dead weeks (Thanksgiving week in the US; the week between Christmas and New Year; local equivalents).

**The break clause.** A cadence has to have an explicit end — the "breakup email" or "final touch" that closes the loop. Cadences that never end fatigue the account and burn the domain reputation. The final touch is typically a short, professional close: "If this isn't a priority now, no worries — I'll follow up in a quarter."

**Cadence example (mid-market SaaS, Level 2 personalisation, 12-touch, 4-week):**

```
Day 1  — Email #1  (introduction + trigger-personalised opener + soft CTA)
Day 3  — LinkedIn connection request (no message)
Day 5  — Email #2  (angle #2 — different pain framing)
Day 8  — Phone call #1 + voicemail if no answer
Day 10 — LinkedIn direct message (referencing the email thread)
Day 12 — Email #3  (case study + social-proof angle)
Day 15 — Phone call #2 + voicemail
Day 17 — Email #4  (short — "am I reaching the right person?")
Day 20 — Video message (60-90 sec Loom, personalised)
Day 22 — Email #5  (angle #3 — economic-buyer-framing)
Day 25 — Phone call #3
Day 28 — Email #6  (breakup — "closing the loop")
```

Every touch is logged in the cadence tool; response at any touch pauses the cadence and routes the reply to the SDR to handle live. If the cadence completes without response, the account moves to a nurture list (light re-engagement quarterly) rather than being immediately re-prospected.

### Response-rate benchmarks

Standard benchmarks from the outbound-cadence tooling vendors (Outreach.io State of Sales, SalesLoft benchmark reports, Apollo benchmark data, HubSpot Sales Benchmark Report):

- **Open rate (email)** — 30-50% for well-written subject lines against warm-ish lists; below 20% often signals deliverability problems (spam filtering) rather than copy problems. <!-- needs-research: pin open-rate benchmarks against current Outreach / SalesLoft State of Sales reports -->
- **Reply rate (email)** — 3-8% for Level-2 personalised outbound at mid-market; 8-15% for Level-3 deeply-personalised outbound.
- **Positive-reply rate** — 20-40% of replies are positive (interested in a meeting or in more information); 30-50% are polite declines; 20-30% are unsubscribes or aggressive declines.
- **Meeting-booked rate** — 1-3% of touches lead to a booked meeting for well-run cadences at mid-market ICP; 3-6% for high-fit Level-3 tier.
- **Meeting-held rate** — 60-80% of booked meetings actually happen (the balance are cancellations, reschedules that never re-book, and no-shows).
- **Meeting-to-opportunity rate** — 40-60% of held meetings pass the AE's qualification bar and become opportunities.
- **Opportunity-to-close rate** — 20-40% for mid-market SaaS; higher for warm inbound, lower for cold outbound.

Compound these end-to-end: a mid-market cadence at 1000 touches / month produces roughly 10-30 booked meetings / month → 6-24 held meetings → 3-14 opportunities → 0.6-6 closed deals. The compounding tells the founder how many touches the pipeline math requires — it is often 3-5× more than intuition suggests.

**Benchmarks are working ranges, not laws.** A specific product's numbers may sit at the top of the range (strong PMF, obvious ICP, urgent pain) or at the bottom (early-stage, unclear positioning, weak pain). The benchmarks are a diagnostic — if the numbers sit below the low end of the range on multiple stages, the motion has a problem to diagnose. Chapter 5 develops the pipeline-hygiene discipline that makes the diagnosis possible.

### Hand-off criteria — the SDR → AE gate

The hand-off between SDR and AE is where most SDR-AE motions leak. If the hand-off bar is too loose, the AE inherits unqualified opportunities and closes at a low rate — which the AE blames on the SDR and the SDR blames on the AE's demo. If the hand-off bar is too tight, the SDR under-books, the AE has a light calendar, and pipeline coverage collapses. The bar has to be calibrated deliberately.

**The BANT alternative and its replacements.** The classic hand-off framework was **BANT** (Budget, Authority, Need, Timeline) — IBM-vintage, still used, and structurally outdated for modern SaaS motions where budget is often not yet allocated and timeline is often not yet defined. Modern replacements:

- **CHAMP** (Challenges, Authority, Money, Prioritisation) — lightweight, opens with pain rather than budget.
- **FAINT** (Funds, Authority, Interest, Need, Timing) — a slightly enterprise-flavoured update to BANT.
- **SPICED-lite for hand-off** — Situation, Pain, Champion, Interest confirmed — a lighter version of the SPICED framework developed in mod-105 Chapter 3.

Working hand-off criteria for a mid-market SDR-AE motion (a defensible starting point; every team tunes to its own data):

1. **ICP-fit confirmed** — the account matches Layer 1 (firmographic) and Layer 2 (behavioural) criteria from mod-104. If the SDR cannot answer "why is this account ICP-fit?" in one sentence, the hand-off is premature.
2. **Buyer role identified** — the meeting is with a buyer, champion, or user-with-influence, not a generic contact. "Interested in learning more" is not a buyer role.
3. **Pain articulated** — the SDR has a one-line description of the pain in the buyer's own words, not paraphrased into vendor language.
4. **Meeting scheduled and confirmed** — an actual calendar invite exists, accepted by the buyer.
5. **Timeline signal** — the buyer has some notion of when a decision might happen (this quarter, next quarter, actively evaluating). "Just curious" is not a timeline signal.

The SDR writes these five as a **hand-off note** in the CRM against the opportunity. The AE reviews the note before the discovery call and either accepts the hand-off (opportunity moves to Discovery stage) or rejects it back to the SDR with a specific reason (opportunity moves back to Prospect stage; SDR requeues or nurtures).

**Hand-off metric.** The most useful SDR-AE-motion metric is *SDR-booked meeting → AE-accepted opportunity conversion*. If the ratio is 90%+ the hand-off bar is too loose (SDR is booking anything with a pulse); if the ratio is 40% or lower the hand-off bar is too tight or the SDR-to-AE communication is broken. The healthy zone is roughly 60-80%.

### When the founder is the SDR-AE-hybrid, and when to hire the split

The single most-consequential timing decision in the SDR-AE motion at seed is *when to stop being the seller yourself*. mod-105 develops the founder-led sales motion — the founder personally prospects, discovers, demos, negotiates, and closes the first 20-30 deals. That founder-led phase produces the raw material the SDR-AE motion is built from: the working discovery script, the demo narrative that closes, the objections the buyer actually raises, the pricing conversation that lands, the target-account list that responds. Without that raw material, the SDR-AE motion is an empty shell.

**Signals the founder-led motion is ready to hand off** (per Kazanjy's *Founding Sales* and the Roberge / Skok / Kellogg canon):

- The founder has personally closed **20-30 paying deals** with a consistent ICP.
- The **close rate on qualified opportunities is stable** — the same win rate this quarter as last quarter, indicating the motion is reproducible rather than founder-luck.
- The **discovery script and demo narrative are written** — the founder can hand them to a stranger and the stranger could run a passable version tomorrow.
- The **objections the buyer raises are known and answered** — the founder has heard the same 5-10 objections and has a defensible response to each.
- The **target-account list is characterised** — the founder can describe why an ICP-fit account converts and an off-fit account does not; the SDR will inherit a list, not build one blind.
- The founder has become the **bottleneck on capacity, not the bottleneck on knowledge** — the calendar is fully booked with demos and closes; the constraint is her time, not her insight into what to say.

When all six signals are present, the founder is ready to hire the split. When any signal is missing, the founder is not ready — hiring produces a rep who cannot draw on the founder's un-transferred pattern-knowledge, and the rep fails.

**Which role first — AE or SDR?** Standard practitioner advice (Kazanjy, Roberge, most YC content): **the first hire is an AE**, not an SDR. The founder continues to be the SDR (or hires an SDR contract role, or splits the SDR job across a growth or ops hire) while the first AE takes over the demo / proposal / close side of the motion — the highest-leverage part of the founder's time to reclaim. The SDR hire follows once the AE is closing at target and the AE is complaining about pipeline volume. Hiring an SDR first without an AE to close the meetings produces booked meetings that the founder still has to run — the founder's time is not reclaimed and the SDR's output is bottlenecked on the founder.

The one exception: **PLG-heavy motions where a sales-assist role fills the AE slot**. In a stacked PLG-plus-sales-assist motion (Chapter 2), the founder may hire a sales-assist rep before a full AE, because the sales-assist role is lighter and closer to the founder's own working style. The PLG-side hand-off then follows the sales-assist SLA rather than an SDR-AE hand-off bar.

**When to hire the SDR.** Once the AE is closing at target and complaining about pipeline volume — usually 4-8 months after the AE hire — the SDR hire follows. Common structure: hire 1 SDR to feed the AE; add a second SDR when the first is booking at target and the AE's pipeline coverage is still below the target ratio (typically 3-4× annual quota in open pipeline).

**When to hire the sales manager.** *Not until the third or fourth AE.* Hiring a sales manager to manage one or two AEs is over-investment; the founder or VP-of-something-else can manage two AEs. Hiring a VP Sales before PMF and before a repeatable motion is the canonical wrong-first-hire pattern (mod-110 develops this).

### The tooling stack

The working modern SDR-AE tooling stack (working defaults; every team modifies):

- **CRM** — Salesforce (enterprise / larger scale) or HubSpot (SMB and early mid-market). Attio and Close are modern alternatives at seed scale. The CRM is the source of truth for opportunities, stages, and forecast.
- **Sales engagement / cadence platform** — Outreach.io, SalesLoft, Apollo, Groove. Owns the cadence execution; syncs to CRM. Apollo has the advantage of also including contact data (avoids buying ZoomInfo separately) and is a common seed-stage choice.
- **Contact-data / enrichment** — ZoomInfo, Apollo, LinkedIn Sales Navigator, Clay. Provides contact enrichment for the target-account list.
- **Conversation-intelligence** — Gong, Chorus (SalesLoft), Fireflies. Records and analyses sales calls; used for coaching and win / loss analysis. Not required at seed but valuable once there are 2+ AEs.
- **Proposal / e-signature** — DocuSign, PandaDoc, HelloSign. E-signature for the close.
- **Calendaring** — Chili Piper, Calendly, HubSpot Meetings. Used for demo booking and lead routing.
- **Data warehouse + BI** — Snowflake / BigQuery / Redshift + Looker / Mode / Metabase. Where the pipeline metrics get modelled once the CRM's built-in reporting is insufficient.

The stack decision is not innocent — each tool has a monthly cost, an onboarding cost, and an integration cost. At seed scale the stack should be minimal (CRM + cadence + enrichment + calendaring); each additional tool has to earn its cost. Buying the full enterprise stack before the motion is validated is a common failure — the team invests months in Salesforce configuration for a motion that ultimately does not fit the market.

## Concrete example — Loomly hires the SDR-AE split

By the time Loomly's founder Jane has personally closed 25 mid-market deals (per mod-105) using the SDR-AE-hybrid motion (she is running discovery / demo / close herself, with the PLG top-of-funnel from Chapter 2 feeding half the pipeline), the six readiness signals are all present: 25 closed deals, stable 32% close rate on qualified opportunities, discovery script and demo narrative written, objections known, target-account list characterised, calendar fully booked with demos.

**Step 1 — Hire the first AE.** Jane hires an AE with 3-5 years' mid-market SaaS experience, ICP-adjacent industry background (devtools or infrastructure preferred). Comp: $130K base + $130K variable at plan = $260K OTE against a $1.3M annual quota (5× OTE, mid-market benchmark). Ramp: 4 months to full quota (typical for mid-market). Onboarding: 6 weeks of shadowing Jane's calls, taking over as second-chair on live demos in weeks 3-4, running first solo demos in week 5, first solo close in week 6.

**Step 2 — Founder stays as SDR-hybrid.** For the first 3 months of the AE's ramp, Jane continues prospecting personally (with the PLG top-of-funnel feeding half the pipeline). The AE receives ~15 opportunities / month from Jane's prospecting + PLG hand-off; ~12 hold; ~7 pass qualification. AE runs 7 opportunities through the funnel; closes 2-3 per month by month 4.

**Step 3 — Hire the first SDR.** At month 5 the AE is at target close rate but complaining about pipeline capacity — she can handle 15 opportunities / month but is receiving 10. Jane's prospecting time is at its limit and PLG signals are being handled slower than the SLA. Hire the first SDR: $70K base + $30K variable = $100K OTE, target 30 booked meetings / month with a hand-off-accepted ratio of 65%+. Onboarding: 4 weeks of shadowing Jane's prospecting, 2 weeks of ramping into own book, week 7 target 20 booked meetings, month 3 target full 30.

**Step 4 — The cadence design.** SDR takes over the cadence Jane was already running: 12-touch, 4-week, Level-2 personalised for the top 200 accounts, Level-3 for the top 50. Channels: email (Outreach.io), LinkedIn (Sales Navigator), phone. Video message for Level-3 tier. Cadence template exists in Outreach; SDR runs 2 cadences: outbound-cold-mid-market (200 accounts/month rotation) and PLG-triggered-sales-assist (PQL alerts from the product; SLA 4-hour reach-out).

**Step 5 — The hand-off protocol.** SDR writes a hand-off note in HubSpot with the five criteria (ICP-fit rationale, buyer role, one-line pain, confirmed meeting, timeline signal). AE reviews before each discovery call and marks accept / reject. Weekly Monday standup: SDR and AE review the previous week's hand-off ratio, discuss any rejected hand-offs, tune the qualification bar together. Month-1 hand-off ratio: 55% (too tight — SDR is over-qualifying and under-booking). Month-3 hand-off ratio: 72% (healthy zone).

**Step 6 — Instrumentation.** HubSpot dashboards track: touches per SDR per week, booked meetings per SDR per week, held meetings, hand-off-accepted opportunities, opportunities per AE, opportunity → close win rate per AE, average sales cycle per AE, quota attainment per AE. Weekly forecast meeting on Fridays: AE runs each open opportunity through SPICED coverage; each opportunity's stage-exit criteria are named; forecast is committed or downgraded on the call, not in the founder's inbox.

**Step 7 — The transition.** By month 8 the AE is at 100% quota, the SDR is at 30 meetings / month, and Jane's time on selling has dropped from 40 hours / week to 6 hours / week (kept for the enterprise-adjacent expansion deals that the AE is not yet ready for). Jane can now spend time on the next motion decision — hire the second AE and expand into an enterprise motion for the top-of-market accounts (Chapter 4), or double down on the PLG layer and hire a growth engineer, or expand internationally. The motion decision is Chapter 1's matrix run again with new inputs.

The transition took 8 months. If Jane had hired the AE at month 3 instead of month 12, the AE would have inherited a motion that had not yet been tested at scale, would have failed against objections Jane had not yet heard, and would have consumed a year of runway rebuilding what Jane's own selling would have produced faster.

## Common failure patterns

- **Hire-the-SDR-before-the-AE trap.** Founder hires an SDR because "we need pipeline." SDR books meetings; founder still has to run them all; founder's time is not reclaimed; SDR's output is bottlenecked on founder's calendar. Fix: hire the AE first; hire the SDR only after the AE is at target and complaining about pipeline volume.
- **Hire-the-VP-Sales-before-PMF trap.** Founder hires a VP Sales at pre-Seed to "lead the sales effort." VP Sales installs a Salesforce configuration, hires SDRs and AEs, ships a playbook — none of which is tested against real buyers because the founder had not yet run 20-30 deals herself. Six months later, cash-burn spike, no revenue, VP Sales fired. Canonical wrong-first-hire pattern; mod-110 develops the diagnosis. Fix: founder-led sales through PMF; first AE after; VP Sales only after ≥3 AEs.
- **Cadence-templates-imported-without-tuning trap.** Team copies an Outreach template from a public blog post; runs it for 6 weeks; response rate is 0.4%. Team concludes "outbound doesn't work for our market." Actual issue: the template was designed for a different ICP with different pain and different objections. Fix: cadences are derived from the founder's own working scripts; templates are inputs to the derivation, not substitutes for it.
- **Hand-off bar too loose trap.** SDR books anything with a pulse to hit meeting quota. AE inherits 25 opportunities / month, only 8 of which are real; AE burns time; AE close rate is 12%; AE blames SDR. Fix: hand-off criteria are explicit; SDR-AE Monday standup reviews rejected hand-offs and tunes the bar; hand-off-accepted ratio has a target (60-80%).
- **Hand-off bar too tight trap.** SDR over-qualifies; books only pre-qualified accounts; misses booked meetings for accounts that would have converted with an AE's discovery. Hand-off-accepted ratio is 95%+; AE's pipeline coverage is thin. Fix: relax the bar; move borderline accounts to AE-with-note rather than SDR-nurture.
- **Meeting-booked-not-held trap.** SDR reports 40 meetings booked; only 18 actually happen. AE hasn't been told about the no-shows; forecast is based on the booked number. Fix: track booked vs. held separately; forecast on held; SDR compensated on held-meeting attainment, not booked.
- **Tools-before-motion trap.** Team spends 3 months configuring Salesforce and Outreach before running a single outbound touch. Configuration is theoretical because nobody has tested what actually converts. Fix: start with the minimum-viable tooling stack; ship the motion; add tooling as bottlenecks appear.
- **Founder-still-selling-past-hand-off-point trap.** Founder hires the AE but continues personally closing deals; AE inherits leftovers; AE ramp fails because AE is not given the strongest opportunities. Fix: at hand-off, founder stops selling primary deals; founder pipeline becomes 100% AE's; founder role shifts to enterprise / expansion / new-market.
- **Cadence-with-no-break-clause trap.** SDR runs cadences without a defined breakup email; accounts get emailed indefinitely; domain reputation crashes; deliverability collapses. Fix: every cadence has a defined final touch; unresponsive accounts move to nurture, not re-cadence.
- **Comp-plan-not-aligned-to-motion trap.** SDR compensated on meetings booked (not held); AE compensated on opportunity-created (not closed). Each rep optimises for their own metric, degrading the motion. Fix: comp plans align to the metric that most closely predicts revenue — SDR on held meetings or hand-off-accepted opportunities; AE on closed revenue (with clawbacks for cancellations within 90 days).
- **Ignoring-benchmarks trap.** Team reports SDR's 25 meetings / month as "good" without checking that mid-market SDR benchmark is 30-50. Under-performance is invisible. Fix: publish benchmarks on the dashboard; deltas from benchmark are diagnosable.
- **One-channel-only trap.** SDR runs email-only cadences. Response rates 40% below multi-channel. Team blames "cold email doesn't work." Fix: multi-channel; add LinkedIn touches, add phone, add video for top-tier accounts.
- **Personalisation-race trap.** Team decides "everything gets Level 3 personalisation." SDR spends 40 minutes per account; volume drops from 200/month to 40/month; pipeline collapses even though per-touch conversion is higher. Fix: tier personalisation by ICP fit; Level 3 to the top 50, Level 2 to the next 200, Level 1 to the long tail.

## Summary

- The SDR-AE inside-sales motion is the workhorse of mid-market B2B SaaS. It descends from Aaron Ross's *Predictable Revenue* (2011), refined by Roberge's *Sales Acceleration Formula* (2015) and McMahon's *The Qualified Sales Leader* (2020) — three books that form the working canon.
- **Role split**: the SDR owns top-of-funnel (prospecting, cadence, inbound qualification, hand-off); the AE owns middle-and-bottom-of-funnel (discovery, demo, proposal, close, sometimes expansion). Each role has its own metric, its own quota, its own comp plan.
- **Ratios**: 1-3 SDRs per AE for mid-market; 3-5 for low-mid-market; 0.5-1 for enterprise. The correct ratio keeps the AE's calendar full without stuffing it.
- **Cadence design**: multi-channel (email + LinkedIn + phone + video), multi-touch (8-14 touches over 3-6 weeks), tiered personalisation (Level 1 for the long tail, Level 3 for the top of the ICP list), timing-disciplined, with an explicit break clause.
- **Response-rate benchmarks**: open 30-50%, reply 3-8% (Level 2) or 8-15% (Level 3), meeting-booked 1-3% of touches, meeting-held 60-80% of booked, meeting-to-opportunity 40-60% of held, opportunity-to-close 20-40%. Benchmarks are diagnostic ranges, not laws.
- **Hand-off criteria**: ICP-fit confirmed, buyer role identified, pain articulated, meeting confirmed, timeline signal. Hand-off-accepted ratio target is 60-80% (looser = SDR over-books; tighter = SDR under-books).
- **Timing the split**: the founder is the SDR-AE-hybrid for the first 20-30 deals (mod-105). Hire the **AE first** once six readiness signals are met (closed deals, stable close rate, written script, known objections, characterised list, capacity-not-knowledge bottleneck). Hire the **SDR after** the AE is at target and complaining about pipeline capacity. Hire the **sales manager** only after ≥3 AEs. The **wrong-first-hire pattern** — VP Sales before PMF — is a common cash-burn spike.
- **Tooling stack**: minimum-viable at seed (CRM + cadence + enrichment + calendaring); add conversation-intelligence, proposal / e-signature, and BI as the team scales. Do not over-invest in tools before the motion is validated.
- **Failure modes**: hire-order inversion (SDR first, or VP Sales too early), cadence-templates-without-tuning, hand-off bar too loose or too tight, ignoring benchmarks, one-channel cadences, personalisation-race, tools-before-motion.
- The SDR-AE motion is often the **middle-tier** in a stacked motion — PLG feeds it from above (Chapter 2's sales-assist trigger), enterprise pulls specific deals out the top (Chapter 4). The stacking is designed deliberately; each layer has defined entry and exit.
- Chapter 4 develops the **enterprise MEDDIC / MEDDPICC motion** for the high-ACV band above the SDR-AE motion. Chapter 5 threads the qualification framework — SPICED, MEDDIC, MEDDPICC — through every stage of the CRM funnel.
