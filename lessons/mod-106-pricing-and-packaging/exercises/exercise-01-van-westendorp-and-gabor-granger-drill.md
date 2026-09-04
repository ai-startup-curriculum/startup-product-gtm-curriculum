# Exercise 01 — Van Westendorp + Gabor-Granger Drill

**Estimated time:** 3 hours
**Chapter link:** [`01-willingness-to-pay-research.md`](../01-willingness-to-pay-research.md)
**Prerequisite:** Chapter 1 read end-to-end; a mod-104 ICP scorecard (or an equivalent working ICP + primary buyer persona); access to 30-60 candidate respondents who match the ICP (real prospects, existing customers on your ICP, or a warm founder-network list — not a general internet panel).

## Problem statement

Chapter 1 named the failure modes: skipping willingness-to-pay research and picking a number by intuition; running WTP research on the wrong sample; running the wrong instrument for the question; reading sharp OPP numbers off 30 respondents as if they were consumer-scale samples. The remedy is a small, disciplined, founder-run WTP research cycle that (a) fields **Van Westendorp** and **Gabor-Granger** against the same ICP-matched respondent set, (b) reports outputs as **bands, not points**, and (c) is defensible on sample, instrument, and interpretation grounds when a board member asks "how do you know?"

This exercise trains you to **field, analyse, and interpret** a two-instrument WTP study end-to-end — the survey form, the recruiting brief, the sample-size disclosure, the PSM curves, the Gabor-Granger demand and revenue curves, and a one-page findings memo that names the acceptable band, the revenue-max sub-band, the segment-level cuts, and the *specific misreads you refuse to make* off this sample. The output is not a pricing decision (that's Exercise 04 and Chapter 6). The output is the empirical anchor Chapters 2-5 will calibrate against.

The failure mode this exercise exists to catch: **the founder fields four PSM questions, reads the OPP off 30 respondents to the nearest dollar, drops the number into a pricing slide, and never confronts the anchoring, sampling, and stated-vs-real gaps that Chapter 1 named. The chart lends false confidence to what is still a small-sample directional signal.**

## Requirements

Deliver a folder `exercise-01/` with:

- `part-a-instrument-and-recruiting-brief.md` — the survey questions, the recruiting brief, the screening rules, the compensation policy, the deliberate sample-size disclosure.
- `part-b-data-and-analysis.md` — the raw data table (or a link to a sheet), the PSM curves, the Gabor-Granger demand + revenue curves, per-segment cuts.
- `part-c-findings-memo.md` — the one-page WTP research summary written in the Chapter 6 pack shape.

### Part A — Author the instrument and recruiting brief (45 min)

Deliver `part-a-instrument-and-recruiting-brief.md`.

**A1 — Van Westendorp PSM instrument (10 min).** Author the four PSM questions using Chapter 1's canonical wording, adapted to your product's language:

- Too cheap ("At what price would you consider it so *inexpensive* that you'd question quality and not want to buy?")
- Bargain ("At what price would you consider it a *bargain* — a great buy for the money?")
- Getting expensive ("At what price would you consider it to start getting *expensive* but still worth considering?")
- Too expensive ("At what price would you consider it so *expensive* that you would not consider buying it?")

Each question must specify the **unit** the respondent is answering in (per month, per year, per seat, per repo, per event — whichever matches your target pricing metric candidate). Author a two-sentence product description (the same paragraph shown to every respondent before the questions) so the respondent is pricing the same thing.

**A2 — Gabor-Granger instrument (10 min).** Author the buy / no-buy question at each price point. Pick **5 price points** spanning ~4× (e.g. {$3, $6, $12, $24, $48}) that bracket your best current guess of the acceptable range. State the randomisation rule explicitly — every respondent's starting price is drawn uniformly from the 5. Author the follow-up branching: if yes at $X, ask at the next-higher price; if no at $X, ask at the next-lower price. Cycle until the highest-yes price is bracketed.

**A3 — Recruiting brief and screening rules (15 min).** Author the recruiting brief you'll use to source respondents. Cover:

- **Screen-in criteria** derived from the mod-104 ICP scorecard (Layer 1 firmographic + Layer 2 behavioural). A respondent that fails any screen-in is excluded from the analysis regardless of whether she completes the survey.
- **Screen-out criteria** — competitor employees, journalists, students, and anyone who has already been quoted a specific price by you (they anchor to your quote, not the market).
- **Recruitment channels** — name each channel (existing customers, mod-105 outbound list, ICP-adjacent Slack / community, warm-intro list). For each channel, note the expected sample-fraction and any covariate risk (e.g., "Slack-community respondents are more price-sensitive because they self-select for cost-consciousness").
- **Target sample size** and **realistic sample size** — the number you'd like (Chapter 1's 30-100 for early-stage B2B) vs. the number you can actually field. If you can only reach 25, say so; a smaller-but-honest run beats a padded one.
- **Compensation policy** — non-cash (early access, share of results, favour banked) preferred over cash for ICP respondents at meaningful ACVs.

**A4 — Fielding logistics (10 min).** Which tool (Google Form / Typeform / Qualtrics / Conjointly), how the four PSM prices are captured (free-text vs. dropdown; free-text preferred for PSM), how Gabor-Granger branching is implemented (native Qualtrics logic vs. two-page Google Form vs. structured 1:1 interview), and the expected in-field window (1-2 weeks realistic for a hand-recruited B2B run).

### Part B — Field, capture, and analyse (75 min)

Deliver `part-b-data-and-analysis.md`.

You may **either** (i) field the survey against real respondents this week and analyse the actual responses, **or** (ii) run a paper simulation — hand-enter plausible responses from at least 30 named-account personas you've researched (in the shape of mod-101 discovery-corpus reasoning). If simulating, label it clearly at the top of Part B and treat the outputs as a *mechanics* demonstration, not a pricing signal. Real fielding is preferred; simulation is acceptable when the founder does not yet have a fielded run.

**B1 — Raw data (10 min).** Table (or linked sheet): one row per respondent; columns for respondent-ID, ICP-fit-verified (yes/no), recruitment channel, segment tag (e.g. "SMB / mid-market / enterprise" or "US / EU / LATAM"), the four PSM prices, the Gabor-Granger starting price, and the highest-yes price reached in the branching.

**B2 — Van Westendorp analysis (20 min).** Compute the four cumulative distributions ("too cheap," "bargain," "getting expensive," "too expensive"). Plot on a single chart (ASCII, spreadsheet screenshot, or matplotlib is fine). Identify:

- **PMC** — intersection of "too cheap" and "getting expensive."
- **PME** — intersection of "bargain" and "too expensive."
- **OPP** — intersection of "too cheap" and "too expensive."
- **IPP** — intersection of "bargain" and "getting expensive."

Report each as a **range** with an explicit confidence band based on your sample size (Chapter 1's discipline: 30 respondents ⇒ ~$3-5 wide bands, not a point). If your sample is small enough that the intersections are jittery, say so and report the range you *would* stake to.

**B3 — Gabor-Granger analysis (20 min).** Compute the demand curve (fraction who would buy at each price point). Multiply by price to get the revenue curve. Identify:

- The **peak** of the revenue curve (with the band around it).
- The **anchoring check** — does the demand curve depend on the starting price? Cross-tab willing-to-buy at $X by starting-price bucket. If starting price shifts the curve meaningfully, note it.
- The **stated-vs-real discount** — pick a discount (Chapter 1: 25-50% is standard) and report the revenue curve peak on both bases: "raw stated" and "discounted-for-real-purchase."

**B4 — Per-segment cuts (15 min).** Cut the sample by at least one meaningful segment (usually ICP sub-segment: SMB vs. mid-market, or region). Report per-segment PMC / PME / revenue-max separately. If any segment has < 10 respondents, note it and treat the cut as directional only.

**B5 — Data-quality notes (10 min).** List every reason a respondent's data should be discounted:

- ICP-fit failed the screen (should already be excluded).
- Response inconsistent (e.g., "too cheap" > "getting expensive" — the respondent didn't read the question).
- Respondent completed the survey in < 60 seconds (didn't think).
- Starting-price anchoring is visible on the individual response (all four PSM prices cluster within $5 of the starting price they saw, suggests anchor dominance).

Report the count of dropped responses and the reasons.

### Part C — The one-page findings memo (30 min)

Deliver `part-c-findings-memo.md`. Write the one-page WTP-research summary in the shape Chapter 6 requires (Section 5 of the pricing pack). Structure:

```
# WTP Research Summary — {product} — {segment} — {date}

## Sample
- N = {respondents}. ICP-matched = {n}. Segments: {sub-cuts + counts}.
- Fielded via {tool} between {date} and {date}. Channels: {list}.
- Sample-size caveats: {explicit statement of what you will and will not claim off this N}.

## Van Westendorp (per {unit})
- PMC (lower bound of acceptable): ${range}
- OPP (modal acceptable): ${range}
- IPP (bargain / expensive break-even): ${range}
- PME (upper bound of acceptable): ${range}
- Acceptable band: ${PMC-PME range}

## Gabor-Granger (per {unit})
- Demand curve peak (revenue-max, raw): ${range}
- Demand curve peak (discounted 30% for real-vs-stated): ${range}
- Anchoring check: {any anchor dependence noted}

## Per-segment cuts
- {Segment A}: {PMC-PME + revenue-max}
- {Segment B}: {PMC-PME + revenue-max}
- Diagnostic: {what the segment gap says — e.g., "enterprise 3× the mid-market ceiling"}

## Value-gap flag
- Anchor price the pack will test at v1: ${single number}
- Position relative to bands: {inside acceptable, above OPP, below PME, etc.}
- Gap to Chapter 2 value ceiling (fill in from Exercise 02 when authored): {TBD or ratio}

## Misreads I explicitly refuse
- {list 3-5 specific claims you will NOT make off this sample — e.g., "the OPP is $8.00 to the dollar; N is too small for that"}

## Next research cycle
- Refresh scheduled: {date, ~12 months out}
- Max-Diff (feature ranking): {planned / not planned}
- Any segment where the sample is too thin to interpret: {list; plan to boost next cycle}
```

Compress ruthlessly. If the memo runs longer than one page, the discipline hasn't landed — cut, don't append.

## Starter guidance

- **The PSM answer is a range, not a number.** Chapter 1 is explicit: 30-100 respondents in a niche B2B setting produces wide bands. Report ranges everywhere. A "range = single number" is a symptom of not respecting the sample.
- **The recruiting brief is the load-bearing part.** A brilliantly-analysed PSM curve fielded against off-ICP respondents is decoration. Spend real time on Part A3 — the screen-in / screen-out rules — before writing the questions. If in doubt on whether to include a respondent, exclude her and record why.
- **Randomise the Gabor-Granger starting price.** Chapter 1's most common Gabor-Granger failure is a fixed starting anchor. Even in a Google Form, you can implement rotation (5 form variants, respondents distributed evenly). Log which starting price each respondent saw so you can do B3's anchoring check.
- **PSM free-text > PSM dropdown.** Dropdowns discretise the answers to your buckets, hiding the shape of the distribution. Free-text (or a slider with 100+ positions) is the honest capture. Yes, this makes the analysis harder; do it anyway.
- **Simulation is a permission, not a shortcut.** If you're simulating Part B because you can't yet field, the exercise still trains the mechanics — but label the simulation clearly at the top of the memo, and re-run against real data as soon as you can field.
- **The "stated vs. real" discount is a policy, not a formula.** Chapter 1's 25-50% range is a working default; the specific discount you apply is a stake in the ground you defend. Pick one; state it; explain why (based on your buyer's decision-making psychology, not a plucked number).
- **Cross the two instruments.** The PSM band and the Gabor-Granger peak should overlap. If they don't, one of them is wrong — usually a small-sample artifact, occasionally a real signal (the market is stated-cheaper than it is revealed-cheaper, or vice versa). The disagreement is diagnostic.
- **Do not compute Max-Diff in this exercise.** Chapter 1 covers Max-Diff and you should note where it fits in the memo, but running it well requires a balanced experimental design that is beyond the scope of a 3-hour drill. Note it as a follow-on in the memo's "next research cycle" section.
- **Cite your provenance.** If a specific price was quoted or a specific number was reported by a respondent, the raw-data row is the citation. In the findings memo, do not invent numbers that are not in Part B's raw data.
- **The "misreads I refuse" list is the discipline signal.** A memo without this section is a memo that will overclaim. Force yourself to name at least three specific claims you would refuse to defend off this sample — that list is what protects you when the founder-CEO (you) is tempted to overreach in a board update.

## Acceptance criteria

Your submission is complete when:

- [ ] Part A contains the four PSM questions with a common product-description paragraph, the Gabor-Granger price points with an explicit randomisation rule, and the branching logic.
- [ ] Part A's recruiting brief names screen-in criteria (from ICP scorecard), screen-out criteria (competitors / press / anchored respondents), recruitment channels with per-channel covariate risks, target and realistic sample sizes, and compensation policy.
- [ ] Part A names the fielding tool and describes how randomisation and branching are implemented in that tool.
- [ ] Part B contains a raw-data table (or link) with per-respondent columns for ICP-fit, channel, segment, four PSM prices, Gabor-Granger starting price, and highest-yes price.
- [ ] Part B's PSM analysis plots the four curves and reports PMC / OPP / IPP / PME as **ranges** with confidence bands appropriate to the sample size.
- [ ] Part B's Gabor-Granger analysis reports the demand curve, the revenue curve, the peak with a band, an anchoring cross-tab, and a stated-vs-real discount with an explicit % chosen.
- [ ] Part B's per-segment cuts report at least one meaningful segmentation with per-segment PMC / PME / revenue-max, flagging any thin cut.
- [ ] Part B's data-quality notes list the drop reasons and the drop count.
- [ ] Part C is one page in the Chapter 6 pack shape, with sample block, PSM block, Gabor-Granger block, per-segment cuts, a value-gap flag placeholder for Exercise 02, an anchor-price-for-v1 stake, and the "misreads I refuse" list of at least 3 items.
- [ ] Any fielding you did not actually complete is labelled `simulated` at the top of Part B and the memo; simulation results are not reported as fielded findings.
- [ ] Any factual claim (a benchmark rate, a competitor price, a category norm) that is not from your own data is flagged `<!-- needs-research: ... -->` rather than invented.

## Common ways this exercise goes wrong

- **The wrong-sample trap.** Founder fields against a general-panel or Slack-community respondent pool that is not ICP-matched; the resulting curves reflect the wrong market. Fix: Part A's screen-in rules from the ICP scorecard, applied hard.
- **The sharp-number-off-small-sample trap.** OPP reported as "$74.00" off 30 respondents. Fix: report as "$60-$90" and stake to the band.
- **The fixed-anchor Gabor-Granger trap.** Every respondent saw the same starting price; the demand curve is a picture of the anchor. Fix: rotate the starting price across the 5 buckets; verify in B3's anchoring cross-tab.
- **The stated-intent-as-real-forecast trap.** Founder reports the raw Gabor-Granger revenue-max as the pricing recommendation. Real purchase is lower than stated by 25-50%. Fix: apply and disclose a discount in B3.
- **The single-segment-collapse trap.** All respondents pooled; the "acceptable band" hides that enterprise and SMB have completely different curves. Fix: at least one per-segment cut in B4; call out thin cuts explicitly.
- **The over-friendly-respondent trap.** Founder recruits only warm respondents who like her; every PSM answer is generously priced. Fix: at least one channel in Part A is a cold-outreach or community channel; screen for social-desirability bias.
- **The invented-response trap.** Founder is simulating and invents responses that match the answer she wants. Fix: simulated Part B is a mechanics-only demonstration, clearly labelled, and only used to teach the analysis pipeline before fielding.
- **The Max-Diff-scope-creep trap.** Founder tries to also run a Max-Diff and gets 30% of the way. Fix: leave Max-Diff to a follow-on cycle; note it in the memo's "next research cycle" block.
- **The two-instruments-disagree-and-founder-picks-one trap.** PSM says $80; Gabor-Granger says $130; founder picks the number she likes. Fix: report both, name the disagreement, offer a diagnostic hypothesis (small-sample artefact, stated-vs-revealed gap, wrong segment mix), and pick the number you'll test with justification.
- **The no-misreads-list trap.** Part C ships without the "misreads I refuse" block. Fix: force the list; the memo without it becomes over-claim ammunition later.
- **The findings-memo-longer-than-one-page trap.** Compression discipline lost; three pages of analysis in the memo. Fix: one page. Deep analysis lives in Part B. The memo is a compressed decision artifact.
- **The single-run-and-done trap.** Memo does not schedule a refresh. Twelve months later the curve is stale and the pricing pack has drifted. Fix: Part C's "next research cycle" line names a refresh date ~12 months out.
