# Willingness-to-Pay Research — Van Westendorp, Gabor-Granger, Max-Diff

## Motivation

Pricing is almost always set the wrong way at a seed-stage startup. Either the founder picks a number — $49, $99, $499 — because it "feels right" and "matches what competitors charge," or she runs a cost-plus calculation ("hosting is $12 per customer per month, so we'll charge $60 to hit a 5× margin"), or she asks three friendly buyers "would you pay $X?" and takes the loudest yes as evidence. Every one of these methods produces a number that has no relationship to what the market will actually pay, and the founder discovers this only after quarters of soft close rates and stubbornly-low ARPU that no discount can fix.

Willingness-to-pay (WTP) research is the discipline of asking buyers about price in a **structured** way that produces a *distribution*, not a point estimate — a curve that says "here's the fraction of the target segment that finds the price acceptable at $X, at $Y, at $Z." The output is not "the right price is $99;" the output is "at $49 we lose 8% of the segment on being-too-cheap-to-be-credible, at $199 we lose 62% on being-too-expensive, and the acceptable band is $79-$129 with a modal point around $99." Once the curve exists, the pricing conversation is grounded in something the founder can test, refute, and iterate on.

Three primary instruments produce that curve, each with different mechanics, different sample-size requirements, and different failure modes. This chapter fixes their operating shape:

- **The Van Westendorp Price-Sensitivity Meter (PSM)** — four direct price questions per respondent, plotted as intersecting curves that identify a "range of acceptable prices" and an "optimal price point."
- **Gabor-Granger** — direct accept / reject sampling at randomised price points, plotted as a demand curve that estimates revenue-maximising price.
- **Max-Diff (best-worst scaling)** — an indirect feature-preference instrument that ranks *what* buyers value most, which then feeds tier construction and the pricing metric decision.

The failure mode this chapter exists to catch: **the founder either skips WTP research entirely and picks a number by intuition, or runs WTP research incorrectly (leading questions, wrong sample, wrong instrument for the question being asked) and treats the resulting bad number as if it were empirically defended.** Both patterns cost the same amount of revenue — the second is worse because it comes with false confidence.

This chapter is the empirical foundation the rest of the module rests on. Chapter 2 anchors the *value* the buyer is paying for; Chapter 3 arranges that value into tiers; Chapter 4 chooses the *metric* that ties the price to usage. The WTP curve here is the input every one of those decisions is calibrated against.

## Core concepts

### Why WTP research at all — the value / cost / competitor triangle

The classic pricing frame (Nagle & Müller, *The Strategy and Tactics of Pricing*) sets three anchors any pricing decision has to be defensible against:

- **Cost** — the floor. Charging below fully-loaded cost destroys the business per unit sold. Cost tells you where the *bottom* is; it does *not* tell you where the price is.
- **Competitor** — the reference. A price that ignores what the buyer's existing alternatives cost forces the buyer to construct her own reference, badly. Competitor prices tell you where the *anchor* is; they do *not* tell you where the price should be.
- **Value** — the ceiling. The value the buyer captures from the product sets the maximum defensible price — anything above that fails ROI math. Value tells you where the *top* is; the strategic question is where inside the [cost, value] band the price should sit.

WTP research is how the founder *measures the ceiling* — not by asking "what is the ROI" (Chapter 2's job) but by asking the buyer directly, in a structured way, where the price would tip from acceptable into too-expensive. The two are complementary: value-based pricing (Chapter 2) computes the ROI ceiling from the buyer's economics; WTP research measures the buyer's *stated* ceiling. They usually differ, and the gap is diagnostic — a value ceiling far above stated WTP means the buyer has not yet been sold on the value; a stated WTP far above the value ceiling means the buyer is over-optimistic (or the instrument is misdesigned).

### Instrument 1 — Van Westendorp Price-Sensitivity Meter

Peter Van Westendorp's PSM (introduced at the ESOMAR Congress in 1976 and widely used since) asks each respondent four direct price questions about the product:

1. **Too cheap** — "At what price would you consider the product to be so *inexpensive* that you would question its quality and not want to buy it?"
2. **Bargain** — "At what price would you consider the product to be a *bargain* — a great buy for the money?"
3. **Getting expensive** — "At what price would you consider the product to start getting *expensive*, but still worth considering?"
4. **Too expensive** — "At what price would you consider the product to be so *expensive* that you would not consider buying it?"

Each respondent's four numbers get plotted as cumulative distributions across the sample. Four curves emerge:

- Cumulative *"too cheap"* — the fraction of respondents who find the price *at least* that cheap (descending as price rises).
- Cumulative *"bargain"* — descending (fraction who consider price at least this good a bargain).
- Cumulative *"getting expensive"* — ascending.
- Cumulative *"too expensive"* — ascending.

The intersections define four named points:

- **Point of Marginal Cheapness (PMC)** — intersection of "too cheap" and "getting expensive" — the lower bound of acceptable prices.
- **Point of Marginal Expensiveness (PME)** — intersection of "bargain" and "too expensive" — the upper bound of acceptable prices.
- **Optimal Price Point (OPP)** — intersection of "too cheap" and "too expensive" — the price at which the fraction rejecting for being too cheap equals the fraction rejecting for being too expensive.
- **Indifference Price Point (IPP)** — intersection of "bargain" and "getting expensive" — the price at which the fraction feeling the price is a bargain equals the fraction feeling it's expensive.

The **range of acceptable prices** is [PMC, PME]. The OPP is a modal price point inside that range.

```
% respondents
100 |xx
    |  xx           too expensive ____________/
 75 |    xx                         _________/
    |      xxx      getting exp. __/       /
 50 |         xxx  ________________.OPP___/
    |            xx    __.IPP___/
 25 | bargain      xxx      /
    |____xxxxx__       xxx/
  0 |         xxxxxxxx  too cheap
    +---------|---------|---------|---------|-------→ price
              PMC      OPP       IPP        PME
              lower    modal     bargain    upper
              accept   accept.   perceived  accept
```

**What PSM is good for:** getting a first-pass acceptable range and modal price when the product category is *familiar enough* that respondents can price it directly (they've bought analogous products; they have a mental reference). It is fast to run and interpretable without a statistician.

**What PSM is bad for:** genuinely new categories where respondents have no reference point. If the buyer has never bought anything like the product, her stated numbers are guesses. PSM in a category-creation setting produces noise dressed up as a curve.

**Sample size:** working practitioner minimums are **200-400 respondents** per segment for stable curves; **150 minimum** is quoted in some references but produces jittery intersections. If the target segment is a niche B2B ICP where 200 respondents does not exist, run PSM on a smaller pool (30-50) and treat the output as a *directional signal*, not a defensible curve — report the ranges as wide bands, not sharp points.

**Common misreads:**

- Treating the OPP as *the* price. The OPP is a modal point; the operating band is [PMC, PME]. Founders who ship the OPP without testing points inside the band under-explore the range.
- Running PSM on the wrong sample — free-tier users, general internet panel, existing customers. Only the target-ICP buyer's WTP curve is meaningful; a curve built from users who would not actually buy is decoration.
- Confusing "consider" with "purchase." Van Westendorp's questions ask about *consideration*, not stated purchase intent. A price inside the acceptable range means the buyer would not reject on price alone; it does *not* guarantee she would buy.
- Reading the PSM as if the sample were representative of the market when it was a panel of easy-to-recruit respondents. WTP curves are only as good as the sampling frame.

### Instrument 2 — Gabor-Granger

Gabor-Granger (Andre Gabor and Clive Granger, "Price Sensitivity of the Consumer," *Journal of Advertising Research* 1964; and Gabor, *Pricing: Concepts and Methods for Effective Marketing* 1988) asks each respondent whether she would purchase the product at a specific price. If yes, ask again at a higher price. If no, ask again at a lower price. Cycle until the highest-price-she-would-pay is bracketed.

The output is a **demand curve** — the fraction of the sample who would buy at each price point. Multiply by price to get an **estimated-revenue curve** whose peak is the *revenue-maximising* price:

```
    fraction     |                    revenue curve
    who buy      |                       (fraction × price)
       ↑         |
     100% |xxx   |xxx
          |   xx |    xxx
      75% |     x|       xxx
          |      |x         xxx        __.max
      50% |      |  xx     __.__.___.__/  \xx
          |      |    xxx_/                  \xxx
      25% |      | __xx  \___                   \xx
          | ____/xxxx     demand curve            \xx
       0  +------+-----+-----+-----+-----+-----+-----→ price
             low          mid                      high
```

**What Gabor-Granger is good for:** estimating a demand curve directly, when the product has clear enough definition that a respondent can answer "would you buy at $X" without prolonged setup. It is the standard instrument when the goal is to estimate a **revenue-maximising** price rather than a range of acceptable prices.

**What Gabor-Granger is bad for:**

- **Stated intent vs. real purchase.** Gabor-Granger measures *stated* buying intent, which reliably overstates real purchase behaviour. Practitioners typically discount the fraction-who-buy figures (a common convention is a 25-50% discount before treating the number as a purchase forecast).
- **Anchoring.** The first price shown to a respondent anchors her subsequent answers. Serious runs randomise the starting price across respondents; sloppy runs use a fixed start and produce a curve that reflects the anchor more than the market.
- **New categories.** Same limitation as PSM — without a reference, the respondent's buy/no-buy answer is a guess.

**Sample size:** working minimum **200-300 respondents** per segment for a smooth demand curve. Below 100 the peak of the revenue curve is unstable — it can shift by 20-30% with small sample changes. B2B niche runs (30-50 respondents) can still produce a signal but should report a *range* around the revenue-maximising price, not a point.

**Common misreads:**

- Treating the peak of the revenue curve as *the* price. The peak is one anchor; the pricing decision also has to consider adoption rate (a higher price yields more revenue per customer but fewer customers, which changes CAC payback and expansion dynamics not captured in the instrument).
- Not randomising the starting price and reporting the anchored answer.
- Applying no discount to stated buying intent and forecasting bookings against the raw fractions.

### Instrument 3 — Max-Diff (best-worst scaling)

Max-Diff (Jordan Louviere, working from the late 1980s; formalised in Louviere, Flynn & Marley, *Best-Worst Scaling: Theory, Methods and Applications*, 2015) is an **indirect** instrument. Instead of asking about price, it asks the respondent to look at short lists of features (or attributes, or benefits) — usually 4-6 items — and choose the *most important* and the *least important* item from each list.

Each respondent sees many such lists (typically 8-15 sets, drawn from a balanced design), which produces a preference-share estimate for every attribute in the master list. The output is a ranked list of attributes with **relative importance scores** that sum to 100 across the item set:

```
Attribute                    Preference share
────────────────────────────────────────────
1. Multi-repo dependency graph      22.4%
2. GitHub Actions integration       18.1%
3. Slack alerting                   14.7%
4. Historical trend reports         12.9%
5. Priority ticket routing          10.6%
6. SSO / SAML                        7.8%
7. On-prem deploy option             5.9%
8. Public API                        4.1%
9. Terraform provider                3.5%
```

**What Max-Diff is good for:**

- **Feature prioritisation for packaging.** Which features belong in the anchor tier (Chapter 3), which go into the premium tier, and which are decoration. The ranking is what the packaging decision should be calibrated against.
- **Pricing-metric selection input.** If "per-repo scanning" ranks near the top for the target segment, per-repo is a candidate pricing metric (Chapter 4); if "per-user access" ranks near the top, per-seat is a candidate.
- **Discriminating between segments.** Running the same Max-Diff across two ICP sub-segments often produces different rankings, which is the input to whether the product needs one packaging structure or two.

**What Max-Diff is bad for:**

- **Measuring price directly.** Max-Diff does not answer "how much will they pay." It answers "what matters most, relatively," which is a different question. Founders sometimes conflate the two and treat "the top-ranked feature must justify a premium tier" as if it also told them how much premium. It does not — the *how much* comes from PSM / Gabor-Granger.
- **Absolute importance.** The scores are relative (they sum to 100 within the item set). Removing or adding items changes every score. The instrument tells you the ordering, not the absolute weight.
- **Overloaded item lists.** More than 20-30 attributes exhausts respondents; the last third of the lists degrades. Working practice caps the master list at **12-20 attributes**.

**Sample size:** **150-300 respondents** produces stable rankings; below 100 the tail-end ordering is unreliable. Because Max-Diff uses a balanced experimental design, small samples produce noisy tail rankings even when the top three are stable — trust the top rankings more than the bottom in a small run.

**Common misreads:**

- Interpreting the score as "22.4% of buyers primarily want this" — it is not a purchase share; it is a *relative importance* share.
- Mixing categories in the item list — putting "SSO" alongside "cheaper price" alongside "faster onboarding" produces a ranking whose meaning is muddled. Every item in a Max-Diff should be at the same conceptual altitude (all features, or all benefits, or all attributes — pick one).
- Skipping the "sanity attribute." Practitioner-standard Max-Diff includes at least one obviously-important and one obviously-unimportant item. If the sanity attributes don't rank as expected, the sample is wrong.

### Trade-off summary — pick the instrument to the question

| Question you're trying to answer | Instrument | Why |
|---|---|---|
| What's the acceptable price *range* for this offering to this segment? | Van Westendorp PSM | Cheapest way to bracket the [floor, ceiling] band |
| What single price *maximises revenue* against my current demand curve? | Gabor-Granger | Direct demand-curve estimation; peak of revenue = fraction × price |
| Which *features* belong in which packaging tier? | Max-Diff | Ranked preference, calibrated across the segment |
| Which *pricing metric* (seat / usage / outcome) do buyers weight most? | Max-Diff on candidate metrics | Same instrument, different item list |
| Do two candidate segments have different WTP or different feature ranks? | Any of the above, run per segment | The comparison across segments is the actual output |

The three are complements, not substitutes. A serious pricing pack ships with all three signals: PSM for the acceptable range, Gabor-Granger for the revenue-maximising anchor inside the range, Max-Diff for the packaging cuts and metric-selection input. Founders who run only one — usually PSM, because it is the easiest — end up with a range but no packaging structure or metric, and end up guessing on both.

### Sample-size discipline — B2B vs. consumer

The 200-400-respondent working minimums quoted above assume a consumer-scale panel where recruiting 300 respondents is a $2K-$5K panel purchase and takes days. In B2B startup practice, the target segment is often **500-5000 companies total** in the world, of which perhaps **50-200 buyers** are practically reachable. The published sample-size guidance from consumer-research literature does not translate directly.

Working practice for early-stage B2B WTP:

- **30 respondents** is the minimum for any WTP instrument to produce even a directional signal. Below 30 the instrument is a survey with a chart, not a WTP curve.
- **50-100 respondents** is realistic for a well-resourced B2B startup with a defined ICP list and a founder willing to hand-recruit — this produces wide bands but useful comparison across sub-segments.
- **150-300** is achievable only for consumer / prosumer / very-large-ICP B2B; if the segment is smaller than that in total, do not attempt to fake a consumer-scale run.

When the sample is smaller than the guidance, be explicit about the confidence range:

- Report bands, not points. "The PMC is $60-$90" not "the PMC is $74."
- Segment interpretation is more valuable than absolute number. "Enterprise sub-segment shows PMC $180 vs. mid-market $60" is a defensible statement from a 30-respondent-per-segment run; "the OPP is $147" is not.
- Combine with observed WTP from actual founder-led sales calls (mod-105). A stated-price curve from 30 respondents plus 20 actual price-reactions from live discovery calls is a better signal than either alone.

### Recruiting the respondents — the same discipline as mod-101

WTP research fails at the recruiting step more often than at the instrument step. If the respondents are not the actual ICP buyer (mod-104), the curve reflects the wrong market's price sensitivity and every downstream decision is calibrated wrong.

Working recruiting rules:

- **Respondents must match the ICP scorecard** (mod-104). No off-ICP respondents "for the sample" — one buyer of a $500K enterprise deal has different WTP for the same product than 20 solo prosumers, and mixing them poisons the curve.
- **Recruit from the same channels the sales motion recruits from.** Panel respondents recruited from generic B2B panels behave differently than respondents recruited from the ICP-adjacent Slack community or the actual outbound list. The recruiting channel is a covariate on the WTP curve.
- **Compensate proportionally, not lavishly.** Consumer-panel gift-card compensation is fine for consumer runs. B2B ICP respondents who are being paid $500 to complete a 20-minute survey may be gaming the incentive — the answers are worth less. Non-cash compensation (early product access, a share of results, a favour banked) often produces better data.
- **Screen out competitor employees, journalists, students.** A single non-buyer respondent inside 30 is a 3.3% noise floor.

### Instrument mechanics — where the curve gets generated

The three instruments can be run in three progressively-heavier setups:

- **Founder-run on a Google Form / Typeform** with a spreadsheet analysis (PSM curves in a Sheet chart, Gabor-Granger with a simple binomial rule, Max-Diff by hand for small item sets) — appropriate for 30-100 respondents; free; the founder has to think about every intersection herself.
- **Practitioner tooling** — Sawtooth Software (the industry standard for choice-based methods including Max-Diff, ~$1K+ for a project seat), Qualtrics (PSM and Gabor-Granger templates in enterprise plans), Conjointly (mid-market pricing-research SaaS with PSM, Gabor-Granger, and Max-Diff modules) — appropriate for 100-500 respondents.
- **Full-service pricing consultancy** — Simon-Kucher, Vistio, PriceBeam — appropriate for post-Series-A pricing exercises where the wrong number costs $500K+. Not appropriate at seed stage; the exercise is the founder's, not a vendor's.

At seed stage, run the founder-tooled version. The point is that the founder herself has to look at the intersections and think about them; buying the curve from a consultancy without doing the reasoning produces a spreadsheet, not a pricing decision.

## Concrete example — Loomly runs all three instruments on a 60-respondent B2B sample

Loomly (the running mid-market devtools example from mod-103 / mod-104: dependency-graph SaaS for B2B engineering teams; ~$12K ACV target; ICP is 50-150-engineer B2B SaaS companies on GitHub) runs a WTP research cycle before committing to the v1 pricing pack.

**Step 1 — Recruiting.** The founder hand-recruits 60 respondents against the ICP scorecard: 20 from the outbound list she was already emailing (mod-105 Chapter 2's outreach targets), 20 from a devtools-focused Slack community she participates in, 20 from her mod-101 discovery-interview corpus (respondents who agreed to a follow-up). Every respondent's title is VP Engineering, Engineering Manager, or Head of Platform at a company matching the Layer-1 firmographics. Compensation: early access to Loomly's beta + a share of the anonymised aggregate results.

**Step 2 — PSM (Van Westendorp).** Each respondent answers the four price questions about a "dependency-graph SaaS priced per repository per month." Curves are plotted; intersections computed:

- PMC ≈ $2/repo/month — below this the buyer questions quality.
- OPP ≈ $6/repo/month — modal acceptable point.
- IPP ≈ $8/repo/month — bargain / expensive break-even.
- PME ≈ $14/repo/month — upper bound of the acceptable range.

Bands are wide (60 respondents in a niche B2B segment). The founder reports the *range* as $4-$12/repo/month and does not commit to $6 as a hard number.

**Step 3 — Gabor-Granger.** Each respondent gets asked "would you buy at $X/repo/month" with $X randomised per respondent from {$3, $5, $8, $12, $18}. The demand curve slopes down (100% at $3, ~5% at $18). The revenue curve (fraction × price × assumed 40 repos) peaks at ~$8/repo/month for a 100-repo customer, with the peak being flat between $7-$10 — a wide plateau that says the exact peak is not sharply defined by the sample.

**Step 4 — Max-Diff.** The item list has 14 attributes (dependency-graph accuracy, GitHub Actions integration, Slack alerting, historical trends, priority routing, SSO, on-prem deploy, public API, Terraform, GitLab support, Bitbucket support, per-commit scanning, PR-time scanning, monorepo support). Each respondent completes 12 best-worst sets. Rankings:

1. Dependency-graph accuracy — 21%
2. GitHub Actions integration — 17%
3. PR-time scanning — 14%
4. Slack alerting — 11%
5. Historical trends — 9%
6. Monorepo support — 8%
7-14. All under 7%, with SSO and on-prem clustering around 4% each.

**Step 5 — Interpretation.** The three instruments converge to:

- **Acceptable pricing band:** $4-$12/repo/month, with $7-$10 as the revenue-maximising sub-band.
- **Anchor tier composition:** the top-4 features (accuracy, GitHub Actions, PR-time scanning, Slack alerting) belong in the anchor tier — buyers ranked these as core.
- **Premium tier features:** SSO, on-prem deploy, priority routing rank low in the mid-market segment but the founder plans to run Max-Diff separately against enterprise-adjacent respondents to check whether SSO / on-prem ranks differently there.
- **Pricing-metric signal:** the ICP thinks in terms of *repositories*, not seats or scans — the metric conversation is per-repo, per-scan, or per-project. Chapter 4 develops this decision.

The founder does not commit to $8/repo. She commits to a range and an experiment plan: v1 launches with a $6/repo anchor tier and a $12/repo premium tier, and Chapter 5's experiments will move the anchor within the acceptable band based on close rate + expansion signal from actual sales.

## Common failure patterns

- **Skipping WTP research entirely.** Founder picks $99 because it "feels right." Twelve months later the pricing is still $99 because there is no framework to change it against. The absence of WTP research is itself a decision — one that locks in the founder's intuition as the market's value math.
- **The one-friendly-buyer trap.** Founder asks three trusted buyers "would you pay $X" and takes the yes as evidence. Friendly buyers give yes answers to preserve the friendship; the yes is a data point about the relationship, not the price. WTP research is structured so the respondent can say no without social cost.
- **Wrong instrument for the question.** Founder runs Max-Diff and reports "the answer to what we should charge is $99." Max-Diff does not answer that question. Or founder runs PSM in a category-creation setting where respondents have no reference and reports the OPP as if it were a price recommendation.
- **Under-sampling and reporting sharp numbers.** 30 respondents produces a directional signal; reporting the OPP to the nearest dollar off 30 respondents fakes precision. Report bands, or say the sample is small.
- **Off-ICP respondents.** WTP curve is built from panel respondents who would not buy the product. The curve reflects the wrong population and every downstream decision inherits the error.
- **Anchoring in Gabor-Granger.** Every respondent sees $99 first. The demand curve peaks near $99 for reasons that are entirely about the anchor. Randomise the start.
- **Confusing stated WTP with real WTP.** Real purchase behaviour is lower than stated intent by a factor of 2-3× at high prices. Founders who forecast bookings from raw Gabor-Granger fractions over-forecast by 100%+ and then panic when close rate looks weak.
- **Running WTP once at seed and never again.** The market moves, the product moves, the competitive alternatives move. A WTP study run at seed is stale by Series A. Re-run at each pricing-pack revision (Chapter 6).
- **Buying the curve from a consultancy at seed stage.** The founder has to do the reasoning; the consultant produces a slide deck the founder cannot defend against a board question. Founder-tooled WTP at seed; consultancy at scale.
- **Reporting the OPP as *the* price and moving on.** The OPP is one anchor. The pricing decision also has to consider packaging (Chapter 3), the pricing metric (Chapter 4), competitive alternatives, and the experiment plan (Chapter 5). WTP research is an input, not an output.

## Summary

- Willingness-to-pay research is the discipline of asking buyers about price in a structured way that produces a *distribution*, not a point estimate. The output is a curve the founder can test, refute, and iterate against — not a single number to commit to.
- **Van Westendorp PSM** — four price questions per respondent, curves intersect at PMC / OPP / IPP / PME, output is a **range of acceptable prices**. Good for familiar categories, bad for category creation, requires 200-400 respondents at consumer scale (30-100 with wide bands in B2B niche).
- **Gabor-Granger** — direct accept / reject at randomised prices, output is a **demand curve** whose peak (× price) gives the **revenue-maximising** price. Good for direct demand estimation, bad for stated-vs-real gap, requires anchoring discipline.
- **Max-Diff (best-worst scaling)** — indirect **feature-preference** ranking; output feeds packaging (which features go in which tier) and pricing-metric selection (which axis to charge on). Does not measure price directly.
- The three are complements — a serious WTP pack ships all three signals. Skipping one produces a partial picture: PSM alone gives a range with no packaging structure; Gabor-Granger alone gives a peak with no feature ranking; Max-Diff alone gives features with no price.
- **Sample-size discipline** — the consumer-panel 200-400 minimums do not translate to niche B2B. Working practice: 30 is the floor for directional signal, 50-100 is realistic for early-stage B2B, 150-300 is achievable only in consumer / prosumer / large-ICP settings. Report bands, not points, when the sample is small.
- **Recruiting discipline** — respondents must match the ICP (mod-104); recruiting channel is a covariate; compensation shouldn't game the sample. Off-ICP respondents produce curves for the wrong market.
- **Common misreads** — treating the OPP as *the* price, skipping randomisation in Gabor-Granger, confusing Max-Diff relative scores with purchase intent, forecasting bookings from raw stated-intent fractions.
- WTP is the *empirical anchor* for the rest of the module. Chapter 2 computes the value ceiling from buyer economics; Chapter 3 arranges the price into tiers; Chapter 4 chooses the metric. All three depend on the WTP curve as input.
