# Exercise 03 — Outbound Cadence Design

**Estimated time:** 3 hours
**Chapter link:** [`03-sdr-ae-outbound-motion.md`](../03-sdr-ae-outbound-motion.md)
**Prerequisite:** Chapter 3 read end-to-end; a mod-104 ICP scorecard with a specific target-account list (or a plausible sample of 20-50 ICP-fit accounts you could enumerate by name); a mod-105 discovery-derived pitch-and-pain summary (or an equivalent working version). If Exercise 01's motion decision is *not* SDR-AE-primary or SDR-AE-layered, you may still run this exercise as the "outbound layer under a PLG motion" or as a "what would inside sales look like" thought experiment.

## Problem statement

Chapter 3 named the SDR-AE inside-sales motion as the workhorse of mid-market B2B software sales, drew on Aaron Ross's *Predictable Revenue* and Mark Roberge's *Sales Acceleration Formula*, and named the failure mode: founders import a cadence template from a public blog, run it for six weeks, get a 0.4% response rate, and conclude "outbound doesn't work for our market" — when the actual problem was that the cadence was designed for a different ICP and different pain and was never tuned to theirs.

This exercise trains you to **author a first cadence** — the multi-channel, multi-touch, tiered-personalisation sequence an SDR (or founder-as-SDR-hybrid per mod-105) actually runs against a specific target-account list, with response-rate expectations grounded in Chapter 3's benchmark ranges and hand-off criteria matched to whichever motion (mid-market SDR-AE or enterprise-adjacent) the ICP + ACV combination requires.

The failure mode this exercise exists to catch: **the founder writes an eight-email cadence borrowed from an Outreach template, sends it to 300 accounts, gets 4 replies (all polite declines), and abandons outbound — without ever tiering personalisation, without a multi-channel design, without a hand-off bar, and without any explicit response-rate expectation to grade the cadence against**.

## Requirements

Deliver a folder `exercise-03/` with three files:

- `part-a-target-list-and-tiering.md` — the target-account list with fit-scoring and personalisation tiering.
- `part-b-cadence-design.md` — the touch-by-touch cadence with channels, timing, and copy.
- `part-c-hand-off-and-benchmarks.md` — the SDR→AE hand-off criteria and the expected response-rate math.

### Part A — Target-account list and personalisation tiering (60 min)

Deliver `part-a-target-list-and-tiering.md`.

**A1 — Target-account list (20 min).** Enumerate at least 20 (ideally 50) named accounts that fit your ICP. For each account, list:

- **Company name**.
- **ICP fit-score** — apply your mod-104 ICP scorecard (firmographic + behavioural). Score each account 1-5 (or Green / Yellow / Red).
- **Buyer role identified** — the specific person (with name if publicly known, or the role and hiring context if not) you would target with the outreach.
- **Trigger event (if any)** — a recent funding round, executive hire, product launch, LinkedIn post, RFP posting, or other public signal that gives the outreach a hook.

Use publicly available sources (LinkedIn, company blog, funding databases like Crunchbase, GitHub / job boards / community signals). Do not invent people or events.

**A2 — Personalisation tiering (20 min).** Chapter 3 differentiates three levels of personalisation:

- **Level 1 (segment-personalised)** — template + account name. Response rate 1-2%.
- **Level 2 (trigger-personalised)** — template + one-sentence reference to a recent event. Response rate 3-5%.
- **Level 3 (deeply-personalised)** — custom email referencing specific product usage, specific job posts, specific technical content. Response rate 8-15%.

Sort your target list into three tiers:

- **Tier 1 (Level 3 personalisation)** — the top ~10-20% of the list by fit-score + trigger strength. Highest ICP fit + strongest trigger event. Deep personalisation; ~30-40 minutes per account of research + drafting.
- **Tier 2 (Level 2 personalisation)** — the middle ~40-60% of the list. Good ICP fit; trigger-based hook. Moderate personalisation; ~5-10 minutes per account.
- **Tier 3 (Level 1 personalisation)** — the long tail. ICP-fit but no strong trigger. Template with account name inserted; ~1 minute per account.

Report the count per tier.

**A3 — Volume math (10 min).** From the tier counts, compute the SDR's realistic weekly capacity:

- Tier 1: how many accounts × 30-40 min/account = how many hours/week the SDR spends on Tier 1?
- Tier 2: how many accounts × 5-10 min/account?
- Tier 3: how many accounts × 1 min/account?
- Total: should fit into ~15-20 hours/week of outreach work (an SDR's other time goes to reply handling, meetings booked, admin, coaching).

If your Tier 1 count × the per-account time exceeds the capacity, either narrow Tier 1 or lower per-account time (with an explicit trade-off note).

**A4 — Not-yet-outreach list (10 min).** Which accounts are *not* on the outbound list right now, and why? Explicit deferral is what keeps the outbound list tight. Examples:

- Accounts already in the CRM pipeline (do not double-touch).
- Accounts served better by PLG top-of-funnel (Chapter 2) — free-tier sign-ups from ICP-fit companies should not be cold-outbounded; they are already in the funnel.
- Accounts below the ACV floor that the SDR-AE motion cannot amortise.
- Accounts above the ACV ceiling that require enterprise motion instead.

### Part B — Cadence design (75 min)

Deliver `part-b-cadence-design.md`.

**B1 — Cadence shape (10 min).** Author a cadence with:

- **Total touches**: 8-14 per Chapter 3's default range.
- **Duration**: 3-6 weeks.
- **Channels**: at least 3 (email + LinkedIn + phone; add video for Tier 1).
- **Break clause**: explicit final touch (breakup email) at the end.

Name your specific numbers (e.g., "12 touches over 4 weeks: 6 emails, 3 LinkedIn, 2 phone, 1 video").

**B2 — Touch schedule (20 min).** Author a day-by-day schedule for the cadence. Structure:

```
Day 1  — Email #1 (introduction + {trigger opener for Tier 1/2 or generic opener for Tier 3} + soft CTA)
Day 3  — LinkedIn connection request (no message)
Day 5  — Email #2 (angle #2 — different pain framing)
Day 8  — Phone call #1 + voicemail if no answer
Day 10 — LinkedIn direct message (referencing the email thread)
Day 12 — Email #3 (case study or social proof)
...
Day 28 — Email #6 (breakup — "closing the loop")
```

Every touch names: the channel, the angle (pain framing / social proof / case study / short check-in / breakup), and whether the copy is templated or personalised. Timing is stated in business days.

**B3 — Copy drafts for the primary email touches (25 min).** Draft actual copy for at least 3 of the email touches — the opener, one mid-cadence angle, and the breakup. Each draft has:

- **Subject line** (or 2-3 subject-line candidates for A/B testing).
- **Body** — 3-8 sentences maximum. Chapter 3's discipline: the buyer reads on mobile, in a busy inbox, in 3 seconds.
- **CTA** — one specific ask (booking a meeting, replying with a yes/no, forwarding to a colleague). One ask per email.

Draft copy for a Tier 2 (trigger-personalised) account. Note where a Tier 3 version would substitute in deeper personalisation, and where a Tier 1 version would generalise.

**B4 — Phone and LinkedIn scripts (10 min).** Draft:

- **Phone script** — a 30-45 second voicemail script for a phone touch, plus a 60-90 second live-call opening if the buyer picks up.
- **LinkedIn direct message** — 2-3 sentences referencing the email thread; different from the email copy.

**B5 — Video message design for Tier 1 (10 min).** For Tier 1 accounts, describe the video message:

- Length (60-90 seconds per Chapter 3's benchmark).
- Content structure (who you are, why you're reaching out to this specific account with this specific hook, one specific ask).
- Tooling (Loom, Vidyard, Sendspark).
- Personalisation depth (name of the account, name of the person, reference to something specific about their environment).

You don't have to record the video; describe the design.

### Part C — Hand-off criteria and response-rate math (45 min)

Deliver `part-c-hand-off-and-benchmarks.md`.

**C1 — Hand-off criteria (15 min).** Author the specific criteria a booked meeting must meet before the SDR hands it to the AE. Chapter 3's default (adapt to your motion):

1. **ICP-fit confirmed** — the SDR can answer "why is this account ICP-fit?" in one sentence.
2. **Buyer role identified** — the meeting is with a buyer, champion, or user-with-influence (not "someone who was curious").
3. **Pain articulated** — a one-line description of the pain in the buyer's own words.
4. **Meeting confirmed** — an actual calendar invite exists, accepted.
5. **Timeline signal** — the buyer has some notion of when a decision might happen.

Adapt each criterion to your product's specifics. Write the hand-off-note template the SDR fills in for each opportunity.

**C2 — Response-rate math (15 min).** Compound the Chapter 3 benchmarks against your cadence to project realistic monthly output:

- Touches / month per tier × per-tier reply-rate benchmark = replies / month per tier.
- Replies × positive-reply-rate = positive replies.
- Positive replies × meeting-book-rate = meetings booked.
- Meetings booked × meeting-held-rate = meetings held.
- Meetings held × hand-off-accepted-rate (60-80% healthy zone) = opportunities.
- Opportunities × close-rate (20-40% mid-market) = closed deals.

Present as a table. Use Chapter 3's benchmark ranges; note where you're using the top or bottom of the range and why.

**C3 — Comp-plan alignment (5 min).** Chapter 3's rule: SDR compensated on the metric that most closely predicts revenue — **held meetings** or **hand-off-accepted opportunities**, not booked meetings. Author the SDR quota structure:

- Base + variable split.
- Primary quota metric (held meetings / hand-off-accepted opps).
- Secondary metrics tracked but not comped on.
- Ramp period (typically 4-8 weeks to full quota for a mid-market SDR).

**C4 — SDR readiness / founder-hybrid mode (10 min).** Per Chapter 3's timing discussion, name where the SDR role sits in your team today:

- **Founder-as-SDR-hybrid mode** — the founder runs this cadence herself; the exercise output is the founder's own daily discipline.
- **First SDR hire post-AE-at-target** — SDR is hired after the founder has closed 20-30 deals (mod-105) and the AE is at target and complaining about pipeline capacity.
- **Second+ SDR** — scale the motion after the first SDR is at target.

If you are pre-first-SDR, note it explicitly; the cadence is what the founder runs herself until the hiring signals are green.

## Starter guidance

- **The target-account list is the load-bearing input.** A brilliantly-designed cadence run against off-ICP accounts is decoration. Spend real time on A1's fit-scoring and A2's tiering; the cadence quality lives or dies on which accounts you touch, not what the email says.
- **Personalisation tiering is what scales the motion.** Level 3 everywhere is unaffordable (30 min × 300 accounts = 150 hours = 4 weeks of a full-time SDR just on drafting). Level 1 everywhere caps response at ~1%. Tiering is what lets a real SDR ship 300-500 touches / month with a defensible response rate.
- **Multi-channel is not optional.** Email-only cadences see 30-50% lower response rates than multi-channel per Chapter 3. LinkedIn + phone are cheap adjacent touches that meaningfully lift the compound response; video is high-effort but Tier-1-effective.
- **Timing matters.** Chapter 3's default: 2-4 days apart at the front of the cadence, tightening near the end. Send in the buyer's timezone. Skip Fridays, Mondays, holidays. Do not batch-send at 9 AM on a Monday to a global list; the buyer reads on her clock, not yours.
- **The breakup email is not decoration.** Cadences without an explicit end fatigue the account and burn the SDR's domain reputation over time. The breakup email closes the loop cleanly ("if this isn't a priority now, no worries — I'll follow up in a quarter") and moves the account to nurture rather than perpetual cadence.
- **Copy should sound like a human.** Read your Part B copy aloud; if it sounds like a template (buzzwords, generic pain claims, three CTAs stacked), the buyer will read it as a template and skip. Write like you'd write to a peer.
- **One ask per email.** "Book a meeting" OR "reply yes/no" OR "forward to a colleague," not all three. Multiple asks reduce conversion because the reader defers the decision.
- **The hand-off note is what makes the SDR-AE motion work.** Chapter 3's hand-off-accepted ratio (60-80% healthy zone) is only measurable when the hand-off note is a defined artifact. Draft the template in C1; make it a required field in the CRM.
- **Response-rate math grounds expectations.** If your Part C math predicts 6 booked meetings/month against a quota of 30, either the math is optimistic (the founder is guessing high on reply-rates) or the volume is too low (the SDR needs more touches). Reconcile before running the cadence, not after.
- **Do not run the cadence until the AE (or founder-as-AE) has ramp capacity.** Chapter 3's *hire-SDR-before-AE* trap. Booking meetings the AE cannot run wastes the SDR's output and the buyer's time.
- **Comp on held, not booked.** Chapter 3's discipline: the SDR's quota is held-meetings or hand-off-accepted opportunities. Comping on booked incentivises the SDR to book anything with a pulse; held-meeting comp forces the SDR to book meetings that actually happen.
- **The founder-as-SDR-hybrid stage is not shameful; it's mandatory.** Chapter 3 is explicit that the founder personally runs the SDR role during the first 20-30 deals (mod-105 boundary). The exercise output at this stage is *the founder's own daily cadence discipline*, not a hire spec.

## Acceptance criteria

Your submission is complete when:

- [ ] Part A enumerates at least 20 named target accounts with ICP fit-score, buyer role identified, and (where available) a trigger event citation to a public source.
- [ ] Part A sorts accounts into Tier 1 / 2 / 3 with per-tier counts and per-tier personalisation description (Level 1 / 2 / 3).
- [ ] Part A runs the volume math (touches/week × personalisation minutes = SDR-hours needed) and reconciles to a realistic 15-20 hours/week outreach budget.
- [ ] Part A names accounts explicitly *not* on the outbound list with rationale (in-pipeline / served by PLG / below ACV floor / above ACV ceiling).
- [ ] Part B names cadence shape (touch count, duration, channels, break clause).
- [ ] Part B names a day-by-day touch schedule with channel, angle, and templated/personalised distinction per touch.
- [ ] Part B drafts actual copy for at least 3 email touches (opener + mid-cadence + breakup) with subject line, body ≤ 8 sentences, and single CTA per email.
- [ ] Part B drafts a phone voicemail script (30-45s) and a live-call opening (60-90s), plus a LinkedIn direct message (2-3 sentences).
- [ ] Part B describes the Tier 1 video message design (length, structure, tooling, personalisation depth).
- [ ] Part C names the hand-off criteria (5 items or your adapted set) and provides a hand-off-note template.
- [ ] Part C runs the response-rate math table compounding Chapter 3 benchmarks against the Part A + B design, projecting monthly output from touches to closed deals.
- [ ] Part C names the SDR comp-plan structure (base/variable, primary quota metric, ramp period) — or, if in founder-as-SDR-hybrid mode, explicitly names that mode and describes the founder's daily discipline.
- [ ] Any factual claim (a benchmark rate, a competitor cadence pattern) that is not from Chapter 3's cited sources or your own data is flagged `<!-- needs-research: ... -->` rather than invented.
- [ ] Every named person or trigger event in Part A is either citable to a public source (LinkedIn URL, funding-round announcement, company blog post) or clearly labelled as a role-only reference (e.g., "VP Engineering at Acme Corp — specific person not yet identified").

## Common ways this exercise goes wrong

- **Off-ICP-target-list trap.** Part A pads the list with 50 accounts pulled from a generic industry database without ICP-scoring. Cadence runs but the accounts don't respond because they're not the right accounts. Fix: A1's ICP-scoring is required; unscored accounts don't go on the list.
- **Level-3-everywhere trap.** Founder writes "we'll personalise all 200 accounts deeply." Volume math (A3) shows 200 × 30 min = 100 hours; SDR has 20 hours/week for outreach. Cadence never fully executes. Fix: tier the list; Level 3 to the top 20-30 accounts only.
- **Level-1-everywhere trap.** Founder writes "we'll do templated outreach at scale." Response rate caps at ~1%; volume-to-conversion math (C2) shows the pipeline never generates enough opportunities. Fix: at least 20% of the list gets Level 2 or Level 3.
- **Email-only-cadence trap.** Part B skips LinkedIn / phone / video entirely. Response rate 30-50% below multi-channel benchmark. Fix: cadence includes at least 3 channels; Tier 1 includes 4.
- **Cadence-with-no-breakup trap.** Part B's schedule ends at Email #6 with no explicit "closing the loop" touch. Account gets emailed indefinitely; domain reputation burns. Fix: explicit breakup email in B2's schedule.
- **Copy-reads-as-template trap.** Part B's drafted copy is buzzwordy, has stacked CTAs, or sounds like a sales robot. Read aloud; if it sounds template, rewrite. Fix: one specific pain, one specific hook, one specific ask per email; sentence structure that mirrors how the founder would email a peer.
- **Timing-copy-from-blog trap.** Part B's schedule is copy-pasted from a public Outreach template with no adaptation to the founder's buyer's actual timezone / industry rhythm. Fix: name the timezone; skip holidays and dead weeks; note if the buyer's industry has cyclical rhythm (retail Q4 freeze, education summer break).
- **Missing-hand-off-note trap.** Part C names hand-off criteria but doesn't produce a template the SDR fills in. Fix: the hand-off note is an artifact — draft the exact fields the SDR fills in, so the AE sees consistent structure per opportunity.
- **Response-rate-math-optimistic trap.** Part C's compounded math predicts unrealistic output ("we'll close 8 deals/month from 200 touches"). Founder using the top of every benchmark range without justification. Fix: use midpoints of Chapter 3's ranges; note when you're using the top and why (specific ICP fit, historical evidence).
- **Response-rate-math-pessimistic trap.** Mirror of the above — founder uses the bottom of every range and predicts 0.5 deals/month, gives up. Fix: use midpoints unless historical data justifies below-benchmark expectations.
- **Comp-on-booked trap.** Part C's comp plan comps the SDR on booked meetings without factoring in held-rate or hand-off-accepted. SDR books junk to hit quota. Fix: primary comp metric is held meetings or hand-off-accepted opportunities.
- **Founder-hides-from-being-SDR trap.** Founder writes an SDR job spec instead of running Part B herself. The cadence is theoretical because it was never tested against real buyers. Fix: if pre-first-SDR-hire, run the cadence yourself for 4-6 weeks first; the exercise's real output is the *tested* cadence you'll hand to the first SDR when hired.
- **No-not-yet-list trap.** Part A includes every ICP-fit account without carve-outs for in-pipeline accounts, PLG-served accounts, or above/below-ACV accounts. Cadence double-touches active pipeline and dilutes signal. Fix: A4's not-yet list is required; every named account is either on the outbound list with a fit-score, or on the not-yet list with a reason.
- **No-tuning-cycle trap.** Cadence is authored once and shipped forever; response rates drift down as templates fatigue, no A/B testing is scheduled. Fix: note in Part B that email copy is A/B tested monthly, phone scripts quarterly, video templates each product-cycle change.
