# Expansion Motion Design

## Motivation

Chapter 2 named **expansion ARR** as the "N" in NRR — the specific revenue that lifts the roll-up above the GRR floor and pushes NRR above 100%. This chapter is where you *design the motion that produces it*.

The common founder pattern is to treat expansion as a customer-success afterthought — "our CSMs will figure out upgrades organically" — or to conflate expansion with retention ("if we just retain customers, they'll grow on their own"). Both are wrong. **Expansion is a first-order revenue lever with its own instrumentation, its own qualifying signals, its own playbooks, and its own owner.** Companies that produce NRR ≥ 120% did not get there by accident; they designed the surface, the pricing metric, and the trigger events, and they resourced the motion the same way they resourced new-logo acquisition.

This chapter unpacks the three expansion primitives (seat, cross-sell, usage-based upgrade), shows how the mod-106 pricing metric constrains what is available, walks the qualifying-signal and playbook layer, and names the ownership question that determines whether expansion is a real motion or a wish.

## Core concepts

### The three expansion primitives

Every expansion motion in the modern SaaS canon reduces to one (or a composition) of three primitives. Pick the ones the pricing model and product surface support; do not try to run all three at pre-Series-A scale.

**1. Seat expansion.** More users of the same product inside the same account pay more.

- **Applies when:** pricing metric is per-seat / per-user / per-active-user, and the product's value scales with number of users inside the customer's team.
- **Motion:** invite-driven virality inside the account (individual contributor invites their teammate); admin-driven seat provisioning; land-and-expand outbound to peer teams inside the same company.
- **Signal-of-fit:** users invite teammates unprompted; account seat count grows without a rep touching the deal; the product has explicit multi-user features (mentions, assignments, shared workspaces).
- **Examples in the practitioner canon:** Slack (per-active-user), Notion (per-seat), Figma (per-editor). Each is a per-seat metric with in-product invite loops that make seat expansion nearly organic. ([Reforge — Growth Loops](https://www.reforge.com/blog/growth-loops); [Lenny Rachitsky — writeups on PLG expansion motions](https://www.lennysnewsletter.com/)).

**2. Usage-based upgrade.** More usage of the same product surface pays more.

- **Applies when:** pricing metric is usage-metered — API calls, GB stored, events processed, transactions, GPU hours, seats × usage — and the customer's usage scales as the product embeds deeper in their workflow.
- **Motion:** in-product usage dashboards that show consumption approaching plan limits; automated tier upgrades on plan-limit breach; sales-assisted commit expansion at renewal time.
- **Signal-of-fit:** usage per customer grows month-over-month independent of seat count; a large fraction of your active customers are consistently in the top usage decile of their tier; overage revenue is a meaningful fraction of subscription revenue.
- **Examples in the practitioner canon:** Snowflake (compute-hour metric), Twilio (message / call), Stripe (transaction fee), Datadog (host / metric). The public-market NRR bands of these companies (typically 120%+ in growth-phase reporting per [Bessemer — State of the Cloud](https://www.bvp.com/atlas)) are the archetype for what a usage-based expansion motion produces at scale.

**3. Cross-sell into adjacent product surface.** More of the customer's problem-space is served by additional products or modules.

- **Applies when:** the company has (or can build) a second product line that solves an adjacent problem for the same buyer, and the second product has meaningful value to a customer who already owns the first.
- **Motion:** package-tier upgrades (Basic → Pro → Enterprise); explicit second-SKU sales cycle (usually AE-driven); bundle discounting; integrated-experience nudges inside the primary product.
- **Signal-of-fit:** existing customers routinely ask for or wire up the adjacent capability from a competitor; sales conversations at renewal open the door to a second-workflow conversation; the buyer's economic decision-maker owns both problems.
- **Examples in the practitioner canon:** HubSpot's Sales/Marketing/Service Hubs (three products sold to overlapping buyers), Atlassian's Jira + Confluence + Bitbucket bundle, Salesforce's Sales Cloud + Service Cloud + Marketing Cloud, Zoom's meetings → phone → rooms → events product family.

**Composition.** Real motions often layer two of the three. Slack's motion is majority seat expansion (per-active-user) with modest cross-sell (Enterprise Grid tier features, Slack Connect). Snowflake is majority usage expansion (compute) with cross-sell (Snowpark, Cortex). At Series-A, **pick one primary primitive and instrument it end-to-end** before layering a second. Trying all three at seed scale produces three shallow motions, none of which produces measurable NRR lift.

### The pricing metric constrains what is available

Chapter 3 depends on mod-106 Chapter 5's **pricing metric** choice. The metric determines which primitives are even available.

| Pricing metric | Seat expansion | Usage upgrade | Cross-sell |
|---|---|---|---|
| **Flat per-account subscription** | Not available | Not available | Only available lever |
| **Per-seat / per-user** | Primary lever | Not available | Available |
| **Usage-metered (per API call / GB / txn)** | Only if layered on top of seats | Primary lever | Available |
| **Hybrid (seat + usage)** | Primary or secondary | Primary or secondary | Available |
| **Percentage of value transacted (e.g. Stripe)** | Not applicable | Effectively primary lever | Available |

**Implication.** A team that priced flat per-account at mod-106 and now wants to hit NRR ≥ 100% has exactly one primitive available (cross-sell) — and building a second product line is a large multi-quarter investment. The natural expansion motions (seat and usage) are unavailable because the pricing metric does not tick when the customer grows their use.

This is one of the most common self-inflicted expansion problems: a flat pricing model at mod-106 that produces no expansion surface at mod-109. If the team is at Series-A with a flat-subscription pricing model and no cross-sell product, the honest scorecard read is *"NRR is structurally capped at 100% until we re-price"* — and re-pricing an existing book is expensive and disruptive. **The right time to solve the mod-109 expansion motion is at mod-106, when the pricing metric is chosen.** This chapter's job is to make the constraint legible before it hardens.

### The qualifying-signal layer — who is ready to expand

An expansion motion needs a qualifying signal layer analogous to the mod-104 ICP scoring or the mod-107 PQL (product-qualified lead) definition. The signal identifies *which accounts are ripe for which expansion primitive*, and it feeds the trigger (in-product nudge, CSM outreach, AE upsell touch).

For each primitive, the signal is different:

**Seat expansion qualifying signals:**

- Number of active users approaching seat cap on the current plan.
- New users being invited faster than they can be onboarded (indicates strong pull inside the account).
- Users mentioned or shared with but not yet in the account (invitees who did not convert — a specific expansion opportunity).
- Cross-departmental adoption pattern (users from a second BU appearing in the account).

**Usage-based upgrade qualifying signals:**

- Consumption approaching the plan-tier ceiling (e.g., 80% of monthly usage cap for two consecutive months).
- Overage patterns — customers paying overage rather than upgrading to a tier that covers their usage.
- Sudden usage growth (a "surge event" — an integration went live, a new use case went into production).
- Concentrated usage in features gated behind a higher tier.

**Cross-sell qualifying signals:**

- Explicit customer request for a capability the adjacent product provides.
- Integration with a competing tool for the adjacent capability (visible in tech-graph tools like BuiltWith / HG Insights, or via support tickets).
- Champion score / relationship strength — the mod-104 champion role is present and highly engaged.
- Renewal cycle timing — cross-sell conversations land best 60–120 days before renewal.

The signal layer is **instrumented, not tribal**. If you cannot compute the signal from your product-usage data + CRM data automatically, you cannot run the motion at scale — you have a founder-CSM heuristic that will not survive the first three CSM hires.

### The trigger and playbook — what happens when the signal fires

Each qualifying signal triggers a specific playbook. Three archetypes, roughly ordered by ACV band:

**In-product upgrade prompt (self-serve).** Cheapest, fastest, correct for low-ACV PLG motions.

- User hits a plan limit → in-product modal offers upgrade → self-serve payment → new tier active in minutes.
- Instrumented in the product; no human touch required.
- Correct for individual and small-team PLG products where the upgrade decision is under $500/mo.

**CSM-assisted expansion touch.** Correct for mid-market accounts where the buyer wants a human conversation.

- Signal fires → CSM gets a task in the CS tool → CSM books a call with the account's champion → conversation walks the usage data and proposes the upgrade → deal booked with a light-touch order form.
- Instrumented as a CS workflow (Gainsight, Vitally, Catalyst, or a manual CRM view) with SLA on time-to-touch after signal fires.

**AE-led upsell / cross-sell cycle.** Correct for enterprise accounts where the second-product decision is a real sales cycle.

- Signal fires → AE takes the account (often the same AE who closed the original deal, sometimes a specialised "expansion AE" or "customer-success AE") → discovery, demo, proposal, close on the second product or expanded contract → new contract booked, sometimes co-termed with the original.
- Instrumented as a CRM opportunity in a distinct "Expansion" pipeline separate from new-logo pipeline; forecasted separately.

Every real expansion motion has an owner per playbook. Two failure modes to watch:

- **No owner.** "Expansion is everyone's job" is code for "no one is measured on it." Assign the number to a specific role — Head of CS, Head of Growth, first Expansion AE, or the founder — and hold them to it.
- **Wrong owner.** A CSM whose only comp is renewals will not run cross-sell aggressively; an AE whose only comp is new logos will not run expansion at all. The comp structure has to align with the number. Comp design is a mod-107 / mod-110 topic; the *decision* to align it belongs here.

### Instrumentation — what has to be in the stack

A working expansion motion at Series-A scale requires four data flows connected:

1. **Product usage event stream.** Every user's every value action, cohorted by account. Fed by product instrumentation into a warehouse or analytics tool (Amplitude, Mixpanel, Segment → warehouse). Without this, the qualifying signals are guesses.
2. **Account CRM + subscription state.** Every account's current plan, seat count, usage tier, contract dates, renewal date, primary contact, champion, decision-maker. Salesforce, HubSpot, or the equivalent, kept clean (mod-105 Chapter 7 CRM hygiene rules apply).
3. **Signal computation layer.** A recurring job (nightly or hourly) that reads product usage + CRM, computes the qualifying-signal thresholds per account, and writes back a signal state ("ripe for seat expansion", "ripe for usage upgrade", "ripe for cross-sell", "not ripe"). Implemented in the warehouse (dbt models + reverse-ETL back to CRM) or in a CS platform (Gainsight, Vitally, Catalyst) that supports rules over usage data.
4. **Playbook trigger layer.** Signal state changes fire the right playbook — in-product modal (Pendo / Appcues / built in-house), CSM task creation (Gainsight / Vitally / CRM task), AE opportunity creation (CRM), or a sequenced email cadence (Outreach / Salesloft / marketing automation).

The instrumentation is not optional at Series-A. A founder-run motion that touches expansion opportunities based on the founder's memory of who might be ready does not scale past ~30 accounts. Instrument it before you scale the CSM / AE team, not after.

### Expansion ARR as a separate P&L line — the reporting discipline

The Chapter 2 metric decomposition is the reporting anchor: **New ARR, Expansion ARR, Downgrade ARR, Churned ARR** are the four buckets, and Expansion ARR is a *separate P&L line* that gets forecasted, tracked, and reviewed with the same rigour as new-logo ARR.

Concretely, at Series-A a working expansion motion produces:

- **A monthly Expansion ARR number** decomposed by primitive (seat / usage / cross-sell) and by owner.
- **A rolling Expansion pipeline forecast** — dollar-weighted, with stage transitions and probability weights just like new-logo pipeline.
- **A weekly review** — the CS / expansion team reads the pipeline the same way the AE team reads new-logo pipeline, with a next-step SLA on every open opportunity.
- **A per-account expansion timeline** — the CRM shows when an account was last touched for expansion, what the current stage is, and what the next trigger date is.

Where the reporting most often breaks is **at the boundary with customer success**. If Expansion ARR is buried in a "renewals" number that also contains base renewal, it disappears; if it is booked as new ARR because the second-product deal was managed by a new-logo AE, it double-counts. The metric integrity in Chapter 2 requires the reporting layer here to be clean.

## Concrete example — the code-review-tool expansion motion

Return to the code-review-tool book from Chapter 2 — NRR = 110%, GRR = 78%, per-seat pricing, one cross-sell tier ("Premium Security") introduced six months ago.

**Primitives available (per pricing metric):** per-seat metric enables seat expansion (primary); the Premium Security tier enables tier upsell / cross-sell (secondary); no usage-based metric (would require re-pricing).

**Primary primitive: seat expansion.**

- **Qualifying signals.**
  - Team's active-user count > 80% of seat cap in the past two weeks (upgrade trigger).
  - Team invited a new user in the past week and the invitee has been active for ≥ 3 days (organic expansion signal — the invite is not a curiosity click).
  - Team's mentions to non-users are non-zero (indicates workflow pull for missing users).
- **Playbook.** In-product modal on user #N-of-cap creation offering seat upgrade at prorated price. Self-serve for mid-market; CS-assisted touch for enterprise. Escalate to CSM after 7 days if no self-serve conversion.
- **Owner.** Head of CS, comp'd on Expansion ARR from seats. Instrumented in the CS tool with a "seat-cap alert" workflow.

**Secondary primitive: cross-sell to Premium Security.**

- **Qualifying signals.**
  - Team on the base tier has enabled the "SSO integration" (a low-tier feature that indicates security-conscious buyer).
  - Team has a security-role user (from title in enrichment) in the account.
  - Team is 60–120 days pre-renewal.
- **Playbook.** AE-led. CSM identifies the qualified account and hands to an "Expansion AE" (currently the founder, first hire post-Series-A). Discovery call, security-focused demo, proposal, close. Contract co-termed with base subscription.
- **Owner.** Founder (transitioning to first Expansion AE hire in the next two quarters).

**Excluded primitive: usage-based upgrade.**

- Not available — pricing metric is per-seat, not usage-metered. Explicitly not attempting. If NRR needs to expand further, the mod-109 → mod-106 conversation is *"do we add a usage-metered layer for API access to the code-review data?"* — but that is a next-year decision, not a next-quarter one.

**Instrumentation.**

- Product events (auto-nudge fired, PR reviewed, mention, invite) → warehouse (BigQuery, dbt).
- CRM (Salesforce) with per-account plan, seat count, contract dates, renewal date.
- Reverse-ETL job nightly writes "seat-cap alert" and "cross-sell ripe" flags back to Salesforce and CS tool.
- In-product modal implemented in the product (custom, ~1 sprint of work).
- CS tool workflow triggers CSM task on cross-sell-ripe flag with 48-hour SLA.

**Reporting.**

- Monthly Expansion ARR = $X from seats + $Y from Premium Security. Reviewed in the same monthly cadence as New ARR.
- Rolling 90-day Expansion pipeline in a dedicated CRM view; forecast weight against a Chapter-2 dollar-weighted model.
- Owner scorecard (CS Head, founder) updated monthly with Expansion ARR attained vs. plan.

That is a working expansion motion. It is designed, instrumented, resourced, and reported — and the pieces that are missing (Expansion AE hire, usage-metered pricing layer) are named and dated rather than being handwaved.

## Common failure patterns

- **"Expansion happens organically if the product is good."** True for a small fraction of consumer viral products; false for essentially every B2B motion. Design the motion.
- **No owner.** Nobody is comp'd on expansion; the number is whatever falls out. Assign the number.
- **CSM comp'd only on renewals.** CSMs do not push expansion; NRR stalls at GRR + a small organic uplift. Fix comp.
- **Running all three primitives at seed scale.** Three shallow motions produce no measurable lift. Pick one primary; instrument end-to-end; then layer a second.
- **Pricing metric does not support any primitive except cross-sell.** Structurally cap NRR at 100% + cross-sell rate. Named at Chapter 2; fixed by re-pricing (mod-106).
- **Expansion ARR buried in "renewals."** The metric disappears; the motion is not managed. Break out.
- **In-product upgrade prompt implemented, no CSM path for accounts too big for self-serve.** Enterprise buyers do not click self-serve upgrade modals. Escalation path required.
- **Signal layer is tribal knowledge.** Founder or Head of CS remembers who to touch; does not scale past 30 accounts. Instrument the signal in the warehouse or CS tool.
- **Expansion pipeline not forecasted.** Board pack has new-logo forecast but not expansion; expansion misses go unexplained. Forecast both.
- **Cross-sell cycle managed by the same AE who closed the original deal, with no attribution mechanism.** The AE has no incentive to prioritise cross-sell over their next new-logo deal. Attribution / SPIF / dedicated Expansion AE role solves this.

## Summary

- **Expansion is a first-order revenue lever with its own instrumentation, playbooks, and owner.** Not a CS afterthought.
- **Three primitives — seat expansion, usage-based upgrade, cross-sell.** Pick one primary at Series-A; layer a second only after the first is instrumented and producing measurable ARR.
- **The pricing metric constrains what is available.** Flat pricing produces only cross-sell; per-seat produces seat + cross-sell; usage-metered enables the full range. The mod-106 pricing metric choice is a mod-109 constraint.
- **Qualifying signal + playbook trigger.** Instrumented signals (from product usage + CRM) fire specific playbooks (in-product modal, CSM touch, AE cycle) with SLAs and owners.
- **Instrumentation is not optional at Series-A.** Product events → warehouse → signal computation → CRM / CS tool → playbook trigger.
- **Expansion ARR is a separate P&L line** with its own forecast, its own pipeline, and its own owner comp'd on the number.
- **Common failures are ownership and design failures** — no owner, wrong comp, wrong primitive for the pricing metric, tribal signals. All are cheap to fix once named.
