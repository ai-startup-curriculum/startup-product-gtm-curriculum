# Exercise 03 — SPICED and MEDDIC Qualification Drill

**Estimated time:** 3 hours
**Chapter link:** [`03-discovery-call-spiced-and-meddic.md`](../03-discovery-call-spiced-and-meddic.md)
**Prerequisite:** Chapter 3 read end-to-end; Exercise 02 (discovery script + role-play); a working knowledge of the mod-104 ICP scorecard.

## Problem statement

Chapter 3 named the framework choice as ACV-driven — SPICED for mid-market and below (fast cycles, single-buyer or small committee), MEDDIC for larger deals with formal committees ($50K-$250K range), MEDDPICC (adds Paper process and Competition) for enterprise ($250K+). It also named the two failure modes: using SPICED on a $300K enterprise deal that then slips a quarter at procurement no one saw coming, or using MEDDIC's full 8-letter discipline on a $6K self-serve transaction and losing the deal because the buyer felt over-managed.

This exercise trains you to **score 5 real (or realistic) opportunities against both frameworks**, produce a per-opportunity **framework-choice verdict** (SPICED / MEDDIC / MEDDPICC), and populate the **framework-specific qualification worksheet** for each. The output is a working artifact set that shows you can differentiate framework choice by ACV band and can populate each framework's letters with defensible evidence, not vibes.

The failure mode this exercise exists to catch: **the founder treats SPICED and MEDDIC as interchangeable jargon, populates SPICED letters on every deal regardless of ACV, and misses the Economic-buyer / Decision-process / Paper-process discipline that catches enterprise-deal slippage. Or the reverse — populates MEDDPICC on transactional deals and grinds the motion to a halt.**

## Requirements

Deliver a folder `exercise-03/` with:

- `part-a-opportunity-slate.md` — the 5 opportunities scored across the ACV band, with the framework-choice rationale per deal.
- `part-b-qualification-worksheets.md` — one framework-populated worksheet per opportunity.
- `part-c-verdict-and-pattern.md` — the per-opportunity verdict + the pattern-diagnosis across the 5.

### Part A — Assemble the 5-opportunity slate (30 min)

Deliver `part-a-opportunity-slate.md`. Pick 5 real (or realistic) opportunities — ideally drawn from your Exercise 01 accounts, extended with mid-cycle or later-stage detail from role-plays, notes, or actual discovery calls if you have them. If you have no live pipeline, fabricate realistically using your ICP.

**Deliberately span the ACV band.** The distribution must include:

- At least 1 deal at ACV < $10K (SPICED territory, transactional).
- At least 2 deals at ACV $10K-$50K (SPICED territory, small committee).
- At least 1 deal at ACV $50K-$250K (MEDDIC territory).
- At least 1 deal at ACV $250K+ (MEDDPICC territory).

If your product's real ACV distribution does not span these bands, pick the closest fit and note the calibration (a $20K product's "MEDDPICC-equivalent" enterprise deal might be a multi-year multi-team deal at $60K TCV; annotate the reasoning).

For each opportunity, capture:

- **Opportunity ID.** `O01` … `O05`.
- **Company snapshot.** Same shape as Exercise 01 Part A.
- **Named contacts.** Champion, buyer, economic buyer (if known), user (if known). Names, roles, LinkedIn where possible.
- **Where the deal is in the six-stage model** (Prospect / Outreach / Discovery / Demo / Proposal / Close).
- **Estimated ACV** and the cycle length so far (weeks since first meeting).
- **Framework-choice verdict.** `SPICED` / `MEDDIC` / `MEDDPICC`, with a one-paragraph rationale citing Chapter 3's ACV band guidance.

### Part B — Populate the framework worksheet per opportunity (120 min)

Deliver `part-b-qualification-worksheets.md`. For each of the 5 opportunities, produce a framework-populated worksheet in the following shape.

**SPICED worksheet (for opportunities in the < $50K band):**

```
Opportunity: {ID} — {company} — {estimated ACV} — {stage}
Framework: SPICED

S — Situation
  {2-4 sentences: team size, stack, current workflow, geography}
  Source: {discovery call date, LinkedIn research, public engineering blog, etc.}

P — Pain
  {2-4 sentences: specific pain, in the buyer's own language if captured}
  Source: {discovery call quote / paraphrase, or research provenance}

I — Impact
  {2-4 sentences: sized in dollars, hours, missed goals; the arithmetic if worked together}
  Sized number: ${X}/year (or hours/week × people × rate)
  Source: {who provided the number, when}

C — Critical event
  {1-2 sentences: the specific event forcing the decision by a date}
  Date the event triggers: {specific date if known}
  Source: {buyer's statement or inference}

D — Decision
  Champion: {name, title, seniority, why they want this}
  Buyer: {name, title, budget authority}
  Economic buyer: {name if applicable, or "same as buyer at this ACV"}
  User(s): {names or roles}
  Blockers: {any named potential vetos — security, legal, incumbent-owner}
  Decision process: {rough steps and duration}

Coverage verdict: {complete / partial / gap named}
Verdict: {Qualified In (book demo) / Needs second call / Qualified Out — reason code}
Next step (with date): {specific action, specific date}
```

**MEDDIC worksheet (for opportunities in the $50K-$250K band):**

```
Opportunity: {ID} — {company} — {estimated ACV} — {stage}
Framework: MEDDIC

M — Metrics
  {The exact quantitative outcomes the buyer will use internally to justify the purchase}
  Number: {specific — "reduce cycle time by 30%, saving $200K/year"}
  Source: {who articulated the number, when}

E — Economic buyer
  Name: {specific — do not accept "the CFO"}
  Engaged directly: {yes / no / planned}
  Their KPIs: {what the economic buyer is measured on}
  Their decision criteria: {what matters to them specifically}

D — Decision criteria
  {Stated criteria the buyer will use to compare vendors — technical, integration, security, price}
  Gap analysis: {which criteria the product does / does not meet}

D — Decision process
  Step 1: {who, when, duration}
  Step 2: ...
  Full sequence: {mapped from "we're interested" to "signed contract"}

I — Identify pain
  {Same as SPICED's Pain + Impact, but with multiple stakeholders' perceptions captured}
  Champion pain: {...}
  Buyer pain: {...}
  Economic-buyer pain: {...}
  User pain: {...}

C — Champion
  Name: {specific}
  Coached: {what materials they have — ROI doc, talking points, case studies}
  Political capital: {champion's credibility and willingness to spend it}
  Enablement gap: {what the champion still needs from the vendor}

Coverage verdict: {complete / partial / gap named}
Verdict + next step (as above)
```

**MEDDPICC worksheet (for opportunities in the $250K+ band):**

Extend the MEDDIC worksheet with two more sections:

```
P — Paper process
  Legal step: {duration, owner}
  Security review: {duration, owner — start early!}
  Procurement / PO issuance: {duration, owner}
  Total paper-process duration estimate: {weeks}
  Start date: {when the paper process starts — ideally at demo, not at proposal}

C — Competition
  Incumbent solution: {named — "we currently do this in-house" or "we use vendor X"}
  Other vendors evaluated: {named — "also looking at vendor Y and vendor Z"}
  Vendor differentiation per criterion: {where the product wins / loses vs. each}
  "Build in-house" analysis: {is this an option the buyer is considering, and what would it take?}
```

For every letter across all worksheets: if the information is not known, mark it explicitly as `Unknown — resolve on next call via {specific question}`. Do not fabricate.

### Part C — Verdict + pattern diagnosis (30 min)

Deliver `part-c-verdict-and-pattern.md`. Two halves.

**Half 1 — per-opportunity verdict.** For each of the 5 opportunities, produce a one-paragraph verdict:

- Framework coverage: complete / partial / gap named.
- Verdict: Qualified In (with next step) / Needs second call (with specific missing element) / Qualified Out (with reason code from Chapter 7).
- Immediate action: what happens this week.

**Half 2 — pattern diagnosis across the 5.** Write a one-page synthesis answering:

- **Where are the gaps clustering?** Across the 5 opportunities, which framework letters are most-often marked `Unknown`? A cluster on `Economic buyer` or `Paper process` says the discovery script is missing a specific question; a cluster on `Metrics` says the Impact conversation is not sizing pain hard enough.
- **Are the framework choices calibrated?** If a $12K deal is on MEDDPICC, or a $200K deal is on SPICED, name why and correct if wrong.
- **Which deals are actually forecastable this quarter, and which are not?** Based on the framework coverage, name Commit / Best-case / Pipeline for each opportunity (using Chapter 7's classification). Deals with `Unknown` on Critical event or Economic buyer are almost never Commit — the discipline should surface this honestly.
- **What are the two most-common script edits owed** from this drill? Compare to Exercise 02's script; the gaps in Part B are the specific v1.1 improvements.
- **What are the two most-common reason-code disqualifications** you would ship this week if you honestly close-losted the deals that are not moving? The exercise's whole point is that the framework produces decisions, not documentation.

## Starter guidance

- **Framework choice is a real decision, not a preference.** SPICED is not "the easy one"; MEDDIC is not "the enterprise show-off one." Choose against ACV band, cycle length, and committee complexity. A wrong-framework call is a specific gap the exercise catches.
- **Populate `Unknown` honestly.** The exercise's whole point is to surface what you do not know. A worksheet with every letter populated is either a fabricated worksheet or a very-late-stage deal — most real opportunities have 2-4 `Unknown` letters that need to be resolved on the next call.
- **Name the resolving question for every `Unknown`.** An `Unknown` without a specific plan to resolve is a `pre-call research gap`, which is a founder-side failure mode. Name the discovery question that will surface the answer.
- **`M — Metrics` in MEDDIC is stricter than SPICED's `I — Impact`.** Metrics is the exact number the champion will use in the internal deal review — it has to be defensible against the economic buyer's scepticism. If you cannot cite a specific customer or a specific baseline for the metric, sharpen it before shipping.
- **`E — Economic buyer` is where MEDDIC catches enterprise-deal slippage.** Deals that lose "because the CFO said no" almost always never engaged the economic buyer directly. Named + engaged + KPIs-known is the discipline; anything less is a red flag.
- **`Paper process` is often the single longest step of an enterprise deal.** Underestimating it is the most common enterprise-forecast miss. Start security review at demo, not at proposal — and score this specifically in the worksheet.
- **`Champion` in MEDDIC is coached, not passive.** The champion has ROI docs, talking points, case-study snippets. If your champion is "interested and taking meetings but not driving anything internally," the champion designation is wrong.
- **Framework coverage does not equal deal quality.** A fully-populated MEDDIC worksheet on an out-of-ICP deal is a failure of the ICP scorecard, not a success of the framework. Cross-check every opportunity's ICP-fit before rewarding a complete worksheet.
- **The pattern diagnosis is the point.** If Part B produces 5 beautiful worksheets and Part C says "everything is fine," the exercise did not surface anything. Force the gap-cluster analysis.

## Acceptance criteria

Your submission is complete when:

- [ ] Part A contains 5 opportunities spanning the ACV band (at least 1 < $10K, 2 in $10K-$50K, 1 in $50K-$250K, 1 in $250K+).
- [ ] Each opportunity has a framework-choice verdict with a Chapter-3-cited rationale.
- [ ] Part B contains one populated worksheet per opportunity, using the correct framework (SPICED / MEDDIC / MEDDPICC).
- [ ] Every framework letter is either populated with evidence + source, or marked `Unknown — resolve on next call via {specific question}`.
- [ ] MEDDIC / MEDDPICC opportunities have named Economic Buyers (or an explicit "not yet engaged, plan to on next call").
- [ ] MEDDPICC opportunities have populated Paper process and Competition sections.
- [ ] Part C contains a per-opportunity verdict paragraph (framework coverage + verdict + immediate action).
- [ ] Part C contains a one-page pattern diagnosis naming gap-clusters, framework-choice calibration, Commit / Best-case / Pipeline classification, script edits owed, and reason-code disqualifications owed.
- [ ] Every claim in the worksheets that cannot be cited to a source is flagged as `Unknown` rather than fabricated.

## Common ways this exercise goes wrong

- **The framework-interchangeability trap.** Founder populates SPICED letters on every deal, regardless of ACV. Enterprise deals slip; discipline collapses. Fix: framework choice per opportunity, cited to Chapter 3's ACV bands.
- **The over-populated worksheet trap.** Every letter is filled with plausible-sounding content. Half the entries are fabricated. Fix: mark `Unknown` liberally; the honest gaps are the diagnostic signal.
- **The `Unknown`-without-resolution trap.** `Unknown` fields sit without a resolving question. The founder does not know what to ask next. Fix: every `Unknown` has a paired discovery question.
- **The Metrics-hand-wave trap.** MEDDIC's `M` is "reduce cycle time" without a number. Champion has no internal-sale ammunition. Fix: specific number, defensible source.
- **The Economic-buyer-role-only trap.** `E` is "the CFO" without a name. Deal loses at the last step. Fix: named individual; engagement plan.
- **The no-Paper-process-on-enterprise trap.** MEDDPICC deals with `P` skipped or one line. Deal misses the quarter because procurement took 6 weeks. Fix: paper-process mapped step-by-step with owners.
- **The no-Competition trap.** MEDDPICC deals with `C` blank because "we don't have competition" — usually wrong. Even "we'll build it in-house" and "the incumbent solution" are competition. Fix: name all three sources of competition.
- **The framework-coverage-conflated-with-deal-quality trap.** Fully-populated MEDDIC worksheet on an out-of-ICP deal is still an out-of-ICP deal. Fix: cross-check ICP-fit; framework rigor does not save a mis-targeted opportunity.
- **The forecast-inflation trap.** Deals with `Unknown` on Critical event are classified as Commit in the pattern diagnosis. Fix: `Unknown` on the critical letters (Critical event, Economic buyer, Champion) almost always means Pipeline, not Commit.
- **The no-pattern-diagnosis trap.** Part B is beautiful; Part C is skipped or generic. No script iteration signal captured. Fix: gap-clusters, script edits, disqualification decisions — Part C is the point.
- **The wrong-framework-forcing trap.** Founder forces MEDDPICC on a $30K deal because "I want to practice enterprise discipline." Deal grinds; buyer feels over-managed. Fix: framework matches ACV band; practice on a real enterprise deal, not a mis-fit.
- **The role-not-name trap.** Champion / Buyer / Economic Buyer / User all populated with roles. Fix: named humans, LinkedIn URLs where possible, seniority captured.
