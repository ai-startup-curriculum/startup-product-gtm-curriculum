# Exercise 01 — PMF vs. Traction Diagnostic

**Estimated time:** 2 hours
**Chapter links:** [`01-what-pmf-means.md`](../01-what-pmf-means.md), [`02-anecdotal-traction-vs-pmf.md`](../02-anecdotal-traction-vs-pmf.md)
**Prerequisite reading:** [Marc Andreessen — "The Only Thing That Matters" (2007)](https://pmarchive.com/guide_to_startups_part4.html) (~15 min); [Andy Rachleff — "Product/Market Fit: What it really means" (Wealthfront blog)](https://www.wealthfront.com/blog/product-market-fit/) (~10 min)

## Problem statement

The single most damaging Chapter 2 mistake is treating a **loud, salient anecdote** as evidence of product-market fit. This exercise drills the diagnostic reflex from Chapter 2: given a pile of "our startup is going great" signals, classify each as **PMF signal**, **anecdotal traction (routes to a specific downstream module)**, or **noise** — and back the classification with the specific move Chapter 2 recommends (cohort, isolate, check what sustains).

You will run the diagnostic against **two founder pitches** — one you construct and one provided — and then against **your own startup or a public one** you pick.

## Requirements

Complete all three parts. Deliver as a single markdown file `exercise-01-pmf-vs-traction.md`.

### Part A — Diagnose the provided pitch (30 min)

The following is a lightly-fictionalised founder update. Diagnose it.

> **Founder update, Q3 2026:**
>
> *We had an amazing quarter. Our launch on Product Hunt drove 3,400 signups in one weekend — we hit #2 for the day. Our angel investor (60k Twitter followers) posted a thread about us that got 12k likes. We closed three design-partner LOIs from top-tier fintechs — Company X, Company Y, and Company Z — and the CTO at Company X sent us a personal note saying "this is exactly what we've been waiting for". Weekly signups are up 8x since the launch. We think we have product-market fit and are ready to hire two AEs and start our Series A raise.*

For each of the five signals in the update, produce:

1. **The signal.** Quote the exact language.
2. **What it is evidence of.** Per Chapter 2's "what each row is evidence of" column.
3. **What it is *not* evidence of.** Per the "not evidence of" column.
4. **The diagnostic move.** The specific cohort/isolate/check-what-sustains move the founder should run before believing the signal is PMF signal.
5. **Verdict.** One of: **PMF signal**, **anecdotal traction (route to \[module\])**, **noise**, or **insufficient data — need X**.

Then answer the meta question: **is the "we have PMF and are ready to raise" claim in the update defensible from the evidence presented?** In one paragraph, with a reason grounded in Chapter 1's Rachleff and Andreessen frames.

### Part B — Construct a pitch that hides no-PMF behind three loud signals (30 min)

Write a 1-paragraph founder update in the same shape as Part A that would be genuinely persuasive to a lay reader but that hides three of the following underlying facts (pick which three):

- Retention curve decays to zero by W6.
- Sean Ellis "very disappointed" on 400 signups (not filtered to actives) is 8%.
- 90% of paid revenue comes from one customer who is the founder's college roommate.
- Signups are up 8× post-launch but the flat tail is at 40% of the pre-launch baseline.
- 500 design-partner LOIs signed with 0 converting to paid at end-of-pilot.
- Weekly viral tweet drives spikes that decay by day 5.

The output is a pitch **plus** a hidden-fact reveal box:

> **What the pitch says:** [your paragraph]
>
> **What is actually true (hidden):** [the three facts you chose]
>
> **The diagnostic move that would surface each hidden fact:** [one per fact]

This half of the exercise is a *seeing* drill — you learn to spot the pattern in others' updates by writing one yourself.

### Part C — Run the diagnostic against a real startup (60 min)

Pick a real startup you know something about — your own, a friend's, or a public one that has been press-covered for a "traction" reason in the last 18 months (Product Hunt launch, viral moment, big-logo pilot). Sources for public examples: [First Round Review](https://review.firstround.com/), [Lenny's Newsletter](https://www.lennysnewsletter.com/), the Y Combinator library, a16z podcasts.

Deliver as a table:

| Signal (what was publicly cited) | What it's evidence of | What it's *not* evidence of | Diagnostic move | Verdict | Route to |
|---|---|---|---|---|---|

Fill at least **five rows**. For each verdict, if you cannot compute the diagnostic move because the data is private, say so explicitly and note *what specific question you would ask the founder to run the diagnostic*.

Then, in one closing paragraph, state whether from the *public* evidence you can defensibly conclude the company has PMF today, does not have PMF, or that the public evidence is insufficient. Cite the Chapter 1 frames.

## Starter guidance

- Read Chapter 1 and Chapter 2 end-to-end before starting. The four-row table in Chapter 2 is your rubric.
- The "diagnostic move" column is the whole learning target — every anecdote gets *the same operation*: cohort the users the signal generated, isolate their retention, compare to baseline, check what sustains after the pulse ends.
- The verdict "noise" is legitimate — press-friendly signals like "viral tweet with 12k likes" often produce zero enrolled ICP-fit users. Use it when the signal, correctly cohorted, is empirically zero.
- "Insufficient data — need X" is also legitimate and often the correct verdict for public examples where the retention curve is not published. The whole point of the exercise is to name the specific X you would need.
- Do not be polite about the fictional pitch in Part A. The founder is over-reading loud signals; the diagnostic is what tells them so.
- For Part C, if you cannot find a public startup with enough surfaced data, use your own startup and write with an honesty about it that you would not put on the deck. This exercise is not for external consumption; write against your own vanity.

## Acceptance criteria

Your submission is complete when:

- [ ] Part A diagnoses all five signals from the provided update with the five-field structure (signal / evidence / not-evidence / move / verdict) and a defensibility paragraph grounded in Rachleff and Andreessen.
- [ ] Part B contains a persuasive-sounding pitch that hides three specifically-named underlying facts, plus a reveal box naming the diagnostic move for each.
- [ ] Part C has ≥ 5 rows of a real startup's cited signals, each with all six columns filled; "insufficient data — need X" is a legitimate verdict where public data is thin, but requires naming the specific X.
- [ ] Every verdict maps to either **PMF signal** or a **specific routing to a downstream module** (mod-101 / 103 / 104 / 106 / 108 / 109) or **noise** or **insufficient data — need X**.
- [ ] No verdict is "we have PMF" based solely on any single row's signal — the exercise is designed to catch that pattern.

## Common ways this exercise goes wrong

- **Being kind to the fictional founder in Part A.** The founder is over-reading; the whole point is to *not* be kind. Reject the "we have PMF" claim explicitly with the reason.
- **Part B is too obvious.** If the constructed pitch reads as a warning-label parody, it does not train the pattern-recognition. Write it as a plausible founder update that most people would read straight.
- **Part C uses a startup with no surfaced data.** If you cannot find any public signals with enough context to diagnose, pick a different startup — or use your own. The exercise requires *specific* signals.
- **Verdicts without diagnostic moves.** "Noise" without saying what test would prove it noise is not a verdict, it is a dismissal. Name the move.
- **Confusing "route to mod-108" with "not PMF".** A high-scoring narrow segment with a thin distribution channel is real PMF plus a channel problem. Chapter 6 mode 3 is the vocabulary; if you route to mod-108, the segment has PMF *and* needs channel work.
