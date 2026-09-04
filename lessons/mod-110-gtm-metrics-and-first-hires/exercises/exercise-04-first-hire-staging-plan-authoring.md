# Exercise 04 — First-Hire Staging Plan Authoring

**Estimated time:** 3 hours
**Chapter link:** [`06-staging-the-first-three-gtm-hires.md`](../06-staging-the-first-three-gtm-hires.md), [`07-shipping-the-gtm-one-pager-and-hire-staging-plan.md`](../07-shipping-the-gtm-one-pager-and-hire-staging-plan.md)
**Prerequisite reading:** [Pete Kazanjy — *Founding Sales*](https://foundingsales.com/) (Chapters on founder-led-to-first-AE and on hiring the first AE, ~45 min); [Mark Roberge — *The Sales Acceleration Formula*](https://www.markroberge.com/) (Chapter on the science of hiring, ~30 min); [SaaStr — Jason Lemkin on "when to hire your first VP Sales"](https://www.saastr.com/) (search "first VP Sales" and "when to hire"; ~20 min); [Winning by Design — GTM hire sequencing blueprints](https://winningbydesign.com/) (skim relevant blueprints; ~15 min)

## Problem statement

Chapter 6 fixed the default staging sequence (founder-led → first AE → first PMM or DG → second and third AEs → first sales manager) with per-hire trigger criteria, and Chapter 7 fixed the ship discipline for the 12-month staging plan (versioning, current-state readouts, explicit "not yet" calls, board narrative). This exercise makes you *author a real, defensible 12-month staging plan* for a startup you know well, complete with trigger criteria per hire, current-state reads against the criteria, and explicit deferrals for the roles the founder is being pressured to hire.

You will:

1. Author a 12-month staging plan for a real (or realistic) startup at the Series-A boundary.
2. For each proposed hire, produce trigger-criteria checklist, current-state readout, "if not met" contingency, and review cadence — per the Chapter 7 template.
3. Include an explicit deferrals section for at least three roles the founder has been pressured to hire (typically VP Sales, RevOps, Sales Enablement) with the specific reason each defers.
4. Write the board narrative paragraph that defends the plan against a hire-faster counter-proposal, with the specific arithmetic that makes the recommendation more defensible.

The exercise trains the staging discipline that turns "we should hire faster because the board wants growth" into "here is the specific numerical trigger for each hire, here is why hire N is now and hire N+1 is not, and here is the arithmetic of the hire-faster alternative."

## Requirements

Deliver a folder `exercise-04/` with:

- `staging-plan.md` — the 12-month staging plan for your chosen startup, authored to the Chapter 7 template.
- `board-narrative.md` — the paragraph that would accompany the plan when presented to the board (or a section of `staging-plan.md`; either is fine).
- Optionally: a spreadsheet of the plan's fully-loaded 12-month GTM salary spend vs. a hire-faster alternative.

### Part A — Author the staging plan (90 min)

Pick a startup — yours, one you know well, or the running code-review-tool (but use different specifics from Chapter 6's example so this is a fresh authoring, not a transcription). The startup must be at or near the Series-A boundary — pre-Series-A, immediately post-Series-A, or 6–12 months post — because the staging discipline is calibrated to that stage.

Deliver `staging-plan.md` to the Chapter 7 template:

1. **Header.** Startup name, author, version, date, prior-versions list, plan horizon (12 months by quarter).
2. **Current GTM org (as of [date]).** Name every current GTM person (founder, AEs, CS, marketing, SDRs, etc.), their hire date, and their current role. If a role is founder-worn (e.g., founder is functionally the sales manager), name that explicitly.
3. **Current one-pager signal (from most recent monthly).** Cite the AE quota attainment, pipeline coverage vs. required multiplier, blended CAC with T3M trend, magic number, and the current funnel constraint (top-of-funnel volume, stage conversion, or other).
4. **Hire #1 — [Role]. Target date: [YYYY-QN].**
   - Trigger criteria — a checklist of ≥3 items, each specific and checkable, drawn from the Chapter 6 trigger lists per role.
   - Current state — per-criterion met / not met / partially met.
   - If not met — what has to change and by when.
   - Review cadence — monthly or quarterly.
   - Which — if the hire is a fork (PMM vs. DG, for example), the signal-based choice logic.
5. **Hire #2 — [Role]. Target date: [YYYY-QN].** Same structure.
6. **Hire #3 — [Role]. Target date: [YYYY-QN].** Same structure.
7. **Hire #4 — [Role, or "contingent on Hire #N"]. Target date: [YYYY-QN or later].** Same structure. If the trigger is contingent on a prior hire landing, name the dependency explicitly.
8. **Explicit deferrals — things NOT on the plan.** At least three roles the founder is being pressured to hire and why they defer. VP Sales is one of them (Chapter 6 Pattern 1); RevOps and Sales Enablement are common others; a second AE or SDR before the corresponding trigger is met is another candidate.
9. **Board narrative.** One paragraph. (Details in Part B.)
10. **Appendix.** Links to the current monthly + weekly one-pager, prior staging plan versions, the underlying mod-102 PMF scorecard and mod-109 retention scorecard, and any mod-107 playbook or mod-105 script docs in flight.

**Constraints:**

- **At least one hire on the plan is a "not yet" call** — a hire whose trigger criteria are not met and whose primary output is "when will these be met, and under what monthly re-read cadence."
- **At least three roles in the deferrals section**, each with an explicit deferral criterion (what would have to be true for the hire to be reconsidered).
- **Every trigger criterion is a specific numerical bar or artifact-completion trigger**, not a subjective judgment. "Priya at ≥100% quota for 2 consecutive quarters" is a trigger; "Priya doing well" is not.
- **The plan is versioned.** Even if this is v1, list "prior versions: none — inaugural" and note the compensating discipline.

### Part B — Author the board narrative (45 min)

Deliver a board-narrative paragraph (or a `board-narrative.md` section) that:

1. **States the plan's total fully-loaded 12-month GTM salary spend** (sum of the fully-loaded costs of every hire on the plan × the fraction of 12 months they will be on the payroll after hire).
2. **States the alternative "hire faster" plan's spend.** The alternative is typically what a board member or investor has been suggesting — often a VP Sales + a second AE + one or two SDRs starting in the current or next quarter, before the current plan's trigger criteria are met.
3. **Names the specific reason the recommended plan is more defensible.** Which trigger criterion is not yet met; which numerical signal on the one-pager confirms the trigger's absence; what happens if you hire ahead of the trigger anyway (Chapter 6 Pattern 1 / 2 / 3 as applicable).
4. **States the specific numerical bet.** At the current one-pager numbers (magic number, first AE attainment, pipeline coverage), what does the recommended plan produce in net-new ARR this year? What would the alternative plan need to produce to be breakeven at the equivalent magic number? Is that arithmetically available given the current funnel-loading constraint?
5. **Names the specific review triggers that would change the plan.** Which numbers on the one-pager, if they moved, would qualify the deferred hires? Under what cadence will they be re-read?

The paragraph should be defensible against a "let's hire faster and figure out the trigger later" counter-argument. If it is not, iterate.

### Part C — Ship-checklist review and fix pass (30 min)

Run the Chapter 7 staging-plan ship checklist against your artifact:

- [ ] Dated, signed, prior versions listed.
- [ ] Current GTM org and current one-pager signal named at the top.
- [ ] Every hire has trigger criteria (specific and checkable), current-state readouts, and a review cadence.
- [ ] At least one hire is a "not yet" call with explicit deferral criteria.
- [ ] Explicit deferrals section names the roles the founder has been pressured to hire and why they defer.
- [ ] Board narrative names the recommended plan's spend, the alternative "hire faster" spend, and defends the recommendation on the numbers.

For every Fail, quote the specific edit made to the artifact to pass. If you cannot pass a specific line honestly (e.g., "at least one hire is a 'not yet' call" — but all your hires have met triggers), note the compensating discipline and explain why the "not yet" section is thin.

### Part D — Reflection (15 min)

A short closing paragraph:

- Which hire on your plan was hardest to trigger-criteria-ise, and why? (Common: the first PMM vs. DG fork; the second-AE trigger, because "2 consecutive quarters at quota" feels slow to a founder under board pressure.)
- Which deferral was the most difficult to defend, and what was the pressure? (Common: VP Sales, because the board wants a senior GTM name on the org chart.)
- If a prospective incoming VP GTM (say 3–6 months from now) read your plan cold, what one clarification would they push on? (Common: the fork logic between PMM and DG; the specific mod-105 / mod-107 artifacts named as pre-conditions for the first AE.)
- What number on the one-pager, if it moved next month, would most change the plan?

## Starter guidance

- Chapter 6's per-hire trigger-criteria lists are your operating checklists. Cite them verbatim in the trigger sections and mark each per-criterion.
- Chapter 7's template is the shape. Do not re-invent; adapt the fields to your startup's specifics.
- The **"not yet" discipline is the load-bearing move.** If your plan has four affirmative hires and zero deferrals, you have not applied Chapter 6's central discipline — you have a hire-everyone plan. Re-read Chapter 6's Pattern 1 (VP Sales before PMF) and reconsider.
- The **board narrative's arithmetic is the specific instrument** that makes the plan defensible. "$195k of GTM salary vs. $920k for the alternative, against a motion that has not yet demonstrated it can support a second AE, per the one-pager." Do the math; do not hand-wave.
- For the fork hires (PMM vs. DG), the Chapter 6 rule is: **volume constraint → DG first; conversion constraint → PMM first.** State the signal, then choose.
- For the deferrals, the three most common roles founders are pressured to hire and defer at Series-A are: **VP Sales** (Chapter 6 Pattern 1 — do not hire before PMF and ≥3 AEs); **RevOps** (defers until tooling / process complexity threshold met, typically at ≥2 AEs); **Sales Enablement** (defers until second AE onboarding produces enough operational learning to codify). Use these as defaults if you cannot think of others.
- For the "which one-pager number would most change the plan" reflection: the honest answer is usually the AE quota attainment or the pipeline coverage vs. required multiplier. Both are on the monthly; both are checkable next month.
- If your startup has an unusual motion (pure PLG, enterprise-first, consumer), read the Chapter 6 "consumer / PLG / enterprise-first variants" section and adapt the sequence — but hold the trigger-criteria-before-hire principle constant.
- Do not hire ahead of the trigger in the exercise. The whole point of the exercise is to sit with the "not yet" tension and produce the plan that survives it.

## Acceptance criteria

Your submission is complete when:

- [ ] Staging plan has header (dated, signed, versioned, plan horizon).
- [ ] Current GTM org section names every current GTM person by name / role / hire date.
- [ ] Current one-pager signal section cites AE quota attainment, pipeline coverage vs. required, blended CAC + T3M trend, magic number, and the current funnel constraint.
- [ ] At least four proposed hires (or three plus one "not yet" call) are on the plan, each with trigger criteria, current-state readouts, "if not met" contingency, and review cadence.
- [ ] At least one hire on the plan is an explicit "not yet" call.
- [ ] At least three roles in the deferrals section, each with an explicit deferral criterion.
- [ ] VP Sales is in the deferrals section (unless your startup is genuinely at ≥3 AEs each at quota for ≥2 quarters — in which case, name why and cite the numbers).
- [ ] Every trigger criterion is specific and checkable (a number to hit, an artifact to exist by a date, a scorecard verdict to be green).
- [ ] The PMM vs. DG fork (if applicable) has an explicit signal-based choice logic.
- [ ] Board narrative names the plan's total 12-month GTM salary spend.
- [ ] Board narrative names the alternative "hire faster" plan's spend.
- [ ] Board narrative names the specific reason the recommended plan is more defensible, tied to the one-pager numbers.
- [ ] Board narrative includes the specific numerical bet (net-new ARR at current magic number vs. what the alternative would need).
- [ ] Board narrative names the specific review triggers that would change the plan.
- [ ] Ship-checklist review names Pass / Fail per checklist line with the fix applied for every Fail.
- [ ] Reflection names a hardest-to-trigger-criteria-ise hire, a hardest-to-defend deferral, an incoming-VP-GTM pushback, and the one-pager number that would most change the plan.

## Common ways this exercise goes wrong

- **Zero "not yet" calls.** The single most common failure. A plan with only affirmative hires is a hire-everyone plan and produces the over-hire trap.
- **VP Sales on the plan, not in the deferrals.** Unless the trigger criteria (≥3 AEs each at quota for ≥2 quarters) are genuinely met, VP Sales belongs in deferrals. Chapter 6 Pattern 1.
- **SDR hires before the first AE trigger is met.** Chapter 6 Pattern 2. SDRs go on the plan only *after* the first AE is at quota for ≥2 quarters and the SDR is coupled to the *second* AE.
- **First AE on the plan without the mod-105 script / mod-107 motion doc pre-conditions.** Chapter 6 Pattern 3. The founder-artifact hand-off must be in-flight or complete before the AE hire triggers.
- **Trigger criteria that are subjective judgments, not numbers or artifacts.** "Motion feels ready" is not a trigger; "Priya at ≥100% quota for 2 consecutive quarters" is.
- **PMM vs. DG fork with no signal-based logic.** "Hire whichever we find first" is not a plan. State the constraint (volume vs. conversion), then choose.
- **Board narrative with no arithmetic.** The whole point of the paragraph is the specific spend comparison and the specific ARR bet. Hand-waving reads as un-defended and the board will push through it.
- **"Hire faster" alternative not named.** The comparison is the load-bearing move; if you do not name the alternative and its spend, you have nothing to defend against.
- **Plan versioned as "v1" with no compensating discipline note.** If this is your first staging plan, name the weekly / monthly one-pager cadence that will feed v2 in a quarter — otherwise you have shipped an artifact with no operating loop.
- **Skipping the review cadence per hire.** Trigger criteria without a review cadence leave the trigger buried in the founder's head; the monthly one-pager re-read is what surfaces it.
- **Confusing staging with hire mechanics.** The exercise is about *whether to hire and when*, not *how to construct the job description and offer package*. The latter defers sideways to `startup-operations-governance-curriculum`; do not spend the exercise budget there.
