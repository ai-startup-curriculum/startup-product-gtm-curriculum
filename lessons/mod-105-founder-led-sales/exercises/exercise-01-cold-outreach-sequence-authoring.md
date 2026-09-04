# Exercise 01 — Cold Outreach Sequence Authoring

**Estimated time:** 3 hours
**Chapter link:** [`02-cold-outreach-and-top-of-funnel-by-hand.md`](../02-cold-outreach-and-top-of-funnel-by-hand.md)
**Prerequisite:** Chapter 2 read end-to-end; mod-104 ICP scorecard (Exercise 01 of mod-104) or an equivalent working ICP + persona; a real (or realistic) list of 15-25 named accounts to sequence against.

## Problem statement

Chapter 2 named the failure modes: sending 200 identical emails from an unwarmed domain and concluding "outbound doesn't work," or hiring an SDR in month 2 to run an un-characterised script and burning the SDR's ramp. The remedy is a small, disciplined, hand-personalised sequence — 15-30 accounts per week, 4-6 touches per account, tracked on a two-metric scoreboard — that the founder runs herself long enough to validate before delegating.

This exercise trains you to **author a complete, ready-to-run outbound sequence pack** — subject-line + opening-line library, per-touch templates with personalisation slots, a channel-mix rule per account, a two-metric measurement instrument, and a deliverability checklist — sized to be run against a real 15-25 account list next week. The output is not a marketing artifact; it is the specific working document a founder or first SDR will send from.

The failure mode this exercise exists to catch: **the founder authors a single beautiful email, admires it, never actually sequences it, and ships a "pack" that is one email plus a footer.** A pack is a sequence + measurement instrument + deliverability posture; anything less is a template.

## Requirements

Deliver a folder `exercise-01/` with:

- `part-a-account-list.md` — the 15-25 named accounts to sequence against, with the per-account research notes.
- `part-b-sequence-pack.md` — the 4-6 touch sequence, subject-line library, opening-line library, channel-mix rules.
- `part-c-scoreboard-and-deliverability.md` — the two-metric scoreboard shape, the weekly review cadence, the deliverability checklist.

### Part A — Assemble the 15-25 named account list (45 min)

Deliver `part-a-account-list.md`. Pick 15-25 named accounts against the mod-104 ICP. For each account, capture the pre-outreach research packet:

- **Account ID.** `A01` … `A25`.
- **Company snapshot.** Employee count, revenue / ARR band if known, industry, funding stage, geography, primary technology-graph fingerprint (from Layer 1 of mod-104).
- **Named contact.** Specific human name, title, LinkedIn URL. Persona (buyer / user / champion) with confidence.
- **Personalisation hook.** One specific, verifiable, non-obvious observation about the account — a recent product ship, an engineering blog post, a strategic statement from a public talk, a specific hire, a specific integration in their stack. This is the raw material for the opening line of Touch 1.
- **Warm-intro path (if any).** Named mutual connection (LinkedIn second-degree), the mutual's role at the account or vs. the founder, the founder's degree-of-comfort asking the mutual for an intro.
- **Priority tier.** `P1` (obvious high-fit + hot triggering event), `P2` (high-fit, cool timing), `P3` (research validation account — worth sequencing to learn even if fit is uncertain).

**Deliberately span the priority distribution.** At least 3 `P1`, at least 5 `P2`, at least 2 `P3`. All-P1 lists produce fake reply-rate numbers because the top-of-funnel selection carried the deal, not the sequence.

Any account you cannot fully research should be flagged with `<!-- needs-research: ... -->` — do not fabricate a personalisation hook. A fabricated hook fires as spam in the buyer's inbox and burns the domain reputation.

### Part B — Author the sequence pack (105 min)

Deliver `part-b-sequence-pack.md` with the following components.

**B1 — Subject-line library (15 min).** 8-12 subject lines that follow Chapter 2's rules: short (3-6 words), specific, non-marketing-looking, lowercase, no emojis, no "quick question." Each subject line is paired with the *type of personalisation* it draws on (recent-ship, blog-post, funding-round, hiring-signal, technology-graph). Draw from your account list — every subject line should be usable against at least one account in Part A.

**B2 — Opening-line library (20 min).** 10-15 opening lines. Chapter 2's rule: never a compliment; always a specific observation only applicable to this account. Each opening line is paired with the *account it was authored against* — real personalisation, not templated fill-in-the-blanks.

**B3 — The 4-6 touch sequence template (60 min).** Author each touch as a working template with clearly-marked personalisation slots (`{opener}`, `{value_hypothesis}`, `{ask}`) and the templated middle. Follow Chapter 2's canonical arc:

- **Touch 1 (day 0)** — 3-5 sentences: hand-personalised opener, one value hypothesis (named pain → named consequence → named outcome → named specificity), one soft ask.
- **Touch 2 (day 3-4)** — same thread, different angle. Include what "different angle" means in your context.
- **Touch 3 (day 7-8)** — cross-channel touch (LinkedIn connection request or InMail, or a warm-intro nudge). Include the LinkedIn message template *and* the forwardable-email template for the warm-intro path.
- **Touch 4 (day 12-14)** — third angle: case study snippet, market shift, or content-driven hook.
- **Touch 5 (day 18-20)** — the break-up: "assuming this isn't a priority right now — mind if I close the loop?" Author the exact wording; the break-up is where the highest reply rate often sits.
- **Touch 6 (optional, day 30+)** — reactivation trigger with a specific new hook. Author the condition that would trigger this touch (new feature ship, new case study, market event).

For each touch, name **which of the two failure modes** it is optimising against — opener quality (reply rate) or hypothesis quality (positive-reply rate).

**B4 — The channel-mix rule (10 min).** Given your ICP: for which accounts is cold email primary, when does LinkedIn become primary, when is a warm-intro path required (not optional)? Name the specific decision rule you will apply per account.

### Part C — Scoreboard and deliverability (30 min)

Deliver `part-c-scoreboard-and-deliverability.md`.

**C1 — The two-metric scoreboard (15 min).** Author the specific spreadsheet or CRM view that tracks per-week:

| Metric | Definition | Target (founder-scale) | Diagnoses what if low? |
|---|---|---|---|
| Reply rate | Any reply / touch-1 sent | 15-25% cumulative over full sequence | Opener quality / subject line / sender reputation |
| Positive-reply rate | "Wants to talk" / touch-1 sent | 3-8% cumulative | Value hypothesis quality / ICP fit |
| Meetings booked | Accounts that book a first meeting / touch-1 sent | 3-7% cumulative | Ask quality / calendaring friction |

Extend the table with your own targets. Include the specific weekly review question you will ask against each row.

**C2 — The deliverability checklist (15 min).** Working through Chapter 2's deliverability discipline, author the specific steps you will take *before* the first Touch 1 goes out:

- Sending domain choice (primary vs. secondary).
- Domain warm-up plan (service used, ramp schedule, weeks required).
- SPF / DKIM / DMARC configuration verification (specific DNS records, or a note that you will use a checker tool).
- Reply-tracking vs. open-tracking decision.
- Send-volume ramp for weeks 1-4.

Any step you cannot personally validate should be flagged with `<!-- needs-research: ... -->` (e.g., current best warm-up service if unfamiliar).

## Starter guidance

- **The value hypothesis is the hardest part.** Founders reach for feature descriptions ("we do X, Y, Z") when the working shape is named pain → named consequence → named outcome → named specificity. Write out your value hypothesis first, in your own voice, then test it on a friend outside the domain — if she cannot restate the ask in her own words after one read, sharpen it.
- **Personalisation lives in 2-4 sentences.** Volume ceiling is 15-30 hand-personalised touch-1's per week. If your Part B has 40 accounts scheduled for touch-1 next week, either drop accounts or accept that personalisation will collapse and reply rate with it.
- **Break-up email is not optional.** The 5-15% of buyers who respond only to the break-up are why the sequence math works. Author it deliberately; do not soften it into another polite follow-up.
- **The warm-intro path is often the highest-ROI channel and the most underused.** For at least 3 of your accounts, author the specific forwardable email you would send the mutual. Do not skip this because it feels awkward — the discomfort is the whole point.
- **Deliverability plumbing is not optional.** A sequence that lands in spam has a 0% reply rate regardless of how good the copy is. If you have not warmed the sending domain and configured SPF/DKIM/DMARC before Part C, your Part B is a fictional exercise.
- **Do not write more than 6 touches.** Beyond 6 the incremental reply rate falls off a cliff and the sender reputation risk rises. The 4-6 touch discipline is Chapter 2's stated ceiling.
- **Track reply rate AND positive-reply rate.** The two-metric scoreboard is what distinguishes an opener problem from a hypothesis problem. Founders who track only reply rate iterate randomly.
- **Match channel to ICP, not to founder comfort.** If your ICP reads Twitter and does not read LinkedIn, do not sequence on LinkedIn just because you have a nicely-set-up profile there. The channel-mix rule (B4) forces the ICP-first choice.
- **The break-up is a decision-forcing mechanic, not a threat.** Author it with a "close the loop" tone, not a "let me know or else" tone. Buyers respond to graceful decision-forcing; they ignore aggressive one.

## Acceptance criteria

Your submission is complete when:

- [ ] Part A contains 15-25 named accounts, each with the six research fields, sources traceable, priority tier assigned, and at least 3 P1 / 5 P2 / 2 P3.
- [ ] No account carries a fabricated personalisation hook; any un-researched hook is flagged `needs-research`.
- [ ] Part B — subject-line library has 8-12 lines, each obeying Chapter 2's rules (short, specific, non-marketing-looking) and paired with a personalisation type.
- [ ] Part B — opening-line library has 10-15 openers, each authored against a real account in Part A, none of them a compliment.
- [ ] Part B — the 4-6 touch sequence is fully drafted with clearly-marked personalisation slots and templated middles.
- [ ] Every touch names which failure mode it optimises against (opener quality or hypothesis quality).
- [ ] Touch 3 includes both the LinkedIn touch template *and* the forwardable-email template for the warm-intro path.
- [ ] Touch 5 (break-up) is drafted with the specific wording, not paraphrased.
- [ ] Part B — the channel-mix rule names a specific decision rule that maps account attributes → channel primary / secondary / warm-intro-required.
- [ ] Part C — the two-metric scoreboard shape is written, with targets per metric and a diagnosis question per row.
- [ ] Part C — the deliverability checklist covers sending domain, warm-up plan, SPF/DKIM/DMARC, tracking decision, and send-volume ramp.
- [ ] At least 3 accounts in Part A have a full forwardable-email drafted for the warm-intro path.
- [ ] Any technical detail you cannot personally validate is flagged `needs-research` rather than fabricated.

## Common ways this exercise goes wrong

- **The template-with-no-personalisation-slot trap.** The touch template uses `{firstName}` and `{company}` and nothing more. Buyers detect fake personalisation immediately. Fix: 2-4 sentences of hand-authored opener, plus the templated value hypothesis and ask.
- **The single-email-not-sequence trap.** Part B has one great Touch 1 and vague sketches of Touches 2-5. The sequence math never works. Fix: every touch fully drafted with the same rigor as Touch 1.
- **The product-pitch-in-touch-1 trap.** The email describes the product's features. Fix: value hypothesis (named pain, consequence, outcome, specificity), not product pitch.
- **The no-break-up trap.** Sequence ends politely at Touch 4 or ships with a placeholder break-up. Fix: explicit break-up copy in Touch 5, decision-forcing tone.
- **The over-cited-social-proof trap.** "Trusted by leading companies including X, Y, Z" where X, Y, Z are not real customers. Buyers verify. Fix: cite only real, verifiable, relevant customers with permission; if you have none, omit the social proof.
- **The one-channel-only trap.** All accounts on cold email; no LinkedIn touches; no warm-intro paths. Fix: at least 3 warm-intro-drafted accounts and a channel-mix rule that maps account attributes to channel choice.
- **The no-deliverability-plan trap.** Part C is skipped or written as "I'll set up SPF later." Sequence goes to spam. Fix: deliverability checklist completed before any Touch 1 sends.
- **The single-metric scoreboard trap.** Only reply rate is tracked; positive-reply rate is not. Diagnostic power collapses. Fix: two-metric scoreboard mandatory.
- **The over-large account list trap.** 60 accounts scheduled for Touch 1 next week; personalisation collapses. Fix: 15-30 hand-personalised accounts, no more.
- **The all-P1 list trap.** Every account is a P1. Reply-rate numbers are inflated by the selection, not the sequence. Fix: enforced P1/P2/P3 mix.
- **The no-warm-intros trap.** Zero accounts have a forwardable-email drafted. Highest-ROI channel is left on the table. Fix: at least 3 accounts with the forwardable-email fully written.
- **The fabricated-personalisation trap.** An account's opener references a "recent product ship" that did not happen. Buyer notices. Fix: only real, verifiable observations; flag `needs-research` when uncertain.
- **The sequence-without-scoreboard trap.** Part B is beautiful; Part C is skipped. No iteration happens. Fix: scoreboard is what makes the pack learnable.
