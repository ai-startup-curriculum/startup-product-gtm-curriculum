# Shipping the PMF Scorecard

## Motivation

Six chapters of survey design, cohort analysis, iteration engines, and failure-mode routing produce a lot of paper. **The deliverable is not the paper.** The deliverable is a single-page **PMF scorecard** that a founder, a co-founder, a first hire, an investor, or the founder-two-weeks-from-now can read in five minutes and act on.

The scorecard is a **decision document**, not a research report. It compresses the survey run, the cohort retention read, the main-benefit statement, the top blocker cohort, the failure-mode diagnosis, and the single next-iteration hypothesis into one page. Everything else in the module is raw material for this page.

This chapter names the shape, the length, and the evidence bar.

## Core concepts

### What the scorecard must contain

The PMF scorecard is one document with six sections. Do not add more; do not skip any.

1. **Header.** Startup name, date, author, version. The scorecard has a shelf life; the header is what tells the reader whether it is still current.
2. **Sean Ellis result.** The aggregate score, then the segment split (always both). The very-disappointed % per segment, with n's, and the working PMF zone (from Chapter 3's four-zone table).
3. **Retention curve.** One chart of segmented cohort retention (Chapter 4). At minimum: the top segment, the bottom segment, and the aggregate. Cadence (DAU/WAU/MAU) and "active" definition named.
4. **Main-benefit statement.** The modal main-benefit language from the very-disappointed cohort's free-text (Chapter 5, Step 1). One sentence in the users' words — not the founder's marketing draft.
5. **Top blocker cohort + top blockers.** The three highest-frequency blockers from the in-ICP somewhat-disappointed cohort (Chapter 5, Step 3), with citation counts.
6. **Failure-mode verdict + next-iteration hypothesis.** Which of the four modes (Chapter 6) fires per segment, and a single **falsifiable next-iteration hypothesis** in the *we believe X / we would know we are wrong if Y / next action Z* form.

Every claim is either a number sourced from the survey / cohort read or a quote from the free-text. No unsourced assertion appears anywhere.

### Length and tone

- **Total length: one page — two at maximum.** If it does not fit, cut. The scorecard is not the appendix; the appendix links out to the survey CSV, the cohort chart underlying the summary, and the raw free-text.
- **Opinionated, not neutral.** "Mid-market has PMF at 56% VD with 70% W12 retention; enterprise fails mode 2; small-teams fail mode 1" is a claim. Write claims.
- **Cite the data, not the founder's intuition.** Every number has a source (survey CSV path, cohort chart export). Every free-text quote has a respondent ID.
- **Segmented, not aggregated.** The aggregate goes at the top for context; the operating claims are per-segment. This is the enforced version of Chapters 3 and 4's "segment first" rule.

### The failure-mode verdict — the section most founders soften

Chapter 6's failure-mode diagnostic is the sharpest part of the scorecard, and the section founders instinctively soften into vague "we're still finding our way" prose. Do not do this.

For each segment where the diagnostic tree fires a mode, name it explicitly:

- Mid-market → **no mode fires, PMF in this segment** (per Chapter 6 Q1 = yes).
- Small teams → **mode 1 (wrong market)** — route to mod-101 or deprioritise.
- Enterprise → **mode 2 (wrong product for this segment)** — route to mod-101 re-audit + Chapter 5 engine after enterprise-specific features ship.

Each verdict is one line. Each names the mode and the routing module. A first hire, an investor, or a co-founder reading the scorecard should be able to say *"okay, so we double down on mid-market, deprioritise small teams, park enterprise"* — because the scorecard names those decisions in three lines.

### The next-iteration hypothesis — what makes this a decision document

The last section is the whole point. Everything above justifies this one hypothesis.

The shape (borrowed from mod-101 Chapter 7's discovery-report hypothesis format, adapted for PMF):

> **Hypothesis:** [we believe X will move the mid-market VD score from 56% → 62% next quarter].
> **How we would know we are wrong:** [next quarter's re-survey shows mid-market VD score flat or declining].
> **Next action:** [ship the three main-benefit-hardening features from the Chapter 5 Step 2 audit + unblock top-three somewhat-disappointed blockers by end of quarter].

One hypothesis per scorecard. Ideally the highest-leverage one — the one that, if wrong, would most change the roadmap. Two or three is a memo; one is a decision.

### The scorecard is dated, is signed, and is versioned

Reused from mod-101 Chapter 7 because the discipline is identical:

- **Dated.** Put the date at the top. A PMF scorecard from twelve months ago is a historical document, not a decision document. Chapter 1's system-state framing is why.
- **Signed.** Put the author's name at the top. PMF diagnoses are opinionated; the reader needs to know whose diagnosis they are reading.
- **Versioned.** When you re-run the survey (quarterly per Chapter 5), write it as v2 and preserve v1. **The delta between versions is the engine's output.** A team without version history has no way to tell whether their iterations are moving the needle.

### The one-page scorecard template

A minimal template you can adapt. Keep to this shape; add nothing.

```
PMF Scorecard — [Startup name]
Author: [Founder]. Version [N]. Date: [YYYY-MM-DD].
Prior versions: [v1: 2026-05-15, v2: 2026-08-15, ...]

1. SEAN ELLIS RESULT
   Aggregate: [N]% very-disappointed (n = [N_total responses])
   Sample filter: [active-user definition, e.g. "≥2 sessions in past 14d"]
   Segment split:
   - [Segment A]: [N]% VD (n=[N]) [zone: strong-PMF / working-PMF / approaching / pre-PMF]
   - [Segment B]: [N]% VD (n=[N]) [zone: ...]
   - [Segment C]: [N]% VD (n=[N]) [zone: ...]

2. RETENTION CURVE
   Cadence: [DAU / WAU / MAU]
   "Active" defined as: [the specific action]
   [Chart or ASCII sparkline per segment; W0 / W1 / W4 / W12 marked]
   Verdict: [Segment A flattens at N%; Segment B decays; ...]

3. MAIN-BENEFIT STATEMENT (very-disappointed cohort, modal)
   "[Users' modal wording of the benefit — one sentence, in their words]"
   Convergence: [X of Y very-disappointed users used this framing]

4. TOP BLOCKER COHORT + TOP BLOCKERS
   Cohort: in-ICP somewhat-disappointed (n=[N] of [total SD])
   Top blockers (by mention count):
     1. [Blocker 1] — cited [N] times
     2. [Blocker 2] — cited [N] times
     3. [Blocker 3] — cited [N] times

5. FAILURE-MODE VERDICT (per segment)
   - [Segment A]: [Mode N / no mode fires] — route: [module]
   - [Segment B]: [Mode N] — route: [module]
   - [Segment C]: [Mode N] — route: [module]

6. NEXT-ITERATION HYPOTHESIS
   We believe: [X]
   We would know we are wrong if: [Y]
   Next action: [Z, with owner and date]

APPENDIX (linked)
   - Raw survey CSV: [link]
   - Cohort retention chart export: [link]
   - Free-text quotes (redacted): [link]
```

That is the whole scorecard. One page filled cleanly conveys more decision-value than any 30-page PMF strategy deck.

### How the scorecard feeds forward

The scorecard is the input to five downstream modules and one project of this track:

- **[mod-103](../mod-103-positioning-and-messaging)** takes the **main-benefit statement** as the value component of the Dunford five-component positioning frame. Positioning that contradicts the surveyed main benefit is founder invention.
- **[mod-104](../mod-104-icp-and-buyer-personas)** takes the **top-scoring segment definition** as the ICP seed and the **low-scoring segments** as ICP disqualifiers.
- **[mod-106](../mod-106-pricing-and-packaging)** picks up any **mode-4 (wrong price)** diagnosis and runs the WTP research to fix it.
- **[mod-108](../mod-108-demand-generation-and-channels)** picks up any **mode-3 (wrong distribution)** diagnosis and runs channel-market fit.
- **[mod-109](../mod-109-retention-expansion-and-growth-loops)** deepens the retention read once PMF is established — this module teaches the *diagnostic* read, mod-109 teaches the *durability* read.
- **[`project-103-pmf-and-retention-scorecard`](../../projects/project-103-pmf-and-retention-scorecard)** takes the scorecard as its seed artifact.

If the scorecard is thin, all five downstream artifacts inherit the thinness. That is why the evidence bar in this chapter is high.

## Concrete example — a full scorecard for the code-review-tool

Assembled from Chapters 3–6:

```
PMF Scorecard — Reviewer.io (working name)
Author: Alex Reyes. Version 2. Date: 2026-08-21.
Prior versions: v1 (2026-05-15).

1. SEAN ELLIS RESULT
   Aggregate: 25% very-disappointed (n=89, response rate 26% on 340 active)
   Sample filter: teams that acted on ≥1 auto-nudge in past 14 days
   Segment split:
   - Mid-market (50-200 eng, distributed): 56% VD (n=27) [strong-PMF zone]
   - Small teams (<20 eng): 13% VD (n=30) [pre-PMF zone]
   - Enterprise (500+ eng, single-BU pilot): 9% VD (n=32) [pre-PMF zone]

2. RETENTION CURVE
   Cadence: WAU
   "Active" defined as: team acted on >=1 auto-nudge or reassignment that week
   Mid-market:  W0=100 W1=88 W2=82 W3=78 W4=75 W8=71 W12=70  [flattens at ~70%]
   Small teams: W0=100 W1=45 W2=26 W3=14 W4=8  W8=2  W12=1   [decays to zero]
   Enterprise:  W0=100 W1=92 W2=88 W3=75 W4=50 W8=25 W12=18  [pilot-then-decay]

3. MAIN-BENEFIT STATEMENT (very-disappointed cohort, modal)
   "Finally know exactly who to nudge on a stale review without becoming the nag."
   Convergence: 11 of 15 very-disappointed mid-market free-texts used this framing;
                7 of 15 also cited "seeing which reviews are stalled at a glance".

4. TOP BLOCKER COHORT + TOP BLOCKERS
   Cohort: in-ICP (mid-market) somewhat-disappointed users (n=18 of 30 SD)
   Top blockers:
     1. GitHub Enterprise Server support — cited 9 times
     2. Per-team ownership rules (currently global) — cited 7 times
     3. Digest volume too high (default one Slack ping per stale PR) — cited 6 times

5. FAILURE-MODE VERDICT (per segment)
   - Mid-market: no mode fires, PMF holds — route: strengthen via Chapter 5 engine;
                 check Chapter 6 Q2 (only 27 actives) — likely mod-108 channel work next.
   - Small teams: Mode 1 (wrong market) — route: deprioritise; do not spend more mod-101
                 discovery cycles here unless a specific sub-segment hypothesis surfaces.
   - Enterprise: Mode 2 (wrong product for this segment) — route: mod-101 re-audit against
                 enterprise JTBD outcomes; park motion (mod-107) until enterprise-specific
                 features ship.

6. NEXT-ITERATION HYPOTHESIS
   We believe: shipping (a) per-team ownership rules, (b) reduced-noise digest defaults,
     and (c) GitHub Enterprise support this quarter will move mid-market VD from 56% -> 65%
     by the next quarterly survey, driven by conversion of the 18 in-ICP somewhat-
     disappointed users into very-disappointed.
   We would know we are wrong if: mid-market VD is flat or declining at the next survey,
     OR the somewhat-disappointed cohort's blocker list at next survey is the same three
     items (i.e. we shipped them but they did not perceptibly clear the blockers).
   Next action: PM to sequence the three features into the next-quarter roadmap
     (owner: Alex, due: 2026-09-01); re-run survey against same active filter on
     2026-11-15.

APPENDIX (linked)
   - Raw survey CSV: /pmf/2026-Q3/survey-responses.csv
   - Cohort retention chart export: /pmf/2026-Q3/retention-by-segment.png
   - Free-text quotes (redacted): /pmf/2026-Q3/free-text-redacted.md
```

One page. Every number is sourced. The three routing decisions are legible in the second half. The next-iteration hypothesis is falsifiable. A first hire reading this on their first day knows: mid-market is the ICP, small teams are anti-ICP, enterprise is parked, and the three features being built this quarter are answering the top blocker list — not the founder's taste.

## Common failure patterns

- **The scorecard is a slide deck.** Slides let you elide claims. A one-page memo forces you to write them. Save the deck for board updates and fundraising narratives (mod-103); ship a memo here.
- **Aggregate only.** No segment split hides both the win and the loss. Chapter 3 said this; Chapter 4 said it; Chapter 6 said it; this chapter says it again.
- **Vague failure-mode verdicts.** "We're still finding fit" is not a verdict. Name Mode 1/2/3/4 or "no mode fires" per segment.
- **Hypotheses that are not falsifiable.** "We believe the product will resonate more next quarter" is not a hypothesis. "We believe mid-market VD will move from 56% to 65% by 2026-11-15" is.
- **Free-text paraphrased into founder-marketing language.** The main-benefit statement must be in the *users' words*. Paraphrasing loses the positioning signal and lets the founder unconsciously back-fit the message.
- **No version comparison.** v2 published without a v1 delta hides whether the engine is moving the needle. Always include the prior scorecard's number for the same segment.
- **Thirty pages.** No one reads it. Cut.

## Summary

- The PMF scorecard is the module's ship deliverable. **One page, six sections, dated, signed, versioned.**
- Six sections: **Sean Ellis result (segmented), retention curve (segmented), main-benefit statement (very-disappointed cohort, in their words), top blockers (in-ICP somewhat-disappointed cohort), failure-mode verdict per segment, one falsifiable next-iteration hypothesis.**
- Every claim cites the underlying data (survey CSV, cohort export, free-text quote).
- **Segmented, always** — aggregate scores are context, not conclusions.
- The failure-mode verdict determines the next module. Naming the mode is the whole payoff.
- The scorecard is the input to five downstream modules and one project. Thin scorecard → thin everything downstream. Version-diff every re-run.
