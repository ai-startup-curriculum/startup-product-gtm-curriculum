# ICP-Fit, ACV-Fit, Timing-Fit — Three-Axis Lead Scoring on Real Prospects

## Motivation

Chapters 1-4 built the ICP as a scoreable artifact: firmographic + behavioural criteria, disqualification checklist, buyer / user / champion personas. This chapter is where the artifact meets a real inbound or outbound lead, and where the founder's tacit habit of "score every lead against a single 'is this a good lead' vibe" gets replaced with a disciplined three-axis read.

The failure mode this chapter exists to catch: **the AE looks at a lead, forms an overall impression ("solid," "meh," "hot"), routes it accordingly, and cannot articulate why one solid-feeling lead closed in three weeks while another solid-feeling lead died at proposal after nine.** The two leads scored the same on the vibe axis; they were completely different on the three axes that actually predict outcome. The AE was integrating three signals into one number and losing the discriminating power of each.

The three axes are **ICP-fit** (does the company match the ICP scorecard?), **ACV-fit** (can the company pay at the price point the sales motion targets?), and **timing-fit** (is *now* the moment they will buy?). All three are load-bearing; missing any one produces a specific failure mode; scoring them independently produces a routing decision that separates deals-to-work-hard-now, deals-to-work-slow, deals-to-nurture, and deals-to-close-lost — with the AE's time deliberately allocated across the four.

This chapter names each axis, the specific questions to score it, the six routing combinations that come out of the three-axis matrix, and the operational discipline that keeps the axes from collapsing back into a single vibe score.

## Core concepts

### Axis 1 — ICP-fit (the Chapter 1-4 scorecard applied)

ICP-fit is the score the Chapter 2 firmographic + behavioural scorecard produces when applied to a specific lead. It answers: **does this company match the profile of the customers we can win with the current product at the current motion?**

Scoring: use the weighted rubric from Chapter 2. The output is a single 0-100 percentage plus a must-have-check.

The band-splits from Chapter 2 apply here directly:

- **Strong ICP-fit (≥ 80% of max, zero disqualifier misses):** the company matches the ideal profile the AE was hired to close. Firmographic and behavioural criteria align; no disqualifiers fired.
- **Moderate ICP-fit (50-80%, zero disqualifier misses):** the company is a plausible fit with a specific gap named. The AE proceeds with the gap as a known risk (e.g., "great fit but they deploy monthly instead of weekly, so the urgency framing needs to bridge the gap").
- **Weak / Out ICP-fit (< 50%, or any disqualifier miss):** the company is not a fit today. Chapter 3's disqualifier discipline routes this to close-lost with a reason code and (if applicable) an unlock condition.

ICP-fit alone is insufficient. A strong-ICP-fit lead can fail on ACV-fit (they match the profile but cannot pay the price) or on timing-fit (they match the profile but are not in the market right now). Both are legitimate close-lost verdicts even for a "perfect" ICP-fit lead.

### Axis 2 — ACV-fit (can they pay at the target price?)

ACV-fit answers: **can the company pay at the ACV the sales motion targets, given their buying-motion posture and budget authority?**

The failure mode this axis catches: **the lead matches the ICP but the price point sits above their departmental budget authority, below the ceiling that would trigger a formal procurement / RFP process, or in a weird zone that requires unusual approval sequences.** The AE spends a full cycle on a deal that closes at a heavy discount or drags through a nine-week procurement process because ACV-fit was not scored explicitly.

Scoring: three sub-questions produce the ACV-fit read.

1. **Is the buyer authorised to spend at your target ACV without escalation?** If the target ACV is $30k and the buyer's departmental authority is $10k, the deal requires escalation to a higher approver — extending the cycle and introducing a new persona to sell to. This is not a disqualifier by itself, but it is a strong signal the cycle will be 2× as long and the deal-close probability lower.
2. **Is there budget line-item allocated to your category this year?** A budget-authorised buyer with no allocated line-item for your category has to *create* budget — either steal from another line or wait for the next budget cycle. This significantly extends the cycle and reduces close probability.
3. **Does your ACV fall in the "avoid the RFP threshold" band?** Many companies have specific thresholds — $25k, $50k, $100k — above which a formal RFP or procurement-team review is triggered. An ACV just above the threshold is worse than the same ACV in either direction (either lower, avoiding the RFP, or higher, justifying the RFP with a full enterprise-motion resource commitment).

ACV-fit output: **strong** (all three sub-questions yes), **moderate** (two of three yes), **weak** (one or zero yes, or a specific "structural mismatch" flag). A weak ACV-fit is usually a close-lost even for a strong ICP-fit lead — the price is simply outside their buying posture.

The AE-actionable version: **before spending more than 20 minutes on any prospect, the AE should be able to answer: "does this buyer have the authority to sign a $Ntk contract without additional approvals?"** If no, the AE re-scopes the conversation to reach the higher approver (turning the current contact into a champion, per Chapter 4) or downgrades the deal-priority ranking.

### Axis 3 — timing-fit (is *now* the moment?)

Timing-fit answers: **is the company in a buying moment where the purchase is likely to close this quarter, or is the interest genuine but timing distant?**

The failure mode this axis catches: **the lead is a great ICP-fit and has budget, but is 6-9 months away from actually buying, and the AE spends the current quarter's hours on a deal that closes (if at all) in a future quarter.** The AE is working the deal at the wrong time.

Scoring: five timing-fit signals, each yes / no.

1. **A recent triggering event.** A new VP Eng joined; a funding round closed; a competitor's product was deprecated; the company hit a specific milestone that made the pain acute. Triggering events are the strongest single timing signal.
2. **A named budget cycle or approval window.** "We're finalising the H2 budget in four weeks" is a specific timing anchor. "We have general interest in solving this" is not.
3. **The buyer has an explicit deadline or KPI tied to the outcome.** "The VP has a Q3 goal to reduce cycle time" gives the deal a specific close-by date. "The VP thinks throughput is important" does not.
4. **The pain has become newly visible.** A recent incident, a board question, an audit finding, a churn event — something that made the previously-latent pain newly salient. New pain closes faster than tolerated pain.
5. **An active evaluation is underway.** The buyer is comparing options, has a shortlist, has scheduled demos with vendors. This is late-stage timing — the deal will close (with someone) in the next quarter; the AE is racing to be that someone.

Timing-fit output: **hot** (three or more signals present), **warm** (one or two signals), **cold** (zero signals, general interest only).

Cold timing-fit is not a disqualifier — the lead may become hot next quarter — but it is a routing signal. Cold leads go to nurture (Chapter 6-adjacent territory), not to the AE's active-work queue.

### The three-axis matrix — six routing verdicts

Combining the three axes produces a routing matrix. The three axes each have three bands (strong / moderate / weak-or-cold), so the full matrix has 27 cells; the operational compression is into **six routing verdicts** the AE can act on directly:

| ICP-fit | ACV-fit | Timing-fit | Verdict | AE action |
|---|---|---|---|---|
| Strong | Strong | Hot | **Priority 1 — work now, hard** | Full cycle, weekly progress, aim for close this quarter |
| Strong | Strong | Warm | **Priority 2 — work now, patient** | Full cycle, monthly cadence, aim for close next quarter |
| Strong | Strong | Cold | **Nurture — high-priority long-cycle** | Marketing nurture, quarterly personal touch, watch for triggering event |
| Strong | Weak | Any | **Downgrade or refer** | Downgrade to lower ACV product tier if available; refer to peer / partner otherwise; do not run full cycle |
| Moderate | Strong | Hot | **Priority 2 — work now, patient** | Full cycle, name the ICP gap as a known risk, cycle length may be longer |
| Any | Any | Any (with disqualifier) | **Close-lost with reason code** | End cycle at discovery, close-lost with the specific disqualifier |

Two observations. First: the "Priority 1" cell — the AE's most valuable hours — is the intersection of strong on all three axes. That cell is usually small; typically 5-15% of the AE's total lead volume. The whole point of scoring the axes explicitly is to make sure the AE's Priority 1 hours are spent in the Priority 1 cell, not diffused across everything.

Second: the "Downgrade or refer" cell exists because the founder's instinct is to work a strong-ICP-fit lead even at weak ACV — "we can help them, let's find a way." At SEED the "way" is usually a discount that breaks the pricing anchor, a custom contract that consumes founder-hours, or a compromise motion that dilutes the beachhead commitment. The refer / partner / downgrade path preserves the ICP integrity while still serving the buyer.

### Separating the three axes prevents the "seemed like a good lead" trap

The reason the three-axis discipline matters is that founders and inexperienced AEs *integrate* the axes into a single vibe score and lose the discriminating power of each.

Consider two prospects, both "solid":

- **Prospect A**: mid-market B2B SaaS devtools company, 100 engineers, using GitHub, engineering leader has a throughput metric. ICP-fit strong. Budget: departmental authority up to $50k; our ACV is $12k. ACV-fit strong. Timing: no specific event; VP is "generally interested"; no budget cycle in the next 6 months. Timing-fit cold.
- **Prospect B**: same firmographic profile. Same behavioural profile. ICP-fit strong. Budget: departmental authority is $8k; our ACV is $12k, requires CFO co-sign. ACV-fit moderate. Timing: VP joined 8 weeks ago, has a 90-day plan to demonstrate a productivity win. Timing-fit hot.

To a "vibe" scorer, both feel like solid leads and the AE splits hours across them. To the three-axis scorer, Prospect A is a *nurture* (great fit, no urgency) and Prospect B is a *Priority 2 with an ACV-fit caveat* (right timing, will require CFO conversation). Different treatments, different weekly hours, dramatically different close-rate outcomes.

The three-axis discipline is what makes this discrimination visible. Chapter 7's shipping-artifact section on lead scoring bakes this discipline into the artifact.

### Inbound vs outbound — the axes score differently on each

The three-axis framework applies to both inbound and outbound leads, but the *default* scores differ, and confusing the two produces bad prioritisation.

**Inbound leads** — the prospect came to you, via marketing content, a product-hunt launch, a referral, or a direct request-a-demo. Default properties:

- **ICP-fit varies wildly.** Inbound is unqualified at the top of the funnel; some percentage of inbound is deeply out-of-ICP (wrong industry, wrong size, wrong stage). The ICP-fit scoring is the first filter; a significant fraction of inbound is a fast close-lost against ICP.
- **Timing-fit is usually warm-to-hot.** People do not fill in a demo request for something they might buy in 2028. Inbound self-selects for at-least-warm timing.
- **ACV-fit varies.** No prior knowledge of the buyer's budget posture; the AE has to surface it in the first call.

The inbound routing bias: **inbound is filtered hard on ICP-fit and ACV-fit; the timing signal is already usable.** A large fraction of inbound (30-50% is common at SEED) close-loses against ICP-fit in the first-call verdict.

**Outbound leads** — the AE / SDR sourced the account and reached out cold. Default properties:

- **ICP-fit is high by construction** — the list was built from the ICP's Layer 1 firmographic criteria, so unless the list-builder was sloppy, most outbound leads are at least moderate ICP-fit.
- **Timing-fit is usually cold.** The prospect did not raise their hand; the AE is interrupting. The default state is "not thinking about this right now."
- **ACV-fit varies but tends to be moderate-to-strong** because the outbound list was targeted to match the target ACV.

The outbound routing bias: **outbound is filtered hard on timing-fit; the ICP and ACV are usually usable.** The AE's job on outbound is not to sell but to identify or *create* a triggering event that shifts timing-fit from cold to warm.

Confusing the two — treating inbound like outbound (working every inbound as if timing was cold) or outbound like inbound (assuming outbound is at least warm) — miscalibrates the AE's effort per lead. Score the axes separately per channel.

### The five-inbound / five-outbound calibration exercise (see Exercise 03)

The operational calibration for a first AE hire: **score five real inbound and five real outbound leads against the three axes, produce a routing verdict for each, and compare against the founder's independent verdict.** Discrepancies are the training feedback loop.

The point of the exercise is not to prove the AE right or the founder right — it is to surface where the ICP artifact is ambiguous, where the discovery questions do not resolve the ambiguity, and where the AE and founder are collapsing axes differently. Exercise 03 develops this drill in full.

### The routing must be operationally enforced

The most common failure of a three-axis system: the AE scores the axes but does not actually route differently based on the score. Every deal ends up in the "work now" bucket regardless of score. The score is theatre.

The remedy is a hard cadence rule: **the AE's calendar time is allocated by verdict.** For example:

- **Priority 1 deals**: 60% of AE selling hours. Weekly progress required or the deal is downgraded.
- **Priority 2 deals**: 25% of AE selling hours. Monthly progress required or the deal moves to nurture.
- **Nurture deals**: 5% of AE selling hours. Quarterly personal touch. Marketing carries the rest.
- **Downgrade / refer**: 5% of AE selling hours. Explicit hand-off, then out of the AE's queue.
- **Close-lost**: 5% for the process of clean close-out and reason coding.

The specific percentages are illustrative; the discipline is that verdicts have specific time budgets. Without the time budget, every deal drifts back to "work now" and the three-axis discipline dissolves. Chapter 7's operating cadence section makes this explicit.

## Concrete example — Loomly scoring five inbound and five outbound

Applied to Loomly, with realistic scored leads. Each lead is a one-line synthesis; the exercise (Exercise 03) develops each into a full worksheet.

### Inbound (past 30 days)

| Lead | Company shape | ICP-fit | ACV-fit | Timing-fit | Verdict |
|---|---|---|---|---|---|
| I1 | 80-eng B2B SaaS devtools; GitHub; VP Eng requested demo after reading blog post; VP has "cycle time down 20%" as Q3 OKR | Strong (all criteria) | Strong ($15k in dept budget) | Hot (Q3 OKR + demo request) | **Priority 1** |
| I2 | 3-eng bootstrapped indie hacker; using GitHub; requested demo out of curiosity | Weak (headcount disqualifier) | N/A | N/A | **Close-lost** — outside ICP |
| I3 | 300-eng healthcare software company; GitLab-based; asked about GitLab support in demo request | Weak (GitLab disqualifier D1) | N/A | N/A | **Close-lost** — GitLab, unshipped |
| I4 | 120-eng B2B SaaS observability; GitHub; distributed; eng manager filled form but doesn't have a metric goal, "just curious" | Moderate (weak on B1 metric ownership) | Moderate (buyer authority unclear) | Cold (no trigger, "just curious") | **Nurture** |
| I5 | 60-eng B2B SaaS cybersecurity; GitHub; VP Eng and CTO on discovery call; recent security incident traced to slow PR reviews on security-patch branch | Strong | Strong | Hot (recent incident + CTO on call) | **Priority 1** |

Two Priority 1s, one Nurture, two Close-losts. Of five inbound leads, the AE's active-work list is two; the other three route to lower-effort channels. Without the three-axis discipline, an AE would run four or five full cycles and close roughly the same number of deals in more hours.

### Outbound (targeted list, past 30 days)

| Lead | Company shape | ICP-fit | ACV-fit | Timing-fit | Verdict |
|---|---|---|---|---|---|
| O1 | 110-eng B2B SaaS devtools; GitHub; distributed; recent VP Eng hire (LinkedIn) | Strong | Strong | Hot (new VP Eng — 90-day plan window) | **Priority 1** |
| O2 | 90-eng B2B SaaS observability; GitHub; hybrid; no visible trigger | Strong | Strong | Cold (no trigger) | **Priority 2 warm-up** — outbound nurture, watch for trigger |
| O3 | 140-eng fintech; GitHub; distributed; but fintech is outside beachhead | Weak (beachhead disqualifier D4) | N/A | N/A | **Close-lost** — outside beachhead; refer to Fintech waitlist |
| O4 | 200-eng B2B SaaS devtools; GitHub; distributed; recent funding round; hiring 30+ engineers per LinkedIn | Strong | Strong | Warm (funding + hiring surge → likely productivity investment) | **Priority 2** |
| O5 | 100-eng B2B SaaS devtools; GitHub; but heavily gated procurement per public case study | Moderate (fires anti-signal on procurement) | Weak (procurement > 60 days) | Warm | **Priority 2 with ACV-fit caveat** — expect long cycle |

One Priority 1, three Priority 2s with different caveats, one Close-lost. Outbound skews toward Priority 2 with cold-to-warm timing; the AE's job is to convert warm to hot via a triggering-event conversation.

### The pattern the AE should notice

Across the ten leads:

- Two are Priority 1 (both had explicit triggering events — Q3 OKR, recent security incident, new VP Eng).
- Four are Priority 2 (mostly outbound; the AE's job is to create urgency).
- One is Nurture.
- Three are Close-lost (all against named disqualifiers).

Of the AE's 40 selling hours in a week, roughly 24 go to Priority 1 (two deals), 10 go to Priority 2 (four deals), and the remainder to nurture + close-out. Without the three-axis routing, the AE would spread 40 hours over 7 deals evenly, close roughly the same number, and have no basis for improving the ratio next quarter.

## Common failure patterns

- **Single "vibe" score instead of three axes.** The AE integrates the signals into "feels solid / feels weak" and loses the discriminating power of each axis. Score all three, always, independently.
- **ICP-fit only.** Every ICP-fit lead is worked at full effort regardless of ACV or timing. Result: quarters absorbed by great-fit-wrong-time deals.
- **Timing-fit only ("this is hot, don't scrutinise it").** A hot lead is not necessarily an ICP-fit lead. Hot-out-of-ICP is one of the fastest ways for an AE to close a deal that never renews (mod-109 churn territory).
- **ACV-fit as a soft signal.** "They can probably find the budget" is not an ACV-fit read. The three specific sub-questions — authority, allocation, RFP-band — need explicit answers.
- **Nurture bucket is a graveyard.** Deals routed to "nurture" are forgotten; there is no cadence, no triggering-event monitor, no re-scoring. Nurture is a real operating mode with a real cadence, not a euphemism for "we gave up."
- **Downgrade / refer path missing.** The AE has no lower-tier product to downsell to and no partner to refer to, so every out-of-fit deal either closes at a discount or is worked to close-lost after full effort. Build the downgrade path deliberately (mod-106 pricing tier work; mod-108 partner referrals).
- **Routing verdict not enforced with calendar time.** The AE scores the axes and then works every deal the same amount. Without a specific hours-per-verdict budget, the score does nothing.
- **Inbound and outbound scored the same way.** Inbound self-selects for warm-to-hot timing; outbound self-selects for cold. Same three axes, different default expectations.
- **AE not authorised to close-lost against a routing verdict.** Every close-lost gets re-litigated; the AE stops routing to close-lost. Explicit AE authorisation to close against a named routing verdict is required (same discipline as Chapter 3's disqualifier authorisation).
- **Founder overriding routing verdicts on gut feel.** The founder sees an "interesting" lead in the close-lost bucket and re-opens it. Occasionally right, usually wrong; more corrosive than the individual deal because it teaches the AE that the routing is advisory, not binding.

## Summary

- Every lead — inbound or outbound — is scored on **three independent axes**: ICP-fit (Chapter 2 scorecard), ACV-fit (buying authority + budget allocation + RFP threshold), timing-fit (triggering event + budget window + explicit deadline + newly-visible pain + active evaluation).
- Each axis has **three bands**: strong / moderate / weak-or-cold. Combining across axes produces **six operational routing verdicts**: Priority 1, Priority 2, Nurture, Downgrade / Refer, Close-lost, with an "active evaluation" catch-all for late-stage inbound.
- **Inbound self-selects for warm-to-hot timing** but not ICP or ACV; the ICP-fit filter is the primary inbound work.
- **Outbound self-selects for high ICP-fit** (by list construction) but cold timing; the AE's job on outbound is to identify or create a triggering event.
- The **Priority 1 cell — strong on all three axes — is small** (typically 5-15% of lead volume). The whole discipline exists to make sure the AE's most valuable hours are spent there, not diffused across everything.
- The **routing must be enforced with calendar time**: hours-per-verdict budgets, weekly / monthly / quarterly cadences per verdict. Without the time budget the routing is theatre.
- **Scoring the axes independently prevents the "seemed like a good lead" trap** — the AE loses the ability to explain why one solid-feeling lead closed and another died late, and the founder loses the ability to coach the AE toward better prioritisation.
- Chapter 6 develops the **beachhead-narrowed commitment** — how the ICP explicitly says-no to three segments to protect the one segment it says yes to — the discipline that keeps the three-axis routing from re-drifting into serve-everyone territory.
