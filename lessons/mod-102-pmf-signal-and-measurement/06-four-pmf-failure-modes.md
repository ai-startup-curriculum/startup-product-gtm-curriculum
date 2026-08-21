# The Four PMF Failure Modes

## Motivation

"We don't have PMF" is not one problem. It is at least four problems that look identical from the outside — a flat retention curve and a sub-40% Sean Ellis score — and require completely different remedies. Team A pivots to a new market when the fix was a $200 tier. Team B rebuilds the product when the fix was a landing page. Team C hires an SDR when nobody in the market wants the product at all. The wrong diagnosis burns quarters and can burn the whole runway.

This chapter names the four failure modes at the level of resolution a Chapter 3 survey + Chapter 4 retention read can distinguish, gives you the diagnostic that separates them, and — as important — tells you **which downstream module the failure routes to**. The failure mode determines the module; the module is where the actual fix lives.

## Core concepts

### The four modes — a one-line taxonomy

The four failure modes, in the order they typically appear when you work through a PMF diagnostic:

| Mode | The claim | The signature |
|---|---|---|
| **1. Wrong market** | No one wants the thing you're building at all. | Sean Ellis <15% across every segment; retention decays to zero across every segment; no free-text convergence on any main benefit. |
| **2. Wrong product** | People want the thing, but not this shape of thing. | Sean Ellis 15–30% aggregate but no segment above 35%; retention decays but slower than wrong-market; free-text names benefits you *don't* deliver. |
| **3. Wrong distribution** | People want it, and this shape works, but they never encounter it. | Sean Ellis ≥40% in a small n; retention flattens strongly on the actives; but top-of-funnel volume is a trickle and the acquired users all came from one narrow channel. |
| **4. Wrong price** | They want it and this shape works and they can find it, but they can't or won't pay what you're charging. | Sean Ellis ≥40% and retention flattens on the free-trial cohort; conversion to paid collapses at the price point; paid users retain but the paid cohort is tiny. |

The four modes are not mutually exclusive — a startup can have wrong-market *and* wrong-product simultaneously, or wrong-distribution stacked on top of wrong-price. But the diagnostic sequence below moves through them in an order that catches the biggest, most catastrophic mode first.

### Mode 1 — wrong market

**The claim:** the *problem* you built for is not a problem anyone will pay to solve. Alternatively, the segment you built for does not exist at the size or intensity you assumed.

**How to know:** the Sean Ellis score is low across **every** segment you can slice by; free-text "who benefits most" answers do not converge on any coherent segment; retention decays to zero across every cohort; the discovery corpus from mod-101 — reread with a hard eye — shows people were polite in interviews but did not describe the problem in unprompted specifics. The tell is that **you cannot find even a small n where the score is high**. If mid-market design agencies score 55% and enterprise scores 5%, you have wrong-*segment*, not wrong-*market*; if *every* slice is under 20%, the market is not there.

Wrong market is the most expensive failure mode to be in and the one founders resist naming, because the fix is to change what you are building. Some percentage of the time, a re-segmentation inside a broader market does the job — the underlying market exists but you had the wrong sub-segment — and the fix is a mod-101 re-discovery loop. Some percentage of the time, the market does not exist at your intended scale at all, and the fix is a pivot.

**Route:** back to **[mod-101](../mod-101-customer-discovery-and-problem-validation)** — re-run discovery interviews against a hypothesis about a different segment or a different problem. Do not try to fix wrong-market with distribution or price work; every downstream module is built on the assumption of a real market.

### Mode 2 — wrong product

**The claim:** the problem is real and the segment is real, but your *product shape* does not deliver on it. Users describe a benefit they *want* to receive; when they try the product they receive a different benefit; they leave.

**How to know:** the Sean Ellis score has a segment or two around 15–30% but none crosses 40%; the very-disappointed cohort is small; the free-text on "main benefit" is *thin* — users struggle to name what they get — or it names a benefit you did not intend and do not deliver well. The "how to improve" free-text asks for features that would fundamentally reshape the product, not incremental improvements. Retention curves in the segment where you would expect PMF decay steadily.

The subtle tell: the discovery interviews (mod-101) surfaced clear jobs and outcomes, but your product only weakly serves them. The problem exists; the shape of your solution is a partial answer. Wrong product is often the *result* of a mod-101 discovery report where the JTBD outcomes did not have enough constraint to reject the wrong solution shape (mod-101 Chapter 4's rejection drill exists to prevent this).

**Route:** back to **[mod-101](../mod-101-customer-discovery-and-problem-validation)** to re-audit the JTBD outcomes and the solution rejection drill, and then **iterate the product against the modal-benefit statement** using the Chapter 5 engine. Wrong product is the failure mode Superhuman was in at 22%. The engine (Chapter 5) is the remedy — provided the segment and market are real.

### Mode 3 — wrong distribution

**The claim:** the product works in its segment, the segment wants it, but the segment cannot find it. You have PMF in the users you managed to reach; you cannot reach enough of them for the fit to matter.

**How to know:** the Sean Ellis score in your actives is high — often ≥40% — but **your total active-user count is small** and heavily concentrated in one acquisition channel (a founder's network, a single high-signal launch, a single community). Retention curves in the segment flatten strongly. Free-text is convergent on both segment and benefit. Users report having heard about the product from one specific place, or from a personal contact. The waitlist / signup flow is quiet when you stop pushing.

Wrong-distribution is often mistaken for weak PMF because the *scale* is small. But scale is not fit — a 40 mid-market-design-agency active-user base with 55% very-disappointed *is* PMF in that segment; you have not proven the growth hypothesis (mod-108) yet, but the value hypothesis is proven.

**Route:** forward to **[mod-108](../mod-108-demand-generation-and-channels)** — channel selection, channel-market fit, one primary channel per stage. Wrong-distribution is a channel problem, not a product problem. The engine (Chapter 5) will not fix it; the retention is already strong. What is missing is a scaled way for the ICP to encounter the product.

### Mode 4 — wrong price

**The claim:** the product works, users find it, they use it — but they will not pay what you're asking, or the pricing model / packaging does not match how they buy.

**How to know:** the Sean Ellis score on the **free** or **trial** cohort is high; retention on the trial cohort flattens; but **conversion to paid is <10%** at the current price and free-to-paid drop-off happens sharply at the moment the paywall activates. Free-text mentions the price ("we love it, but $X is too much for our budget", "we couldn't get our procurement to buy a per-seat plan", "there's no plan that fits our team shape"). Paying users retain well; the paying cohort is just tiny.

Wrong-price splits into two sub-failures worth naming:

- **Wrong price point.** The value is real, users would pay, but not $X. Van Westendorp / Gabor-Granger research surfaces this cleanly (mod-106 Chapter 1 on WTP methods).
- **Wrong pricing metric.** The unit you charge on does not match how value accrues to the buyer. Per-seat pricing on a product where value is per-transaction misprices badly; per-transaction on a workflow-tool with unpredictable volume kills forecastability. This is a mod-106 mid-module problem.

**Route:** forward to **[mod-106](../mod-106-pricing-and-packaging)** — willingness-to-pay research, value-based pricing, packaging tiers, price-metric selection. Wrong-price is not a product problem — the product is working. It is a pricing / packaging problem, and mod-106 is where the fix lives.

### The diagnostic tree — which mode am I in?

Run the diagnostic in this order. It catches the most catastrophic mode first and does not waste diagnostic effort on higher-order modes when a lower-order one has already fired.

```
Q1. Does *any* segment score ≥40% "very disappointed" with retention that flattens?
      no  -> Q1a. Does *any* segment score ≥25% with retention that flattens or bends?
                   no  -> WRONG MARKET     (Mode 1) -> mod-101
                   yes -> WRONG PRODUCT    (Mode 2) -> mod-101 re-audit + Chapter 5 engine
      yes -> Q2

Q2. Is the total active-user count in that segment big enough to matter (e.g. >100 for
      B2B, >10k for consumer — sanity-check against your ARR target)?
      no  -> WRONG DISTRIBUTION (Mode 3) -> mod-108
      yes -> Q3

Q3. Does trial / free-tier retention flatten but conversion-to-paid collapse
      at the current price point?
      yes -> WRONG PRICE      (Mode 4) -> mod-106
      no  -> No PMF failure diagnosed — durability work in mod-109 / scale work in mod-108
```

The tree is deliberately simple. A more nuanced diagnostic would introduce more modes (wrong-positioning is arguably a fifth; wrong-ICP a sixth) — but at PRE-SEED the coarser four-mode taxonomy usually gets you to the right routing decision. Wrong-positioning shows up as wrong-product in this taxonomy (the product is not experienced as its intended benefit); wrong-ICP shows up as wrong-market (no segment scores well). Those failure-mode → module routes hold either way.

### Why route to a module is the whole point

The failure-mode diagnosis is only useful if it maps to a specific next action. That is what the routing column exists for: **the diagnosis tells you which module owns the fix.**

- Wrong market → [mod-101](../mod-101-customer-discovery-and-problem-validation) (re-discovery)
- Wrong product → [mod-101](../mod-101-customer-discovery-and-problem-validation) re-audit + this module's Chapter 5 engine
- Wrong distribution → [mod-108](../mod-108-demand-generation-and-channels) (channel-market fit)
- Wrong price → [mod-106](../mod-106-pricing-and-packaging) (WTP + packaging)

A team without the routing habit will apply the wrong module's tools to the wrong mode: hiring an SDR to fix wrong-market (mode 1 fixed with mod-108 tools) is the classic disaster. The founder's discipline is to name the mode before touching a downstream module.

### The one-mode-at-a-time rule

If the diagnostic surfaces two modes simultaneously — say, wrong-product *and* wrong-distribution — **fix the lower-numbered mode first.** Working on distribution when the product is still wrong scales the leak. Working on price when you cannot get the product in front of anyone at any price is theatre. The order is deliberate: mode 1 blocks mode 2 blocks mode 3 blocks mode 4.

## Concrete example — the code-review-tool routes three segments differently

Return to the code-review-tool's segment splits from Chapter 3:

- **Mid-market (50–200 eng, distributed teams):** Sean Ellis 56%, WAU retention flattens at ~70% (Chapter 4). No mode fires — this segment has PMF. Move to Chapter 5 engine to strengthen, and check Q2: total mid-market active teams = 27. That is small — check whether the 27 came from one narrow channel; if yes, add mod-108 channel-market fit work.
- **Small teams (<20 eng):** Sean Ellis 13%, retention decays to zero. Modes 1 → 2 diagnostic: are any small-team users scoring high? No convergent benefit either. This is **Mode 1 (wrong market)** for the small-team segment. Route: either re-select segment (drop small-teams from ICP — deprioritise) or re-run mod-101 discovery against a sharper small-team hypothesis if the founders believe there is a sub-segment they missed.
- **Enterprise (500+ eng, single-BU pilot):** Sean Ellis 9%, retention has the pilot-then-decay shape from Chapter 4. Free-text reveals users describe the product as *"the right idea but missing SSO / audit-log / centralised admin"* — they name specific enterprise features you do not have. That is **Mode 2 (wrong product)** for the enterprise segment: the problem is real, the shape is close, but the enterprise-specific features required to deliver on the promise are missing. Route: mod-101 re-audit against enterprise-specific JTBD outcomes; do not scale enterprise motion (mod-107) until the product shape resolves.

Three segments; three different modes; three different downstream modules. The single most valuable output of this module is that these three routes are named and separated. A team that read the aggregate 25% would apply one uniform response to all three; each of those uniform responses would be wrong for two of the three segments.

## Common failure patterns

- **Applying mod-108 (marketing) to a Mode 2 problem.** Buying paid ads for a product with a leaky retention curve scales the churn.
- **Applying mod-106 (pricing) to a Mode 1 problem.** Making the price cheaper does not make people want something they do not want. Free is still too expensive if there is no value.
- **Pivoting on Mode 3.** The classic tragedy — a startup with strong PMF in a narrow reachable pool decides "we don't have PMF" and pivots away from the fit, when the actual work is distribution. Chapter 5's engine + Chapter 4's segmented retention read prevents this.
- **Skipping the diagnostic and just "iterating".** Iterating without naming the mode is a random walk. Wrong-market cannot be fixed by iteration; wrong-price cannot be fixed by product work; wrong-distribution cannot be fixed by more product features.
- **Reading the aggregate.** As Chapter 3 and Chapter 4 both stressed — the aggregate hides the segment splits, and the segment splits are where the mode diagnosis lives. The diagnostic tree assumes segment-level reads.
- **Treating "no mode fires" as PMF success.** No-mode-fires means no diagnosed *failure*; it does not automatically mean scale-ready. Chapter 7's scorecard is the actual sign-off document.

## Summary

- Four failure modes at the resolution the survey + retention read can distinguish: **wrong market, wrong product, wrong distribution, wrong price.**
- Each routes to a different downstream module — **mod-101, mod-101 + this Chapter 5, mod-108, mod-106** respectively.
- Diagnostic order matters: **market → product → distribution → price**. Fix lower-numbered modes first; working on higher-numbered ones while a lower-numbered one is live magnifies the underlying leak.
- **Wrong-distribution is the most-often-misdiagnosed mode.** A high-scoring narrow segment is real PMF; scale it via mod-108, do not pivot the product.
- The diagnostic requires **segmented** reads. Aggregate scores obscure exactly the differences the tree needs to route on.
- The point is not diagnosis for its own sake; **the mode determines the module**. That is the whole payoff.
