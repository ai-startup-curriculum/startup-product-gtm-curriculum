# Shipping the Retention + Expansion Scorecard

## Motivation

Six chapters of cohort reads, NRR arithmetic, expansion motion design, loop diagnosis, activation programme design, and churn decomposition produce a lot of paper. **The deliverable is not the paper.** The deliverable is a single-page **retention + expansion scorecard** that a founder, a Head of CS, a Head of Growth, an incoming Series-B investor, or the founder two quarters from now can read in five minutes and act on.

The scorecard is a **decision document**, not a research report. It compresses the cohort retention read, the GRR and NRR numbers, the expansion motion definition, the loop diagnosis, the activation programme, and the churn programme into one page. Everything else in the module is raw material for this page.

This chapter mirrors the mod-102 Chapter 7 discipline (PMF scorecard) — same evidence bar, same length constraint, same versioning discipline. Reuse the shape; adapt the content.

## Core concepts

### What the scorecard must contain

The retention + expansion scorecard is one document with seven sections. Do not add more; do not skip any.

1. **Header.** Startup name, date, author, version. The scorecard has a shelf life; the header tells the reader whether it is still current.
2. **Cohort retention read.** Segmented cohort curves (Chapter 1). At minimum: the primary ICP segment, one other segment, and the cohort-over-cohort roll-up on the durability period (W12 or Mn). Cadence and "active" event named.
3. **GRR and NRR.** Both numbers (Chapter 2), decomposed by the four movements (new, expansion, downgrade, churn), and segmented by at least ARR tier and cohort year. Benchmark call-out.
4. **Expansion motion.** Primary primitive (seat / usage / cross-sell — Chapter 3), qualifying signals, playbooks, owner, and current-quarter Expansion ARR vs. plan.
5. **Growth loop diagnosis.** Which loop the product supports (Chapter 4), the loop metric measured on real data, and one line naming the loops the product *does not* support and why.
6. **Magic moment + activation programme.** The magic moment triple (Chapter 5), the retention lift, the current activation rate, and the activation programme's target for next quarter.
7. **Churn diagnosis.** Voluntary / involuntary split (Chapter 6), sub-reason decomposition, save-rate per bucket, and the specific in-flight remediation (dunning programme status, multi-threading playbook, activation re-diagnosis, etc.).

Every claim is either a number sourced from the product analytics / billing system / CRM or a quote from an exit-survey free-text. No unsourced assertion appears anywhere.

### Length and tone

- **Total length: one page — two at maximum.** If it does not fit, cut. The scorecard is not the appendix; the appendix links out to the cohort chart export, the billing-system CSV, the exit-survey free-text.
- **Opinionated, not neutral.** "NRR 110% clears the Series-A bar but GRR 78% is 12 points below the mid-market band, and expansion is compensating not compounding" is a claim. Write claims.
- **Cite the data, not the founder's intuition.** Every number has a source (product event query, billing system report, CRM view).
- **Segmented, not aggregated.** The aggregate goes at the top for context; the operating claims are per-segment. The mod-102 Chapter 4 "segment first" rule persists here.

### The one-page scorecard template

A minimal template you can adapt. Keep to this shape; add nothing.

```
RETENTION + EXPANSION SCORECARD — [Startup name]
Author: [Founder / Head of CS / Head of Growth]. Version [N]. Date: [YYYY-MM-DD].
Prior versions: [v1: 2026-05-15, v2: 2026-08-15, ...]

1. COHORT RETENTION READ
   Cadence: [DAU / WAU / MAU]
   "Active" defined as: [the specific value action]
   Segmentation: [ICP tier / acquisition channel / product version]
   [Chart or ASCII sparkline per segment; W12 (or Mn) marked]
   Cohort-over-cohort W12 trend (last 6 cohorts): [flat / drifting down / drifting up]
   Verdict: [Segment A floor holding at N%; Segment B drifting from N% to M%; ...]

2. GRR AND NRR
   Cohort locked at: [YYYY-MM-DD], Starting ARR: $[N]
   Movements (period):
     - Expansion ARR: $[N]
     - Downgrade ARR: $[N]
     - Churned ARR: $[N]
   GRR: [N]%  (benchmark for [ARR tier / motion]: [range])
   NRR: [N]%  (benchmark for [stage]: ≥ 100% at Series-A)
   Segment decomposition:
     - Enterprise: GRR [N]%, NRR [N]%
     - Mid-market: GRR [N]%, NRR [N]%
     - SMB: GRR [N]%, NRR [N]%
   Verdict: [one-sentence read — e.g. "NRR clears bar; GRR weak in SMB;
             expansion doing heavy lifting"]

3. EXPANSION MOTION
   Primary primitive: [seat / usage / cross-sell]
   Pricing metric constraint: [what the mod-106 metric enables and excludes]
   Qualifying signals: [list]
   Playbook: [in-product / CSM / AE cycle]
   Owner: [name + role]
   Current-quarter Expansion ARR: $[N] / $[N] plan ([N]% of plan)
   Secondary primitive (if any): [brief]

4. GROWTH LOOP DIAGNOSIS
   Primary loop: [viral / content / paid / sales-assisted / none]
     Loop metric: [K-factor / referenced-deal cycle time / etc.] = [value]
     Verdict: [working / partial / not net-productive]
   Secondary loop (if invested): [name + metric + verdict]
   Explicit non-loops: [which loops the product does not support and why]

5. MAGIC MOMENT + ACTIVATION PROGRAMME
   Magic moment: [action + count + window]
   Retention lift (W12): [N]× (crossed [N]% vs. did not cross [N]%)
   Activation rate (current cohort): [N]%
   Target next quarter: [N]%
   Programme components: [onboarding + empty-state + nudges + human-touch]
   Owner: [name + role]

6. CHURN DIAGNOSIS
   Period: [YYYY-MM to YYYY-MM]
   Total churned ARR: $[N] ([N] accounts)
   Involuntary: $[N] ([N] accounts), sub-reasons: [expired / declined / ...]
   Voluntary: $[N] ([N] accounts), sub-reasons: [competitor / champion / price / ...]
   Save-rate scorecard: [per-bucket rates vs. targets]
   In-flight remediation:
     - Dunning programme: [status + ship date]
     - [Other remediation]: [status + ship date]

7. HEADLINE VERDICT + ONE NEXT-QUARTER PRIORITY
   [One paragraph — is the retention motion durable, compensating, or leaking?
    Is the expansion motion producing? Which loop is the primary bet?
    What is the one investment that most changes the picture next quarter?]

APPENDIX (linked)
   - Cohort retention chart export: [link]
   - Billing-system GRR/NRR decomposition: [link]
   - Exit-survey free-text (redacted): [link]
   - Expansion pipeline CRM view: [link]
```

That is the whole scorecard. One page filled cleanly conveys more decision-value than any 40-page board deck.

### The scorecard is dated, is signed, and is versioned

Same discipline as mod-102 Chapter 7 (and mod-101 Chapter 7):

- **Dated.** Put the date at the top. A retention scorecard from twelve months ago is a historical document, not a decision document. Chapter 1's cohort-over-cohort drift is why.
- **Signed.** Put the author's name at the top. Retention diagnoses are opinionated; the reader needs to know whose diagnosis they are reading.
- **Versioned.** Re-run the scorecard **monthly** (not quarterly — retention drift moves faster than PMF drift, and the durability-instrument cadence is monthly). Preserve v(n-1) alongside v(n). **The delta between versions is the operating engine's output.**

### The headline verdict — the whole point

The last section is the point. Everything above is evidence in service of one paragraph that answers three questions:

- **Is the retention motion durable, compensating, or leaking?** Durable = GRR clears the segment band and cohort-over-cohort is flat. Compensating = NRR clears 100% but GRR is weak and expansion is masking. Leaking = both weak; motion is not investable at Series-A economics.
- **Is the expansion motion producing?** Yes with room to compound / yes but at plan / no.
- **Which loop is the primary bet?** Named, with the loop metric.

Followed by **one next-quarter priority** — the single investment that most changes the picture next quarter. Not a list of five; one. If you cannot pick one, the scorecard has not converged and you have not decoded the signal.

### How the scorecard feeds forward

The scorecard is the input to two downstream artifacts:

- **[mod-110](../mod-110-gtm-metrics-and-first-hires)** takes GRR, NRR, cohort retention, and the expansion vs. new-logo ARR split as core inputs to the GTM one-pager and the OpenView / SaaStr benchmark reads. It also takes the churn programme's sub-reason routing as input to the first-hire staging conversation (do we need a CS Ops hire? An expansion AE?).
- **[`project-103-pmf-and-retention-scorecard`](../../projects/project-103-pmf-and-retention-scorecard)** takes this scorecard as one of its three anchor artifacts (alongside the mod-102 PMF scorecard and the mod-110 GTM one-pager).

If the scorecard is thin, both downstream artifacts inherit the thinness. The evidence bar has to hold.

## Concrete example — the code-review-tool retention + expansion scorecard

Assembled from Chapters 1–6:

```
RETENTION + EXPANSION SCORECARD — Reviewer.io (working name)
Author: Alex Reyes (Founder / CEO). Version 4. Date: 2026-08-21.
Prior versions: v1 (2026-05), v2 (2026-06), v3 (2026-07).

1. COHORT RETENTION READ
   Cadence: WAU
   "Active" defined as: team acted on >=1 auto-nudge or reassignment that week
   Segmentation: ICP tier (mid-market / SMB / enterprise) + acquisition channel
   Mid-market outbound-acquired:  W0=100 W4=75 W12=72  (floor holding)
   Mid-market paid-acquired:      W0=100 W4=68 W12=58  (drift)
   Enterprise pilots:             W0=100 W4=50 W12=18  (pilot-then-decay)
   Cohort-over-cohort W12 trend (last 6 cohorts): drifting from 72% -> 62%,
     driven by mix shift toward paid channel (mod-108 Chapter 2 issue,
     not product regression).
   Verdict: Product-fit holds in outbound-acquired mid-market. Aggregate drift
     is a channel-mix problem; fix at mod-108 layer, not product layer.

2. GRR AND NRR
   Cohort locked at: 2025-01-01, Starting ARR: $2,160,000 (108 mid-market teams)
   Movements (YoY):
     - Expansion ARR: $700,000  (seat $580k + Premium Security cross-sell $120k)
     - Downgrade ARR: $180,000
     - Churned ARR:   $300,000
   GRR: 77.8%  (benchmark for mid-market: >=90% — WEAK, 12pt below band)
   NRR: 110.2% (benchmark for Series-A: >=100% — clears)
   Segment decomposition:
     - Mid-market outbound cohort: GRR 89%, NRR 118%
     - Mid-market paid cohort:     GRR 63%, NRR 92%
     - Enterprise pilots:          GRR 44%, NRR 44% (pilots decay)
   Verdict: Headline NRR clears the Series-A bar; GRR is weak because the paid
     cohort is bleeding. Expansion is compensating, not compounding, in the paid
     cohort. Outbound cohort compounds cleanly.

3. EXPANSION MOTION
   Primary primitive: seat expansion (per-user pricing metric enables)
   Pricing metric constraint: per-seat metric enables seat expansion; Premium
     Security tier enables cross-sell; no usage metric available (would require
     re-pricing — mod-106 conversation, not this quarter).
   Qualifying signals: seat-cap approaching 80%; teammate invited & activated
     >=3 days; mentions to non-users
   Playbook: in-product modal at seat cap for self-serve; CSM-assisted for
     enterprise-tier; AE (currently founder) for Premium Security cross-sell.
   Owner: Head of CS (seats) + Founder (cross-sell, transitioning to first
     Expansion AE hire in Q4).
   Current-quarter Expansion ARR: $180k / $220k plan (82% of plan)
   Secondary primitive: cross-sell to Premium Security (working, small)

4. GROWTH LOOP DIAGNOSIS
   Primary loop: sales-assisted (referenced-deal cycle time 42d vs. cold 78d;
     win rate 38% vs. 22%; 11 named-peer opportunities from 2 anchor customers
     in past 6 months). Working. Invest in formal reference programme and
     case-study production tied to expansion outcomes.
   Secondary loop: partial viral (K=0.4). Investable if admin-invite shifts to
     user-invite. One-sprint experiment queued for Q4.
   Explicit non-loops:
     - No content loop (users produce no indexable public artifacts; the
       marketing blog is editorial-produced, a paid loop in effect)
     - Paid loop is not net-productive at current economics (LTV/CAC 2.1x;
       payback 14mo; CAC drifted from $3.8k -> $4.9k as spend scaled). Do not
       scale until channel-market-fit fixed (mod-108 Chapter 2 audit in flight).

5. MAGIC MOMENT + ACTIVATION PROGRAMME
   Magic moment: team acts on >=3 auto-nudges in the first 7 days
   Retention lift (W12): 5.1x (crossed 71% vs. did not cross 14%)
   Activation rate (current cohort): 34%
   Target next quarter: 55%
   Programme components:
     - Scripted first-run: install one initial nudge rule; do not end onboarding
       until first nudge acted on
     - Empty-state: "Connect GitHub org + create first rule" affordance
     - Nudges: email at day 3 if 0 acted-on; in-product modal at day 5 if 1-2
     - Human-touch: CSM activation call within 3 days for enterprise-tier (>=200
       seats)
   Owner: Head of Product + Head of CS.

6. CHURN DIAGNOSIS
   Period: 2026-Q1
   Total churned ARR: $340k (12 accounts)
   Involuntary: $84k (6 accounts) — card expired 4, card declined 2
   Voluntary: $256k (6 accounts) — competitor won 2 ($88k), champion left 2
     ($76k), price 1 ($42k), onboarding failure 1 ($50k)
   Save-rate scorecard (current -> target):
     - Involuntary retry recovery: 0% -> 30% (need dunning programme)
     - Involuntary card update via email: 0% -> 40%
     - Involuntary CS call for accounts > $5k/mo: N/A -> 65%
     - Voluntary save call on competitor-mention: 0% -> 15%
   In-flight remediation:
     - Dunning programme (Stripe smart retry + card update flow + email cadence
       + card updater services + CS call for high-ACV). Owner: eng lead + Head
       of CS. Ship: 2026-09-30. Expected recovery: $34-50k ARR/quarter.
     - Multi-threading playbook (require second contact within 30d of signup).
       Owner: Head of CS. Ship: 2026-09-15.
     - Chapter 5 activation programme re-diagnosis on the onboarding-failure
       account. Owner: Head of Product. Ship: 2026-09-01.
     - Win-loss analysis on 2 competitor losses (Copilot, Graphite). Owner:
       Alex. Ship: 2026-08-30. Feeds mod-103 positioning re-audit.

7. HEADLINE VERDICT + ONE NEXT-QUARTER PRIORITY
   The retention motion is COMPENSATING, not compounding. NRR 110% clears the
   Series-A bar but is masked by strong expansion on a weak (77.8%) GRR floor,
   itself dragged down by paid-channel-acquired cohorts that do not retain
   at the outbound cohort's level. The expansion motion is producing at 82%
   of plan; the primary growth loop is sales-assisted and working; the magic
   moment is identified and the activation programme is designed. The single
   next-quarter priority is SHIP THE DUNNING PROGRAMME — it recovers an
   expected $34-50k ARR/quarter (roughly 4-5 GRR points) with fixed engineering
   cost, has no product-risk downside, and single-handedly moves GRR closer to
   the mid-market band. Second priority (Q1 2027): fix or defund the paid
   channel per mod-108 Chapter 2.

APPENDIX (linked)
   - Cohort retention chart export:      /retention/2026-08/cohorts-by-segment.png
   - GRR/NRR decomposition (billing):    /retention/2026-08/grr-nrr-decomp.csv
   - Exit-survey free-text (redacted):   /retention/2026-08/exit-survey.md
   - Expansion pipeline CRM view:        /crm/expansion-pipeline
   - Activation-rate cohort chart:       /activation/2026-08/activation-cohort.png
   - Dunning programme spec:             /eng/2026-Q3/dunning-spec.md
```

One page. Every number sourced. The three routing decisions (dunning ship, channel-market-fit audit, positioning re-audit) are legible in the second half. The next-quarter priority is falsifiable — either dunning ships and recovers the expected ARR or it does not. A Head of CS reading this on their first day knows: the outbound cohort compounds, the paid cohort bleeds, dunning is the highest-ROI ship this quarter, and the expansion motion needs a first Expansion AE hire by Q4.

## Common failure patterns

- **The scorecard is a 40-page board deck.** Slides let you elide claims. A one-page memo forces you to write them. Save the deck for the fundraise (mod-103 narrative work); ship a memo here.
- **NRR headline without GRR.** Chapter 2 said this; this chapter says it again. Report both.
- **Aggregate-only.** No segment split hides whether one cohort is compounding and another is decaying. Segment.
- **"Retention motion is healthy" without evidence.** The word "healthy" is not a claim. Cite the numbers.
- **Loop diagnosis with no loop metric.** Naming a loop is not a diagnosis. Measure K, or referenced-deal cycle time, or paid unit economics on real data.
- **Magic moment "we think it's X."** The magic moment is empirically derived (Chapter 5). Do not guess.
- **Churn as a single number.** Sub-reason decomposition is the whole point of Chapter 6.
- **No next-quarter priority.** Everything is a priority; therefore nothing is. Pick one.
- **No version comparison.** v4 published without a v3 delta hides whether the programme is moving the numbers. Preserve prior versions.

## Summary

- The retention + expansion scorecard is the module's ship deliverable. **One page, seven sections, dated, signed, versioned monthly.**
- Seven sections: **cohort retention read (segmented + cohort-over-cohort), GRR and NRR (both, decomposed and segmented), expansion motion (primary primitive + owner + Expansion ARR vs. plan), growth-loop diagnosis (with the loop metric on real data), magic moment + activation programme, churn diagnosis (voluntary / involuntary + save-rate + in-flight remediation), headline verdict + one next-quarter priority.**
- **Every claim cites the data.** Product analytics, billing system, CRM, exit-survey free-text.
- **Segmented, always.** Aggregate is context; per-segment is decision-relevant.
- **The headline verdict is opinionated.** Is the motion durable, compensating, or leaking? Is expansion producing? Which loop? One next-quarter priority.
- The scorecard feeds mod-110 and the project-103 anchor artifact set. Thin scorecard → thin downstream. Version-diff every re-run.
