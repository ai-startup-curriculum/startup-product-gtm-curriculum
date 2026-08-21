# Pricing Metric vs. Price Point — The Metric Is the Strategy, the Number Tests

## Motivation

A pricing decision has two parts, and they are commonly confused.

The **pricing metric** is *what you charge per unit of* — per seat, per transaction, per GB stored, per message sent, per workflow run, per event, per API call, per active user, per model-inference, per document processed. It answers "along what axis does the customer's bill scale as she uses more of the product?"

The **price point** is the *number* attached to that metric — $10 per seat / month, $0.001 per event, $500 per workflow-run.

Founders spend most of their pricing energy debating price points ("should it be $99 or $149?") and almost none on the metric ("should we charge per seat, per event, or per outcome?"). This inverts the actual strategic weight. **The metric is the strategic choice; the number tests.** A wrong number is annoying and fixable in a quarter. A wrong metric shapes the sales motion, the customer's growth curve, the incentive alignment, and — because switching pricing metrics is dramatically harder than adjusting prices — the wrong metric locks in wrong incentives for years.

The failure mode this chapter exists to catch: **the founder picks the pricing metric by copying whichever category leader she happens to know about ("Slack charges per seat, so we'll charge per seat") without checking whether that metric aligns with her product's value creation, her buyer's growth curve, or her sales motion — and then rebuilds the product's meterin, billing, and quote-to-cash infrastructure 18 months later when she finally realises the metric was wrong.**

This chapter fixes:

- The strategic weight of the pricing metric — why it matters more than the price point.
- The primary metric families (seat, usage, outcome, hybrid) and their trade-offs.
- The four alignment tests a metric has to pass before it's the right metric.
- The relationship between the metric and the pricing tiers from Chapter 3.
- The signals that say "you picked the wrong metric" and what to do about it.

Chapter 5 handles experiments that test *price points* along a chosen metric. This chapter is about picking the metric — the change that is much harder to undo.

## Core concepts

### Why the metric matters more than the number

Consider two hypothetical pricing structures for a hypothetical monitoring SaaS product:

- **Structure A:** $50 per seat / month. A team of 20 pays $1000 / month regardless of how much monitoring they do.
- **Structure B:** $0.001 per event ingested. A team of 20 that ingests 1M events / month pays $1000; a team of 20 that ingests 10M events pays $10,000.

Both structures produce $1000 / month for the reference customer. But:

- **The customer's growth curve is different.** Under seat pricing, the vendor grows with headcount (slowly, in fits and starts). Under event pricing, the vendor grows with usage (organically, as the customer's business grows).
- **The sales conversation is different.** Seat pricing gets negotiated once — "how many seats do you need." Event pricing has to explain the metric, help the buyer estimate usage, and defend the per-unit price. The buyer's economic buyer (usually a CFO for usage-priced tools) is different from the seat-pricing buyer (usually the champion who owns headcount).
- **The customer's incentives are different.** Under seat pricing, the customer's incentive is to *minimise seats* (only give access to people who really need it) and to *maximise usage per seat* (get every feature out of every user). Under event pricing, the customer's incentive is to *minimise events* — turn off noisy sources, sample down, delete data — which is directly hostile to the value the vendor creates.
- **The churn risk is different.** Seat-priced customers churn when they lay off users; event-priced customers churn when they optimise event volume down. The two churn events look different in the retention curve and require different intervention playbooks.
- **The switching cost of the metric itself is high.** Changing from seat to event (or vice versa) requires re-writing every existing contract, rebuilding metering + billing, retraining sales, reworking the pricing page, and communicating with every existing customer. In practice most companies change price points 3-5× before they ever change the metric.

The metric is the *shape* of the pricing structure; the price point is just the height. Changing the height is a spreadsheet decision; changing the shape is a company-wide project.

### The primary metric families

Four metric families cover almost all B2B SaaS pricing. Each has characteristic strengths, weaknesses, and best-fit sales motions.

**Family 1 — Per-seat / per-user pricing.**

- **What you charge for:** every human who has a login to the product.
- **Standard examples:** Slack, Notion, Figma, Salesforce, HubSpot, Linear.
- **Strengths:** buyer easily estimates cost (she knows headcount); predictable revenue for the vendor; simple to explain and negotiate; billing/quote is trivial; aligns with buyer's HR growth curve.
- **Weaknesses:** decouples price from value in products where value doesn't scale with users (a 5-user team getting 100× the value of a 5-user team pays the same); creates the "shadow user" workaround (customers share logins); does not capture usage-driven growth in the product.
- **Best fit:** collaboration tools, communication tools, workflow apps where each user is an independent workspace-consumer; sales motions where headcount is the buyer's natural growth vector.

**Family 2 — Usage / consumption pricing.**

- **What you charge for:** units of a metered event — API calls, events ingested, GB stored, messages sent, minutes processed, model inferences, workflow-runs, records synced.
- **Standard examples:** AWS (everything), Twilio (messages), Stripe (transactions), Snowflake (compute), Vercel (serverless invocations), Datadog (hosts and metrics), Segment (events tracked), OpenAI API (tokens).
- **Strengths:** aligns price to value delivered when value scales with usage; low friction to start (buyer isn't committing to a big number); vendor grows with customer's business automatically; supports usage-based expansion without a sales conversation.
- **Weaknesses:** unpredictable bills (buyers get surprise invoices); complex to model; economic buyer often different from champion; incentive to minimise usage cuts into value; requires accurate metering infrastructure from day 1; forecasting revenue is harder for the vendor.
- **Best fit:** infrastructure products, data-flow products, AI / model API products, transaction-processing products; product-led motions where the customer's growth is the pricing driver.

**Family 3 — Value / outcome pricing.**

- **What you charge for:** a specific business outcome — appointments booked, leads generated, tickets resolved, incidents mitigated, dollars processed, hires made.
- **Standard examples:** Salesforce Einstein (some SKUs), Gong (per rep with attribution guarantees), some outcomes-based services (marketing agencies, sales-development-as-a-service), performance-fee SaaS in specific verticals.
- **Strengths:** perfect value-price alignment; sales conversation is directly the ROI conversation; premium pricing power when the outcome is high-value.
- **Weaknesses:** attribution is hard (was the outcome from the product, or from something else the buyer did?); measurement infrastructure is complex; buyer disputes over outcome counts are frequent; requires the vendor to bear execution risk; not compatible with self-serve.
- **Best fit:** high-ACV enterprise deals where the outcome is unambiguous and jointly measurable; verticals with established outcome-attribution norms (some parts of marketing, some parts of financial services).

**Family 4 — Hybrid metrics.**

- **What you charge for:** a combination — commonly a *seat-based floor* plus *usage-based expansion*, or a *tier subscription* plus *usage overage*, or *seat * usage tier*.
- **Standard examples:** most enterprise SaaS at scale (Salesforce base + Einstein usage; HubSpot seats + marketing contacts; Notion seats + AI usage add-on).
- **Strengths:** captures the reliability of subscription with the expansion of usage; different metrics can align with different personas (seat = champion's growth, usage = economic buyer's ROI); reduces the "surprise bill" risk of pure usage while preserving usage-driven expansion.
- **Weaknesses:** more complex to explain; the buyer has to reason about two dimensions; billing infrastructure is more complex; can feel gimmicky if the two dimensions don't align with the buyer's natural growth vectors.
- **Best fit:** established mid-market and enterprise SaaS where a pure metric is insufficient; specifically, products where subscription commitment is important for the vendor's revenue predictability but expansion is important for growth.

### The four alignment tests — how to pick the right metric

A candidate pricing metric has to pass four tests to be the right metric for the product.

**Test 1 — Does it scale with the value the customer captures?** If the customer's value from the product doubles, the customer's bill should approximately double. If a metric would leave the bill flat while the customer captures 10× the value (or would inflate the bill while the value is flat), the metric is misaligned.

- Loomly's value equation (Chapter 2) is cycle-time recovery × PRs / year × cost of delay per day. PRs / year scales roughly with repos and with team velocity. **Per-repo** scales with value (a customer with 3× the repos gets roughly 3× the cycle-time recovery). **Per-seat** would scale with the wrong axis (headcount, not repo count).

**Test 2 — Does the customer's natural growth vector match the metric?** As the customer's business grows, the metric should grow with it — organically, without a sales conversation for every increment. This is the "expansion built into the pricing" property.

- Slack per-seat expansion works because customers grow by hiring; the metric moves as HR moves.
- Twilio per-message expansion works because customers grow by messaging more; the metric moves as the customer's usage moves.
- A "per-workflow" metric for a product whose customer uses the same 3 workflows forever is misaligned — the customer's growth doesn't move the metric.

**Test 3 — Can the customer estimate her cost without doing months of pilot work?** If a buyer cannot get to a defensible estimate of her monthly bill within 15 minutes of understanding the metric, the metric has a sales-friction problem. Buyers who cannot predict their bill either don't buy (deal killer) or buy small and stall (revenue drag).

- Per-seat is trivially estimable — the buyer knows her headcount.
- Per-repo is estimable — the buyer can count repos.
- Per-event is often *not* estimable at seat time — the buyer has no clue how many events her system emits. This is why event-priced products have to invest heavily in "here's what to expect" calculators and forecast tooling.

**Test 4 — Does the metric align the vendor's incentive with the customer's success?** The metric should reward the vendor for making the customer *use the product more*, not for making the customer *minimise usage to control the bill*.

- Per-seat rewards the vendor for expanding to more users (the customer's success = more users = more revenue).
- Per-event rewards the vendor for *ingesting more events* — but the customer's success may involve *reducing events* through better telemetry. This is a classic misalignment; several observability vendors have publicly restructured pricing to address it.
- Per-outcome rewards the vendor for delivering more outcomes — the strongest incentive alignment when attribution works.

A metric that passes all four tests is a candidate. A metric that fails one is workable with mitigation (e.g. a metric that fails Test 3 needs cost calculators and predictable-bill tools). A metric that fails two or more is probably the wrong metric — search for a better one before pricing against it.

### Picking the metric from the value equation

The most reliable way to derive the pricing metric is to look at the value equation from Chapter 2 and identify the *variable* that most strongly drives the value.

If the value equation is:

```
Value = (baseline metric - improved metric) × cost per unit × frequency
```

then the pricing metric should be a proxy for *frequency* — the variable that determines "how much value the customer gets per unit of time."

- **DORA cycle-time SaaS (Loomly):** Value = cycle-time reduction × cost per PR × PRs / year. The frequency variable is **PRs / year**, which proxies for **active repos**. Per-repo is the aligned metric.
- **AI chat SaaS:** Value = query resolved × avoided support-agent-minute × queries / month. The frequency variable is **queries / month**, which is the pricing metric directly.
- **Sales enablement SaaS:** Value = deal accelerated × deal size × deals / quarter. The frequency variable is **deals / quarter**, or its proxy **active sellers**. Per-seat is aligned with per-seller.

When the value equation has multiple frequency variables (both team-size and per-team-usage matter), a hybrid metric (per-seat + per-usage) is often the honest choice.

### Metric selection interacts with the tier composition (Chapter 3)

The pricing metric and the tier composition are two parts of the same decision. The metric is the axis along which price scales *within* each tier; the tier boundary is drawn by features. But the metric choice also constrains tier design:

- **Per-seat metric.** Tiers usually have different *per-seat prices* (Team at $12/seat, Business at $28/seat) plus different feature sets. The tier chosen determines the per-seat price and the feature set; expansion within a tier is by seat count.
- **Usage metric.** Tiers usually have different *usage brackets* (Starter includes 10K events, Team includes 100K, Business includes 1M) plus different feature sets. Expansion within a tier is by usage; if usage exceeds the tier bracket, the customer either upgrades or pays overage.
- **Hybrid metric.** Tiers have both dimensions — feature composition plus per-seat plus usage overage rules. Most complex to explain but most flexible for customer heterogeneity.

The interaction to design against: the tier the customer belongs to should be a natural consequence of her scale, not a source of friction. If the mainstream ICP customer routinely hits the middle-tier usage cap and pays surprise overages, the middle tier's usage bracket is too tight; if she never approaches the cap, the bracket is too loose (revenue on the table).

### The pricing metric page and calculator

For any pricing metric more complex than per-seat, the pricing page needs a **calculator** — an interactive widget that lets the buyer input her expected usage and see a projected bill. This is not optional for consumption pricing; the metric fails Test 3 (estimability) without one.

The calculator should:

- Take **inputs the buyer already knows** — headcount, repos, monthly transactions, or whatever the buyer can source from her own systems in seconds.
- Show a **monthly bill projection** at each tier, with the tier the buyer's inputs land in highlighted.
- Show the **overage cost** for the middle tier if inputs push above its bracket, so the buyer sees the decision to upgrade explicitly.
- Handle **annual vs. monthly billing** and show both, with the annual discount visible.

A buyer who has to email sales to get an estimate of her bill for a self-serve or PLG product will bounce; the calculator is the substitute for the sales rep at the low-friction end of the funnel.

### Signals the pricing metric is wrong

Even a well-chosen metric can prove wrong when it meets the market. Signals to watch:

- **Bill-surprise churn.** Customers churning at renewal because "the bill kept surprising us" — the metric fails Test 3.
- **Anti-usage optimisation.** Customer-success calls that boil down to "help me use less" — the metric fails Test 4.
- **Bill-flat, value-growing.** Customers whose value from the product has 5× while their bill has moved 20% — the metric fails Test 1 (misses expansion).
- **Bill-growing, value-flat.** Customers whose bill has 3× while their perceived value hasn't changed — the metric fails Test 1 (over-charges without value creation).
- **Sales cycles collapse on "how much will it cost me."** Deals dying at the estimation step, before the value slide — the metric is not estimable enough (fails Test 3).
- **Champion-vs-CFO fights over the bill.** The champion loves the product; the CFO doesn't understand the metric or the growth curve; the deal dies in procurement. The metric is not economic-buyer legible.
- **Every enterprise deal comes with a "custom" clause on the metric.** Enterprise buyers insist on modifying the metric (per-user cap, cost floor, cost ceiling). The metric doesn't fit at the top end.

Any one of these signals is worth investigating; two or three in the same quarter suggest a metric change is on the table.

### Changing the metric — how it goes

Changing the pricing metric mid-flight is the hardest change in a company's pricing lifecycle. It involves:

- **Rebuilding metering infrastructure** — the new metric has to be measured accurately for every existing customer starting immediately.
- **Renegotiating every existing contract** — annual contracts under the old metric run until renewal; monthly contracts can be migrated but require notice and communication.
- **Retraining every sales conversation** — the AE has to be able to explain the new metric, defend the change, and translate a customer's old-metric bill into new-metric terms.
- **Rewriting the pricing page and every supporting doc**.
- **Grandfathering (Chapter 5)** — most metric changes preserve existing customers on old terms for at least the current contract period, sometimes longer. This creates complexity: two co-existing pricing systems until the old one has been fully rolled forward.

Because changing the metric is so hard, the calculus should be: pick the right metric *before scale*; when the metric proves wrong, delay the change until the pain of keeping it exceeds the (large) pain of changing it; when you do change it, do it once, well, with a grandfathering policy explicit up front.

Public examples of metric changes that have been widely written about include the shifts in observability and data-warehouse pricing between "per host / per node" and "per event / per usage" — both directions have been tried by major vendors, with mixed reception. The lesson from those cases is not "one direction is right" but "the change is expensive, and the buyers most likely to be angry are the ones you most want to keep."

## Concrete example — Loomly picks the pricing metric

Continuing the running example. Loomly runs the metric-selection exercise before committing to the tier structure from Chapter 3.

**Candidate metrics considered:**

1. **Per-seat (per engineer with access to Loomly).**
2. **Per-repo (per repository monitored).**
3. **Per-scan (per PR-time or per-commit scan).**
4. **Per-outcome (per PR-time reduction hour delivered, measured against baseline).**
5. **Hybrid — per-seat base + per-scan overage.**

**Test 1 (value scaling):**
- Per-seat: weak. A 20-eng team with 200 repos gets much more value than a 20-eng team with 20 repos, but pays the same.
- Per-repo: strong. Repo count is a close proxy for PR volume (which is the value driver).
- Per-scan: strong. Scans directly track the value-creating events.
- Per-outcome: strongest in theory; attribution is hard in practice.
- Hybrid: mixed — depends on the ratio.

**Test 2 (growth vector):**
- Per-seat: matches HR growth, not repo growth. Loomly's customers grow repos faster than they grow engineers (microservices proliferation).
- Per-repo: matches the growth vector directly.
- Per-scan: matches, but scan count also fluctuates with team activity in ways the buyer doesn't want to be billed on (e.g. a hot week of shipping).
- Per-outcome: matches in the abstract; outcomes are lumpy and hard to measure per-month.

**Test 3 (estimability):**
- Per-seat: trivially estimable.
- Per-repo: easily estimable (buyer can count repos in her GitHub org).
- Per-scan: hard to estimate — buyer would need to model expected PR frequency × commits per PR.
- Per-outcome: not estimable pre-purchase.

**Test 4 (incentive alignment):**
- Per-seat: weak — vendor wants more logins; customer wants to gate access.
- Per-repo: aligned — customer's success is more repos being observed; vendor's revenue grows with observability coverage.
- Per-scan: weakly *mis-*aligned — customer's success is more scans catching more dependency issues, but bill fluctuations create pressure to sample down.
- Per-outcome: aligned but requires attribution work Loomly cannot deliver at seed.

**Decision:** Loomly picks **per-repo** as the primary pricing metric. It passes all four tests, aligns with the value equation (cycle-time reduction × PR frequency ≈ per-repo), matches how the buyer's brain thinks about her environment, and doesn't create the incentive-misalignment of per-scan.

**Ancillary metric decisions:**

- **No hybrid.** Loomly considered per-seat + per-repo but rejected: the per-seat dimension would be complexity the buyer doesn't need at this ACV. Revisit at Series B when enterprise deals routinely have both dimensions.
- **Bracket cap** for the Starter tier at 25 repos (Chapter 3), which functions as both a tier boundary and a soft usage cap. Above 25 repos, the customer moves to Team.
- **Calculator** built into the pricing page: buyer enters her org's repo count, sees each tier's estimated bill, sees the upgrade point.
- **Overage policy** documented up front: Team and Business tiers include unlimited repos within the tier; there is no overage. Simplifies the sales conversation and eliminates surprise bills.

**What Loomly explicitly rejects:**

- Copying **per-seat** because Snyk and LinearB use it. Per-seat fails Test 1 for Loomly's value equation and would leave 3-5× ARPU on the table for customers with many repos per engineer.
- Copying **per-scan** because Datadog uses per-event pricing. Per-scan fails Test 4 (creates optimize-to-reduce-scans pressure) and Test 3 (hard to estimate).
- Charging **per-outcome** because it "aligns perfectly." Attribution work is not viable at seed; revisit at Series C with mature cohort measurement.

The founder documents the metric choice in the pricing pack with the four-test worksheet as the defence. When she later revisits pricing at Series A, she has a specific written argument to reason against.

## Common failure patterns

- **Copying the category leader's metric without alignment testing.** "Slack uses per-seat, so we'll use per-seat." Two years later the founder discovers her product's value scales with something else and rebuilding the pricing metric is a 12-month engineering + go-to-market project.
- **Optimising the price point when the metric is wrong.** Founder spends six months A/B testing $99 vs. $149 while the underlying metric is misaligned with the value curve. The number moves are churn-neutral because the metric issue dominates.
- **Picking usage pricing without the metering infrastructure.** Founder announces per-event pricing; billing engineering realises there is no accurate per-customer event count in the product. Every invoice is manually reconciled from BigQuery; six months of accounting drift accumulate before the metering is rebuilt.
- **Picking outcome pricing without an attribution story.** Founder promises "you only pay for the leads we generate." Customers dispute lead counts. The vendor spends more time in attribution disputes than in selling.
- **Ignoring the calculator for a usage-priced product.** Buyer cannot estimate her bill; asks sales; sales gives a range; deal stalls in procurement over the range. Fix: calculator on the pricing page, buyer inputs from her own systems, projected bill visible.
- **Failing to align the metric with the sales motion.** Enterprise product with per-event pricing means the enterprise deal is "how much will we use × per-event price" — an unbounded number that terrifies CFOs and gets cut. Enterprise pricing usually needs a bounded commitment (annual dollar minimum, custom-terms structure) even if the underlying meter is per-event.
- **Metric-metric misalignment between champion and CFO.** Champion loves the product on a per-seat basis (predictable). CFO thinks per-event is more fair. The two are the same people (mod-104's persona split) but under different pressures. If the metric works for only one, the deal dies in the other's court.
- **Bloating the pricing metric with add-on line items.** Base metric is per-repo; then add-on for premium scans; then add-on for enterprise integrations; then per-seat for admin roles. Buyer sees a 5-line quote and every line is a negotiation. Working practice: one primary metric per product, at most one usage overage, everything else in the tier composition.
- **Never revisiting the metric after launch.** The metric was right at seed; two years and a product-scope expansion later, the metric no longer fits. Working practice: revisit the four alignment tests at every pricing-pack revision (Chapter 6's quarterly cadence).
- **Assuming the metric that maximises seed-stage revenue also maximises expansion.** A per-seat metric may close seed customers faster (predictable) but a per-usage metric may drive higher NRR (mod-109). The right metric for landing the first 30 customers is not necessarily the right metric for scaling to 1000. Working practice: pick the metric for where the business will be at the end of the next 18 months, not the start.

## Summary

- The pricing decision has two parts: the **pricing metric** (what dimension you charge along) and the **price point** (the number). The metric is the strategic choice; the number is the test.
- Changing the metric is dramatically harder than changing the price point — it touches metering infrastructure, contracts, sales training, billing, and pricing pages simultaneously. Pick the metric carefully at seed; expect to change price points 3-5× before the metric changes once.
- **Four metric families:** per-seat / per-user (aligned to HR growth, easy to estimate, weak value alignment when value doesn't scale with users), usage / consumption (aligned to activity growth, needs calculators, can create anti-usage incentives), value / outcome (perfect alignment when attribution works, brittle when it doesn't), hybrid (subscription + usage combines predictability with expansion).
- **Four alignment tests** for a candidate metric: (1) scales with value, (2) matches the customer's growth vector, (3) is estimable by the buyer without a pilot, (4) aligns vendor and customer incentives. Metrics failing 2+ tests are usually wrong; failing 1 is workable with mitigation.
- The most reliable derivation route: read the **value equation** from Chapter 2 and pick the *frequency variable* (or its closest proxy) as the metric. Value = base × cost × frequency ⇒ metric ∝ frequency.
- The metric interacts with the **tier composition** from Chapter 3. Per-seat tiers scale by seats per tier plus different prices; usage tiers scale by bracket per tier plus overage rules; hybrid tiers combine both. The tier the mainstream customer belongs to should follow naturally from her scale.
- Usage / hybrid pricing requires a **calculator** on the pricing page that takes buyer-known inputs and returns a projected bill. Without one, the metric fails the estimability test in practice.
- **Signals the metric is wrong** — bill-surprise churn, anti-usage optimisation, bill-flat / value-growing, deals dying at estimation, champion-vs-CFO fights, every enterprise deal requiring custom-clause on the metric.
- **Common failure patterns** — copying the category leader without alignment testing, optimising the number when the metric is broken, promising usage pricing without metering infrastructure, promising outcome pricing without attribution.
- Output of this chapter is the **pricing-metric decision** with the four-test worksheet as the defence. Combined with Chapter 3's tier composition and Chapter 2's value-derived anchor, this completes the "one primary metric + three tiers + one anchor price per tier" spec that Chapter 6's shipping pack assembles.
