# Exercise 04 — Growth Loop vs. Funnel Drill

**Estimated time:** 3 hours
**Chapter link:** [`04-growth-loops-vs-funnel.md`](../04-growth-loops-vs-funnel.md)
**Prerequisite reading:** [Reforge — "Growth Loops are the New Funnels"](https://www.reforge.com/blog/growth-loops) (~20 min); [Brian Balfour — Four Fits framework](https://brianbalfour.com/four-fits-growth-framework) (~30 min); [Dave McClure — "Startup Metrics for Pirates" (AARRR)](https://500hats.typepad.com/500blogs/2007/09/startup-metrics.html) (~15 min); [Andrew Chen — "The Power User Curve"](https://andrewchen.com/power-user-curve/) (~15 min); [Elena Verna — writing on growth loops (Reforge / Substack)](https://elenaverna.substack.com/) (skim, ~20 min)

## Problem statement

Chapter 4 named the four loop archetypes (viral, content, paid, sales-assisted), the diagnostic questions per loop, and the operating rule that **the honest answer is often "one primary loop, and none of the others."** This exercise makes you run the diagnostic on real (or realistic) products and produce the loop verdict — including the "no loop here" call when the data does not support one.

You will:

1. Diagnose four well-known products against all four loop archetypes and pick the primary loop from public evidence.
2. Run the same diagnostic on a real (or realistic hypothetical) startup — with the loop metrics computed on real data where possible — and produce the loop-diagnosis section of the retention + expansion scorecard.
3. Write a short critique of an AARRR-funnel-only growth plan, translating it into the loop model or naming that the business is honestly a linear-funnel business.

The exercise trains the loop-vs-funnel distinction so that "we're building growth loops" stops being a talking point and becomes a measurable claim with a specific metric and a specific investment threshold.

## Requirements

Deliver a folder `exercise-04/` with:

- `part-a-loop-diagnoses.md` — the four-loop diagnostic across four provided products.
- `part-b-your-loop-diagnosis.md` — the loop diagnosis for a chosen startup, in scorecard-section-5 shape.
- `part-c-funnel-critique.md` — critique of a funnel-only growth plan.

### Part A — Diagnose four products across the four loop archetypes (75 min)

For each product, produce a diagnosis in this structure:

1. **Viral loop diagnostic.** Does a single user's value action inherently expose another person to the product? Is the multi-user experience better than the single-user experience? What is a reasonable public-evidence estimate of K (or a note that K is not publicly estimable)?
2. **Content loop diagnostic.** Do users produce indexable artifacts useful to non-users? Is there external traffic to user-generated content at meaningful volume? If the team turned off editorial content investment, would organic acquisition keep growing?
3. **Paid loop diagnostic.** Public evidence for LTV/CAC and payback (S-1s, published unit economics, practitioner writeups where available). Does the retention curve support a paid loop?
4. **Sales-assisted loop diagnostic.** Is there evidence that referenced deals materially outperform cold outbound? Any published examples of enterprise expansion via reference?
5. **Verdict.** Which loop(s) is primary; which is secondary; which honestly does not exist. Cite public sources.

**Product 1 — Notion.** Product-led collaboration / docs / databases. Individual and team plans; enterprise tier. Template gallery is public.

**Product 2 — Snowflake.** Enterprise cloud data warehouse. Public S-1 and quarterly reports available. Consumption-based pricing.

**Product 3 — Duolingo.** Consumer language-learning mobile app. Freemium + subscription. Public S-1 and post-IPO filings.

**Product 4 — HubSpot.** Multi-product B2B SaaS (marketing, sales, service). Long-running content-marketing programme; SMB → mid-market → enterprise motion. Public financials.

For each: full five-field diagnosis, one to two paragraphs. Cite at least one primary source (S-1, quarterly report, official blog post, or a named practitioner writeup) for each loop verdict — do not invent the numbers.

<!-- needs-research: verify the specific loop verdicts against the most recent public filings and practitioner writing for each of the four products. -->

### Part B — Diagnose the loops your startup supports (75 min)

Pick a startup — yours, one you know well, or the running code-review-tool (design a variant so you are not copying Chapter 4's verdict).

Deliver `part-b-your-loop-diagnosis.md` in the shape of scorecard section 5:

1. **The four diagnostics.** Same structure as Part A. For each loop:
   - **Viral loop:** K-factor computed on real data if possible (or state the instrumentation gap that prevents computing it). At minimum, an estimate with the source named.
   - **Content loop:** the organic-traffic-to-user-generated-content number and the ratio of user-generated to editorial content in the acquisition mix.
   - **Paid loop:** LTV, CAC, payback, and the retention curve in the paid-acquired cohort (from Exercise 01 / Chapter 1 data if you did that).
   - **Sales-assisted loop:** cycle-time and win-rate for referenced deals vs. cold-outbound (from CRM data if you have it).
2. **Loop-metric table.** One row per loop; columns for the specific loop metric, current value, and net-productive threshold.
3. **Primary loop verdict.** One-sentence claim naming the primary loop and the evidence.
4. **Secondary loop verdict.** One-sentence claim naming a loop you are investing in as secondary — or "none, investing only in the primary this year."
5. **Explicit "no loop" call.** For each loop you are *not* claiming, one sentence naming why (K < 0.1; content is editorial not user-generated; LTV/CAC below threshold; sales cycle no faster on referenced deals).
6. **Roadmap allocation.** One paragraph on how loop investment shows up in the next-quarter roadmap — an experiment, a product change, a channel investment — tied to the primary and secondary loops.

Length: 1–2 pages. Do not exceed 2. Where public data is not available, mark as hypothetical and justify against benchmark ranges.

### Part C — Funnel-only growth-plan critique (30 min)

Below is a synthetic Q3 growth plan from a Series-A startup ("Contour Analytics" — synthetic; a B2B analytics tool for SMB e-commerce operators). Critique it in the loop framework:

> **Contour Q3 Growth Plan (as submitted by Head of Growth):**
>
> - **Acquisition.** Increase LinkedIn Ads spend from $18k/mo to $40k/mo. Expected 2.2× signup volume based on Q2 CAC-per-signup.
> - **Activation.** New product-tour walkthrough on first login; expected activation rate lift from 34% to 42%.
> - **Retention.** Weekly product-tips email; expected W4 retention lift from 42% to 48%.
> - **Referral.** New "refer a friend for a $50 credit" button in the app. Expected 8% of active users to refer within 90 days.
> - **Revenue.** No pricing changes.
> - **Summary.** "Doubling top-of-funnel spend and moving each stage's conversion rate by 5–10% delivers a 2.4× revenue plan for Q3."

Produce a `part-c-funnel-critique.md` (~600 words) that:

1. Names the AARRR-as-growth-model failure this plan encodes (Chapter 4).
2. For each of the four loop archetypes, states whether the plan invests in it, ignores it, or actively degrades it.
3. Names the specific loop this plan would produce if any (or "none — this is a linear-funnel plan").
4. Rewrites the plan into the loop framing that fits the business: what the primary loop hypothesis is, what the loop metric is, and what one experiment would test whether the loop is working.
5. If the honest verdict is *"there is no compounding loop in this business, and the plan is a linear-funnel plan"*, say so — Chapter 4's core discipline is to name this rather than dress up a funnel as a loop.

### Part D — Reflection (15 min)

A short closing paragraph:

- Which of the four products in Part A was hardest to loop-diagnose from public evidence, and what data would you want that isn't public?
- For your Part B startup, what loop *do you wish* you had that the product does not currently support, and what single product change would create it (or what would you have to accept about being a linear-funnel business)?
- Where does the funnel remain the right instrument in your Part B business (per-stage conversion, cohort walkthroughs, user-journey mapping — Chapter 4's "funnel still has a job" section)?

## Starter guidance

- The K-factor arithmetic is `K = invites-per-active-user × conversion-rate-of-invites`. K > 1 is exponential; 0 < K < 1 amplifies but does not self-sustain; K = 0 is no loop. If you cannot compute K on real data, name the instrumentation gap and estimate the range.
- The Chapter 4 content-loop diagnostic hinges on the question *"if you turned off editorial investment, would user-generated content keep acquiring users?"* HubSpot's blog is editorial-plus-community; Stack Overflow is nearly pure user-generated; Notion's template gallery is user-generated with editorial curation. Score the mix honestly.
- The paid-loop diagnostic requires the leaky-bucket read from Chapter 1 — if the paid-acquired cohorts churn faster than the outbound-acquired cohorts, the paid loop is not net-productive regardless of the top-line LTV/CAC.
- The sales-assisted loop diagnostic requires computing referenced-deal cycle time and win rate vs. cold-outbound cycle time and win rate. If your CRM does not have a "source of lead" field distinguishing reference from outbound, the loop is not measurable — that itself is the instrumentation gap.
- For Part A's public products, prioritise primary sources: S-1s (SEC EDGAR is the free source of truth), quarterly reports, official product blogs. Do not invent metrics from memory.
- For Part C, the trap is to accept the plan on its own terms. The Chapter 4 discipline is to reframe — either into a loop hypothesis with a loop metric or into an honest "this is a linear-funnel business, so scale-of-funnel is the plan, and please stop calling it a growth loop."
- A "refer a friend" button is Chapter 4's canonical example of a *not-a-loop* dressed up as a loop. If the product's value action does not inherently expose another person, adding a referral button will not create a viral loop.

## Acceptance criteria

Your submission is complete when:

- [ ] Part A diagnoses all four products across all four loops with at least one primary-source citation per verdict.
- [ ] Part A distinguishes user-generated content loops (Notion templates, Duolingo user-generated leaderboards / user artifacts if any) from editorial content programmes (HubSpot blog).
- [ ] Part A names Snowflake's primary loop as sales-assisted (or usage-revenue) and not viral, and cites the S-1 / annual report evidence.
- [ ] Part A names HubSpot's primary loop with the content-vs-content-marketing distinction explicit.
- [ ] Part B computes (or estimates with source) each loop metric with the net-productive threshold called out.
- [ ] Part B has an explicit "no loop" call for at least one archetype the product does not support.
- [ ] Part B ties primary and secondary loop verdicts to a next-quarter roadmap allocation.
- [ ] Part C's critique names the AARRR-as-growth-model failure explicitly and reframes into either a specific loop hypothesis or an honest linear-funnel call.
- [ ] Part C's critique addresses the "refer a friend button = viral loop" fallacy directly.
- [ ] Part D reflection names a public-data gap, a wished-for loop that the product does not currently support, and where the AARRR funnel is still useful.

## Common ways this exercise goes wrong

- **Claiming a viral loop from a "refer a friend" button.** Chapter 4's canonical example of a not-a-loop. The value action has to inherently expose another person.
- **Calling a content-marketing programme a "content loop."** Editorial-produced content is a paid loop in effect. A content loop requires user-produced content that acquires more users.
- **Claiming a paid loop with LTV/CAC < 1.** That is buying revenue below cost, subsidised by fundraise. Chapter 4 said it explicitly.
- **Claiming a sales-assisted loop when referenced deals don't outperform cold-outbound on cycle time and win rate.** Compute both.
- **Running all four loops at 25% investment each in the roadmap.** Chapter 4's parallel to mod-108 Chapter 1's channel-portfolio anti-pattern.
- **Refusing to name "no loop exists here."** Some businesses are honestly linear-funnel businesses. Naming it is not a failure; pretending otherwise costs 12–18 months.
- **Skipping the loop metric in Part B.** A loop without a measurable conversion rate and cycle time is not a loop; it is a hope.
- **Accepting the Part C plan on its own terms.** The exercise's whole point is to reframe or refuse.
- **Using loop language to justify a strategy the metrics do not support.** If K is 0.3 and LTV/CAC is 1.5, saying "we're building for loops" does not fix the numbers.
- **Reporting Snowflake's primary loop as "viral" or "content."** Public financials disprove both; the primary loop is sales-assisted + usage-revenue.
