# Exercise 01 — Author a One-Page ICP Scorecard

**Estimated time:** 3 hours
**Chapter links:** [`01-what-an-icp-is-and-why-it-must-be-scoreable.md`](../01-what-an-icp-is-and-why-it-must-be-scoreable.md), [`02-firmographic-and-behavioural-criteria.md`](../02-firmographic-and-behavioural-criteria.md), [`03-the-disqualification-checklist.md`](../03-the-disqualification-checklist.md), [`07-icp-scorecard-and-drift-diagnosis.md`](../07-icp-scorecard-and-drift-diagnosis.md)
**Prerequisite reading:** Chapter 1-3 end-to-end; Chapter 7's one-page layout section

## Problem statement

Chapter 1 fixed the operating bar: an ICP that a first sales hire, six weeks in, can use on a live discovery call to make a defensible in-or-out call without escalating to the founder. Chapters 2-3 built the criteria discipline (two-layer scoring + disqualification checklist) and Chapter 7 specified the one-page shipping shape.

This exercise trains you to author a **shippable one-page ICP scorecard** for a real (or realistic) startup, defended against the failure modes each chapter names — the marketing-paragraph ICP, the Layer-1-only ICP, the disqualifier-free ICP.

The output is the artifact a first AE hire could pick up on day one, run against a live discovery call, and score to an in-or-out verdict. If your artifact does not support that action, it has not cleared the module's bar.

This exercise is the seed of the ship artifact revisited in Exercise 04 (beachhead narrowing) and Exercise 05 (drift diagnosis). Exercise 02 layers the persona split on top; Exercise 03 stress-tests the scorecard against real leads. The five exercises together produce the shippable ICP artifact set.

## Requirements

Deliver a folder `exercise-01/` with:

- `part-a-startup-brief.md` — the startup, the raw material you're compressing from.
- `part-b-scorecard.md` — the one-page scorecard.
- `part-c-defence.md` — the criterion-by-criterion defence + failure-mode check.

### Part A — Pick the startup and gather the raw material (45 min)

Pick one of the following:

- **Your own startup** (preferred) — you have the raw material.
- **A public startup** whose customer base and product surface are documented publicly enough to reason about — YC batch companies with case studies, Lenny's Newsletter / First Round Review profiles, launch-year companies with public product hunt / crunch base data.
- **The running Loomly example from the chapters** — extend the ICP into your own defensible authoring; do not simply copy Chapter 7's compressed version.

Whichever you pick, produce `part-a-startup-brief.md` containing:

- Startup name (or working name).
- Product one-liner in your own words.
- Current customer count and revenue band (approx OK).
- The **raw material** the scorecard is compressing from — at minimum:
  - A summary of the mod-101 discovery corpus (10+ interview themes) *or*, if none exists, 5+ simulated buyer sketches drawn from real segment knowledge (label clearly).
  - A summary of the mod-102 PMF cohort characteristics *or*, if no PMF cohort has been measured, the shared traits of the 5 strongest existing customers.
  - The mod-103 positioning document's Component 4 (best-for characteristics) and Chapter 5 (beachhead segment) *or* an equivalent statement of "who we position against and which segment we've committed to."

If your startup has none of the above upstream artifacts, write short synthetic versions of them for this exercise — but note the gap explicitly with `<!-- needs-research: run real mod-101 discovery interviews before shipping this ICP for real -->`. The exercise's output is legitimate practice authoring; it should not be treated as a real ship-artifact if the upstream is missing.

### Part B — Author the one-page scorecard (90 min)

Deliver `part-b-scorecard.md`. Use the exact section shape from Chapter 7 ("The one-page ICP scorecard — the shipping shape"). Every section must be present, even if compressed. The specific requirements per section:

**Metadata line**
- Version, date, owner (real name), one-line version-history entry.

**Beachhead segment (one sentence)**
- Compressed from mod-103 Chapter 5's beachhead choice. If you cannot state the beachhead in one sentence, your upstream work is incomplete — go back to mod-103 before authoring the ICP.

**Disqualifiers (2-4)**
- Each disqualifier: criterion + specific discovery question the AE asks + reason code for close-lost + (optional) unlock condition.
- At least one from each archetype where relevant: whole-product gap, ACV / budget-authority, pain-severity, beachhead-scope.
- The AE is authorised to close-lose against any single disqualifier failure in the first-call verdict — note the authorisation explicitly.

**Layer 1 — firmographic criteria (4-6)**
- Each criterion: exact value/range + weight (must-have / weight-3 / weight-2 / weight-1) + data source it's filterable from.
- Every criterion must be answerable from a third-party lookup (LinkedIn, Crunchbase, BuiltWith, ZoomInfo, Apollo, PitchBook) without a conversation. If a criterion cannot be filtered from a data source, either drop it or move it to Layer 2.

**Layer 2 — behavioural criteria (3-5)**
- Each criterion: description + weight + the specific 15-25-word discovery question that surfaces the answer in ≤ 90 seconds.
- Every behavioural criterion must have a stated provenance: mod-102 PMF cohort, mod-101 discovery corpus, or structural product constraint.

**Personas (placeholder in this exercise; Exercise 02 develops them fully)**
- For this exercise, list buyer / user / champion titles and the "who to identify" question. Full development in Exercise 02.

**Three-axis routing (reference the Chapter 5 verdicts; full application in Exercise 03)**
- List the six routing verdicts and the AE action per verdict.

**Not-now segments (placeholder in this exercise; Exercise 04 develops them fully)**
- List three named not-now segments with one-line "why not" per. Full development in Exercise 04.

**Operating cadence**
- The weekly / monthly / quarterly cadence per Chapter 7. Named owners.

**Total scorecard length:** one screen. If it does not fit, cut ruthlessly — the exercise's discipline is compression. A three-screen scorecard has failed the bar.

### Part C — Criterion-by-criterion defence (45 min)

Deliver `part-c-defence.md`. For each criterion in Part B (both Layers, plus disqualifiers), one paragraph of defence answering:

- **Provenance.** Where did this criterion come from? (mod-102 cohort? mod-101 corpus? product constraint? founder intuition — if the latter, flag it.)
- **Scoreable test.** How does the AE actually score it — the exact question, the data source, or the observable signal?
- **Cost of dropping it.** What sales failure would happen if this criterion were absent from the scorecard? (If none — drop it.)
- **Cost of keeping it wrong.** What would happen if the criterion is authored incorrectly — false positives (deals let through that should have been disqualified) or false negatives (deals disqualified that should have been let through)?

At the end of Part C, run the **six failure-mode check** (Chapter 1's Common failure patterns):

1. Is the scorecard a *marketing paragraph* in disguise? Test: can you find 3+ pieces of copywriter-language ("modern," "best-in-class," "high-growth") that are not scoreable? If yes, rewrite them.
2. Does the ICP try to serve *multiple segments*? Test: is the beachhead one segment, or three "or" segments smuggled into one line? If the latter, pick one; the others go on the not-now list.
3. Are any *person-level attributes* in the company-level scorecard? Test: does any Layer 1 or Layer 2 criterion describe a person rather than a company? If yes, lift to the persona section.
4. Is the ICP *aspirational* — requiring unshipped product? Test: do any criteria imply features / integrations / compliance the product does not have today? If yes, mark as future-tier and drop from current-ICP.
5. Are there disqualifiers? Test: are there 2-4 must-haves that hard-fail the deal? If zero, add them.
6. Does the scorecard fit on **one page / one screen**? Test: paste into a Notion doc; check it fits above the fold on a 1440×900 screen. If not, compress.

Note the result of each of the six checks. Any failure requires a specific edit; either produce v0.2 with the edits applied, or note the specific unresolved issue.

## Starter guidance

- **Do the upstream work first, or borrow it.** The ICP is a *compression* of mod-101, mod-102, mod-103 outputs. Without those inputs, the exercise's outputs will be founder-intuition guesses. If you don't have real upstream artifacts, synthesize summary versions in Part A but flag the gaps.
- **Start with Layer 2, not Layer 1.** Founders default to firmographic criteria because they feel objective. But Layer 2 is where the ICP has real discriminating power — start there, drive out the two or three behavioural criteria that separate strong-fit from weak-fit customers you actually know, and use those to constrain the Layer 1 criteria.
- **Draft the disqualifiers first, not last.** The most-common failure mode is a disqualifier-free ICP. Author the 2-4 disqualifiers early — before you get sentimental about the qualifying criteria — using the four archetypes as a checklist.
- **Bound the count aggressively.** 4-6 firmographic + 3-5 behavioural + 2-4 disqualifiers is the working range. If your first pass has 12 criteria, pick the load-bearing subset; the others are usually correlated with the load-bearing ones and are decoration.
- **Test each criterion against your best current customer.** Score your top current customer against your draft ICP. Does the ICP correctly rate them as strong fit? If not, the ICP is broken. Score your worst-fit current customer (a churn risk or difficult account). Does the ICP correctly flag them? If not, the ICP is broken.
- **Test each criterion against the demand-gen view.** Take your Layer 1 criteria into LinkedIn Sales Navigator. Can you build a target list from them? If a criterion cannot be filtered in Sales Navigator or an equivalent third-party tool, it does not belong in Layer 1 — either move to Layer 2 or drop.
- **The one-page constraint is not aesthetic.** An AE on a discovery call cannot navigate a three-tab document. The compression is what makes the artifact usable. If you find yourself wanting to write more, the sub-page is the linked mod-101 / mod-102 / mod-103 document — the ICP is the compression.
- **Do not write the persona section in full here.** Exercise 02 develops the personas. In Part B, list titles and identification questions; full authoring belongs in the next exercise. Trying to author the personas in this exercise inflates the scorecard past the one-page bar.
- **Do not write the full not-now section here.** Exercise 04 develops the not-now list. In Part B, name the three segments with one-line "why not"; the full detail (unlock condition, meanwhile action, revisit trigger) is in the next exercise.
- **Flag every unsourced claim.** If you cite a "80% of PMF cohort had this" figure that you cannot trace to an actual mod-102 cohort analysis, mark it `<!-- needs-research: verify against actual cohort -->`. The gaps are the exercise's most useful output — they name the empirical work you still owe.

## Acceptance criteria

Your submission is complete when:

- [ ] Part A names the startup, includes the raw material (mod-101 corpus summary + mod-102 cohort summary + mod-103 positioning + beachhead) or explicitly flags the gaps.
- [ ] Part B is a one-page scorecard using Chapter 7's exact section shape — metadata, beachhead, disqualifiers, Layer 1, Layer 2, personas (placeholder), routing, not-now (placeholder), operating cadence.
- [ ] The scorecard fits on **one screen** (approx 60-80 lines including formatting).
- [ ] There are **2-4 disqualifiers**, each with (a) criterion, (b) specific discovery question, (c) reason code, and where applicable (d) unlock condition. The AE authorisation to close-lose is explicitly noted.
- [ ] Layer 1 has **4-6 firmographic criteria**, each with a specific value/range, a weight, and a stated data source. Every criterion is filterable in a third-party data tool without conversation.
- [ ] Layer 2 has **3-5 behavioural criteria**, each with a specific 15-25-word discovery question and a stated provenance (mod-102 cohort / mod-101 corpus / structural product constraint).
- [ ] Part C defends every criterion (in both Layers + disqualifiers) with provenance, scoreable test, cost-of-dropping, cost-of-wrong-authoring.
- [ ] Part C runs the six failure-mode checks and notes the outcome of each with any required edits applied or flagged.
- [ ] Any criterion that cannot be defended without a factual claim is flagged with `needs-research` rather than inventing the fact.
- [ ] The version / date / owner metadata is present. An undated / unowned scorecard fails the exercise regardless of content quality.

## Common ways this exercise goes wrong

- **Marketing paragraph in Layer 2 clothing.** "Companies with a modern engineering culture" is a marketing paragraph. Even if it's in the Layer 2 section, if it can't be scored, it's decoration. Every criterion must have a specific answer to a specific question.
- **Twelve criteria because they all felt important.** The 12-criterion scorecard is the AE-friendly-looking version that no AE actually uses in real time. 6-8 is the working ceiling across both layers. Compress.
- **No disqualifiers because "we don't want to lose good deals."** The disqualifier-free ICP inflates the pipeline 3× and drops close rate 2×. Missing disqualifiers cost more than they save. 2-4, per Chapter 3.
- **Every criterion is "must-have."** The scoring collapses (a deal missing any criterion fails); the ICP over-disqualifies. Only 2-4 must-haves; the rest are weighted.
- **Person-level attributes in the company-level scorecard.** "Growth-mindset engineering leaders" is a persona attribute, not a firmographic one. Lift to Chapter 4 / Exercise 02's persona section.
- **Layer 1 criteria not filterable.** "Companies that value velocity" is not filterable in Sales Navigator. Every Layer 1 criterion should be resolvable from a specific third-party field.
- **Layer 2 criteria without discovery questions.** "Team has strong metric ownership" is a rating, not a question. The AE needs the exact words to say: "does anyone on your engineering leadership team have a throughput or cycle-time KPI they report up?"
- **Aspirational ICP that requires unshipped product.** "Fortune 500 healthcare CIOs" is not the ICP; it's the roadmap. Current-ICP is what you can win today.
- **Scorecard longer than one page.** If it doesn't fit on one screen, it's not the shipping artifact — it's the research document. Compress.
- **No provenance.** Every criterion without a mod-102 / mod-101 / product-constraint source is a founder guess. Provenance discipline is what keeps the ICP empirical.
- **No AE authorisation clause.** The scorecard exists but the AE has to escalate every close-lost to the founder. The authorisation is what makes the disqualifier operational.
- **Missing metadata line.** No version, no date, no owner. The scorecard drifts silently. Add the metadata.
- **Full persona authoring in this exercise.** Personas are Exercise 02. Placeholder here; full authoring next. Trying to do both bloats the scorecard.
