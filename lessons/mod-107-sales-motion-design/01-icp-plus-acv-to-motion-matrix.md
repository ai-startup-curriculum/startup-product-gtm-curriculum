# ICP + ACV → the Motion Matrix

## Motivation

A GTM motion is a *system of choices* — who prospects, who qualifies, who demos, who negotiates, what the buyer touches before she sees a human, what the human touches before the buyer signs — and every one of those choices is set by two upstream facts: **who the buyer is** (mod-104's ICP — the firmographics, the behavioural criteria, the buyer/user/champion split) and **how much the deal is worth** (mod-106's pricing pack — the ACV, the packaging, the pricing metric). Get the motion wrong for the ICP + ACV combination and everything downstream degrades: PLG conversion rates for a mid-market ACV never touch the numbers self-serve products post, enterprise MEDDPICC ceremony on a $99/month sign-up produces zero paying customers and a Slack channel full of angry developers, and outbound SDR-AE teams stapled to a bottoms-up developer tool fail because the "buyer" they're prospecting isn't the buyer at all.

Motion selection is one of the highest-leverage decisions in early-stage GTM. It sets the shape of the team the founder is about to build (do we need an SDR? an AE? a solutions engineer? a customer-success rep?), the shape of the funnel she is about to instrument (which stages? which conversion rates? which cohort measurements?), and the shape of the pricing pack (does the tier lineup support in-product upgrade prompts, or does it assume a redlined MSA?). A motion mismatch is not a bug you fix in the next sprint — it is a foundational error that costs quarters of team time, mis-hires, and re-tooled infrastructure. Chapter 1 sets the frame the rest of the module is calibrated against.

The failure mode this chapter exists to catch: **the founder chooses the motion she likes (usually the one she has seen work in a previous company, or the one that sounds least sales-y, or the one whose playbook is most fashionable that quarter), rather than the motion the ICP + ACV combination demands. She then spends two quarters wondering why "self-serve isn't converting" or "enterprise sales won't close" — when the actual answer is that the motion never fit the market to begin with.**

This module treats motion selection as a *derivation from the pricing pack and the ICP*, not a preference. Chapter 1 sets that derivation up as a matrix. Chapters 2, 3, and 4 develop the three motion archetypes (PLG, SDR-AE, enterprise) in detail. Chapter 5 threads the qualification framework through the CRM. Chapter 6 diagnoses the mismatches — which is where most of the reader's early-career pattern-recognition will come from.

## Core concepts

### The two axes — ACV and self-service willingness

The primary axis is **ACV** — the annual contract value the deal is worth. Everything else (cycle time, buyer complexity, deliverable ceremony, comp structure) correlates with ACV so tightly that the sales-motion literature typically indexes on it directly. The bands the working literature uses (Christoph Janz's "Five Ways to Build a $100M Business" is the canonical framing, updated across the OpenView and Bessemer benchmark series):

- **Micro / self-serve ACV** — under ~$1K/year per customer. The unit economics require thousands to tens of thousands of customers; human touch per customer is cost-prohibitive.
- **Low ACV** — ~$1K–$10K/year. Human touch is possible but costly; PLG with a light sales-assist layer is common; pure SDR-AE inside sales is often over-invested unless the product needs a demo to activate.
- **Mid-market ACV** — ~$10K–$100K/year. The economics support an inside-sales SDR-AE team; the deal is complex enough that a demo and a proposal are typically needed; the buyer is usually a director or VP but not an enterprise buying committee.
- **Enterprise ACV** — ~$100K–$1M/year. The deal has a formal buying committee, procurement, legal review, security review; MEDDIC / MEDDPICC discipline is load-bearing; sales cycles are 6-18 months; the account team includes an AE, an SE, and often a CS onboarding lead.
- **Strategic / mega-deal ACV** — > ~$1M/year. Board-level buying, custom terms, executive sponsorship, multi-quarter deal cycles; often a dedicated named-account team; largely out of scope at the seed / Series-A boundary this module targets.

The bands are working conventions, not physical laws — a $12K ACV can be sold on a light-touch inside-sales motion or on a PLG self-serve motion depending on the ICP and the product. But the *shape* of the motion is set by the band, and forcing a motion two bands off from the ACV band is what produces the mismatches Chapter 6 dissects.

The secondary axis is **self-service willingness** — how willing the buyer is to complete the purchase without talking to a human. Self-service willingness depends on:

- **Buyer sophistication** — developers, PLG-native product-managers, and startup-founder buyers self-serve happily; enterprise procurement, security-cleared IT buyers, and regulated-industry buyers do not.
- **Deal complexity** — a single-user tool with a credit-card price is self-serviceable; a tool that requires SSO configuration, security review, and legal terms is not.
- **Buyer role vs. user role** — when the user is also the buyer (individual developer buys their own tool with a personal card, or expenses under a small team's discretionary budget), self-service works; when the user (developer) and the buyer (VP, procurement) are different people, a human touch is usually required to bridge them.

The two axes cross into a matrix:

```
                                 self-service willingness →
                                 low                    high
                       +--------------------+-----------------------+
        enterprise     | MEDDPICC          | (rare — usually       |
        ACV            | enterprise motion  | a two-track hybrid)   |
        ($100K+)       | with full ceremony |                       |
                       +--------------------+-----------------------+
        mid-market     | SDR-AE inside sales| PLG + sales-assist    |
        ACV            | (Predictable       | (product-led with     |
        ($10-100K)     | Revenue tradition) | human upgrade path)   |
                       +--------------------+-----------------------+
        low ACV        | (unstable — usually| PLG / self-serve      |
        ($1-10K)       | means the ACV      | (Wes Bush / OpenView) |
                       | should be higher)  |                       |
                       +--------------------+-----------------------+
        micro ACV      | (economically      | Self-serve pure       |
        (<$1K)         | infeasible)        | (no human in the loop)|
                       +--------------------+-----------------------+
```

The diagonals — high-ACV / high-self-service and low-ACV / low-self-service — are the mismatch zones. High-ACV / high-self-service (a $250K deal that closes on a Stripe checkout) is vanishingly rare in practice; when it appears it is usually a deal that grew from a self-serve seed into an enterprise expansion, and the enterprise expansion still runs the ceremony. Low-ACV / low-self-service (a $3K deal that requires a 12-week SDR-AE cycle) is economically unstable — the CAC eats the ACV and the payback stretches beyond the retention window. The motion mismatch is almost always caught at unit-economic review: the CAC / payback numbers do not survive.

### The three motion archetypes

The rest of the module develops the three cells that dominate practice:

- **PLG / self-serve** — Chapter 2. Buyer discovers the product (organic, referral, community, content), signs up herself, activates inside the product, hits a natural expansion trigger (team invite, usage limit, gated feature), and upgrades — with the sales conversation happening either in-product (upgrade prompt) or on a light-touch sales-assist call.
- **SDR-AE inside sales** — Chapter 3. SDR (or founder acting as SDR) generates the opportunity from a target-account list, hands off to an AE (or founder acting as AE) at a defined qualification bar, AE runs discovery + demo + proposal + close over a 4-12 week cycle, single-quota comp for the AE (with SDR sitting on a booked-meeting or booked-opportunity metric).
- **Enterprise MEDDPICC** — Chapter 4. Named-account team (AE + SE + CS) runs a 6-18 month cycle across a formal buying committee (economic buyer + technical evaluator + user + procurement + legal + security), with MEDDPICC discipline (Metrics, Economic buyer, Decision criteria, Decision process, Identify pain, Champion, Paper process, Competition) threaded through every stage transition.

The three motions are not mutually exclusive. A mature SaaS company runs a PLG top-of-funnel that produces PQLs which the SDR-AE team qualifies into demos which — when the account crosses a threshold — get handed off to the enterprise team for the six-figure expansion. The three archetypes are the *building blocks*; a company's actual motion is often a stack of two or three of them. But the stack has to be designed intentionally — a company that says "we do all three motions" without designing the hand-offs between them ends up with three under-invested motions, none of which produces revenue.

### The ICP inputs — what mod-104 sends to this module

mod-104's ICP scorecard is the primary input. The three components that most directly determine the motion:

- **The firmographic band** — company size, revenue band, funding stage, geography. A 10-50-person startup ICP maps naturally to a low-ACV self-serve or light-touch motion; a Fortune 500 ICP maps to an enterprise MEDDPICC motion. Firmographic mixing (an ICP that spans "10-person startups and Fortune 500 enterprises") is usually an ICP-drift symptom (mod-104 Chapter 7); the motion the founder chooses will fit one end and mismatch the other.
- **The behavioural criteria** — what the buyer does before she comes to the vendor. A buyer who Googles for the solution and evaluates 4-5 vendors self-serve is a PLG-native buyer; a buyer who issues an RFP through a procurement process is an enterprise buyer.
- **The buyer / user / champion split** — the more the roles are separated (user is a developer, buyer is a VP, champion is an engineering manager, economic buyer is a CFO), the more the motion has to be human-touch — because a self-serve product cannot bridge four separate humans by itself.

Where mod-104 produces an ICP that spans multiple firmographic or behavioural clusters, the motion decision has to *pick the primary segment* (the beachhead — mod-104 Chapter 6) and design the motion for that segment. The other clusters get a "not now" annotation until the primary motion is stable.

### The ACV inputs — what mod-106 sends to this module

mod-106's pricing pack is the second input. The three components that most directly determine the motion:

- **The primary ACV** — the anchor tier's per-customer annual revenue at the target adoption level. This is the ACV band the motion is designed for. A pricing pack whose anchor tier is $8K ACV cannot support a motion that costs $15K per closed customer; the CAC swallows the ACV in year one.
- **The pricing metric** — per seat aligns naturally with SDR-AE inside sales (seat expansion is the natural land-and-expand vector); per-usage aligns naturally with PLG (the usage curve is the in-product upgrade prompt); per-outcome or per-license aligns with enterprise (the outcome is what the CFO is buying). Mismatched metric-to-motion combinations (per-seat with a PLG motion where seat additions happen invisibly; per-usage with an enterprise motion where the CFO cannot forecast the bill) produce revenue drag.
- **The tier structure** — a good/better/best pack with a "team" tier priced at $20K ACV and an "enterprise" tier priced at $80K ACV is offering two motions simultaneously; the sales team has to be able to run both. A single-tier pack ($99/user/month, no enterprise option) implicitly rules out the enterprise motion.

The pricing pack is not immutable. If the ICP obviously demands an enterprise motion but the pricing pack has no enterprise tier, the fix is to revisit the pricing pack (mod-106) before the motion — not to run enterprise sales on a $99/month sticker.

### Why forcing the wrong motion breaks GTM

Three concrete failure modes recur across the practitioner literature (Kazanjy, Bush, Skok, Ross, Roberge):

**Enterprise ceremony on a self-serve product.** The founder — often from an enterprise-sales background — insists on running a "proper sales process" against a $99/month self-serve product. The buyer, who wanted a credit-card sign-up, is asked to book a 30-minute discovery call, sit through a demo, receive a proposal, negotiate a term, and sign an MSA. She abandons at the discovery-call step and buys a competitor's self-serve product instead. The founder concludes the market is not ready; the actual answer is that enterprise ceremony destroyed a self-serve motion that would have converted on its own. The fix is to remove the human from the funnel (self-serve checkout, in-product onboarding, PLG upgrade prompts) — the motion Chapter 2 develops.

**Self-serve on a $100K contract.** The founder — often from a developer-tools or consumer background — ships a "start free, invite your team, upgrade when you're ready" motion at a $100K ACV. The buyer's procurement process demands an MSA, security review, and a redlined contract; the self-serve upgrade path has no place to route the procurement conversation. The deal stalls in a Slack DM between the champion and the founder, no forecast can be made, and the deal either close-losts or drags into next year with no visibility. The fix is to run a real enterprise motion — named account, MEDDPICC, SE support, procurement engagement — the motion Chapter 4 develops.

**Mid-market SDR-AE on a bottoms-up developer product.** The founder — often advised by "you need to hire SDRs" from an investor — hires a two-SDR-and-one-AE team and points them at a developer-tools product whose buyer discovers the product by Googling "how do I fix X" and adopting it inside a nights-and-weekends prototype. The SDRs cold-call the head of engineering; the head of engineering has never heard of the product; the AE demos to a buyer who did not ask for a demo; the developer who already loves the product is not on any of the calls. Six months later the SDR-AE team has produced zero pipeline; meanwhile the product has 4,000 individual developers using it who would have upgraded to a team plan if there had been a team-plan checkout flow. The fix is to build the PLG motion (Chapter 2), replace the SDRs with a growth engineer, and use the AE role for sales-assist on the accounts that self-serve into the top of the tier lineup.

Each failure mode is diagnosable in the same way: **CAC / payback numbers fail** (the motion is too expensive for the deal size), **conversion rates fail across the stage boundary** (the buyer disengages at the ceremony step, or at the checkout step, depending on direction), and **the sales team's forecast falls apart** (the AEs are calling deals as pipeline that never move to demo, or the growth funnel is producing sign-ups that never upgrade). Chapter 6 turns this diagnostic into a repeatable teardown.

### The one-motion-first discipline

A common trap: founders try to run all three motions simultaneously at seed, because "we don't know yet which will work." This is a false thrift. Every motion has fixed overhead — the SDR-AE motion needs a target-account list, a cadence tool, a CRM stage set, a comp plan; the PLG motion needs a self-serve checkout, in-product upgrade prompts, a PQL definition, a growth-analytics instrument; the enterprise motion needs an MSA, a security package, a proposal template, an SE role. Three under-invested motions produce less revenue than one properly-invested motion — because each of them fails at the last-10%-of-execution step where the tooling and the discipline become load-bearing.

The one-motion-first discipline: **pick the motion that fits the primary ICP + primary ACV combination, invest fully in it, run it until it produces a repeatable close rate at a defensible CAC / payback, then add the second motion.** The second motion is almost always a *layer* on the first — a PLG top-of-funnel added under an SDR-AE motion, an enterprise expansion tier added on top of a PLG motion. The layering has to be deliberate; the layers have to be designed against each other. A stacked motion is a Chapter 6 topic; a single motion at Chapters 2-4 is the pre-requisite.

## Concrete example — Loomly picks its motion

Loomly (the running mid-market devtools example: dependency-graph SaaS for B2B engineering teams; ICP is 50-150-engineer B2B SaaS companies on GitHub; pricing pack from mod-106 = $6/repo/month anchor tier with $12/repo/month premium, average ICP customer has ~40 repos → $12K/year anchor, $24K/year premium; buyer/user/champion split from mod-104 = VP Eng (buyer), Engineering Manager (champion), individual engineer on the platform team (user)) sits down to pick the motion.

**Step 1 — Locate on the matrix.** ACV is $12K–$24K/year — mid-market band. Self-service willingness is medium: the individual engineer would happily self-serve a free tier, but the $12K purchase almost always requires the VP Eng's sign-off, and mid-market VP Engs at 50-150-engineer companies typically want a demo before they approve a new tool for team-wide use. That puts the deal in the "mid-market ACV, medium self-service" cell.

**Step 2 — Consider each of the three motions.**

- *Pure PLG / self-serve* — possible: a free tier scans one repo, the individual engineer adopts it, invites her team, the team hits the paywall at repo 6, and upgrades. Would work if the buyer were the individual engineer with a personal budget; but the actual budget owner is the VP Eng, and the VP Eng needs a demo. Pure PLG risks stalling every deal at the "our VP needs to see this before we upgrade" step with no sales-assist infrastructure to answer the call.
- *SDR-AE inside sales* — possible: an SDR prospects the target-account list (50-150-engineer B2B SaaS companies on GitHub, ~800 companies in the accessible market), books demos with the VP Eng, an AE runs the SPICED discovery / demo / proposal / close cycle at $12K–$24K ACV over 4-8 weeks. Would work; the deal shape supports it. Requires an SDR-AE team, which the founder does not yet have; the founder could run as SDR-AE hybrid herself for the first 20 deals (mod-105).
- *Enterprise MEDDPICC* — over-investment. $12K–$24K ACV cannot amortise a 6-month enterprise cycle with an SE and a formal procurement conversation. The ICP does not have Fortune 500 enterprise-buyer complexity — the VP Eng owns the tools budget directly.

**Step 3 — Pick the primary motion and the layer.**

- Primary: **SDR-AE inside sales** (founder-led at seed per mod-105; hire the split once the motion is repeatable per Chapter 3 of this module). Deal shape and ACV fit the band cleanly.
- Layer: **PLG top-of-funnel** as a lead-generation source. Free-tier sign-ups from individual engineers become the target-account list; a sign-up from a company on the ICP list triggers an SDR outreach ("we noticed three engineers at Acme signed up; would the VP Eng like a walkthrough?"). The PLG layer is subordinate — its job is to feed the SDR-AE motion, not to close its own deals.

**Step 4 — Explicitly rule out the mismatches.**

- Not a pure PLG motion (would stall at VP-Eng approval).
- Not an enterprise MEDDPICC motion (over-invested for ACV).
- Not a "we run all three" motion (fixed overhead sinks each of them).

**Step 5 — Design the motion.** SDR-AE inside sales motion designed in Chapter 3; PLG lead-generation layer designed in Chapter 2 (subset — activation event and PQL definition, but not full self-serve upgrade). Enterprise motion (Chapter 4) is deferred to a future stage when the ICP expands to include 500+-engineer companies with formal procurement.

The motion decision, made this way, is one paragraph of rationale plus a matrix cell. It is defensible against a board question ("why aren't you running PLG?") because the reasoning traces to the ICP and the ACV. It is diagnosable if the numbers fail six months in ("SDR-AE conversion is 40% below benchmark") because the CRM stages will show *where* the failure is — as opposed to a founder-intuition motion where a bad number is un-attributable.

## Common failure patterns

- **Choose-the-motion-you-know trap.** The founder picks the motion she has seen work in a previous company, regardless of whether the current ICP + ACV combination supports it. Ex-enterprise founders default to enterprise; ex-PLG founders default to PLG; ex-Predictable-Revenue founders default to SDR-AE. Fix: derive the motion from mod-104 + mod-106, not from career history.
- **Choose-the-motion-that's-fashionable trap.** The founder picks the motion currently discussed on Twitter / on First Round Review / at the last conference. PLG had a moment 2020-2023; enterprise came back into fashion 2024-2026. Fix: fashion is a signal about *what other founders are talking about*, not about *what this ICP + ACV combination requires*.
- **Run-all-three-motions-simultaneously trap.** Founder does not want to choose; runs a light version of all three. Each motion is under-invested; none produces a repeatable close rate. Fix: pick one motion, invest fully, layer the second only when the first is stable.
- **Motion-locked-in-before-pricing trap.** Founder picks the motion (say, PLG) before the pricing pack (mod-106) is set, then discovers the pricing pack demands an enterprise tier — but the motion has no enterprise team, and the founder half-runs enterprise deals on top of a PLG motion. Fix: pricing pack (mod-106) precedes motion decision; motion is derived from the pricing pack, not chosen alongside it.
- **Ignore-the-buyer-user-champion-split trap.** Founder picks the motion based on the user (self-serve because the user is a developer who self-serves) and forgets that the buyer (VP Eng, with a budget-approval process) has a different motion requirement. Fix: motion has to serve the buyer's decision process, not just the user's adoption process.
- **Confuse-free-trial-with-PLG trap.** Founder ships a 14-day free trial with a "book a demo to continue" wall at day 14 and calls it PLG. This is *inside sales with a free trial as a lead magnet*, not PLG. Fix: PLG means the buyer can self-serve to the paid state; if she can't, it isn't PLG.
- **Confuse-hiring-an-SDR-with-having-an-outbound-motion trap.** Founder hires an SDR before designing the target-account list, the cadence, the response-rate benchmark, or the AE-hand-off criteria. SDR does not produce pipeline. Fix: motion design (this module) precedes hiring; hiring is what you do to *scale* a validated motion.
- **Enterprise-because-one-big-logo-asked trap.** Founder pivots to enterprise motion because a Fortune 500 buyer replied to a cold email and asked for a proposal. The rest of the ICP is mid-market. Founder rebuilds the pricing pack, the sales process, and the SE role for one deal — and that deal close-losts anyway because the enterprise motion isn't ready. Fix: one enterprise deal is not a motion; treat it as bespoke and continue running the mid-market motion for the primary ICP.
- **Sub-scale-CAC / payback trap.** Founder picks a motion whose CAC ($8K to close through SDR-AE) exceeds the ACV ($6K/year). The unit economics don't work no matter how well the motion executes. Fix: match motion to ACV band; if the ICP + product only supports low ACV, the motion has to be self-serve; if the ICP only supports human-touch, the pricing pack has to move up-market.

## Summary

- A GTM motion is a **system of choices** derived from two upstream facts: the **ICP** (mod-104) and the **ACV** (mod-106). Motion selection is not a preference; it is a derivation.
- The primary axis is **ACV** — micro (<$1K), low ($1-10K), mid-market ($10-100K), enterprise ($100K-$1M), strategic ($1M+). The secondary axis is **self-service willingness** — a function of buyer sophistication, deal complexity, and buyer-user-role separation.
- The three motion archetypes: **PLG / self-serve** (Chapter 2), **SDR-AE inside sales** (Chapter 3), **enterprise MEDDPICC** (Chapter 4). The matrix cell the ICP + ACV combination lands in tells you which one to pick.
- The **mismatch zones** — high-ACV / high-self-service and low-ACV / low-self-service — are usually diagnosable in unit economics (CAC / payback fails) and in conversion rates (buyer disengages at the mismatched step).
- The three canonical failure modes: **enterprise ceremony on a self-serve product**, **self-serve on a $100K contract**, **SDR-AE on a bottoms-up developer product**. Each maps to a specific fix from the motion each mis-selected against.
- Motions are not mutually exclusive at scale — a mature company **layers** two or three of them — but the layering has to be deliberate, and the second motion is added only after the first produces a repeatable close rate at a defensible CAC / payback.
- The **one-motion-first discipline** — pick the motion that fits the primary ICP + primary ACV combination, invest fully, run to repeatability, then layer. Three under-invested motions produce less revenue than one properly-invested motion.
- The **inputs** the motion is derived from: mod-104's firmographic + behavioural + buyer/user/champion split (the ICP), and mod-106's ACV + pricing metric + tier structure (the pricing pack). The motion is a *dependent variable* on both.
- Chapter 2 develops the **PLG motion**; Chapter 3 develops the **SDR-AE motion**; Chapter 4 develops the **enterprise MEDDPICC motion**; Chapter 5 threads the qualification framework through the CRM; Chapter 6 turns the mismatch diagnosis into a repeatable teardown.
