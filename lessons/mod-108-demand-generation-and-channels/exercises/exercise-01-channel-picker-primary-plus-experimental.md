# Exercise 01 — Channel Picker (Primary + Experimental)

**Estimated time:** 3 hours
**Chapter link:** [`01-channel-portfolio-one-primary-plus-one-experimental.md`](../01-channel-portfolio-one-primary-plus-one-experimental.md)
**Prerequisite:** Chapter 1 read end-to-end; a mod-104 ICP scorecard (or an equivalent working ICP + primary buyer / user / champion split); a mod-105 founder-led-sales pack summary — where did the first 15-30 deals come from? (or a working best-guess if mod-105 has not run yet); a mod-106 pricing-pack summary (ACV band + pricing metric); a mod-107 motion decision (PLG / SDR-AE / Enterprise MEDDPICC). If any prerequisite is not yet authored, use a labelled `PLACEHOLDER` per Chapter 1's placeholder discipline (also called out in mod-107 exercise 01).

## Problem statement

Chapter 1 named the primary channel decision as a **derivation** from three upstream inputs: the ICP's information graph (mod-104), the founder-led signal (mod-105), and the CAC math the ACV + pricing pack support (mod-106). The failure mode: the founder picks the channel from career history ("last company did outbound, so we're doing outbound"), from investor advice ("you should run paid"), or from what is fashionable that quarter ("everyone's talking about community") — and burns 6-18 months of runway on a channel the derivation would have flagged as wrong on day one.

This exercise trains you to **run the derivation explicitly** on the startup you own or are evaluating — score each of the six channel archetypes against the three-question test, pick the primary, pick the experimental, populate a dated "not now" list for the four rejected archetypes with re-evaluation triggers, and commit the decision to a one-page portfolio brief the shape Chapter 1's Loomly example implies.

The failure mode this exercise exists to catch: **the founder writes "we're doing outbound + inbound + a bit of community + paid + partnerships" without running the derivation, funds each at 15-20% of minimum viable investment, and eighteen months later has burned the seed round producing zero repeatable channels — because six half-funded channels each fail diagnostic-invisibly.**

## Requirements

Deliver a folder `exercise-01/` with four files:

- `part-a-inputs.md` — the ICP + founder-led signal + pricing-pack summaries condensed to what the channel derivation needs.
- `part-b-three-question-scoring.md` — the six channel archetypes scored against Chapter 1's three-question test.
- `part-c-portfolio-decision.md` — the primary + experimental + "not now" list with re-evaluation triggers.
- `part-d-portfolio-brief.md` — the one-page brief in board-ready shape.

### Part A — Extract the inputs (30 min)

Deliver `part-a-inputs.md`. Condense the three upstream inputs to what the derivation needs. Do not re-derive them; cite mod-104 / mod-105 / mod-106 or label a `PLACEHOLDER`.

**A1 — ICP information graph (10 min).** Where does the ICP already look for solutions? Name specific surfaces, not categories:

- **Search:** what specific queries does the ICP type? What Google search patterns show up in customer discovery calls?
- **Peer / community discussion:** what Slacks / Discords / subreddits / forums / newsletters / podcasts does the ICP consume?
- **Events:** what conferences, meetups, or workshops does the ICP attend?
- **Social platforms:** LinkedIn / X / Reddit / YouTube — which does the ICP actually use, and how (active vs. passive)?
- **Existing tools:** what adjacent tools does the ICP already run (BuiltWith / Wappalyzer / GitHub-observable patterns for technical ICPs)?
- **Explicitly *not* present:** which surfaces do NOT reach the ICP at meaningful volume (e.g., "not on Meta at scale", "not attending IT trade shows")?

**A2 — Founder-led signal (10 min).** From your mod-105 founder-led-sales pack (or best-guess if mod-105 has not run yet), for each of the first 10-30 closed deals name the *first-touch source*. Group by channel:

- Founder's Twitter / LinkedIn / personal blog / open-source project
- Founder-authored cold outbound
- Conference talk / event / podcast appearance
- HN / Reddit / community post / thread
- Warm introduction / referral / network
- Inbound "someone found us" (specify how)
- Other (name)

If the mod-105 phase has not produced enough deals to answer, note that and use best-available signal (design-partner conversations, early-user acquisition patterns) — labelled.

**A3 — Pricing / CAC math summary (10 min).** From your mod-106 pack:

- Primary ACV band per Chapter 2's tiering (micro / low / mid-market / enterprise / strategic).
- Pricing metric (per-seat / per-usage / per-outcome / per-license / hybrid).
- Gross margin (assumed if not yet measured — 70-80% is the SaaS default).
- **Derived CAC ceiling** (fully-loaded) at 12-month payback and 18-month payback. Show the arithmetic per Chapter 2's formula.
- **Derived CAC ceiling implication**: what motions / channels can the ACV support (per Chapter 2's table)?

### Part B — Score the six channel archetypes (75 min)

Deliver `part-b-three-question-scoring.md`.

**B1 — Reproduce the three-question test rubric (5 min).** Chapter 1's three-question test:

- **Q1 — where does the ICP already look for solutions to this problem?** (Route to the answer from Part A1.)
- **Q2 — where has the founder-led sales motion already produced signal?** (Route to the answer from Part A2.)
- **Q3 — what does the ACV + payback math support?** (Route to the answer from Part A3.)

For each channel archetype in Part B2, score against each question on a 0-3 scale:
- **3** — strong fit. The ICP is heavily present on this surface; the founder-led signal was concentrated here; the CAC math comfortably supports it.
- **2** — plausible fit. Moderate ICP presence; some founder-led signal; CAC math supports it at defensible edges.
- **1** — weak fit. Marginal ICP presence; occasional signal; CAC math supports only at the upper edge of the band.
- **0** — no fit. ICP absent; no founder-led signal; CAC math does not support it.

**B2 — Score each of the six archetypes (60 min).** For each of the six Chapter 1 archetypes — **founder-led outbound, inbound / content + SEO, community, paid acquisition, partnerships / channel, events / DevRel** — write a 3-5 sentence assessment structured as:

- Q1 score + rationale
- Q2 score + rationale
- Q3 score + rationale
- Composite (sum of three scores + one-sentence takeaway)
- Time-to-signal window (from Chapter 1's minimum-viable-investment table)
- Minimum-viable-investment level (from same table)
- Chapter-2 unit-economic feasibility (per your Part A3 CAC ceiling — does this channel plausibly produce customers inside the envelope?)

**B3 — Rank the six archetypes (10 min).** Produce a ranking table:

| Rank | Channel | Composite score (0-9) | Time-to-signal | MVI cost | Fit summary (1 line) |
|---|---|---|---|---|---|

Highest composite → rank 1; ties broken by (a) time-to-signal (shorter wins for primary candidacy), then (b) fit with the mod-107 motion.

### Part C — The portfolio decision (45 min)

Deliver `part-c-portfolio-decision.md`.

**C1 — Pick the primary (10 min).** Name the primary channel from Part B3's ranking. Write a paragraph that:

- Cites the composite score.
- Names why this channel — not the second-ranked — is the primary. If the top two are tied, name the tiebreaker (motion fit, time-to-signal, resource availability, mod-105 evidence strength).
- Confirms it fits the mod-107 motion (a PLG motion + outbound-primary is a channel-motion mismatch; name why your combination is not a mismatch).
- Names the founder-owned resource allocation: who is executing this channel, how many hours per week, what fraction of the seed marketing budget.

**C2 — Pick the experimental (10 min).** Name the experimental from Part B3's ranking or from a strategic-gap consideration (Chapter 1: the experimental has three jobs — hedge, generate the next-stage hypothesis, cover a strategic gap the primary does not). Write a paragraph that:

- Cites the composite score OR names why a lower-composite channel is chosen (e.g., "community's composite is 5 but its strategic role as the retention flywheel makes it the right experimental even at lower score").
- Names which of the three experimental-slot jobs it is serving (hedge / next-hypothesis / strategic gap).
- Names the exploratory-scale investment (20-40% of MVI); who owns it; what the checkpoint gates are.

**C3 — Populate the "not now" list (15 min).** For each of the four rejected archetypes, write a 3-4 sentence "not now" entry structured as:

- **Rationale** — why this channel is not now (score-based; ICP-fit-based; motion-mismatch-based; time-to-signal-based; resource-based).
- **Re-evaluation trigger** — the specific signal that would move this channel from "not now" back into candidacy. Examples: "re-evaluate at 100 paying customers", "re-evaluate when ACV expands into the $50K+ enterprise band", "re-evaluate at Series A close", "re-evaluate if the primary shows Chapter 7 decay signals".
- **Owner** — who is watching for the re-evaluation trigger.

**C4 — Rule-out the six-channel-parade (10 min).** Write a paragraph that names the specific channels you are choosing NOT to run in parallel, and cites Chapter 1's minimum-viable-investment argument. This is a discipline exercise — the temptation to add "a little bit of X" is what the doctrine exists to resist. Name what you would be tempted to add, and why you are not adding it.

### Part D — The one-page portfolio brief (30 min)

Deliver `part-d-portfolio-brief.md`. Write in the shape a board member, a first go-to-market hire, or an incoming co-founder would use to understand the portfolio decision without reading Chapters 1-2. Structure:

```
# Channel Portfolio Brief — {product} — {date}

## Inputs
- ICP information graph (top 3 surfaces): {list}
- Founder-led signal concentration: {top 1-2 sources of first 10-30 deals}
- ACV band + CAC ceiling: {band} / ${18-mo payback CAC ceiling}
- Motion (mod-107): {PLG / SDR-AE / Enterprise MEDDPICC / stacked}

## Primary channel
- {channel}
- Composite score: {0-9}
- Why this channel: {2-3 sentences citing Q1/Q2/Q3 evidence}
- Motion fit: {1 sentence — how this channel pairs with the mod-107 motion}
- Owner + investment: {who, hours/week, $/quarter}
- Time-to-signal target: {chapter 1 window}

## Experimental channel
- {channel}
- Composite score OR strategic-gap rationale: {}
- Which of three experimental-slot jobs: {hedge / next-hypothesis / strategic gap}
- Owner + investment: {who, hours/week, $/quarter — at 20-40% of MVI}
- Checkpoint gates: {when + what}

## "Not now" list
- {channel 1}: {rationale}; re-evaluate: {trigger}; owner: {who}
- {channel 2}: {rationale}; re-evaluate: {trigger}; owner: {who}
- {channel 3}: {rationale}; re-evaluate: {trigger}; owner: {who}
- {channel 4}: {rationale}; re-evaluate: {trigger}; owner: {who}

## Six-channel-parade rule-out
- {2-3 sentences naming what would tempt an add-on and why the discipline holds}

## Next-decision triggers
- Re-run the derivation when: {2-3 signals — ICP drift per mod-104 Chapter 7, motion pivot per mod-107 Chapter 6, primary shows Chapter 7 decay, ACV band opens/closes per mod-106 Chapter 5}

## Open questions / placeholders
- {any Part A placeholders that materially would change the derivation if wrong}
```

Compress ruthlessly to one page. If it runs longer, cut. The compressed version is the artifact that gets referenced quarterly (Chapter 7's quarterly-review).

## Starter guidance

- **The ICP's information graph is the load-bearing input.** Spend real time on Part A1 — a wrong ICP graph propagates through every downstream question. If your ICP is technical (developers, platform engineers, data teams), you will find them on GitHub, HN, Lobsters, dev-focused newsletters, and specific conferences — not on LinkedIn Ads at scale. If your ICP is a non-technical mid-market VP (Marketing, Ops, Finance), you will find them on LinkedIn (organic + paid), in industry newsletters, and at vertical conferences — not on HN.
- **The founder-led signal is the strongest working hypothesis for the primary.** Chapter 1 names the "discount-the-working-channel trap" explicitly — founders often discount the channel that produced their founder-led deals because it "isn't scalable" or "was luck". Do not discount it. If 8 of your 22 deals came from the founder's Twitter presence, the primary hypothesis is *inbound / owned social*, not *paid* — even if paid feels more scalable.
- **The CAC ceiling from Part A3 is a hard constraint, not a suggestion.** A $99/month self-serve product has a $200-800 CAC ceiling; an SDR-AE motion at $60K/quarter fully-loaded cannot fit inside it regardless of how much the ICP is on LinkedIn. If your Q3 score for a channel is 0 (CAC math does not support), the composite drops to at most 6 and the channel is essentially disqualified for primary.
- **Score honestly on Q2, even when the founder-led signal was small.** With only 3-5 founder-led deals, no single channel has strong signal. In that case, weight Q1 (ICP graph) and Q3 (CAC math) more heavily; note in Part D that the Q2 score is provisional and will be re-run at the next quarterly review with more deals in the sample.
- **The experimental slot is a real commitment, not decoration.** Chapter 1 names the "experimental-as-decoration trap" — a slot with no assignee, no calendar, and no attribution instrumentation. If you cannot name an owner and a 20-40%-of-MVI investment for the experimental, the slot is empty and you have a portfolio of one channel, not two.
- **Community is often the right experimental even at low composite score.** Chapter 5's retention argument: community is the strongest retention flywheel, and 18 months of investment beginning now produces the flywheel that is load-bearing at Series A. If you defer community entirely, you are foreclosing an option you cannot re-open in 6 weeks; the experimental slot is the right place to seed it.
- **The "not now" list is not a rejection; it is a scheduled re-evaluation.** Every "not now" entry has a specific re-evaluation trigger. "Re-evaluate someday" is not a trigger; "re-evaluate at 100 paying customers" or "re-evaluate when ACV expands into $50K+" is. The dated list is what prevents the same board conversation from re-opening every quarter.
- **Do not skip the six-channel-parade rule-out.** Naming explicitly what you are choosing NOT to run in parallel is a discipline exercise. The temptation to add "a little bit of X" is what the doctrine exists to resist. Write down the specific channels you are being tempted by, and cite why they are being resisted.
- **Cite mod-107 for the motion fit.** If your primary is outbound and your motion is PLG, that is a channel-motion mismatch (mod-107 Chapter 6). If your primary is paid + inbound and your motion is enterprise MEDDPICC, that is a mismatch. The Part D brief has to confirm no mismatch; if there is a mismatch, name that Exercise 06 of mod-107 is where the fix lives.
- **Board-brief compression matters.** A three-page brief is a working document; a one-page brief is a decision artifact that gets carried into quarterly reviews. If the brief runs longer than one page, the reader will not carry it forward. Compress.

## Acceptance criteria

Your submission is complete when:

- [ ] Part A summarises the three upstream inputs — ICP information graph (specific surfaces named), founder-led signal (first-touch source per deal for the first 10-30 deals), pricing / CAC math (band + gross margin + derived CAC ceilings at 12-mo and 18-mo payback), each cited to mod-104 / mod-105 / mod-106 or clearly labelled `PLACEHOLDER`.
- [ ] Part B scores each of the six channel archetypes (founder-led outbound, inbound / content + SEO, community, paid, partnerships / channel, events / DevRel) against the three-question test on a 0-3 scale with rationale.
- [ ] Part B produces a ranked table with composite scores, time-to-signal, MVI cost, and one-line fit summary per channel.
- [ ] Part C names the **primary channel** with owner + investment + motion-fit confirmation.
- [ ] Part C names the **experimental channel** with which of the three experimental-slot jobs it is serving + owner + 20-40%-of-MVI investment.
- [ ] Part C populates a **"not now" list** for each of the four rejected archetypes with rationale + specific re-evaluation trigger + owner.
- [ ] Part C explicitly rules out the six-channel-parade with a paragraph naming what would be tempting to add and why the discipline holds.
- [ ] Part D is a one-page portfolio brief in the given structure, defensible to a board member without reference to Chapters 1-7.
- [ ] Part D names 2-3 **next-decision triggers** that would prompt a re-run of the derivation (per Chapter 7's cross-module rhythm).
- [ ] Any factual claim (a benchmark, a competitor's channel choice, a market convention) that is not cited to mod-104 / mod-105 / mod-106 / a chapter of mod-108 is flagged `<!-- needs-research: ... -->` rather than invented.

## Common ways this exercise goes wrong

- **Channel-by-intuition trap.** Founder writes "we're doing inbound" in Part C without running B2's scoring or B3's ranking. Part D brief reads as decoration; the decision is not defensible. Fix: run B2 explicitly; the scoring is what makes the derivation defensible.
- **Chapter-1-happy-path trap.** Founder mirrors Chapter 1's Loomly example verbatim — primary = outbound, experimental = inbound — without checking whether her own ICP + founder-led signal + CAC math support the same combination. Fix: score your combination independently; the Loomly example is one derivation, not the answer.
- **Ignore-the-founder-led-signal trap.** Founder's own writing produced 8 of 22 founder-led deals; founder scores inbound as "2 — plausible" instead of "3 — strong" because "it doesn't feel scalable". The scoring is dishonest and the derivation misses the strongest working hypothesis. Fix: score Q2 on the evidence, not the feelings.
- **Placeholder-without-labels trap.** Part A guesses the ICP information graph or the CAC ceiling without labelling the guess. Downstream derivation looks defensible but rests on invisible assumptions. Fix: every guess is labelled `PLACEHOLDER` with a `would revisit when` note.
- **Not-now-list-without-triggers trap.** Part C lists rejected channels without dated re-evaluation triggers. Next quarter the same conversation re-opens from zero. Fix: every not-now entry has a specific trigger and an owner who is watching.
- **Empty-experimental-slot trap.** Part C names a "primary" but leaves the experimental slot empty ("we'll figure this out later"). This is Chapter 1's "all-experiments-no-primary" trap in inverse — the founder has a primary but no hedge, no next-hypothesis, no strategic-gap coverage. Fix: pick an experimental at 20-40% MVI even if it is not the highest-scoring candidate; the slot must be filled.
- **Two-primaries-pretending-to-be-one-stack trap.** Founder names "PLG + outbound as co-primaries" but cannot name the ACV-band or PQL-threshold at which the funnel routes from one to the other. This is Chapter 1's "not two primaries" exception being invoked without meeting its conditions. Fix: name a specific routing boundary (accounts crossing a PQL score → outbound; accounts below → PLG self-serve); if you cannot name it, pick one primary and the other becomes a layer or the experimental.
- **Motion-mismatch-not-checked trap.** Part D does not confirm the channel + motion combination is compatible. Founder picks paid as primary against an enterprise MEDDPICC motion; the paid channel produces low-intent MQLs the enterprise motion cannot process. Fix: Part D's motion-fit confirmation is a required section; if the combination is a mismatch, name mod-107 Chapter 6 as the follow-on.
- **Board-brief-too-long trap.** Part D runs to 3-4 pages. The brief loses its function as a quarterly-review artifact. Fix: one page; the working detail lives in Parts B and C.
- **Never-revisit trap.** Exercise 01 is run once and never re-run. The portfolio decision goes stale as the ICP drifts (mod-104 Chapter 7), the pack changes (mod-106 Chapter 5), or the primary decays (mod-108 Chapter 7). Fix: schedule the re-run per Part D's next-decision-triggers; this exercise is quarterly-at-seed cadence.
