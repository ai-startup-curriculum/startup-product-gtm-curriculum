# Exercise 01 — ICP + ACV → Motion Matrix

**Estimated time:** 2 hours
**Chapter link:** [`01-icp-plus-acv-to-motion-matrix.md`](../01-icp-plus-acv-to-motion-matrix.md)
**Prerequisite:** Chapter 1 read end-to-end; a mod-104 ICP scorecard (or an equivalent working ICP + primary buyer / user / champion split); a mod-106 pricing pack (or an equivalent working ACV + primary pricing metric + tier structure). If either prerequisite is not yet authored, use a placeholder that names the ICP / pricing assumptions you'd carry into the exercise; note the placeholder explicitly.

## Problem statement

Chapter 1 named the primary GTM motion decision as a **derivation** from two upstream artifacts — mod-104's ICP scorecard and mod-106's pricing pack — locating the deal on a matrix whose axes are ACV band and self-service willingness. The failure mode: founders pick the motion from career history, from investor advice, or from what is fashionable that quarter, and spend the next 6-18 months tuning the wrong motion against the wrong market.

This exercise trains you to **run the derivation explicitly** on a startup you own or are evaluating — locate the ICP + ACV combination on the Chapter 1 matrix, name the primary motion the combination demands, name the layer(s) if any, rule out the mismatches, and defend the decision in the shape a board member or a first-sales-hire candidate would recognise.

The failure mode this exercise exists to catch: **the founder writes a motion choice as one line ("we're doing PLG") without the derivation, then discovers 6 months in that the ICP + ACV combination never supported it — and cannot answer "why not enterprise?" or "why not inside sales?" because the decision was never grounded in the matrix**.

## Requirements

Deliver a folder `exercise-01/` with three files:

- `part-a-inputs.md` — the ICP scorecard summary and pricing-pack summary, condensed to what the motion derivation needs.
- `part-b-matrix-derivation.md` — the matrix location, the primary motion, the layer(s), the ruled-out alternatives, the rationale.
- `part-c-motion-brief.md` — the one-page motion brief in board-ready shape.

### Part A — Extract the inputs from mod-104 + mod-106 (30 min)

Deliver `part-a-inputs.md`.

**A1 — ICP summary (10 min).** From your mod-104 scorecard, condense to the four inputs Chapter 1 requires:

- **Firmographic band** — company size range, revenue band, funding stage, geography. If the ICP spans multiple bands, name the primary (beachhead) band per mod-104 Chapter 6; the other bands go on a "not now" list.
- **Behavioural criteria** — what the buyer does before she reaches the vendor (Googles for solutions, RFPs, community-driven adoption, procurement-led evaluation).
- **Buyer / user / champion split** — who uses the product, who champions it internally, who has budget authority. Name specific roles, not generic titles.
- **Self-service willingness signal** — from the behavioural criteria, judge whether the buyer will complete purchase without a human (high / medium / low), and cite the specific behaviours you're grading on.

**A2 — Pricing-pack summary (10 min).** From your mod-106 pack, condense to the three inputs Chapter 1 requires:

- **Primary ACV band** — the anchor tier's per-customer annual revenue at typical adoption. Convert to the Chapter 1 bands: micro (<$1K), low ($1-10K), mid-market ($10-100K), enterprise ($100K-$1M), strategic ($1M+).
- **Pricing metric** — per-seat, per-usage, per-outcome, per-license, or hybrid. Name the metric family per mod-106 Chapter 4.
- **Tier structure** — how many tiers, their ACV positioning, whether an enterprise tier exists (with SSO / audit logs / DPA / MSA-negotiable structure) or the pack tops out at team-tier.

**A3 — Placeholder discipline (10 min).** If mod-104 or mod-106 is not yet authored, use best-guess placeholders and label them explicitly as such. Every placeholder line reads `PLACEHOLDER — [what you're guessing] — [what would confirm or deny it]`. Placeholders are permitted for a first-pass exercise; unlabeled guesses are not.

### Part B — Run the matrix derivation (45 min)

Deliver `part-b-matrix-derivation.md`.

**B1 — Locate on the matrix (10 min).** Reproduce the Chapter 1 matrix in your document and mark the cell your ICP + ACV combination lands in. Justify each axis:

- ACV band: name the band and the specific $ number you're pinning.
- Self-service willingness: name high / medium / low and cite the behavioural / role-split evidence from Part A.

**B2 — Consider each of the three motion archetypes (15 min).** For each of PLG / SDR-AE / Enterprise MEDDPICC, write a 3-5 sentence assessment against your ICP + ACV combination. Structure per motion:

- Would this motion work? (Yes / Partial / No)
- What in the ICP + ACV combination supports or contradicts it?
- What would break if you chose it?

**B3 — Pick the primary motion and the layer(s) (10 min).** Name:

- **Primary motion** — the one you invest fully in first. One line + one paragraph rationale.
- **Layer(s)** — any secondary motion that supports the primary (e.g., PLG top-of-funnel feeding SDR-AE; sales-assist trigger feeding self-serve). For each layer, name what it feeds into the primary motion and why the layer is subordinate.
- **Explicitly deferred** — motions you are *not* running now, with a rationale. "Not enterprise" is a stronger statement than "we might get to enterprise someday."

**B4 — Explicitly rule out the mismatches (10 min).** For each of Chapter 1's three canonical mismatches — enterprise ceremony on a self-serve product, self-serve on a $100K contract, mid-market SDR-AE on a bottoms-up developer product — say why the mismatch does not apply to your combination. Two sentences per mismatch. If a mismatch *does* apply (rare but possible for placeholder inputs), name the mismatch and note that Exercise 06's teardown is where you would work the diagnosis.

### Part C — The one-page motion brief (45 min)

Deliver `part-c-motion-brief.md`. Write the motion brief in the shape a board member, a first-sales-hire candidate, or a first-time investor would use to understand the derivation without reading Chapters 1-6.

Structure:

```
# Motion Brief — {product} — {date}

## Inputs
- ICP band (firmographic): {band} — {citation: mod-104 or placeholder}
- ICP behavioural signature: {high-level pattern}
- Buyer / user / champion split: {roles}
- ACV band: {band} — {specific $}
- Pricing metric: {family}
- Tier structure: {number of tiers, enterprise tier yes/no}
- Self-service willingness: {high/med/low + evidence}

## Matrix location
- Cell: {ACV band × self-service willingness}
- Rationale: {2-3 sentences}

## Primary motion
- {PLG / SDR-AE / Enterprise MEDDPICC}
- Why: {2-3 sentences citing Part B's derivation}

## Layer(s)
- {Layer 1}: feeds {primary motion} via {mechanism}
- {Layer 2 if any}: feeds {primary motion} via {mechanism}

## Explicitly deferred motions
- {Deferred motion 1}: {reason not now}
- {Deferred motion 2}: {reason not now}

## Ruled-out mismatches
- Enterprise ceremony on self-serve: {why not}
- Self-serve on $100K contract: {why not}
- SDR-AE on bottoms-up developer product: {why not}

## Next-decision triggers
- Re-run this derivation when: {list 2-3 signals that would prompt a re-derivation — e.g., ICP drift per mod-104 Chapter 7, pack change per mod-106 Chapter 5, new ACV band opened via enterprise expansion}

## Open questions / placeholders
- {any Part A placeholders that would materially change the derivation if wrong}
```

Compress ruthlessly. If the brief runs longer than one page, cut — the compressed version is the artifact that gets referenced quarterly.

## Starter guidance

- **The matrix location is the load-bearing decision.** Everything else in the brief is defending that cell. Spend real time on B1's justification — a mis-located matrix cell propagates every downstream error.
- **The buyer / user / champion split usually decides self-service willingness.** When the user is also the buyer (individual developer with a personal card, or a small-team owner with discretionary budget), self-service is high; when the user and buyer are separated by 2+ organizational layers (developer / eng manager / VP eng / procurement), self-service is low. Grade the split honestly.
- **Enterprise tier existence is a hard gate on the enterprise motion.** If the mod-106 pack has no enterprise tier (no SSO, no audit logs, no MSA-negotiable structure, no priority support), the enterprise motion is not available regardless of what the ICP looks like — the fix is to revisit the pack per mod-106 before selecting the motion.
- **"We might do PLG and enterprise" is not a motion decision.** Chapter 1's *run-all-three-motions-simultaneously* trap is exactly this compromise. Pick the primary. If two motions are genuinely required (PLG feeding sales-assist for mid-market; SDR-AE feeding enterprise expansion for a subset), name one as primary and one as layer, with defined hand-off criteria.
- **Placeholders are honest.** If your mod-104 doesn't yet split buyer / user / champion, write `PLACEHOLDER — assuming VP Eng is both buyer and champion — would revisit once mod-104 exercise 03 is complete`. A labelled placeholder is a followable thread; an unlabeled guess produces a motion decision built on invisible assumptions.
- **The three-mismatch rule-out block is not decoration.** Forcing yourself to explain *why* each canonical mismatch does not apply is what catches the mismatch that *does* apply. The Exercise 06 teardown is where you go if a mismatch surfaces here.
- **Board-brief compression matters.** A three-page brief is a working document; a one-page brief is a decision artifact. If a board member wants more detail she will ask for Part B — the brief in Part C is the one that gets referenced during hiring conversations and quarterly reviews.
- **Cite mod-105 for the founder-led-sales boundary.** If your primary motion is SDR-AE or enterprise, note whether the founder has personally closed the first 20-30 deals per mod-105 Chapter 8's readiness signals. Motion decisions made before the founder-led phase completes are premature; the brief should name that fact honestly rather than assuming the founder-led work has happened.
- **Do not skip the "next-decision triggers" section.** A motion decision without a stated re-evaluation trigger becomes a motion decision that gets carried unchanged for years — even after the ICP drifts, the ACV shifts, or the market position changes. Name 2-3 specific signals that would prompt a re-run.

## Acceptance criteria

Your submission is complete when:

- [ ] Part A summarises the ICP inputs (firmographic band + behavioural criteria + buyer/user/champion split + self-service willingness) and the pricing-pack inputs (primary ACV band + pricing metric + tier structure), each cited to mod-104 / mod-106 or clearly labelled `PLACEHOLDER`.
- [ ] Part B reproduces the Chapter 1 matrix and marks the cell your ICP + ACV combination lands in, with a justification for each axis.
- [ ] Part B contains a 3-5 sentence assessment for each of the three motion archetypes against your combination (yes / partial / no + specific reasons).
- [ ] Part B names the **primary motion**, any **layer(s)** with hand-off mechanism, and any **explicitly deferred** motions with rationale.
- [ ] Part B rules out each of the three canonical mismatches with a specific reason (or names a mismatch that *does* apply and flags Exercise 06 as the follow-on).
- [ ] Part C is a one-page motion brief in the given structure, defensible to a board member without reference to Chapters 1-6.
- [ ] Part C names 2-3 **next-decision triggers** that would prompt a re-run of the derivation.
- [ ] Any factual claim (a benchmark, a competitor motion, a market convention) that is not cited to mod-104 / mod-106 / a chapter of mod-107 is flagged `<!-- needs-research: ... -->` rather than invented.

## Common ways this exercise goes wrong

- **Motion-by-intuition trap.** Founder writes "we're doing SDR-AE" in Part B without running B1's matrix location or B2's per-archetype assessment. The Part C brief reads as decoration; the decision is not defensible. Fix: run B1 and B2 explicitly; the derivation is what makes the decision defensible.
- **Mismatch-hand-wave trap.** Part B's rule-out block reads "not applicable" for each mismatch without a specific reason. The exercise misses its central purpose (catching the mismatch that *does* apply). Fix: two sentences per mismatch, citing the specific ICP or ACV feature that rules it out.
- **Placeholder-without-labels trap.** Part A guesses the ICP band or the ACV without labelling the guess. Downstream derivation looks defensible but rests on invisible assumptions. Fix: every guess is labelled `PLACEHOLDER` with a `would revisit when` note.
- **Motion-plus-layer-without-hand-off trap.** Part B names "SDR-AE primary + PLG layer" without saying how the PLG layer feeds the SDR-AE motion (via PQL alerts routing to SDR outreach? via free-tier sign-ups populating the target-account list?). The layer becomes decoration. Fix: every layer names the specific mechanism it feeds the primary motion.
- **Board-brief-too-long trap.** Part C runs 3-4 pages of detail. The brief loses its function as a quarterly-reference artifact. Fix: one page; deep detail lives in Part B.
- **Missing-next-decision-triggers trap.** Part C ships without the triggers block. Motion decision becomes permanent. Fix: name 2-3 specific triggers that would prompt a re-run; without them the derivation cannot self-correct.
- **Choose-motion-you-know trap.** Founder with enterprise background writes "enterprise" for a $6K-ACV self-serve product. Part B's B2 archetype assessment would have flagged this if run honestly. Fix: score B2 blind of your own background; if the paper answer disagrees with your gut, the paper answer wins.
- **Assuming-founder-led-sales-is-complete trap.** Brief assumes SDR-AE motion is ready to hire against without noting whether the founder has closed the first 20-30 deals herself (mod-105 boundary). Fix: reference mod-105 Chapter 8 readiness signals in Part C's brief; if the founder-led work isn't complete, name it as a prerequisite.
- **Pack-doesn't-support-motion trap.** Brief names enterprise as primary motion but the pack has no enterprise tier; brief names PLG as primary motion but the pack has no self-serve checkout. Fix: verify the pack change is in place (or scheduled) before naming a motion the pack does not yet support.
- **Never-revisit trap.** Exercise 01 is run once and never re-run even as the ICP drifts or the pack changes. The motion decision goes stale. Fix: schedule the re-run per the next-decision-triggers block; treat this exercise as quarterly-at-seed / monthly-at-Series-A cadence.
