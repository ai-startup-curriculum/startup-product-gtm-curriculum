# Exercise 04 — JTBD Outcome Statement Authoring

**Estimated time:** 3 hours
**Chapter link:** [`04-jobs-to-be-done-outcomes.md`](../04-jobs-to-be-done-outcomes.md)
**Prerequisite:** completed Exercise 03 (or another corpus of ≥5 interview notes)

## Problem statement

Chapter 4 taught the JTBD vocabulary — Christensen-shape job statements, Ulwick-shape outcome statements, and the four forces of progress. This exercise operates the pipeline: turn the transcripts you produced in Exercise 03 into a de-duplicated list of jobs, outcomes, and forces that can *reject* a proposed solution.

The output of this exercise is the JTBD half of the discovery report (Chapter 7); it will be reused in Exercise 05 and, if you continue to project-101, in the ICP and founder-led-sales work.

## Requirements

Deliver a single markdown file `exercise-04-jtbd.md` under your working folder, containing four sections. Every claim in every section must be cited to specific interview IDs from Exercise 03.

### 1. Candidate jobs (Christensen shape) — 30 minutes

For each interview note from Exercise 03:

- Highlight every phrase that describes a specific action taken, a specific pain felt, or a specific outcome wanted.
- Turn each into a candidate job in the shape *"When [situation], I want to [motivation], so I can [outcome]."*
- Cite the interview ID and the source phrase for each candidate.

Aim for 15–30 candidate statements across five interviews. Duplication at this stage is fine — deduplication happens in step 2.

### 2. Deduplicated jobs — 30 minutes

Cluster the candidates from step 1. Two candidates that describe the same underlying job — even in different words — become one. Deliver:

- 3–7 deduplicated job statements.
- For each, the list of source interview IDs that support it (from the candidate list).
- Rewrite the surviving job statements so they are **product-agnostic** — no mention of your product, no mention of a specific tool. Any of ten different solutions should be able to hire in against a well-written job.

### 3. Outcome statements (Ulwick shape) — 45 minutes

For each deduplicated job, author 1–3 **outcome statements** in the Ulwick shape:

> _[direction of improvement]_ the _[metric]_ of _[unit of measure]_ _[context]_.

For each outcome:

- Write it out. Verify all four parts are present (direction, metric, unit, context).
- Score **importance** (high / medium / low) — from the corpus, how much did interviewees emphasise it?
- Score **satisfaction with current solutions** (high / medium / low) — from the corpus, how well are today's tools handling it?
- Star (**\***) any outcome that is **high-importance / low-satisfaction** — the underserved outcomes are where opportunity lives (Chapter 4).
- Cite the interview IDs that justify the importance and satisfaction scores.

Aim for 5–12 outcome statements total; expect 2–5 stars.

### 4. Forces observed (Chapter 4) — 30 minutes

For every interviewee who described a switch story (they moved from one solution to another, or considered it and did not), record their forces in the four-column table format:

| Interview ID | Push | Pull | Anxiety | Habit |
|---|---|---|---|---|

If none of your interviewees had a switch story, that is itself a finding — record it explicitly ("no switch stories in this batch; ICP has been on current-state workflow for years") and note that Exercise 03 batch 2 should recruit for that specifically.

### 5. Solution rejection drill — 30 minutes

Propose **three plausible solutions** for the problem space you interviewed against. For each, score against the outcome list from step 3:

- Which starred outcomes does the solution move?
- Which starred outcomes does it *not* move?
- On the importance-vs-satisfaction map, is this solution attacking an underserved outcome or a served one?
- Verdict: **build**, **iterate**, or **reject** — with a one-sentence reason grounded in the outcome scoring, not in the founder's taste.

At least one of the three proposed solutions should be one you would have believed was worth building before this exercise. If all three survive the rejection drill, either your outcomes are too weakly scored or your solutions are too safely chosen — try again with one solution that would move only served outcomes so you can practise the rejection.

### 6. Reflection (~15 min)

A short closing paragraph:

- Which of the outcomes surprised you? (You expected it not to be starred and it was, or vice versa.)
- Which forces dominated in the switch stories? Was habit or anxiety the bigger blocker?
- If you had to describe the highest-signal underserved outcome in a single sentence for a first hire, what would that sentence be?

## Starter guidance

- Print your five interview notes (or open them side-by-side). The clustering step is much easier when you can literally see the highlighted phrases in front of you at once.
- The hardest step is 2 (deduplication) — resist the urge to keep candidates as separate jobs just because the words are different. Two phrasings of the same underlying job are one job.
- The second-hardest is 3 (Ulwick shape) — most first-draft outcome statements are missing a metric or a unit. Re-read the Chapter 4 examples and check every outcome has all four parts.
- The rejection drill (step 5) is the whole point. If it feels awkward to reject a solution you like, that is the exercise doing its job.
- Do not synthesise outcomes that are not supported by the corpus. If you find yourself writing an outcome and cannot cite a source, delete it — you are pattern-matching to the founder's intuition, which is what the pipeline exists to check.

## Acceptance criteria

Your submission is complete when:

- [ ] Step 1 has 15–30 candidate job statements, each cited to an interview ID and source phrase.
- [ ] Step 2 has 3–7 deduplicated, product-agnostic Christensen-shape job statements with source lists.
- [ ] Step 3 has 5–12 Ulwick-shape outcome statements — each with direction, metric, unit, context — scored on importance and satisfaction, with 2–5 starred and citations for each score.
- [ ] Step 4 records forces for every switch story, or explicitly names the absence of switch stories as a finding.
- [ ] Step 5 has 3 proposed solutions with per-solution outcome scoring and a **build / iterate / reject** verdict; at least one solution is rejected.
- [ ] Reflection paragraph names at least one surprise and one dominant force from the switch stories.

## Common ways this exercise goes wrong

- **Job statements that mention the product.** *"When a user opens our dashboard, they want..."* is a product statement. Rewrite without any product reference.
- **Outcome statements without a metric.** *"Users want a better experience"* fails the shape. Every outcome needs direction + metric + unit + context.
- **Cluster count that hides real diversity.** Deduplicating aggressively down to 2 "big" jobs loses information. If the underlying motivations differ, keep them separate.
- **Rejection drill where nothing gets rejected.** You have chosen safe solutions or scored outcomes too weakly. Add a fourth solution designed to be rejected and practise the move.
- **Outcomes invented rather than sourced.** Every outcome must trace to interview evidence. Invention here contaminates the discovery report downstream.
