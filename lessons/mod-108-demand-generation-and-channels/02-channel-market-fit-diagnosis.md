# Channel-Market Fit — the Diagnosis Before Scaling

## Motivation

A channel that produces leads is not necessarily a channel that produces revenue. A channel that produces revenue is not necessarily a channel that produces revenue *at a defensible cost*. And a channel that produces revenue at a defensible cost this quarter is not necessarily a channel that produces revenue at a defensible cost when the founder scales the spend or hires a second SDR against it. Every scaling step reveals a different failure mode; every failure mode looks superficially like success at the previous step.

The failure mode this chapter exists to catch: **the founder observes lead volume from a channel, concludes "the channel is working", scales spend or headcount into it, and discovers three quarters later that the leads were ICP-adjacent but not ICP-fit — the pipeline moved through the funnel but the close rate was 3× worse than the founder-led channel, the CAC blew past the payback benchmark, retention on the acquired customers was 40% worse than on organically-acquired ones, and the runway is now short by the amount of the mis-invested scale.** Every one of those failures was diagnosable months earlier — but the founder was reading lead volume instead of channel-market fit.

Balfour's four-fit framework (Chapter 1) names the diagnosis: a channel has to be **market-channel fit** (the target market is reachable at this channel at all, at ICP-fit quality) **and channel-model fit** (the CAC curve at this channel is compatible with the LTV / payback curve the pricing model supports). Both fits have to hold; either one failing kills the channel. Reading only one of them — usually the market-channel side, because leads are visible and CAC is not — is what produces the mis-scaling failure.

This chapter builds the diagnosis as a set of four gates the primary channel has to pass before spend or headcount scales into it. Each gate is a testable, numeric criterion — not a vibe. The gates are: **(1) ICP-fit lead quality**, **(2) unit-economic viability (CAC / LTV / payback)**, **(3) time-to-signal maturity**, and **(4) attribution honesty**. A channel that passes all four is scaled deliberately; a channel that fails one is fixed at that gate before spend increases; a channel that fails two or more is a candidate for demotion to the "not now" list and replacement by the experimental channel (Chapter 1) or a new candidate. This diagnosis is what turns "we're doing outbound / content / paid / community" from a slogan into a testable claim.

## Core concepts

### The four gates — an overview

Every candidate primary channel has to clear four sequential gates before scale spend or scale hiring commits against it. The gates are sequential in the sense that failing an earlier gate makes the later gates meaningless — an ICP-fit-failing channel has no useful CAC number, because the CAC is computed against the wrong denominator.

| # | Gate | Question | Fails if |
|---|---|---|---|
| 1 | **ICP-fit** | Are the leads from this channel the same shape as the ICP the founder-led motion has been closing? | Lead-to-opportunity conversion is <50% of founder-led-channel benchmark, or closed-won accounts are firmographic outliers |
| 2 | **Unit economics** | Does the channel's CAC survive the LTV / payback envelope? | Fully-loaded CAC > payback ceiling; CAC : LTV ratio worse than 1:3; payback longer than 18-24 months |
| 3 | **Time-to-signal** | Has the channel run long enough for its natural window to have opened? | Channel is <50% into its time-to-signal window; sample size (opportunities / closed deals) is too small for the CAC calculation to be meaningful |
| 4 | **Attribution honesty** | Do we actually know the channel produced the deal — or are we crediting last-touch to something we can measure while first-touch was somewhere else? | Attribution is single-touch on a multi-touch buyer journey; UTM discipline is inconsistent; self-reported source data is not collected |

The order is deliberate. **ICP-fit first** because a channel producing wrong-fit leads corrupts every downstream metric. **Unit economics second** because a channel producing ICP-fit leads at unaffordable CAC is a channel that will kill the company at scale. **Time-to-signal third** because the CAC number is only meaningful once the window has opened and the denominator is real. **Attribution last** because attribution errors show up as anomalies at the earlier gates — you notice them when the numbers stop making sense.

### Gate 1 — ICP-fit lead quality

The single most-common way a channel appears to work and then does not: it produces **volume** but not **ICP-fit volume**. Content marketing at a low-quality topic (mod-108 Chapter 3 develops this) attracts developers who are curious but have no buying authority; paid search on high-volume adjacent keywords attracts students, competitors, and job-seekers; community-driven top-of-funnel attracts open-source enthusiasts who will never pay for the commercial tier. Each of these produces demo requests, sign-ups, or dashboard-visible lead counts — and none of them converts into pipeline.

The ICP-fit gate has three sub-tests.

**Sub-test 1A — firmographic match.** For every closed-won deal, does the account match the mod-104 ICP scorecard? Score against the same criteria the founder-led motion used. The healthy target: **>80% of closed-won accounts are Layer-1 ICP-fit** (firmographic tier — company size, industry, geography); **>60% are Layer-2 ICP-fit** (behavioural tier — the buyer / user / champion behaviour pattern). A channel producing 30% Layer-1 ICP-fit is not a working channel; it is an ICP-adjacent channel that will burn resources on non-repeatable deals.

**Sub-test 1B — conversion parity.** The channel's lead-to-opportunity and opportunity-to-close rates should be comparable to (not necessarily identical to, but within a factor of ~2 of) the founder-led-channel benchmark. If founder-led outbound converts leads → opportunities at 40% and opportunities → close at 32%, a working primary channel should show 20-40% and 16-32%. A channel showing 5% lead → opportunity and 8% opportunity → close is producing wrong-fit leads that pipe through but do not close.

**Sub-test 1C — retention parity.** Once acquired customers reach the 90-day and 180-day marks, does their retention curve match organically-acquired customers'? Andrew Chen's canonical retention diagnostic (mod-109 Chapter 1) applies here — if the channel produces customers whose 90-day retention is 30% below the founder-led-channel cohort, the channel is producing acquire-and-churn customers whose LTV is much lower than the average LTV number would suggest.

Sub-tests 1A and 1B can be run at 4-8 weeks; sub-test 1C requires the first cohort to have reached 90-180 days, which is often 3-6 months into the channel. The gate is not "passed" until all three sub-tests are read; a channel that passes 1A and 1B but fails 1C is a channel that is producing the wrong customers at the right initial cost — and the CAC : LTV number will look fine until the churn hits.

### Gate 2 — unit economics (CAC / LTV / payback)

The unit-economic gate is the arithmetic on the channel: the fully-loaded acquisition cost per closed customer, the customer lifetime value, and the payback period. Full theoretical treatment lives in mod-110 (GTM Metrics and First Hires); this chapter uses the *operator subset* — the numbers a founder has to know at channel-level to make the scale-or-kill decision.

**Fully-loaded channel CAC.** The all-in cost to close one paying customer via the channel, over a defined period (usually a quarter or a rolling three-month window):

```
Channel CAC = (channel spend + fully-loaded people cost + tooling cost + attributable overhead)
              ─────────────────────────────────────────────────────────────────────────────
                                       closed-won accounts from the channel
```

The three components most founders under-count:

- **Fully-loaded people cost.** If Jane and the AE together spend 25 hours/week on outbound, at a blended $200/hour fully-loaded cost, that is $5,000/week or $65,000/quarter of people cost — regardless of whether the outbound tool is $500/month. Founders often report "CAC" as tooling + ad spend, ignoring the largest component.
- **Attributable overhead.** CRM, cadence tool, enrichment, video / demo tooling, meeting scheduling — the fixed tooling stack the channel requires. Amortise across the channels that use it; do not zero it just because it existed before the channel started.
- **Failed-channel cost.** If the last quarter was spent testing paid before pivoting to outbound, the paid test cost is retrospectively a discovery cost against the winning channel. Founders often exclude failed-experiment cost from CAC calculations — but the discovery cost was real and the runway spent is not recoverable.

Working benchmark ranges for fully-loaded CAC by motion + ACV band (calibrated against David Skok / OpenView / SaaStr / Bessemer practitioner data; working ranges, not laws):

| ACV band | Motion | Healthy CAC range | CAC / LTV target |
|---|---|---|---|
| $99-499/month self-serve | PLG / inbound-heavy | $200-800 | 1 : 3+ |
| $1K-10K/year low ACV | PLG + sales-assist | $800-3K | 1 : 3+ |
| $10K-30K/year low-mid | SDR-AE inside sales | $3K-9K | 1 : 3+ |
| $30K-100K/year mid-market | SDR-AE inside sales | $8K-25K | 1 : 3+ |
| $100K-500K/year enterprise | MEDDPICC named-account | $25K-100K+ | 1 : 3+ |

<!-- needs-research: pin these CAC benchmark ranges against current OpenView SaaS Benchmarks report, David Skok's SaaS metrics writing, or the current SaaStr benchmark posts; the ranges above are working defaults -->

**Customer LTV.** Cohort-based, not blended-ARR. The correct formulation for an operator-level LTV at the channel-diagnosis stage:

```
LTV ≈ ARPA × gross margin × 1 / (monthly churn rate)
```

Where **ARPA** = average revenue per account (usually the ACV), **gross margin** = revenue minus cost-of-goods (typically 70-85% for SaaS), **monthly churn** = the monthly logo-churn rate on the relevant cohort. mod-109 develops the retention-curve version that is more accurate but more expensive to compute; at the channel-diagnosis stage the formula above is a working proxy.

**Payback period.** Months of gross profit to recover fully-loaded CAC:

```
Payback (months) = CAC / (monthly ARPA × gross margin)
```

Modern practitioner benchmark: **payback < 12 months is healthy** for a mid-market SaaS motion; **payback 12-18 months is defensible** at ACV bands where the motion is heavier; **payback > 24 months is a red flag** at any band — either the CAC is too high or the ACV is too low; the pricing pack (mod-106) may need to move up-market before the channel scales further. Skok's *SaaS Metrics 2.0* article is the canonical writeup ([Skok — For Entrepreneurs](https://www.forentrepreneurs.com/saas-metrics-2/)).

**The CAC / LTV ratio.** The composite: **CAC : LTV of 1 : 3 or better** is the modern benchmark. A 1 : 3 ratio means the channel produces $3 of lifetime gross profit for every $1 spent to acquire; below that, the channel is unit-negative at scale. A 1 : 5 or better ratio is a channel that can be scaled aggressively; a 1 : 2 ratio is a channel that survives on paper but degrades to unit-negative under any adverse condition (churn spike, ACV compression, CAC inflation).

**Reading the gate.** A channel passes the unit-economic gate when:
- Fully-loaded CAC is inside the healthy range for its motion + ACV band.
- Payback period is <18 months.
- CAC : LTV ratio is 1 : 3 or better, and holding across at least two consecutive quarters.

A channel that passes on one quarter's numbers but the numbers were computed on 6 closed deals is failing sub-test 3 (time-to-signal), not passing gate 2 — the sample size is too small to trust.

### Gate 3 — time-to-signal maturity

Every channel has a natural window inside which its numbers become meaningful. Reading the numbers before the window has opened produces false positives (small-sample noise that reads as success) and false negatives (an under-invested channel that is actually working but has not had time to show it).

**The window is a function of the channel's operating cadence and the sales cycle it feeds.** For each channel:

| Channel | Time to first opportunity | Time to first closed deal | Time to defensible CAC calculation |
|---|---|---|---|
| Founder-led outbound (SDR-AE motion) | 2-4 weeks | 8-16 weeks | 4-6 months of consistent execution + ≥20 closed deals |
| Inbound / content + SEO | 8-16 weeks | 16-32 weeks | 6-12 months + ≥30 closed deals from ranked content |
| Community | 12-24 weeks | 24-52 weeks | 12-18 months + ≥20 closed deals from community-sourced accounts |
| Paid acquisition | 2-4 weeks | 6-12 weeks | 3-6 months of consistent spend + ≥50 closed deals |
| Partnerships / channel | 8-16 weeks | 16-32 weeks | 9-18 months + ≥10 closed deals from ≥3 distinct partners |
| Events / DevRel | 2-4 weeks | 12-24 weeks | 4-6 quarters + ≥15 closed deals from ≥3 distinct events |

<!-- needs-research: pin channel time-to-signal windows against practitioner references (Reforge, Balfour, First Round Review) rather than practitioner defaults -->

The gate is **read before scaling, not skipped**. Two anti-patterns show up:

- **Kill-before-window-opens.** Founder runs paid for 4 weeks, sees 8 conversions, computes a $2,400 CAC, panics because it is above target, kills the channel. The 4-week window was pre-mature — 4 weeks is 30% of paid's time-to-signal, the 8-conversion sample is well below the 50-conversion threshold for defensible CAC, and the CAC calculation was noise. The correct read is "the sample is too small; extend the test another 8 weeks or accept the null result".
- **Scale-before-window-opens.** Founder runs outbound for 4 weeks, sees 20 booked meetings, extrapolates "we're on track for 200 booked meetings per quarter, let's hire two more SDRs". The 4-week window was pre-mature — the reply rate on cold outbound decays past the first-warm-list effect, meetings booked at week 4 do not necessarily project to weeks 8-16, and the SDR-AE hand-off ratio (mod-107 Chapter 3) has not yet stabilised. The correct read is "let the first cadence complete; scale the SDR headcount after the second full cadence run confirms the numbers".

### Gate 4 — attribution honesty

Attribution at seed stage is bad. Buyers touch the product across multiple channels (a founder's tweet leads to a search for the company name leads to a Google Ads click leads to a signup; last-touch attribution credits the ad, first-touch attribution credits the tweet, both are technically true, neither is fully explanatory). If the founder is scaling spend on the channel that got last-touch credit, she is scaling the wrong thing.

Three attribution disciplines the gate looks for:

**Discipline 1 — self-reported source data collected on every sign-up and every demo booking.** A single field: *"how did you hear about us?"* — free-text, not a dropdown (dropdowns bias to whatever is at the top of the list). Founders often skip this because "the data is noisy"; it is noisy, but its signal-to-noise is better than pixel-based tracking for a small B2B funnel. The rule of thumb: **if 20-40% of self-reported source data disagrees with the tracked-attribution source, the tracked attribution is unreliable at the current sample size** — trust the self-reported side and use tracked as a secondary signal.

**Discipline 2 — first-touch and last-touch reported side-by-side, never blended.** Most CRMs (HubSpot, Salesforce with Bizible / Marketo, Attio) support both. Report both; look for the first-touch → last-touch pattern. A healthy inbound channel shows first-touch = channel and last-touch = branded search or direct traffic (the buyer discovered you via the channel and returned via brand-search); a healthy outbound channel shows first-touch = outreach email and last-touch = demo booking. If first and last are on wildly different channels, either the buyer journey is multi-channel (which is fine, and multi-touch attribution is the correct interpretation) or the pixel tracking is broken.

**Discipline 3 — UTM discipline on every outbound link, every content publication, every partner referral.** UTM parameters are simple and free; not tagging them means attribution is guessing. The four core parameters: `utm_source` (the channel, e.g. `linkedin`, `outbound_email`, `hn`), `utm_medium` (the format, e.g. `organic`, `paid`, `newsletter`), `utm_campaign` (the specific campaign or article), `utm_content` (the specific asset — link position, variant). The rule: **every link Loomly's team publishes has UTMs; every partner is issued a partner-specific UTM'd URL; every ad has its own UTM template**. Missing UTMs invalidate the attribution report for those links.

**The attribution honesty check** — pick a random sample of 10 closed-won deals from the previous quarter; for each one, reconstruct the buyer journey from first-touch to close using the CRM's attribution report + self-reported source data + email thread history. If more than 3 of the 10 have "we don't actually know" as the answer, the attribution stack is not yet mature enough to trust for scaling decisions.

### Reading the four gates together — the diagnostic dashboard

The gates are read as a single dashboard, weekly during the primary channel's ramp and monthly once it is stable. The dashboard has four sections; each has a green / amber / red status against numeric thresholds.

**Gate 1 — ICP-fit lead quality.**
- 1A Firmographic match: % of closed-won that pass Layer-1 ICP scorecard. Green ≥80%, amber 60-79%, red <60%.
- 1B Conversion parity: lead-to-opportunity rate as % of founder-led benchmark. Green ≥70%, amber 40-69%, red <40%.
- 1C Retention parity: 90-day retention delta vs. founder-led cohort. Green within 10pp, amber 10-25pp gap, red >25pp gap.

**Gate 2 — Unit economics.**
- Fully-loaded channel CAC vs. band benchmark. Green inside range, amber within 25% above range, red >25% above range.
- Payback period. Green <12 months, amber 12-18 months, red >18 months.
- CAC : LTV ratio. Green ≥1 : 3, amber 1 : 2 to 1 : 3, red <1 : 2.

**Gate 3 — Time-to-signal maturity.**
- % of time-to-signal window elapsed. Green ≥100%, amber 50-99%, red <50%.
- Sample size (closed-won accounts) against defensible-CAC threshold. Green ≥threshold, amber 50-100% of threshold, red <50%.

**Gate 4 — Attribution honesty.**
- Self-reported source data collection rate. Green ≥90% of sign-ups have a field filled, amber 60-89%, red <60%.
- Reconstruction accuracy on 10-deal sample. Green ≥8/10 reconstructible, amber 5-7, red ≤4.

**Reading the composite.** A channel is **ready to scale** when all four gates are green. A channel is **hold and diagnose** when one gate is amber (fix the amber gate before scaling further). A channel is **demote to experimental** when two gates are amber or any gate is red — the channel is not yet a working primary and either needs more time, more fix-work, or replacement.

The dashboard prevents the two common founder errors: **premature scaling** (spending against a channel that has one green light and three unread lights) and **premature killing** (killing a channel because one gate is red without checking whether the failure is upstream of a fixable input like ICP scoring or attribution setup).

## Concrete example — Loomly's Q1 outbound channel-market-fit read

Loomly (Chapter 1's running example; ACV $12-24K; mid-market SDR-AE motion + PLG top-of-funnel layer; primary channel = founder-led outbound; experimental = inbound content + SEO). By end of Q1 Jane runs the four-gate diagnosis on the outbound primary before hiring the second SDR planned for Q2.

**Setup.** 12 weeks of consistent execution; 1 AE + 1 SDR + Jane running Level-3 top-30 tier herself; 200 target accounts per SDR cadence rotation; combined ~2,400 touches across the quarter. Results: 42 booked meetings, 31 held meetings, 21 opportunities passed AE qualification, 7 closed-won deals at an average $18K ACV, $126K new ARR.

**Gate 1 read — ICP-fit lead quality.**
- *Sub-test 1A firmographic match.* 6 of 7 closed-won accounts are 50-150-engineer B2B SaaS on GitHub (Layer-1 ICP-fit): 86%. **Green.**
- *Sub-test 1B conversion parity.* Lead → opportunity = 21/42 = 50%; founder-led benchmark was 55% during the mod-105 phase. Ratio: 91%. **Green.**
- *Sub-test 1C retention parity.* Too early — the first cohort is 4-12 weeks old, not yet at 90 days. **Deferred; re-read at end of Q2.**

Gate 1 composite: **Green with a deferred sub-test.** Scale decision can proceed conditional on Gate 1C being re-checked at Q2.

**Gate 2 read — unit economics.**
- *Fully-loaded channel CAC.* People cost: 40 hrs/week AE + 40 hrs/week SDR + 15 hrs/week Jane × $150 blended = $22,500/week × 12 weeks = $270K quarterly people cost. Tooling: HubSpot ($1,800/mo), Outreach ($3,000/mo), Apollo ($2,500/mo), LinkedIn Sales Nav ($800/mo) = $8,100/mo × 3 = $24,300 tooling. Attributable overhead: none new. Total: $294,300. Closed-won: 7. **Channel CAC = $42,043.** Benchmark for $18K ACV mid-market: $8-25K. **Red — CAC is 68-425% above the healthy range.**
- *Payback period.* $18K ARR × 78% gross margin = $14,040 annual gross profit = $1,170/month gross profit. Payback = $42,043 / $1,170 = **36 months.** Benchmark: <18 months. **Red — 2× the ceiling.**
- *CAC : LTV.* LTV proxy = $14,040 / assumed 2% monthly churn = $702,000. CAC : LTV = $42,043 : $702,000 = **1 : 16.7.** By ratio alone: green. But the ratio hides the payback problem — the channel is technically LTV-positive but ties up cash for three years before returning it. **Amber on ratio interpretation.**

Gate 2 composite: **Red.** CAC is well above band; payback is well above ceiling. The channel is not currently ready to scale.

**Gate 3 read — time-to-signal maturity.**
- *Window elapsed.* Outbound time-to-signal is 4-6 months of consistent execution + ≥20 closed deals. Loomly is at 3 months, 7 deals. Window elapsed: ~60%. **Amber.**
- *Sample size.* 7 closed deals; defensible threshold is 20. **Red.**

Gate 3 composite: **Amber-red.** The Gate 2 CAC calculation is not yet on a defensible sample. The CAC number might drop as later cohorts close and the ramp effects fade — or might not. **The correct read is "extend the window, re-diagnose in 6 weeks with more closed deals in the sample" before deciding whether the CAC failure is a fix-the-channel problem or a kill-the-channel problem.**

**Gate 4 read — attribution honesty.**
- *Self-reported source data.* HubSpot form has a "how did you hear about us?" field; 88% completion rate on demo-booking form. **Green.**
- *Reconstruction accuracy.* Random sample of 5 closed deals (small quarter): all 5 reconstructible from CRM + email history + self-reported source. **Green.**

Gate 4 composite: **Green.**

**Composite read.** Gate 1: green + deferred. Gate 2: red. Gate 3: amber-red. Gate 4: green. The channel is **hold and diagnose** — do not scale to a second SDR yet. The Gate 2 CAC failure is real but is contaminated by the Gate 3 immaturity — the sample is too small to know whether the CAC number is the channel's steady-state or an artifact of ramp inefficiency.

**Q2 fix plan.**
- Extend the outbound execution another 12 weeks without adding SDR headcount. Track whether closed-deal count reaches 20 by end of Q2 (would put the cumulative deal count at 27 across two quarters — inside the defensible-CAC-sample threshold).
- Diagnose the CAC inefficiency: is it the top-of-tier Level-3 personalisation (which Jane is doing herself and which consumes 15 hrs/week at $200/hr fully-loaded)? Consider handing Level-3 to the AE and freeing Jane's 15 hours for the inbound experimental channel — that alone drops people cost by $36K/quarter, and moves the CAC toward the healthy band.
- Read Gate 1C at Q2 end — if 90-day retention on the acquired cohort is at parity with founder-led, the channel is genuinely producing right-fit customers and the CAC problem is a scale-and-efficiency problem, not a wrong-customer problem.
- Do not hire the second SDR until Gate 2 is amber or better on a defensible-sample CAC calculation.

The alternative — scaling to a second SDR because "42 booked meetings feels like a win" — would have compounded the CAC problem, added another $200-250K of quarterly people cost, and produced a $500K+ per-quarter outbound spend that returns cash on a 36-month cycle. The four-gate diagnostic caught the mismatch before the runway was committed.

## Common failure patterns

- **Read-only-the-lead-count trap.** Founder reports "42 booked meetings" as the primary channel metric; leads are visible in the CRM dashboard, CAC and ICP-fit are not. Founder scales spend on the channel producing the most leads without knowing what the leads convert to. Fix: the primary channel dashboard reports leads *and* Gate 1-4 status; leads without gate status is decoration.
- **CAC-without-fully-loaded-people-cost trap.** Founder reports "CAC = $2,400" (tooling + ad spend) and ignores the $250K/quarter in AE + SDR + founder time. Channel appears wildly profitable; scaling reveals the real math. Fix: fully-loaded CAC always; people cost is the largest line item.
- **CAC-computed-on-6-deals trap.** Founder computes CAC on a 6-closed-deal quarter; number bounces 40% quarter-to-quarter depending on whether one big deal landed; scaling decisions get made against noise. Fix: CAC is only defensible at the sample-size threshold for the channel (Gate 3); below threshold, the CAC number is not a signal.
- **Ignore-retention-parity trap.** Founder reads Gate 1A and 1B at week 8, both green, declares ICP-fit passed, scales. Six months later 90-day retention on the acquired cohort is 30 percentage points below organic; the LTV number was computed against organic retention and is 40% too high; the CAC : LTV ratio was never actually 1 : 5, it was 1 : 3 and dropping. Fix: Gate 1C is *deferred*, not skipped; the ready-to-scale decision has a re-check condition attached.
- **Blended-attribution-across-channels trap.** Founder reports one blended-source attribution for all deals; cannot distinguish outbound-sourced from inbound-sourced revenue; scale decisions are made against a channel-mix number that could mean anything. Fix: attribution is per-channel; blended is a diagnostic view, not an operational view.
- **Self-reported-data-not-collected trap.** No "how did you hear about us?" field; attribution is 100% pixel-based; pixel-based attribution disagrees with reality 30-50% of the time at seed-stage volumes. Fix: self-reported source on every conversion form; treat it as first-order data.
- **UTM-discipline-forgotten trap.** Team posts links on Twitter, HN, LinkedIn without UTMs; team writes cold emails without UTM'd calendar links; attribution reports show "direct traffic" as 60% of sign-ups. Fix: UTM discipline on every published link; templates enforced.
- **Kill-before-window-opens trap.** Founder runs paid for 4 weeks, computes CAC on 8 conversions, panics, kills. Actual answer: 4 weeks is pre-mature; run another 8 weeks, then diagnose. Fix: Gate 3 is a *gate*; you don't kill before the window closes any more than you scale before the window closes.
- **Scale-before-window-opens trap.** Founder runs outbound for 4 weeks, hires two more SDRs on the extrapolation. Cadence performance decays as the target-account list ages; two SDRs against a stale list under-produce. Fix: hire on a defensible-sample number, not a first-quarter extrapolation.
- **CAC : LTV in isolation trap.** Founder reads CAC : LTV = 1 : 5, calls the channel efficient, ignores that payback is 30 months. The channel is LTV-positive on paper but ties up cash for 2.5 years; if the runway is 18 months, the channel bankrupts the company before returning cash. Fix: read CAC : LTV *and* payback; payback dominates at pre-Series-A cash constraint.
- **Confuse-motion-CAC-with-channel-CAC trap.** Founder blends the outbound-channel CAC with the paid-channel CAC into a "sales CAC" figure. When outbound is 1 : 8 and paid is 1 : 1.5, the blended number looks like 1 : 3 — masking that paid is unit-negative. Fix: read every channel separately; only blend when doing top-of-house reporting to the board.
- **Diagnostic-dashboard-not-shared-with-team trap.** Only the founder reads the four-gate dashboard; AEs and SDRs report on activity metrics that are decoupled from the gate signals. Team optimises for booked meetings; nobody notices the CAC failing. Fix: the four-gate dashboard is a shared artifact; SDR and AE weekly review reads it; scaling decisions are visible.
- **Retention-parity-check-deferred-forever trap.** Gate 1C is deferred at the initial read; nobody schedules the re-check; the deferral becomes permanent. Fix: the deferral has a date and an owner; the re-check is a calendar item.

## Summary

- A channel that produces **volume** is not necessarily a channel that produces **ICP-fit revenue at defensible CAC**. The gate-based diagnosis prevents scaling on lead-count alone.
- Four sequential gates: **(1) ICP-fit lead quality** (firmographic + conversion + retention parity vs. the founder-led benchmark), **(2) unit economics** (fully-loaded CAC inside band; payback <18 months; CAC : LTV ≥1 : 3), **(3) time-to-signal maturity** (window elapsed; defensible sample), **(4) attribution honesty** (self-reported source + reconstruction accuracy on a 10-deal sample).
- **Gate 1 is first** because a wrong-ICP channel corrupts every downstream metric. Sub-test 1C (retention parity) is deferred until the first cohort reaches 90-180 days; the deferral has to have a date and owner.
- **Gate 2** uses the operator-level CAC / LTV / payback subset (mod-110 develops the full theoretical treatment). Fully-loaded CAC includes people cost, tooling, and attributable overhead; payback is the practical constraint at pre-Series-A cash levels, not CAC : LTV alone.
- **Gate 3** exists because premature reads produce both false positives (scale-before-window) and false negatives (kill-before-window). Every channel has a natural window; scale decisions wait for it.
- **Gate 4** — attribution honesty — is the diagnostic on the diagnostic. Self-reported source data collected on every conversion; first-touch and last-touch reported side-by-side; UTM discipline on every link; random-sample reconstruction to check the CRM against reality.
- **Composite read**: all green = ready to scale; one amber = hold and diagnose; two amber or any red = demote to experimental or kill.
- The dashboard is a **shared team artifact**, not a founder secret. Weekly during ramp; monthly once stable. Scaling decisions cite the dashboard, not intuition.
- Chapters 3-6 apply this diagnosis inside each of the four primary channel archetypes — inbound (Chapter 3), outbound (Chapter 4), community (Chapter 5), paid (Chapter 6). Chapter 7 develops the **experimentation cadence** that keeps the diagnosis running quarter after quarter as channels decay.
