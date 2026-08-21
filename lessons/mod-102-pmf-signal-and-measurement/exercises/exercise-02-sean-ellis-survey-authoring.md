# Exercise 02 — Sean Ellis Survey Authoring

**Estimated time:** 2 hours
**Chapter link:** [`03-sean-ellis-survey.md`](../03-sean-ellis-survey.md)
**Prerequisite reading:** [Sean Ellis — "Using Product/Market Fit to Drive Sustainable Growth" (2009, archived)](https://web.archive.org/web/20101025110359/http://startup-marketing.com/using-product-market-fit-to-drive-sustainable-growth/) (~15 min); [Rahul Vohra — "How Superhuman Built an Engine to Find Product/Market Fit"](https://review.firstround.com/how-superhuman-built-an-engine-to-find-product-market-fit/) (~30 min)

## Problem statement

The Sean Ellis survey is *the* portable PMF instrument. Its power depends on running it properly — right sample, right wording, right diagnostic follow-ups, right segmentation plan. This exercise makes you **author a real survey instrument end-to-end**, including the sample filter, the send plan, and the analysis plan, for a real startup — yours or a hypothetical one drawn from mod-101.

You will not run the survey (that's the lab). You will produce the instrument in a form a co-founder or first hire could deploy tomorrow without re-authoring anything.

## Requirements

Deliver a folder `exercise-02/` with:

- `survey-instrument.md` — the actual survey (questions, options, wording notes).
- `sample-plan.md` — sample filter, source-of-truth query, send mechanics.
- `analysis-plan.md` — the pre-registered analysis plan (segments, expected verdicts, decision boundaries).
- `pilot-invitation.md` — the recruitment email / in-product prompt that gets people to answer the survey.

### 1. Survey instrument — 30 minutes

Author `survey-instrument.md` with all five questions in the shape from Chapter 3. Do **not** paraphrase the primary question — use Ellis's exact wording.

- **Q1** (primary): "How would you feel if you could no longer use \[Product\]?" — with the four canonical options (Very disappointed / Somewhat disappointed / Not disappointed / N/A).
- **Q2** (diagnostic): "What type of people do you think would most benefit from \[Product\]?" — open text.
- **Q3** (diagnostic): "What is the main benefit you receive from \[Product\]?" — open text.
- **Q4** (diagnostic): "Have you recommended \[Product\] to anyone? If so, how did you describe it?" — open text.
- **Q5** (diagnostic): "How can we improve \[Product\] for you?" — open text.

Optionally include the sixth question: **"What would you likely use as an alternative if \[Product\] were no longer available?"**

For each question, in a note directly below it, explain in one sentence *what downstream artifact you plan to feed the answer into*: ICP (mod-104), positioning (mod-103), main-benefit hardening (Chapter 5), roadmap-blocker cohort (Chapter 5), competitive alternatives set (mod-103).

Include a set of **metadata fields** to append server-side so segmentation works:

- User role / title.
- Company size band.
- Industry / vertical.
- Tenure on product (days since activation).
- Plan / SKU.

Any others required for your specific segmentation plan.

### 2. Sample plan — 30 minutes

Author `sample-plan.md`:

- **Active-user definition.** State the exact activation event and the recency filter (e.g. "sent ≥1 message in past 14 days"). Justify why this event corresponds to "user experienced the product's value" per Chapter 3.
- **Exclusion rules.** Who *not* to survey (non-activated signups, churned users, users on plans where "could no longer use this" means something different, users who joined <7 days ago, etc.).
- **Source-of-truth query.** Pseudocode or SQL for the exact query that would produce the sample list from your product data (or the equivalent script against Amplitude / Mixpanel).
- **Target sample size.** Compute: what response rate do you expect, how many respondents do you need in the very-disappointed bucket (target ≥30), therefore how many people you need to survey. Show the math.
- **Send mechanics.** Email vs. in-product prompt vs. both; single-send vs. reminder cadence; timing (day of week / time of day) with a one-sentence rationale.

### 3. Analysis plan — 45 minutes

Author `analysis-plan.md`. This is **pre-registered** — you write down what verdicts you will draw *before* seeing the data, so you cannot rationalise after the fact.

- **Aggregate score bands.** Restate Chapter 3's four-zone table with your commitment for each: what will you do if aggregate lands in each band? (Note: aggregate is context, not decision — the decision is per-segment.)
- **Segments to split by.** List the segments you will slice by (minimum: two firmographic + one behavioural + tenure). For each segment, state:
  - The expected n range.
  - Whether the segment has enough n to draw a segment-level conclusion (rule of thumb: ≥15 responses total, ≥5 very-disappointed).
- **Per-segment decision boundaries.** For each planned segment: what score would fire the Chapter 6 failure-mode diagnostic tree for that segment, and what would each verdict route to? Write it as if the Chapter 6 tree were being executed.
- **Free-text coding plan.** How will you deduplicate and cluster free-text answers into the modal main-benefit statement (Chapter 5 Step 1)? Name the exact process (highlight, cluster into ≤5 buckets, count citations per bucket, name the modal one).
- **Falsification lines.** If the results contradict a Chapter 5 iteration hypothesis from a prior survey, what will you do? A pre-registered "we will not spin the results to fit our thesis" clause.

### 4. Pilot invitation — 15 minutes

Author `pilot-invitation.md`: the exact email or in-product prompt that will get users to open the survey. Constraints:

- Explain the ask ("we're trying to understand what you get from \[Product\]") without leading toward a specific answer.
- Bounded time ("2 minutes").
- Concrete return ("we use this to decide what we build next; happy to share a summary of what we learn").
- **Do not** promise a reward that would bias the sample (a $100 Amazon card skews toward respondents who want the card, not respondents who use the product).
- **Do not** cue the desired answer ("help us prove that our users love us").

Include the alternative in-product variant (a modal or banner) if you plan a dual-channel send.

## Starter guidance

- Chapter 3 is the operating manual. Every question, threshold, and sample rule in this exercise comes from that chapter.
- If you cannot pick a startup for this exercise, borrow the running code-review-tool example from the chapters — the chapter examples are complete enough to write the whole instrument against.
- The single most common execution error is **sampling all signups**. If your source-of-truth query does not have an activation filter, it is wrong; rewrite it.
- The pre-registered analysis plan is the anti-motivated-reasoning discipline. Once you have real data, motivated reasoning is very hard to resist. The plan is what protects the read.
- Free-text coding is where most survey runs fall apart. Commit to a specific process: read all answers, cluster into ≤5 buckets, count, name the modal bucket. Do not sub-cluster past 5 unless you have >100 responses; more clusters = less signal.
- Do not skip the metadata fields. Survey answers without segment metadata are aggregate-only and useless per Chapter 3.

## Acceptance criteria

Your submission is complete when:

- [ ] `survey-instrument.md` contains all five (or six) questions in Chapter 3 wording; each has a downstream-artifact note; metadata fields are enumerated.
- [ ] `sample-plan.md` has an active-user definition tied to a specific product event, exclusion rules, a query pseudocode, a sample-size calculation with the target 30-VD math, and a send-mechanics plan.
- [ ] `analysis-plan.md` names the segments, the per-segment n expectations, the Chapter 6 failure-mode routes per possible verdict, the free-text coding process, and a pre-registered falsification clause.
- [ ] `pilot-invitation.md` is a real, sendable message that explains the ask, bounds the time, promises a concrete return, does not bias with rewards, and does not cue the answer.
- [ ] The whole instrument could be deployed by a co-founder tomorrow with zero re-authoring.

## Common ways this exercise goes wrong

- **Paraphrasing the primary question.** "How disappointed would you be" is not "how would you feel". The wording is calibrated; leave it alone.
- **Sample plan that surveys all signups.** The exercise's core failure mode; if the plan does not filter to actives it is a failing submission.
- **Analysis plan that does not segment.** "We'll look at the aggregate and see" is not a plan; it is a lack of one.
- **No target-n math.** "We'll email everyone and see" produces surveys that never hit 30 VD and whose scores are unstable.
- **Pilot invitation that leads the witness.** "Help us prove product-market fit" or "we know you love the product" both bias the sample toward respondents who agree with the frame.
- **No free-text coding plan.** Free-text without a clustering process becomes a wall of anecdotes; the modal benefit statement never surfaces; the survey produces a number and no roadmap.
- **Analysis plan that gets written after seeing the data.** The whole discipline is that it is pre-registered. Rewrite chronologically: plan first, then run, then compare.
