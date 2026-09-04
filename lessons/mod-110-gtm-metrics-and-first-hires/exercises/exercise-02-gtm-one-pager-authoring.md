# Exercise 02 — GTM One-Pager Authoring

**Estimated time:** 3 hours
**Chapter link:** [`05-leading-vs-lagging-and-the-gtm-one-pager.md`](../05-leading-vs-lagging-and-the-gtm-one-pager.md)
**Prerequisite reading:** [David Skok — "SaaS Metrics 2.0"](https://www.forentrepreneurs.com/saas-metrics-2/) (skim, ~20 min); [OpenView — Expansion SaaS Benchmarks (most recent)](https://openviewpartners.com/expansion-saas-benchmarks/) (skim, ~20 min); [SaaStr — writing on the founder's weekly / monthly cadence](https://www.saastr.com/) (search "weekly metrics" / "board pack"; ~15 min); [Winning by Design — Blueprints on GTM instrumentation](https://winningbydesign.com/) (skim relevant blueprints, ~15 min)

## Problem statement

Chapter 5 fixed the two-cadence discipline (weekly = leading, monthly = lagging), the section-by-section template for each one-pager, the "one focus / one priority" forcing function, and the sourcing / dating / signing / versioning discipline that makes both artifacts operational. This exercise makes you *author both one-pagers, end-to-end, for a real (or realistic) startup*, and stress-test the artifact against the Chapter 5 acceptance discipline.

You will:

1. Author a current-week **weekly one-pager** for a startup you know well (or the running code-review-tool example — see Part C for the variant instruction).
2. Author a most-recent-month **monthly one-pager** for the same startup, plugging in the CAC / LTV / payback / magic-number / retention numbers from Exercise 01 (or fresh computations if you did not do Exercise 01 against this startup).
3. Run the Chapter 7 full-ship checklist against both artifacts and fix anything that fails.

The exercise trains the operator loop — activity read on Monday drives the focus that drives the priority that drives next month's numbers — such that the two artifacts stop being status reports and start being decision documents.

## Requirements

Deliver a folder `exercise-02/` with:

- `weekly-one-pager.md` — the current-week weekly one-pager for your chosen startup, authored to the Chapter 5 template.
- `monthly-one-pager.md` — the most-recent-month monthly one-pager for the same startup, authored to the Chapter 5 template.
- `ship-checklist.md` — the Chapter 7 full-ship checklist run against both artifacts, with any failures called out and fixed.
- Optionally: prior-version stubs (a made-up v(n-1) and v(n-2) of the monthly, to demonstrate the versioning discipline).

### Part A — Author the weekly one-pager (60 min)

Pick a startup and a specific week (this week, ideally). Deliver `weekly-one-pager.md` to the Chapter 5 template:

1. **Header.** Startup name, week of YYYY-MM-DD, author name, publish cadence.
2. **Section 1 — Activity (last 7 days).** Founder outbound (accounts touched, meetings booked). AE outbound per rep. Inbound response (MQL count, median response time). Demos held vs. target. Proposals sent.
3. **Section 2 — Pipeline creation (last 7 days).** New opportunities by count and $ARR; per-channel; per-rep. Opportunities advanced. Opportunities regressed / no-decision.
4. **Section 3 — Pipeline health (as of Monday).** Total open pipeline. Coverage vs. quarterly quota (with the required-for-historic-conversion multiplier). Stalled deals count and $ARR.
5. **Section 4 — Current-quarter forecast.** Committed / best-case / pipeline. Quota. Delta.
6. **Section 5 — This week's one focus.** One specific thing that most changes next month's revenue if fixed this week. Owner, success criterion by Friday.

**Constraints:**

- Every number is a leading indicator or a same-week forecast. **No CAC, no LTV, no retention, no NRR on the weekly** — those are on the monthly.
- Every number cites a system of record (CRM, ad platform, calendar, etc.) — a hostile question has a same-day answer.
- The "one focus" line must be specific (not "improve conversion"), numerical or artifact-based, owned by a specific person, and time-bound by Friday.

If your book is genuinely small (pre-first-AE, founder-only, ≤3 open opportunities), scale the template — the sections are still all there, but the numbers may be single-digit and per-rep may collapse to per-founder.

### Part B — Author the monthly one-pager (75 min)

Same startup, most recent completed month. Deliver `monthly-one-pager.md` to the Chapter 5 template:

1. **Header.** Startup name, month YYYY, author name, prior-versions list (list at least three prior monthly versions by date, even if you have to backfill or mark as "v1 — reconstructed"), publish cadence.
2. **Section 1 — Revenue.** Closed MRR / ARR (month), net-new ARR (month) with YoY, total ARR with M/M growth, segment split (Enterprise / Mid-market / SMB).
3. **Section 2 — CAC (fully-loaded, per-channel).** Blended CAC with T3M trend. Per-channel CAC with logo count. Benchmark band call-out for the applicable motion and ARR tier.
4. **Section 3 — LTV, Payback, LTV/CAC.** Per-channel, cohort-based, gross-margin adjusted, capped at 36 months. Blended. Benchmark bar.
5. **Section 4 — Efficiency ratios.** Magic number (net, prior-quarter S&M) with T3M trend. Sales efficiency. Burn multiple.
6. **Section 5 — Retention.** GRR (T12M) with segment split; NRR (T12M) with segment split; cohort W12 for the latest primary-segment cohort with the last-6-cohorts trend. Inherit from mod-109 if you have a mod-109 scorecard for this startup.
7. **Section 6 — Funnel conversion.** MQL → SAL → Discovery → Demo → Proposal → Closed-Won for the month vs. the T6M baseline. Delta in pp.
8. **Section 7 — Headline read + one priority.** One paragraph answering the three operator questions from Chapter 1 (is the motion working? efficient? ready to scale?). One falsifiable priority for the month ahead — specific, numerical, owned, time-bound.
9. **Appendix.** Links to the CAC decomposition worksheet, cohort retention chart, funnel detail, CRM pipeline view.
10. **Sourcing footer.** One line naming the systems of record for every number.

**Constraints:**

- Per-channel decomposition on CAC (Chapter 2 discipline). Per-channel on LTV / payback / LTV/CAC (Chapter 3). Per-segment on retention (Chapter 5 discipline; mod-109 inheritance).
- Every number sourced.
- **No fundraising-view intrusion.** No multi-year LTV under a discount rate, no payback sensitivity across scenarios, no projected 18-month runway model. Chapter 1's boundary.
- The "one priority" line must be falsifiable (specific, numerical or artifact-based, owned, time-bound, checkable at the next monthly ship).

If your Exercise 01 book is different from your Exercise 02 startup, note it — the monthly may need fresh CAC / LTV / payback / magic-number derivation before you can fill sections 2–4.

### Part C — Ship-checklist review and fix pass (45 min)

Deliver `ship-checklist.md` — run the Chapter 7 full-ship checklist against both artifacts. Structure:

1. **Weekly one-pager checklist run.**
   - Dated, signed? (Pass / Fail — cite line.)
   - All five sections filled? (Pass / Fail — cite any thin section.)
   - Every number traces to a system of record? (Pass / Fail — cite any un-sourced number.)
   - "One focus" line specific, numerical / artifact-based, owned, time-bound? (Pass / Fail — quote the line.)
   - No lagging indicators? (Pass / Fail — cite any CAC / retention / LTV that leaked in.)
2. **Monthly one-pager checklist run.** Same structure against the seven-item checklist in Chapter 7.
3. **Fixes applied.** For every Fail, quote the specific edit made to the artifact to pass. If you cannot pass a specific checklist line (e.g., no prior-versions to list because the startup is pre-monthly), name the compensating discipline.
4. **Hostile-question stress test.** Pick three numbers on the monthly one-pager and answer *"where did that number come from?"* in one sentence each. Every answer must trace to a system of record you named in the sourcing footer.

**Variant note for the code-review-tool startup:** if you use the running code-review-tool example, do NOT copy Chapter 5's June 2026 monthly one-pager. Instead, author a *different month* (May 2026, or April 2026 — you can imagine plausible numbers upstream of Chapter 5's June state) so the exercise produces a fresh artifact rather than a transcription.

### Part D — Reflection (20 min)

A short closing paragraph:

- Which of the two one-pagers took longer to author, and why? (Usually the monthly, because per-channel CAC decomposition is expensive.)
- Which section of the monthly was hardest to fill honestly, and what instrumentation would make it easier?
- If your board read the monthly cold, which number would be the most likely target for a hostile question? Do you have a same-day answer?
- What is the one prior-version delta that would be most informative in your monthly (e.g., "CAC month-over-month per channel" or "cohort W12 trend across the last six cohorts")? Is that delta legible in the current version?

## Starter guidance

- Chapter 5's templates are copy-paste starting points. The discipline is in the numbers and the "one focus / one priority" lines, not in the shape.
- Do not skip the sourcing footer. A one-pager whose CAC line cannot be reconstructed from HubSpot + payroll + ad platforms is not defensible in ten minutes.
- The "one focus" and "one priority" lines are the whole point. If you cannot pick one, either the numbers have not converged (do the diagnostic) or you are trying to do too many things at once (pick).
- For the weekly, per-rep breakdowns are required as soon as you have more than one seller (founder + AE = two). Per-rep-per-channel is even more informative.
- For the monthly, the per-channel CAC / LTV / LTV/CAC table is the operating meat. If you cannot decompose, your ad platform + CRM + payroll instrumentation has a gap — name it.
- Benchmark call-outs must cite vintage. "OpenView benchmark" without the year is not defensible; the numbers shift year-over-year.
- Prior versions listed as `v6-Jun-2026, v5-May-2026, ...` in the header make the M/M delta legible at a glance. If you have only v1 (first month), list "prior versions: none — inaugural monthly, v1" and note the compensating discipline (weekly one-pagers preserved).
- The ship-checklist run in Part C is not busywork — it is the specific discipline that catches the "monthly one-pager with no per-channel decomposition" failure Chapter 5 warned about. Do it seriously.
- If you cannot fill a section honestly because the data does not exist yet (e.g., no cohort retention because the startup is <12 months old), say so — write "cohort W12 not yet available; earliest cohort is [date]" rather than making a number up.

## Acceptance criteria

Your submission is complete when:

- [ ] Weekly one-pager has all five sections filled, dated, signed, with a specific/numerical/owned/time-bound "one focus" line.
- [ ] Weekly contains no lagging indicators (no CAC, LTV, retention, NRR).
- [ ] Weekly's activity, pipeline creation, pipeline health, and forecast numbers all trace to a specific system of record (CRM, ad platform, calendar).
- [ ] Monthly one-pager has all seven sections filled, dated, signed, with prior-versions list (or explicit "v1 — inaugural" call-out).
- [ ] Monthly's CAC section shows per-channel decomposition (at least three channels).
- [ ] Monthly's LTV / payback / LTV/CAC section shows per-channel breakdown with the cohort-based, gross-margin-adjusted, 36-mo cap disciplines explicit.
- [ ] Monthly's retention section shows GRR + NRR + cohort W12 with per-segment split.
- [ ] Monthly's funnel conversion section shows the current month vs. the T6M baseline with the pp delta.
- [ ] Monthly's headline read paragraph answers the three operator questions from Chapter 1.
- [ ] Monthly's "one priority" line is specific, numerical or artifact-based, owned, time-bound, and checkable at the next monthly ship.
- [ ] Monthly has a sourcing footer naming the systems of record for every number.
- [ ] Ship-checklist review names Pass / Fail per checklist line for both artifacts and quotes the fix applied for every Fail.
- [ ] Ship-checklist includes a three-number hostile-question stress test with a same-day answer per number.
- [ ] Reflection names the hardest-to-fill section, an instrumentation gap, and the prior-version delta most informative for the operator loop.

## Common ways this exercise goes wrong

- **Weekly with lagging indicators.** CAC, retention, LTV, NRR on the weekly is the specific mistake Chapter 5 warned about. If they show up, move them to the monthly.
- **Monthly with blended-only CAC.** Chapter 2 discipline; Chapter 5 enforces. Per-channel or the one-pager fails.
- **Monthly with a "60-month LTV, uncapped, ARPU × life" number.** Chapter 3 discipline. Cohort-based, 36-mo cap, gross-margin adjusted. Otherwise it is a fundraising-view number that leaked in.
- **"One focus" line that is not a decision.** "Focus on outbound this week" is not a focus; "book 6 new demos on the healthcare-vertical target list, owner Alex, by Friday" is.
- **"One priority" line that is not falsifiable.** "Improve efficiency" is not a priority; "recover Demo → Proposal to ≥40% by end of month, owner Priya" is.
- **No prior-versions list.** The delta between versions is the operating output; if it is not preserved, the operator loop is not closed.
- **No sourcing footer.** A hostile question on any number has to have a same-day answer; the footer is the map from number to source.
- **Fundraising-view intrusion.** Multi-year LTV, payback sensitivity, projected runway — all belong in the fundraising view. Chapter 1's boundary.
- **Monthly one-pager assembled from scratch in a rush, with numbers reconstructed from memory.** The exercise's whole point is to author to the discipline; a reconstructed monthly fails the "defensible against a hostile question" bar the same day it ships.
- **Skipping the ship-checklist run "because the artifact looks fine."** Chapter 7 built the checklist for a reason; the failure modes are the ones authors miss on their own.
