# Proposal, Close, and Founder-Led-Sales Anti-Patterns

## Motivation

Stages 5 and 6 of Kazanjy's model — proposal and close — are where the deal architecture becomes contractual and where the founder's unbounded authority becomes either a superpower or a liability. It is also the stage where the four highest-cost founder-led-sales anti-patterns actually happen: **deep-discounting to close a wobbly deal**, **feature-promising to unstick a stalled proposal**, **taking non-ICP deals to hit a revenue number**, and **saying yes to a scope the product cannot deliver in the promised timeframe**. Each of these has a specific dynamic — the founder is under real pressure (runway, quarter-end, board meeting) and reaches for a tool that closes today's deal at tomorrow's expense.

The pressure is real. But the tools are wrong. A deal closed at 60% discount trains the pipeline to expect 60% discount. A deal closed on a feature promise that ships two quarters late trains the customer to churn. A non-ICP deal absorbs 3-5x the CSM cost of an ICP deal and often churns anyway. A yes to unsupported scope creates a support burden that the founder personally absorbs for years. Every one of these is a decision the founder has authority to make and would be well-advised not to.

The failure mode this chapter exists to catch: **the founder writes a proposal without a template, negotiates without a rate card, closes without a specific paper-out plan, and uses her unbounded authority to close deals that shouldn't have closed — inflating the closed-won number while degrading the pipeline's future characterisation.**

The remedy: a **written proposal template**, a **rate card + discount authority ladder**, a **paper-out plan** for every deal above a defined ACV, and a working knowledge of the four anti-patterns with a rehearsed script for saying no when the founder should. This chapter develops both halves — the mechanics of proposal-through-close, and the anti-patterns that turn those mechanics into liabilities.

## Core concepts

### The proposal — what it is and what it does

The **proposal** is the written artifact that converts a demo-qualified deal into a contractable one. It has four working functions:

1. **Locks the scope.** What the customer is buying — the product tier, the user count, the integration set, the SLA level. Ambiguity here becomes a support-escalation later; specificity here becomes a clean expansion path later (mod-109).
2. **Locks the price and payment terms.** Annual vs. monthly, quarterly billing vs. annual up-front, seat pricing vs. flat, discount if any (with the reason coded), payment terms (net 30 default, sometimes net 60 for enterprise).
3. **Locks the commercial terms.** Contract length (12 months default at SEED — longer terms trade discount for cash certainty), auto-renewal clause (default 60 days notice; be careful with 90+), termination-for-convenience if any, SLA credits for uptime failures.
4. **Locks the close plan.** The specific sequence of steps from proposal-sent to signed contract, with dates for each — mirror of the mutual-action-plan from Chapter 5 for MEDDPICC deals, compressed for SMB deals.

The proposal is not a place to hedge. Every hedge — "starting price," "typical range," "we could discuss" — is a request the buyer will exercise. The founder writes a proposal that is *the deal* the founder actually wants, at the price the founder actually wants, at the scope the founder actually wants, and defends it. Discounting from a defended proposal is a strategic choice; discounting from a hedged proposal is default behaviour.

### The proposal template — the shipping shape

The founder-led-sales proposal template ships as a 2-3 page document (not a slide deck; deals close on documents, not decks). The shape:

```
─────────────────────────────────────────────────────────
PROPOSAL — {product} for {customer} — {date} — v{version}
Prepared by: {founder}. Contact: {email} / {phone}
─────────────────────────────────────────────────────────

1. CONTEXT (½ page)
   {2-3 sentence recap of the pain, sized in the buyer's language and numbers}
   {1-2 sentence recap of what this proposal addresses and how}

2. SCOPE (½ page)
   Product tier: {name of tier}
   Included: {seat count, integrations, features, SLA level}
   Not included: {what's not in scope — this list matters for expansion later}
   Deployment: {SaaS-hosted / dedicated / on-prem — usually SaaS at SEED}

3. PRICE (¼ page)
   Annual contract value: ${X}
   Payment terms: {annual up-front / quarterly / monthly}
   Contract length: {12 mo default}
   Auto-renewal: {60-day notice-required default}
   Discount applied (if any): {%} — reason: {promo / multi-year / logo}

4. IMPLEMENTATION + SUCCESS (¼ page)
   Kickoff date: {target}
   Onboarding scope: {what the vendor does; what the customer does}
   Success metric baseline: {the mutually-agreed KPI at 30 / 60 / 90 days}
   CSM contact: {founder as CSM at SEED; named CSM later}

5. CLOSE PLAN (¼ page)
   Step 1: Redline round 1 by {date, owner: customer legal}
   Step 2: Security review response by {date, owner: vendor}
   Step 3: Economic-buyer / CFO sign-off by {date, owner: customer}
   Step 4: Final redlines by {date, owner: joint}
   Step 5: Countersign + PO by {date, owner: joint}
   Step 6: Kickoff by {date, owner: joint}

6. TERMS + LEGAL (½ page or attached MSA)
   Payment: {net 30}
   Termination: {termination-for-convenience with 30-day notice, if any}
   Data / DPA: {DPA attached, SOC 2 report available under NDA}
   Governing law: {vendor's state, negotiable}

─────────────────────────────────────────────────────────
```

The template is versioned per customer (v1 initial, v2 post-redline, v3 final). Every version is dated. The template is a working document, not a marketing artifact — the customer's legal will redline it, and the redlines are the actual negotiation.

### The rate card and the discount ladder

Founders default to "let me see what I can do" pricing. This is the specific dynamic that produces deep-discounting anti-patterns. The remedy is a **rate card**: a written, internal document that specifies the standard price for each tier, the discretion band for each seller role, and the escalation authority for anything beyond.

A founder-scale rate card (before AE hires):

```
─────────────────────────────────────────────────────────
LOOMLY RATE CARD — v{version} — {date}
─────────────────────────────────────────────────────────

STANDARD PRICING
  Starter (up to 50 eng):        $6,000/year
  Growth (up to 150 eng):        $12,000/year
  Scale (150-500 eng):           $30,000/year
  Enterprise (500+ eng):         custom, floor $75,000/year

FOUNDER DISCRETION
  ≤ 15% discount:                 approved (any reason coded)
  16-25% discount:                 approved with reason: logo / multi-year / non-standard scope
  > 25% discount:                  requires deliberate exception + logged rationale

DISCOUNT REASONS (coded)
  MULTIYEAR:    signed 24- or 36-month contract, 10-15% typical
  LOGO:         high-value reference customer, ≤ 20% typical
  PROMO:        Q4 push or launch promo, ≤ 15%, time-bounded
  SCOPE:        reduced-scope tier (fewer users / features)
  EXCEPTION:    everything else — deliberate override

RENEWAL FLOOR
  Renewals price at or above initial ACV; exceptions only for scope reduction.
─────────────────────────────────────────────────────────
```

Two rules land the rate card:

- **Never quote a price without a reason for the price.** Every discount lands with a coded reason logged in the CRM. This is what lets Chapter 7's win/loss analysis distinguish a healthy multi-year discount ($ up-front + logo value) from an unhealthy panic discount (quarter-end pressure).
- **The founder does not violate her own rate card without a written exception.** If a deal genuinely requires a 40% discount, the founder pauses, writes down the reason (a two-sentence rationale in the CRM), and either approves it as a deliberate exception or holds the line and lets the deal walk. The exception log is what surfaces patterns — three "one-time" 40% discounts in a quarter is not one-time, it is a pricing problem (mod-106).

### The four founder-led-sales anti-patterns

The four anti-patterns share a shape: the founder is under real pressure, reaches for a tool that closes today's deal at tomorrow's expense, and rationalises it because "we need the revenue." Recognising the pattern in the moment is the discipline.

**Anti-pattern 1: Deep-discounting to close.**

The pattern: buyer stalls at proposal; founder offers a 40% "for you today" discount; deal closes. Two costs:

- **Pipeline conditioning.** Every buyer in the same segment eventually learns the price is negotiable at 40%. Deals that would have closed at rate card now close at rate-card-minus-40. Blended ACV drops without a visible cause.
- **Anchor collapse.** Renewal negotiations start from the discounted price, not the rate-card price. What was a "one-time" 40% discount becomes the customer's expected price. Renewal expansion (mod-109) has to overcome a discount hangover.

The healthy alternative: **discount only against a coded reason and a written rate-card band**. A multi-year discount ($ up-front + long commitment) is a fair trade. A quarter-end panic discount is not — it is the founder solving her cash-flow anxiety at the customer relationship's expense. If a deal genuinely will not close without a > 25% discount, that deal is either mis-priced (mod-106 signal), out-of-ICP (mod-104 signal), or genuinely walk-away. Walking away is a strategic choice; a rate-card violation is not.

**Anti-pattern 2: Feature-promising.**

The pattern: buyer at proposal says "we need X to close" (X is a feature the product does not have); founder says "yes, we'll build that in the next quarter"; deal closes. Three costs:

- **Roadmap distortion.** The next-quarter roadmap now has an unplanned commitment. Either it ships (crowding out planned work) or it doesn't (the customer churns).
- **Trust collapse if late.** Founder-committed feature dates are, empirically, wildly optimistic. When the feature ships two quarters late, the customer's champion is embarrassed internally and the deal churns at renewal.
- **Precedent for the next deal.** Every subsequent buyer learns that feature-promises are how deals close. The pattern compounds.

The healthy alternatives:

- **Honest disqualification.** If X is a hard requirement and X is genuinely > 6 months away, the deal is not a fit today. Name it; commit to reactivation when X ships; close-lost clean.
- **Contractual promise with real dates.** If X is genuinely coming in 8 weeks (and the founder is right about the 8 weeks), commit to the ship date *in the contract*. The customer's SLA can include a right-to-terminate if the feature does not ship by the contracted date. This makes the promise real for both parties and forces the founder to be honest with herself about ship dates.
- **Scope adjustment.** If X is nice-to-have (not hard requirement), re-scope the deal to work without X, discount trivially, sign now, and add X later as an expansion (mod-109). The customer gets value today; the vendor gets a real deal with a natural upsell path.

**Anti-pattern 3: Taking non-ICP deals to hit a number.**

The pattern: quarter is ending, the number is short, a non-ICP deal is in the pipeline (wrong segment, wrong ACV, wrong buyer, wrong stage); founder closes it to hit the number. Four costs, all documented in mod-104's ICP-drift discussion:

- **Support burden.** Non-ICP customers are 3-5x more support-intensive than ICP customers because the product is not built for their workflow. Founder-hours pour into custom work.
- **Churn risk.** Non-ICP customers churn at 2-3x the rate of ICP customers. Six months later, the deal is gone and the CSM cost is not recoverable.
- **Product-pull distortion.** The non-ICP customer's feature requests pull the roadmap in a direction that doesn't help the ICP. Two quarters later, the product has drifted (mod-104 Chapter 7's ICP drift).
- **Reference-pattern pollution.** The non-ICP customer, if she does convert to a case study, is not a reference the ICP will respond to. The case-study library, and the outbound narrative it feeds, degrades.

The healthy alternative: **honest disqualification, referral to a partner where possible, close-lost clean, and eat the quarter-miss**. The board / investor / co-founder will notice a missed quarter; they will not notice the ICP drift that a "hit-the-number" deal causes until six months later. The right conversation is the honest one now, not the quiet-drift one later.

**Anti-pattern 4: Saying yes to a scope the product cannot deliver.**

Related to feature-promising but broader: the buyer asks for a custom integration, a bespoke deployment, a hand-holding onboarding, a custom SLA, a data-residency arrangement, or a legal term the vendor's boilerplate cannot support. The founder — pressured, empowered, and eager to close — says yes to all of them. The costs compound over the customer relationship: the custom integration requires ongoing engineering maintenance, the bespoke deployment breaks with every product upgrade, the hand-holding onboarding sets a precedent that scales to zero, the custom SLA creates liability exposure the vendor has no legal team to manage, the data-residency arrangement pins the customer to a region the vendor does not otherwise support.

The healthy alternative: **defended standard scope with a documented exception process**. Custom scope is negotiated the way rate-card discounts are negotiated — with a coded reason, a written rationale, an explicit exception log, and — critically — an *incremental price* attached. Custom integrations at a $50K one-time engineering fee; bespoke SLA at a 30% premium; on-prem deployment at 2x the SaaS price. Pricing the exception is what makes it a business decision instead of a favour.

### The close plan — the paper path

The close plan is the specific sequence of steps between proposal-sent and countersigned-contract. For SMB deals it may be 3-4 steps and fit in a paragraph; for enterprise deals it is a full MAP (Chapter 5). Either way it must exist in writing.

The canonical close-plan steps:

1. **Redline round 1.** Customer's legal reviews the proposal and returns comments. Typical duration: 3-10 business days. Ownership: customer legal, with vendor pushing for timeline.
2. **Vendor response to redlines.** Vendor accepts / counters each redline. Typical duration: 2-5 business days. Complex commercial redlines require a founder decision; boilerplate MSA redlines can be handled with a standard playbook.
3. **Security review.** Customer's security / IT reviews vendor's SOC 2, DPA, security-questionnaire. Typical duration: 1-3 weeks (this is often the longest step; it should be started as early as possible, ideally at demo not at proposal).
4. **Economic-buyer sign-off.** For MEDDIC deals, the CFO / department head signs off on the price and terms. Typical duration: 1 meeting + 2-5 days. Champion is on the hook for scheduling this.
5. **Final redlines + countersign.** Any remaining terms are finalised; both parties sign. Typical duration: 2-5 business days.
6. **PO issuance (enterprise) or invoice-and-pay (SMB).** Customer procurement issues a PO, or SMB pays the invoice. Typical duration: 1-4 weeks for enterprise procurement (this is the second-longest step, often invisible to sellers).
7. **Countersign complete + kickoff booked.** Deal is closed; kickoff meeting is on the calendar within 1-2 weeks.

Every step has an owner, a target date, and a status. Every stall of a step triggers a specific action: 3-day slip → soft nudge; 7-day slip → escalation to champion; 14-day slip → escalation to buyer + honest "is this deal still real?" conversation.

### The paper process — the specific enterprise trap

MEDDPICC's "P" — paper process — is the enterprise-scale version of the close plan and often the longest single stage of a large deal. Paper processes fail two ways:

- **Underestimated duration.** Founder forecasts a $200K deal to close in 4 weeks; procurement takes 6 weeks to issue the PO. Founder misses the quarter and the forecast is wrong.
- **Undermanaged escalation.** A step stalls with no owner; days become weeks; the deal slips a quarter. The founder was polite when she should have been persistent.

The remedy: paper process is mapped and managed with the same rigor as discovery and demo. The champion and (increasingly, as the deal moves) the buyer are on the hook for driving internal steps; the founder pushes weekly and does not accept "we're working on it" as a status without a specific date.

### The commercial terms that matter most at SEED

Legal will negotiate every term in the MSA. A few terms carry disproportionate weight at SEED and warrant the founder's specific attention:

- **Auto-renewal + notice period.** Default 12-month term with auto-renewal and 60-day notice is standard. Longer notice periods (90-120 days) benefit the vendor at renewal negotiation; shorter (30 days) benefit the customer. Aggressive customers push for termination-for-convenience with 30-day notice, which converts an annual contract into an effective monthly one. Push back.
- **Termination for convenience.** A right to terminate without cause. Aggressive customers push for it; it is a real ARR reduction. If granted, price for it (5-10% higher ACV as a hedge).
- **SLA credits.** Uptime commitments with service credits for failures. At SEED, offering 99.5% or 99.9% is standard; offering 99.99% is a real operational commitment the vendor may not be able to meet. Match the SLA to actual operational capability.
- **Liability cap.** Vendor's maximum exposure on damages. Standard cap is 1x-2x annual fees; enterprise buyers push for 3x or higher, or uncapped. Uncapped liability is a company-existential risk; hold the line at 1-2x with rare exceptions.
- **Indemnification scope.** Vendor indemnifies against IP infringement (standard); customer indemnifies against use-of-data violations (standard, often forgotten). Both sides usually.
- **Data processing addendum (DPA).** GDPR compliance for European customers, similar for CCPA / other US state laws. Standard DPA templates exist; use one. Reviewing every DPA from scratch is a founder-time trap.
- **Auto-renewal price escalator.** Some vendors bake a 5-8% annual escalator into the renewal clause. Reasonable at scale; unusual at SEED (customers push back hard).

Founders without legal counsel should engage a startup lawyer for the first 3-5 MSAs, learn the standard playbook, and then handle boilerplate deals themselves. The first-lawyer investment (typically $2-5K per MSA) pays back many times over on subsequent deals.

### The say-no rehearsal

The four anti-patterns each have a rehearsed "say no" script the founder can deliver in the moment. Rehearsal matters — under real pressure the founder will default to yes unless the no is muscle memory.

- **Deep discount refusal**: "I hear you on the price. Our rate-card price for this tier is $12K/year — we can move to $10K if you're signing a 24-month contract [reason coded: MULTIYEAR]. Below that, we'd be treating our other customers unfairly and setting a precedent I'd have to honor. Would the multi-year work for you, or should we look at a different tier?"
- **Feature-promise refusal**: "That's a real requirement I understand. Honestly — that feature is on our roadmap but not in the next 6 months. Rather than promise a ship date I won't hit, let me suggest two options: sign now for the current scope and I'll flag your account when we do ship it; or hold off and I'll reach back out when it's shipping. Which works for you?"
- **Non-ICP-deal refusal**: "Being honest — I don't think we're the right fit for what you're trying to do. We're built specifically for [ICP description]; your team is different in [specific way]. Rather than sell you something you'd probably regret in 6 months, I'd point you at [alternative]. Happy to make an intro."
- **Custom-scope refusal**: "That custom [integration / deployment / SLA] is possible but it's outside our standard scope. To do it we'd need to add [X% / $Y one-time / different tier]; it's not because we're being difficult, it's because the ongoing engineering / operational cost is real. Does that work for the budget, or should we look at a different shape?"

The scripts do three things. First, they *give the founder language* — under pressure, having pre-loaded language is what enables the no. Second, they *offer an alternative* — every no is paired with a legitimate yes-shape, which keeps the conversation open. Third, they *code the reason* — the founder's post-call notes record the moment, which builds pattern data for pricing / product / positioning feedback.

### The healthy discount patterns — when yes is the right answer

Not every discount is unhealthy. Three patterns of discounting are strategically sound and should be pre-authorised in the rate card:

- **Multi-year for cash certainty.** 10-15% discount for a 24-month contract, 15-20% for 36-month. The trade is real: the customer commits, the vendor gets cash and revenue predictability. Both sides win.
- **Logo / reference for asymmetric value.** A high-visibility logo (a customer whose name will win the vendor 10x more accounts through peer credibility) gets a 15-20% discount in exchange for a case-study commitment, a reference commitment (2-3 references per quarter), and a logo-usage right. The trade is real; price the reference commitment into the contract.
- **Time-bounded promotional launch.** A launch quarter or a specific product-release moment — 10-15% off for signing in the promotion window, with a hard end date. Reasonable if used sparingly; degrades to always-discount if used every quarter.

Each is a *strategic discount* with a defensible reason. The reason gets logged. The pattern of strategic discounts (30-40% of deals with a rate-card discount is normal; 80% is a pricing signal from mod-106) is what Chapter 7's monthly review monitors.

## Concrete example — Loomly's Q3 close and a resisted anti-pattern

Continuing the Acme deal. Post-demo, Jane sends the proposal within 48 hours.

**Proposal v1** — Loomly Growth tier, $12,000/year, quarterly billing, 12-month contract, 30-day trial clause, standard MSA with 60-day auto-renewal notice, SLA 99.9%, liability cap 1x annual fees. Close plan: redlines by day 14, security review by day 21, CFO sign-off by day 28, countersign by day 35.

**Redline round 1** (day 12). Acme's legal returns: (1) request for termination-for-convenience with 30-day notice; (2) request for extended SLA to 99.95% with 5% credit tier; (3) push for annual billing rather than quarterly.

Jane's responses:

- Termination-for-convenience: **holds the line** — "we don't offer TFC as standard; we offer a 30-day trial that turns off if it doesn't work for you." Language rehearsed. Not granted.
- SLA to 99.95%: **negotiates** — offers 99.9% SLA with credit clause, matches internal operational reality. Acme accepts the 99.9%.
- Annual billing: **grants** — annual up-front billing is a cash-timing win for Loomly, and the price stays at $12K. Chose to bundle a 5% "annual-payment discount" to $11.4K in exchange, coded PROMO — deliberate.

**Security review** (day 18). Loomly's SOC 2 report + DPA sent under NDA. Acme security clears in 6 days. Ahead of plan.

**Anti-pattern near-miss** (day 22). Ramesh comes back — CFO wants a 20% discount to sign this quarter. This is the deep-discount temptation. Jane pauses. The rate-card discretion is 15%; 20% is a discretion violation. She writes the rationale in her CRM: "Q3 end, deal would move to Q4 if we hold — CFO is pressuring on quarter-end. Not a multi-year or logo case." She holds the line. Language:

> "Ramesh — I hear the ask. Our best price at this tier is what we already discussed ($11.4K annual with the payment discount). We can go to 15% off if you can sign a 24-month contract; the reason is straightforward — it's the discount we can defend across all our customers. If the CFO can move to 24 months at $10.2K/year, we're done; otherwise I'd rather hold and revisit in Q4 than set a precedent I can't defend to our board."

Ramesh brings it back to the CFO. The CFO agrees to the 24-month path at $10.2K/year. Deal closes on day 34 at $20.4K TCV, coded MULTIYEAR, well within the rate card. Jane logs the exchange for the pattern file.

**Contrast — what would have happened at 20% single-year.** The deal closes at $9.6K/year with a "one-time" reason code. Two months later, another buyer in the same segment asks for the same 20%; Jane's own precedent obliges. Six months later, the blended ACV in the segment has dropped 15% and nobody can name why. The one deal did not just cost 20% on this contract — it cost 15% on the next dozen. The multi-year alternative was strictly better for the business.

**Contrast — what would have happened if Jane had said yes to a custom scope request.** Suppose the CFO instead asked for a data-residency arrangement (Loomly hosts in EU only for Acme). Loomly's product is US-hosted; supporting EU-only for a single account requires a new deployment topology, ongoing operational overhead, and possibly a new SOC 2 audit for EU compliance. The single deal is $10K/year; the cost of supporting the exception is easily $50-100K/year in engineering + ops + legal. Anti-pattern 4 — Jane holds the line: "we don't support EU-only hosting today; we may in Q4 when we have a European customer cohort. Rather than promise it now, let's revisit at that time or defer this deal." Deal moves to nurture. Painful in the moment; correct in the year.

## Common failure patterns

- **The hedged-proposal trap.** Proposal has "starting price" and "typical range" language. Buyer treats the starting price as the ceiling and negotiates down. Fix: proposal is the actual deal; no hedging.
- **The no-rate-card trap.** Founder quotes different prices to different customers with no coded reason. Renewal negotiations chaos; win/loss analysis unreadable. Fix: written rate card, coded discount reasons, exception log.
- **The deep-discount-to-close trap.** 30-50% discount to close today's deal. Trains pipeline to expect the discount; degrades renewals. Fix: rate-card discipline; discount only against coded reasons; walk away rather than violate.
- **The feature-promise trap.** "Yes we'll build that next quarter." Roadmap distortion; trust collapse if late. Fix: honest disqualification, contractual promise with real dates, or scope adjustment.
- **The non-ICP-deal-to-hit-number trap.** Quarter-end pressure closes deals outside ICP. Support burden 3-5x, churn 2-3x, product-pull distortion. Fix: honest disqualification and miss the quarter.
- **The custom-scope-favour trap.** Custom integration / deployment / SLA / legal term granted as a favour. Ongoing operational cost that outlasts the deal. Fix: price the exception (X% premium, $Y one-time fee, different tier) or refuse.
- **The paper-process-underestimation trap.** Founder forecasts a 4-week close; procurement takes 6 weeks. Fix: map the paper process at proposal, add procurement duration to the forecast, start security review at demo not at proposal.
- **The uncapped-liability trap.** Founder agrees to uncapped liability or 5x-10x liability cap to close a deal. Company-existential exposure. Fix: hold at 1x-2x annual fees; consult a lawyer for exceptions.
- **The auto-renewal-carelessness trap.** 90-120 day notice on auto-renewal or aggressive termination clauses agreed without thinking. Renewal negotiation surprises. Fix: 60-day notice as default; termination-for-convenience priced or refused.
- **The DPA-from-scratch trap.** Founder reviews every DPA line-by-line. Founder-time trap. Fix: standard DPA template + lawyer review of first 3-5; delegate boilerplate.
- **The no-close-plan-in-writing trap.** Close plan lives in the founder's head. Steps slip unnoticed. Fix: written close plan in proposal, shared with champion, updated weekly.
- **The no-exception-log trap.** Discretion-violating discounts happen "one-time." Three "one-time" 40% discounts in a quarter go un-noticed. Fix: exception log rolled up monthly; three-strikes is a pricing signal.
- **The lack-of-say-no-rehearsal trap.** Founder has never rehearsed language for refusing a discount / feature / scope request. Under pressure, defaults to yes. Fix: memorise the four say-no scripts; practice them out loud.
- **The healthy-discount-avoidance trap.** Founder refuses all discounts including multi-year and logo — leaves strategic value on the table. Fix: rate card includes healthy discount patterns (multi-year, logo, promo) with pre-authorised bands.

## Summary

- The **proposal** locks scope, price, commercial terms, and close plan. It is the deal the founder actually wants — no hedging. Discounting from a defended proposal is a strategic choice; discounting from a hedged proposal is default.
- The **proposal template** ships as a 2-3-page document with six sections: context, scope, price, implementation, close plan, terms. Versioned per customer; every version dated.
- The **rate card + discount ladder** replaces "let me see what I can do" pricing. Written, internal, with pre-authorised discretion bands (typically ≤ 15% approved, 16-25% with coded reason, > 25% requires deliberate exception).
- **Four founder-led-sales anti-patterns** — deep-discounting to close, feature-promising, taking non-ICP deals to hit a number, saying yes to custom scope. Each has a specific dynamic and a specific say-no script the founder rehearses.
- **Healthy discount patterns** — multi-year for cash certainty (10-15% off 24 months, 15-20% off 36), logo / reference for asymmetric value (15-20% with case-study + reference commitments), time-bounded promotional launch. Each is coded and defensible.
- The **close plan** — redline round 1, vendor response, security review, economic-buyer sign-off, final redlines, PO / invoice, countersign + kickoff — has an owner, a target date, and a status per step. Slip triggers escalation.
- The **paper process** (MEDDPICC's P) is the enterprise-scale close plan. Underestimated procurement duration is the single most common enterprise-forecast miss.
- **Commercial terms that matter most at SEED**: auto-renewal notice (60-day default), termination-for-convenience (price if granted), SLA credits (match operational capability), liability cap (1x-2x fees), DPA (standard template), auto-renewal escalator (unusual at SEED).
- The **say-no rehearsal** — memorised language for each anti-pattern — is what enables the no under real pressure. Every no offers a legitimate alternative and codes the reason.
- Every close, healthy or unhealthy, produces **learnings for the win/loss pattern** (Chapter 7). The pattern is what Chapter 8's first-hire readiness check reads to decide whether the motion is repeatable enough to hand off.
- Chapter 7 picks up the **CRM hygiene and honest forecast** discipline that turns 20-30 individual deals into a legible operating instrument.
