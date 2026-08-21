# Price Experiments and Grandfathering — Cohort Tracking Over Snapshot ARR

## Motivation

The pricing pack from Chapters 1-4 is a hypothesis, not a finished artifact. The value equation is derived from imperfect inputs; the WTP research is a small sample; the metric-choice defence is a bet; the tier composition is intuition backed by a worksheet. Every single decision in the pack has to be **tested against the market** to become defensible, and that testing is not "run one A/B test" — it is a structured programme of price experiments run over the first 12-24 months after launch.

Startup-stage price experimentation is not what enterprise SaaS pricing consultancies run at scale (thousand-customer conjoint studies, multi-week randomised holdouts). The founder-led-sales stage of the business has 20-100 customers, not 10,000; sample sizes for classical statistical significance are unreachable. Instead, the founder runs a small set of **founder-scale** experiments — first-conversation pricing tests, plan-tier switches, geographic / segment variants, grandfathering policies for existing customers — and reads the results through **cohort-level tracking**, not snapshot ARR.

The failure mode this chapter exists to catch: **the founder either (a) never runs price experiments — "we'll figure out pricing later" — and locks in the original guess through inertia; or (b) runs experiments badly — snapshot-ARR reads that miss cohort effects, guerrilla price changes that anger existing customers, undocumented grandfathering that costs the finance team quarters of reconciliation.** Both patterns cost the same amount of ARR; the second costs it in a way that is much harder to diagnose.

This chapter fixes:

- The four founder-scale experiment types — first-conversation, plan-tier switch, segment / geo variant, grandfathering — and how to design each.
- **Cohort-level tracking** as the primary read on any price change, and why snapshot ARR misleads.
- **Grandfathering policy** — the specific rules for how existing customers are treated when new pricing lands, and the failure modes of ad-hoc grandfathering.
- **Guardrails** — the small set of pre-committed rules that prevent price experiments from silently damaging the business.
- The **experiment cadence** and how the pack (Chapter 6) commits to one experiment per quarter.

Chapter 6 assembles the shipping pack that includes at least one supported experiment for the next quarter. This chapter is where the experiment gets designed.

## Core concepts

### Why startup-scale experimentation is different

Enterprise-scale A/B testing on prices assumes independence, sample size, and homogeneous customers. Startup-stage sales has none of these:

- **Sample size:** 20-100 customers total is not enough for a statistically significant read on any single variant. Classical p-values are unreachable; the founder is reading directional signal from small samples, not confirming statistical hypotheses.
- **Independence:** customers talk. A price variant offered to Customer A gets discussed on the ICP Slack channel Customer B is in; the founder's variant becomes public within days. Serious A/B testing assumes variants are unobservable across the sample; startup-stage they usually aren't.
- **Homogeneity:** two customers in the same segment can have wildly different WTP based on situation (budget cycle, urgency, executive sponsorship). Sample variance dominates any small treatment effect.
- **Cost of a bad read:** losing a customer to a price experiment at seed stage matters — that's 5% of your MRR gone from one call. The cost of exploration is not amortised across a large base.

Startup-scale price experimentation therefore looks less like an academic RCT and more like an **operational discipline**: run one experiment at a time; design it so the results are readable without needing statistical power; commit to how you'll interpret the results *before* looking at them; document what you learn even when the sample is small.

### Experiment type 1 — first-conversation pricing tests

The lowest-cost, highest-throughput experiment: **change the anchor price you quote in the first sales conversation** for one week, measure the reaction, revert or continue.

**How it works:**

- Founder is doing mod-105 discovery calls. In the second-half of each call, the price conversation happens ("here's how our pricing works — the middle tier is $X / month, the premium is $Y").
- For one calibrated period (a week, or 10 discovery calls, or whichever is smaller), the founder quotes an *adjusted* anchor — say, $X + 25% or $X - 15%.
- Founder records the reaction against a small ordinal scale — 1 (obvious sticker shock, deal likely dead), 2 (visible discomfort, will require justification), 3 (neutral, expected), 4 (positive, buyer thinks it's fair or a bargain), 5 (buyer volunteers she'd pay more).
- After the calibrated period, compare the reaction distribution to the baseline period.

**What you can learn:** whether the anchor is in the right band. If a 25% price increase produces mostly-3s with a couple of 2s, the anchor is under-priced; if the same increase produces 1s and 2s dominating, the anchor is at or near the ceiling.

**What you cannot learn:** exact revenue impact (small sample), long-term retention effects, differential effect across sub-segments.

**Design rules:**

- Only vary the anchor tier's price. Do not change the metric, tier composition, or features simultaneously — a compound change is un-decodable.
- Log the reaction *before* the conversation moves on. Memory reconstructs favourably; write it down at the end of the call.
- Do not lie about which price is "the real price." If a customer accepts the experimental anchor, that becomes the real price for her. Bait-and-switch destroys trust and violates the point of the exercise.
- One week per direction. If you're testing +25% and -15%, that's two weeks; if the results are ambiguous, run another two-week cycle.

**Common failure modes:**

- Founder cherry-picks the results ("the deal we lost was because of the buyer's budget cycle, not the price"). The point of the ordinal-scale logging is to prevent this.
- Founder introduces the experimental price as "we're testing" — buyers who know they're in an experiment behave differently. Quote the price straight.
- Founder runs the experiment on the wrong-fit buyer. If the first two calls of the experimental week are off-ICP, the read is worthless. Every experimental call has to pass the ICP scorecard (mod-104) first.

### Experiment type 2 — plan-tier switches

**How it works:** for a defined cohort of new sign-ups (usually a time window: "all customers signing in November"), change the composition or price of one or more tiers, and measure the resulting **tier-mix distribution** over the next quarter — what fraction lands in Starter vs. Team vs. Business.

**What you can learn:** whether a tier-composition or price change moves buyers to the intended tier. The read is the *mix shift* between cohorts, not the individual conversions.

**Design rules:**

- Change **one** thing between cohorts: either the middle-tier price, or a specific feature's tier assignment, or the entry-tier's usage bracket — not multiple simultaneously.
- Measure the tier-mix over a **consistent time window** post-signup (e.g. 60 days from signup) — otherwise cohorts at different maturities aren't comparable.
- Keep the treatment period **at least 2× the length of the average sales cycle** (mod-105) — otherwise the cohort under measurement is contaminated by pre-experiment deals still closing.
- Publish the pricing page change to everyone in the cohort period; do not selectively show different tier pages to different buyers unless you have proper cohort isolation infrastructure (most seed-stage startups don't).

**What you cannot learn:** the counterfactual for the same cohort under the old pricing. Time-series reads confound seasonal effects (Q4 procurement freezes, budget cycles, launch spikes). Compare to the *same period from last year* if possible; otherwise interpret with wide bands.

**Common failure modes:**

- Reading tier mix at 30 days when the sales cycle is 45 days — the mix measured is dominated by fast-closing deals, which are not representative of the cohort.
- Attributing all mix change to the experiment when other things changed at the same time (new marketing campaign, new AE, new competitor launch).
- Not writing down the pre-experiment mix baseline before the change lands.

### Experiment type 3 — segment / geographical variants

**How it works:** run different pricing structures for different **segments** (enterprise vs. mid-market vs. SMB) or **geographies** (US vs. EU vs. LATAM) simultaneously, and measure the segment-specific close rate + ARPU.

**What you can learn:** whether a segment's WTP or purchase behaviour differs enough to justify a segment-specific pricing structure. Common findings: enterprise willing to pay 2-3× per-unit for the same product; LATAM / Asia SMB pricing needs to be structurally lower (often 30-50%) to hit local WTP; certain verticals (healthcare, finance) tolerate significantly higher prices for identical features.

**Design rules:**

- Segment definitions have to be **enforceable** — you need a way to route the buyer to the correct pricing (based on country IP, self-declared company size, verified verticals). Un-enforceable segmentation collapses when a mid-market buyer discovers the SMB price on the same page.
- Publish the segmentation policy: "We offer regional pricing for LATAM markets" is defensible; hiding it is not. Discovered segment discrimination is a trust event.
- Enterprise pricing being higher via custom-terms negotiation is standard and expected. Regional pricing being lower is standard for consumer / prosumer. Vertical-specific pricing needs to be defended by a clear feature-set justification (usually the "premium tier" is what's sold to the high-tolerance vertical, not a different price for the same tier).
- Track the segment mix carefully — if the segment definitions leak (SMB buyer accesses mid-market pricing), the cohort tracking has to flag it.

**What you cannot learn:** how a customer would have behaved under a different segment's pricing. Segment experiments are natural experiments across observably-different populations; they are not causal.

**Common failure modes:**

- **Discovered arbitrage.** A US buyer routes to the LATAM pricing via a VPN. If arbitrage is easy, the segmentation is not enforceable; either invest in enforcement or drop the segmentation.
- **Un-defensible vertical pricing.** Vendor charges healthcare 2× the price for identical features "because healthcare pays more." When discovered, this is a trust event. Vertical pricing needs a compliance / feature justification.
- **Salesforce spillover.** Sales team quotes the LATAM price to a US mid-market prospect because "we want to close it." The segment policy erodes through case-by-case exceptions.

### Experiment type 4 — grandfathering (the migration policy)

**How it works:** when new pricing lands, **grandfathering** is the policy for how existing customers are treated. Four common policies:

- **Full grandfather — indefinite:** existing customers stay on old pricing forever, or until they voluntarily upgrade. New customers get new pricing. Preserves existing customer trust; slows the transition; leaves ARPU on the table for existing customers.
- **Full grandfather — sunset window:** existing customers stay on old pricing for a defined window (12 months, or their current contract term + 12 months), then migrate to new pricing at renewal. Balances trust with revenue capture. This is the modal choice for well-run pricing transitions.
- **Partial grandfather — feature or metric only:** existing customers keep their old price but get access to new features (or lose access to features moved to a higher tier under new pricing). Complex to explain; used when the tier composition changes but not the price.
- **No grandfather — immediate migration:** all customers migrate to new pricing at next billing. Fastest ARR impact; highest churn risk; usually appropriate only when the underlying product has changed meaningfully or when the old pricing was demonstrably unsustainable.

**Design rules for grandfathering:**

- **Decide the policy *before* the pricing launch.** Ad-hoc grandfathering — case-by-case decisions about which customers keep which prices — is what produces the "our finance team spent 3 quarters reconciling contracts" outcome. The rule has to be pre-committed.
- **Communicate the policy directly to existing customers.** Every existing customer gets an email explaining what their pricing will be, when any changes take effect, and what they can do about it. Silent price migrations are a trust event.
- **Provide a lock-in period.** Existing customers should have the option to renew at their current price for one more term (typically 12 months) as a good-faith preservation of their existing bet on the vendor.
- **Document the grandfathered customers.** The customer base splits into "grandfathered" and "current" pricing cohorts. This has to be trackable in the CRM and in cohort-analysis tooling — otherwise the finance team can't answer "how many customers are on old pricing" a year later.
- **Sunset the grandfathered cohort explicitly.** If the policy is "12 months grandfather," the grandfathered cohort should be zero-ing out on a known date. If it isn't, either the policy has slipped or the finance team is not tracking the migration.

**What you can learn:** how much of the ARR impact of new pricing is being *realised* vs. being deferred by grandfathering; the churn signal from customers who migrated to new pricing (compared to a control of customers who haven't yet migrated).

**Common failure modes:**

- **Case-by-case grandfathering.** Sales rep grandfathers a customer to close a renewal; another sales rep does not grandfather a similar customer; the customers talk; the trust event is worse than either uniform policy.
- **Forgotten grandfathered customers.** Three years post-transition, 40 customers are still on old pricing that no one at the company remembers offering. The revenue impact of the pricing change was never fully realised.
- **Grandfathering used as retention bribery.** Customer threatens to churn; vendor offers grandfathered pricing. Churn averted, but the policy becomes "threaten churn, get grandfathered pricing" and cascades.
- **No lock-in period offered.** Customers see a price increase with 30-day notice; churn spike is 3-5× normal at the next renewal cycle.
- **Silent grandfathering.** Vendor doesn't tell customers they were grandfathered. Later the customer discovers a new customer got the newer, better tier at the same price. Trust event.

### Cohort tracking — why snapshot ARR misleads

The critical instrumentation discipline for any price change is **cohort-level tracking**: measure the price change's impact separately for each *cohort* of customers (typically the month or quarter of signup), and read the cohort curves rather than the aggregate ARR snapshot.

**Why snapshot ARR misleads.** Suppose the founder raises the middle-tier price by 25% in Month 1 with a full grandfather (existing customers stay on old pricing). In Month 4:

- Existing customers still pay the old price. Their ARR is unchanged.
- New customers pay the new price. Their ARR is 25% higher per customer.
- New customer volume is (say) 10% lower because the higher price has slowed sales cycles.

The aggregate ARR change: new-customer count × new-price - what-they-would-have-paid-under-old-price - lost-new-customers × old-price. If new customers are 20% of the base, the aggregate ARR moves by maybe 3-5%. The founder looks at the ARR number, sees a small move, and concludes "the price change was a wash."

**What she's missing:** the *cohort* view. The Month 1 cohort (new customers under new pricing) has 25% higher ARPU than the Month 0 cohort (last cohort under old pricing). The cohort's *close rate* is slightly lower. The cohort's *90-day retention* is (say) unchanged — no dropoff from paying more. The cohort-level read is unambiguous: the price change captured more value per customer at a small close-rate cost, and the trade is likely favourable.

Snapshot ARR conflates: (a) new customers under new pricing, (b) existing customers under old pricing, (c) churn (whose distribution across cohorts matters), (d) upsell / expansion. Cohort tracking separates these effects and lets you attribute movement to the price change specifically.

**Cohort tracking discipline:**

- **Tag every customer with her signup cohort** (month or quarter) and her *pricing regime* (which pricing pack was in effect at her signup).
- **Compute per-cohort ARPU, close rate, and retention curve** monthly.
- **Compare cohorts before and after the price change** rather than looking at the aggregate.
- **Include the grandfathered cohort explicitly** — treat existing customers on old pricing as one cohort, existing customers migrated to new pricing as a second cohort, new customers under new pricing as a third.

This discipline is why mod-102 (PMF measurement) and mod-109 (retention / cohort analysis) are dependencies for this module. The cohort-tracking infrastructure has to exist before price experiments are run; retrofitting it after a price change loses the pre-change baseline.

### Guardrails — the pre-committed rules

Any price experiment has to have guardrails: pre-committed rules that say "if X happens, we stop / reverse / escalate." Guardrails prevent the "we ran the experiment for six months because the results were ambiguous" outcome.

Standard guardrails:

- **Close-rate floor.** "If the new-cohort close rate drops below X% (measured over Y days), revert." X is a fraction of the pre-experiment close rate (usually 70-80%).
- **Cohort-retention floor.** "If the 30-day retention of the new-cohort drops below Y%, revert." Y is a fraction of the pre-experiment retention.
- **Voluntary churn spike.** "If voluntary churn in any cohort exceeds Z above baseline, investigate immediately."
- **Support ticket spike.** "If pricing-related support tickets exceed baseline by Z%, pause the experiment."
- **Sales rep signal.** "If ≥ Y AEs raise concerns about the pricing in a given week, discuss in the weekly forecast meeting."

The guardrails should be committed *before* the experiment starts, and the guardrail thresholds should be part of the experiment's design doc. Guardrails discovered mid-experiment ("well, actually, we shouldn't cross this line") are not guardrails — they are rationalisations.

### Experiment cadence — one per quarter

At founder-scale, running more than one price experiment simultaneously is a false economy. Two overlapping experiments contaminate each other (which caused the cohort shift?) and consume all the founder's remaining pricing-attention budget.

Working cadence: **one supported experiment per quarter.** The experiment is:

- **Chosen at the pricing pack's quarterly review** (Chapter 6). The pack revision names the next quarter's experiment specifically.
- **Designed against the four types** — first-conversation, plan-tier switch, segment / geo, grandfathering. Occasionally a hybrid of two.
- **Run for a defined window** — typically 4-12 weeks depending on the experiment type. First-conversation tests can run in a week; plan-tier switch experiments need at least one full sales cycle post-launch.
- **Read against the guardrails and against the cohort tracking** — not against snapshot ARR.
- **Documented in the pack** — what was tried, what was seen, what was concluded. The documentation is what compounds; a year of un-documented experiments produces no learning even if each individual experiment was informative.

Over 12-18 months, this cadence produces 4-6 documented experiments — enough to answer the module's core questions with real market data instead of derivation-only reasoning.

## Concrete example — Loomly's Q2 experiment

Continuing the running example. Loomly launched its pricing pack in Q1 (Starter $4/repo, Team $12/repo, Business $28/repo, per-repo metric). By end of Q1 there are 30 paying customers: 5 on Starter, 22 on Team, 3 on Business.

**Diagnosis at Q1 review:** Team-tier mix is 73%, which is healthy (anchor tier winning). But *within Team*, the win rate on deals over 200 repos is high (85%) while the win rate on deals under 60 repos is lower (30%) — small-repo customers see $12/repo as high relative to their small footprint. Meanwhile, Business-tier volume is low; only 3 customers, and the founder isn't sure whether Business is priced right or just not-marketed-enough.

**Q2 experiment choice:** the founder picks **plan-tier switch** experiment as the highest-value single experiment. Specifically, she introduces a **volume-based discount** to Team-tier pricing:

- 1-50 repos: $12/repo (unchanged).
- 51-150 repos: $10/repo (17% discount).
- 151+ repos: $8/repo (33% discount).

The theory: the Team tier is priced right for the mid-scale customer but over-priced for the small-scale customer (who might be pushed to Starter) and under-priced for the large-scale customer (who is comfortable with $12 but might have accepted more). The tier stays; the per-metric price becomes a step function within the tier.

**Baseline metrics:**
- Q1 close rate: 42% on Team-tier deals.
- Q1 ACV: $10,800 mean.
- Q1 sales cycle: 38 days mean.
- Q1 30-day retention: 96%.

**Guardrails:**
- If Q2 close rate drops below 35%, pause.
- If 30-day retention drops below 92%, pause.
- If pricing-related support tickets in any week exceed 3× Q1 baseline, pause.
- Weekly review at the founder-led-sales pipeline meeting (mod-105 Chapter 7).

**Communication policy:**
- New pricing goes on the pricing page on Day 1 of Q2.
- Existing customers keep their current terms until renewal (full grandfather, 12-month sunset). Explicit email to every existing customer.
- New calculator on the pricing page reflects the volume tiers so the buyer can see her projected bill.

**Cohort tracking setup:**
- Q1 cohort tagged "pricing v1 flat."
- Q2 cohort tagged "pricing v2 volume-tier."
- Existing Q1 customers tagged "grandfathered v1."
- ARPU, close rate, retention tracked separately per cohort, measured at 30 / 60 / 90 days.

**End-of-Q2 read (hypothetical):**
- Q2 close rate on Team-tier deals: 51% (up from 42%).
- Q2 mean ACV: $9,400 (down from $10,800; volume discount pulling ACV down for the big deals, but volume of deals up).
- Q2 total Team-tier ARR contribution: $340K vs. Q1's $240K — up 40%.
- 30-day retention: 97% (unchanged, within noise).
- Grandfathered cohort behaviour: unchanged, no churn spike.

**Conclusion:** the volume-tier discount within Team was a positive move. ARPU per deal fell (as expected), but close rate improved enough to more than compensate. The pack revision at Q3 canonises the volume tier as the standard Team-tier pricing.

**Documentation:** the experiment design doc, the guardrails, the pre-experiment baseline, the cohort read, and the conclusion are appended to the pricing pack under a "Change log" section. Twelve months later, when the pricing is questioned again, the founder can point at this document rather than re-litigate the change.

## Common failure patterns

- **The-price-change-that-was-actually-five-changes.** Founder changes the middle-tier price, the middle-tier feature composition, the metric definition, and adds a new tier all in one launch. Six months later the cohort behaves differently and no one can attribute the change to any single move. Rule: one variable at a time.
- **Snapshot-ARR reads.** Founder looks at the ARR number at Month 3 post-change, sees no movement, concludes the change was a wash. The change actually captured 25% higher ARPU on the 20% of the base that is new customers; the aggregate is masked by the 80% still on old terms. Fix: cohort tracking, not snapshot.
- **Un-committed guardrails.** Experiment runs into trouble; founder debates internally whether the trouble crosses a line worth reverting for; by the time the debate is resolved, more customers have been affected. The guardrails have to be pre-committed with specific thresholds.
- **Ad-hoc grandfathering.** No policy; sales reps make case-by-case decisions; the customer base is a mosaic of pricing regimes no one can enumerate. Fix: one policy, communicated in writing, tracked in CRM.
- **Grandfathering forever without sunset.** Full-indefinite grandfather never planned to end; three years later the average customer's ARPU is 40% below the current price because most of the base pre-dates the current pricing. Fix: sunset windows on grandfather policies; even 24-month sunsets are much better than indefinite.
- **Silent price migrations.** Vendor changes pricing without telling existing customers; they discover it when the next invoice looks different; trust event; churn spike. Fix: explicit communication ≥30 days before any change to an existing customer's bill.
- **Segment pricing that leaks.** LATAM pricing accessible via VPN; US buyer discovers it; trust event; either the segmentation gets rolled back (loss of face) or the enforcement gets stronger (engineering cost). Fix: enforce segmentation at signup, or don't segment.
- **Bait-and-switch experimentation.** Founder quotes an experimental price, buyer accepts, founder then says "actually the real price is different." The customer walks, tells the community, and the founder's ability to run future experiments in that community is damaged. Fix: any price quoted in an experiment is a real price the vendor honours.
- **Running experiments without ICP filtering.** The three customers in the experimental week are all off-ICP. Their reactions to price are noise. Fix: every experimental call has to pass mod-104's ICP scorecard before being included in the read.
- **Continuous experimentation without a pack revision.** Founder runs experiments constantly; the "current pricing" is whatever was last tried; the sales team can't quote confidently; buyers see different prices depending on when they arrived. Fix: one supported experiment per quarter, canonised in the pack at the end of the quarter; between-quarter pricing is stable.
- **Not documenting the experiment.** Founder runs an experiment, reads the results, moves on. Six months later someone asks "why did we change to volume tiering?" and no one remembers the reasoning. Fix: append every experiment's design + baseline + read + conclusion to the pricing pack under a change log.
- **Confusing statistical significance with operational significance.** Founder tries to hit p < 0.05 with 30 customers, can't, and concludes the experiment "didn't reach significance." Startup-scale experimentation is about directional signal + operational judgement, not classical significance. Fix: report effect sizes and cohort-comparison bands, not p-values.

## Summary

- Startup-stage price experimentation is fundamentally different from enterprise-scale A/B testing — small samples, non-independent customers, heterogeneous WTP, and high cost of a bad read. The discipline is **operational**, not academic — directional signal + guardrails + documentation, not classical significance.
- **Four experiment types** — first-conversation pricing tests (fastest read, one variable, the anchor tier), plan-tier switches (change one thing in tier composition or price, read tier-mix shift across cohorts), segment / geo variants (natural experiments across observably-different populations, requires enforceable segmentation), grandfathering policies (how existing customers are migrated to new pricing).
- **Cohort-level tracking** is the primary instrumentation. Snapshot ARR masks change because it aggregates new customers under new pricing, existing customers on old, grandfathered cohorts, churn, and expansion — all of which move independently. Per-cohort ARPU, close rate, retention curves separate the effects.
- **Grandfathering** — decide the policy *before* the launch. Full-indefinite is safe but leaves ARPU on the table; sunset-window (12-24 months) is the modal choice; partial grandfather (feature-only) is complex but sometimes right; no-grandfather is high-churn-risk. Ad-hoc grandfathering is worse than any principled policy.
- **Guardrails** — pre-committed rules with specific thresholds — prevent experiments from silently damaging the business. Standard guardrails: close-rate floor, retention floor, voluntary churn spike alert, support ticket spike, sales rep concern signal. Guardrails discovered mid-experiment are rationalisations.
- **Experiment cadence: one supported experiment per quarter.** Multiple simultaneous experiments contaminate each other; the founder's pricing-attention budget is finite. The quarterly pack revision (Chapter 6) names the next quarter's experiment.
- The experiment's **design doc** — what's changing, guardrails, baseline metrics, cohort tracking, communication policy, read timeline — is written before the experiment starts. The doc plus the eventual conclusion is appended to the pricing pack under a change log, so that 12 months later the reasoning can be re-examined.
- **Common failure patterns** — five-changes-at-once, snapshot-ARR reads, un-committed guardrails, ad-hoc grandfathering, silent price migrations, leaky segment pricing, bait-and-switch experiments, non-ICP experimental samples, continuous experimentation without canonisation.
- The experiment discipline is what turns the pricing pack from a *derivation* (Chapters 1-4) into a *learning system*. The pack ships with an experiment plan (Chapter 6) and evolves through documented experiment cycles rather than through founder-intuition edits between cycles.
