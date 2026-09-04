# Exercise 05 — Crossing-the-Chasm Beachhead Selection

**Estimated time:** 3 hours
**Chapter links:** [`05-chasm-beachhead.md`](../05-chasm-beachhead.md), [`02-dunford-five-components.md`](../02-dunford-five-components.md)
**Depends on:** Exercise 01 — the Component 4 best-for characteristics are the space this exercise's beachhead is a slice of.
**Prerequisite reading:** [Geoffrey Moore — *Crossing the Chasm*](https://www.harpercollins.com/products/crossing-the-chasm-3rd-edition-geoffrey-a-moore) Introduction + Chapters 3-4 (~2 hr); Chapter 5 (~30 min).

## Problem statement

Chapter 5 named Moore's technology-adoption lifecycle (innovators → early adopters → early majority → late majority → laggards), the **chasm** between visionary early adopters and pragmatist early majority, and the **beachhead** strategy Moore proposed for crossing it — pick one narrow segment, concentrate resources on winning it dominantly, generate a concentrated reference pattern, then expand via **bowling-pin adjacency** to the second-row segments.

The failure mode this exercise exists to catch: **the founder ships a positioning that serves five plausible segments equally well, hires against all five, spends demand-gen budget across all five, and 18 months later has 12 unhappy customers per segment instead of 60 happy customers in one segment.** Positioning without segment commitment is theatre; the beachhead choice is the whole point.

This exercise makes you enumerate three candidate beachhead segments for your Exercise 01 positioning, score each against Moore's six criteria, pick one and defend the choice, and — the un-optional part — write the explicit "not-now" list of segments you are saying no to for the next 12 months.

## Requirements

Deliver a folder `exercise-05/` with:

- `part-a-candidate-segments.md` — three candidate beachhead segments enumerated from the Exercise 01 best-for space.
- `part-b-six-criteria-scoring.md` — each candidate scored against Moore's six criteria with defensible reasoning.
- `part-c-beachhead-selection-memo.md` — a one-page memo picking one beachhead, defending the pick, and listing the explicit "not-now" segments with per-segment reasoning.
- `part-d-bowling-pin-plan.md` — the second-row and third-row pins the beachhead's wins will unlock, with per-adjacency reasoning.

### Part A — Enumerate three candidate beachhead segments (45 min)

Return to your Exercise 01 Component 4 (best-for characteristics). The best-for space is the *broadest* population where your positioning resonates. The beachhead is a *narrower slice* of that space — narrow enough to dominate this quarter with the resources you have, and structured enough to generate a concentrated reference pattern.

Enumerate **three candidate beachhead segments** you could commit to. Each candidate is a specific slice of the best-for space, tightened along one or more of:

- **Vertical / industry** — devtools/observability vs. data-infra vs. fintech vs. healthtech.
- **Company stage / size** — pre-seed / seed / Series-A / Series-B / mid-market / enterprise.
- **Geography** — SF Bay Area / NYC / London / EU / global.
- **Technology stack** — GitHub vs. GitLab; AWS vs. GCP; specific incumbent tools installed.
- **Situational trigger** — recent funding round / recent hiring push / recent org restructuring / board-imposed KPI.
- **Buyer characteristic** — engineering-manager-owned vs. VP-Eng-owned vs. platform-team-owned.

For each candidate, produce:

- **Candidate name and one-line description.** ("Mid-market B2B SaaS devtools companies, 50-150 engineers, distributed / async-first, on GitHub, engineering-manager-KPI on PR cycle time.")
- **Rough sizing.** How many companies globally / regionally fit this description? A rough order of magnitude is enough (100? 500? 5,000?); source the number if you can.
- **Peer community.** Where do members of this segment congregate — conferences, Slack communities, subreddits, industry publications, executive dinners? If there is no shared peer community, name that (it will fail Moore's reference-able criterion in Part B).
- **Existing candidates from your customer base or discovery corpus.** If you have real customers or interview subjects who fit this segment, name how many.

Pick three candidates that are *plausibly viable* — not three obviously-doomed candidates plus one clear winner. The exercise is the honest scoring of three real options.

### Part B — Score each candidate against Moore's six criteria (60 min)

For each of the three candidates, score against Chapter 5's six beachhead criteria. Deliver as a table (one row per candidate) plus a per-criterion paragraph for each candidate.

The six criteria, restated from Chapter 5:

1. **Compelling reason to buy.** Segment has pain acute enough that inaction is more expensive than switching cost. Not "nice to have."
2. **Whole product achievable.** Your product plus a small, achievable set of partners / integrations / services delivers the *complete* solution the segment needs. No 10-feature gaps.
3. **Reference-able.** Segment members talk to each other. Wins compound because buyers know each other, attend the same conferences, participate in the same peer communities.
4. **Named alternatives structurally beatable.** Segment currently uses alternatives you can be *obviously* better than (per Exercise 01 Component 1). Not a well-loved incumbent you can only match at parity.
5. **Sized for concentrated wins.** Small enough that you can *dominate* it with the resources you have (fraction of a founder's time, one AE, one PMM). Not a segment that requires 100 salespeople.
6. **Adjacent to the "next" segments.** Beachhead has clear second-row pins — technically, culturally, or via shared buyer identity adjacent to the segments you'll want next.

For each candidate × criterion combination, produce:

- **Score:** PASS / MIXED / FAIL.
- **Reasoning:** one paragraph naming the specific evidence for the score. Not "yes, this segment has a compelling reason to buy" — "the segment's engineering managers are personally spending 6-8 hours a week on PR coordination (per interview 3, interview 7); the pain is acute; the switching cost of onboarding a tool is 1-2 hours per manager; the trade-off tips."

A candidate that scores FAIL on any criterion is disqualified as a beachhead *this quarter* — note it and move on. A candidate that scores MIXED on ≥ 2 criteria is at high risk and should be scored down in Part C's selection.

The six-criteria scoring is the hardest part of the exercise. It is also the point.

### Part C — Beachhead selection memo (60 min)

Pick **one** candidate as your beachhead. Write a one-page memo (~500-800 words) in the following structure:

1. **The pick.** Which candidate you selected, in one sentence.
2. **The defence.** Why this candidate over the other two, one paragraph per rejected candidate naming the specific criterion (or criteria) that tipped the decision. Do not hand-wave — if you rejected Candidate B because it fails Criterion 2 (whole product achievable), name the specific whole-product gap.
3. **The commitment.** What "committing to this beachhead" means operationally for the next 12 months: which sales motion, which demand-gen channels, which product bets, which pricing shape, which conference sponsorships or content properties. This is the ripple through the rest of the track — mod-104 (ICP), mod-105 (sales), mod-106 (pricing), mod-107 (motion), mod-108 (channels) all follow from this pick.
4. **The two temporal reads.** Chapter 5's two reads: (a) *early-adopter validation now* — which specific customers in this segment can we win this quarter and next, generating the first 10-30 concentrated wins; (b) *mainstream reference-buyer path later* — if we dominate this beachhead in 12 months, does the reference pattern let us cross the chasm into the early majority? Name both. If the two agree, say so. If they diverge, name which one you're weighting and why.
5. **The pressure test.** In one paragraph, name the specific way this beachhead choice could be wrong — the failure mode you are most worried about. Chapter 5 lists six common failure modes (too broad, too narrow, wrong adjacencies, whole-product gap, not reference-able, quarter-optimising). Which of these is your beachhead most at risk of? What would you watch for over the next 90 days that would tell you the choice was wrong?

#### The "not-now" list (the un-optional part)

The beachhead choice is not binding unless you name the segments you are saying **no to for the next 12 months**. Include a list in the memo — every segment from the best-for space that you are *not* committing to, each with a reason:

- **Segment name and one-line description.**
- **Reason for not now** — one of: whole-product gap (name it), not reference-able (name why), wrong adjacencies (name what the wins wouldn't unlock), quarter-optimising vs. mainstream path (name the divergence), resources (specify what you'd need to serve it).
- **Revisit trigger** — the specific event that would move the segment from "not now" to "now." "When we ship SSO/SCIM/audit logs" or "when the mid-market beachhead is dominated (60+ concentrated wins in devtools/observability)" or "when the seed-stage segment shows a repeatable pilot pattern."

The revisit-trigger discipline is what turns "no" into "not yet." A no-list without triggers is a permanent kill; a no-list with triggers is a sequencing document.

### Part D — Bowling-pin adjacency plan (45 min)

For the beachhead you picked in Part C, name the second-row and third-row pins the beachhead's wins will unlock. Deliver `part-d-bowling-pin-plan.md` as a small diagram or table.

- **Second-row pins (2-4 segments).** Each: name the segment, name the shared characteristic (technical / cultural / buyer-identity / product-surface) that makes the beachhead wins applicable, name the specific mechanism by which the wins in the beachhead help you sell into this second-row pin (case-study transfer, executive-network overlap, product-surface reuse, analyst-coverage carryover).
- **Third-row pins (2-4 segments, sketched).** These are the segments the second-row pins would unlock. Sketch, don't over-develop.

If you cannot name 2+ second-row pins with credible adjacency, Chapter 5 argues the beachhead itself is misspecified — you have picked a segment with no growth story. Either the beachhead is too peculiar (too narrow) or the vision behind it is too parochial (fails Criterion 6 — adjacency). Note this and revisit Part C.

## Starter guidance

- Read Chapter 5 end-to-end before starting. The six criteria are the operating rubric; the two temporal reads are the strategic frame; the "not now" list is the discipline.
- **The most common failure mode in this exercise is picking three candidate segments that are all obvious variants of the same segment.** "Mid-market B2B SaaS" and "Series-B B2B SaaS" and "growth-stage B2B SaaS" are the same candidate scored three times. Force yourself to enumerate candidates that are structurally different — e.g., mid-market vertical vs. enterprise vertical vs. adjacent-vertical-with-shared-buyer.
- **Score honestly on Criterion 2 (whole product achievable).** Founders under-weight this most. If the segment requires SSO, SCIM, audit logs, per-team RBAC, industry-specific compliance certifications, or 4+ integrations you don't have, the segment is not a beachhead this quarter — it is a wish for after the whole-product gap closes.
- **Criterion 3 (reference-able) is the criterion that separates beachheads from markets.** "SMB SaaS" is not a beachhead — SMB SaaS members do not talk to each other; there is no shared peer community; wins in one buyer do not beget wins in others. Pick a segment with a specific, nameable community — a conference, a Slack, an industry publication, a peer executive dinner series.
- **Criterion 5 (sized for concentrated wins) is a founder-resource check.** How many prospects can the founder personally touch in a quarter? At founder-led sales scale that is usually 30-60 conversations. If the beachhead is 5,000 companies distributed across three continents, you cannot dominate it this quarter — narrow further.
- **Criterion 6 (adjacent to next segments) is the vision check.** A beachhead that is defensible but has no clear next pin is a beachhead that ends at 30 customers. If Part D's second-row pins are hand-waved, revisit Part C.
- **Do not skip the "not now" list.** Founders leave it blank because saying no feels risky. Blank is the failure — the whole beachhead discipline is the *saying no*. If you cannot name what you are giving up, you have not made the choice.
- **The two temporal reads sometimes disagree.** If the easiest segment to sell this quarter is not the same as the segment whose reference pattern lets you cross the chasm later, name the disagreement. Chapter 5 argues the mainstream-path read wins; if you disagree, defend the choice explicitly.
- Cross-reference with mod-102's PMF scorecard if you have one. A segment where retention is flattening and Sean Ellis scores well is the strongest early-adopter validation for a beachhead candidate. A segment where retention is leaking is a beachhead only if you're prepared to fix the leak first.
- If you are pre-customer and cannot ground the six-criteria scoring in real data, mark each score `<!-- needs-research: [what you need to verify] -->` and note in the memo that the beachhead selection is provisional pending discovery / pilot data.

## Acceptance criteria

Your submission is complete when:

- [ ] Part A enumerates ≥ 3 candidate beachhead segments, each with a one-line description, a rough sizing, a named peer community (or an explicit "no shared community"), and any existing customer / interview evidence.
- [ ] The three candidates are structurally different — not three variants of the same segment.
- [ ] Part B scores each of the three candidates against all six Moore criteria (PASS / MIXED / FAIL) with per-cell reasoning grounded in specific evidence.
- [ ] Any FAIL score is defended with a specific gap named (e.g., "SSO/SCIM/audit logs missing" — not "not enterprise-ready").
- [ ] Part C's memo picks one beachhead in one sentence, defends against the two rejected candidates with the specific criterion (or criteria) that tipped, names the operational commitment (motion, channels, pricing shape, sales-hire profile) for the next 12 months, addresses both temporal reads (early-adopter now, mainstream reference-buyer later), and names the specific failure mode the choice is most at risk of.
- [ ] Part C includes an explicit "not now" list with per-segment reason and per-segment revisit trigger. The list is non-empty — at least the two rejected candidates plus any other segments from the best-for space you are not committing to.
- [ ] Part D names ≥ 2 second-row pins and ≥ 2 third-row-pin sketches, each with the specific adjacency mechanism (shared buyer, shared community, shared product surface, shared analyst coverage) named.
- [ ] The beachhead selected in Part C is narrower than the Exercise 01 Component 4 best-for space. If it is the same, revisit — the beachhead discipline requires narrower than best-for.
- [ ] The beachhead selected is compatible with the Exercise 03 strategic-narrative shift. If the narrative's shift is "AI collapses the cost of X" and the beachhead is a segment for whom X is not the primary pain, one of the two is inconsistent — reconcile.

## Common ways this exercise goes wrong

- **Three candidates that are variants of the same segment.** Force structural difference.
- **Scoring the six criteria as PASS / PASS / PASS / PASS / PASS / PASS.** If every criterion passes for every candidate, you have not scored honestly. Chapter 5 explicitly calls out that founders under-weight Criterion 2 (whole product) and Criterion 6 (adjacencies); check those first.
- **"SMB SaaS" as a beachhead.** SMB SaaS is a market size, not a segment. There is no peer community that "SMB SaaS" attends. Narrow to a specific vertical, a specific stage, or a specific buyer.
- **Whole-product gap ignored.** If the segment requires 6 months of engineering to reach parity on table-stakes features, it is not a beachhead this quarter — mark it as a "not now" and revisit when the features ship.
- **Empty "not now" list.** The whole discipline. Blank means the choice was not made.
- **"Not now" list without revisit triggers.** No is not equal to no forever. Each no needs a specific event that would move it to yes.
- **Beachhead = best-for.** The best-for is the space; the beachhead is a slice. Committing to the whole best-for space this quarter is not the beachhead discipline; it is the "we can't say no to any segment" failure.
- **No bowling-pin plan.** A beachhead with no named next pins is a beachhead that ends at 30 customers.
- **Quarter-optimising.** Picking the segment that is easiest to sell this quarter, ignoring whether the wins there generate the reference pattern for the mainstream buyer. Chapter 5 explicitly weights the mainstream-path read.
- **Ignoring the narrative + positioning coupling.** The beachhead has to be compatible with the Chapter 4 narrative's shift and the Chapter 2 positioning's alternatives. If they diverge, one is wrong.
- **Treating this as a paper exercise.** The beachhead memo is a *commitment* document. It should be dated, signed, versioned, and reviewed at least quarterly. If it is not going into the founder's operating playbook, the exercise did not land.
