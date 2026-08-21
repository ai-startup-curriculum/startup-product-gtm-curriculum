# Shipping the GTM One-Pager + 12-Month First-Hire Staging Plan

## Motivation

Chapters 1–6 produce two artifacts: **a GTM one-pager** (weekly + monthly, from Chapter 5) and **a first-hire staging plan** (12-month, from Chapter 6). This chapter fixes the *ship discipline* — the shape of the final deliverable, the versioning and dating and signing convention, the board-pack extension, and the falsifiable-priority discipline that makes both artifacts operational rather than decorative.

The deliverable is not a research report; it is a **decision document**. It compresses six chapters of definitional work, benchmark reads, cadence discipline, and hire-trigger logic into two artifacts a founder, a GTM lead, an incoming VP GTM, a board member, or a Series-B underwriter can read in fifteen minutes and act on. Everything else in the module is raw material for these two.

This chapter mirrors the [mod-102 Chapter 7](../mod-102-pmf-signal-and-measurement/) and [mod-109 Chapter 7](../mod-109-retention-expansion-and-growth-loops/07-retention-expansion-scorecard.md) scorecard discipline — same evidence bar, same length constraint, same versioning discipline. Reuse the shape; adapt the content.

## Core concepts

### What the ship deliverable contains

The mod-110 ship deliverable is **two artifacts, both dated, signed, and versioned**:

- **Artifact A — The GTM operator one-pager.** Two versions of the same document: a **weekly** version (leading indicators) and a **monthly** version (lagging indicators + composite ratios + retention). Both authored to the Chapter 5 template. The current-week weekly + the most recent monthly are the "ship" state.
- **Artifact B — The 12-month first-hire staging plan.** Authored to the Chapter 6 discipline — sequential hires with per-hire trigger criteria, current-state readouts, explicit "not yet" calls, and review cadence. Covers the coming 12 months (four quarters), with the specific numerical triggers that route the plan.

**Both artifacts share a common evidence base** — the same one-pager numbers that drive the weekly and monthly reads are the same numbers that drive the trigger criteria in the staging plan. This is deliberate: the one-pager is the *instrument* that reads the numbers; the staging plan is the *decision* the instrument routes to.

**Length constraint:** one page (each) — two at maximum. The board-pack extension can run to three pages for the quarterly variant. Anything longer means you have written a report, not a decision document. Cut.

### Reuse the Chapter 5 templates verbatim

The weekly one-pager template and the monthly one-pager template from Chapter 5 are the ship shape. Nothing to re-invent here. The one thing this chapter adds to the template discipline:

- **Prior-versions header line.** Under the "Author" line, name the last N versions with dates. This makes version-over-version comparison legible at a glance.
- **Sourcing footer.** At the bottom of each one-pager, name the systems of record every number comes from. A single line: *"CAC / spend from HubSpot + payroll + ad platforms; ARR from Stripe; retention from Amplitude cohort tables; funnel conversion from HubSpot; benchmarks from OpenView 2026 SaaS Benchmarks + KeyBanc SaaS Survey 2026."* Enables the fast defensibility check.

### The staging-plan template

The Chapter 6 staging-plan example fixed the working shape. Reproduced here as a template:

```
GTM FIRST-HIRE STAGING PLAN — [Startup name]
Author: [Founder / GTM Lead]. Version [N]. Date: [YYYY-MM-DD]
Prior versions: [v1: 2026-Q1, v2: 2026-Q2, ...]
Plan horizon: [YYYY-QN through YYYY-QN] (12 months)

CURRENT GTM ORG (as of [date])
   [Name] — [role] — hired [date], ramped [date]
   [...]

CURRENT ONE-PAGER SIGNAL (from monthly one-pager v[N], date):
   AE quota attainment: [X]% (T3M: [+/-])
   Pipeline coverage: [X]x vs. required [Y]x
   Blended CAC: $[X] (T3M: [+/-])
   Magic number: [X.X]
   Funnel constraint: [top-of-funnel volume / stage conversion / other]

HIRE #1 — [Role]. Target date: [YYYY-QN]
   Trigger criteria:
     [ ] [Specific numerical trigger 1 from the one-pager]
     [ ] [Specific artifact-completion trigger from mod-105 / mod-107 / etc.]
     [ ] [Specific ICP / motion pre-condition]
   Current state:
     [Per-criterion: met / not met / partially met]
   If not met: [what has to change and by when]
   Review cadence: [monthly / quarterly]
   Which — [if a fork, e.g. PMM vs DG]: [signal-based choice logic]

HIRE #2 — [Role]. Target date: [YYYY-QN]
   [Same structure]

HIRE #3 — [Role]. Target date: [YYYY-QN]
   [Same structure]

HIRE #4 — [Role]. Target date: [YYYY-QN or "contingent on Hire #N"]
   [Same structure]

EXPLICIT DEFERRALS (things NOT on the plan and why):
   VP Sales — [why deferred; what would trigger reconsideration]
   RevOps — [why deferred; trigger]
   Sales Enablement — [why deferred; trigger]
   [Other roles the founder has been pressured to hire]

BOARD NARRATIVE (one paragraph):
   [The plan's total 12-month fully-loaded GTM spend]
   [The alternative "hire faster" plan the board might suggest and its spend]
   [The specific reason the recommended plan is more defensible]

APPENDIX
   - Current monthly one-pager: [link]
   - Current weekly one-pager: [link]
   - Prior staging plan versions: [links]
   - Underlying mod-102 PMF scorecard: [link]
   - Underlying mod-109 retention scorecard: [link]
```

The staging plan is versioned quarterly. Preserve prior versions; the delta is the operational output — did Hire #1 land as planned? Did the trigger criteria for Hire #2 land? What changed since v(n-1)?

### The board-pack GTM section

The quarterly board pack is not a new artifact. It is:

- **The monthly one-pager** (trailing three months compressed into a trend view).
- **The staging plan** (current version, with quarter-over-quarter delta noted).
- **A short narrative** — one paragraph per operator question (Chapter 1: working / efficient / ready to scale) plus one paragraph on the hire plan (what happened last quarter, what's next).

Total board-pack GTM section: 3 pages, published one week ahead of the board meeting, no new data collection. If you cannot assemble it from the monthly one-pagers and the staging plan without new work, the underlying monthly discipline slipped.

The exercise `exercise-06-board-pack-gtm-section-drill.md` fleshes this out.

### The falsifiable-priority discipline

Every ship of the monthly one-pager ends with **one falsifiable priority** for the coming month. Every ship of the staging plan ends with **one falsifiable hire trigger** or **one falsifiable "not yet" review**. A "falsifiable" priority or trigger means:

- **Specific.** Not "improve conversion"; "recover Demo → Proposal to ≥40% by end of month."
- **Numerical or artifact-based.** A number that has to move, or an artifact that has to exist by a date.
- **Owned.** A specific person, not "the team."
- **Time-bound.** By a specific date.
- **Checkable at the next ship.** The next month's one-pager will report whether the priority landed or did not.

The whole point of the one-page constraint is that the priority is not buried. **A priority nobody remembers is a priority nobody delivered.** The falsifiable discipline is what turns the one-pager from a status report into an operating loop.

### The date, signature, and version discipline

Same three items as mod-102 Chapter 7 and mod-109 Chapter 7:

- **Dated.** Every one-pager and every version of the staging plan has a date at the top. A weekly one-pager from three weeks ago is a historical document.
- **Signed.** The author is named. The one-pager and the staging plan are opinionated; the reader needs to know whose read they are absorbing. For a two-person GTM team it is the founder; for a larger team it is the founder plus the GTM lead (both named).
- **Versioned.** The weekly ships weekly; the monthly ships monthly; the staging plan ships quarterly. Preserve prior versions in a persistent location (an internal wiki, a Notion or Confluence page, a company file drive). The delta between versions is the operating engine's output.

### The full-ship checklist

Before publishing any of the three artifacts, run the checklist:

**Weekly one-pager:**
- [ ] Dated, signed.
- [ ] All five sections filled (activity, pipeline creation, pipeline health, forecast, one focus).
- [ ] Every number traces to a system of record (a hostile question has a same-day answer).
- [ ] "One focus" line is specific, numerical / artifact-based, owned, time-bound.
- [ ] No lagging indicators (CAC, retention, LTV) — those are on the monthly.

**Monthly one-pager:**
- [ ] Dated, signed, prior versions listed.
- [ ] All seven sections filled (revenue, CAC, LTV/payback/LTV/CAC, efficiency ratios, retention, funnel conversion, headline + priority).
- [ ] CAC decomposed per-channel; LTV and LTV/CAC decomposed per-channel; retention decomposed per-segment.
- [ ] Every number cites a source; benchmarks call out the specific band and motion type.
- [ ] Headline read answers the three operator questions from Chapter 1.
- [ ] "One priority" line is specific, numerical, owned, time-bound.
- [ ] No fundraising-view intrusion (multi-year LTV, payback sensitivity, projected runway model).

**Staging plan:**
- [ ] Dated, signed, prior versions listed.
- [ ] Current GTM org and current one-pager signal named at the top.
- [ ] Every hire has trigger criteria (specific and checkable), current-state readouts, and a review cadence.
- [ ] At least one hire is a "not yet" call with explicit deferral criteria.
- [ ] Explicit deferrals section names the roles the founder has been pressured to hire and why they defer.
- [ ] Board narrative names the recommended plan's spend and the alternative "hire faster" spend, and defends the recommendation on the numbers.

### How the ship deliverable feeds `project-103`

The mod-110 GTM one-pager and staging plan are two of the anchor artifacts for [`project-103-pmf-and-retention-scorecard`](../../projects/project-103-pmf-and-retention-scorecard). The project integrates:

- The mod-102 PMF scorecard (from mod-102 Chapter 7).
- The mod-109 retention + expansion scorecard (from mod-109 Chapter 7).
- **The mod-110 GTM operator one-pager** (from this chapter).
- **The mod-110 first-hire staging plan** (from this chapter).
- The mod-106 pricing pack.

Plus a board-facing narrative that ties the five artifacts to a single operating and fundraising story. If any of the five is thin, the project is thin; the evidence bar has to hold across all of them.

## Concrete example — the code-review-tool ship deliverable

Two artifacts, dated 2026-08-21 (matching the mod-109 scorecard's date so all artifacts are same-week).

### Artifact A — Monthly one-pager (July 2026, published 2026-08-03)

*(The full template with the code-review-tool's numbers. Reproduced from Chapter 5's example — the shape is fixed; the ship discipline is that the artifact is dated, signed, prior-versions listed, and sourced.)*

```
GTM MONTHLY — Reviewer.io — July 2026
Author: Alex Reyes (Founder / CEO). Version 7.
Prior versions: v6-Jun-2026, v5-May-2026, v4-Apr-2026, v3-Mar-2026, v2-Feb-2026, v1-Jan-2026.

[Sections 1-7 per Chapter 5 template, with July numbers reflecting the paid-channel
 audit having concluded and paid spend having been capped at Q1 levels.]

7. HEADLINE READ + ONE PRIORITY FOR AUGUST
   Paid-channel defund executed 2026-07-08 per prior priority; per-channel CAC
   for July shows blended CAC at $8,940 (down from $10,551 in June); magic
   number recovered to 2.9. Funnel Demo -> Proposal recovered from 32% to 41%
   (still below 45% baseline, but trending back). AE Priya on track for
   ~100% of Q3 quota. Motion is producing efficiently on the fit-holding
   channels; the "ready to scale" question is answered by Priya's Q3 landing.

   ONE PRIORITY FOR AUGUST: Complete mod-107 sales playbook documentation to
     first-AE-transferability standard (discovery script, demo checklist,
     proposal template, competitive teardown, objection handling).
     Owner: Priya + Alex. Success: playbook published in company wiki by
     2026-08-31, reviewed with Priya in weekly 1:1 through August.

Systems of record: CAC / spend from HubSpot + payroll + ad platforms;
                    ARR from Stripe; retention from Amplitude cohort tables;
                    funnel conversion from HubSpot; benchmarks from
                    OpenView 2026 Expansion SaaS Benchmarks.
```

### Artifact B — 12-month first-hire staging plan (v3, 2026-08-21)

```
GTM FIRST-HIRE STAGING PLAN — Reviewer.io
Author: Alex Reyes (Founder / CEO). Version 3. Date: 2026-08-21.
Prior versions: v1-2026-01 (post-Series-A), v2-2026-05.
Plan horizon: 2026-Q3 through 2027-Q2.

CURRENT GTM ORG (as of 2026-08-21):
   Alex Reyes — Founder / CEO (~50% selling)
   Priya Menon — First AE (hired 2026-Q1, ramped 2026-Q2, Q3 forecast ~100%)
   Jordan Kim — Head of CS (hired 2026-Q1, owns mod-109 retention motion)
   Sam Chen — Marketing Manager (hired 2025-Q4, covers content/paid/events)

CURRENT ONE-PAGER SIGNAL (from July 2026 monthly, v7):
   AE quota attainment: 82% (Q2) -> 95-105% (Q3 forecast); +T3M
   Pipeline coverage: 3.5x vs. required 6.4x (short)
   Blended CAC: $8,940 (July; down from $10,551 in June post-defund)
   Magic number: 2.9 (recovered from 2.6 in June)
   Funnel constraint: top-of-funnel volume (coverage short, not conversion)

HIRE #1 — First Demand-Gen Lead. Target date: 2026-Q4.
   Trigger criteria:
     [ ] Priya at >=100% of Q3 quota (currently forecast; land or defer to Q1)
     [x] One-pager signal is top-of-funnel volume (met — coverage 3.5x vs. 6.4x)
     [x] Paid channel decision executed (met — defunded 2026-07-08)
     [x] mod-108 Chapter 2 channel-market-fit audit complete (met — concluded 2026-07)
   Current state: 1 of 4 criteria pending (Q3 quota).
   If not met (Q3 comes in <90%): defer to 2027-Q1; re-read after Q4 lands.
   Which — DG or PMM: DG (signal is volume, not conversion).
   Review cadence: monthly against one-pager; hire decision in October.

HIRE #2 — Second AE. Target date: 2027-Q1 (earliest).
   Trigger criteria:
     [ ] Priya at >=100% of quota for 2 consecutive quarters (Q3 + Q4)
     [ ] DG hire loading pipeline coverage to >=5x
     [ ] mod-107 playbook documented to first-AE-transferability standard
         (in flight — August priority)
     [ ] Written 60/90/120-day ramp plan calibrated against Priya's ramp
   Current state: 0 of 4 fully met (playbook in flight per August priority).
   If not met: defer to 2027-Q2; the plan does not scale AE headcount on
     a single-quarter attainment signal.
   Review cadence: quarterly; decision in January 2027.

HIRE #3 — First PMM. Target date: 2027-Q2 or later ("not yet").
   Trigger criteria:
     [ ] Volume constraint solved by DG hire (pipeline coverage healthy)
     [ ] Conversion constraint emerging (systematic Discovery/Demo/Proposal drop)
     [ ] Positioning gap in win-loss (mod-103 signals)
   Current state: none met; no systematic conversion constraint; no
     positioning gap in win-loss (competitor losses are motion-execution,
     not positioning).
   If not met: defer indefinitely; re-read quarterly after DG hire lands.
   Review cadence: quarterly.

HIRE #4 — Third AE + First SDR. Target date: 2027-Q3 or later ("not yet").
   Trigger criteria:
     [ ] Second AE ramped and at quota
     [ ] Founder still bottlenecked on close
     [ ] SDR is coupled to Second AE (feeds them, not the first)
   Current state: contingent on Hire #2.
   Review cadence: after Hire #2's first quarter.

EXPLICIT DEFERRALS (things NOT on the plan):
   VP Sales — Deferred indefinitely. Trigger: >=3 AEs each at quota for >=2
     consecutive quarters; motion documented; founder time on hiring / coaching
     >20h/wk. None of these will land within 18 months.
   RevOps hire — Deferred to 2027-Q2 at earliest, contingent on Second AE
     landing (tooling / process complexity threshold not yet met).
   Sales Enablement — Deferred to 2027-Q3+ contingent on Second AE's
     onboarding producing enough operational learning to codify.

BOARD NARRATIVE:
   The plan spends approximately $195k in fully-loaded GTM salary over the
   coming 12 months (one DG hire in Q4 2026, contingent on Priya's Q3
   attainment landing). The alternative "hire faster" plan some board
   members have suggested — hiring a VP Sales and a second AE and two SDRs
   in Q4 2026 — would spend approximately $920k in fully-loaded GTM salary
   against a motion that has not yet demonstrated it can support a second
   AE (per the one-pager). The recommended plan defers the additional spend
   until the trigger criteria are met, and reads them monthly from the
   operator one-pager. The specific numeric bet: at 2.9 magic number and
   ~100% Priya attainment, the current motion produces ~$1.7M net-new ARR
   this year with the recommended spend; the alternative "hire faster"
   plan would need to produce ~$3.5M net-new ARR to be breakeven at
   equivalent magic-number, and the funnel-loading constraint (3.5x
   coverage) makes this arithmetically unavailable.

APPENDIX
   - Current monthly one-pager (July 2026, v7): /gtm/monthly/2026-07.md
   - Current weekly one-pager (week of 2026-08-18, v34): /gtm/weekly/2026-w34.md
   - Prior staging plan versions: /gtm/staging/{v1,v2}.md
   - Underlying mod-102 PMF scorecard: /pmf/scorecard-2026-08.md
   - Underlying mod-109 retention scorecard: /retention/scorecard-2026-08.md
   - mod-107 sales playbook (in flight): /sales/playbook-2026-08.md
```

**Two artifacts. Both dated. Both signed. Both versioned. Both sourced. Both operational.** A hostile board question on any hire trigger or one-pager number has a same-day answer. The board narrative is defensible against a hire-faster pressure because every deferral is tied to a specific numerical trigger visible on the one-pager the board already sees.

## Common failure patterns

- **A single dashboard replacing both artifacts.** Weekly and monthly are two cadences. The staging plan is a third artifact. Three documents.
- **Ship without prior-versions list.** Delta over time is the operating signal. Preserve prior versions.
- **Ship without systems-of-record footer.** A hostile question has to have a same-day answer. Cite the sources.
- **"One priority" that is not falsifiable.** "Improve efficiency" is not a priority; "recover Demo → Proposal to ≥40% by 2026-08-31, owner Priya" is.
- **Staging plan with only affirmative hires.** The "not yet" and "explicit deferrals" sections are load-bearing. A plan without them is the over-hire trap in written form.
- **Board pack assembled from scratch.** If you did that, the monthly discipline slipped. The board pack is the trailing three monthlies plus the current staging plan; no new work.
- **Fundraising-view intrusion in the operator one-pager.** Multi-year LTV, payback sensitivity, projected runway — all belong in the fundraising view. Chapter 1's boundary; Chapter 5's template enforces.
- **Retention numbers on the mod-110 one-pager that do not reconcile to the mod-109 scorecard.** Both are the same data; if the numbers do not agree, the metric-integrity discipline slipped somewhere.
- **Aggregate-only per-channel and per-segment cuts.** Chapter 2 argued this for CAC; Chapter 3 for LTV/CAC; Chapter 5 for the one-pager; Chapter 6 for the trigger criteria; Chapter 7 enforces. Segment.

## Summary

- **Two artifacts ship from this module.** The GTM operator one-pager (weekly + monthly) and the 12-month first-hire staging plan.
- **Both are dated, signed, versioned, sourced.** Preserve prior versions; the delta is the operating output.
- **Weekly one-pager: leading indicators, published Monday, 5-minute read, ends with one falsifiable focus.**
- **Monthly one-pager: lagging indicators + composite ratios + retention, published on the 3rd, 10-minute read, ends with one falsifiable priority.**
- **Staging plan: 12-month horizon, per-hire trigger criteria + current-state + review cadence, explicit "not yet" section, board narrative.**
- **The board-pack GTM section is the monthly one-pager assembled into a trailing-3-month trend view plus the current staging plan.** No new data collection.
- **The falsifiable-priority discipline is what turns the artifacts from status reports into operating loops.** Specific, numerical, owned, time-bound, checkable next month.
- **The mod-110 ship deliverable feeds `project-103` as one of the anchor artifacts** alongside the mod-102 PMF scorecard, the mod-109 retention scorecard, and the mod-106 pricing pack.
- **The ship discipline enforces every prior chapter's boundaries.** Per-channel / per-segment decomposition; leading vs. lagging separation; no fundraising-view intrusion; every hire tied to a numerical trigger on the one-pager.
