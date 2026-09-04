# Exercise 03 — Good / Better / Best Packaging Authoring

**Estimated time:** 3 hours
**Chapter link:** [`03-good-better-best-packaging.md`](../03-good-better-best-packaging.md)
**Prerequisite:** Chapters 2 and 3 read end-to-end; Exercise 02's anchor price for the middle tier (or an equivalent value-derived anchor); a full list of product capabilities you can copy from a working feature list / roadmap / marketing site; access to the WTP research from Exercise 01 (or an equivalent PSM range).

## Problem statement

Chapter 3 named the failure modes: "starter / pro / enterprise" three-packs authored by intuition; the middle tier that nobody picks; the anaemic middle that forces upgrades resented as trickery; the hollow entry that no real buyer would use; the parallel-universe premium that doesn't anchor; sliding tier boundaries via sales concessions; naming buyers can't map to their situation. The remedy is a **tier-composition worksheet** — capabilities × tiers matrix — plus three coherent tier prices, a coherence check, and an anti-pattern teardown of the worksheet before ship.

This exercise trains you to **author the three-tier pricing structure end-to-end** — the composition worksheet, three tier names, three positioning statements, three anchor prices, the expected-mix stake, and a coherence pass against each of Chapter 3's eight anti-patterns. The output is the tier-structure half of the Chapter 6 pricing pack; combined with the pricing metric from Exercise 04, it becomes the shippable pack.

The failure mode this exercise exists to catch: **the founder invents three tier names, assigns features by intuition, sets three price points that "feel right" as a ladder, and ships a starter/pro/enterprise pack whose middle tier is either bloated (cannibalises premium) or anaemic (forces upgrades). The pack looks like packaging; it is three independent price points wearing packaging clothing.**

## Requirements

Deliver a folder `exercise-03/` with:

- `part-a-tier-composition-worksheet.md` — the capabilities × tiers matrix, per-tier feature composition, per-tier axis dials.
- `part-b-tier-prices-and-positioning.md` — three tier names, three positioning statements, three anchor prices with the ratio defence, expected mix.
- `part-c-coherence-check-and-anti-pattern-teardown.md` — the packaging coherence check plus the eight-anti-pattern teardown.

### Part A — The tier-composition worksheet (75 min)

Deliver `part-a-tier-composition-worksheet.md`.

**A1 — Enumerate capabilities (15 min).** List **every product capability** buyers might value. Aim for 15-30 rows. Sources:

- The product's current feature list / marketing site.
- The Max-Diff attribute list from Exercise 01 (if run) — the top-ranked items are candidates for the anchor tier.
- The roadmap items likely to ship in the next 2 quarters — flag them, but do not include them in the shippable pack (features that don't exist yet cannot be tier-assigned).
- Non-feature capabilities that also differentiate tiers: SSO, SAML, audit logs, on-prem deploy, custom SLA, priority support, dedicated CSM, procurement-friendly contract terms, invoice-vs-credit-card billing, DPA / MSA availability.

Each row is a capability the buyer can name or notice. If she can't tell the difference between two rows in a demo, they are the same capability — merge.

**A2 — Assign capabilities to tiers (25 min).** Fill in the worksheet in Chapter 3's shape. For each capability, mark which tiers include it (`✓` for full include, a note like `rate-limited` or `10/day` for a capped version, `—` for excluded).

```
                                  | Entry | Middle | Premium |
--------------------------------- | :---: | :----: | :-----: |
Capability 1                       |       |        |         |
Capability 2                       |       |        |         |
...                                |       |        |         |
```

Use Chapter 3's discipline:

- **Every tier includes** the capabilities required by the *smallest legitimate use case in that tier*. Entry must be usable for a real small-team persona; middle must be usable for the mainstream ICP without upgrade friction; premium adds the structurally-different capabilities (SSO, enterprise integrations, dedicated CSM, on-prem).
- **The tier boundary is drawn by specific features.** For each of the two boundaries (entry → middle, middle → premium), name the **1-3 specific capabilities** that force the upgrade when the customer needs them. Circle these in the worksheet.
- **Decorative features** (present in every tier or in none, no differentiating role) should be flagged as candidates for removal or de-marketing.

**A3 — Axis-based dials (15 min).** Add the axis-based expansion dials below the feature matrix — the in-tier growth dials that let a customer expand inside a tier before hitting the boundary. Standard dials:

- Seat cap (per tier).
- Repo / project / workspace / entity cap (per tier).
- Usage bracket (events / month, transactions, minutes) if usage-priced.
- Support level (community / email / phone).
- History / retention (7d / 90d / 3yr).

The axis-dials are what the pricing metric (Exercise 04) scales along inside each tier. Feature-fit draws the tier boundary; axis-based scales expansion.

**A4 — Boundary-forcing feature callout (10 min).** For each tier boundary, write one paragraph naming:

- **Which specific capability** forces the upgrade (from A2's circled items).
- **Which persona** is the natural upgrader (the mod-104 persona whose scale or use case first hits the constraint).
- **What signal** in the customer's usage will trigger the upgrade conversation (e.g., "customer hits 8 of the 10 seat cap," "customer requests SSO in a security review").
- **Whether the upgrade is friction-full or friction-light** — a friction-light upgrade is a good boundary (natural growth); a friction-full boundary (customer resents the forced upgrade) is a warning that the boundary is drawn in the wrong place.

**A5 — Roadmap-feature quarantine (10 min).** For any capability you listed in A1 that has not yet shipped, add a `<!-- roadmap: {ETA} -->` marker and *exclude it from the tier assignment*. Shipping-pack tiers may only include capabilities the product actually delivers today. A tier promising an unshipped feature is a bait-and-switch waiting to happen. Note the roadmap items in a separate block at the bottom of the worksheet so the tier composition can be updated when they ship.

### Part B — Tier names, prices, positioning, expected mix (45 min)

Deliver `part-b-tier-prices-and-positioning.md`.

**B1 — Tier names (10 min).** Pick three names from Chapter 3's naming conventions (descriptive of team size / feature richness / business shape). Write down:

- The three names.
- The **audience the name signals** — who does the name tell the buyer this tier is *for*? ("Team" signals mainstream mid-market; "Business" signals procurement-friendly enterprise-adjacent; "Starter" signals evaluation / small teams).
- **The single alternative name you rejected** for each tier, and why (usually to force yourself to think about what the name signals).

Avoid the anti-pattern: precious-metal names ("Silver / Gold / Platinum") that require the buyer to construct her own mapping.

**B2 — Middle-tier anchor price (10 min).** From Exercise 02's value-derived anchor, set the middle tier's per-unit price (per repo, per seat, per event, per month — whatever your candidate metric is). Note:

- **The value-derivation reference** — "middle tier price of $12/repo captures ~7% of the conservative value ceiling."
- **The WTP position** — "$12/repo sits above the OPP of $6-$8 from Exercise 01 and below the PME of $14, i.e. inside the acceptable band, above the modal point."
- **The competitor-sticker position** — where this lands relative to the 3-5 named competitor references.

**B3 — Premium-tier anchor price (10 min).** Set the premium tier at 2-4× the middle (Chapter 3's ratio band). Justify the specific ratio:

- **Feature-set justification** — the structurally-different capabilities the premium adds (SSO, enterprise integrations, dedicated CSM, on-prem) should feel like enough value for the multiple.
- **Enterprise-anchor role** — is this the anchor for a bespoke enterprise negotiation (published as ceiling) or the actual closing price for premium buyers (published as target)?
- **Expected published-vs-closing gap** — if enterprise deals close bespoke, name the range you expect closing prices to land in vs. the published anchor.

**B4 — Entry-tier anchor price (10 min).** Set the entry tier at 20-40% of the middle (or free if the sales motion supports freemium). Justify:

- **Positioning-as-stripped-anchor** — the entry's role is to defend the middle from low-end price war, not to be the vendor's revenue-driver.
- **The freemium-vs-paid choice** — driven by mod-107 sales motion (PLG → freemium; SDR-AE → paid entry).
- **Real-buyer usability** — what specific small-team use case can actually use the entry tier and be served (not a hollow tier)? What's the seat-cap / feature-cap combination that makes it real for that use case?

**B5 — Positioning statements (5 min).** Write one sentence per tier answering "who is this tier for?" in the buyer's language. Examples from Chapter 3:

- "Solo eng / small teams under 10 engineers, GitHub-only."
- "Most teams start here. 20-200 engineers on GitHub."
- "For SSO / compliance / multi-VCS environments."

Every positioning statement names the audience *and* one distinguishing capability or constraint.

**B6 — Expected mix (5 min).** State the fraction of new customers you expect to land in each tier at steady state:

- **Starter: __%.**
- **Middle: __% (the anchor should be highest; typical 60-75%).**
- **Premium: __% (typical 10-15%; > 20% signals a middle-tier feature gap).**

Add a threshold: "if actual mix diverges from expected by more than 10 points, the pack triggers a Chapter 5 experiment." This becomes a guardrail in the Chapter 6 pack (Section 3).

### Part C — Coherence check + anti-pattern teardown (60 min)

Deliver `part-c-coherence-check-and-anti-pattern-teardown.md`.

**C1 — Coherence check (25 min).** Chapter 3 defines the three roles: anchor (middle), ceiling raiser (premium), stripped protector (entry). Test your Part A + B pack against each:

- **Middle-tier-as-anchor test.** For the mod-104 mainstream persona, does the middle tier contain every capability she needs to succeed with the product? Walk through her use case step-by-step and check every capability she would need is present. If she has to upgrade to premium for a mainstream need, the middle is anaemic.
- **Premium-tier-as-ceiling-raiser test.** Does the premium tier include features that are *structurally different* from the middle (SSO, enterprise integrations, dedicated support), not just "more of the same"? If premium is just "middle + higher seat cap," it's not a ceiling raiser.
- **Entry-tier-as-stripped-protector test.** Is the entry priced honestly (20-40% of middle, not 80%) and constrained enough that a mainstream buyer cannot use it? Is there at least one real small-team use case it serves so it isn't hollow? If a mainstream buyer *can* use the entry tier as a permanent home, it will cannibalise the middle.

Answer each test with "pass / partial / fail" and specific evidence from the worksheet.

**C2 — Middle-tier walk-through (15 min).** Take the mod-104 mainstream persona and walk her through the customer lifecycle:

- Signup: does she land in the middle tier or does the pricing page steer her elsewhere?
- Onboarding: does the middle include everything she needs to be successful in the first month?
- Expansion (3-6 months): as her team grows, does the axis-dial (seat count, usage) let her expand inside the middle tier without hitting the boundary too early? What signal would trigger the middle → premium upgrade conversation?
- Renewal: at 12 months, does she look at her invoice and think "fair price for what we're using," or does she feel over- or under-served?

Any friction point is a design flaw in the tier composition.

**C3 — Eight-anti-pattern teardown (20 min).** For each of Chapter 3's eight tier-construction anti-patterns, evaluate your pack:

```
Anti-pattern                          | Fires? | Evidence + fix
------------------------------------- | ------ | ---------------
1. Bloated middle                     | Y/N/P  | ...
2. Anaemic middle                     | Y/N/P  | ...
3. Hollow entry                       | Y/N/P  | ...
4. Parallel-universe premium          | Y/N/P  | ...
5. Linear seat pack (only "how much") | Y/N/P  | ...
6. Features-only, no quotas           | Y/N/P  | ...
7. Everything-and-the-kitchen-sink    | Y/N/P  | ...
   premium (illegible feature list)  |        |
8. Tier boundary that slides          | Y/N/P  | ...
   (sales concessions)               |        |
```

For each `Y` or `P` (partially), write the corrective action you'll apply before the pack ships. For each `N`, write one sentence of evidence — "premium adds SSO, enterprise integrations, on-prem — structurally different, not just 'more of middle'" — not "did not fire."

## Starter guidance

- **Start with the worksheet, not the price.** Chapter 3's discipline: capability × tier matrix first, prices last. Founders who name prices first cannot un-anchor from those prices and rationalise the composition around them.
- **The mainstream ICP is the persona the middle serves.** Every "does the middle include feature X?" question is answered by "does the mainstream persona need feature X?" — not by "would a big customer want it." If a big customer wants it and the mainstream doesn't need it, it's a premium feature.
- **Structurally-different premium features win.** SSO, SAML, on-prem, dedicated CSM, custom contracts, procurement-friendly terms, high-touch support — these are the premium-tier features that buyers understand as belonging to a different tier. "Same as middle but with more seats" doesn't anchor.
- **The entry-tier honesty test:** would a real solo engineer / 5-person team use it as her permanent home for at least 6 months? If yes, it's real; if not, it's hollow. Chapter 3's hollow-entry anti-pattern is a credibility killer — buyers notice and it undermines the whole pack.
- **The freemium decision is a mod-107 decision, not a mod-106 decision.** Chapter 3 explicitly punts to Chapter 4 / mod-107 on freemium-vs-paid entry. Do not overthink it here; pick based on your sales motion (PLG → freemium; sales-led → paid entry) and note the choice.
- **The 2-4× ratio is a band, not a formula.** Chapter 3's ratio band is 2-4× middle → premium; the specific pick depends on how structurally-different the premium feature set is. Two features that are enterprise-must-haves justify 3×; ten features that are mostly cosmetic justify 2×.
- **Enterprise premium tiers can be published-as-anchor.** Chapter 3 notes that many B2B motions publish a premium tier price knowing the actual closing price for enterprise is bespoke. The published price anchors the negotiation. Do not hide the price behind "Contact us" unless the product is truly custom-only.
- **Expected mix is a stake, not a prediction.** You may be wrong; the stake creates the guardrail for Chapter 5's experiments. If you refuse to stake, the pack has no way to notice when mix drifts.
- **The coherence check is the exercise's spine.** Part C1 is where most packs fail. If any of the three role tests scores "fail," the pack isn't ready to ship — go back and revise Parts A or B before Part C2/C3.
- **The mainstream-persona walk-through in C2 catches friction.** A tier that reads well on paper often breaks when you actually walk a persona through her lifecycle. Do C2 with a real persona in mind, not an abstraction.
- **The anti-pattern teardown is not self-flattery.** If all 8 anti-patterns "did not fire," you probably did not check hard enough. Founders routinely have at least 2 partial-fires on a first pack. Honesty in C3 lets you catch them before they cost real revenue.
- **Roadmap features do not belong in the tier assignment.** A tier promising unshipped features is bait-and-switch. Quarantine roadmap items in A5; update the composition when they ship.

## Acceptance criteria

Your submission is complete when:

- [ ] Part A's capability list contains 15-30 rows sourced from the product's actual feature list and Max-Diff attributes (if available).
- [ ] Every capability is assigned to Entry / Middle / Premium (or `—` for excluded) with capped-version notes where appropriate.
- [ ] The tier boundary features (entry → middle, middle → premium) are named explicitly and circled in the worksheet — 1-3 features per boundary.
- [ ] Axis-based dials (seat cap, usage bracket, support level, retention) are listed for each tier.
- [ ] Every roadmap-only feature is marked `<!-- roadmap: {ETA} -->` and excluded from the tier assignment.
- [ ] Part B's three tier names each include the audience they signal and the alternative name rejected.
- [ ] Middle-tier price cites the Exercise 02 value derivation reference, the Exercise 01 WTP-band position, and the competitor-sticker position.
- [ ] Premium-tier price is 2-4× the middle with the ratio justified against the feature-set delta and the published-vs-negotiated policy stated.
- [ ] Entry-tier price is 20-40% of middle (or free with freemium-vs-paid justification) with a named real small-team use case.
- [ ] Each tier has a one-sentence positioning statement naming the audience and one distinguishing capability.
- [ ] Expected mix is stated with a threshold ("mix drift > 10 points triggers experiment") that will feed Chapter 6's guardrails.
- [ ] Part C1 tests the pack against the three roles (anchor / ceiling raiser / stripped protector) with pass / partial / fail + evidence.
- [ ] Part C2 walks the mod-104 mainstream persona through signup / onboarding / expansion / renewal with any friction points named.
- [ ] Part C3 evaluates the pack against all 8 anti-patterns with fire status + evidence + corrective action (for fires) or specific evidence (for non-fires).
- [ ] Any anti-pattern that fires has a specific corrective action to apply before the pack is used in a live sales conversation.

## Common ways this exercise goes wrong

- **The three-independent-prices trap.** Three tiers picked as three price points; no thinking about anchor / ceiling / protector roles. Fix: Part C1's coherence check is what catches this — if any of the three role tests fails, revisit.
- **The anaemic-middle trap.** Middle tier missing team features the mainstream ICP needs (SSO for teams with real IT, roles / permissions, shared workspaces). Mainstream buyers forced to premium, resent the trickery, or stuck at entry with capped ARPU. Fix: C2's mainstream-persona walk-through exposes this; add the missing features to middle.
- **The bloated-middle trap.** Middle includes SSO, SAML, and dedicated CSM. Premium is only chosen by buyers who need on-prem. Premium ARPU is much lower than it should be. Fix: move enterprise features to premium; middle contains what mainstream needs, not what enterprise wants.
- **The hollow-entry trap.** Entry is 1 seat, 100 rows, no export — no real buyer uses it. Buyers see through it. Fix: entry serves a real small-team use case with a specific persona in mind.
- **The parallel-universe-premium trap.** Premium tier is priced 20× the middle and includes an entirely different product. Buyers don't mentally compare it to middle; anchor effect breaks. Fix: 2-4× ratio and structurally-different-but-comparable features.
- **The linear-seat-pack trap.** Entry / middle / premium differ only by seat cap and per-seat price. Fails compromise effect, fails ceiling raiser, fails stripped protector. Fix: feature-fit differentiation at tier boundaries plus axis-dials within tier.
- **The features-only-no-quotas trap.** No caps on anything. Customer cannot expand inside a tier; every expansion is a tier upgrade with churn risk at the boundary. Fix: axis dials per tier (A3) for smooth in-tier expansion.
- **The kitchen-sink-premium trap.** Premium's feature list has 30 items; buyer cannot scan. Anchor effect requires legible comparison. Fix: cap premium's marginal-vs-middle features at 4-6 items; deep detail lives in a comparison chart, not on the tier card.
- **The precious-metal-name trap.** Silver / Gold / Platinum tiers; buyer cannot map to her situation. Fix: descriptive names ("Starter / Team / Business") that communicate who the tier is for.
- **The published-mix-that-becomes-a-prediction trap.** Founder states "we expect 60% Team" and then ignores it. Fix: expected mix is a guardrail with a threshold ("> 10 point drift → Chapter 5 experiment") that gets tracked in the Chapter 6 pack.
- **The roadmap-feature-in-tier trap.** Tier includes a feature that hasn't shipped. Sales team promises it; buyer discovers it doesn't work; deal churns. Fix: A5's roadmap quarantine.
- **The pricing-first-composition-second trap.** Founder picks $99 / $299 / $999 and back-fills the feature composition to justify. Fix: composition worksheet in Part A, prices in Part B — in that order.
- **The self-flattering coherence check.** All three role tests pass; all 8 anti-patterns "did not fire." Fix: honest evidence, not "we thought about this and it's fine" — the exercise's value is in catching what you missed.
- **The tier-that-doesn't-map-to-a-persona.** A tier exists that no mod-104 persona would pick. Fix: every tier serves a specific persona; if no persona uses it, either the persona is missing from mod-104 or the tier shouldn't exist.
