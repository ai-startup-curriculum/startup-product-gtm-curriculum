# Shipping the Discovery Report

## Motivation

Twenty interviews of notes, four synthesis memos, and a theme index are not the deliverable. They are the raw material. The deliverable — the artifact this module ends with, and the artifact `project-101-first-thirty-paying-customers` picks up from — is a **discovery report**: a short, opinionated document that another founder, a co-founder, an investor, or a first hire can read in twenty minutes and act on.

The report is not a research paper. It is a **decision document**: this is who the customer is, this is the problem they have, this is what we are going to build next, and this is what we will test to know whether we are right.

This chapter names the shape, the length, and the evidence bar for the report.

## Core concepts

### What the report must contain

The discovery report is one document with six sections. Do not add more; do not skip any.

1. **Problem statement.** One paragraph. Whose problem, in what situation, at what magnitude.
2. **Top jobs (2–4).** Christensen-shape statements from Chapter 4, cited to the corpus.
3. **Top outcomes (3–6).** Ulwick-shape statements, each scored on importance × satisfaction. Star the underserved ones.
4. **Top forces summary.** The recurring push, pull, anxiety, habit patterns from switch stories.
5. **Disqualifying customer signals.** The observable properties of a prospect who *looks* like an ICP but is not — the ones you will use to route away from wasted sales cycles later.
6. **Three testable hypotheses for the next round.** Each hypothesis stated in a form the next round of interviews (or a mod-102 PMF measurement) can falsify.

Every section cites the corpus by interview ID. The corpus (Chapter 6) is what makes the report defensible; the report is what makes the corpus useful.

### Length and tone

- **Total length: 3–6 pages.** Long enough to justify the claims, short enough that the co-founder, the investor, and the first hire will all actually read it.
- **Opinionated, not neutral.** "The problem exists for high-volume freelance consultants and not for the mass consultant market" is a claim. Write claims, not surveys.
- **Cite the corpus, not the founder's intuition.** Every claim has a footnote: *"J1 supported by interviews 2026-08-14-alex, 2026-08-16-bruno, 2026-08-20-cara."* If a claim cannot be cited, it does not belong in the report.
- **No slides.** The narrative deck belongs to positioning (mod-103), not to discovery. Discovery is a memo.

### The problem statement — the hardest paragraph

The problem-statement paragraph is the most-read and most-mis-written part of the report. A useful template:

> **Who:** [specific ICP — role + company shape + a behavioural qualifier that separates in-ICP from out-of-ICP].
> **Situation:** [the triggering situation from the Christensen job — when the problem arises].
> **What they do today:** [current-state workflow in their language, not yours].
> **Cost of the current state:** [magnitude in time, money, missed opportunity, emotional / social — as recorded in the corpus].
> **Why it is still unsolved:** [a one-sentence read on what the market has tried and why it hasn't stuck].

Filled in for the running code-review-tool example:

> **Who:** engineering managers at 50–200-person companies with distributed teams across at least three time zones.
> **Situation:** an engineer's PR has been open more than a day without a review.
> **What they do today:** nag on Slack, DM specific reviewers by hand, or absorb the latency and move the engineer to a different task; four of five EMs interviewed said they had done all three in the last month.
> **Cost of the current state:** median junior-engineer PR waits 26 hours to first review, per self-report from six EMs; two EMs described losing a sprint's worth of momentum from a single stalled review.
> **Why it is still unsolved:** GitHub's built-in review-request tooling notifies but does not escalate; the market's dashboard tools (a competitor + an open-source project) put the intervention in a place the EM has to remember to look.

This paragraph does the work of the whole report on its own; if the reader stops after the first section, they should still know who the customer is and what the pain is.

### The disqualifying signals — the section most founders skip

Chapter 4 taught the JTBD outcomes; Chapter 6 taught the corpus. Both are about the customer you *do* want. Section 5 is about the customer who **looks like your ICP but is not** — the wrong-fit prospect who will consume sales cycles and generate churn if you sell to them.

Two examples for the code-review-tool:

- **Disqualifier D1**: teams smaller than 10 engineers. Review latency at that size is not painful; the EM is often the reviewer themselves.
- **Disqualifier D2**: teams where reviews are done in a fully synchronous ceremony (weekly review-meeting). The problem shape does not exist; the tool solves nothing.

Naming disqualifiers up front is what separates a discovery report from a marketing brochure. It is also the single most valuable content for the first sales hire, who otherwise will spend six months figuring out how to say no.

### The three testable hypotheses — what makes this a decision document

The last section is the whole point. Everything above justifies these three.

Each hypothesis has the same shape:

> **Hypothesis H1:** [we believe X].
> **How we would know we are wrong:** [a specific observable outcome from the next round of interviews, a prototype test, or a PMF instrument that would falsify H1].
> **Next action:** [what we do next to run that test].

Examples for the code-review-tool:

> **H1:** An in-workflow escalation (GitHub-native, auto-reassign after N hours) will land with the ICP where a separate dashboard will not.
> How we would know we are wrong: 5 of 10 solution-interview EMs prefer the dashboard artifact when shown three options.
> Next action: run 10 solution interviews with 3 artifacts (dashboard, inline bot, digest).
>
> **H2:** The buyer is the engineering manager, not the VP Eng, at ICP company sizes.
> How we would know we are wrong: the first three signed design-partner LOIs come with a VP-Eng name on the contract, not an EM.
> Next action: recruit 5 VP-Eng-level interviews to test whether purchase authority sits above the EM.
>
> **H3:** Willingness to pay is meaningful ($X per team per month is not too high) once the auto-reassign works.
> How we would know we are wrong: fewer than 3 of 10 design partners convert to paid at any price after a 30-day free pilot.
> Next action: build the paid pilot conversion flow into the alpha, run against 10 signed design partners.

Every hypothesis has a specific falsifier and a specific next action. That is what distinguishes a discovery report from a strategy document: it names what would prove it wrong.

### The report is dated, is signed, and is versioned

- **Dated.** Put the date at the top. A discovery report from twelve months ago is a historical document, not a decision document.
- **Signed.** Put the author's name at the top. Discovery is opinionated; readers need to know whose opinion they are reading.
- **Versioned.** When you re-run the loop and update the report, write it as v2 and preserve v1. The delta between versions is itself learning.

### How the report feeds forward

The report is the input to five downstream modules of this track:

- **mod-102 (PMF Signal and Measurement)** takes the three testable hypotheses and turns them into measurable PMF instruments (Sean Ellis survey, cohort retention read, main-benefit statement).
- **mod-103 (Positioning and Messaging)** takes the problem statement, the top jobs, and the top forces as inputs to the Dunford five-component positioning frame.
- **mod-104 (ICP and Buyer Personas)** takes the "who" from the problem statement and the disqualifying signals and hardens them into a scoreable ICP + disqualification checklist.
- **mod-105 (Founder-Led Sales)** takes the report as the underlying justification for the discovery call script — every question in the call maps to a top job or a top force from the report.
- **`project-101-first-thirty-paying-customers`** takes the ICP + the disqualifying signals + the top jobs and applies them end-to-end to the first thirty paying customers.

If the report is thin, all five downstream artifacts inherit the thinness. That is why the evidence bar in this chapter is high.

## Concrete example — the report as a table of contents

Full table of contents for a shippable discovery report on the running code-review-tool example:

```
Discovery Report — [Startup name]
Authored by [Founder]. Version 1, 2026-08-31.

1. Problem statement                              [1 paragraph]
2. Top jobs                                       [3 jobs]
    J1 — When PR has been open >1d, know who owns escalation
    J2 — Onboard new juniors to fast reviews without nagging
    J3 — Get an accurate weekly read on review latency
3. Top outcomes                                   [5 outcomes, 3 starred]
    O1 * — Minimise time-to-identify owner of stalled review
    O2 * — Minimise median hours-to-first-review for new-hire PRs
    O3   — Accuracy of weekly review-latency read
    O4 * — Minimise reviewer-load imbalance across the team
    O5   — Minimise effort to onboard the tool to a new team
4. Top forces observed                            [4 push, 3 pull, 4 anxiety, 5 habit]
5. Disqualifying customer signals                 [3 disqualifiers]
    D1 — <10 engineers on the team
    D2 — Synchronous weekly review ceremony
    D3 — No GitHub App install permission
6. Three testable hypotheses for the next round   [H1 shape / H2 buyer / H3 WTP]

Appendix A: theme index (link)
Appendix B: interview notes (link, 22 files)
Appendix C: synthesis memos (link, 4 memos across batches of 5-6)
```

3–4 pages of body plus the appendix links. A reader gets the decision in twenty minutes and can drill in as far as the corpus if they want to check any claim.

## Common failure patterns

- **The report is a slide deck.** Slides let you elide claims. A memo forces you to write them. Save the deck for positioning (mod-103); ship a memo here.
- **No disqualifiers.** The report describes the ICP but not the anti-ICP. First AE downstream will waste months.
- **Hypotheses that are not falsifiable.** "We believe our tool will resonate with EMs" is not a hypothesis. "Fewer than 3 of 10 EMs shown the auto-reassign shape will prefer a dashboard" is.
- **Claims without corpus pointers.** The report becomes the founder's opinion instead of a defended position. Readers cannot check; therefore they should not trust.
- **The report is 30 pages.** No one reads it. Discipline yourself to 3–6.
- **The report is never updated.** Discovery is a loop; the report should be re-versioned every time you re-run the loop with new evidence.

## Summary

- The discovery report is the module's ship deliverable. **Six sections, 3–6 pages, dated, signed, versioned.**
- Six sections: **problem statement, top jobs, top outcomes, top forces, disqualifying signals, three testable hypotheses.**
- Every claim cites the corpus. Every hypothesis has a specific falsifier and a specific next action.
- The disqualifiers section is what a first sales hire will thank you for.
- The report is the input to five downstream modules and the first project. Thin report → thin everything downstream.
