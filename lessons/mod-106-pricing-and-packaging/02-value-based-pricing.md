# Value-Based Pricing — Anchoring to the Buyer's Economic Outcome

## Motivation

The WTP research in Chapter 1 tells the founder what the buyer will *say* about price. It does not tell her what the buyer *should* pay. The two are frequently — sometimes dramatically — different, because most buyers don't do the ROI math themselves before answering a survey. The buyer's stated WTP is anchored to prices she's already seen in the category; the buyer's *value-defensible* price is anchored to what the product actually does for her P&L.

**Value-based pricing** is the discipline of setting price against the *buyer's economic outcome* — the ROI, the hours saved, the seats replaced, the incident cost avoided, the deal cycle shortened — rather than against internal cost or competitor sticker. The output is a price the founder can *defend* in a sales conversation with a spreadsheet: "our product saves your team ~$180K/year in cycle-time cost; we charge $18K/year; you're keeping 90% of the value we create." Once that math exists on a slide, the founder is negotiating from ROI, not from a rate card the buyer can undercut.

The failure modes this chapter exists to catch:

- **Cost-plus pricing** — the founder computes fully-loaded cost per customer ($240 / year for hosting, support, and gross margin overhead), applies a 5× markup, and lands at $1200 / year — a number that has no relationship to what the buyer values the product at, and is often 10× under what the value math would support.
- **Competitor-sticker pricing** — the founder finds three competitors charging $99, $149, and $199 and picks $99 to "undercut," ceding the entire value story to whoever priced first (usually the incumbent whose price was itself set by the market's earliest guesser).
- **Willingness-to-pay-only pricing** — the founder runs Van Westendorp, finds the OPP is $99, and ships $99 without checking whether the value math would support 3× that. The stated WTP is *floor* information, not *ceiling* information; treating it as the ceiling caps the ARPU permanently.

This chapter fixes the value-based-pricing derivation as a repeatable exercise: identify the buyer's economic outcome, translate it into a dollar-denominated value equation, anchor the price at a defensible share of that value, and pressure-test the derivation against the WTP research and the mod-105 discovery script. Chapter 3 arranges the value-defended price into tiers; Chapter 4 chooses the metric it's charged on; the whole module rests on this chapter's discipline.

## Core concepts

### The three pricing anchors — recap and where value fits

Chapter 1 introduced Nagle & Müller's three anchors. Restating them with a sharper focus on value:

- **Cost** — sets the *floor*. Charging below fully-loaded cost destroys unit economics. Cost alone does not set price.
- **Competitor** — sets a *reference point* for the buyer. If the buyer's mental model of "what dependency-graph tooling costs" is $10K/year (because that's what SnykOSS costs), pricing at $50K/year requires the founder to move the buyer's reference point — feasible, but not free. Competitor prices constrain the *narrative*, not the *number*.
- **Value** — sets the *ceiling*. The dollar-denominated value the buyer captures from the product is the maximum a rational buyer would pay before the ROI equation goes negative. Value alone does not set price either — pricing at the ceiling captures 100% of the value the buyer created; pricing below it captures some fraction the buyer keeps as ROI.

Value-based pricing is the discipline of computing the value ceiling, and then choosing a price *inside* that ceiling that (a) leaves enough ROI on the table for the buyer to say yes and (b) captures enough of the value for the vendor to build a business. The strategic conversation is about the *ratio* — the "value share captured" — not about the price in isolation.

### The value equation — the buyer's economic outcome, in dollars

Every value-based pricing derivation starts with an **economic outcome** — one thing the product changes about the buyer's business that can be measured in dollars per unit of time. The outcome has to be:

- **Buyer-owned.** A metric the buyer's team already reports up. If the founder invents a metric ("developer joy score") that no VP Engineering reports to her CFO, the value story does not translate to the buyer's spreadsheet.
- **Dollar-denominated.** Hours × hourly rate. Seats × seat cost. Incidents × incident cost. Deals × deal size. The unit has to reduce to dollars per year (or dollars per event) — otherwise the ROI math has no denominator and the price is arbitrary.
- **Attributable.** The buyer must credibly believe the product is what caused the outcome to change. "You'll increase revenue by 3%" is a value claim; attributing that 3% to the product specifically is a separate argument the founder has to win.

**Common value-equation templates for B2B software:**

1. **Hours saved × hourly rate.** Product saves N hours / week per user × $H fully-loaded hourly rate × 52 weeks = $ annual value / user. Multiply by users. Standard for tools that displace manual work.
2. **Seats replaced × seat cost.** Product replaces some fraction of an existing tool's seats (or of a headcount role). Value = seats × (old cost - new cost). Standard for consolidation plays.
3. **Incidents avoided × incident cost.** Product reduces N incidents / quarter × $I average incident cost = $ value / quarter. Standard for observability, security, reliability tools.
4. **Cycle time × cost of delay.** Product shortens a business cycle (deploys, deal cycle, month-end close) by D days × $C per day of delay = $ value / cycle × cycles / year. Standard for developer productivity, sales-cycle acceleration, finance-ops tools.
5. **Revenue enabled × attributable share.** Product enables the buyer to close revenue that would not have closed = $R attributable × attribution % = $ value / year. Standard for demand-gen, revenue-ops tools. Requires the strongest attribution argument.
6. **Risk avoided × probability × severity.** Product reduces the probability of a rare, high-cost event = P × S = $ expected value / year. Standard for security, compliance, insurance-substitute tools. Requires named event definitions the buyer's team already accepts.

The founder's derivation picks one primary equation — the one the buyer's ICP most naturally reasons in — and treats the others as supporting cross-checks. **Multiple equations that agree** produce a defensible ceiling; **one equation** produces a marketing slide.

### The 10-20-25% capture rule of thumb

Once the value equation gives an annual dollar figure per customer, the pricing question is: how much of that value does the vendor capture, and how much does the buyer keep as ROI?

The practitioner rule of thumb (widely used in B2B SaaS pricing, referenced in Ramanujam & Tacke, *Monetizing Innovation*, 2016, and in Simon-Kucher's published writing) is that a healthy value-share for a differentiated B2B product is roughly **10-25% of the annual value created for the buyer**, with:

- **10% or lower** — commodity or highly-competitive category, low pricing power. The buyer expects to keep 90%+ of the value.
- **15-20%** — mid-market defensible SaaS. The buyer sees 4-7× ROI on the annual spend, enough to defend the purchase easily.
- **25-30%** — high-differentiation, high-switching-cost, category-leading product. The buyer sees 3-4× ROI, still positive but with meaningful vendor capture.
- **Above 30%** — either the buyer has no alternative and the vendor is a temporary monopoly, or the value equation is over-stated. Usually the latter.

The *specific* target inside the band is a strategic choice. Higher capture means higher ARPU but slower adoption (higher price, more objections); lower capture means faster adoption but leaves ARPU on the table. At seed / early stage, the working default is **~10-15% capture** — the goal is to get customers on the board quickly enough to close the CDD loop (mod-101 discovery → mod-102 PMF → mod-105 sales), and the extra 10 points of capture is worth less than the extra 30% adoption speed. At Series-A and beyond, the working default drifts toward **~15-25% capture** — the CDD loop is closed, the value story is defensible, and the ARPU lift compounds through the funnel.

This rule of thumb is a *sanity check*, not a formula. If the value equation says annual value is $500K and the vendor's price is $100K, the 20% capture is defensible. If the value equation says annual value is $500K and the vendor's price is $10K, the 2% capture means either the founder is under-pricing dramatically or (much more likely) the value equation is inflated. Both directions of divergence from the rule are signals to re-examine.

### Working the derivation end-to-end

The value-based-pricing derivation is a five-step exercise that produces one worksheet per ICP segment. Every step has to be defensible in a sales conversation:

**Step 1 — Name the economic outcome.** Pick the *one* outcome that the buyer's persona (mod-104) already reports up her chain. "PR review cycle time" for a VP Engineering with a cycle-time KPI. "Time to first response" for a Support Ops leader. "Attributed pipeline" for a Head of Demand Gen. If no such KPI exists in the buyer's world, the outcome is unownable and the value story doesn't survive a discovery call — go back to mod-104 and re-check the persona.

**Step 2 — Write the value equation.** In dollars per year (or dollars per event × events per year). Pick one primary equation from the six templates; note one or two supporting cross-checks. Every input must be a *number the buyer can source* — either from her internal reporting, or from a public benchmark the buyer will accept.

**Step 3 — Compute the per-customer annual value.** Fill in the equation with the buyer's actual (or benchmarked-plausible) inputs. Produce a range, not a point — a "conservative case" and a "likely case" the buyer can pick between. The conservative case is what she takes to her CFO; the likely case is what she uses internally to justify the purchase to herself.

**Step 4 — Choose the value-capture ratio.** Given the category dynamics (commodity vs. differentiated), the current stage (early-stage seeking adoption vs. growth-stage optimising ARPU), the pricing power narrative (Chapter 3's packaging), and the competitor-sticker anchor, pick a target capture ratio (10-25% band). Multiply by the conservative annual value to get the anchor price.

**Step 5 — Cross-check against WTP research and competitor sticker.** The anchor price from Step 4 has to be:
- Inside the [PMC, PME] band from Van Westendorp (Chapter 1). If it's above PME, the value equation may be right but the buyer's stated WTP is a constraint that will force a discount, a proof-point requirement, or a longer sales cycle. If it's below PMC, the pricing is under-anchored and the founder should reconsider.
- Within the [0.5×, 2×] range of the competitor sticker for the reference alternative. Outside that range requires a narrative move (Chapter 3 packaging + mod-103 positioning) to reframe the reference.
- Consistent with the observed reactions in mod-105's actual sales calls. If the founder has quoted the target anchor to 5+ live buyers and every one has recoiled, the derivation is wrong somewhere.

**Output:** a one-page value worksheet with the equation, the inputs, the range, the capture ratio, and the anchor price — plus explicit notes on how it relates to Chapter 1's WTP curve and the competitor stickers. This worksheet becomes the "value" slide in the mod-105 discovery / demo flow, and the anchor tier's price in Chapter 3's packaging.

### The buyer-value slide — how the derivation lands in the sales conversation

The value derivation isn't a private founder exercise. It has to land in the sales conversation as a slide the buyer can walk out of the meeting with. The slide has four elements:

1. **The named outcome** — "Your team's PR review cycle time." The specific KPI the buyer's persona owns.
2. **The current-state number** — "Currently ~3.2 days (industry benchmark: ~1.5 days for similar-size teams)." The buyer's or benchmark number, with source.
3. **The changed-state math** — "Loomly customers of similar size reduce cycle time to ~1.6 days. For a 50-engineer team, that's ~$180K/year in recovered developer time, using the DORA cost-of-delay methodology at $500/day/engineer."
4. **The ratio slide** — "Loomly costs $18K/year. Your team keeps 90% of the value we create."

The slide is the value derivation compressed to one screen. If the founder cannot get the value story onto one screen, the derivation isn't tight enough for a sales conversation. Buyers do not sit through 12-slide ROI decks. One screen, four numbers, one attribution argument.

### When value-based pricing breaks — the three failure modes

Value-based pricing fails cleanly in three ways.

**Failure 1 — the buyer doesn't believe the attribution.** The value equation is right, the number is defensible, but the buyer thinks "yeah, my cycle time will improve, but maybe half of that is us adopting Kubernetes at the same time, not your product." The attribution argument is where value-based pricing lives or dies. Fixes: proof points (mod-105 case studies), pilot programmes (see if cycle time drops during the pilot), attribution structure (before / during / after measurement with the buyer as her own control).

**Failure 2 — the outcome isn't buyer-owned.** The value equation is about "developer productivity;" the buyer is a CFO who does not have a developer-productivity line item. The founder built the value equation for the wrong persona. Fix: mod-104's persona split — the value equation for the *economic buyer* (CFO) is different from the value equation for the *champion* (VP Eng), and the sales conversation needs both.

**Failure 3 — the ratio is wrong.** The math says the buyer keeps 90% of the value, but the buyer's mental model of "software products cost $10-20K/year for our size" caps the price regardless. The value math is right; the anchor from the buyer's category reference beats the value story. Fix: reframe the category (mod-103 positioning) so the buyer's reference class changes — or accept the ratio the market gives you (higher capture, lower price) and price against WTP + competitor rather than value.

The last failure is the most common and the most important. Value-based pricing is *aspirational* against a category's existing reference — it has to be paired with positioning work that moves the reference. Without the positioning move, the buyer says "I understand the math, but that's not what tools like this cost" and the value story loses. This is why mod-103 (positioning) has to precede mod-106 (pricing) in the module dependency graph.

### Value-based pricing vs. willingness-to-pay — the resolution rule

The obvious question after Chapters 1 and 2: what happens when the value ceiling and the stated WTP disagree? The resolution rule:

- **If value ceiling > stated WTP by 2× or less:** the value story is defensible and the stated WTP is under-anchored. Price at the low end of the value band (~10-15% capture), lead with the value slide in the sales conversation, expect a longer sales cycle as the buyer's reference moves.
- **If value ceiling > stated WTP by 3× or more:** either the value equation is inflated (most likely) or the category's stated-price anchor is very sticky (also likely). Price closer to the WTP band, use the value story as a *narrative* argument for premium positioning, but do not expect the buyer to pay the value-derived price on the first cycle. Re-run WTP after 6-12 months of case-study accumulation.
- **If value ceiling ≈ stated WTP:** the two anchors converge; price with confidence in the middle. This is the healthiest state.
- **If value ceiling < stated WTP:** unusual, and usually means the founder is under-computing value. Re-check the equation; the buyers know something the founder hasn't yet translated into her spreadsheet.

The rule is not "always pick the higher number" or "always pick the lower number." It is that value and WTP are *two different measurements of the ceiling* — value from the buyer's economics, WTP from the buyer's stated reaction — and the gap between them is a diagnostic signal about the pricing narrative work still to do.

## Concrete example — Loomly derives value-based pricing against the mid-market ICP

Continuing the running Loomly example. After the WTP research (Chapter 1) produces a $4-$12/repo/month acceptable range with a $7-$10 revenue-maximising sub-band, the founder runs a value-based derivation to test whether the WTP band is under-anchored, over-anchored, or right.

**Step 1 — Named outcome.** VP Engineering (mod-104's economic buyer for the mid-market segment) reports up on **PR review cycle time** and **deploy frequency**. Both roll into the DORA metrics the CTO reports to the CEO quarterly. The named outcome for the value equation is **PR review cycle time**.

**Step 2 — Value equation.** Cycle-time × cost-of-delay:

```
Value = (baseline cycle time - improved cycle time) × cost per day of delay × active PRs / year
      = (3.2 days - 1.6 days) × $500/day/engineer × 800 PRs/year
      = 1.6 × $500 × 800
      = $640,000 / year of recovered engineering capacity

(For a 50-engineer team; scales roughly linearly with team size.)
```

Inputs sourced:
- Baseline cycle time: buyer's own dashboard (or DORA benchmark: 1-7 days for medium performers).
- Improved cycle time: Loomly's own aggregated customer data across 8 similar-sized customers (currently: mean 1.7 days, median 1.5 days).
- Cost per day of delay per PR: DORA 2023 "Accelerate State of DevOps" report methodology + $500/day fully-loaded engineer cost. Conservative case uses $300/day; likely case uses $500/day.
- Active PRs / year: 800 for a 50-engineer team is derived from Loomly's telemetry (avg 16 PRs/engineer/year); replaceable with buyer's own GitHub Insights number.

Conservative case: $384K / year of recovered capacity. Likely case: $640K.

**Step 3 — Per-customer annual value:** Conservative $384K, likely $640K, for a 50-engineer team.

**Step 4 — Capture ratio.** Loomly is early-stage seed, differentiated (no direct competitor in the "cross-repo dependency graph for GitHub-based B2B SaaS teams" segment), moving fast to close CDD loop. Working default: **10-12% capture**.

- 10% of $384K conservative = $38.4K / year.
- 12% of $640K likely = $76.8K / year.

Anchor price range from value math: **$38K-$77K / year for a 50-engineer team**.

**Step 5 — Cross-check.** The 50-engineer team has ~100 repos in Loomly's segment (2:1 repos-per-engineer heuristic, verified in-sample). The Van Westendorp OPP was $6-$8/repo/month, which for 100 repos is $600-$800/month = $7.2K-$9.6K/year. Gabor-Granger revenue-max was $7-$10/repo = $8.4K-$12K/year.

The value math ($38K-$77K/year) is **4-8× the WTP ceiling** ($10K/year). Diagnostic:

- The value ceiling is defensibly derived and the equation is not inflated (Loomly has customer telemetry, not assumptions, backing the improved-cycle-time input; DORA methodology backs the cost-of-delay input).
- The stated WTP is anchored to what the mid-market VP Engineering pays for *dev tools she already knows about* — Snyk, Sentry, DataDog agent add-ons, LinearB — which cluster in the $2-$10/repo/month or $10-$50/seat/month bands.
- The gap is a positioning problem, not a value problem. The buyer thinks Loomly is "another dev tool," priced against dev tools; the value math says Loomly is closer to "productivity platform" priced against productivity outcomes.

**Founder's resolution.** Following the resolution rule (value ≥ 3× WTP → price closer to WTP, use value as narrative, run experiment cycles): v1 anchor tier prices at $12/repo/month = $14.4K/year for a 100-repo team. That's above the OPP of $8/repo, below the revenue-max upper end, above the WTP-only ceiling of the OPP by 50%, and captures ~2-4% of the conservative value (10-30× under the value-derived ceiling).

The founder documents the derivation and *the gap* explicitly in the pricing pack (Chapter 6). The gap is the target of Chapter 5's experiments — accumulate case studies over 6-12 months, re-run WTP research, and move the price up the ladder as the reference class shifts. The value math sets the ambition; the WTP research sets the current constraint; the experiments close the gap.

## Common failure patterns

- **Cost-plus pricing dressed up as value-based.** Founder computes cost, applies a markup, calls it "value pricing" because she said the word "value" in the sales conversation. The number has no relationship to any buyer outcome. Test: can the founder point at the specific dollar figure of buyer value on a slide? If not, it's cost-plus.
- **Competitor-sticker pricing dressed up as value-based.** Founder prices at 80% of competitor sticker "because we're a challenger." The number is anchored to whoever priced first, not to the buyer's economics. The value math is decorative. Test: if the competitor moved their price 20% tomorrow, would this pricing move too?
- **The unownable-outcome trap.** Founder picks "developer happiness" or "team collaboration" as the value outcome. The buyer's persona has no KPI for either. The value equation exists on the founder's slide and nowhere in the buyer's spreadsheet. Fix: only use outcomes the buyer's persona already reports up.
- **The un-attributable-outcome trap.** The outcome improves during the pilot, but the buyer thinks Kubernetes / hiring / general team maturation caused the improvement. Fix: attribution structure — before/during/after measurement, buyer-as-her-own-control, comparable-team baselines. If attribution is genuinely weak, the value math has to be discounted; a 50%-attributed outcome captures 50% of the value ceiling.
- **The inflated-equation trap.** Founder assumes 100% of the theoretical value at maximum benchmark input. Real deployments capture 30-70% of theoretical. Working practice: report the equation at a **conservative** case (30-50% capture of theoretical) and a **likely** case (50-70%), never at the theoretical maximum. Buyers who have been burned by inflated ROI decks discount the whole story.
- **Capture-ratio miscalibration.** Founder picks 40% capture because "our product is really valuable." Buyer sees the price relative to the value math, computes she's keeping only 60% of the value, and does not close. Capture > 30% requires a monopoly narrative most seed-stage products cannot support. Default 10-25%.
- **Value-based pricing without positioning.** The value math says the price should be 5× the category reference. Positioning still puts the product in the same category as the reference. Buyer's mental price ceiling wins. Fix: mod-103 positioning has to move the reference class *before* the value pricing lands.
- **Reporting a single number instead of a range.** The value equation has 4-5 inputs, each with uncertainty. Reporting "value is $640K" pretends precision that does not exist. Report ranges — conservative and likely — and let the buyer pick which one to defend to her CFO.
- **Not running the derivation per segment.** The value equation for enterprise ($10M value ceiling for a 500-engineer team) is different from mid-market ($500K for 50-engineer) is different from SMB ($50K for 10-engineer). One derivation per ICP segment is the working discipline; a single derivation across all segments over-fits to one segment and under-serves the others.
- **Skipping the buyer-value slide in the sales conversation.** The founder derives the value math privately, prices against it, and then never shows the buyer the math. The buyer defends the purchase to her CFO with no ROI story and gets pushed back. The value slide isn't optional — it's the artifact the buyer walks out with.

## Summary

- **Value-based pricing** anchors price to the buyer's dollar-denominated economic outcome — hours saved, seats replaced, incidents avoided, cycle time recovered, revenue enabled — rather than to internal cost (which sets the floor) or competitor sticker (which sets a reference).
- Every derivation starts with a **named outcome** that the buyer's persona already reports up. If the outcome is unownable by the buyer, the value story does not survive a discovery call. Six standard value-equation templates cover most B2B software: hours × rate, seats × cost, incidents × cost, cycle × cost-of-delay, revenue × attribution, risk × probability × severity.
- **Value capture** is the vendor's share of the value created. Working defaults: 10-15% at early-stage seeking adoption, 15-25% at differentiated growth-stage, 25-30% only with high switching cost and category-leader positioning. Above 30% is either a temporary monopoly or an inflated equation.
- The five-step derivation — **name the outcome, write the equation, compute the range, choose the capture ratio, cross-check against WTP + competitor + live sales reactions** — produces a one-page value worksheet that becomes both the anchor-tier price (Chapter 3) and the sales-conversation "value slide."
- The buyer-value slide has four elements: named outcome, current-state number, changed-state math, ratio (buyer's kept share of the value). If the founder cannot compress the value story onto one screen, the derivation isn't tight enough for a sales conversation.
- **Three failure modes** — the buyer doesn't believe the attribution (fix: proof points, pilot structure), the outcome isn't buyer-owned (fix: mod-104 persona re-check), the ratio is wrong relative to the category reference (fix: mod-103 positioning to move the reference class).
- **Resolution rule when value ceiling and WTP disagree** — 2× gap: price low-end of value band, lead with the value slide. 3×+ gap: price closer to WTP, use value as narrative, run experiments to close the gap over 6-12 months. Convergence: price with confidence in the middle. Value < WTP: re-check the equation.
- Value-based pricing without positioning work fails. The buyer's category reference class beats any value equation until the reference class is moved. Mod-103 positioning is a prerequisite for mod-106 value-based pricing to land; the module dependency graph reflects this.
- The output of this chapter is the **value worksheet per ICP segment** — one primary equation, one range, one capture ratio, one anchor price, one slide. That anchor price becomes the input to Chapter 3's packaging tiers.
