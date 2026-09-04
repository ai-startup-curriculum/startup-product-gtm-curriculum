# Exercise 04 — Beachhead Segment Decision: One Yes, Three Nos

**Estimated time:** 3 hours
**Chapter link:** [`06-beachhead-and-the-not-now-list.md`](../06-beachhead-and-the-not-now-list.md)
**Prerequisite:** Exercise 01 (ICP scorecard with not-now placeholder); Chapter 6 read end-to-end; [mod-103 Chapter 5](../../mod-103-positioning-and-messaging/05-chasm-beachhead.md) for the strategic-altitude beachhead frame

## Problem statement

mod-103 Chapter 5 committed the startup to a single beachhead segment at the positioning altitude. Chapter 6 of this module operationalises that commitment at the ICP altitude: the ICP artifact carries an explicit **not-now section** naming the three segments the founder has deliberately chosen not to serve during the current beachhead — with unlock conditions, meanwhile actions, and revisit triggers per segment.

This exercise trains you to (a) restate the yes-segment sharply enough that an AE can recognise it on a call, (b) author the three (or 2-5) not-now segments with the five required fields per segment, and (c) build the specific hand-off packet that mod-107 (sales-motion design) and mod-108 (channel-selection) will pick up when an unlock condition trips. The output is the not-now section of the ICP scorecard, ready to drop back into Exercise 01's one-page artifact, plus a hand-off document that names the sequenced motion / channel investments implied by the not-now list.

The failure mode this exercise exists to catch: **the founder committed to the beachhead in the positioning workshop, but the ICP has no not-now section, and by month four the AE is working deals in four segments simultaneously because "this one came in and it seemed too good to pass up."** Without written-down exclusions with named unlock conditions and meanwhile actions, the beachhead choice dissolves silently deal by deal.

## Requirements

Deliver a folder `exercise-04/` with:

- `part-a-yes-segment-restatement.md` — the beachhead sharpened to the AE-recognisable form.
- `part-b-not-now-list.md` — the three (or 2-5) not-now segments with all five fields.
- `part-c-handoff-packet.md` — the sequenced motion / channel investments the not-now list implies.

### Part A — Sharpen the yes-segment (30 min)

Deliver `part-a-yes-segment-restatement.md`. Reuse the startup and the mod-103 beachhead choice from Exercise 01. Produce:

- **The one-sentence beachhead statement.** ≤ 25 words. Names the segment specifically enough that an AE can recognise a matching account from a LinkedIn profile in 30 seconds. "Growth-stage B2B SaaS" is not a beachhead statement; "mid-market (50-150-engineer) B2B SaaS devtools / observability / security-tooling companies using GitHub, distributed, with an engineering leader owning a throughput or cycle-time KPI" is.
- **The Moore six-criteria check.** Moore's *Crossing the Chasm* names six criteria a beachhead should pass: (1) identifiable target customer, (2) compelling reason to buy, (3) whole-product surface achievable in the current motion, (4) no entrenched competitor, (5) reference-able (buyers talk to each other in a peer community), (6) big enough to matter, small enough to dominate. For each of the six, write one paragraph: does the chosen beachhead pass, and *why* — with specific evidence, not "yes because we think so." A beachhead that fails 2+ criteria is not defensible; go back to mod-103 Chapter 5 before continuing.
- **The reference-pattern predicate.** Name the specific peer community the beachhead's buyers live in — the Slack channels, the conferences, the podcasts, the subreddits, the newsletters. Two or more concrete named venues. This is the discipline that separates a real beachhead (whose reference pattern carries between customers) from a founder-invented segment (whose customers do not actually talk to each other).
- **The 30-50 nameable-target-accounts list.** Chapter 1 named "30-50 target accounts the founder can name by hand" as the SEED-ICP concentration bar. List at least 20 named target accounts inside the beachhead. If you cannot name 20, the beachhead is either too narrow (fewer than 20 accounts exist) — in which case widen it a notch — or the founder's account-level knowledge is thin — in which case do the research before shipping the ICP.

### Part B — Author the not-now list (90 min)

Deliver `part-b-not-now-list.md`. Author **three to five** not-now segments. The recommended split covers the four not-now archetypes from Chapter 6:

- **The obvious adjacent segment** (peer-community mismatch — reference pattern doesn't carry).
- **The aspirationally larger segment** (usually enterprise — whole-product gap, wrong motion).
- **The emotionally sympathetic smaller segment** (usually individual practitioner / OSS / SMB — ACV too small for the current motion).
- **Optional: the horizontal-adjacent product play** (a segment that requires a positioning shift, not just a segmentation change — a mod-103 question, not a mod-104 one).

For each not-now segment, produce the five required fields per Chapter 6:

```
Not-now segment {N}: {short name}
  What it looks like: {2-3 firmographic + behavioural sentences — enough for an AE to recognise a lead that falls in this segment}
  Why not now: {1-2 sentences — whole-product gap? motion mismatch? beachhead-adjacency risk? reference-pattern non-transfer? name the specific reason, not "not our focus"}
  Unlock condition: {a specific, auditable triggering event that would let the founder revisit — e.g., "SSO + SCIM + audit logs shipped AND first enterprise AE hired AND at least three mid-market Series-A pilot customers referenceable at the 300-500-engineer size"; a "when we grow" clause is not an unlock}
  Meanwhile action: {one of: refer to peer/partner (name the partner if you have one) | downgrade to lower ACV tier (name the tier) | add to segment-specific waitlist (name the owner + cadence) | close-lost with reason code (name the code)}
  Revisit trigger: {who monitors the unlock at what cadence — e.g., "founder reviews quarterly; automatic trigger from product-management notification when SSO/SCIM ship"}
```

At the top of Part B, publish an **unlock-sequencing summary table**:

| Segment | Unlock condition | Expected unlock timing (best-guess quarter) | Implied roadmap / motion investment | Hand-off to mod-107 / mod-108 |
|---|---|---|---|---|

The table is what turns the not-now list from a static exclusion document into a working sequencing input for the next 12-24 months.

At the bottom of Part B, add a **founder-exception log template**:

```
Exception log: any deal from a not-now segment that the founder chose to work
  Date | Account | Not-now segment | Reason for exception | Outcome | Retrospective diagnosis
```

The log exists to make founder-exceptions visible and reviewable. Chapter 6's central failure mode is deal-by-deal founder exceptions that dissolve the beachhead; a written log turns each exception into a reviewable decision rather than an invisible drift.

### Part C — The mod-107 / mod-108 hand-off packet (60 min)

Deliver `part-c-handoff-packet.md`. The not-now list implies a specific sequenced set of motion / channel investments that mod-107 and mod-108 will pick up when unlocks trip. This exercise's job is to name them explicitly so the hand-off is legible.

For each not-now segment, produce:

- **Motion required to serve this segment (mod-107 hand-off).** Which sales motion (PLG self-serve / SDR-AE mid-market / enterprise MEDDPICC / field-sales) matches this segment's ACV and buying process? How does it differ from the current beachhead motion? Which of the current AE's skills transfer, and which need to be net-new hires? What is the motion's expected cycle length and close rate? *Name the motion type; do not design it in full — that is mod-107's job.*
- **Channels required to reach this segment (mod-108 hand-off).** Where do this segment's buyers live? Which conferences, publications, communities, analyst-report authors, paid-media surfaces? Which of the current beachhead channels overlap (usually few), and which are net-new? What is the estimated CAC differential vs. the beachhead? *Name the channel stack; do not design it in full — that is mod-108's job.*
- **Whole-product surface required (mod-106 / product roadmap hand-off).** What ships / integrates / certifies for this segment to be serve-able? Which items map to the unlock condition in Part B, and which are additional? What is the estimated engineering investment?
- **The "which unlock trips first" sequencing.** If you had to invest in one segment's unlock over the next four quarters, which would it be — and why? The answer is a strategic bet; naming it makes the bet reviewable rather than tacit.

At the bottom of Part C, close with a one-page **beachhead-commitment memo** — one page addressed to the founder's team stating: for the next N quarters, we are serving the yes-segment exclusively; here are the three not-now segments we are deliberately excluding; here are their unlock conditions and expected timing; here is what changes if any unlock trips early. The memo is what makes the beachhead commitment binding across the team, not just documented in the ICP artifact.

## Starter guidance

- **Do not write the not-now list without doing the Moore six-criteria check on the yes-segment first.** The most common failure is a well-authored not-now list defending a beachhead that itself fails the reference-ability or whole-product criteria. If the yes-segment doesn't pass six-of-six, the exclusions are protecting the wrong thing.
- **Author the aspirational-enterprise not-now first.** The founder's deepest un-said desire is usually to serve enterprise "eventually"; naming enterprise as a not-now with an explicit unlock forces the tacit "we'll get there" wish into a defensible sequencing bet. Every founder-led-sales startup has this exclusion; author it first and specifically.
- **The unlock condition must be auditable.** "When we grow" is not an unlock; "when SSO + SCIM ship, and we have hired our first enterprise AE, and three current mid-market customers have expanded to 300+ seats" is. If the unlock cannot be checked with a yes/no verdict in a founder review, it is not written sharply enough.
- **The meanwhile action must be specific.** "We'll figure it out" is not a meanwhile. Every not-now segment gets exactly one of the four canonical actions (refer / downgrade / waitlist / close-lost) with a named owner, cadence, and template. Without the meanwhile, the AE improvises on the fly and drifts back into serving the excluded segment.
- **Test each not-now against a real inbound lead.** For each of the three not-now segments, name a real inbound lead your startup received (or would plausibly receive) that falls in the segment. Walk through the meanwhile action step by step: does the referral partner exist? Is the waitlist email template written? Who sends it? The exercise exposes the meanwhile-action fantasy where the "waitlist" is a promised email nobody has ever actually sent.
- **The peer-community differential is often decisive.** The most common founder mistake in beachhead selection is picking two adjacent segments as one beachhead because they look firmographically similar — but their buyers hang out in completely different communities, and the reference pattern from customer A does not persuade customer B. If you cannot name a shared peer community where both segments' buyers actually talk to each other, they are two segments, not one.
- **Write the founder-exception log even if it is empty.** A missing log means every exception is tacit; a present log — even with zero entries — means exceptions are reviewable. Ship the log with a v0 entry ("exception log established on {date}") so the artifact is live from day one.
- **The hand-off packet is legibility, not design.** You are not designing the enterprise motion or the fintech channel stack; you are naming what will need to be designed, when, by whom. If you find yourself writing an SDR-AE role-and-responsibilities document, stop — that is mod-107's job. Name the requirement; do not build the solution.
- **Sequence the unlocks explicitly.** If four segments all unlock on the same product investment (SOC 2 Type II), that is a strong prioritisation signal — the not-now list becomes a demand-signal for the roadmap. If four unlocks are all independent and require four different investments, the founder faces a sequencing bet — name the bet you are making.

## Acceptance criteria

Your submission is complete when:

- [ ] Part A restates the beachhead in ≤ 25 words, sharp enough for AE-recognition from a LinkedIn profile.
- [ ] Part A runs the Moore six-criteria check with a paragraph and specific evidence per criterion; the beachhead passes ≥ 5 of 6, with any failure explicitly discussed.
- [ ] Part A names the reference-pattern peer community — ≥ 2 concrete venues where the beachhead's buyers actually talk to each other.
- [ ] Part A lists ≥ 20 named target accounts inside the beachhead (or explicitly flags research-gap if fewer).
- [ ] Part B authors **3-5 not-now segments** spanning at least three of the four Chapter 6 archetypes (obvious-adjacent, aspirationally-larger, emotionally-sympathetic-smaller, horizontal-adjacent).
- [ ] Each not-now segment has all **five required fields**: what it looks like, why not now, unlock condition, meanwhile action, revisit trigger. No field is "we'll figure it out."
- [ ] Every unlock condition is **auditable** — a yes/no verdict against a specific triggering event, not a "when we grow" clause.
- [ ] Every meanwhile action is **operationally specific** — the canonical action (refer / downgrade / waitlist / close-lost) plus named owner, cadence, and template location.
- [ ] The unlock-sequencing summary table is present at the top of Part B, with best-guess timing and implied investment per segment.
- [ ] The founder-exception log template is present at the bottom of Part B.
- [ ] Part C names the required motion, channel stack, whole-product surface, and mod-107 / mod-108 / product-roadmap hand-off per not-now segment — as sequencing input, not as designed solutions.
- [ ] Part C closes with a one-page beachhead-commitment memo addressed to the founder's team.
- [ ] The not-now section fits back into the Exercise 01 ICP one-page scorecard as a compressed 3-4-line summary per segment; the full detail lives in this exercise's `part-b-not-now-list.md` as the linked supporting document.
- [ ] Any factual claim (partner names, expected unlock timing, competitor deprecation dates) that cannot be defended from public sources is flagged with `needs-research` rather than fabricated.

## Common ways this exercise goes wrong

- **Yes-segment too broad to defend.** The beachhead statement includes three "or" clauses and covers 500 companies — the segment is too broad to concentrate on and too broad to reference-pattern across. Narrow until the Moore criteria all pass.
- **Not-now list of only-obvious exclusions.** Naming "consumer" as a not-now for a B2B startup is not a discipline — no one was going to serve consumer. The not-now list has to name the segments the founder is *tempted* to serve — usually the aspirational-enterprise, the peer-adjacent, and the sympathetic-smaller.
- **Unlock condition without a specific auditable trigger.** "When the time is right" is not an unlock; the founder cannot check whether it has fired. Every unlock is a specific event with a yes/no answer six months from now.
- **Meanwhile action that has never been executed.** The "waitlist" is a promised email nobody has ever actually sent; the "referral partner" is a name in a slide deck with no reciprocal agreement. Test each meanwhile against a real lead; the fantasy meanwhiles are the ones that dissolve when the founder needs to enforce them.
- **Missing the emotionally-sympathetic-smaller segment.** The founder writes off "obvious enterprise" cleanly but has a soft spot for the individual OSS maintainer or the bootstrapped indie hacker — and quietly serves them. Name the sympathetic segment as a not-now; the emotional cost of naming it is exactly the sign it needs to be named.
- **Hand-off packet that designs the motion.** The exercise is legibility, not design. Naming "enterprise MEDDPICC will be required" is the hand-off; writing the enterprise-AE job description belongs in mod-107.
- **No founder-exception log.** Without a written log, every exception is tacit; the log makes exceptions reviewable. Ship even an empty log.
- **Beachhead-adjacency risk under-weighted.** The founder picks a not-now segment where the firmographic distance from the beachhead is small ("fintech is basically like devtools") and lets deals in. The distance that matters is *reference-pattern distance* — whether the beachhead's customers talk to the fintech segment's buyers. Usually they don't; the beachhead's win doesn't reference into fintech.
- **Not-now list that never gets revisited.** Author the quarterly review cadence into Part B ("founder reviews all not-now unlocks quarterly on {calendar date}"), or the list ossifies and segments stay excluded years after they should have opened.
- **Beachhead-commitment memo missing.** The team needs to hear the exclusion decision from the founder's voice, not read it in an ICP document. The one-page memo is the socialisation instrument; without it, the team's individual instincts pull deals from not-now segments.
- **Too many not-now segments.** Twelve exclusions is not discipline; it is defensive over-authoring. Three to five is the working range; if you find yourself listing more, the beachhead is probably too narrow — widen it a notch and re-author.
