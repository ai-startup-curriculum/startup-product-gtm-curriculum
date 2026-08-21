# Shipping the ICP Scorecard — and Diagnosing ICP Drift

## Motivation

Chapters 1-6 developed the components: the operating bar, the two-layer scoreable criteria, the disqualification checklist, the buyer / user / champion personas, the three-axis lead-scoring routing, the beachhead-narrowed commitment. This final chapter does two things. First, it specifies the *shipping artifact* — the one-page ICP scorecard that carries all the components together in a form a first AE hire can put on their desk and use as a working instrument. Second, it names *ICP drift* — the founder-led-sales pattern of quietly taking any customer that will pay — and specifies both the detection signals and the operating discipline for when to enforce the ICP versus when to revisit it.

The failure mode this chapter exists to catch: **the founder writes a beautiful multi-page ICP document, saves it to Notion, and no one — including the AE — ever opens it again. Six months later, the customer list looks nothing like the ICP, and no one noticed because there was no monitoring instrument, no enforcement cadence, and no explicit "the ICP has drifted; do we enforce or revisit" trigger.**

The remedy is the one-page ship artifact with a defined operating cadence and a defined drift-diagnosis discipline. The ICP is not a strategy document; it is a working instrument that governs the operating loop.

## Core concepts

### The one-page ICP scorecard — the shipping shape

The ICP artifact ships as a **single page**, physically or in a Notion-shaped document that fits on one screen without scrolling. The rationale is not aesthetic; it is operational: an AE on a discovery call needs the whole artifact in view without switching tabs. A three-page ICP is a three-page ICP that no one uses in real time.

The one-page layout, in the order the AE encounters it during a call:

```
─────────────────────────────────────────────────────────────────
ICP — {product name} — {version} — {date} — {owner}
Version history: {last change date} {by whom} {what changed}
─────────────────────────────────────────────────────────────────

BEACHHEAD SEGMENT (the yes)
  {one-sentence segment name}

DISQUALIFIERS (must-haves — any single fail closes the deal lost)
  D1: {criterion} | ask: "{question}" | reason code: {code}
  D2: {criterion} | ask: "{question}" | reason code: {code}
  D3: {criterion} | ask: "{question}" | reason code: {code}
  D4: {criterion} | ask: "{question}" | reason code: {code}

LAYER 1 — FIRMOGRAPHIC (score at list-build, verify on call)
  F1: {criterion} | weight {W} | source: {data-source}
  F2: {criterion} | weight {W} | source: {data-source}
  ...

LAYER 2 — BEHAVIOURAL (score during discovery)
  B1: {criterion} | weight {W} | ask: "{question}"
  B2: {criterion} | weight {W} | ask: "{question}"
  ...

PERSONAS
  Buyer: {titles} | budget-authority | ask: "{identify question}" | value story | objections
  Champion: {titles} | motivation | ask: "{identify question}" | value story | objections
  User: {titles} | usage pattern | ask: "{identify question}" | value story | objections

THREE-AXIS ROUTING
  Priority 1: ICP strong + ACV strong + Timing hot → work now, weekly
  Priority 2: any of two strong → work now, monthly
  Nurture: strong ICP + strong ACV + cold timing → marketing nurture, quarterly touch
  Downgrade/Refer: strong ICP + weak ACV → refer or downsell
  Close-lost: any disqualifier fail → clean close, reason code

NOT-NOW SEGMENTS (the three explicit nos)
  NN1: {segment} | why not: {reason} | unlock: {condition} | meanwhile: {action}
  NN2: {segment} | why not: {reason} | unlock: {condition} | meanwhile: {action}
  NN3: {segment} | why not: {reason} | unlock: {condition} | meanwhile: {action}

OPERATING CADENCE
  AE weekly: pipeline review by verdict, close-lost reason-code roll-up
  Founder monthly: score drift on last 20 closed deals
  Founder quarterly: not-now list review (unlocks tripped? beachhead won? segments shifted?)
─────────────────────────────────────────────────────────────────
```

Every section is a compressed form of one of Chapters 2-6. Nothing is decorative. If a field would not be read on a live discovery call or in a weekly pipeline review, it does not belong on the one-pager.

### The metadata line — version, date, owner

The top-line metadata (version, date, owner, version history) is not administrative overhead. It is a governance instrument.

- **Version** — the ICP is expected to change. v1.0 at SEED month 3; v1.1 when the first ten sales cycles surface a should-have that was missed; v2.0 when the beachhead is won and the second bowling pin opens. Version numbers make the change history legible.
- **Date** — the ICP is a snapshot. An artifact with no date invites the assumption it is current; a dated artifact invites the question "is this still current?"
- **Owner** — one named person owns the artifact. Not "GTM team"; the CEO, the founding sales lead, or the head of GTM by name. Ownership is what triggers the cadence reviews and the version bumps.
- **Version history** — one-line description of what changed and why, per version. This is what makes the artifact institutionally learnable — the next founder / operator can read the version history and understand not just where the ICP landed but why.

The metadata is also what distinguishes an ICP from a wiki page. Wiki pages don't have versioned change history. Working instruments do.

### The three integration points — CRM, marketing automation, weekly review

The one-page artifact ships to three destinations, each with a specific integration:

1. **CRM (Salesforce, HubSpot, Attio, whichever).** The ICP scorecard drives specific CRM fields — a scored ICP-fit percentage, a stored ACV-fit and timing-fit rating, close-lost reason codes tied to the disqualifier list, a routing verdict field. The AE fills these in per deal; the founder / sales lead uses them for weekly pipeline review. mod-105 (founder-led sales) and mod-110 (GTM metrics) both develop the CRM discipline further.
2. **Marketing automation / demand-gen tooling.** Layer 1 firmographic criteria feed into Sales Navigator list-builds, Apollo / ZoomInfo filters, intent-data segmentation, paid-media targeting. The demand-gen owner uses the ICP directly. mod-108 develops this integration.
3. **Weekly pipeline review artifact.** The AE + founder weekly review is structured around the ICP: each open deal is discussed with its ICP-fit / ACV-fit / timing-fit scores and its routing verdict. Deals that drifted in ICP-fit rating are surfaced explicitly. The review is the operating instrument that catches drift before it becomes a pattern.

Without at least the first two integrations, the ICP is a document. With them, it is an operating system.

### ICP drift — the founder-led-sales pattern

**ICP drift** is the specific pattern where the founder-led-sales team, chasing revenue and responding to opportunistic inbound, gradually accepts customers outside the original ICP — until the customer base looks nothing like the artifact and no one noticed the change happen.

The pattern is *not* the same as "the ICP was wrong and we learned better" (which is legitimate and produces an ICP version bump). Drift is the *un-diagnosed*, *un-decided* version where nobody explicitly chose to serve the new customers and no one explicitly re-authored the ICP. It just happened.

The drift dynamics are:

- **Founder-led sales at SEED is opportunistic.** The founder is closing every deal they can, because revenue matters and pipeline is thin. Some deals close from outside the ICP; the founder rationalises each one individually.
- **The AE inherits the pattern.** The first AE hire watches the founder close out-of-ICP deals and concludes that the ICP is aspirational, not binding. The AE applies the same opportunistic pattern.
- **The out-of-ICP customers are demanding.** Because they were not well-fit at the sale, they are hard to serve — support tickets, custom feature requests, escalations. Founder-hours pour into these accounts.
- **The out-of-ICP customers churn.** Six to twelve months later, the misfit accounts churn. GRR drops. NRR is unrecoverable without expansion the misfit accounts cannot provide.
- **The pattern is visible only in aggregate.** No single deal looked wrong at the time; the cumulative pattern is where the ICP has silently moved.

By the time drift is diagnosed post-hoc — usually at a board meeting where someone asks "which segment are we winning in" and the founder cannot give a clean answer — the correction takes 12-18 months. Prevention is dramatically cheaper.

### The drift-detection signals

Drift is detected before it is catastrophic by monitoring specific signals on a monthly cadence. The five drift signals a founder / sales-lead should track:

1. **The mix of closed-won deals against the beachhead segment.** Run monthly: what percentage of last 30 days' closed-won revenue was inside the beachhead segment? A healthy SEED-stage motion is 80%+ beachhead concentration. Dropping below 70% is a drift signal; below 50% is a crisis.
2. **The distribution of ICP-fit scores at close.** Historical baseline: the founder's / AE's ICP-fit-score distribution on closed-won deals over the last quarter. When the distribution starts shifting toward lower ICP-fit scores at close (deals that would have close-lost at 45% under the old scorecard now closing at 45%), the discipline has slipped.
3. **The rate of "close-lost with reason code" as a fraction of pipeline.** A healthy AE / motion produces close-lost reason codes on ~30-50% of pipeline (disqualified against Chapter 3's checklist). A drop to < 15% is a strong signal the AE has stopped enforcing the checklist — every deal is being kept alive.
4. **Discovery-call time to disqualifier check.** How long into the first call is the AE actually running the disqualifier questions? A well-functioning motion has the disqualifiers within the first 10-15 minutes; a drifted motion has them deferred to the second or third call, or not at all.
5. **Founder-hours spent on customer escalations.** Rising escalation load per customer is a lagging signal that out-of-ICP customers are consuming the founder-team. When the escalation load per account is rising month over month, the underlying cause is often ICP drift — misfits demand disproportionate support.

These five signals are the monthly instrument. Chapter 7's operating cadence puts them on the founder's monthly review; a drift signal firing on two or more of the five triggers the drift-response protocol.

### The drift-response protocol — enforce or revisit?

When drift is detected, the founder faces a specific decision: **enforce the current ICP (say no to the drifted deals, tighten AE discipline), or revisit the ICP (accept that the artifact has been overtaken by learning and re-author)?**

Both are legitimate responses. Choosing wrongly produces a specific failure mode: enforcing an ICP that is genuinely obsolete strangles the deals that are actually the new fit; revisiting an ICP prematurely rewards drift and dissolves the beachhead commitment.

The decision framework — a short set of questions:

- **Are the out-of-ICP customers retaining and expanding as well as the in-ICP customers?** If yes, the ICP may have been drawn too narrow, and the drift is signal. If no (out-of-ICP has higher churn / lower NPS / lower expansion), the drift is noise and enforcement is correct.
- **Are the out-of-ICP customers concentrated in one adjacent segment?** If yes, the natural read is "the second bowling pin is opening earlier than expected"; the segment might be newly-in-scope, and the ICP evolves to acknowledge it (revisit). If no (out-of-ICP is scattered across many one-off segments), the drift is opportunistic and enforcement is correct.
- **Has the whole-product surface changed?** If a Chapter 3 disqualifier's unlock condition tripped (SSO shipped, enterprise motion staffed), a segment that used to disqualify may legitimately now qualify. That is a revisit. Without a corresponding product change, drift usually is not signal.
- **Is the AE enforcing the disqualifier checklist?** If close-lost reason codes have dropped below the healthy rate, the drift is an enforcement problem, not an ICP problem. The response is to re-authorise the AE to close-lost and re-emphasise the operating discipline, not to rewrite the ICP.

The bias is toward **enforcement first, revisit second**. Revisiting the ICP is a real strategic act — it should be triggered by real evidence, not by AE fatigue or founder anxiety. Rewriting the ICP because the AE is uncomfortable saying no is the fastest way to break the beachhead.

### The version-bump protocol — how the ICP legitimately changes

When the decision is "revisit," the ICP goes through a version bump. The discipline that keeps this from being ad-hoc:

- **Named trigger.** Every version bump has a stated trigger. "v1.1 because we shipped SSO"; "v1.2 because the mod-102 PMF cohort re-analysis surfaced two new behavioural criteria"; "v2.0 because we've won the beachhead and the second bowling pin is opening." The trigger is what makes the bump defensible.
- **Named change.** What specifically changed — added / removed / modified criteria; added / retired disqualifiers; personas re-scoped; not-now segments re-classified. Line-level clarity.
- **Named authors and reviewers.** Owner writes it; founder / CEO reviews and approves; sales lead confirms operational applicability; demand-gen confirms filterability; product confirms roadmap alignment.
- **Rollout communication.** The version bump lands with a specific communication to sales and marketing: what changed, when it takes effect (usually immediately for outbound list-builds; end-of-current-cycle for open deals), how in-flight deals under the old version are handled.
- **Instrument update.** CRM fields updated, Sales Navigator filters re-run, marketing automation re-segmented, weekly review template refreshed.

An ICP that changes without this discipline is drifting; an ICP that follows this discipline is legitimately evolving.

### When the ICP is right and the pipeline is still empty

A separate diagnostic case: the ICP is well-authored, the AE is enforcing, and the pipeline is empty. The three-axis routing produces almost no Priority 1 or Priority 2 deals. The AE is close-lost-ing every incoming lead.

This is not ICP drift; it is the *opposite* — the ICP may be too narrow, or the demand-gen motion may not be sourcing the right leads. The diagnosis routes to mod-108 (channels) or to the beachhead-review question ("was the beachhead too narrow?" — mod-103 Chapter 5).

The distinction matters. Drift and pipeline-emptiness look superficially similar (both produce founder anxiety about the ICP), but the response is opposite: drift wants enforcement + discipline; empty pipeline wants demand-gen investment + beachhead re-review. Chapter 7's monthly review distinguishes the two by looking at both the ICP-fit-score distribution *and* the volume of leads scored — low volume with high scores is a demand-gen problem; high volume with low scores is a targeting problem; low volume with low scores is possibly a beachhead problem.

### The ICP as a hiring / onboarding instrument

A well-shipped ICP is one of the highest-leverage onboarding artifacts for the first sales hire. The first two weeks of an AE's ramp include:

- Read the ICP one-pager end-to-end.
- Read the mod-101 discovery report the ICP was compressed from.
- Read the mod-103 positioning document and the beachhead choice.
- Sit in on five founder-led discovery calls, scoring the ICP in parallel on each; compare with founder's score.
- Run five discovery calls independently, scoring the ICP; review with founder weekly for the first month.

This ramp is dramatically faster with a shippable one-page ICP than without one. The AE ramp-to-productivity target (mod-110) is often 90 days; a shippable ICP compresses it toward 60. Without the ICP, ramp stretches to 180 days because the AE is reconstructing the founder's tacit qualification model from scratch, deal by deal.

Chapter 7's artifact discipline is therefore not just a documentation exercise; it is a hiring cost.

## Concrete example — Loomly's shipped ICP + drift diagnosis

### The one-pager (compressed for space; the exercise develops the full page)

```
ICP — Loomly — v1.0 — 2026-03-15 — Owner: Jane Chen (founder / CEO)
Version history: v1.0 initial ship; based on 27 discovery interviews, 12 closed customers, mod-102 PMF cohort of 8.

BEACHHEAD: Mid-market (50-150 eng) B2B SaaS devtools / observability / security-tooling companies using GitHub, distributed, with an engineering leader owning cycle-time or throughput KPI.

DISQUALIFIERS
  D1: Not using GitHub as primary code host | ask: "what's your primary code host?" | reason: "unsupported code host"
  D2: No metric owner for eng throughput / cycle time | ask: "does anyone in eng leadership have a throughput or cycle-time KPI they report up?" | reason: "no metric owner"
  D3: Procurement > 60 days at ACV $12k | ask: "for tools $10-25k/yr, how does purchase work?" | reason: "procurement-gated"
  D4: > 500 engineers (outside beachhead) | ask: "how many engineers overall?" | reason: "outside beachhead — enterprise waitlist"

LAYER 1 (firmographic)
  F1: 50-150 eng / 100-400 total | must-have | LinkedIn+ZoomInfo
  F2: B2B SaaS devtools/observability/security | must-have | LinkedIn industry+manual
  F3: GitHub Cloud or Enterprise Cloud primary | must-have | BuiltWith / engineering blog
  F4: Distributed/hybrid (≥40% remote) | weight 3 | LinkedIn / company handbook
  F5: Series A-C or bootstrapped ≥$5M ARR | weight 2 | Crunchbase / PitchBook
  F6: US/Canada/UK/EU geography | weight 1 | LinkedIn HQ

LAYER 2 (behavioural — surface in discovery)
  B1: Metric ownership for throughput/cycle time | must-have (also D2) | ask above
  B2: Existing PR-review workflow (Slack pings, weekly review, manager who chases) | weight 3 | "how does your team handle stalled PRs today?"
  B3: Deploys ≥ 1×/week | weight 2 | "how often do you deploy to production?"
  B4: Eng-tool budget owned by VP Eng/CTO at this ACV | weight 2 | ACV-fit question
  B5: Adopted new eng-productivity tool in past 12 mo | weight 1 | "what dev-productivity tools have you rolled out this year?"

PERSONAS
  Buyer: VP Engineering, sometimes CTO (< 100 eng) | budget authority ≤ $50k | ask: "who owns the budget for eng-productivity tools?" | ROI+throughput story | objections: "we can build this ourselves"
  Champion: Engineering Manager / Team Lead | motivation: team's cycle-time in perf review | ask: "on your team, who's accountable for keeping cycle time low?" | team-outcome+credit story | objections: "risk of championing something that fails"
  User: Senior/Staff Engineer | passive receiver of nudges | ask: "who currently notices stalled PRs?" | fewer-Slack-pings story | objections: "one more notification"

THREE-AXIS ROUTING: standard (see Chapter 5)

NOT-NOW
  NN1: Enterprise (>500 eng) B2B SaaS | why not: whole-product gap (SSO/SCIM/audit/on-prem), wrong motion | unlock: SSO+SCIM+audit shipped, first enterprise AE hired | meanwhile: waitlist
  NN2: Fintech / healthtech / martech (non-devtools verticals) | why not: reference pattern from devtools doesn't carry; demand-gen channels differ | unlock: 5-10 devtools reference customers + case studies published | meanwhile: nurture only
  NN3: Individual OSS / bootstrapped teams (<10 eng) | why not: ACV too low for sales cycle; wrong buyer psychology | unlock: PLG self-serve tier productised | meanwhile: waitlist for self-serve

OPERATING CADENCE
  AE weekly: pipeline review by verdict, close-lost reason-code roll-up
  Founder monthly: drift signals (mix in beachhead, ICP-fit-score distribution, close-lost rate, discovery-question timing, escalation load)
  Founder quarterly: not-now list unlock review
```

### The drift diagnosis at month 6

Six months after v1.0 ships, Loomly's founder runs the monthly drift check and sees:

- **Mix in beachhead**: closed-won in last 30 days is 60% beachhead (down from 85% at month 3). **Drift signal.**
- **ICP-fit-score distribution**: last 20 closed-won had a median ICP-fit of 62% (down from 78% at month 3). **Drift signal.**
- **Close-lost reason-code rate**: 18% of pipeline (down from 40%). **Drift signal.**
- **Discovery timing**: AE has been running disqualifier check at minute 22 rather than minute 12. **Drift signal.**
- **Escalation load per account**: rising month over month; four of the last six new customers have had 2+ founder-CEO escalations in first 60 days. **Drift signal.**

Five of five signals firing. This is drift, not learning.

The response — enforcement, not revisit:

1. Reset with the AE: reinforce the disqualifier authorisation, re-run the discovery-call sequencing training, work the pipeline review with the ICP scorecard open on-screen.
2. Close-lose 12 of the current pipeline's 40 open deals that fail Chapter 3 disqualifiers on second-look re-scoring.
3. Refuse new out-of-ICP deals for 90 days, with a specific "we don't currently serve X" script and a partner referral where possible.
4. Reset the escalation-load meter; expect it to drop 30 days after the out-of-ICP customers churn or are handed to CSM.

If, after 90 days of enforcement, the pipeline is empty *and* the ICP-fit-score distribution is healthy on the small volume that closed, the diagnosis then routes to demand-gen (pipeline volume) or beachhead review (was the beachhead too narrow). That is a different response and a different decision.

### The revisit case (a counter-example)

Contrast the drift case with a legitimate revisit. Suppose at month 9, SSO ships, and Loomly closes three of the previously-waitlisted enterprise leads over 60 days. The three enterprise customers have higher ACV than the mid-market average, healthy adoption, and no elevated escalation load. Two of the three came from referrals from mid-market beachhead customers who moved to larger companies.

This is **not drift**. This is the unlock condition for the enterprise not-now segment tripping and the second bowling pin opening on schedule. The response is a **v2.0 ICP** that formally adds the enterprise segment as an in-scope tier, adds enterprise-specific criteria (SSO enforcement, procurement-friendly clauses, on-prem deployment), and adjusts the personas + routing accordingly. The mid-market beachhead stays as the primary tier; enterprise becomes a second tier with its own scorecard slice.

The two cases look superficially similar (customer base has shifted from ICP v1.0) but the diagnoses and responses are opposite: drift → enforce; unlock-triggered evolution → revisit.

## Common failure patterns

- **Multi-page ICP document nobody uses.** The artifact is comprehensive and unusable. One page, in view during calls; everything else is supporting material in the linked mod-101 / mod-102 / mod-103 documents.
- **No version, no date, no owner.** The ICP is undated, unowned, unversioned. When drift happens six months later, no one knows what the ICP was at the last consensus and no one knows whose job it is to fix. Add the metadata line.
- **No CRM integration.** The ICP exists in Notion, deals live in Salesforce, the AE fills in nothing. Weekly pipeline review is on gut feel. Fix: CRM fields for ICP-fit score, ACV-fit rating, timing-fit rating, disqualifier hits, routing verdict, close-lost reason code.
- **No monthly drift monitoring.** Drift is only discovered at board meetings when someone asks "which segment are we winning?" Set the monthly cadence and the five signals; drift is caught at month 3 instead of month 9.
- **Drift-as-learning-fallacy.** "We're learning; the ICP is evolving." Sometimes true; often a rationalisation for un-decided drift. Apply the four-question decision framework before revising the ICP.
- **Revisiting the ICP without triggering event.** ICP is rewritten because the AE feels the current version is too restrictive. Without a named trigger (product change, PMF-cohort re-analysis, beachhead-won), the revision rewards drift.
- **Enforcing an ICP that has genuinely been overtaken.** The whole-product surface shipped, the second bowling pin opened, but the ICP still reads v1.0 and the AE is close-losing legitimately-in-scope leads. Revisit protocol needed.
- **Version-bump without CRM/marketing/roadmap integration update.** The document changes; the operating instruments (CRM fields, Sales Navigator filters, roadmap) do not. The AE reads the new version but the tools still enforce the old. Update the instruments as part of the version bump.
- **Weekly pipeline review that doesn't reference the ICP.** The AE and founder talk deals without opening the ICP; the ICP is not the framing of the review. Every deal in review is discussed with its ICP-fit / ACV-fit / timing-fit / routing verdict named.
- **Silent AE improvisation on disqualifier exceptions.** The AE gives themselves "one-off" exceptions to close-lose on disqualifier hits, without recording the exception. The exception becomes a pattern. Fix: any deviation from the disqualifier's stated action is logged and rolled up at the monthly review.
- **No hiring / onboarding integration.** The first AE hire is not given the ICP on day one; the ramp stretches to 180 days as the AE reconstructs the qualification model from scratch. Ramp cost is the highest-leverage argument for shipping a good ICP.
- **Marketing team uses a different ICP.** Sales and marketing operate on different ICPs because the artifact ships to only one. One ICP, three integration points (CRM, marketing automation, weekly review) — everyone runs off the same version.

## Summary

- The ICP ships as a **one-page scorecard** carrying: beachhead segment, disqualifiers, Layer 1 firmographic + Layer 2 behavioural criteria, buyer / user / champion personas, three-axis routing, not-now segments, operating cadence. On one screen, without scrolling.
- **Metadata is a governance instrument** — version, date, owner, version history. An undated / unowned / unversioned artifact drifts silently.
- The ICP integrates into three places: **CRM** (scored fields), **marketing automation** (Layer 1 filter), **weekly pipeline review** (framing). Without at least the first two integrations, the artifact is documentation, not an operating instrument.
- **ICP drift** is the pattern where founder-led sales gradually accepts out-of-ICP customers deal by deal until the customer base looks nothing like the artifact. It is the opposite of learning; it is un-diagnosed dilution.
- **Five drift-detection signals**, monitored monthly: mix of closed-won in beachhead; ICP-fit-score distribution at close; close-lost reason-code rate; discovery-call time-to-disqualifier check; founder-hours on customer escalations. Two-or-more firing triggers the drift-response protocol.
- The **drift-response protocol** distinguishes two cases: (a) drift → **enforce** (re-authorise the AE, re-run the pipeline against the checklist, refuse out-of-ICP deals for 90 days); (b) genuinely overtaken by product / market change → **revisit** (version-bump with named trigger + change + rollout).
- The **bias is enforcement first, revisit second**. Rewriting the ICP because the AE is uncomfortable saying no is the fastest way to dissolve the beachhead. Revisit requires a named triggering event.
- **Version bumps follow a discipline**: named trigger, named change, owner + reviewer sign-off, rollout communication to sales + marketing, instrument update (CRM fields, Sales Navigator filters, roadmap alignment).
- The one-page ICP is a **hiring instrument** — it compresses the first AE's ramp from 180 days to 60. The absence of a shipped ICP is a first-hire ramp cost the founder often does not attribute correctly.
- The module's arc lands here: **from a scoreable definition (Chapter 1), through the two-layer criteria (2), the disqualifier discipline (3), the three personas (4), the three-axis routing (5), the beachhead-narrowed commitment (6), to the shipped one-page artifact with a drift-diagnosis protocol (7).** The next module (mod-105 Founder-Led Sales) picks this up as the qualification instrument the founder-led motion runs on end-to-end.
