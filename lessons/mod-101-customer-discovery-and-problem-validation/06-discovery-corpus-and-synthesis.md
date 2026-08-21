# The Discovery Corpus — Notes, Synthesis, Theme Index

## Motivation

The most avoidable failure mode of a discovery push is not a bad interview — it is a good interview that vanishes. Twenty conversations happen; twenty transcripts sit in twenty different places; three months later a co-founder joins and asks *"which customers actually said the payment-chasing thing?"* and the founder cannot answer without re-interviewing.

The fix is a **structured corpus**: one note per person, one written synthesis every five interviews, and one running theme index that is updated as new interviews arrive. All three artifacts are cheap to build if you build them as you go and impossibly expensive to reconstruct after the fact.

This chapter is the file-management chapter of the module. It is not glamorous. It is the reason a discovery push is worth anything six weeks after the interviews.

## Core concepts

### Three artifacts, three cadences

The corpus has exactly three artifacts, updated on three different cadences. Do not add more; do not skip any.

| Artifact | Cadence | Purpose |
|---|---|---|
| **Interview note** | one per interview, written same day | Preserves the specific transcript in searchable form so any claim in the synthesis can be traced back to a source line |
| **Synthesis memo** | one per five interviews | Turns raw notes into an updated pattern read — what changed since the last five, what stayed |
| **Theme index** | one file, updated after each synthesis | The running spine — a de-duplicated list of every job, force, and outcome, each with pointers to the transcripts that support it |

A single writer can maintain all three in an afternoon per five-interview batch. The batch cadence is what makes it sustainable — you never sit down to synthesise twenty at once.

### The interview note — one file per interviewee

Write it the **same day**, before you sleep. The template — copy this to a template file and re-use it — has six sections:

```markdown
# [Interviewee name / handle] — [YYYY-MM-DD]

## Context
- Role, company (size, industry), how recruited (personal / referred / community / cold)
- Screening confirmation — do they actually fit the ICP as recruited?
- Interview type: problem / solution / product
- Duration, medium (video / phone / in-person)
- Consent to record? Recording link if yes.

## Their current-state workflow
- [Direct quotes and specific past-tense descriptions of how they do the workflow today]
- [Named tools they use, integrations, workarounds]
- [Volume / frequency / cost — the three Mom Test diagnostics]

## Pain and workarounds
- [Specific instances they described, with dates or approximate recency]
- [What they did about each — action, not opinion]
- [Emotional / social dimension where it came out]

## Jobs / outcomes surfaced (Chapter 4 language)
- [Christensen-shape statement 1, in their words if possible]
- [Ulwick-shape outcome 1, marked with importance/satisfaction if it came out]

## Forces (if a switch story came up)
- Push:
- Pull:
- Anxiety:
- Habit:

## Commitment given at end
- What they said yes to (referral / follow-up / prototype session / LOI / deposit)
- Referrals volunteered — names + intros?

## My editorialising (kept separate)
- What surprised me
- What I want to test next
- What I would ask them differently if I could re-run
```

**The single most important rule about the interview note: keep the editorialising in its own section.** Founders rewrite history. If the "what they said" section is polluted with the founder's interpretation, the note becomes unreliable and the synthesis compounds the unreliability.

If you recorded the call, drop the transcript in an appendix. Do not lean on the transcript instead of the note — the note is the compressed, categorised form your future self will actually read.

**One naming convention.** Use a stable file name pattern like `2026-08-14-alex-em-tectonic.md` — date first for sortability, name + role + company slug for skimmability. If you cannot use the interviewee's real name for privacy reasons, use a stable pseudonym; refer to them by that pseudonym everywhere in the corpus.

### The synthesis memo — one per five interviews

Every five interviews, sit down and write a **synthesis memo**. It is one to two pages. Template:

```markdown
# Synthesis — interviews N-4 through N — [YYYY-MM-DD]

## New signal since last synthesis
- [Themes that appeared for the first time or grew notably stronger]
- [Themes that faded — mentioned less than last batch, or contradicted]

## Confirmed patterns
- [Themes that were in the last synthesis and are still holding]

## Contradictions
- [Interview A said X; interview B said not-X. Which segment does each fall into? Is the segmentation the confounder?]

## Segment drift
- Are the last 5 interviews actually the same segment as the first N-5? If not, is that intentional (mini-pivot in progress) or accidental (recruit-your-friends bias)?

## Solution-shape hypotheses updated
- Which candidate shapes look stronger? Which look weaker?

## Kill-list — hypotheses this batch killed
- [Explicit "we thought X; we now believe not-X because of these three transcripts"]

## What I'd change about my interviews next batch
- Questions to add, questions to drop, ICP to tighten
```

The **kill-list** is the memo's most important section. Discovery is worth the time it takes only if it kills bad hypotheses cheaply. The kill-list is where you make that explicit — hypothesis X, three sources that killed it, so we stop investing in it.

The batch of five is the right cadence for two reasons:

- Fewer than five and the pattern is noise (one loud interviewee dominates).
- More than five and you cannot hold the details in your head; you skim your own notes.

### The theme index — one running file

The theme index is a single markdown file (or a spreadsheet — either works) that lists every theme surfaced across the whole corpus, deduplicated, with pointers to the source interviews. Template:

```markdown
# Discovery theme index — as of [YYYY-MM-DD]

## Jobs
| # | Job statement (Christensen shape) | Sources | Times mentioned |
|---|---|---|---|
| J1 | When [situation], I want to [motivation], so I can [outcome] | 2026-08-14-alex; 2026-08-16-bruno; 2026-08-20-cara | 3 |

## Outcomes
| # | Outcome statement (Ulwick shape) | Importance | Satisfaction | Sources |
|---|---|---|---|---|
| O1 | Minimise the time to identify owner of a stalled PR review | high | low | J1 sources + 2026-08-21-dee |

## Forces observed
| # | Force type | Description | Sources |
|---|---|---|---|
| F1 | Push | "junior engineer lost a sprint waiting for a review" | 2026-08-14-alex |
| F2 | Habit | "we've been on GitHub-only for years — process debt aversion" | 2026-08-16-bruno; 2026-08-20-cara |

## Disqualifying signals
| # | Signal | Description | Sources |
|---|---|---|---|
| D1 | Segment mismatch | "our review latency is fine — 4 hours median" (large-team ICP) | 2026-08-18-erin |

## Killed hypotheses
| # | Hypothesis | Killed by | Batch |
|---|---|---|---|
| K1 | "Founders will want a weekly summary email" | 2026-08-14-alex; 2026-08-16-bruno both waved it off | Batch 2 (interviews 6-10) |
```

The theme index is the artifact a co-founder or first hire reads instead of interviewing thirty people from scratch. **The pointer column is the whole reason this file is useful.** Any claim in the index can be traced back to a specific interview note; any interview note can trace back to a specific quote or recording moment.

### One convention across the corpus — the same vocabulary

Nothing destroys a discovery corpus faster than inconsistent vocabulary. If you sometimes write "invoice chasing", sometimes "AR follow-up", and sometimes "getting paid", the theme index cannot deduplicate. Decide once — early — on the canonical terms for the top five nouns and top five verbs in your problem space, and enforce them across every artifact.

The Chapter 4 pipeline (transcripts → jobs → outcomes) is the natural source of this vocabulary; the outcomes are worded once and every note references the same wording.

### Where to store the corpus

Practical constraints matter. Two rules:

- **Everything in one place, versioned.** A private Git repo, a shared Notion, a shared Google Drive folder. Not scattered across Docs, email, and Notes-app.
- **Consent-aware.** If interviewees asked for confidentiality, honour it — redact company names, use pseudonyms, keep recordings out of shared drives if the ask required it. Note the consent status in the Context section of each interview note.

Tooling is not the interesting question at n<50. The interesting question is whether you are writing at all.

### An LLM-assisted synthesis is a first draft, not the artifact

If you use a language model to draft synthesis memos from transcripts, treat the output as a **first draft you then edit against the source notes**. Two failure modes to watch:

- **Hallucinated attributions.** The model may attribute a quote to the wrong interview. Trace every attribution back to the note before it enters the theme index.
- **Averaging away the outliers.** The model tends to summarise the modal opinion; the outlier stories (the failed switch, the strong dissent, the disqualifying signal) are often the most valuable and get lost. Read the source notes for outliers by hand.

The corpus is only worth anything if you can defend every claim in it against the transcripts. LLM-drafted memos that cannot be defended that way are a liability, not an asset.

## Concrete example — a corpus after 15 interviews

The code-review-tool founder from previous chapters, at week 6:

- `notes/` — 15 markdown files, one per interviewee, ~1 page each, all following the template.
- `synthesis/2026-08-15-batch-1.md` — synthesised interviews 1–5. Kill-list: "solo-EMs at <10-person teams are not the ICP; latency is not a pain at that scale."
- `synthesis/2026-08-22-batch-2.md` — synthesised interviews 6–10. Kill-list: "weekly summary email is not the shape; users want an in-workflow intervention."
- `synthesis/2026-08-29-batch-3.md` — synthesised interviews 11–15. Kill-list: "self-serve installation via a bot is a table-stakes constraint; enterprise SSO can wait but GitHub App install cannot."
- `theme-index.md` — one file, ~3 pages, listing jobs J1–J7, outcomes O1–O9, forces F1–F12, disqualifying signals D1–D4, killed hypotheses K1–K6, all with source pointers.

A new co-founder joining in week 7 reads the theme index (10 minutes), skims the three synthesis memos (30 minutes), and pulls two of the interview notes for detail (15 minutes). She is now caught up. **No re-interviewing.** That is the whole payoff.

## Common failure patterns

- **Notes written from memory a week later.** They are wrong. Write same day.
- **Editorialising blended with facts.** Any reader downstream cannot tell what the interviewee actually said. Keep the sections separated.
- **No batch synthesis.** Founder has 40 notes and no synthesis; the corpus is unreadable and no one uses it.
- **Theme index updated once and abandoned.** After every synthesis, update it. Otherwise it drifts out of date within a batch.
- **Every interview note in a different format.** Deduplication becomes impossible. Use the template.
- **The transcript replaces the note.** Recordings are for evidence; notes are for reading. You will not re-listen to 20 hours of tape at week six. Write the note.

## Summary

- Three artifacts, three cadences: **interview note** (one per person, same day), **synthesis memo** (one per five interviews), **theme index** (running, updated after each synthesis).
- The **kill-list** in every synthesis is the memo's most important section. Discovery pays off only if it kills bad hypotheses.
- The **pointer column** in the theme index is what makes the artifact defensible — every claim traces back to a note; every note traces back to a quote or recording.
- Keep facts and editorialising in separate sections of the note. Use one canonical vocabulary across the corpus.
- LLM-drafted synthesis is a first draft. Trace attributions by hand and watch for lost outliers.
- The corpus payoff is that a co-founder or first hire can act on the discovery **without re-interviewing**.
