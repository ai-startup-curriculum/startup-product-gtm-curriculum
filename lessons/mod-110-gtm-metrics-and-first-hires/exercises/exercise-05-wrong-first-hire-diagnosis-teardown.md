# Exercise 05 — Wrong-First-Hire Diagnosis Teardown

**Estimated time:** 2 hours
**Chapter link:** [`06-staging-the-first-three-gtm-hires.md`](../06-staging-the-first-three-gtm-hires.md)
**Prerequisite reading:** [SaaStr — Jason Lemkin on the first VP Sales hire](https://www.saastr.com/) (search "first VP Sales" / "when to hire VP Sales" / "VP Sales fired"; ~30 min across two or three posts); [Pete Kazanjy — *Founding Sales*](https://foundingsales.com/) (Chapter on the founder-to-first-AE handoff and Chapter on why the SDR-first sequence fails; ~30 min); [Mark Roberge — *The Sales Acceleration Formula*](https://www.markroberge.com/) (Chapter on hiring criteria and the ramp-plan; ~20 min); [First Round Review — writing on GTM leadership hires that went wrong](https://review.firstround.com/) (search "VP Sales" / "sales hire"; ~20 min)

## Problem statement

Chapter 6 named three specific wrong-first-hire patterns:

- **Pattern 1 — VP Sales before PMF.** The founder hires a VP Sales expecting them to invent a motion the founder never validated; 12–18 months and $250–350k in comp later, the VP is fired (or leaves) and the team is worse off.
- **Pattern 2 — SDR team before AE motion works.** The founder hires 2–4 SDRs before the first AE has demonstrated a repeatable motion; the SDRs load the funnel, the founder cannot close what the SDRs produce, or the first AE cannot close because the motion is not yet fit for a non-founder.
- **Pattern 3 — First AE against an undocumented founder script.** The founder hires the first AE without completing the mod-105 script / mod-107 motion documentation; the AE is expected to "shadow the founder," ramps for six months producing nothing, is let go, and the founder concludes "the AE was the wrong hire" when in fact the artifact hand-off never happened.

This exercise trains the diagnostic muscle to spot each pattern early, name it precisely, and prescribe the correct sequence — including the specific mod-102 / mod-104 / mod-105 / mod-107 / mod-108 upstream work that has to complete before the wrongly-timed hire becomes rightly-timed.

You will:

1. Teardown three case snippets (one per pattern) — name the pattern, name the missing pre-condition, name what the founder should have done instead, and prescribe the remediation from where the story ends.
2. Author one case study of your own — either a wrong-first-hire pattern you have seen (in your own company or a company you know well) or a plausible fourth-pattern that is not one of Chapter 6's three (there are more; catalog one).
3. Produce a one-page anti-pattern cheat sheet you would print and pin above the founder's desk during their first year post-Series-A.

The exercise trains the earliness of the diagnosis — the point is to spot each pattern in month 1 of the wrong hire, not month 18 when the damage is complete.

## Requirements

Deliver a folder `exercise-05/` with:

- `part-a-case-teardowns.md` — the three case-snippet teardowns.
- `part-b-your-case-study.md` — your own case study of a wrong-first-hire pattern.
- `part-c-cheat-sheet.md` — a one-page anti-pattern cheat sheet.

### Part A — Teardown three case snippets (75 min)

For each case, deliver a teardown in this structure:

1. **Pattern identification.** Which of Chapter 6's three patterns is at play (or a variant)?
2. **Missing pre-condition.** Which specific mod-102 / mod-104 / mod-105 / mod-107 / mod-108 upstream artifact or one-pager number would have qualified the hire? Cite chapter and section.
3. **Anti-pattern quote.** One sentence from the case that most precisely reveals the pattern (the "smoking gun" line).
4. **What the founder should have done instead.** The specific alternative hire (or no hire) plus the specific upstream work the founder should have completed first.
5. **Remediation from where the story ends.** The founder is now N months in with a wrong hire in place. What is the specific sequence of moves — with rough timing — that gets the team back onto the Chapter 6 staging sequence?

**Case 1 — Series-A / VP Sales hire post-raise.**

> LumenIQ, a mid-market B2B analytics SaaS, closed a $9M Series-A in late Q1 2026 on the strength of $1.2M in ARR from 42 customers (36 mid-market, 6 SMB) — all closed by founder Emma over the prior 18 months. The lead investor's partner suggested "you need a real sales leader to build the team" in the week the round closed. Emma agreed and by end of Q2 2026 had hired Rob — 12 years of experience, most recently VP Sales at a $50M-ARR growth-stage SaaS, joined at $350k OTE plus significant equity.
>
> Rob's mandate: "build the sales team; take the sales function off Emma so she can focus on product." His first 90 days: hired two AEs and one SDR, contracted with a sales-enablement consultancy to build a "world-class onboarding programme," and began a top-down account-planning exercise for the top 100 mid-market targets.
>
> In October 2026, Emma reports to the board that Q3 net-new ARR is $180k (down from $260k in Q1) and per-channel CAC has doubled from ~$5k to ~$10k. In February 2027, Rob and Emma agree that "the timing wasn't right" and Rob departs. Total spend on Rob's tenure and his hires' partial ramps: approximately $850k. The two AEs have written 4 and 6 opportunities each and closed one and zero respectively.

**Case 2 — SDR team stood up to "scale outbound."**

> Waverly Labs, a horizontal collaboration tool, closed a $3M seed round in Q1 2026 with $260k in ARR from 18 customers, all closed by co-founders Sam (technical) and Kai (commercial). The team decided to "scale outbound" in Q2 2026 by hiring three SDRs at $80k base + $20k variable each ($300k total loaded) reporting to Kai, on the reasoning that "SDRs are cheaper than AEs and let us focus the founder time on closing."
>
> By end of Q3 2026, the three SDRs are booking approximately 60 meetings per month (20 each). Kai is running 45 of those meetings personally; Sam is running 10; 5 are being rescheduled or cancelled. Sam and Kai together closed $190k of net-new ARR in Q3 — up modestly from $140k in Q2. Kai reports to the board that "the SDR programme is working; we're generating strong pipeline."
>
> In Q4 2026, Sam and Kai run out of closing capacity; SDR-generated pipeline coverage grows to $2.1M against a Q4 forecast of $220k. Two SDRs are considering leaving because their "close rate" reads as low (SDRs are being evaluated in part on downstream close rate, which is a Kai-and-Sam bottleneck, not an SDR failing). Kai is exhausted and considering hiring an AE, but has no documented sales script beyond a shared Google Doc with talking points.

**Case 3 — First AE hired against an undocumented founder script.**

> Rowan Systems, a developer-tools company, closed a $5M Series-A in Q2 2026 on $700k of ARR from 22 customers, all closed by founder Priyanka over the prior 24 months. Priyanka hired Chris, a strong second-year AE from a peer developer-tools company, at $200k OTE in July 2026. Chris was told "shadow me on calls for the first six weeks; you'll pick it up; we've got a great motion here."
>
> By end of Q3 2026, Chris has shadowed 22 discovery calls, 14 demos, and 6 proposal reviews. Chris has been running his own calls since week 5 but has closed only one deal ($18k) and has 4 stalled opportunities. Discovery-call notes across Chris's calls read very differently from Priyanka's — Chris is asking different questions, disqualifying against different criteria, and the demo he's giving is a 30-minute product tour rather than the tight 12-minute problem-focused walkthrough Priyanka runs. Priyanka's assessment: "Chris was the wrong hire; I don't think he has the sales instinct we need. Let's coach him for one more quarter and if it doesn't turn, replace him."
>
> Priyanka has not written down: the discovery script; the demo checklist; the qualifying criteria; the objection-handling for the top four objections; the proposal template. All are "in her head" and she has been the only person to close a deal.

For each case, produce the full five-field teardown. Do not shortcut the "remediation from where the story ends" field — that is the operating deliverable of the exercise.

### Part B — Your own case study (30 min)

Deliver `part-b-your-case-study.md` — a 400–700 word case study of a wrong-first-hire pattern you have seen. Options:

- **Option 1 — First-hand.** A wrong-first-hire pattern you have seen in your own company, either as founder, employee, board member, advisor, or investor. Anonymise if needed.
- **Option 2 — Second-hand.** A wrong-first-hire pattern you have seen in a company you know well (a portfolio company, a peer startup, a well-documented public case). Anonymise if needed.
- **Option 3 — Fourth-pattern.** A wrong-first-hire pattern that is *not* one of Chapter 6's three. Catalogue it — there are more. Examples to prime the pump: hiring a CRO from an enterprise SaaS to run a bottom-up PLG motion; hiring a marketing consultant on retainer as a stand-in for a demand-gen lead; hiring a "founding AE" at $180k OTE who expects a 100-account book handed to them; hiring a Customer Success Manager before there are customers to succeed with.

Structure the case study as:

1. **Setup.** What was the startup's stage, ARR, motion, and the founder's read at the time of the hire?
2. **The hire.** Who was hired, into what role, on what mandate, at what comp / equity?
3. **The pattern.** Which of the three Chapter 6 patterns is this, or which fourth-pattern is it? What was the missing pre-condition?
4. **The damage.** What was the specific cost — dollars spent, months lost, opportunities missed, downstream effects on the next hire?
5. **The lesson.** What is the one specific pre-condition or one-pager trigger you would name as the check-list item that would have prevented this?

If you cannot produce a first-hand or second-hand case, do a fourth-pattern. The point is to work the diagnostic against a case that is not one of Chapter 6's three, so the pattern-recognition generalises.

### Part C — Anti-pattern cheat sheet (15 min)

Deliver `part-c-cheat-sheet.md` — a one-page (≤400 words) anti-pattern cheat sheet you would print and pin above the founder's desk during the first year post-Series-A. Structure freely, but include:

- **Three patterns.** Named, one line each.
- **Three checklist items** the founder should confirm before any GTM hire ("no, wait, is [specific pre-condition] met?").
- **Three phrases** the founder should be wary of when a board member or advisor suggests a hire ("you need a real sales leader"; "SDRs are cheaper"; "just hire an AE — they'll pick it up").
- **One escalation rule** — the specific one-pager number or artifact that must be in place before the founder greenlights any GTM hire past the first AE.

Optimise for legibility. The cheat sheet should be readable in 60 seconds and remembered.

## Starter guidance

- Chapter 6's three patterns are your baseline vocabulary. Cite the pattern number in your Part A teardowns.
- The **missing pre-condition** field is the load-bearing one. Naming "PMF was not green" is too vague; naming "mod-102 Chapter 4 scorecard was not green in the mid-market ICP; specifically, Sean Ellis 40% metric had never been run" is what the exercise is training.
- For Case 1 (LumenIQ), the specific missing pre-conditions are typically: (a) mod-102 PMF scorecard not established (42 customers is early; PMF in the mid-market segment specifically is what needs to be green); (b) mod-105 readiness signals not documented (the founder can close, but is the script repeatable? the win-loss patterns consistent?); (c) mod-107 motion not documented; (d) mod-104 ICP not codified.
- For Case 2 (Waverly Labs), the specific missing pre-condition is: **the first AE has not been hired, so there is no repeatable AE motion for the SDR to feed.** The remediation is not to fire the SDRs immediately — it is to hire the first AE (once the mod-105 script exists), have the AE take over Kai's closing load using SDR-generated pipeline, and re-evaluate SDR productivity against downstream AE close rate rather than founder-close-rate.
- For Case 3 (Rowan Systems), the specific missing pre-condition is: **mod-105 documentation — script, demo checklist, discovery template, objection handling, proposal template — has not been written down.** The remediation is not to replace Chris; it is to have Priyanka author the mod-105 artifacts in November–December 2026 (with Chris co-authoring where possible), then reset Chris's ramp against the newly-documented motion.
- The "remediation from where the story ends" field is the specific practitioner value of the exercise. The wrong hire has been made; what does the founder do now to get back onto the Chapter 6 sequence? Options include: (a) restructure the wrong hire's role; (b) mutual departure with the wrong hire and pause on the next hire until the pre-condition is met; (c) complete the missing upstream work in parallel with the wrong hire's continuing tenure and re-align mandate; (d) accept the sunk cost and reset the sequence from stage 0.
- For the cheat sheet, brevity is a feature. A one-page cheat sheet that captures the three patterns, three checklist items, three warning phrases, and one escalation rule is more useful than a five-page memo.

## Acceptance criteria

Your submission is complete when:

- [ ] All three Part A cases teared down with the full five-field structure.
- [ ] Each Part A case identifies the specific Chapter 6 pattern number (1, 2, or 3) or a variant.
- [ ] Each Part A "missing pre-condition" cites a specific mod-102 / mod-104 / mod-105 / mod-107 / mod-108 chapter and artifact — not a vague "PMF wasn't there."
- [ ] Each Part A "anti-pattern quote" identifies the smoking-gun line from the case.
- [ ] Each Part A "what should have happened instead" prescribes a specific alternative hire (or no hire) plus the specific upstream work.
- [ ] Each Part A "remediation from where the story ends" is an actionable, time-bounded sequence — not a "start over" hand-wave.
- [ ] Part B case study is 400–700 words, structured with the five-field breakdown (setup, hire, pattern, damage, lesson).
- [ ] Part B case study names the specific pre-condition or one-pager trigger that would have prevented the pattern.
- [ ] Part C cheat sheet is one page (≤400 words), includes three patterns, three checklist items, three warning phrases, and one escalation rule.
- [ ] Cheat sheet is legible in 60 seconds (not a dense wall of text).

## Common ways this exercise goes wrong

- **Blaming the wrong hire personally.** Each of the three patterns is *structural*, not personal. Rob (Case 1) was not a bad VP Sales; the role was wrong-timed. Chris (Case 3) was not a bad AE; the script wasn't documented. Naming the person as the failure hides the structural miss.
- **"Missing pre-condition = PMF."** Too vague. Cite the specific mod-102 chapter, the specific artifact, the specific segment. The exercise trains precision.
- **Remediation = "fire the wrong hire and start over."** Sometimes correct, often not the operating optimum. Consider role restructuring, mandate re-alignment, upstream-work-in-parallel, and the specific timing of any transition.
- **"What should have happened instead = 'wait for PMF.'"** Too vague. Cite the specific hire that should have happened first (or no hire), and the specific mod-105 / mod-107 / mod-108 work in parallel.
- **Case 2 remediation = "fire the SDRs."** The SDRs are the visible symptom, not the root cause. The root is the missing first AE and the founder-close-capacity bottleneck. Fire only if the AE hire cannot happen in a reasonable timeframe.
- **Case 3 remediation = "coach Chris harder."** Chris is a smart second-year AE with no artifact to learn from. Coaching against a non-existent script is not remediation. The founder must author the mod-105 artifacts.
- **Part B case study skipped or shortened to a paragraph.** The whole point is to work the diagnostic against a case that is not one of Chapter 6's three. If you cannot find first-hand or second-hand, do a fourth-pattern.
- **Cheat sheet that is two pages.** One page — pin-above-desk length. Cut.
- **Cheat sheet with vague warning phrases.** "You need a real sales leader" is a specific phrase to be wary of; "sales leadership talk" is not. Quote specific phrases the founder will actually hear.
- **Missing the escalation rule.** The cheat sheet needs one specific one-pager number or artifact-check as the escalation gate. Without it, the sheet is decorative.
