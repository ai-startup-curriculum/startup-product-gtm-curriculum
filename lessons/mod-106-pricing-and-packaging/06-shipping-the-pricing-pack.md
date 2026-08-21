# Shipping the Pricing and Packaging Pack

## Motivation

Chapters 1-5 build the parts. Chapter 1 gives the WTP research (the buyer's stated ceiling). Chapter 2 gives the value derivation (the buyer's economic ceiling). Chapter 3 gives the three-tier packaging (the anchor / ceiling raiser / stripped protector shape). Chapter 4 gives the pricing metric (the axis the tiers scale on). Chapter 5 gives the experiment discipline (how the pack evolves after launch).

This chapter is where those parts get **assembled into a single shippable artifact** — the *pricing pack* — that the founder maintains, that the sales team quotes from, that the finance team bills off, that the board can read, and that Chapter 5's experiments update on a quarterly cadence.

The failure mode this chapter exists to catch: **the founder has done the individual work — a value derivation on one slide, a WTP curve in a Google Sheet, a tier composition in a Notion doc, a pricing page in the marketing site — but the artifacts live in different places, disagree with each other, and drift silently. The sales team quotes from the pricing page; the founder answers "what's our value story" from a different slide; the pricing page's tier features have diverged from what the product actually ships; and no one owns the reconciliation.** The remedy is a single document — the pack — that is the *source of truth* for every pricing-related decision, updated on a defined cadence with a defined owner.

This chapter fixes:

- The **required contents** of the shippable pack — one primary pricing metric, three tiers, one anchor price per tier, one supported experiment for the next quarter.
- The **layout and shipping shape** — one document, one page-length rule per section, one owner, one versioning discipline.
- The **operating cadence** — weekly, monthly, quarterly reviews and what gets touched at each.
- The **three-audience test** — the pack has to serve the founder, the AE, and the investor / board member.
- The **boundary** to `startup-finance-fundraising-curriculum` — where GTM-depth pricing ends and unit-economics modelling for fundraising begins.

## Core concepts

### The pack's required contents

A shippable pricing pack contains, at minimum, seven sections. Every section is present; every section is compressed; every section has a named owner.

**Section 1 — Metadata.** Version, date, owner, one-line change-log entry against the prior version. Any pack without a version-and-date is unrideable — six months on, no one knows whether the doc is current.

**Section 2 — Primary pricing metric (Chapter 4).** One sentence naming the metric ("Loomly charges per repository monitored per month"), one paragraph on the four-alignment-test defence (value / growth vector / estimability / incentive alignment), and one paragraph on why the alternative metrics were rejected. This is where the strategic-choice reasoning lives; without it the metric is un-defended when a board member asks "why not per-seat?"

**Section 3 — Three tiers (Chapter 3).** The tier-composition worksheet (capabilities × tiers matrix), the three tier names, the three tier positioning statements (one sentence per tier: who it's for), and the expected mix (what fraction of new customers you expect in each tier). The mix expectations become the guardrail for Chapter 5's experiments — if actual mix diverges from expected by more than ~10 points, the pack needs revisiting.

**Section 4 — Anchor price per tier.** The three price points, with:
- The value-derivation reference for the middle tier's price (from Chapter 2).
- The ratio to the middle tier for the top and bottom (2-4× for top, 20-40% for bottom).
- The per-metric price (per repo / per seat / per event) or the fixed-price structure.
- The published-vs-negotiated policy — which tier prices are stable public prices vs. which are anchors for negotiation.

**Section 5 — WTP research summary (Chapter 1).** The most recent research findings compressed to one page:
- Van Westendorp PSM: PMC / OPP / IPP / PME ranges, sample size, date.
- Gabor-Granger: demand curve peak and range, sample size, date.
- Max-Diff: top-6 attribute ranking, sample size, date.
- Any per-segment differences.
- Explicit sample-size caveats when the sample is small.
- The gap between value ceiling (from Section 4 derivation) and stated WTP — this is the "narrative work still to do" number.

**Section 6 — Supported next-quarter experiment (Chapter 5).** One experiment, chosen from the four types:
- What's changing (specifically).
- Why (which pack section it's testing).
- Baseline metrics (close rate, ACV, retention).
- Guardrails (thresholds that revert or pause).
- Cohort-tracking design.
- Timeline and read date.
- Named owner.

**Section 7 — Operating cadence + grandfathering policy.**
- Weekly / monthly / quarterly review cadence and what happens at each.
- The current grandfathering policy for any recent pricing change (which cohorts are on which pricing, sunset dates).
- The change-log summary for the last 4 quarters.

**Section 8 (optional) — Category context.** A short (half-page) analysis of competitor pricing, category norms, and the pack's position relative to them. Useful for the sales conversation and for board updates; not load-bearing.

Total pack length: **6-10 pages**, ideally in a single document (Notion doc, Google Doc, or a markdown file in the company's playbook repo). If the pack is longer than that, it isn't a pack — it's a research library. Compress.

### The one-page pricing summary — the quotable version

Inside the pack, the first page should be a **one-page pricing summary** that the sales team can share with a customer, quote from in a discovery call, or paste into a proposal. This is not the full pack — it is the compressed customer-facing artifact.

Standard one-page summary layout:

```
─────────────────────────────────────────────────────────────
LOOMLY — PRICING SUMMARY                              v3.2 · 2026-08-15
─────────────────────────────────────────────────────────────
                                                                     
                Starter          Team ★           Business           
                                                                     
Price           $4/repo/mo       $12/repo/mo      $28/repo/mo         
                (annual)         (annual)         (annual)            
                                                                     
For             Small teams      Most teams       Enterprise-adj.     
                <10 eng, GH      20-200 eng       SSO / compliance    
                                                                     
Includes                                                             
  Dependency    ✓ (limited)      ✓                ✓                    
    graph                                                             
  GitHub                                                             
    Actions     ✓ (rate)         ✓                ✓                    
  Slack alerts  —                ✓                ✓                    
  Historical    7d               90d              3yr                  
    trends                                                             
  Monorepo      —                ✓                ✓                    
  Multi-VCS     GitHub only      GitHub only      GitHub+GitLab+BB    
  SSO/SAML      —                —                ✓                    
  On-prem       —                —                ✓                    
  Dedicated     —                —                ✓                    
    CSM                                                                
                                                                     
Seat cap        ≤10              unlimited        unlimited           
Repo cap        ≤25              unlimited        unlimited           
Support         Community        Email            Phone + Slack       
                                                                     
                                                                     
Value story: For a 50-engineer team, Loomly typically recovers        
~$180K/year in engineering cycle time. Team tier ($14.4K/year for a  
100-repo team) captures ~8% of the value delivered.                  
                                                                     
─────────────────────────────────────────────────────────────
Full pricing pack: <link>. Owner: <founder>. Reviews weekly.
─────────────────────────────────────────────────────────────
```

Rules:
- One page. No wrap. Readable in 60 seconds.
- Middle tier visually marked as default.
- Value story compressed to two sentences.
- Full pack linked but not included; the summary is a *derived* artifact.
- Owner and cadence named at the bottom — no one has to hunt for who to escalate to.

### The operating cadence — weekly / monthly / quarterly

The pack is not a launch document. It is an operating document with a defined update cadence.

**Weekly (5-10 minutes, at the mod-105 pipeline meeting):**
- Any new close-lost coded to "pricing" — is the reason a tier feature gap, a price-point objection, or a metric-misalignment? Aggregate by category.
- Any new customer whose deal was closed *outside* the standard pricing structure — flag for the monthly review.
- The current-quarter experiment's progress and any guardrail signals.

**Monthly (30 minutes, dedicated agenda):**
- Cohort-level metrics (Chapter 5): per-cohort ARPU, close rate, 30/60/90-day retention. Any diverging cohort warrants investigation.
- Tier-mix vs. expected mix. Divergence > 10 points is a flag.
- Non-standard deals from the weekly review — is there a pattern the pack should absorb, or are they one-offs?
- Support ticket volume tagged "pricing" or "billing" — spike is a flag.
- Update the pack's change-log if anything meaningful moved.

**Quarterly (2-3 hours, pricing-pack revision meeting):**
- Full pack review. Every section re-examined against the last quarter's data.
- Current-quarter experiment's final read. Guardrail-based decision (keep / revert / iterate).
- Next-quarter experiment chosen.
- WTP research refresh scheduled if the last research is > 12 months old.
- Value derivation refreshed if the product's scope has changed materially.
- New pack version stamped; change-log entry written; the pack is re-shared with the sales team, the finance team, and the founder-CEO's board update.

**Annually (integrated into strategic planning):**
- Full WTP research rerun (Chapter 1) if the market or product has shifted.
- Value-derivation validation against actual measured customer outcomes (Chapter 2's ROI claims stress-tested against real customer telemetry — did they actually get the outcome we promised?).
- Metric review (Chapter 4) — does the four-alignment-test worksheet still hold?
- Tier composition review (Chapter 3) — does the tier-mix suggest the composition is right?

The cadence is what turns pricing from a launch-once activity into an operating discipline. Founders who skip the cadence end up with the pricing they shipped 18 months ago and no defensible reason for any of it.

### The three-audience test — founder, AE, investor

A pack that serves only one audience is fragile. The shippable pack has to work for three:

- **The founder (herself, next quarter).** Six months from now, the founder is on a customer call and has to answer "why do we charge per-repo?" The pack has to answer that question in the founder's own voice, without her having to re-derive from first principles. The pack is a memory instrument.

- **The AE (first sales hire, or the AE the founder is coaching).** The AE reads the pack on day one. She needs the pricing page summary, the tier positioning, the value story, and the objection-handling — all callable from her memory during a discovery call. If the pack requires the AE to hold the four-test metric defence in her head, the pack is too abstract.

- **The investor / board member.** She reads the pack (or a compressed board-facing version — the one-page pricing summary + Section 5's WTP research summary + Section 6's experiment plan) and can distinguish "founder has thought about pricing" from "founder has an intuition-based number on a slide." A pack that is legible to the investor is what makes pricing a defensible topic in fundraising conversations (see boundary below).

An artifact serving only the founder is a diary; one serving only the AE is a sales cheat sheet; one serving only the investor is a slide. The shippable pack serves all three by structure: the one-page summary serves the AE and quick queries; the full pack serves the founder's memory and the investor's rigour check.

### The boundary — where mod-106 ends and startup-finance-fundraising-curriculum begins

Pricing is a topic that spans two curricula. This module (`mod-106`) owns the GTM-depth pricing decisions: WTP research, value derivation, tier composition, metric selection, and startup-scale price experimentation. The pack this module ships is the *operating* artifact for the go-to-market motion.

Deep unit-economics modelling — CAC / LTV / payback with cohort-level financial detail, gross margin analysis by tier, contribution margin optimisation, sensitivity analysis for fundraising narratives, DCF-style discounting for cohort LTV, capital-allocation frameworks for pricing-driven investment decisions — is out of scope. Those live in `startup-finance-fundraising-curriculum`.

The boundary in practice:

- **In-scope for mod-106:** anchor price, tier structure, metric choice, experiment plan, cohort-level tracking of close rate + ARPU + retention.
- **In-scope for `startup-finance-fundraising-curriculum`:** LTV / CAC ratios with discount rates, cohort DCF, gross margin modelling, contribution margin by tier, pricing's effect on the fundraising narrative and valuation multiple.
- **Shared operationally:** the pack's cohort tracking feeds the finance model's cohort LTV; the finance model's discount rate feeds back into the "value capture ratio" defence in Chapter 2.

Where the two overlap in the sales conversation, the pack from this module is the *primary* artifact — the value slide, the tier structure, the anchor price. The finance model is the *supporting* artifact for the board and the investor conversations. Neither replaces the other.

The forward-linked artifacts from `mod-110` (GTM Metrics and First Hires) also connect here: the GTM one-pager uses the pricing pack's cohort-tracking data as one of its inputs, and the CAC / payback benchmarks in mod-110 are computed against the pack's per-tier ARPU.

### The pack in the sales motion (mod-105 / mod-107)

The pricing pack lives inside the sales motion, not alongside it.

- **In discovery (mod-105 Chapter 3):** the AE uses the pack's Section 5 (WTP-derived context) to test the buyer's price-band expectations. "For teams your size, our customers typically pay $X-Y range; is that consistent with what you'd been expecting?" surfaces the buyer's mental model early.
- **In the demo (mod-105 Chapter 4):** the value story from the pack's Section 4 anchoring appears on a value slide. The buyer walks out of the demo with the value math.
- **In the proposal (mod-105 Chapter 6):** the pack's one-page pricing summary is the pricing exhibit in the proposal. The tier composition is not re-authored in each proposal; the pack is quoted.
- **In objection handling:** the pack's Section 2 (metric defence) and Section 4 (value-derivation) become the objection-handling script. "Why per-repo?" → four-test answer from the pack.

The pack is what allows the pricing conversation to be *the same conversation every time*. Without the pack, every discovery call re-derives the pricing story from the founder's memory; with the pack, the pricing story is a stable artifact the founder / AE quotes from.

## Concrete example — Loomly's Q2 pricing pack

Loomly (running example throughout) ships its Q2 pricing pack. Structure:

**Section 1 — Metadata.**
- Version: v3.2 · 2026-08-15 · Owner: [founder name] · Prior: v3.1 (2026-05-10).
- Change vs. v3.1: Volume-based Team-tier pricing introduced ($10/repo above 50, $8/repo above 150); rest of pack unchanged.

**Section 2 — Pricing metric.**
- Metric: per repository monitored per month, billed annually.
- Four-alignment-test defence: (1) scales with value (repo count ≈ PR volume ≈ cycle-time value); (2) matches buyer's growth vector (customers grow repos faster than engineers); (3) estimable (buyer can count repos in her GitHub org); (4) incentive-aligned (customer's success = more repos observed = more revenue).
- Alternatives considered and rejected: per-seat (fails Test 1), per-scan (fails Tests 3 and 4), per-outcome (attribution not viable at seed).

**Section 3 — Three tiers.**
- Tier-composition worksheet (matrix from Chapter 3's example).
- Names: Starter / Team ★ / Business.
- Positioning statements: "Solo eng / small teams" / "Most teams start here" / "SSO / compliance / enterprise-adjacent."
- Expected mix: 20% Starter / 70% Team / 10% Business. Q1 actual: 17% / 73% / 10%. Within guardrail.

**Section 4 — Anchor prices.**
- Starter: $4/repo/month, ~$1.2K/year for 25-repo team.
- Team: $12/repo/month for 1-50 repos, $10 for 51-150, $8 for 151+. Median customer at 100 repos = $12K/year.
- Business: $28/repo/month flat. Median at 150 repos = ~$50K/year.
- Value derivation: for 50-engineer team (100 repos), Loomly recovers ~$180K/year in cycle-time cost; Team tier at $12K captures ~7% of value. Range: 5-10% capture depending on team size.
- Publish policy: Starter and Team prices published; Business tier published price is anchor for enterprise negotiation, actual closing prices range $40K-$120K.

**Section 5 — WTP research summary.**
- Last full run: Q3 2025 (11 months ago; scheduled refresh Q4 2026).
- N = 60 respondents; mid-market B2B SaaS on GitHub.
- Van Westendorp: PMC $2/repo, OPP $6, IPP $8, PME $14. Team's $12 base is inside the acceptable band, above the OPP, below the PME.
- Gabor-Granger: revenue-max peak at $7-$10/repo. Team's $12 is above the peak; the volume tier ($10 above 50 repos, $8 above 150) drops effective per-repo price into the peak band for large customers.
- Max-Diff: top-4 features (dependency-graph accuracy, GitHub Actions, PR-time scanning, Slack alerting) all in Team. Enterprise-signals (SSO, on-prem) rank low in mid-market segment but ranked high in a separate 25-respondent enterprise sub-run.
- Value gap: value ceiling ($50K/year for 100-repo team at 25% capture) vs. WTP ceiling ($10K/year OPP × 100 repos). Ratio ~5×. Positioning-work-to-close-gap flagged as ongoing.

**Section 6 — Q3 experiment.**
- What's changing: introduce a Business-tier volume discount mirroring the Team-tier structure (test whether the mid-market volume approach also captures the enterprise-adjacent segment).
- Why: current Business volume is at expected mix (10%) but ARPU on Business deals varies wildly ($40K-$120K); a published volume structure may tighten the range and improve enterprise negotiation predictability.
- Baseline: Q2 Business close rate 25%, mean ACV $65K, 90-day retention 100% (small sample).
- Guardrails: close rate floor 20%, retention floor 90%, no > 3 pricing-related tickets in any week.
- Cohort tracking: Q3 Business cohort tagged "Business-volume-v1"; Q1-Q2 Business customers stay on flat pricing (12-month grandfather).
- Timeline: publish Q3 Week 1; read at end of Q3; decision at Q4 pack revision.

**Section 7 — Operating cadence + grandfathering.**
- Weekly: pricing objections + non-standard deals at pipeline meeting.
- Monthly: cohort ARPU / close / retention review.
- Quarterly: full pack revision.
- Grandfathering: Q1 Team customers on flat pricing until renewal (all migrate by end of Q1 2027); no other legacy pricing cohorts.
- Change log: v3.0 (2026-01-10, initial launch); v3.1 (2026-05-10, positioning tweak); v3.2 (2026-08-15, Team volume tier).

**Section 8 — Category context.**
- Adjacent tools: Snyk ($5-10/repo range), LinearB ($20-30/seat), Datadog ($X/host). Loomly positioned above Snyk (different value story) and below Datadog (different category).
- Buyer's mental model: mid-market VP Engineering thinks in $10-15/repo range for dev-tool subscriptions; premium ($28) requires narrative work to place Loomly outside the "dev tool" reference class into "productivity platform."

The pack is a single Notion doc, 8 pages long, shared with the founder + AE + CFO + board. The one-page summary is exported and lives on the pricing page + in every proposal template. The next scheduled review is the end-of-Q3 experiment read.

## Common failure patterns

- **The-pack-that-doesn't-exist.** Founder has done the individual pieces — value slide here, WTP curve there, tier composition in Notion, pricing page in Webflow — but there is no consolidated document. Each piece drifts independently; six months on, the pricing page and the value slide disagree on the middle-tier price. Fix: consolidate; one document; owner.
- **The-pack-is-a-slide-deck.** Founder builds a 40-slide pricing deck for the board. It's beautiful. No one uses it operationally because it's not a live document. The sales team quotes from something else; the finance team bills from something else. Fix: the pack is a *working document* (Notion / Google Doc / markdown) with an owner and a cadence — not a slide deck for a single meeting.
- **The-pack-owned-by-nobody.** No named owner. The pack drifts because no one is responsible for updates. Every stale claim in the pack costs a real sales objection six months later. Fix: named owner in the metadata line. Owner is accountable for weekly / monthly / quarterly cadence.
- **The-pack-that-lags-the-product.** Product ships a new feature; the tier composition doesn't get updated; the sales team includes the new feature in Team-tier deals by default; the pack's Business tier value proposition is quietly diluted. Fix: product release checklist includes pack update; pack changes at every material product ship.
- **The-quarterly-review-that-gets-skipped.** Q1 pack revision meeting is on the calendar; Q1 gets busy; the meeting gets moved to Q2; then to Q3; a year later, the pack is 4 quarters stale. Fix: the quarterly meeting is treated as non-negotiable, even if it takes 30 minutes instead of 3 hours; even a small cadence beats no cadence.
- **The-pack-that-only-serves-the-board.** Beautifully polished pack for the fundraising narrative; useless in the discovery call. Fix: three-audience test — founder / AE / investor. If any of the three can't use the pack for their purpose, it's not shippable.
- **The-pack-that-only-serves-the-AE.** Great one-page pricing sheet; no derivation, no defence, no experiment plan. Sales team is happy; the board's "why per-repo" question kills the funding narrative. Fix: the sheet is *inside* the pack; the pack is the whole thing.
- **Pack-length-inflation.** The pack grew to 40 pages because every objection in the last two years got its own section. No one reads it end-to-end. Fix: 6-10 pages is the ship discipline. Deep artifacts (WTP raw data, full experiment history, competitor pricing analyses) get linked out, not included.
- **Change-log-drift.** The pack changes; no one updates the change log; six months later, the "what changed in v3.2 vs v3.1" question is unanswerable. Fix: every version stamp includes a one-line change log entry. It takes 30 seconds; it saves hours later.
- **Version-drift across artifacts.** The pack says $12/repo; the pricing page says $14/repo; the proposal template says $12/repo but has a 10% discount baked in. Sales rep quotes some third number. Fix: single source of truth. The pack drives the pricing page, the proposal template, and the CRM opportunity fields. Any divergence is a bug tracked in the pack's change log.
- **The-experiment-plan-that-gets-forgotten.** Section 6 names a Q2 experiment. Q2 comes and goes; no one runs it. Q3 pack revision has nothing to update. Fix: the experiment plan has an owner and a start date. If it isn't launched by mid-quarter, escalate at the monthly review.
- **Confusing-pack-with-pricing-page.** Founder edits the pricing page directly; the pack lags. Or founder edits the pack; the pricing page lags. Fix: pack is upstream; pricing page derived from pack. Any pricing-page change is a pack change first.

## Summary

- The **pricing pack** is the single artifact that consolidates the outputs of Chapters 1-5 into a working operating document. It has one owner, one cadence, one source of truth for every pricing-related decision.
- **Required contents:** metadata (version + date + owner); primary pricing metric with four-alignment-test defence; three tiers with composition worksheet + names + positioning + expected mix; anchor price per tier with value-derivation reference; WTP research summary; next-quarter experiment plan; operating cadence + grandfathering policy. Optional: category context.
- **Length:** 6-10 pages. The pack is a working document, not a research library. Deep artifacts (raw WTP data, competitor deep-dives, historical experiments) are linked out.
- **One-page pricing summary** lives at the top of the pack — the compressed customer-facing artifact the sales team quotes from, that gets exported to the pricing page and the proposal template. One page, 60-second scan, middle tier marked as default.
- **Operating cadence** — weekly (pipeline meeting): pricing objections + non-standard deals + experiment progress. Monthly: cohort metrics + tier mix + support tickets. Quarterly: full pack revision + experiment read + next-quarter experiment chosen. Annually: WTP refresh + value derivation validation + metric review.
- **Three-audience test** — the pack must serve the founder (memory instrument, next-quarter herself), the AE (sales cheat sheet + objection handling), and the investor / board (fundraising-legible defensibility). Serving only one is fragile.
- **Boundary to `startup-finance-fundraising-curriculum`** — this pack owns GTM-depth pricing (anchor, tiers, metric, experiments, cohort tracking). Unit-economics modelling for fundraising (LTV / CAC with discount rates, gross margin analysis, cohort DCF, valuation-multiple analysis) is out of scope and defers up.
- The pack **lives inside the sales motion** — it is the source for the value slide (mod-105 Chapter 4 demo), the pricing exhibit in proposals (mod-105 Chapter 6), the objection-handling script, and the price-band probe in discovery (mod-105 Chapter 3). The pack turns pricing from an ad-hoc conversation into a stable artifact.
- **Common failure patterns** — no consolidated pack; pack owned by nobody; pack that lags the product; skipped quarterly reviews; pack-length inflation; version drift across artifacts; single-audience packs (board-only or AE-only).
- The pack's cumulative output over 12-18 months (4-6 documented experiments, cohort-tracked learnings, quarterly revisions) is what turns a founder's initial pricing hypothesis into a *market-tested pricing strategy* — the artifact that turns pricing from luck into discipline.
