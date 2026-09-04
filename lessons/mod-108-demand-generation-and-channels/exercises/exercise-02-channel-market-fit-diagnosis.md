# Exercise 02 — Channel-Market-Fit Diagnosis

**Estimated time:** 3 hours
**Chapter link:** [`02-channel-market-fit-diagnosis.md`](../02-channel-market-fit-diagnosis.md)
**Prerequisite:** Chapter 2 read end-to-end; Exercise 01 completed (a chosen primary + experimental channel with owners and investment levels); at least 8-12 weeks of primary-channel data (touches / signups / demos / opportunities / closed-won), or a plausible synthetic dataset for a working example if the primary is not yet ramped. If the primary has been running <8 weeks, use the exercise as a *setup*-diagnostic — score Gate 3 (time-to-signal) red and use the exercise to plan the diagnosis you will run at the 12-week mark.

## Problem statement

Chapter 2 named the failure mode: **the founder observes lead volume from a channel, concludes "the channel is working", scales spend or headcount into it, and discovers three quarters later that the leads were ICP-adjacent but not ICP-fit, the CAC blew past the payback envelope, retention on the acquired customers was 40% worse than on organically-acquired ones, and the runway is now short by the amount of the mis-invested scale**. The remedy is the four-gate diagnosis — ICP-fit lead quality, unit economics, time-to-signal maturity, attribution honesty — run before scaling spend or headcount.

This exercise trains you to **run the four-gate diagnosis on your primary channel (and, if applicable, your experimental channel) with the real numbers you have**. Produce the composite dashboard, name the ready-to-scale / hold-and-diagnose / demote decision, and write the scale-or-fix plan the next quarter's operating cadence runs on.

The failure mode this exercise exists to catch: **the founder reads lead volume off the CRM dashboard, extrapolates "we're on track for 200 booked meetings per quarter, let's hire two more SDRs", hires against a first-quarter number that was noise, and produces an expensive downstream unwind when the gate 2 (CAC) and gate 3 (sample size) reads would have flagged the extrapolation as premature.**

## Requirements

Deliver a folder `exercise-02/` with four files:

- `part-a-data-collection.md` — the primary channel's data assembly (with the specific numbers Chapter 2's gates require).
- `part-b-gate-1-icp-fit.md` — the ICP-fit gate reads (Sub-tests 1A firmographic, 1B conversion parity, 1C retention parity or deferral).
- `part-c-gates-2-3-4.md` — the unit economics, time-to-signal, and attribution gates.
- `part-d-composite-and-plan.md` — the composite dashboard read and the next-quarter scale-or-fix plan.

### Part A — Assemble the data (45 min)

Deliver `part-a-data-collection.md`. Populate the following for the primary channel over the most-recent complete quarter (or the longest complete window ≥ 8 weeks).

**A1 — Channel identification (5 min).**
- Channel name (per Exercise 01's primary decision).
- Time window covered (start date → end date).
- Weeks of consistent execution (a week is "consistent" if the channel's minimum activity level was maintained; incomplete weeks are noted).
- Owner(s) executing the channel.

**A2 — Volume metrics (10 min).**
- **Top-of-funnel actions** (touches, signups, ad clicks, community joins, event conversations — pick the metric that fits the channel).
- **Held meetings / activated users / opportunities passed to AE** (mid-funnel).
- **Closed-won deals from the channel** (bottom-funnel, first-touch-attributed).
- **Closed-won ARR from the channel** (dollar-value).

**A3 — People and tooling cost (10 min).**
- Every person whose time this channel consumed, with hours/week × fully-loaded blended $/hour × weeks in the window. Include founder time (do not exclude — Chapter 2's most common CAC undercount is founder time).
- Tooling cost attributable to this channel (CRM allocated fraction, cadence tool, enrichment, ad-platform fees, community platform, event costs). Amortise fixed tooling across the channels that use it.
- Attributable overhead (any additional overhead specifically consumed by this channel).
- Ad spend (for paid channels).

Total **fully-loaded channel spend for the window** = people cost + tooling + attributable overhead + ad spend.

**A4 — Cohort characteristics (10 min).**
- Number of closed-won accounts from the channel in the window.
- For each closed-won account (or a random sample of 10 if the count is larger), record: firmographic tier (Layer-1 ICP match yes/no per mod-104 scorecard); behavioural tier (Layer-2 match yes/no); first-touch-source (per CRM attribution); self-reported source (per "how did you hear about us?" field); ACV.
- For each closed-won account, record whether it has reached the 90-day and 180-day mark (retention Sub-test 1C is deferred until the earliest cohort reaches 90 days; note the deferral if applicable).

**A5 — Comparison baseline (10 min).**
- Founder-led-sales benchmark from mod-105 or from your Exercise 01 Part A2: lead → opportunity conversion; opportunity → close conversion; 90-day and 180-day retention.
- Chapter 2's benchmark CAC range for your ACV band + motion (per the table).
- Chapter 2's benchmark payback ceiling for your ACV band (default: <18 months).

### Part B — Gate 1 (ICP-fit lead quality) reads (30 min)

Deliver `part-b-gate-1-icp-fit.md`.

**B1 — Sub-test 1A (firmographic match).** From Part A4, compute % of closed-won accounts that are Layer-1 ICP-fit. Compute % Layer-2 ICP-fit. Score:
- Green ≥80% Layer-1 / ≥60% Layer-2
- Amber 60-79% Layer-1 or 40-59% Layer-2
- Red <60% Layer-1 or <40% Layer-2

Write a paragraph on what the ICP-fit distribution reveals — are non-ICP-fit accounts clustering in a specific misfire (adjacent firmographic tier, wrong buyer role, wrong industry)?

**B2 — Sub-test 1B (conversion parity).** Compute:
- Lead → opportunity rate for this channel (from Part A2).
- Opportunity → close rate for this channel.
- Same rates for the founder-led benchmark (Part A5).
- Ratio of channel-rate to founder-led-rate.

Score:
- Green ≥70% of founder-led benchmark
- Amber 40-69%
- Red <40%

Write a paragraph on which stage of the funnel is the closest to founder-led parity and which is furthest. A channel that hits founder-led rates on lead → opportunity but crashes on opportunity → close is producing leads with the right interest signal but wrong buying-context (or vice versa).

**B3 — Sub-test 1C (retention parity).** If the earliest cohort has reached 90 days: compute 90-day logo retention on channel-acquired customers vs. founder-led benchmark; compute delta in percentage points. Score green (delta within 10pp), amber (10-25pp gap), red (>25pp gap).

If the earliest cohort has NOT reached 90 days: **defer** the sub-test. Write down: the specific date the deferral is re-checked (calendar item), the owner of the re-check, the sample size expected at re-check.

**B4 — Gate 1 composite.** Green if all three sub-tests green. Amber if any sub-test is amber (or 1C is deferred with green on 1A and 1B). Red if any sub-test is red.

### Part C — Gates 2, 3, and 4 reads (60 min)

Deliver `part-c-gates-2-3-4.md`.

**C1 — Gate 2 (unit economics) reads (25 min).**

- **Fully-loaded channel CAC.** From Part A3 total spend ÷ Part A4 closed-won count. Show the arithmetic.
- **CAC vs. band benchmark.** From Part A5's benchmark range for your ACV band + motion. Score: green (inside range), amber (up to 25% above range), red (>25% above range).
- **LTV proxy.** ACV × gross margin ÷ monthly churn rate. Use best-available monthly churn (from mod-109 if available; a working default of 2%/month for early-SMB, 1%/month for mid-market, 0.5%/month for enterprise if you have no cohort data yet — label the default).
- **Payback period.** CAC ÷ (monthly ARPA × gross margin). Show arithmetic. Score green (<12 months), amber (12-18 months), red (>18 months).
- **CAC : LTV ratio.** Score green (≥1:3), amber (1:2 to 1:3), red (<1:2).

Gate 2 composite: green if all three metrics green; amber if any single metric is amber; red if any single metric is red *or* if two metrics are amber.

**C2 — Gate 3 (time-to-signal maturity) reads (15 min).**

- **% of time-to-signal window elapsed.** From Part A1's weeks-of-execution vs. Chapter 2's channel-specific time-to-signal window. Score green (≥100%), amber (50-99%), red (<50%).
- **Sample size vs. defensible-CAC threshold.** From Part A4's closed-won count vs. Chapter 2's channel-specific sample threshold. Score green (≥threshold), amber (50-100%), red (<50%).

Gate 3 composite: green if both green; amber if one amber; red if either red.

**Critical interpretive note.** If Gate 3 is red-amber-red or red, the Gate 2 reads are on a thin sample and should be treated as *provisional*, not definitive. Note this explicitly.

**C3 — Gate 4 (attribution honesty) reads (20 min).**

- **Self-reported source completion rate.** From Part A4 sample or from the underlying CRM data: what % of sign-ups (or demo bookings) have a completed self-reported source field? Score green (≥90%), amber (60-89%), red (<60%).
- **Reconstruction accuracy on 10-deal sample.** Pick 10 random closed-won deals from the channel (or all of them if fewer). For each, reconstruct the buyer journey from first-touch to close using CRM + self-reported source + email history + platform reports. Score reconstructible / not-reconstructible per deal. Score green (≥8/10), amber (5-7/10), red (≤4/10).
- **First-touch vs. last-touch cross-check.** For the 10-deal sample, does the first-touch source in your CRM match the self-reported source? Note the disagreement rate. If self-reported disagrees with tracked >30% of the time, add a note that tracked attribution is unreliable at current volumes and the self-reported side should be treated as ground truth.

Gate 4 composite: green if both green (or one green + one amber with a clear plan to fix the amber); amber if two amber; red if any red.

### Part D — Composite dashboard and next-quarter plan (45 min)

Deliver `part-d-composite-and-plan.md`.

**D1 — Composite dashboard (10 min).** One-page dashboard summarising all four gates. Structure:

```
# Channel Diagnosis Dashboard — {channel} — {date}

## Gate 1 — ICP-fit lead quality
- 1A firmographic match: {%} — {G/A/R}
- 1B conversion parity: {ratio} — {G/A/R}
- 1C retention parity: {delta or DEFERRED} — {G/A/R or D}
- Composite: {G/A/R}

## Gate 2 — Unit economics
- Fully-loaded CAC: ${amount} (vs. band ${range}) — {G/A/R}
- Payback: {months} — {G/A/R}
- CAC : LTV: {ratio} — {G/A/R}
- Composite: {G/A/R}

## Gate 3 — Time-to-signal maturity
- Window elapsed: {%} — {G/A/R}
- Sample size: {n} vs. threshold {n} — {G/A/R}
- Composite: {G/A/R}

## Gate 4 — Attribution honesty
- Self-reported source completion: {%} — {G/A/R}
- Reconstruction accuracy: {n/10} — {G/A/R}
- Composite: {G/A/R}

## Overall verdict
- {READY TO SCALE / HOLD AND DIAGNOSE / DEMOTE TO EXPERIMENTAL / KILL}
```

**D2 — Verdict (10 min).** From Chapter 2's composite read:
- All four gates green → **READY TO SCALE**
- One gate amber → **HOLD AND DIAGNOSE** (fix the amber gate before scaling)
- Two gates amber or any single gate red → **DEMOTE TO EXPERIMENTAL** or **KILL** (depending on whether the failure is fixable within the current investment level)

Write one paragraph on the verdict, citing which gate(s) drive it.

**D3 — Fix plan for each non-green gate (15 min).** For each amber or red gate, write a fix plan structured as:

- **Root cause hypothesis.** What is producing the amber/red read? (Small sample? Wrong ICP mid-tier? Attribution misconfiguration?)
- **Fix action.** What specifically will be done in the next 6-12 weeks to address it? (Extend the window with no scale-up? Tighten targeting? Add self-reported source field? Rebuild the attribution stack?)
- **Owner and checkpoint date.** Who is doing it; when is the re-read.

**D4 — Scale-or-fix decision + operating consequences (10 min).** Given the verdict + fix plan, name the operating consequences for the next quarter:

- **Hiring decisions.** Are you hiring the second SDR, the content lead, the paid marketing specialist? If the primary is not READY TO SCALE, the hiring is deferred and named as deferred.
- **Spend decisions.** Are you doubling paid budget? If not READY TO SCALE, spend holds at current level.
- **Experimental-channel implications.** Is the experimental staying the experimental, or is it graduating to co-primary because the primary is failing gates? (Chapter 7's graduation rule; will drive Exercise 06's paid decisions if paid is your experimental.)
- **Next quarterly-review date.** When will the diagnosis be re-run? (Per Chapter 7's quarterly cadence.)

## Starter guidance

- **Full-loaded people cost is the CAC line item founders under-count most.** Chapter 2's most common trap: reporting "CAC = ad spend + tooling" and ignoring the $200K/quarter in AE + SDR + founder time. Include *all* people cost in A3; if the founder is spending 15 hours/week on this channel, that is 15 × 4 × $200/hour blended = $12,000/month of channel cost, whether or not the founder is on payroll.
- **Amber-with-deferred-1C is not green.** Chapter 2's Sub-test 1C is the retention parity read; deferring it (because the cohort hasn't reached 90 days) does not mean it's green. The composite is amber-pending-1C, and the scaling decision has a re-check condition attached. Write the calendar item; do not let the deferral become permanent.
- **Gate 3 red often makes Gate 2 provisional.** If your sample size is 4 closed deals, the CAC calculation is noise. Note this in D3 — the fix for a red Gate 3 is *extending the window*, not concluding the channel has failed. The Gate 2 read is re-taken when the sample is defensible.
- **The self-reported source field is the ground truth against which tracked attribution is calibrated.** Chapter 2's Discipline 1 is not decoration; a channel diagnosis without self-reported source data is guessing at attribution. If your form does not have the field, adding it is the highest-leverage attribution fix in D3.
- **A single-channel CAC does not blend with other channels.** If your outbound CAC is $8K and your paid CAC is $22K, do not report a blended $12K "sales CAC". Each channel is diagnosed independently; blending hides which channel is producing which economics.
- **The scale-or-fix decision is a *decision*, not a report.** D4 has to name specific operating consequences — a hire that gets deferred, a budget that holds, an experimental that graduates. A diagnosis without operating consequences is a report that goes into a folder; a diagnosis with operating consequences is the input to the next quarterly review.
- **If the primary is failing gates and the experimental is passing them, name that.** Chapter 7's graduation rule kicks in here — a passing experimental against a failing primary is a candidate swap. Do not resist the swap because the primary was "the plan"; the diagnosis is what the plan is now.
- **Fix the attribution stack before scaling.** A green Gate 4 is a hard pre-condition for defensible scaling. If Gate 4 is amber or red, the scaling decision is on unreliable data; the highest-priority D3 fix is the attribution stack.

## Acceptance criteria

Your submission is complete when:

- [ ] Part A assembles the primary channel's data with the specific numbers each gate requires (volume metrics, fully-loaded spend including all people cost, cohort characteristics, comparison baseline).
- [ ] Part B computes Sub-tests 1A, 1B, and 1C (or explicitly defers 1C with a calendar item) with green/amber/red scores.
- [ ] Part C computes Gates 2, 3, and 4 with green/amber/red scores per Chapter 2's thresholds.
- [ ] Part D produces a one-page composite dashboard with all four gates + overall verdict.
- [ ] Part D names the verdict (READY TO SCALE / HOLD AND DIAGNOSE / DEMOTE / KILL) with citation to the driving gate.
- [ ] Part D writes a fix plan for each non-green gate with root-cause hypothesis + fix action + owner + checkpoint date.
- [ ] Part D names specific operating consequences — hiring decisions, spend decisions, experimental-channel implications, next quarterly-review date.
- [ ] If the primary has been running <8 weeks, the exercise is treated as a *setup diagnostic* and the plan is for the diagnosis to be re-run at the 12-week mark; the calendar item is written.
- [ ] Any factual claim (a benchmark, a competitor's CAC, an industry retention number) that is not cited to mod-104 / mod-105 / mod-106 / mod-107 / mod-108 or explicitly derived is flagged `<!-- needs-research: ... -->`.

## Common ways this exercise goes wrong

- **CAC-without-fully-loaded-people-cost trap.** Founder reports "CAC = $2,400" (tooling + ad spend) and ignores $250K/quarter of AE + SDR + founder time. Channel appears wildly profitable. Fix: fully-loaded CAC always in A3; people cost is nearly always the largest line item.
- **CAC-computed-on-6-deals trap.** Founder reports a defensible-looking CAC number that was computed on 4-6 closed deals. Number would bounce 40% quarter-to-quarter on which single deals landed. Fix: Gate 3 red on sample size makes Gate 2 provisional; note this in D2's verdict.
- **Ignore-1C trap.** Founder scores Gate 1 green on 1A + 1B and skips 1C entirely ("we'll see about retention later"). Six months later paid-cohort retention is 30pp below organic; the CAC : LTV ratio in D2 was computed on wrong LTV. Fix: 1C is deferred with a calendar item, not skipped.
- **Green-on-attribution-when-no-self-reported-source trap.** Founder claims Gate 4 green based on the CRM's automatic first-touch report; there is no self-reported source field. Automatic attribution is 30-50% wrong at seed volumes; Gate 4 is amber or red until self-reported data collection is in place. Fix: self-reported source is a discipline that has to be running before Gate 4 can be scored green.
- **Verdict-without-plan trap.** D2 names the verdict but D3 does not produce a fix plan for the non-green gates. Diagnosis becomes decoration. Fix: every non-green gate has a specific fix plan with root cause + action + owner + date.
- **Plan-without-operating-consequences trap.** D3 names fixes but D4 does not translate them into hiring / spend / experimental / cadence decisions. Diagnosis stays in the analytics layer. Fix: D4 has to name specific operating consequences; if it does not, the diagnosis is not yet a decision.
- **Confuse-motion-CAC-with-channel-CAC trap.** Founder reports "sales CAC" as a blend of outbound + paid + inbound. When one is 1:1 and one is 1:8, the blend is 1:3 and neither's economics are visible. Fix: separate CAC per channel; only blend at top-of-house board reporting.
- **Diagnostic-dashboard-not-shared trap.** Founder writes the dashboard for herself; AEs and SDRs report on activity metrics decoupled from the gates. Team optimises for booked meetings; no one notices Gate 2 failing. Fix: the dashboard is a shared team artifact; scaling decisions cite it.
- **Kill-before-window-opens trap.** Channel has been running 4 weeks; Gate 2 reads red; founder concludes "the channel doesn't work". 4 weeks is diagnostic-invisible per Gate 3. Fix: Gate 3 is a gate, not a suggestion; kill/scale decisions wait for the window.
- **Never-run-the-diagnosis-again trap.** Exercise 02 is run once and never re-run. The primary channel decays (Chapter 7); no one notices. Fix: D4's next quarterly-review date is a calendar item; the diagnosis is a rhythm, not a one-time exercise.
