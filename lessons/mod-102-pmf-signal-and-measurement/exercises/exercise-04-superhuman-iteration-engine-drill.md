# Exercise 04 — Superhuman Iteration Engine Drill

**Estimated time:** 4 hours
**Chapter link:** [`05-superhuman-iteration-engine.md`](../05-superhuman-iteration-engine.md)
**Prerequisite:** Exercise 02 (Sean Ellis survey instrument authored) and Exercise 03 (retention read produced); ideally with real or realistic survey response data to run against
**Prerequisite reading:** [Rahul Vohra — "How Superhuman Built an Engine to Find Product/Market Fit", First Round Review](https://review.firstround.com/how-superhuman-built-an-engine-to-find-product-market-fit/) — end to end (~45 min)

## Problem statement

The engine's whole discipline is *not* summarising the survey — it is running the **four-step loop** that turns the survey into a driver of roadmap decisions. In this exercise you execute one full cycle of the engine against real (or synthetic-but-realistic) survey data: cohort the very-disappointed, harden the modal main benefit, unblock the in-ICP somewhat-disappointed, and pre-register the re-survey plan.

This exercise is the largest in the module because it exercises every prior chapter — the survey (Chapter 3), the retention read (Chapter 4), and the engine (Chapter 5) — as one integrated loop.

## Requirements

Deliver a folder `exercise-04/` with:

- `step1-very-disappointed-cohort.md` — segment definition and modal main-benefit statement.
- `step2-main-benefit-hardening.md` — roadmap audit against the modal benefit.
- `step3-somewhat-disappointed-blockers.md` — in-ICP blocker cohort and top blockers.
- `step4-resurvey-plan.md` — the pre-registered next-cycle plan.
- `engine-summary.md` — one-page synthesis of steps 1–4 in scorecard-section shape.

You may run this against a real survey from Exercise 02, or against a **synthetic response set** you construct if you do not yet have real data. If synthetic, generate at least 60 realistic responses (mix of very-disappointed / somewhat-disappointed / not-disappointed) with plausible free-text; be explicit at the top of each file that the data is synthetic.

### Step 1 — cohort the very-disappointed (60 min)

Deliver `step1-very-disappointed-cohort.md` with:

- **The full very-disappointed cohort.** Table of every very-disappointed respondent with: role, company size, industry, tenure on product, plan. Target ≥15 respondents; if you have fewer, note the small-n caveat.
- **Segment analysis.** Cluster the very-disappointed cohort on the metadata dimensions. Which cluster dominates? Deliver a segment definition sentence in the form *"the very-disappointed cohort is concentrated in \[role\] at \[company shape\] with \[behavioural qualifier\]"* with the fraction of the cohort that matches (aim for ≥60% of the cohort matching your named segment; if less, the cohort spans multiple segments — split them).
- **Modal main-benefit statement.** Read the "main benefit you receive" free-text for every very-disappointed respondent. Cluster into ≤5 benefit-buckets; count citations per bucket; name the modal bucket in one sentence **in the users' own words** (choose the actual phrasing that best matches the modal cluster from a real response, do not paraphrase into founder-marketing prose).
- **Secondary main-benefit statement (if applicable).** If a second bucket has ≥25% of citations, name it too — it may be relevant to a different sub-segment or a supporting-value component in mod-103.
- **"Who benefits most" convergence.** From the very-disappointed cohort's Q2 answers, does the "who benefits most" language independently converge on the same segment you extracted from the metadata? Report the convergence explicitly. Divergence between metadata segment and self-reported segment is itself a finding — note it.

### Step 2 — harden the modal main benefit (60 min)

Deliver `step2-main-benefit-hardening.md` with:

- **Current-roadmap audit.** List every item on the next 90-day roadmap (target 8–15 items). For each, score:
  - **Makes the modal benefit stronger** (+2), neutral (0), or **weakens / distracts** (-1).
  - One-sentence rationale per item.
- **Reprioritisation.** Reorder the roadmap by benefit-strengthening score. Cut or defer the -1 items unless they are load-bearing for something else (revenue, compliance, safety); if you defer instead of cutting, name the specific downstream reason.
- **Competitive-alternatives check.** For each of the top-3 benefit-strengthening items, in one sentence, name a competitive alternative from the surveyed "what would you use as an alternative" answers, and state whether shipping this item makes the modal benefit *more differentiated* against that alternative. If it does not, the item is a parity feature, not a hardening feature — note that.
- **Ship-first list.** The top-3 (or top-5, if the quarter is long) items you would ship first, sequenced.

### Step 3 — somewhat-disappointed blocker cohort (60 min)

Deliver `step3-somewhat-disappointed-blockers.md` with:

- **The full somewhat-disappointed cohort.** Table of every somewhat-disappointed respondent with the same metadata as Step 1.
- **In-ICP filter.** Filter the somewhat-disappointed cohort to those who match the Step 1 segment definition ("in-ICP somewhat-disappointeds"). Report the fraction that survives the filter. If <50% match ICP, the cohort is diluted with users you should not build for — the in-ICP subset is what matters.
- **Top blockers.** Read the "how to improve" free-text of the in-ICP somewhat-disappointed cohort. Cluster into ≤5 blocker-buckets; count citations per bucket. Report the top 3 blockers with citation counts.
- **Blocker → boundary-crossing hypothesis.** For each of the top 3 blockers, in one sentence, articulate **why unblocking it would move that user from somewhat-disappointed to very-disappointed** — what specifically prevents them from experiencing the modal main benefit today.
- **Out-of-ICP appendix.** List the top 3 blockers from the *out-of-ICP* somewhat-disappointed cohort separately. State explicitly that these are **not** on the roadmap this cycle, and why (they would build a broader product for a segment you are not currently targeting).
- **Cross-check against Step 2.** Do any of Step 2's ship-first items already resolve a top-3 blocker? If yes, note the coincidence (rare — usually blockers are distinct from benefit-hardening). If no, plan to sequence Step 2's items first, then Step 3's blockers, both within the cycle.

### Step 4 — pre-register the re-survey plan (30 min)

Deliver `step4-resurvey-plan.md` with:

- **Re-survey date.** Exactly one quarter from now (or your chosen cadence per Chapter 5 — quarterly is default).
- **Same instrument.** Restated commitment to identical wording and same sample filter from Exercise 02.
- **Segment expectations.** Predict, in numbers, what the re-survey will show if the engine is working:
  - Very-disappointed % in the primary segment: from X% to Y% (justify the delta with the specific Step 2 and Step 3 work that would drive it).
  - Somewhat-disappointed cohort composition: expected shift into very-disappointed (name specific respondent IDs from Step 3 who *should* cross the line if their blockers are cleared).
- **Falsification lines.** What result would tell you the engine is not working?
  - "Primary segment VD is flat or lower" → Step 2 mis-identified the benefit, or Step 2 features shipped but were not perceptible.
  - "Blockers unchanged in re-survey's SD free-text" → Step 3 blockers shipped but did not perceptibly clear.
  - "New blockers dominate" → engine is working (blockers are being resolved), continue to next cycle.
- **Not-a-pivot clause.** Explicitly commit: one bad cycle is not a pivot signal. Two bad cycles → re-examine Step 1 segment definition. Three bad cycles → escalate to Chapter 6 failure-mode diagnostic (may be wrong-market or wrong-product masquerading as slow iteration).

### Engine summary (30 min)

Deliver `engine-summary.md` — one-page synthesis that packages the four steps in scorecard-section shape:

- **Segment + main-benefit statement** (from Step 1).
- **This cycle's roadmap** (top-3 hardening items + top-3 unblocking items, ordered).
- **Re-survey commitment** (date + expected numeric move).
- **Falsification** (what would make you conclude the engine is not working).

This one-pager is the artifact you would circulate to co-founder, first hire, and board as the cycle-1 summary.

## Starter guidance

- Chapter 5 is the operating manual. Read Rahul Vohra's essay end-to-end before starting — the essay is the closest thing to a lived case study of this engine at work.
- If your survey data is real but small (n=20 total responses, 4 very-disappointed): the engine still runs, but note the small-n caveat throughout and treat the segment definition as provisional until the next cycle enlarges the cohort.
- If your data is synthetic: generate responses that look like a *specific* startup in a *specific* segment — do not generate uniform responses. Realistic engine practice comes from realistic distributions. Include a few "not disappointed" responses whose free-text contradicts the very-disappointed cohort (e.g., users who wanted a completely different product); that contradiction is a real diagnostic input.
- The single most common execution error is skipping Step 2 and going straight to Step 3. The blockers list feels more actionable than the benefit-hardening list. Do Step 2 first — hardening the modal benefit is what makes the somewhat-disappointeds cross the line, because the benefit is what they are close to committing to.
- The out-of-ICP blocker appendix (Step 3) is where you *practise saying no*. If it feels bad to leave real user requests off the roadmap, the discipline is doing its job — the roadmap is finite and the boundary-crossing users are where the engine's leverage lives.
- The re-survey prediction (Step 4) is where the exercise turns from analysis to commitment. Write specific numbers. When the re-survey comes back, you compare against those specific numbers. Vague predictions cannot be falsified.

## Acceptance criteria

Your submission is complete when:

- [ ] `step1-very-disappointed-cohort.md` has the cohort table, a named segment with ≥60% cohort match, a modal main-benefit sentence in users' own words with citation count, and the metadata-vs-self-reported convergence check.
- [ ] `step2-main-benefit-hardening.md` audits the full roadmap with +2 / 0 / -1 scoring and rationales, produces a ship-first list, and includes the competitive-alternatives differentiation check on the top-3.
- [ ] `step3-somewhat-disappointed-blockers.md` has the SD cohort table, an in-ICP filter with reported survival fraction, top-3 blockers with citation counts, per-blocker boundary-crossing rationale, an out-of-ICP blocker appendix (with the "not on roadmap this cycle" commitment), and a cross-check against Step 2's ship-first list.
- [ ] `step4-resurvey-plan.md` has a specific date, restated instrument, numeric segment predictions, explicit falsification lines, and the not-a-pivot clause.
- [ ] `engine-summary.md` packages steps 1–4 in one page suitable for a co-founder / board circulation.
- [ ] Every claim in every file cites the specific survey response ID(s) or roadmap item(s) that support it.
- [ ] If data is synthetic, every file's header notes so explicitly.

## Common ways this exercise goes wrong

- **Averaging main-benefit statements across all respondents.** The very-disappointed cohort's benefit is different from the somewhat-disappointed cohort's benefit. Cluster within the very-disappointed cohort only.
- **Skipping the metadata-vs-self-reported convergence check.** When the very-disappointed cohort *is* mid-market EMs but their "who benefits most" free-text says "founders and salespeople", something is off — either your segment framing is wrong or a slice of the cohort is misidentified. Name the divergence.
- **Step 2 roadmap audit that is neutral on every item.** Every real roadmap has items that pull capacity away from the modal benefit; the audit's whole discipline is naming them. If nothing scores -1, the audit was too generous.
- **In-ICP filter that keeps everyone.** If you cannot bear to filter somewhat-disappointeds who are out of the very-disappointed segment, the exercise is failing. The out-of-ICP subset is where the *broader-product-nobody-loves* trap lives.
- **Predictions without numbers in Step 4.** "We think the score will go up" is not a prediction. "VD in mid-market will move from 56% to 65% by 2026-11-15" is.
- **Treating the engine as one-shot.** The engine's whole discipline is the re-survey. If your submission has no Step 4 or a Step 4 without a specific date, you have run half an engine.
- **Building for out-of-ICP blockers to be nice to those users.** They are not in-ICP; unblocking them costs roadmap capacity that would have moved an in-ICP boundary-crossing user. Say no.
