# Exercise 04 — Outbound Sequence Authoring

**Estimated time:** 3 hours
**Chapter link:** [`04-outbound-at-seed-scale.md`](../04-outbound-at-seed-scale.md)
**Prerequisite:** Chapter 4 read end-to-end; Exercise 01 completed (a portfolio that names outbound as either the primary or the experimental — if neither, run this exercise as a targeted-outbound pilot design against a specific ICP sub-segment); a mod-104 ICP scorecard with buyer / user / champion split; a mod-103 positioning statement; a mod-105 cold outreach corpus if available (from mod-105 exercise 01), else the founder's best-guess drafts.

## Problem statement

Chapter 4 named the seed-scale outbound motion as three modifications to the *Predictable Revenue* tradition: **founder-as-first-SDR**, **hand-curated signal-selected list**, and **deep personalisation on every touch**. The failure mode: the founder loads a 5,000-account Apollo export against firmographic filters, sends templated emails, gets 0.4% reply rate, concludes "outbound doesn't work". The Level-3-on-every-touch version against 100-300 hand-curated accounts produces 8-20% reply rates — the difference between "outbound doesn't work" and "outbound is producing meetings".

This exercise trains you to **author the seed-outbound cadence** — the signal-selection criteria for the list, the six-touch cadence with three distinct angles, three example fully-hand-written touches against real target accounts, the personalisation scaffold, the objection-and-response scripts, and the instrumentation setup. The output is the cadence document the mod-107 Chapter 3 SDR-AE motion will eventually inherit.

The failure mode this exercise exists to catch: **the founder runs outbound in her head — writes each email on the fly, has no signal-selection discipline, has no angle diversity across touches, has no personalisation scaffold — and produces a Q1 of outbound that generates some meetings but no transferable pattern-knowledge; the future SDR hire arrives and cannot reproduce what the founder was doing because it was never written down.**

## Requirements

Deliver a folder `exercise-04/` with five files:

- `part-a-target-account-list.md` — the signal-selection criteria + 30-account starter list.
- `part-b-cadence-structure.md` — the six-touch cadence structure with three angles.
- `part-c-three-example-sequences.md` — three fully-hand-written cadences to three real target accounts.
- `part-d-objections-and-responses.md` — the objection-and-response scripts.
- `part-e-instrumentation-and-cadence-document.md` — the tracking setup + the cadence document that the SDR inherits.

### Part A — Target-account list criteria + 30-account starter (45 min)

Deliver `part-a-target-account-list.md`. Chapter 4's list-building discipline is signal-selection, not firmographic-filter.

**A1 — Signal-selection criteria (15 min).** For each of Chapter 4's four categories, write your signal-selection criteria:

- **Category A — buying-context signals.** Which specific signals define an in-context account for your ICP? (Funding announcement recency threshold? Hiring signals — which roles specifically? Executive-change signals — which titles? Public pain signals — which topics or events?) For each signal type, name the source (Crunchbase, LinkedIn Jobs, TechCrunch, YC job board, Twitter, GitHub, industry press).
- **Category B — usage / tool signals.** Which adjacent tools / open-source projects / community footprints indicate an account is a fit? Name specific tools, GitHub-observable patterns, community memberships, event-attendee lists.
- **Category C — network / referral signals.** How will you generate referrals from existing customers? Who in your team's network is a second-degree source? Which alumni networks overlap with your ICP?
- **Category D — firmographic signals.** What are the firmographic filters that gate the list (per mod-104 Layer-1)? Name the specific size / industry / geography / funding-stage filters.

For each category, also note:
- Priority tier at seed (Category A = top-tier priority; D-only = deprioritised).
- Weekly volume you expect to source from this category (10-30 new accounts total per week across all categories).

**A2 — 30-account starter list (25 min).** Populate a 30-account starter list. For each account, capture:

| # | Account name | Category (A/B/C/D) | Specific signal-hook | Buyer/champion contact (name + role + LinkedIn URL if known) | Priority tier (top-30 / mid-tier) | Notes |

Half the value of this exercise is the discipline of hand-adding 30 accounts with real signal-hooks — the exercise is not honest if the accounts are made up. Use real companies. If your product is at pre-launch and you cannot yet identify real accounts, use publicly-visible companies in the ICP with the signals you would target if you were live (label as "prospective").

**A3 — List volume check (5 min).** From your A1 volume expectations + A2 list, confirm:
- Weekly new-account add rate → produces a sustainable 100-300 active list over 8-12 weeks.
- The list is bounded — accounts that reach cadence completion without response retire to a nurture list rather than staying active indefinitely.

### Part B — Cadence structure (30 min)

Deliver `part-b-cadence-structure.md`.

**B1 — Six-touch cadence template (10 min).** Reproduce Chapter 4's six-touch cadence, adapted to your channel mix (email + LinkedIn + phone if applicable). For each touch:

- Day (relative to touch 1).
- Channel (email / LinkedIn message / LinkedIn connection request / phone / video / other).
- Purpose (opener / reinforce / new angle / right-person / breakup).
- Rough length target (in words for email; sentences for LinkedIn).

**B2 — Three-angle design (15 min).** For each of Chapter 4's three angles (pain / outcome / right-person), write:

- **Angle name and touch position** (pain = touch 1; outcome = touch 3; right-person = touch 5).
- **The reader-anchor** (what does the recipient see in the first 1-2 sentences that makes her want to keep reading?).
- **The specific pain / outcome / question** the angle attacks — grounded in mod-103 positioning + mod-104 pain shape.
- **The ask** — what specifically does the recipient say yes to? Not "book a demo" for touch 1; a low-commitment ask (a specific question, a "send you the writeup" offer, a "compare notes" call).
- **The signal-hook slot** — how does the touch reference the specific Category-A/B/C signal that put the account on the list?

**B3 — Break-clause design (5 min).** The final touch is professional close ("if this isn't a priority right now, no follow-up from me — happy to reconnect if things change"). Write your specific break-clause template. Confirm it does not "guilt" the recipient and does not create a follow-up commitment the founder can't keep.

### Part C — Three fully-hand-written cadences (60 min)

Deliver `part-c-three-example-sequences.md`.

Pick 3 accounts from Part A2's list — one from Category A (buying-context), one from Category B (tool signal), one from Category C (network / referral). For each, write the full six-touch cadence in the shape it would actually be sent.

**For each cadence:**

- **Header** — account name, contact name and role, signal-hook, priority tier.
- **Touch 1 (Day 1) — full email.** Subject line + body. Personalisation is real and specific to this account. Not a template with a `{{company}}` placeholder; a fully-hand-written first email.
- **Touch 2 (Day 3) — LinkedIn connection.** Note the connection message text (or "no message"), or the alternative touch if LinkedIn is not the fit.
- **Touch 3 (Day 6) — full email #2 (outcome-framing angle).** Subject line + body. References the signal-hook or a related one; different anchor than touch 1.
- **Touch 4 (Day 10) — LinkedIn DM or alternative.** Short, references the email thread.
- **Touch 5 (Day 14) — full email #3 (right-person or new-angle).** Short, asks whether this is the right person or references a specific new signal.
- **Touch 6 (Day 21) — breakup email.** Professional close.

**Time budget check.** Chapter 4's ten-minute rule: each email should have taken ≤12 minutes to write. Note whether your three cadences fit within that budget (be honest — this is the calibration exercise). If any email took 25 minutes, the personalisation is over-invested and the volume will not sustain; edit down.

### Part D — Objections and responses (30 min)

Deliver `part-d-objections-and-responses.md`.

**D1 — Anticipated objections (15 min).** List 5-10 objections you expect to hear in reply to the cadence. Ground the list in either mod-105's discovery-call objection log (if available) or in the practitioner writing (Josh Braun's objection library, Kazanjy's *Founding Sales*). Common seed-outbound objections:

- "We build this in-house."
- "We already use [competitor]."
- "The pain is real but not a priority this quarter."
- "The security / procurement review is a barrier."
- "We're not the right person; [X] handles this."
- "Not interested — please remove me."
- "What's your pricing?" (early-stage price sniff).
- "Send me some info and I'll take a look." (soft brush-off).

**D2 — Response scripts (15 min).** For each objection, write a 3-5 sentence response that:

- Acknowledges the objection genuinely (does not argue or evade).
- Names a *specific* reason the objection may not preclude a conversation (either it does — in which case the response accepts the disqualification and the account goes to nurture — or a specific counter-point that changes the frame).
- Offers a low-commitment next step (a resource, a 15-minute compare-notes call, a specific piece of content).

Chapter 4's rule: the response is what the SDR will use verbatim; if the founder's response only works because she is the founder ("as the founder, I can offer you..."), the response does not transfer and needs to be rewritten in a form the SDR can run.

### Part E — Instrumentation + cadence document (15 min)

Deliver `part-e-instrumentation-and-cadence-document.md`.

**E1 — Minimum-viable instrumentation (5 min).** Name your minimum-viable stack per Chapter 4:

- Account list system (spreadsheet / HubSpot / Attio / Close / Airtable).
- Touch log format (per-account log with touch number, date, channel, subject-line variant, response state).
- Reply-state categories (no-response / positive-reply / negative-reply / meeting-booked / meeting-held / out-of-office / wrong-person / unsubscribe).
- Opportunity-linkage rule (when a meeting produces an opportunity, how is first-touch attribution preserved?).
- Weekly summary metrics (touches sent, open rate, reply rate, positive reply rate, meetings booked, meetings held, rolling 4-week average).

Confirm you are NOT buying full Outreach / Apollo / Gong stack yet (Chapter 4's tool-before-motion trap). Note the trigger for adding the stack: 3+ months of validated cadence + SDR hire imminent.

**E2 — Cadence document (10 min).** Write a 1-2 page cadence document — the artifact the SDR hire inherits. Structure:

```
# Outbound Cadence Document — {product} — {version, date}

## Target-account list criteria
- Category A signals: {specific criteria + sources}
- Category B signals: {specific criteria + sources}
- Category C signals: {specific criteria + sources}
- Category D firmographic filters: {specific filters}
- List size: {100-300 active accounts}
- Weekly new-account add: {10-30}

## Priority tiering
- Top-30: {who runs — founder or top-AE; Level-3 full-hand-written personalisation}
- Mid-tier (30-200): {who runs — SDR or founder overflow; Level-2 template + signal-hook substitution}
- Long tail (200-300 D-only): {who runs — SDR; Level-1 templated}

## Cadence structure
- Touch 1 (Day 1, email): pain-framing; {template scaffold + personalisation rules}
- Touch 2 (Day 3, LinkedIn): connection request; {message template}
- Touch 3 (Day 6, email): outcome-framing; {template scaffold}
- Touch 4 (Day 10, LinkedIn DM): {template scaffold}
- Touch 5 (Day 14, email): right-person angle; {template scaffold}
- Touch 6 (Day 21, email): breakup; {template scaffold}

## Personalisation scaffold (per-touch, 10-minute rule)
- 1 min: pull up the account (specific sources)
- 2 min: identify signal-hook (specific criteria)
- 2 min: connect signal to pain (mod-103 positioning + mod-104 pain shape)
- 3 min: write the ask (low-commitment; see angle library)
- 1 min: subject line + review + send

## Signal-hook ranking (updated quarterly)
- {ranked list of which signal types produce highest reply rate}

## Objections and responses
- {objection 1}: {response}
- {objection 2}: {response}
- ...

## Reply-handling SLA
- Positive replies: ≤4 business hours
- Right-person redirects: ≤1 business day
- Negative / not-a-fit: same-day acknowledgement + move to nurture

## Weekly review agenda
- Touches sent per rep
- Reply rate + positive reply rate
- Meetings booked + held
- Signal-hook performance (which categories produced this week's highest reply rate)
- Adjustments for next week (list weighting, template edits)

## Version history
- v1 — {date} — {author} — {summary of changes}
```

The cadence document is the artifact that makes the founder-to-SDR transition (mod-107 Chapter 3) producible. Without it, the SDR hire inherits nothing and re-learns the pattern-knowledge from scratch.

## Starter guidance

- **Hand-curate the list. Do not shortcut with Apollo.** Chapter 4's reply-rate math depends on the signal-hook per account. If Part A2 has 30 accounts with generic signals ("mid-market SaaS company"), the cadence will not perform. Real signals: "recently posted a Head of Platform role and open-sourced a CODEOWNERS enforcement tool"; "just raised Series B and their engineering blog referenced platform-engineering pain".
- **The 10-minute rule is a discipline.** Below 8 minutes, the personalisation is superficial and the reply rate collapses. Above 12 minutes, the founder cannot sustain the volume. When writing Part C's three cadences, time yourself — if a single email takes 25 minutes, the personalisation is over-invested and the template can be tightened. If it takes 3 minutes, the personalisation is not real.
- **The three angles must be distinct.** A common failure: touches 1, 3, and 5 are three variants of the same pitch. Recipient sees the third as the same email and reply rate does not increase with additional touches. Each angle has a different reader-anchor (pain / outcome / right-person) and a different structural frame.
- **Ask small in touch 1.** "Book a 30-minute demo" is too high-commitment for a cold contact. Ask a specific question ("would a 15-minute compare-notes call be useful, or would it help if I sent our writeup on the four failure modes?"). Escalation to demo happens after positive engagement.
- **The break-clause is not optional.** Every cadence has a professional close on touch 6. Cadences without one fatigue the account, hurt domain reputation, and produce diminishing returns past touch 6. And 10-15% of accounts that reach breakup reply positively.
- **Write the response scripts (Part D) in a form the SDR can run.** If your response requires being the founder ("we've thought about this deeply and are open to redesigning our approach..."), the SDR cannot use it. Rewrite in third-person, with concrete facts, and with a specific next step.
- **The cadence document is the artifact the SDR hire inherits.** Without it, the founder-to-SDR transition (mod-107 Chapter 3) restarts from scratch. Part E's E2 is the load-bearing output of the exercise — everything else feeds into it.
- **Reply-rate below 5% is a mod-103 or mod-104 diagnostic, not a cadence problem.** Chapter 4's Fact 2: if the founder's hand-personalised outbound is producing <5% reply rate on a signal-selected list, the failure is upstream. Do not try to fix a positioning or ICP problem inside the cadence.
- **Signal-hook ranking updates quarterly.** After 8-12 weeks of cadence execution, some signal types will produce higher reply rates than others. Update the cadence document's signal-hook ranking section quarterly (this feeds Chapter 7's quarterly review).

## Acceptance criteria

Your submission is complete when:

- [ ] Part A specifies signal-selection criteria for all four categories (A/B/C/D) with specific signals and sources per category, priorities, and weekly volume expectations.
- [ ] Part A populates a 30-account starter list with real companies, specific signal-hooks, buyer contacts, and priority tiers.
- [ ] Part B reproduces the six-touch cadence structure with day / channel / purpose / length per touch.
- [ ] Part B designs three distinct angles (pain / outcome / right-person) with reader-anchor + specific ask + signal-hook slot per angle.
- [ ] Part B includes a professional break-clause template.
- [ ] Part C writes three fully-hand-written cadences (one Category A account, one Category B account, one Category C account) with all six touches per cadence; each cadence's personalisation is real and specific.
- [ ] Part C confirms the 10-minute-per-touch discipline is met (time-budget honest check).
- [ ] Part D lists 5-10 anticipated objections with 3-5 sentence response scripts that transfer to an SDR (not founder-only responses).
- [ ] Part E names the minimum-viable instrumentation stack (list system, touch log, reply-state categories, opportunity linkage, weekly metrics) and confirms the founder is NOT buying Outreach / Apollo / Gong yet.
- [ ] Part E writes a 1-2 page cadence document in the structured format (list criteria + priority tiering + cadence structure + personalisation scaffold + signal-hook ranking + objections + reply-handling SLA + weekly review agenda + version history).
- [ ] Any factual claim (a specific competitor's cadence, a specific reply-rate benchmark) that is not cited to Chapter 4 or a practitioner reference is flagged `<!-- needs-research: ... -->`.

## Common ways this exercise goes wrong

- **Firmographic-only list trap.** Part A2's 30 accounts are all "50-500-engineer B2B SaaS in the US" without additional signals. This is a machine-generated list; the reply rate will be 1-3%. Fix: every account has a specific Category-A/B/C signal beyond the firmographic filter.
- **Made-up-accounts trap.** Part A2 uses fictional company names. The exercise's discipline is signal-hook hand-curation, which cannot be practised on fictional companies. Fix: use real companies with real observable signals; if the product is pre-launch, use companies that would be the ICP.
- **Templated-personalisation-with-tokens trap.** Part C's three cadences use `{{first_name}}, I noticed {{company_name}} is a {{industry}} company` — the personalisation is auto-filled tokens, not real signal-hook references. Fix: personalisation names something specific the account did, not something the enrichment tool auto-filled.
- **Same-angle-three-times trap.** Touches 1, 3, and 5 are three variants of the same pitch. Fix: three distinct angles (pain / outcome / right-person) with different reader-anchors and different structural frames.
- **12-touch-at-seed trap.** Founder extends the cadence to 12 touches because "that's what Predictable Revenue does". Cannot sustain the volume at Level-3 personalisation; touches 7-12 are fatigued; recipients complain. Fix: 6 touches at seed; volume comes from list quality, not touch count.
- **Ask-a-demo-in-touch-one trap.** Touch 1 opens with "would you like to book a 30-minute demo?" — too high-commitment for cold. Reply rate 0.5%. Fix: low-commitment ask in touch 1; demo ask escalates only after positive engagement.
- **No-break-clause trap.** Cadence has no defined final touch; accounts get emailed indefinitely; domain reputation degrades. Fix: professional close on touch 6.
- **Founder-only-response-scripts trap.** Part D's response scripts require the responder to be the founder ("we spent 18 months thinking about this at Loomly and..."). SDR cannot use them. Fix: rewrite for the SDR — third-person, concrete facts, specific next step.
- **Skip-the-cadence-document trap.** Founder runs Parts A-D and skips Part E's cadence document. The founder's Q1 outbound work does not transfer to the SDR hire; pattern-knowledge is lost. Fix: Part E's E2 is the load-bearing output; if it isn't written, the exercise didn't complete.
- **Tool-before-motion trap.** Founder names "Outreach + Apollo + Gong" as the instrumentation stack. Configuration overhead consumes month 1; motion isn't validated when month 2 starts. Fix: minimum-viable stack (Gmail + text-expander + spreadsheet + free HubSpot) for the first 3 months.
- **Ignore-the-reply-rate-diagnostic trap.** Founder plans to run the cadence expecting a specific reply rate but doesn't note what to do if the rate is below 5%. When it happens 6 weeks in, the founder tunes the cadence instead of checking the ICP + positioning upstream. Fix: E2 names the sub-5%-reply-rate diagnostic explicitly — go to mod-104 or mod-103 before tuning the cadence.
- **Signal-hook-ranking-not-instrumented trap.** Cadence document has no section for tracking which signal categories produce highest reply rate. After 12 weeks the founder has no data on which Category-A signals to double down on. Fix: signal-hook ranking is a section of the cadence document, updated quarterly.
