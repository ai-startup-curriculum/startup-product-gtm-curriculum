# Exercise 05 — Discovery Corpus Synthesis

**Estimated time:** 3 hours
**Chapter links:** [`06-discovery-corpus-and-synthesis.md`](../06-discovery-corpus-and-synthesis.md), [`07-shipping-the-discovery-report.md`](../07-shipping-the-discovery-report.md)
**Prerequisite:** Exercises 03 and 04 complete; ideally a second batch of five interviews as well, but the exercise works at n≥5

## Problem statement

You now have a corpus — interview notes, at least one synthesis memo, a JTBD outcomes list. This exercise assembles them into the shape that a co-founder or first hire can act on **without re-interviewing anyone**: a running **theme index** and a v0 draft of the **discovery report** structure from Chapter 7.

This is the module's ship-quality synthesis exercise. If you have ≥15 interviews (the target for the full module lab), you write the full discovery report. If you have 5–14, you write the theme index and a v0 discovery-report scaffold with each section stubbed.

## Requirements

Deliver a folder `exercise-05/` with:

- `theme-index.md` — the running theme index (Chapter 6 template).
- `discovery-report-v0.md` — the v0 discovery report scaffold (Chapter 7 template).
- `synthesis-batch-N.md` — a fresh synthesis memo if you have not written one for the most recent batch.
- `defensibility-audit.md` — a short audit that traces every claim in the discovery report back to the corpus.

### 1. Theme index (Chapter 6) — 60 minutes

Build the theme index as a single markdown file with the tables from Chapter 6:

- **Jobs table** — every deduplicated Christensen-shape job with source pointers and mention count.
- **Outcomes table** — every Ulwick-shape outcome with importance, satisfaction, and source pointers; underserved outcomes starred.
- **Forces table** — every observed force with type, description, and source pointer.
- **Disqualifying signals table** — observable properties of a prospect who *looks* like the ICP but is not, with source pointers.
- **Killed hypotheses table** — every hypothesis you now believe is dead, with the interview IDs that killed it and the batch in which it was killed.

Every row in every table must have at least one interview-ID citation. If a row cannot be cited, delete it — it is intuition, not evidence.

### 2. Discovery-report scaffold (Chapter 7) — 60 minutes

Draft the discovery report skeleton with all six sections from Chapter 7. For each section, either write the full content (if your corpus size supports it) or write a v0 stub with a `<!-- needs-more-interviews: ... -->` note explaining what additional evidence you need:

1. **Problem statement** — 1 paragraph, filled using the Chapter 7 template (who, situation, current workflow, cost, why unsolved). If the corpus does not yet support all five fields, stub each with a `needs-more-interviews` note.
2. **Top jobs (2–4)** — the highest-signal jobs from the theme index, with per-job source citations.
3. **Top outcomes (3–6)** — the starred outcomes from step 1, with importance / satisfaction scoring.
4. **Top forces summary** — the recurring push / pull / anxiety / habit patterns across switch stories.
5. **Disqualifying signals** — the observable properties of a wrong-fit prospect; must include at least three disqualifiers or an explicit note that the corpus is too thin to surface them yet.
6. **Three testable hypotheses for the next round** — each in the Chapter 7 shape (*we believe X; we would know we are wrong if Y; next action is Z*). Each hypothesis must be falsifiable — a specific observable outcome, not a vague direction.

Length target: 3–6 pages if the corpus supports the full report; 1–2 pages if it is a scaffold.

### 3. Fresh synthesis memo (if applicable) — 30 minutes

If the most recent batch of five has not been synthesised yet (you ran interviews 6–10 after Exercise 03, for example), write a synthesis memo now, using the Chapter 6 template. Emphasise the **kill-list** — hypotheses this batch killed relative to the previous batch.

### 4. Defensibility audit — 30 minutes

Pick **five claims** from the discovery-report scaffold. For each claim, trace it back to:

- The interview note(s) that support it.
- The specific source phrase(s) in each note that support it.
- The theme-index row that references it.

Deliver as a table in `defensibility-audit.md`:

| Claim | Source note(s) | Source phrase(s) | Theme-index row |
|---|---|---|---|

If any of the five claims cannot be defended this way, rewrite it in the report until it can be — or delete it.

## Starter guidance

- The theme index is the load-bearing artifact for this exercise. Build it first; the report scaffold is a derived view of the index.
- The vocabulary discipline from Chapter 6 pays off here. If the same concept is called two different names across your notes, the index cannot deduplicate. Normalise the vocabulary as you build the index; propagate the fix back into the notes if needed.
- The **disqualifying signals** section is the one most learners skip. It is also the section that a first sales hire will thank you for. Force yourself to write at least three, even if the corpus is thin — mark them provisional and cite the source, but do not skip the discipline.
- Do not write hypotheses that are not falsifiable. "Users will love the auto-reassign feature" is not a hypothesis; "if fewer than 6 of 10 solution-interview EMs prefer auto-reassign to a dashboard when shown three artifacts, we abandon that shape" is.
- If you do not yet have 20 interviews, the module lab (`lab-01-publish-a-discovery-report-for-one-startup`) is where the report becomes shippable. This exercise is the intermediate scaffold.

## Acceptance criteria

Your submission is complete when:

- [ ] `theme-index.md` has all five tables (jobs, outcomes, forces, disqualifying signals, killed hypotheses) with source pointers on every row.
- [ ] `discovery-report-v0.md` has all six Chapter 7 sections; each is either fully written or stubbed with a specific `needs-more-interviews` note.
- [ ] The problem-statement paragraph names the ICP with a behavioural qualifier, the situation, current workflow, cost, and why unsolved — or notes which of those five need more evidence.
- [ ] The three hypotheses are each in the *we believe X / would know wrong if Y / next action Z* form and each has a specific, observable falsifier.
- [ ] The defensibility audit table has five rows; every claim traces to specific notes, specific phrases, and a theme-index row.
- [ ] The document dated, signed, and labelled v0 or v1 per the Chapter 7 versioning rule.

## Common ways this exercise goes wrong

- **Theme-index rows without source pointers.** The index is defensible only if every claim traces to a note. Rows without pointers are inadmissible.
- **Hypotheses that name a solution.** "H1: users will love auto-reassign" is a wish. "H1: an in-workflow escalation lands where a dashboard does not — falsified if 5 of 10 solution-interview EMs prefer the dashboard artifact" is a hypothesis.
- **Skipping disqualifiers.** Downstream, the first sales hire will not know how to say no. Even a provisional disqualifier list is better than none.
- **The report reads as neutral.** Discovery is opinionated (Chapter 7). Take a position; cite the corpus.
- **The report is 30 pages.** The reader will not open it. 3–6 pages, ruthlessly cut.
- **Defensibility-audit skipped or done for softball claims.** Pick the five *most load-bearing* claims — the ones that would kill the whole thesis if they were wrong. Audit those.
