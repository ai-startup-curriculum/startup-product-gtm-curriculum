# The Founder Demo — Checklist and Anti-Demo Patterns

## Motivation

The demo is the deal's second-most-consequential meeting (after discovery). It is where the founder confirms the pain the buyer articulated in discovery, shows the product addressing that pain concretely, and either advances the deal to proposal or exits with a clear disqualification. Done well, the demo is a 30-45-minute conversation that leaves the buyer able to say to her boss: "I've seen the tool, it solves our cycle-time problem, here's the ROI, we should move on it." Done badly, the demo is a 60-minute feature tour that leaves the buyer saying "cool product, we'll think about it," and the deal enters pipeline debt.

The chasm between the two is not the product's quality. It is the founder's discipline. Founders default to demoing the product they built — every feature they're proud of, every screen they polished, every workflow they optimised — instead of demoing the *pain-addressing subset* of the product the specific buyer needs to see. The buyer, who spent 30 minutes in discovery describing one specific pain, watches the founder show her twelve features unrelated to that pain and quietly disengages. The deal loses on the demo not because the product was wrong but because the demo did not connect back to the buyer's stated pain.

The failure mode this chapter exists to catch: **the founder runs the demo without a checklist, without a pain recap, without a defined audience, without a defined narrative arc, and without a defined post-demo next step — every demo becomes a variable, un-repeatable, feature-first tour that produces one of three failure modes (demo-drift, feature-spray, over-promising) and stalls the deal.**

The remedy: a **written demo checklist** — pre-demo confirmation, opening pain recap, ROI framing, structured narrative arc, objection surfacing, next-step booking — plus a working knowledge of the four anti-demo patterns the founder is trained to catch in her own delivery. The checklist is the artifact; the anti-pattern awareness is the discipline. Both ship into the first-AE pack.

## Core concepts

### What the demo is (and is not)

The **demo** is the founder-led (later AE-led) product demonstration whose objective is to *confirm the pain sized in discovery, show the product resolving that pain concretely, surface objections, and advance the deal to proposal (or exit with disqualification)*. It is not:

- A feature tour (which is decorative and does not connect to the buyer's pain).
- A pitch (which happens embedded in the pain-recap opening).
- A training session (which happens post-close, at kickoff).
- A general "product walkthrough" (which is a marketing website's job, not a live demo's).

The demo has a specific *narrative arc*: it begins with the buyer's pain (from discovery), moves through 2-4 workflows that resolve that pain, quantifies the resolution in the buyer's own terms, surfaces objections, and closes with a next-step. Every minute of the demo has to advance the arc; minutes that do not advance the arc are minutes that lose the deal.

### The three pre-demo confirmations (the checklist's opening block)

Before the demo happens, three specific things have to be confirmed. If any is missing, the demo should be rescheduled — running a demo without them is a leading indicator of demo failure.

1. **Confirmed audience.** Who will be in the room? The demo audience should include (a) the buyer, (b) the champion, and (c) at least one representative user. Missing the buyer → the demo can be great and the deal still won't advance because the person who signs never saw it. Missing the champion → nobody at the account is left to sell it internally. Missing the user → the demo may pass buyer-approval and fail user-adoption veto later. The founder confirms the audience 48 hours before the demo and re-confirms 2 hours before.
2. **Confirmed agenda.** The founder sends a 3-4-bullet agenda 24 hours before the demo: recap of the pain (from discovery), walkthrough of the specific workflows that address it, ROI framing, next-step discussion. The agenda is not decorative — it lets the buyer flag missing pieces ("actually, our security lead should be on this") before the meeting, and it sets the frame so the founder can hold the demo to the arc without seeming to control the conversation.
3. **Confirmed pain restate.** The founder opens the demo by restating the pain as she heard it in discovery — "when we last spoke, you said cycle time drifted from 8 hours to 3 days over Q3, which delayed the November release and pushed a customer contract into Q1 for ~$180K in delayed revenue; that's what we're going to focus on today." The buyer either confirms ("yes, that's exactly it") or corrects ("actually the number is closer to $250K when we count the second customer"). Either outcome is a win — confirmation earns permission to demo against that pain; correction sharpens the ROI story before the demo runs.

The pre-demo confirmations are the demo's version of discovery's opening frame. They pay off in every remaining minute of the meeting.

### The narrative arc — pain, workflow, workflow, ROI

The demo's body — the 25-35 minutes between the pain recap and the next-step booking — follows a specific arc:

- **Pain recap (2-3 min).** The opening, from the pre-demo confirmations.
- **Workflow 1 — the "in your world today" scenario (5-8 min).** The founder walks through the workflow that resolves the specific pain the buyer articulated, using scenario details from the buyer's world where possible. If the buyer said "cycle time drifted because engineers ignore Slack pings for stale PRs," workflow 1 shows the tool detecting stale PRs, routing the notification to the right person via the right channel, and updating the manager's dashboard. Not "here's our notification engine"; here's the *specific fix* for the *specific pain*.
- **Workflow 2 — the "adjacent value" scenario (5-8 min).** A second workflow that resolves a related pain the buyer alluded to but did not center. If the buyer said "our on-call rotation gets angry when PRs stack up," workflow 2 might show the on-call handoff view or the throughput dashboard. This workflow demonstrates that the product's value extends beyond the single presenting pain.
- **Workflow 3 (optional) — the "team-level rollup" scenario (5 min).** If the audience includes a buyer who reports up to a VP or CFO, a third workflow shows the manager/executive-facing dashboard — the ROI story rendered as an artifact the buyer's boss will see. Skip this workflow if the audience is entirely user-level.
- **ROI framing (3-5 min).** The founder walks through the ROI math *out loud*, using the buyer's own impact numbers from discovery: "you said cycle time cost you $180K in delayed revenue; a 30% reduction saves ~$54K in one quarter alone, against a $12K annual ACV, which is a 4.5× payback in a quarter." The framing has to be tied to *the buyer's number*, not a generic industry benchmark.
- **Objection surfacing (5-10 min).** The founder asks — explicitly — "what would prevent your team from adopting this?" and gives the buyer permission to raise concerns without triggering a defensive sales-response. Common objections at this stage: security / compliance, migration cost, "we could build this ourselves," internal champion insufficient. Every objection surfaced on the demo is one that does not derail the proposal.
- **Next-step booking (5 min).** The founder proposes the next step — proposal in 48 hours, or a specific follow-up (a security review, an integration walkthrough with the tech lead, an economic-buyer meeting) — and books it on the call. See Chapter 5 for the full discipline.

The arc is *not* linear — the buyer will ask questions mid-workflow, and the founder should follow them into the value proposition. The arc is the return-to-baseline; the founder returns to the next arc-step after every buyer-driven side conversation.

### Talking length — the buyer talks a third of the demo

The founder should not talk 90% of the demo. That is the feature-tour pattern. A well-run demo has the buyer talking roughly 30-40% of the meeting — reacting to workflows ("yes, this is exactly what we do today, but with more Slack chaos"), asking questions, pushing back on scenarios, walking through her own screenshots or workflow if useful. The founder's tell that the demo is going well is the buyer *interrupting* to ask "does it also do X?" — interruptions mean the buyer is engaged and mapping the product to her world.

The way the founder achieves this: **stop at natural transition points and ask a question.** After workflow 1, the founder pauses: "does this map to how your team handles this today, or is there a piece I'm missing?" The pause invites the buyer's reaction, which either validates the workflow or surfaces a mismatch to fix in the next demo iteration. Founders who barrel through 40 minutes of workflows without pausing lose the buyer's engagement by minute 15.

### ROI framing — the champion's internal-sale ammunition

The ROI section is not for the buyer to admire. It is for the buyer (or the champion) to *use internally* when she has to justify the deal to her boss or the economic buyer. The founder's job is to hand the champion the ammunition, using the champion's own words and numbers.

The ROI framing has three components:

- **The pain number** — from discovery, restated in the buyer's language. "$180K in delayed revenue from cycle-time drift."
- **The resolution multiplier** — a defensible percentage improvement, ideally grounded in a case study or a comparable customer. "Customers at your scale typically see cycle time drop 20-40% within 6 weeks." The founder should have this number ready and cite the comparable customer (with permission — see mod-104's persona work on identifying reference customers).
- **The payback math** — the arithmetic that converts the resolution into dollars against the ACV. "20% cycle-time recovery on your baseline recovers ~$36K in a quarter, against a $12K annual ACV — that's a 3× payback in three months, 12× annualised." Rounded, plain, defensible.

The founder should send the ROI math to the buyer *in writing* within 24 hours of the demo, formatted as a screenshot or one-pager the champion can literally forward to the economic buyer. This is champion enablement — the artifact that makes the internal sale possible.

### The four anti-demo patterns

Founders — even experienced ones — default into four specific patterns that kill deals. Recognising and self-catching them in the moment is one of the highest-leverage demo skills.

**Anti-pattern 1: The feature tour.** Every screen, every menu, every setting. Founder is proud of the product, wants to show all of it, treats the demo like a museum tour. The buyer sees eight features unrelated to her pain and quietly checks out. The tell: the demo lasts > 45 minutes and none of the buyer's questions reference the specific pain from discovery. Fix: script only the 2-4 workflows that connect to the buyer's stated pain; cut every other screen.

**Anti-pattern 2: The demo-without-discovery.** Founder skipped discovery (Chapter 3's failure mode) and starts the demo with "let me walk you through what we do." No pain to recap, no ROI number to tie to, no personas identified. The demo is generic, the deal doesn't advance. The tell: the demo opens with a product overview instead of a pain recap. Fix: never run a demo without a preceding discovery call; if a prospect insists on a demo before discovery, the first 10 minutes of the demo *is* discovery.

**Anti-pattern 3: Feature-promising (the "yes we do that too" trap).** Buyer asks "does it also do X?" — where X is a feature the product does not have — and the founder says "yes, we have that" or "yes, it's coming in Q1." Two things happen. First, if the buyer buys, she buys against a promise that will not ship in her timeframe, and churn follows. Second, if the buyer verifies internally with a competitor demo or a peer, the vendor is caught in a small lie and the deal loses on trust. The tell: the founder is answering yes to every question. Fix: honest answers — "not yet — is that a hard requirement?" — and if the answer is yes-hard-requirement, either commit to a specific ship date in writing (which becomes contractual) or disqualify the deal on a whole-product gap.

**Anti-pattern 4: The premature-price-avoidance.** Buyer asks "what does this cost?" during the demo and the founder deflects ("let's finish the demo and I'll walk through pricing at the end"). The buyer's price question is a *buying signal*; deflecting it converts a buying signal into a defensive dynamic. Meanwhile, the founder is nervous about pricing because she has no rate card, no anchor, no packaging story. The tell: the founder feels the price question as an attack rather than a signal. Fix: answer the price question when asked — "our current pricing for teams your size is $12K/year for the core tier; here's what's included" — and continue the demo with pricing on the table. Chapter 6's proposal template + mod-106's pricing work is what makes this comfortable.

There is a subtler fifth pattern — **the champion-only demo** — where the founder runs a spectacular demo to a champion who has no authority, and the deal never advances because the buyer / economic buyer never saw the product. This is a pre-demo failure (the audience wasn't right) but manifests in the demo. Fix: enforce the pre-demo audience confirmation.

### Demo variations — recorded, live, and hybrid

Not every demo is a live 45-minute conversation. The founder-led demo motion has three variations, each with a specific use case:

- **Live demo (the default).** 30-45 minutes over Zoom / Google Meet, founder driving, audience of 2-5. The mainstay of the motion; every deal in the ICP band should get one.
- **Recorded demo (asynchronous / self-serve top-of-funnel).** 3-7 minute recorded walkthrough — often produced with Loom or a similar tool — sent as a follow-up to a cold email, embedded in a landing page, or attached to a "here's what our tool does" LinkedIn post. Used to *earn* the discovery call, not to replace it. The founder-scale motion produces one recorded demo, updates it every 2-3 months, and re-uses it heavily.
- **Hybrid demo (the "we recorded, now let's discuss" pattern).** For accounts that are further along or where the buyer wants to see the product before committing to a live meeting, the founder sends a recorded demo and books a 20-minute discussion afterwards. This shifts the founder's live time from "showing" to "discussing," which is a higher-leverage use of the founder's calendar. Useful mid-funnel.

For the ICP band this module targets (mid-market B2B SaaS), the live demo remains the anchor. Recorded and hybrid demos are complements, not replacements.

### The written demo checklist — the shipping artifact

The demo checklist is a written, held-in-hand-or-on-screen 15-25-line document the founder uses on every demo. It is not a shopping list; it is a *scaffold* the founder can hand to the first AE hire on day one.

The checklist's shape:

```
─────────────────────────────────────────────────────
DEMO CHECKLIST — {product} — v{version}
─────────────────────────────────────────────────────

PRE-DEMO (48 hours before)
  [ ] Audience confirmed: buyer + champion + user (min)
  [ ] Agenda sent: pain recap, 2-4 workflows, ROI, next-step
  [ ] Pain restate drafted from discovery notes
  [ ] Screenshots / data prepared where useful

PRE-DEMO (2 hours before)
  [ ] Audience re-confirmed via email
  [ ] Tech check: screen share, audio, no notifications
  [ ] Pain recap read aloud once for delivery
  [ ] Backup plan: static screenshots ready if live env fails

OPENING (2-3 min)
  [ ] Frame the demo — this is about your pain, not our product
  [ ] Restate the pain from discovery — confirm or correct
  [ ] State the arc — 2-4 workflows, ROI, next-step

DEMO BODY (25-35 min)
  [ ] Workflow 1: {pain-1 resolution} — pause + question after
  [ ] Workflow 2: {pain-2 or adjacent value} — pause + question
  [ ] Workflow 3 (optional): {rollup / mgr view}
  [ ] ROI framing: {pain-number} × {resolution %} vs. ACV

CLOSE (5-10 min)
  [ ] Objection surface: "what would prevent adoption?"
  [ ] Handle each objection: address / commit / disqualify
  [ ] Next step: proposal / follow-up / disqualify
  [ ] Book the next step on the call, calendar invite live

POST-DEMO (within 24 hours)
  [ ] Next-step email (Chapter 5 template)
  [ ] ROI one-pager to champion for internal use
  [ ] CRM: stage update, next step logged (Chapter 7)
  [ ] Notes: new language, surprise, objection pattern

ANTI-PATTERN CHECK (run mentally after every demo)
  [ ] Did I feature-tour?
  [ ] Did I skip discovery frame?
  [ ] Did I feature-promise?
  [ ] Did I deflect a price question?
─────────────────────────────────────────────────────
```

The checklist is one page, versioned, dated, owned. Chapter 8 develops the pack-shipping discipline; the demo checklist is one of the Tier-1 artifacts.

## Concrete example — the Loomly demo with Acme

Continuing the Acme deal from Chapter 3. Jane runs the 45-minute demo with Ramesh (VP Eng), Sasha (EM, champion), and Priya (senior engineer, user rep). Pre-demo audience + agenda + pain recap confirmed 24 hours prior.

**Opening (3 min).** Jane restates: "when we last spoke, Sasha, you described a specific case — a critical bug fix PR sat 4 days, blocked an SLA, required you to chase three engineers on Slack. Ramesh, you connected that pattern to your Q3 cycle-time drift (8 hours to 3 days) and the $180K delayed revenue from the November release slip. Today I want to show two workflows that address that specific loop, walk the ROI math against your numbers, and figure out next steps." Ramesh confirms; Priya adds a detail ("the third engineer was actually on-call — she didn't see the Slack ping because she was in an incident"). Jane logs the language ("third-engineer-was-on-call" is a nuance worth adding to the discovery script's on-call question).

**Workflow 1 — stale-PR detection + routing (7 min).** Jane demos the GitHub app detecting a stalled PR (using Loomly's own repo as demo data), routing the notification to the reviewer's preferred channel (Slack DM in Priya's case, mobile push in Sasha's), and escalating to the manager if unread past a configurable threshold. Pause + question: "does this map to how your team handles it today?" Sasha reacts: "we do this manually every morning — this would save me 30 minutes of Slack-chasing daily." Priya asks about the on-call awareness: "does it detect if the reviewer is in an incident and route around them?" — this is a real feature Loomly has (integration with PagerDuty on-call state); Jane demos it and Priya visibly relaxes.

**Workflow 2 — cycle-time dashboard for VP Eng (6 min).** Jane demos the VP-level dashboard showing cycle-time trend, PR-age distribution, and per-team breakdown. This is aimed at Ramesh; his question — "can I export this for the board deck?" — is a buying signal. Jane shows the CSV export and confirms a PDF export is on the near roadmap (honest — the feature is a two-week ship, not a hand-wave).

**Workflow 3 skipped** — the audience is already Ramesh + Sasha + Priya, and the manager-view is covered in workflow 2.

**ROI framing (4 min).** Jane works the math out loud: "your $180K delayed-revenue pain. Comparable customers (Retool at 80 eng, Vercel at 200 eng) saw cycle-time drop 20-40% within 6 weeks. Even at 20%, that's ~$36K of delayed-revenue recovery in a single quarter, against a $12K annual ACV — 3× payback in three months, 12× annualised. Higher if you index against the on-call-anger cost." Ramesh nods; the math is defensible and lands.

**Objection surface (5 min).** Jane: "what would prevent your team from adopting this?" Sasha raises two concerns — (a) getting engineers to accept another notification channel, (b) whether the tool becomes a manager-surveillance mechanism vs. a team-productivity mechanism. Jane addresses (a) with the notification-preference-per-engineer setting; addresses (b) by showing the team-view is opt-in per engineer and the default view is aggregate not individual. Both concerns partially addressed on the demo; Jane offers a 30-day trial to prove out the adoption question. Priya raises no additional concerns.

**Next-step (4 min).** Jane: "sounds like next steps are — I'll send a proposal within 48 hours based on today, priced at $12K/year with a 30-day trial clause. Ramesh, given the Q4 board deadline, I'd propose we aim to sign in the next 2-3 weeks. Between now and proposal — do we need to loop your CFO in for economic-buyer sign-off, or does the $12K fit within your discretionary budget?" Ramesh: "$25K is my discretion, $12K is fine." Deal architecture clarifies. Jane: "great — let me book a 20-minute check-in for Wednesday of next week to walk the proposal together and answer any redline questions." Booked on call.

**Post-demo (2 hours later).** Jane sends the next-step email (Chapter 5 template), the ROI one-pager (screenshot of the math with the customer comparables cited), updates the CRM (stage → Proposal, next step → check-in Wed, ACV $12K), and writes her three notes.

**Anti-pattern check** — did she feature-tour? No, two workflows, both pain-tied. Did she skip discovery frame? No, opened with pain recap. Did she feature-promise? Almost — the PDF export is a two-week ship and she said "on the near roadmap"; she should have said "shipping in two weeks" for cleaner honesty. Did she deflect a price question? No, priced it explicitly in the next-step section. Note to self on the feature-promise line — sharpen the language.

## Common failure patterns

- **The feature-tour trap.** Founder demos every feature she is proud of. Buyer's pain never gets addressed specifically. Deal doesn't advance. Fix: 2-4 workflows only, each tied to a specific discovery-surfaced pain; cut the rest.
- **The demo-without-discovery trap.** Prospect asks for a demo without a discovery call; founder complies. Demo is generic, deal stalls. Fix: never demo without discovery; if the prospect insists, first 10 minutes of the demo *is* discovery.
- **The feature-promise trap.** Founder answers "yes we do that" to every question, including features that don't exist. Trust erodes when the buyer verifies; churn follows if the buyer buys. Fix: honest answers; commit to a specific ship date only when it becomes contractual.
- **The price-deflect trap.** Founder deflects the buyer's price question ("let's cover pricing at the end"). Price question is a buying signal; deflecting shuts it down. Fix: answer the price question when asked; keep talking with pricing on the table.
- **The champion-only-audience trap.** Only the champion is on the demo; buyer and user are absent. Demo is great, deal doesn't advance because the person who signs never saw it. Fix: enforce the pre-demo audience confirmation — buyer + champion + user, or reschedule.
- **The founder-monologue trap.** Founder talks 90% of the demo. Buyer disengages by minute 15. Fix: pause + ask after every workflow; buyer should talk 30-40% of the demo.
- **The no-ROI-framing trap.** Founder shows the product but never converts the value to dollars against the buyer's discovery-sized pain. Champion has no internal-sale ammunition. Fix: explicit ROI arithmetic in the demo body, ROI one-pager to champion within 24 hours.
- **The generic-ROI-number trap.** ROI framing uses "typically customers save 3x" without tying to the buyer's specific pain number. Ungrounded ROI doesn't fund the deal. Fix: ROI math on the buyer's number, cited to comparable customers by name (with permission).
- **The no-objection-surface trap.** Founder ends the demo without asking "what would prevent adoption?" Buyer's objections stay silent, surface at proposal or (worse) at last-minute close, and derail the deal. Fix: explicit objection surface every demo; every objection is easier to handle on the demo than at proposal.
- **The no-next-step-on-call trap.** Founder ends with "I'll send some info over." Deal enters pipeline debt. Fix: propose the next step, book it on call, calendar invite live. Chapter 5 develops the full discipline.
- **The tech-fail-derailment trap.** Screen share fails, product hangs, notification pops up mid-demo. Founder loses composure. Fix: 2-hour-before tech check, backup static screenshots ready, notifications off, product state pre-warmed.
- **The no-anti-pattern-check trap.** Founder never runs the mental anti-pattern check after demos. Same patterns repeat deal to deal, un-diagnosed. Fix: 5-minute post-demo check, notes on which pattern fired, one specific improvement for the next demo.
- **The demo-as-training trap.** Founder demos as if teaching the buyer to use the product. Buyer wants to see whether it solves her pain, not how to configure it. Training is post-close, at kickoff. Fix: show workflows in resolution, not in setup.
- **The no-recorded-demo trap.** Founder does zero recorded demo assets, so every top-of-funnel touch requires a founder-live demo. Founder's calendar collapses. Fix: one 3-7-min recorded demo asset, refreshed every 2-3 months, embedded in outbound + landing pages.

## Summary

- The **demo** is the founder-led product demonstration whose objective is to *confirm the discovery-sized pain, show it addressed concretely, surface objections, and advance the deal to proposal or exit with disqualification*. It is not a feature tour, not a pitch, not a training session.
- The **three pre-demo confirmations** — audience, agenda, pain restate — are the checklist's opening block. Running a demo without them is a leading indicator of failure.
- The **narrative arc** is: pain recap (2-3 min) → workflow 1 tied to primary pain (5-8) → workflow 2 tied to adjacent pain (5-8) → optional workflow 3 (rollup view) → ROI framing (3-5) → objection surface (5-10) → next-step (5). Total 30-45 minutes.
- The founder talks < 70% of the demo. **Pause + ask after every workflow** is the mechanic that converts the demo from monologue to conversation.
- **ROI framing** ties the buyer's discovery-sized pain number × a defensible resolution multiplier × ACV — worked out loud, sent as a one-pager to the champion within 24 hours as internal-sale ammunition.
- The **four anti-demo patterns** — feature tour, demo-without-discovery, feature-promising, price-deflection — are the failure modes the founder is trained to catch in the moment. The mental anti-pattern check runs after every demo.
- **Demo variations** — live (default), recorded (top-of-funnel + async), hybrid (mid-funnel efficiency) — each have a use case. Live remains the anchor for the ICP band this module targets.
- The **written demo checklist** is the Tier-1 pack artifact (Chapter 8): one page, versioned, dated, owned. It is what makes the demo transferrable to the first AE.
- Every demo produces a **post-demo artifact set**: next-step email (Chapter 5), ROI one-pager (champion enablement), CRM stage update (Chapter 7), notes (new language, surprise, objection pattern).
- Chapter 5 picks up the discipline that closes every stage in the model — **next-step discipline** — with the demo as one of its most important applications.
