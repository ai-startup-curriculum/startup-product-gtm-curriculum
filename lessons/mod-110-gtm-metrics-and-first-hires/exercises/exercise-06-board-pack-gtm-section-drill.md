# Exercise 06 — Board-Pack GTM Section Drill

**Estimated time:** 3 hours
**Chapter link:** [`07-shipping-the-gtm-one-pager-and-hire-staging-plan.md`](../07-shipping-the-gtm-one-pager-and-hire-staging-plan.md), [`05-leading-vs-lagging-and-the-gtm-one-pager.md`](../05-leading-vs-lagging-and-the-gtm-one-pager.md), [`06-staging-the-first-three-gtm-hires.md`](../06-staging-the-first-three-gtm-hires.md)
**Prerequisite reading:** [SaaStr — Jason Lemkin on board decks and board management](https://www.saastr.com/) (search "board deck" / "board meeting"; ~20 min); [First Round Review — writing on board packs](https://review.firstround.com/) (search "board deck" / "board meeting"; ~15 min); [Bessemer — State of the Cloud](https://www.bvp.com/atlas) (skim for the metric shapes public SaaS companies report; ~15 min); [OpenView — Expansion SaaS Benchmarks](https://openviewpartners.com/expansion-saas-benchmarks/) (skim, ~15 min)

## Problem statement

Chapter 7 fixed the ship discipline for the board-pack GTM section: it is **the monthly one-pager assembled into a trailing-3-month trend view plus the current staging plan, plus one paragraph per operator question, plus one paragraph on the hire plan.** No new data collection. If the monthly one-pagers were maintained honestly, the board pack falls out.

This exercise makes you *author the board-pack GTM section for one quarter* against three constraints: the trailing three monthly one-pagers must roll up into a defensible trend view; the current staging plan must slot in with quarter-over-quarter delta notes; the narrative paragraphs must answer the three Chapter 1 operator questions without leaking the fundraising view.

The exercise trains the specific discipline that turns the monthly cadence into a quarterly artifact for external audiences — the board, an incoming Series-B partner, an incoming VP GTM — without producing a new artifact from scratch.

You will:

1. Roll up three trailing monthly one-pagers (either from Exercise 02 or from the running code-review-tool set) into a trailing-3-month trend view.
2. Slot in the current staging plan (either from Exercise 04 or a fresh authoring) with quarter-over-quarter deltas noted.
3. Author the three-plus-one narrative paragraphs (operator questions × 3 + hire plan × 1).
4. Run the Chapter 7 ship checklist and stress-test the pack against three hostile board questions.

## Requirements

Deliver a folder `exercise-06/` with:

- `board-pack-gtm-section.md` — the full board-pack GTM section (target 3 pages; hard cap 4).
- `hostile-question-stress-test.md` — three hostile board questions and same-day answers.
- Optionally: a `charts/` sub-folder with the trend sparklines or trailing-3-month tables the pack references.

### Part A — Set up the monthly one-pager set (30 min)

You need three consecutive monthly one-pagers to roll up. Options:

- **Option 1 — Use Exercise 02.** If you did Exercise 02, use the monthly one-pager you authored plus two "prior" monthlies (either real or reasoned backfills — mark backfills as "reconstructed for this exercise, v1 was inaugural").
- **Option 2 — Use the code-review-tool set.** The Chapter 5 example is the June 2026 monthly for Reviewer.io; Chapter 7 references a July 2026 version. Author a plausible May 2026 monthly (upstream of the paid-channel decision) to have three months (May, June, July).
- **Option 3 — Author three fresh monthlies for a startup you know well.** More work; higher fidelity. Do this if the startup has real numbers you can pull.

Whichever option, deliver a table (in `board-pack-gtm-section.md` or as an appendix) that names the three monthlies by date and version and confirms each ships to the Chapter 5 template.

### Part B — Author the board-pack GTM section (120 min)

Deliver `board-pack-gtm-section.md` structured as:

**1. Header.** Startup, quarter (e.g., "Q3 2026"), author, date (should be the week before the board meeting, per Chapter 7's "published one week ahead" discipline).

**2. Executive summary.** ≤5 bullets. The state of the quarter for GTM: is the motion working, efficient, ready to scale? What is the one priority for next quarter? What is the one thing that would most change the picture?

**3. Revenue and growth.** Trailing-3-month table:
   - Total ARR (month-end for each of the three months, with M/M growth per month and Q/Q growth headline).
   - Net-new ARR per month.
   - Segment split (Enterprise / Mid-market / SMB) per month.
   - YoY: total ARR growth for the quarter vs. the same quarter prior year.

**4. Efficiency ratios.** Trailing-3-month table:
   - Blended CAC per month with T3M trend.
   - Per-channel CAC for the current month (with an inline note if the mix shifted materially over the three months).
   - Magic number per month.
   - Sales efficiency per month.
   - Burn multiple per month.
   - LTV / Payback / LTV/CAC — blended and per-channel, most recent month with prior month for delta.
   - Benchmark call-out: which OpenView / KeyBanc / Bessemer / SaaStr band each ratio falls into, with vintage cited.

**5. Retention.** Trailing-3-month table:
   - GRR per month (T12M) with segment split.
   - NRR per month (T12M) with segment split.
   - Cohort W12 for the latest primary-segment cohort (with the last-6-cohorts trend as a sparkline or a three-value comparison).
   - Inherit from the mod-109 retention scorecard; reconcile numbers if they differ.

**6. Funnel conversion.** Current month (or Q-average) stage-by-stage vs. the T6M baseline, with the pp delta and a one-line explanation for any stage that materially degraded or improved.

**7. Narrative — is the motion working?** One paragraph. Read the pipeline creation, funnel conversion, and revenue trend across the three months. Name specific drivers (a channel that scaled or defunded; an AE that ramped; a segment that softened). Answer the question directly, not obliquely.

**8. Narrative — is the motion efficient?** One paragraph. Read the CAC / LTV / payback / magic number / sales efficiency numbers across the three months. Name per-channel decisions the team made or should make. Cite benchmarks.

**9. Narrative — is the motion ready to scale?** One paragraph. Read the AE quota attainment, the funnel constraint, the first-hire staging plan's trigger criteria state. Answer directly whether the next scaling hire is triggered or deferred, and why.

**10. First-hire staging plan (current version).** Slot in the current version of the plan from Exercise 04 (or a fresh authoring). Include the quarter-over-quarter delta: what changed since last quarter's board pack? Which hires landed as planned? Which triggers moved (met or missed)? Which deferrals stayed deferred?

**11. Narrative — hire plan.** One paragraph. Summarise the last quarter's hire actions (or non-actions), the current quarter's planned hire(s) contingent on triggers, and the specific one-pager numbers the board should watch to re-read the plan next quarter.

**12. Priority for next quarter.** One falsifiable priority. Specific, numerical or artifact-based, owned, time-bound, checkable at the next board pack.

**13. Sourcing footer.** Systems of record for every number. Same discipline as the monthly one-pager.

**14. Appendix.** Links to the three monthly one-pagers rolled up, the current + prior staging plan versions, the underlying mod-102 PMF scorecard and mod-109 retention scorecard, and any relevant mod-107 playbook or mod-108 channel-audit artifacts.

**Constraints:**

- **Target 3 pages; hard cap 4.** If it runs longer, cut.
- **No new data collection.** Every number in the pack traces to one of the three monthly one-pagers, the mod-109 retention scorecard, or the current staging plan. If you needed to collect a number specifically for the board pack, name that as a monthly-one-pager gap and add it to the next monthly.
- **No fundraising-view intrusion.** Chapter 1's boundary. No multi-year LTV, no payback sensitivity, no projected runway model, no Rule of 40, no public-comparables multiples. The fundraising view is a separate artifact.
- **Trend visibility on every ratio.** Trailing-3-month is the minimum; YoY where the data supports it. A single-point-in-time board pack fails the board-pack purpose.

### Part C — Hostile-question stress test (30 min)

Deliver `hostile-question-stress-test.md` — three hostile board questions your pack must survive. For each:

1. **The question.** Quote it verbatim (from the list below or invent your own — but the invented ones must be plausible).
2. **The same-day answer.** In ≤3 sentences, cite the specific number(s) and the specific source (which of the three monthly one-pagers, which cell of the CAC decomposition, which cohort in the retention scorecard).
3. **The section of your pack the answer lives in.** Cite by section number from your Part B artifact.

Pick three from the following list (or invent equivalents):

- "Where did the blended CAC number come from?"
- "Why is the paid channel LTV/CAC below 1× and still on the plan?"
- "Why aren't we hiring a VP Sales in the next quarter? Every one of your peer companies at this ARR has one."
- "Your NRR is 118% but your GRR is 82%. Is expansion masking a leaky floor?"
- "The Demo → Proposal conversion rate dropped 13pp in June and only recovered 9pp by July. Is that going to compound?"
- "What is the payback on the next AE hire, and how confident are you in that number?"
- "Why is the second-AE hire in Q1 2027 not in Q4 2026? What specifically has to be true?"
- "How does your magic number compare to public SaaS benchmarks in your ARR band?"
- "If we underperform Q4 by 20%, which hire on the plan falls out?"

The answer discipline is Chapter 7's — same-day answer, specific number, specific source.

### Part D — Ship-checklist review (15 min)

Run the Chapter 7 board-pack-equivalent checklist against your artifact. The checklist synthesises the monthly one-pager and staging plan checklists into a board-pack-specific version:

- [ ] Dated, signed, prior board-pack versions listed.
- [ ] Executive summary is ≤5 bullets and answers the three operator questions.
- [ ] Every metric shown as trailing-3-month trend, not single-point.
- [ ] CAC decomposed per-channel; LTV / LTV/CAC decomposed per-channel; retention decomposed per-segment.
- [ ] Every number cites a source; benchmarks call out band + vintage.
- [ ] Three operator-question narrative paragraphs each answer their question directly.
- [ ] Staging plan section includes quarter-over-quarter delta.
- [ ] Hire plan narrative summarises last quarter's actions and next quarter's contingent plan.
- [ ] One falsifiable priority for next quarter.
- [ ] No fundraising-view intrusion.
- [ ] Sourcing footer names systems of record.
- [ ] Artifact fits in 3–4 pages.

For every Fail, quote the specific edit made to pass.

### Part E — Reflection (15 min)

A short closing paragraph:

- Which of the three operator-question narratives was hardest to write, and why? (Common: "is the motion ready to scale?" because it forces the founder to defend a "not yet" against board pressure.)
- Which of the three hostile-question stress tests was the closest call? Was your answer genuinely same-day or was it "I'll get back to you next week"?
- If your monthly one-pager discipline is thin (or nonexistent), how much extra work did the board-pack authoring take? (This is the specific cost of skipping the monthly cadence — Chapter 7's "board pack from scratch three weeks before the meeting" pathology quantified.)
- Which section of the pack most benefits from a sparkline / small chart vs. a table, and did you include one?

## Starter guidance

- Chapter 7's example (Reviewer.io) is the working shape. Adapt to your startup; do not transcribe.
- The **trailing-3-month trend is the point.** A number in isolation is not a board-pack number; a number with a three-value history is. Sparklines or three-value tables are equally valid.
- The **operator-question narratives are three paragraphs, not three sentences.** They should answer *directly* — "yes, the motion is working, and here is the specific evidence" — not obliquely.
- The **priority for next quarter is falsifiable.** "Recover Demo → Proposal to ≥45% by end of quarter" is falsifiable; "improve conversion" is not.
- The **hostile-question stress test is where the artifact earns its keep.** A board pack that reads well but cannot survive a hostile question is decorative. Do the stress test seriously.
- If your monthly one-pagers do not yet exist, the exercise reveals the specific work-you-should-have-done-monthly cost as board-pack authoring effort. Note this in the reflection — it is Chapter 7's central pedagogical point.
- The staging plan slot-in is not a re-authoring — it is a paste-in of the current version plus a quarter-over-quarter delta annotation. If the plan is unchanged, note that; if a hire landed, note that; if a trigger moved, note that.
- Sourcing footer: one line naming every system of record. Same discipline as the monthly. A hostile question on any number has a same-day answer.
- The hostile questions in Part C are drawn from real practitioner writing (SaaStr, First Round, Lemkin, First Round Review). If you want a fourth or a variant, read a Lemkin post on board management and pick a question he uses as a diagnostic.

## Acceptance criteria

Your submission is complete when:

- [ ] Board pack has all 14 sections filled (header, executive summary, revenue, efficiency, retention, funnel, three narratives, staging plan, hire narrative, priority, sourcing footer, appendix).
- [ ] Board pack shows trailing-3-month trend on every ratio (CAC, magic number, sales efficiency, burn multiple, GRR, NRR).
- [ ] Board pack shows per-channel CAC decomposition for the current month, with a note on mix-shift over the three months if applicable.
- [ ] Board pack shows per-channel LTV / payback / LTV/CAC with prior-month delta.
- [ ] Board pack shows retention per-segment (Enterprise / Mid-market / SMB).
- [ ] Board pack has funnel-stage conversion for the current month vs. T6M baseline with pp delta.
- [ ] Board pack's three operator-question narratives each answer their question directly (not oblique).
- [ ] Board pack's staging plan section includes quarter-over-quarter delta.
- [ ] Board pack's hire narrative names last quarter's actions and next quarter's contingent plan.
- [ ] Board pack's next-quarter priority is falsifiable (specific, numerical or artifact-based, owned, time-bound).
- [ ] Board pack has a sourcing footer.
- [ ] Board pack fits in 3–4 pages.
- [ ] Board pack has no fundraising-view intrusion.
- [ ] Hostile-question stress test has three questions answered with same-day specificity, source citation, and section-of-pack reference.
- [ ] Ship-checklist review names Pass / Fail per checklist line with fix per Fail.
- [ ] Reflection names hardest narrative to write, closest-call hostile question, monthly-discipline cost, and chart-vs-table judgment.

## Common ways this exercise goes wrong

- **A board pack that reads as a status report, not a decision document.** The three operator-question narratives must answer directly. "The motion is largely working" is not a direct answer; "yes, the motion is working — Priya at 100% Q3, per-channel CAC declining, magic number 2.9" is.
- **Single-point-in-time metrics without trend.** A board pack whose CAC row is one number, not a three-month trend, fails the board-pack purpose. Trend is the point.
- **Fundraising-view intrusion.** Multi-year LTV, payback sensitivity, projected runway — none of these belong. Chapter 1's boundary.
- **Board pack assembled from scratch in the week before the board meeting.** If you did this in the exercise, the reflection paragraph is the load-bearing artifact — quantify the cost.
- **Staging plan section that is a full re-authoring rather than a paste-in-plus-delta.** The plan lives in Exercise 04's artifact; the board pack references it and notes the delta.
- **Narrative paragraphs that do not cite specific numbers.** "The motion is efficient" is not a paragraph; "the motion is efficient — blended CAC dropped from $10,551 in June to $8,940 in July after the paid defund, magic number recovered from 2.6 to 2.9, per-channel LTV/CAC now 3.2×, 1.94×, and 1.37× on the three retained channels" is.
- **Priority that is not falsifiable.** "Improve efficiency" is not a priority. "Complete mod-107 playbook by Aug 31, owner Priya + Alex" is.
- **Hostile-question answers that require follow-up work.** "I'll get back to you next week" is a fail; "the $8,940 blended CAC in July came from HubSpot + payroll + ad platforms; see the CAC decomposition worksheet linked in the appendix" is a pass.
- **Board pack that exceeds four pages.** Cut. If you cannot cut without losing signal, the pack has scope creep or the monthly is under-decomposed and the pack is picking up the slack.
- **Missing the quarter-over-quarter delta on the staging plan.** The delta is the operating output — which hires landed, which triggers moved, which deferrals stayed. Without it, the plan reads as static.
- **Skipping the sourcing footer "because the board knows where the numbers come from."** They do not, and a hostile question in the meeting will reveal it.
