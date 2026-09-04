# Diagnosing Motion Mismatches — a Repeatable Teardown

## Motivation

Chapters 2, 3, and 4 develop the three motion archetypes — PLG, SDR-AE inside sales, enterprise MEDDPICC — each in the shape it works when applied to the ICP + ACV combination it was designed for. Chapter 5 threads MEDDIC / SPICED / MEDDPICC discipline through the CRM stages so the pipeline can be *read* rather than intuited. This chapter closes the loop: **how to look at a struggling GTM motion — bad conversion rates, stalled pipeline, CAC that eats the ACV, sales team demoralised — and diagnose whether the fix is inside the motion (execution, discipline, tooling, hiring) or outside it (the motion itself is the wrong archetype for the market the founder is actually selling to)**.

The distinction matters because the remedies look nothing alike. An in-motion problem is a coaching / hiring / tooling problem: relax the SDR-AE hand-off bar, hire the sales-assist role, refresh the cadence template, add the second SE. A motion-mismatch problem is a *strategy* problem: the motion has to change, the roles the founder has hired become the wrong roles, the pricing pack has to move, and — in the hardest case — the founder has to publicly reverse a strategic decision made 6-18 months earlier. Teams that confuse the two invest another quarter tuning the wrong knobs and continue not producing revenue; teams that name the mismatch honestly can pivot in weeks.

The failure mode this chapter exists to catch: **the founder looks at a stalled pipeline and reaches for the in-motion levers first — hire another SDR, raise the SPICED bar, buy a better cadence tool, coach the AE harder, spend more on paid ads — when the actual diagnosis is that the motion never fit the ICP + ACV combination to begin with. Six months later she has spent another $500K-$1M on the wrong motion and the fundraise conversation gets much harder.**

This chapter is not new operating discipline. It is a *reading practice* against the artifacts Chapters 1-5 already produce — the ICP + ACV matrix cell (Chapter 1), the PLG funnel instrumentation (Chapter 2), the SDR-AE cadence and hand-off metrics (Chapter 3), the MEDDPICC coverage panels (Chapter 4), and the CRM stage-with-artifact discipline (Chapter 5). The teardown is a diagnostic pipeline you run *against your own numbers*, monthly at seed and weekly at Series A, and every quarter with a broader retro.

## Core concepts

### The four canonical mismatches

Chapter 1 named three mismatches from the practitioner literature (Kazanjy, Bush, Skok, Ross, Roberge). This chapter adds a fourth (the sub-scale CAC trap) and develops each into a diagnostic pattern with named symptoms, a named root cause, and a named prescription. The four canonical mismatches:

1. **Enterprise ceremony on a self-serve product** — the motion is heavier than the ACV supports; buyer disengages at the ceremony step; the CAC swallows the ACV.
2. **Self-serve on a $100K contract** — the motion is lighter than the deal shape requires; buyer's procurement / security / legal path has no vendor-side owner; the deal stalls in a Slack DM.
3. **Mid-market SDR-AE on a bottoms-up developer product** — the motion targets the wrong buyer; SDRs cold-call heads of engineering for a product adopted individually by developers; no pipeline forms.
4. **Sub-scale CAC / payback on any motion** — the motion's cost per closed customer exceeds what the ACV can amortise inside the retention window; the unit economics never survive contact with the actual customer base regardless of how well the motion executes.

Every real-world mismatch this chapter has seen in the practitioner literature or in early-stage GTM reviews maps to some combination of the four. A "custom" mismatch is usually one of the four with a different label.

### The three symptom families — what a mismatch looks like from the outside

Before naming the mismatch, name the *symptoms*. Symptoms cluster into three families; a mismatch usually surfaces in at least two of the three simultaneously.

**Family A — unit-economic symptoms.** The CAC / payback numbers do not survive.

- CAC is > 12 months of ACV (mid-market benchmark: CAC payback ≤ 12 months; enterprise: ≤ 18-24 months; self-serve: ≤ 6 months).
- Blended CAC has climbed quarter-over-quarter with no offsetting expansion revenue.
- Gross margin on the closed cohort is negative after allocating full sales-team cost.
- Payback stretches past the median retention window (a 24-month payback on a product whose median customer churns at month 18).

**Family B — funnel-shape symptoms.** Conversion rates fail sharply at a specific stage boundary.

- Sign-ups accumulate at the top but paid conversion is stuck at 1-2% quarter after quarter (a PLG symptom — usually a broken or missing activation event / PQL / upgrade prompt, but sometimes the motion mismatch itself).
- SDR books meetings; AE takes discoveries; almost none advance past Discovery to Evaluation (mid-market mismatch on the wrong buyer).
- Enterprise deals reach Proposal but slip a quarter every quarter (enterprise motion running without MEDDPICC discipline, or SPICED-based mid-market motion trying to run an enterprise deal).
- Sales-assist reach-outs go out and no one replies (PLG signal is too weak; account never actually reached PQL).

**Family C — team-and-narrative symptoms.** The people around the motion tell you something is off.

- Sales team is demoralised and turnover is elevated; AEs quit within their ramp period.
- The founder is the only person closing deals despite having hired the AE 6 months ago (mod-105 boundary or motion mismatch — Chapter 3 develops the founder-still-selling trap).
- The buyer's language and the vendor's pitch language diverge — buyers ask for things the pitch doesn't discuss, and the pitch talks about things buyers don't ask about (a positioning / ICP problem from mod-103 / mod-104 that a motion cannot fix).
- The investor updates hedge: "we're still tuning the motion," "we're seeing green shoots," "conversion is improving month-over-month but from a low base" — the language of a founder who cannot yet name the motion that works.

A mismatch usually has one Family-A signal, one Family-B signal, and one Family-C signal running simultaneously. A single-family signal is often an in-motion problem; a cross-family cluster is usually a mismatch.

### The teardown — a five-step pipeline

The mismatch-diagnosis teardown runs five steps in order. Skipping steps is how founders confuse in-motion problems with mismatches.

**Step 1 — Locate the actual motion on the Chapter 1 matrix.** What ICP + ACV combination is the motion designed for? What ICP + ACV combination is the pipeline *actually* selling to? If the two don't match, the mismatch is named — the founder has installed the wrong motion for the market she is in.

**Step 2 — Read the Chapter 5 CRM signals honestly.** Which stage is the pipeline leaking at? Which artifact is missing at that stage? Which MEDDPICC / SPICED letter is systematically red? The CRM is the diagnostic surface; if it hasn't been run with artifact-per-stage discipline (Chapter 5), the teardown pauses here until it has been.

**Step 3 — Score the symptom family cluster.** For each of the three families (A / B / C), name the specific symptoms observed in the last quarter, with the specific number attached (not "CAC is high" but "CAC payback is 22 months against a mid-market benchmark of ≤ 12"). Symptoms are named quantitatively; anecdotes are converted into numbers.

**Step 4 — Match to a canonical mismatch (or rule them out).** Against the four canonical mismatches above, does the symptom cluster fit? Test each; a mismatch that fits has *all three families* of symptoms consistent with it. If no mismatch fits, the problem is probably in-motion (execution, hiring, tooling, discipline) — the teardown exits at Step 4 with an in-motion prescription (relax the hand-off bar, hire the sales-assist role, re-templatise the cadence, refresh the pricing pack, etc.).

**Step 5 — Prescribe the fix and the sequencing.** If a mismatch is named, prescribe the fix in the shape Chapters 1-5 provide: the new motion, the pricing-pack change that supports it (mod-106), the ICP re-scoping if needed (mod-104), the hiring changes (which roles become wrong, which roles become required), and the *sequencing* — what to stop first, what to keep running while the new motion ramps, what to communicate to the team, the board, and the customers. Motion pivots are not overnight; a plan without sequencing produces a whipsaw that costs another quarter.

Steps 1-2 usually take a half-day when the CRM has been run cleanly (Chapter 5); a full week if the CRM has to be reconstructed first. Steps 3-4 take a half-day. Step 5 is a one-day founder-plus-first-hire working session with a written output. The full teardown is on the order of one week of founder time.

### Mismatch 1 — enterprise ceremony on a self-serve product

**Symptoms.**

- Family A: CAC per closed customer is 3-10× the ACV; payback runs 36-60 months against a self-serve benchmark of ≤ 6 months. Sales team cost per rep is $200-400K OTE against a product whose ACV averages $2-8K. Blended margins after full-cost allocation are deeply negative.
- Family B: Free-tier or trial sign-ups accumulate; paid conversion is 0.5-2% (compared to the OpenView 3-5% low-end benchmark for PLG). AEs are running discovery calls on 30-40 opportunities/month; most take one call and go silent. Sales-assist SLA is being met but conversion on sales-assist calls is 2-3× worse than on pure in-product upgrades — the human touch is *reducing* conversion.
- Family C: Buyers say "I just wanted to try it, I don't want a call" in survey exits. AEs complain that "the deals are all $5-10K and take as long as the $50K deals used to." The competitor list is dominated by self-serve products with $10-100/month sticker prices; the founder is pitching against Notion, Linear, and Superhuman with an enterprise deck.

**Root cause.** The motion was chosen from the founder's background (usually ex-enterprise-sales founder) or from an early large deal that suggested "enterprise potential" (mod-107 Chapter 1's *enterprise-because-one-big-logo-asked* trap). The ICP is dominated by self-serve buyers with small-team budgets; the pricing pack is either at $99/month with an enterprise team stapled on top, or at $2K/month with a full enterprise ceremony that the ACV cannot amortise.

**Prescription.**

- **Kill the enterprise ceremony for the primary ICP.** Ship the self-serve checkout, in-product upgrade prompts, and PQL-driven sales-assist trigger from Chapter 2. Move existing enterprise-style AEs to sales-assist roles (30 min calls with a light Situation / Fit / Next Step playbook, not 60 min SPICED discoveries) or reallocate.
- **Rebuild the pricing pack (mod-106) to support one-click self-serve upgrade.** A per-seat or per-usage metric at a per-month price that a credit card can complete.
- **Preserve an enterprise tier as an optional layer** for the small subset of accounts that genuinely need MSA, security review, and procurement — but do not treat that layer as the primary motion. It is a Chapter 4 layer on top of a Chapter 2 primary motion, and the enterprise tier's ACV threshold has to be high enough (usually $50-100K) that the ceremony cost amortises.
- **Sequence** — announce the pack change to the team; run the new self-serve motion in parallel with the enterprise motion for a quarter; kill the enterprise motion for accounts below the tier threshold once the self-serve conversion stabilises; communicate the change to existing customers grandfathered on the old pack (mod-106 Chapter 5's grandfathering discipline is load-bearing here).

**Example (compressed).** A team ships a developer productivity tool at $2K/month per team; sales team is 2 AEs and 1 SDR at $250K OTE each. After 9 months: 400 free sign-ups, 6 paid customers, blended CAC $85K per customer, gross margin deeply negative. Symptoms across all three families. Teardown at Step 4 matches Mismatch 1. Prescription: rebuild the pricing pack to per-seat at $19/user/month, ship a self-serve Stripe checkout, retain one AE as sales-assist for teams > 20 seats, reallocate the second AE to a product-marketing role, let the SDR go. Nine months post-pivot: 400 paying accounts, blended CAC $180, positive payback at month 3.

### Mismatch 2 — self-serve on a $100K contract

**Symptoms.**

- Family A: ACV per closed deal on the enterprise tier is $80-150K but the actual booked revenue is well below plan; deals close in nominal terms but at heavily-negotiated discounts because the vendor has no procurement counterpart. Deal cycle time is highly variable — some close in 2 weeks, others drift for a year. Forecast accuracy is poor; the enterprise pipeline is un-forecastable.
- Family B: Champion-level engagement is high (Slack DM active, product being used heavily) but deals stall between "we're going to sign this" and actual signature. Pipeline shows 8-12 enterprise opportunities at "Verbal" or "Committed" for 3+ quarters. Legal / procurement / security stages don't exist in the CRM because the vendor has no motion to run against them.
- Family C: Champions complain that "our procurement is being difficult" or "legal is taking forever." The founder personally handles every enterprise redline (badly, because she is not a lawyer). Champions who initially loved the product go silent after they hand the deal to their internal procurement team. Ex-champion customers refer new champions who repeat the cycle.

**Root cause.** The motion is PLG-primary with sales-assist for mid-market, but a subset of ICP accounts is genuinely enterprise (Fortune 500 / regulated industry / high-headcount / formal procurement). The vendor has no enterprise-side owner for the Paper Process, Decision Process, or Economic Buyer conversations — no MEDDPICC discipline, no SE role, no legal readiness (MSA template, DPA, SOC2 report, security questionnaire package), no procurement counterpart.

**Prescription.**

- **Segment the enterprise-shaped accounts explicitly.** Which accounts have > 500 employees, require formal procurement, or ask for a redlined MSA on first contact? Those accounts move to an enterprise motion (Chapter 4). Everything below stays on the PLG + sales-assist motion (Chapter 2).
- **Build the enterprise motion the accounts require.** Hire the first enterprise AE (or convert an existing senior AE), retain an SE resource (founder / CTO on the first 2-3 deals per Chapter 4's rhythm), retain external SaaS-contract counsel, ship the security package (SOC2 report, pen-test summary, DPA template, data-flow diagram), publish a Loomly-preferred MSA template.
- **Layer the two motions in the CRM.** Chapter 5's `Motion` custom field routes each opportunity to the right qualification panel (SPICED for PLG-assist / mid-market; MEDDPICC for enterprise); Chapter 4's rhythm (weekly enterprise deal review, monthly executive review, QBRs) is installed only for the enterprise slice.
- **Sequence** — announce the enterprise motion to the sales team; take the first 3-5 stalled enterprise deals through the new motion under the founder's direct supervision (co-run with the enterprise AE) to characterise the playbook; hire the first SE after the first enterprise close; scale from there.

**Example (compressed).** A PLG-primary company reaches Series A on strong self-serve numbers; enterprise tier has been added but is closing 20% of the pipeline it originates because the vendor has no procurement-side motion. Symptoms across Family B (stalled deals) and Family C (champions going silent post-hand-off). Teardown matches Mismatch 2. Prescription: hire the first enterprise AE, run three stalled deals through the new motion, close two of the three within 90 days, characterise the SE playbook via the CTO on the second deal, hire the first SE at month 6, scale enterprise motion to 15% of company revenue by month 12.

### Mismatch 3 — mid-market SDR-AE on a bottoms-up developer product

**Symptoms.**

- Family A: Blended CAC is 2-4× ACV against a mid-market benchmark of ~1×; payback is 24-36 months against a benchmark of ≤ 12. SDR-AE team is expensive ($120-180K OTE for SDR, $200-280K OTE for AE) but the pipeline they produce is not converting.
- Family B: SDR reports 25-35 booked meetings/month against a target of 30-50; held rate is 40-50% (below the 60-80% benchmark); meeting-to-opportunity conversion is 10-15% (below the 40-60% benchmark). AE close rate on outbound-sourced pipeline is 5-10% (below the 20-40% mid-market benchmark). Meanwhile the product has 3-10K individual free-tier or unpaid developers actively using it; no paid tier or team plan exists.
- Family C: SDR cold-calls the VP Engineering; VP Engineering has never heard of the product and forwards the email to a random engineer for evaluation; the engineer already uses the product on nights-and-weekends but is not the buyer, so the SDR's "we should schedule a demo" reads as friction. AEs run demos where the buyer they were sent to says "the engineers actually use this — I'll defer to them." The engineering team's Slack channel has an active enthusiastic community for the product; none of it appears in the CRM.

**Root cause.** The motion targets the *buyer* while the *user* is actually driving adoption. Bottoms-up developer products (Vercel, Supabase, Retool, PostHog, Linear at seed) discover buyers through organic engineer adoption — Google search for "how do I fix X," Hacker News, developer conferences, open-source contributions. The formal buyer (VP Engineering, CTO) enters the process only after 5-30 engineers at the account are already using the product; a cold SDR-AE motion aimed at the buyer skips the entire adoption loop and disintermediates the mechanism that would have produced the deal.

**Prescription.**

- **Rebuild the top-of-funnel as PLG (Chapter 2).** Ship the free tier, the activation event, the PQL definition, the in-product upgrade prompts. Instrument via Amplitude / PostHog / Segment / Chameleon.
- **Replace the SDR role with a growth engineer / developer-experience role.** The SDR's job (cold outbound to a buyer who doesn't know the product) doesn't fit the motion; the growth engineer's job (improve activation, ship in-product prompts, run onboarding experiments) does.
- **Retain the AE role as sales-assist**, feeding from PQL alerts on accounts where 5+ activated developers work at an ICP-fit company; the AE's job is to bridge the developer-adopted product to the VP Engineering / procurement conversation the *account* eventually requires — not to cold-generate the opportunity.
- **Reset the pricing pack (mod-106) around per-seat or per-usage in a range that a credit-card team plan can complete self-serve** ($10-50/user/month for the mid-market team tier); reserve the enterprise tier for accounts crossing the sales-assist ACV threshold (Chapter 2).
- **Sequence** — freeze new SDR outbound; keep the AE running only on the accounts that have crossed the PQL threshold; ship the free tier and activation instrumentation in parallel; measure activation and PQL rates weekly; expect a 60-90 day rebuild before the funnel starts to show recovery.

**Example (compressed).** A developer productivity tool team has 2 SDRs and 1 AE at $500K/year fully-loaded; 6 months of outbound has produced 3 paid deals at $18K/year, blended CAC $85K, obvious mismatch. The product also has 6,000 active free-tier developers who signed up via community referral; no team plan exists. Teardown matches Mismatch 3. Prescription: let the 2 SDRs go, redeploy the AE to sales-assist, hire a growth engineer at $180K, ship the team plan at $25/user/month, ship the activation event and PQL definition, monitor the free-tier-to-paid funnel weekly. Nine months post-pivot: 400 team-plan accounts averaging 6 seats at $25/seat/month = $1.4M ARR from a customer base that was already there but had no path to pay.

### Mismatch 4 — sub-scale CAC / payback on any motion

**Symptoms.**

- Family A: Regardless of motion, the CAC to close a customer exceeds the annual revenue that customer produces, and the retention window is not long enough for expansion to close the gap. Payback beyond 30-36 months even after full expansion modelling.
- Family B: Motion conversion rates may look "okay" on relative terms but the absolute deal size is too small to support the cost of the motion — a well-run SDR-AE motion produces a healthy 25% close rate at an ACV of $6K but the CAC of $12K per closed customer never amortises.
- Family C: Investor updates begin talking about "unit economics" more than pipeline; the CFO's forecast turns cautious; hiring freezes without a stated pivot; the sales team senses uncertainty about their own quotas.

**Root cause.** The motion is correct for the ICP but the ACV is too low, *or* the motion is correct for the ACV but the ICP requires a heavier motion than the ACV supports (usually a two-role split where the ICP has a formal buyer / procurement / security path but the pricing pack has not caught up).

**Prescription.**

- **Move the pricing pack up-market (mod-106).** If the ICP genuinely supports a higher ACV — bigger companies, more users per account, higher usage, longer contracts — the pricing pack should reflect that. A per-seat pack with a low anchor tier ($6/seat/month) trying to serve enterprise ICPs is a common trap; the fix is to add an enterprise tier ($20-50/seat/month) with the features the ICP actually needs (SSO, audit logs, priority support, custom SLA).
- **Or move the ICP down-market.** If the ICP supports the ACV the current pack targets but the motion is priced too heavily for the ICP (SDR-AE for $6K deals; enterprise MEDDPICC for $40K deals), reduce the motion cost — replace SDR-AE with PLG + sales-assist, replace enterprise MEDDPICC with SDR-AE, and let the leaner motion serve the deals the ICP actually generates.
- **Do not brute-force volume through a broken unit-economic motion.** Adding SDRs to a motion whose per-deal CAC is 3× ACV multiplies the loss; it does not compound to profitability. The unit economics have to be solvable at the *first* closed customer before any scaling.
- **Sequence** — model the pack change (mod-106); test with a limited pilot (2-3 deals); confirm the CAC / payback modelling holds on those pilots; then rebuild the pack, the motion, and the team allocation for the new equilibrium.

**Example (compressed).** A team runs an SDR-AE motion at $180K AE OTE + $90K SDR OTE + tooling; blended CAC per closed customer is $22K against an average ACV of $8K. Even with 130% NRR the payback is 32 months against a retention median of 26 months. Symptoms in Family A + hedging in Family C. Teardown matches Mismatch 4. Prescription: (a) move up-market — add a $30K enterprise tier for the top of the ICP list; (b) move down-market for accounts below $15K — introduce a self-serve tier and a sales-assist trigger; (c) reduce total sales headcount from 2 AEs + 1 SDR to 1 AE + 1 sales-assist rep during the transition. Six months post-pivot: enterprise tier averaging $34K ACV across 12 accounts; self-serve tier averaging $6K ACV across 55 accounts, both at defensible CAC / payback.

### Compound mismatches — when more than one canonical pattern fits

Not every mismatch fits one canonical pattern cleanly. Common compounds:

- **Mismatch 1 + Mismatch 4** — enterprise ceremony on a self-serve product *and* sub-scale CAC. Usually the diagnosis is Mismatch 1 (enterprise ceremony is the primary problem; the CAC is a downstream symptom) but the pack change (kill the enterprise ceremony) is the same either way.
- **Mismatch 2 + Mismatch 4** — self-serve on a $100K contract *and* sub-scale CAC. The enterprise deal cost lands on a PLG cost-base; the payback fails because the enterprise motion has no dedicated capacity. Prescription: build the enterprise motion (Mismatch 2 fix) and re-model the CAC across the two motions separately (Mismatch 4 discipline).
- **Mismatch 3 + Mismatch 2** — a bottoms-up developer product with a small subset of legitimate enterprise accounts. The primary motion should be PLG (Mismatch 3 fix), with an enterprise layer (Mismatch 2 fix) for the accounts that cross the enterprise threshold. A stacked motion, designed deliberately.

Compound mismatches usually need to be *unstacked* — name each mismatch, sequence the fixes. Attempting to fix all of them simultaneously is Chapter 1's *run-all-three-motions-simultaneously* trap in the pivot form: three under-invested pivots produce less improvement than one properly-invested pivot.

### The mismatch-vs-execution differential — a decision rule

The teardown's most important call is *is this an in-motion execution problem or a motion mismatch?* A working differential:

- **The problem is in-motion execution if** the symptoms are single-family (Family A alone, or Family B alone), the CRM shows a clear stage the deals leak at, the leak has a named artifact-or-discipline root cause (Chapter 5's stage-exit patterns), and the historical conversion at the leaking stage has been better before some specific change (a new AE hire, a new cadence template, a new pricing pack). Fix: the specific in-motion knob at that stage.
- **The problem is a motion mismatch if** the symptoms cross at least two of the three families, the CRM shows failure across multiple stages rather than one, the underlying ICP + ACV combination does not match the motion the founder installed, and no in-motion knob has produced sustained improvement over the last 2-3 quarters. Fix: pivot the motion per one of the four canonical patterns.

The differential is not perfect — some in-motion problems look like mismatches (a bad first AE hire can produce Family A + B + C symptoms), and some mismatches surface first as apparent in-motion issues (a Mismatch 3 usually looks like "our SDRs aren't performing" for the first quarter before the founder realises the SDR role itself is wrong). The tie-breaker: **if two consecutive quarters of in-motion fixes have not moved the numbers, escalate to a mismatch teardown**. Two quarters is enough time to see whether an in-motion fix is going to work; not so much time that a mismatch goes un-diagnosed for a year.

### Communicating a motion pivot — the four audiences

A motion pivot is a strategic reversal. It has four audiences and each needs a different communication:

- **The team.** Direct, specific, and blame-free — the motion was wrong for the market; we know what to change; here is the sequence and here is what each person's role becomes (or does not). Ambiguity in the team-facing communication is what produces the quiet resignations three weeks after the pivot announcement.
- **The board / investors.** Named honestly and framed as a diagnosis-driven decision, not a founder confession. The teardown is the evidence; the prescription is the plan; the ask is the runway and the expectation-reset on next quarter's numbers. Board members who see the teardown and the plan are usually supportive; boards that hear "we're pivoting" without the diagnosis are alarmed.
- **The customers.** The subset directly affected — customers on a pack that is being replaced, customers whose sales rep is changing, customers whose contract terms shift — are communicated proactively with the migration story (mod-106 Chapter 5's grandfathering discipline is the template). Silence here produces churn that a five-minute email would have prevented.
- **The market.** The pricing page changes; the positioning may shift; the pitch deck for prospects gets updated. Communicating the new pack is a mod-103 / mod-106 topic; the motion pivot has to be reflected in every public-facing surface the vendor owns.

The mistake founders make is under-communicating on the team-facing and customer-facing tracks and over-communicating on the board-facing and market-facing tracks — the audiences that need direct clarity get vague reassurance while the audiences that mostly need to know are being briefed in detail. A working pivot is over-communicated to the team and to affected customers, and briefly-communicated (with the diagnosis) to the board and the market.

### The founder-cost of a mismatch left un-diagnosed

The final case for the teardown: **an un-diagnosed mismatch is one of the most expensive errors a seed-through-Series-B startup can make.** The direct costs are visible — SDR / AE salaries burned for a year on a motion that never produced pipeline, tooling contracts signed and unused, VP Sales hire at $400K OTE that never had a defined motion to lead. The indirect costs are larger — the runway consumed on the wrong motion is runway not spent on the right one; the founder's attention consumed on tuning the wrong motion is attention not spent on the ICP / positioning / pricing work that would have exposed the mismatch earlier; the market position lost to a competitor who ran the right motion in the same window is often unrecoverable.

The teardown itself is cheap — one week of founder time, run against the artifacts Chapters 1-5 already produce. The cost of not running it, quarterly at seed and monthly at Series A, compounds fast.

## Concrete example — Loomly re-runs the teardown at Series A

Loomly's original Chapter 1 motion decision was SDR-AE-primary with a PLG top-of-funnel layer (Loomly Chapter 1 example). By Series A the company is at $4M ARR across 220 mid-market customers averaging $18K ACV; the enterprise tier (Chapter 4 example) has closed 3 large accounts averaging $280K ACV. The board asks: is the motion still fitting?

**Step 1 — Locate on the matrix.** Primary motion (SDR-AE for mid-market) is still fitting — the $18K ACV lives comfortably in the mid-market band; the 50-150-engineer ICP has not drifted (mod-104 Chapter 7 audit clean). PLG layer is producing 40% of new-logo pipeline via PQL alerts; sales-assist conversion is 32%. Enterprise layer at $280K ACV is a new addition and has closed 3 deals in 9 months. No obvious motion-mismatch signal at Step 1.

**Step 2 — Read the CRM signals.** The mid-market SDR-AE motion is running clean — SDR at 42 booked meetings/month against target 35-45; hand-off-accepted at 71% (healthy zone 60-80%); AE close rate 34% on qualified opportunities (mid-market benchmark 25-40%); MRR growth 12% MoM. The enterprise motion is running clean on the three closed deals but the pipeline is thin — 5 open enterprise opportunities across 3 AEs, versus a healthy 3-4× pipeline coverage that would require ~15 opportunities open. PLG layer is producing PQL alerts at expected rate; upgrade-prompt conversion on the self-serve tier is at 4.2% (in the OpenView 3-5% band).

**Step 3 — Symptom family scoring.**

- Family A (unit-economic): mid-market CAC payback 9.5 months (healthy vs. ≤ 12 benchmark); enterprise CAC payback modelling is 22 months on the 3 closed deals (within the ≤ 24 enterprise benchmark but at the edge). Blended margins healthy.
- Family B (funnel-shape): mid-market funnel clean at every stage. Enterprise pipeline is thin at the top of funnel — only 5 opportunities open across 3 AEs, and the SDR is not prospecting enterprise-fit accounts specifically. Enterprise-stage conversion rates are inconclusive with only 3 closed deals to compute against.
- Family C (team-and-narrative): sales team stable, one AE promotion pending. Enterprise deals so far have come inbound from expansion of the parent-company deal (Chapter 4 example) rather than from proactive outbound. Founder is spending 6-8 hours/week on the enterprise motion (mostly executive-sponsor time on the open deals); this is manageable but not sustainable if the enterprise pipeline grows.

**Step 4 — Match to canonical mismatches.**

- Mismatch 1 (enterprise ceremony on self-serve): does not fit. Product is not self-serve at enterprise scale; the ceremony is appropriate to the ACV.
- Mismatch 2 (self-serve on $100K contract): partial fit — the enterprise motion exists but its pipeline is thin because the top-of-funnel for enterprise deals is not designed. The SDR is prospecting mid-market accounts; enterprise-fit accounts (500+ engineers, formal procurement) are not on the target-account list. Enterprise deals to date have been reactive-inbound, not proactive-outbound.
- Mismatch 3 (SDR-AE on bottoms-up developer product): does not fit. Loomly's ICP is a manageable-VP-Eng-driven purchase, not a bottoms-up individual-developer purchase.
- Mismatch 4 (sub-scale CAC): does not fit at the primary motion; enterprise motion is at the payback edge but not below the benchmark.

Diagnosis: **partial Mismatch 2 on the enterprise layer only** — the enterprise motion is running the right MEDDPICC discipline on the deals it has, but the top-of-funnel that would generate a defensible pipeline of enterprise opportunities does not yet exist. Not a strategic mismatch on the primary motion; a build-out gap on the second layer.

**Step 5 — Prescription and sequencing.**

- Primary motion: no change. Continue SDR-AE for mid-market at current cadence; continue PLG layer at current instrumentation.
- Enterprise layer: build the enterprise top-of-funnel. Hire a dedicated enterprise SDR (or promote from within) with a 50-account target list of Fortune-500-and-adjacent accounts on the ICP. Cadence design: Level-3 personalisation, 12-14 touches over 6 weeks (longer cadence than mid-market for enterprise buyers). Target: 5-8 enterprise-qualified opportunities added per quarter, growing to 15 open in the enterprise pipeline over 12 months. Hire the first SE at month 12 (as originally planned per Chapter 4 example).
- Founder-cost: schedule the next teardown for Q4 (quarterly cadence at Series A per this chapter's discipline); watch specifically for enterprise CAC payback drift as the pipeline scales.

**Post-teardown communication.**

- Team: Monday all-hands announces the enterprise-SDR hire and the top-of-funnel investment; frames it as continuing the mid-market motion + investing in enterprise, not pivoting away from anything.
- Board: teardown memo included in the next board update as an appendix; boards value the discipline of the teardown as much as the specific diagnosis.
- Customers: no customer-facing communication needed; the change is upstream of any customer touch.
- Market: no market-facing communication needed; the pricing pack and positioning do not change.

The teardown took one week of founder time. The output — hire an enterprise SDR, invest in enterprise top-of-funnel, preserve the primary motion — is a decision the founder could have arrived at without the teardown, but the teardown is what produces the *defensible* version of that decision. When the enterprise pipeline is thin two quarters from now the founder will not be tempted to over-react ("the enterprise motion isn't working"); the teardown will already have named the top-of-funnel build-out as the load-bearing intervention.

## Common failure patterns

- **Reach-for-in-motion-levers-first trap.** Symptoms cluster across two families; founder reaches for hiring / tooling / coaching before running the teardown. Six months of in-motion tuning wasted. Fix: run the teardown at the first cross-family symptom cluster; two-consecutive-quarter rule for escalation from in-motion to mismatch.
- **Motion-loyalty trap.** Founder has publicly committed to a motion (in a fundraise deck, a podcast, a Twitter thread) and cannot bring herself to name the mismatch. Fix: separate the teardown from the ego cost; the teardown is done in a working session with a small team, and the decision is made on the artifacts, not on the founder's public commitments.
- **Fashion-of-the-moment pivot trap.** Founder reads a Kyle Poyar piece on PLG or a McMahon piece on enterprise and pivots the motion to whatever is currently in the practitioner conversation. The new motion also fails because it wasn't chosen from the ICP + ACV derivation. Fix: teardown produces the diagnosis; the diagnosis produces the motion, not the fashion.
- **Half-pivot trap.** Founder announces the pivot but leaves the old motion running "just in case." Team is confused about which motion is primary; the new motion is under-invested; the old motion continues consuming budget. Fix: sequencing discipline — kill the old motion on a defined date after the new motion has demonstrated pipeline; do not run both indefinitely.
- **Under-communicated pivot trap.** Founder briefs the board in detail and forgets to tell the sales team; three AEs quit within a month. Fix: the team-facing communication is the load-bearing one; over-communicate to the team, briefly to the board.
- **Whipsaw trap.** Founder pivots the motion, then two months later the numbers haven't recovered yet, so she pivots again to something else. Each pivot has 60-90 days of setup cost before it produces signal; multiple back-to-back pivots produce no signal at all. Fix: commit to the pivot for at least 2 full quarters before re-evaluating; if the diagnosis was sound, the numbers will move by then.
- **CRM-not-ready-for-teardown trap.** Team tries to run the teardown but the CRM has not been run with Chapter 5's stage-artifact discipline; the pipeline data is un-diagnosable. Founder guesses at the mismatch without evidence. Fix: Chapter 5 first (a week of CRM clean-up), then the teardown (a week of diagnosis), then the prescription.
- **Blame-the-team trap.** Founder concludes "our AEs aren't good enough" or "the SDR is under-performing"; fires the sales team and hires new reps against the same motion. Same numbers repeat. Fix: teardown before firing; the team is usually not the problem when the motion is the problem.
- **One-big-logo-again trap.** A single large enterprise deal reappears mid-teardown; founder abandons the diagnosis and re-pivots toward enterprise because "if we can close this one, we're an enterprise company." One deal is not a motion; treat it as bespoke and continue the teardown-driven prescription.
- **Ignore-Family-C trap.** Founder tracks Family A and B rigorously but dismisses Family C symptoms as "morale issues, not GTM issues." Family C is often the earliest signal — the buyer's language, the AE's confusion, the champion's silence — and dismissing it wastes the leading indicator. Fix: score all three families every teardown.
- **Never-schedule-the-teardown trap.** Founder runs the teardown once, produces a diagnosis, then never re-runs it. Six months later a new mismatch develops (ICP drift per mod-104 Chapter 7; pricing pack changes per mod-106 Chapter 5 that shift the ACV band) and goes un-diagnosed. Fix: teardown on a quarterly cadence at seed, monthly at Series A, and any time a Family A or C signal changes materially.
- **Pivot-without-pack-change trap.** Founder pivots the motion but leaves the pricing pack untouched; the new motion runs against a pack that does not support it (a per-seat pack for an enterprise motion; a per-outcome pack for PLG). The new motion fails for pricing reasons that look like new-motion failure. Fix: pack change and motion change are joint decisions (mod-106 Chapter 6 develops the pack change; this chapter's prescription always names the pack change alongside the motion change).

## Summary

- The mismatch-vs-execution differential is the highest-leverage diagnostic in early-stage GTM. Getting it wrong costs quarters; getting it right takes one week of founder time.
- The **four canonical mismatches**: (1) **enterprise ceremony on a self-serve product**, (2) **self-serve on a $100K contract**, (3) **mid-market SDR-AE on a bottoms-up developer product**, (4) **sub-scale CAC / payback on any motion**. Every observed mismatch in practitioner writing maps to some combination of the four.
- The **three symptom families**: (A) **unit-economic** (CAC / payback / margin), (B) **funnel-shape** (conversion at named stage boundaries), (C) **team-and-narrative** (buyer language, sales-team confusion, investor hedging). A mismatch usually surfaces across at least two families; a single-family symptom is often an in-motion problem.
- The **five-step teardown**: (1) locate on the Chapter 1 matrix, (2) read the Chapter 5 CRM signals honestly, (3) score the symptom family cluster quantitatively, (4) match to a canonical mismatch or rule them out, (5) prescribe the fix and the sequencing.
- The **differential rule**: in-motion execution problem if single-family + one leaking stage + one specific change is the root cause; motion mismatch if cross-family + multiple leaking stages + no in-motion knob has moved the numbers over 2+ quarters. **Escalate to a mismatch teardown after two consecutive quarters of in-motion fixes that do not move the numbers.**
- Prescriptions are **motion + pack + roles + sequencing**, not motion alone. A pivot without a matching pricing-pack change (mod-106) usually fails for pack reasons; a pivot without a role reallocation ends up under-invested.
- **Compound mismatches** — usually 1+4, 2+4, or 3+2 — are diagnosed by naming each mismatch and sequencing the fixes. Simultaneous pivots produce whipsaw; sequenced pivots produce compounding.
- The **four-audience communication** — team (over-communicate, blame-free), board (diagnosis + plan, briefly), customers (only the affected subset, with migration story), market (only the surfaces that need to change) — is what makes a pivot land instead of alienate.
- The **founder-cost of an un-diagnosed mismatch** compounds fast — direct costs (salaries + tooling + wrong-hires) plus indirect costs (runway on the wrong motion, attention off the ICP / pricing work, competitive position lost). The teardown itself is cheap; the alternative is expensive.
- The teardown runs on a **cadence** — quarterly at seed, monthly at Series A, and any time a Family A or C signal changes materially. It is a *reading practice* against the artifacts Chapters 1-5 already produce; it does not require new instrumentation.
- The **six chapters together** — motion matrix (1), PLG design (2), SDR-AE design (3), enterprise MEDDPICC design (4), CRM with stage-artifacts (5), mismatch diagnosis (6) — form the operating loop for early-stage GTM motion design. The exercises in this module drill each of them; the module lab in `.aicg/curriculum-plan.json` assembles them into a working motion pack for one startup.
