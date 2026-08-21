# Leading vs. Lagging — The Weekly and Monthly GTM One-Pager

## Motivation

Chapters 2–4 fixed the numbers themselves — CAC, LTV, payback, LTV/CAC, magic number, sales efficiency, funnel conversion, cohort retention, NRR, GRR, burn multiple. That is a long list of numbers, and the temptation is to publish all of them on one dashboard on one cadence and call it the operator view.

This is the specific mistake that produces a "dashboard" nobody reads. **The numbers live on two cadences, and the two cadences are load-bearingly different.** The weekly one-pager reads *leading indicators* — activity, pipeline creation, stage advancement — that tell the founder whether the motion is *loading this month*. The monthly one-pager reads *lagging indicators* — CAC, payback, magic number, retention, NRR — that tell the founder whether the motion is *efficient over last month*. Both are necessary; neither substitutes for the other.

The failure mode this chapter exists to catch: **the founder maintains a monthly one-pager with CAC, payback, magic number, LTV/CAC — all lagging — and discovers on the third week of February that January's opportunity-creation rate collapsed in the second week of January, six weeks after the leak could have been diagnosed and fixed. The lagging one-pager could not have caught the January drop; the weekly one-pager would have caught it in the second week of January.**

The remedy: two one-pagers on two cadences, with a **specific discipline about which numbers go on which** — leading indicators on the weekly (activity, pipeline creation, stage advancement, per-AE reads) and lagging indicators on the monthly (CAC, retention, magic number, LTV, payback, NRR).

## Core concepts

### Leading vs. lagging — the distinction that structures the two one-pagers

A **leading indicator** is a number that changes *before* the outcome you care about. Pipeline creation this week leads next month's revenue; SAL-acceptance rate this week leads next month's proposal rate. Activity metrics (calls dialled, demos held, opportunities created) are the most leading; stage-advancement metrics (SAL created, Discovery held, Demo held) are one step less leading; proposals sent and forecast committed are the least leading of the leading-side numbers.

A **lagging indicator** is a number that describes an outcome that has already occurred. Closed-won ARR is lagging (the deal happened); MRR / ARR is lagging; CAC is lagging (the spend and the acquisition have both happened); retention is lagging (the churn has happened); NRR is lagging; payback is lagging.

**The load-bearing rule:** you *react* to lagging indicators; you *manage* leading indicators. If the lagging number is bad, the leading indicator that caused it has already been bad for weeks. Managing on lagging indicators alone means you always find out too late to change the outcome.

The specific coupling that makes this practical: leading indicators are the ones with the most operating leverage — the ones the founder or GTM lead can *directly influence this week*. Lagging indicators are the ones the founder can influence only through the compounding of the leading ones over months.

### The weekly one-pager — leading indicators the founder acts on Monday

The weekly one-pager is published every Monday morning by the founder or GTM lead. Reads in five minutes. Answers *"is the motion working this week?"*

**Contents (recommended template):**

```
GTM WEEKLY — [Startup] — Week of [YYYY-MM-DD]
Author: [Founder / GTM Lead]. Publish cadence: every Monday 09:00.

1. ACTIVITY (last 7 days)
   Founder outbound: N accounts touched, M meetings booked
   AE outbound (per rep): {AE1: N touched, M booked} {AE2: ...}
   Inbound-response: N MQLs, T minutes median response time
   Demos held: N (target: ≥N per week)
   Proposals sent: N

2. PIPELINE CREATION (last 7 days)
   New opportunities created: N ($X ARR, average ACV $Y)
     By channel: [outbound N ($X); inbound N ($X); paid N ($X)]
     By rep: [Founder N ($X); AE1 N ($X); AE2 N ($X)]
   Opportunities advanced (moved forward a stage): N
   Opportunities regressed / marked no-decision: N

3. PIPELINE HEALTH (as of this Monday)
   Total open pipeline (Discovery/Demo/Proposal): $[X]
   Coverage vs. quarterly quota: [X] × (required for historic conv: [Y] ×)
   Stalled deals (no touch in ≥14 days): N ($[X])

4. CURRENT-QUARTER FORECAST
   Committed:    $[X] ([N] deals with ≥90% probability + signed)
   Best-case:    $[X] ([N] deals with ≥50% probability)
   Pipeline:     $[X] ([N] deals with <50% probability)
   Quarter quota / plan: $[X]  Delta to committed: $[+/-X]

5. THIS WEEK'S ONE FOCUS
   [The one specific thing that most changes next month's revenue if fixed this week]
   Owner: [name]  Success: [specific outcome by Friday]
```

Every number on the weekly is a leading indicator or a same-week forecast — nothing lagging. Retention, CAC, NRR, LTV/CAC do not appear on the weekly. They appear on the monthly.

**The "one focus" line is the whole point of the weekly.** The dashboard is instrumental; the focus is the deliverable. If the focus is empty or trivial, the founder should not publish that week's one-pager — she has not made a decision.

### The monthly one-pager — lagging indicators the founder reports and diagnoses

The monthly one-pager is published on (approximately) the 3rd of each month, describing the previous month. Reads in ten minutes. Answers *"is the motion efficient? Is the motion ready to scale?"* — the second and third of the three operator questions from Chapter 1.

**Contents (recommended template):**

```
GTM MONTHLY — [Startup] — [Month YYYY]
Author: [Founder / GTM Lead]. Publish cadence: 3rd of each month.

1. REVENUE
   Closed MRR/ARR (month): $[X]
   Net-new ARR (month): $[X]  YoY: [+/-Y%]
   Total ARR (end of month): $[X]  M/M growth: [+/-Y%]
   Segment split (Enterprise / Mid-market / SMB):
     Enterprise: $[X] MRR, [N] logos
     Mid-market: $[X] MRR, [N] logos
     SMB:        $[X] MRR, [N] logos

2. CAC (fully-loaded, per-channel)
   Blended CAC: $[X]  Trend (T3M): [+/-Y%]
   Per-channel CAC:
     Founder outbound: $[X]  ([N] logos)
     AE outbound:      $[X]  ([N] logos)
     Paid:             $[X]  ([N] logos)
     SEO / content:    $[X]  ([N] logos)
     [Other]:          $[X]  ([N] logos)
   Benchmark band ([motion type], [ARR tier]): $[X]-$[Y]

3. LTV, PAYBACK, LTV/CAC
   Per-channel (cohort-based, gross-margin adjusted, capped 36mo):
                     LTV        Payback   LTV/CAC
     Founder outbnd  $[X]       [N] mo    [X]x
     AE outbound     $[X]       [N] mo    [X]x
     Paid            $[X]       [N] mo    [X]x
     [Other]         $[X]       [N] mo    [X]x
   Blended            $[X]       [N] mo    [X]x
   Benchmark bar:                <[N] mo   >=3x

4. EFFICIENCY RATIOS
   Magic number (net, prior-quarter S&M):    [X.X]  Trend (T3M): [+/-Y%]
   Sales efficiency (New ARR / S&M, same-period): [X.X]
   Burn multiple (net cash burn / net-new ARR): [X.X]x

5. RETENTION (inherited from mod-109)
   GRR (T12M): [X]%  Segment split: E [X]% / MM [X]% / SMB [X]%
   NRR (T12M): [X]%  Segment split: E [X]% / MM [X]% / SMB [X]%
   Cohort W12 retention (latest cohort, primary segment): [X]%
     Trend (last 6 cohorts): [flat / drifting +/-Y pp]

6. FUNNEL CONVERSION (month vs. T6M baseline)
   MQL → SAL:              [X]%  vs. [Y]%  ([+/-] pp)
   SAL → Discovery:        [X]%  vs. [Y]%  ([+/-] pp)
   Discovery → Demo:       [X]%  vs. [Y]%  ([+/-] pp)
   Demo → Proposal:        [X]%  vs. [Y]%  ([+/-] pp)
   Proposal → Closed-Won:  [X]%  vs. [Y]%  ([+/-] pp)
   Top-to-Won:             [X]%  vs. [Y]%  ([+/-] pp)

7. HEADLINE READ + ONE PRIORITY FOR THE MONTH AHEAD
   [One paragraph — the state of the three operator questions:
     Is the motion working? Efficient? Ready to scale?
    One specific priority for the coming month — the number to move.]

APPENDIX (linked)
   - CAC decomposition worksheet: [link]
   - Cohort retention chart: [link]
   - Funnel conversion detail: [link]
   - Pipeline detail (CRM view): [link]
```

Every number cites a source — the billing system, the ad platforms, the CRM, the payroll system, the mod-109 retention read. A hostile question ("where did the $10,551 CAC come from?") has a same-day answer.

### The header discipline — dated, signed, versioned

Same discipline as [mod-102 Chapter 7](../mod-102-pmf-signal-and-measurement/) and [mod-109 Chapter 7](../mod-109-retention-expansion-and-growth-loops/07-retention-expansion-scorecard.md):

- **Dated.** Every one-pager is dated. A weekly from three weeks ago is a historical document; the operator reads the current week's.
- **Signed.** The author is named. The one-pager is opinionated; the reader needs to know whose read they are absorbing.
- **Versioned.** Preserve prior weeks and prior months. The delta between versions is the operating output — a magic number that moved from 1.4 to 0.9 M/M is a signal, and the signal is visible only if v(n-1) is preserved alongside v(n).

### The "one focus" and "one priority" lines — the whole point

Both one-pagers end with a *one-line* operating priority — the weekly ends with the *one focus* for this week; the monthly ends with the *one priority* for the coming month. Not five, not three. One.

If the founder cannot pick one, either the numbers have not converged (in which case the diagnosis is incomplete) or she is trying to do too many things at once (in which case the operating discipline will land nowhere). The "one priority" line is a forcing function — pick one, act on it, and re-read next month.

The mod-109 Chapter 7 scorecard applied the same discipline ("one next-quarter priority") for the same reason. The one-pager inherits it.

### The three operator questions, mapped to the one-pager sections

From Chapter 1:

- **"Is the motion working?"** → Weekly sections 1–4 (activity, pipeline creation, pipeline health, forecast). Monthly section 1 (revenue), section 6 (funnel conversion).
- **"Is the motion efficient?"** → Monthly sections 2 (CAC), 3 (LTV/payback), 4 (efficiency ratios), 5 (retention).
- **"Is the motion ready to scale?"** → Monthly section 7 (headline read + priority) and Chapter 6's first-hire staging plan.

Every number on either one-pager maps to one of the three. If a number cannot be mapped, it does not belong on the one-pager.

### The board-pack extension — quarterly

The board pack (quarterly cadence) is the monthly one-pager plus:

- **Trailing-3-month trend** on every metric — a mini sparkline or a three-value cell.
- **Year-over-year comparison** on the composite ratios.
- **Segment cuts** at the ARR-band level (already in the monthly if the monthly follows the template).
- **A narrative paragraph per operator question.**
- **One next-quarter priority** (aligned with or a rollup of the three monthly priorities from the trailing three months).

**No new data collection.** If the monthly one-pager is maintained honestly, the board pack falls out. The mistake founders make is treating the board pack as its own artifact requiring new data assembly three weeks before the board meeting; if you did that, you skipped the monthly one-pager discipline.

Chapter 7 assembles the board-pack GTM section explicitly.

### Reading the two one-pagers together — the operator loop

The weekly and monthly one-pagers reinforce each other:

- **Weekly detects the leading-indicator drift.** Pipeline creation is off; SAL-acceptance is low; the paid-channel MQLs stopped in week 2. Fix routed same week.
- **Monthly detects the lagging-indicator consequence** (or the absence of it, if the weekly fix worked). CAC drifted; retention held; magic number moved.
- **Weekly's "one focus" is often driven by the previous month's monthly-headline read.** ("Magic number fell to 0.85 last month; this week's focus is the paid-channel CAC audit.")
- **Monthly's "one priority" is often reinforced by the trailing weeks' one-focus lines.** ("Three of the last four weeks focused on Demo → Proposal recovery; this month's priority is the coaching-plan for AE #2.")

The loop is what makes the operator view actually operate. A weekly one-pager that lists numbers with no focus, or a monthly that reports numbers with no priority, produces the dashboard-that-nobody-reads pathology Chapter 1 warned about.

## Concrete example — the code-review-tool weekly + monthly, Q2 2026

**Weekly one-pager, week of 2026-06-30:**

```
GTM WEEKLY — Reviewer.io — Week of 2026-06-30
Author: Alex Reyes (Founder / CEO)

1. ACTIVITY (last 7 days)
   Founder outbound: 48 accounts touched, 6 meetings booked
   AE outbound (Priya): 62 accounts touched, 4 meetings booked
   Inbound-response: 12 MQLs, 22 min median response time (target ≤30 min)
   Demos held: 9 (target: >=8/week)
   Proposals sent: 3

2. PIPELINE CREATION (last 7 days)
   New opportunities created: 7 ($151k ARR, avg ACV $21,600)
     Founder outbound: 4 ($86k)  |  AE outbound: 2 ($43k)  |  Inbound: 1 ($22k)
     [note: 0 from paid this week — 3rd consecutive week of 0 from paid]
   Opportunities advanced: 5
   Opportunities regressed / no-decision: 2

3. PIPELINE HEALTH (as of Monday)
   Total open pipeline (Disc/Demo/Prop): $1.4M
   Coverage vs. Q3 quota ($400k): 3.5x (required for historic conv 15.5%: 6.4x)
   Stalled deals (no touch >=14 days): 6 ($134k)

4. CURRENT-QUARTER (Q3) FORECAST
   Committed: $186k  |  Best-case: $312k  |  Pipeline: $520k
   Q3 quota: $400k  |  Delta to committed: -$214k

5. THIS WEEK'S ONE FOCUS
   Convene mod-108 Chapter 2 paid-channel audit meeting (Wed).
   Objective: decision by Friday on defund vs. re-configure paid.
   Owner: Alex + Marketing Manager (Sam). Success: written decision published.
```

**Monthly one-pager, published 2026-07-03 for June 2026:**

```
GTM MONTHLY — Reviewer.io — June 2026
Author: Alex Reyes. Prior: v-May-2026, v-Apr-2026, v-Mar-2026.

1. REVENUE
   Closed MRR (June): $54k    Net-new ARR (June): $124k
   Total ARR: $5.18M  M/M growth: +2.4%
   Segment: E $760k (14 logos)  MM $3.98M (198 logos)  SMB $440k (36 logos)

2. CAC (fully-loaded, per-channel, June)
   Blended: $10,551 (T3M: +19%, drifting UP — a specific signal)
   Founder outbound:  $5,213 (12 logos)
   AE outbound:       $8,650 (8 logos)
   Paid (LinkedIn):  $13,122 (9 logos)   <-- above benchmark for MM
   SEO / content:    $10,138 (4 logos)
   Event:            $37,025 (1 logo — DevTools Summit, non-repeatable)
   Benchmark (MM AE, ACV ~$22k): commonly $8k-$25k CAC.

3. LTV, PAYBACK, LTV/CAC (cohort-based, 36-mo cap)
                     LTV       Payback    LTV/CAC
   Founder outbnd    $16,760   3.7 mo     3.20x
   AE outbound       $16,760   6.2 mo     1.94x  (AE ramping, per note)
   Paid              $10,246   9.3 mo     0.78x  <-- UNRECOVERABLE
   SEO / content     $13,900   7.2 mo     1.37x
   Blended           $14,200   7.5 mo     1.35x
   Benchmark:        n/a       <18 mo     >=3x

4. EFFICIENCY RATIOS
   Magic number (net, prior-Q S&M): 2.62 (T3M: 2.8 -> 2.4 -> 2.6 — flat-ish)
   Sales efficiency (New ARR / S&M same-period): 0.56
   Burn multiple: 5.5x  <-- HIGH (R&D-heavy; not S&M)

5. RETENTION (from mod-109 scorecard, June)
   GRR (T12M): 77.8%  Segment: E 44%, MM 84%, SMB 71%
   NRR (T12M): 110.2%  Segment: E 44%, MM 118%, SMB 92%
   Cohort W12 (latest MM cohort): 62%  Trend (last 6 cohorts): 72% -> 62% (down)

6. FUNNEL CONVERSION (June vs. T6M baseline)
   MQL -> SAL:            19%   vs. 22%   (-3 pp)
   SAL -> Discovery:      64%   vs. 68%   (-4 pp)
   Discovery -> Demo:     52%   vs. 55%   (-3 pp)
   Demo -> Proposal:      32%   vs. 45%   (-13 pp)  <-- STAGE FAILURE
   Proposal -> Closed-Won: 58%  vs. 62%   (-4 pp)
   Top-to-Won:            1.16% vs. 2.06% (-44% relative)

7. HEADLINE READ + ONE PRIORITY FOR JULY

   Motion is producing efficiently on the founder-outbound and (ramping) AE
   channels — magic number 2.6, per-channel LTV/CAC 3.2x and 1.94x are healthy
   given the AE ramp. Paid channel is UNRECOVERABLE at 0.78x LTV/CAC and CAC
   drifting up materially — this is a mod-108 Chapter 2 channel-market-fit
   failure and defunding is the operator decision. Motion is NOT yet ready to
   scale via a second AE hire: the funnel Demo -> Proposal degraded 13pp this
   month (isolated to paid-channel-sourced opportunities on inspection), and
   the AE-cohort LTV/CAC is still below 2x pending ramp. Retention is
   COMPENSATING (NRR clears bar; GRR weak; expansion doing lifting) per the
   mod-109 scorecard.

   ONE PRIORITY FOR JULY: Complete the mod-108 paid-channel audit and
     execute the defund-or-reconfigure decision. Expected impact: blended CAC
     falls to <$9k, magic number rises back toward 3.0, funnel Demo -> Proposal
     recovers as paid-sourced opportunity mix drops.

APPENDIX (linked)
   - CAC decomposition worksheet:      /gtm/2026-06/cac-worksheet.xlsx
   - Cohort retention chart:           /retention/2026-06/cohorts-by-segment.png
   - Funnel conversion detail:         /gtm/2026-06/funnel-detail.png
   - Pipeline detail (Salesforce):     /crm/pipeline-2026-Q3
```

One page (two if the formatting stretches). Every number sourced. Every ratio benchmarked. Retention inherited from mod-109. The one priority is falsifiable (either the audit ships and paid gets defunded / reconfigured, or it does not). A hostile board question on any number has a same-day answer in the appendix.

## Common failure patterns

- **One dashboard with all the numbers.** Weekly and monthly are different reads for different questions. Two documents; two cadences.
- **Retention / CAC / NRR on the weekly.** These are lagging — they cannot inform this week's decision. Belong on the monthly.
- **Activity / opportunity-creation on the monthly.** These are leading — reading them once a month misses the four weekly signals in between. Belong on the weekly.
- **A monthly one-pager with no per-channel decomposition.** Chapter 2 said this; if the CAC / LTV rows are blended-only, the one-pager fails.
- **A weekly one-pager with no "one focus" line.** The focus is the deliverable; the numbers are the evidence.
- **A monthly with no "one priority" line.** Same problem, longer cadence.
- **Board pack assembled from scratch three weeks before the meeting.** If you did that, you skipped the monthly one-pager discipline for the trailing quarter.
- **Numbers on the one-pager that do not reconcile to a system of record.** Every number cites its source; a hostile question has a same-day answer.
- **Un-versioned one-pagers.** The delta between versions is the operating engine's output; preserve prior versions.

## Summary

- **Leading vs. lagging is the distinction that structures the two one-pagers.** Activity and pipeline creation are leading; revenue, CAC, retention, NRR, magic number are lagging.
- **Weekly one-pager: leading indicators, published Monday, reads in 5 minutes.** Activity, pipeline creation, pipeline health, current-quarter forecast, one focus for the week.
- **Monthly one-pager: lagging indicators, published on the 3rd of the month, reads in 10 minutes.** Revenue, CAC (per-channel), LTV / payback / LTV/CAC (per-channel), efficiency ratios, retention (from mod-109), funnel conversion, headline read + one priority for the month.
- **Both are dated, signed, versioned.** The delta between versions is the operating output.
- **The "one focus" and "one priority" lines are the deliverables.** Numbers without a focus are a dashboard nobody reads.
- **The board pack is the monthly one-pager plus trend and YoY.** No new data collection; if you skipped the monthly, you skipped the board pack too.
- **The three operator questions from Chapter 1 map to the one-pager sections.** Every number belongs to one of the three; if not, cut it.
- **Reading the two together closes the operator loop.** Weekly catches leading drift; monthly measures lagging consequence; the priority-and-focus cycle iterates each month.
