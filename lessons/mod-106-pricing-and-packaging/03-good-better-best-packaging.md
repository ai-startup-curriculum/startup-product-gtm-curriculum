# Good / Better / Best Packaging — Anchor, Premium, Stripped-Anchor

## Motivation

The value derivation in Chapter 2 gives the founder an anchor price for a single offering. But almost no B2B SaaS product ships as a single offering — the market has heterogeneous buyers with different willingness-to-pay, different feature needs, and different appetites for premium. **Packaging** is the discipline of arranging the product into a small number of tiers that let each buyer pick the one that fits her — while also *steering* the buyer toward the tier the vendor wants her in.

The dominant B2B SaaS packaging pattern is **three tiers**: a stripped-down entry ("good"), a middle anchor ("better"), and a premium ceiling ("best"). Every vendor in the category does this because it works — three tiers exploits a stable psychological phenomenon (the middle-option preference; the compromise effect first documented in Simonson, "Choice Based on Reasons: The Case of Attraction and Compromise Effects," *Journal of Consumer Research*, 1989) and produces a *choice architecture* the founder can steer.

But three tiers only works if the three are designed as a coherent system, not three independent price points. Each tier plays a role:

- The **middle tier** is the *anchor* — the one the founder actually wants most buyers to pick. Feature-complete-enough, priced to capture the value math from Chapter 2, positioned as the natural choice.
- The **premium tier** is the *ceiling raiser* — the one that makes the middle tier look reasonable by comparison. Very few buyers pick it; that's fine. Its job is to reframe the middle tier as "the sensible middle option" rather than "the expensive one."
- The **entry tier** is the *stripped anchor* — the one that protects the middle tier from a price war on the low end. Just capable enough to satisfy a real buyer segment (or to serve as a foothold), just constrained enough that buyers who value the missing features have to move to the middle.

The failure mode this chapter exists to catch: **the founder ships a "starter / pro / enterprise" three-pack where the three tiers are three independent price points authored by intuition, without any thinking about which tier is the anchor, which is the ceiling raiser, and which is the stripped protector.** The result is either a middle tier that doesn't get picked (because the entry has too much value for the price), a premium tier that gets picked reluctantly (because the middle has feature gaps it shouldn't), or an entry tier that cannibalises the middle at zero benefit.

Chapter 4 handles the *pricing metric* (per what) that runs across all three tiers; Chapter 5 handles experiments on tier composition and pricing. This chapter fixes the *shape* — three tiers, coherent roles, defended failure modes.

## Core concepts

### Why three tiers — the compromise effect and the extremeness aversion

The three-tier default is not a marketing convention picked at random. It exploits two documented effects:

- **The compromise effect** (Simonson 1989, Simonson & Tversky "Choice in Context: Tradeoff Contrast and Extremeness Aversion" *JMR* 1992): when presented with three options along a value / price gradient, buyers disproportionately choose the middle one. The tendency is robust across categories and independent of specific features — the middle position itself is preferred, other things equal.
- **Extremeness aversion** (same literature): buyers avoid the extremes (cheapest and most expensive) because either extreme requires them to defend a stronger justification. The middle option requires the least defence.

Three tiers is the smallest arrangement that creates a "middle" and two "extremes." Two tiers (entry / premium) forces a binary and does not create a compromise position. Four tiers dilutes the compromise position across two middle options and creates decision friction. Three is the sweet spot the psychology literature supports and the industry has converged on.

There are cases where three is wrong:

- **Truly enterprise-only sales** — one tier plus custom pricing is often more honest than a fake tier structure for a bespoke-contract product.
- **Very simple PLG products** at seed stage — one tier (with just a paid / free split) may be right when the product is early and packaging complexity is premature.
- **Marketplace / two-sided products** — the packaging problem is different (participation-level tiers, not feature tiers).

For the mainstream B2B SaaS case the module is teaching, three tiers is the default and the burden is on any other structure to justify itself.

### The three roles — anchor, ceiling raiser, stripped protector

Each tier plays a specific role, and the packaging works only when all three roles are filled coherently.

**Middle tier — the anchor.** The tier the vendor wants most buyers to pick. Every packaging decision — feature composition, price, positioning — is calibrated to make this tier the obvious choice. Design principles:

- **Feature-complete for the intended buyer.** Contains every capability the mainstream ICP needs to succeed with the product. A middle tier missing a feature the mainstream buyer needs pushes her up to premium and produces friction on the way, or (worse) pushes her out of the funnel.
- **Priced at the value-derived anchor** (Chapter 2). The middle tier price is the price the founder actually wants to be charging on average.
- **Positioned as the default in copy.** "Most teams start here," "recommended for teams of 20-200," a visual highlight, a "Most Popular" badge. The default isn't a coincidence — it's declared.

**Top tier — the ceiling raiser.** The tier that raises the perceived value of the middle by anchoring the top of the price range higher. Design principles:

- **Priced 2-4× the middle tier.** Too close (< 1.5×) and it doesn't create the anchor effect. Too far (> 5×) and it looks like a different product; the anchor breaks because buyers stop mentally comparing it to the middle.
- **Includes real premium-buyer features.** SSO, SAML, advanced audit, custom SLAs, priority support, on-prem deploy, dedicated CSM, procurement-friendly terms. A premium tier that is just "the middle with a bigger seat count" is transparent and fails to anchor.
- **Not for everyone; that's the point.** If more than ~15-20% of buyers pick the premium tier, either it's underpriced or the middle tier has feature gaps that force upgrades. Practitioner data (OpenView, ProfitWell / Paddle reports on SaaS pricing) suggests healthy mid-market SaaS sees ~10-15% of new revenue from the top tier at scale.
- **Serves as the enterprise starting point.** In many B2B motions, the "premium tier" on the pricing page is where the enterprise conversation starts — followed by a custom-terms negotiation for a bespoke annual contract. The published premium price is the *anchor for the negotiation*, not the closing price for the enterprise deal.

**Bottom tier — the stripped anchor (or entry tier).** The tier designed to keep the middle tier looking valuable and to protect the middle from a low-end price war. Design principles:

- **Real, but constrained.** It must be usable for a real buyer segment (usually solo users, tiny teams, or a specific narrow use case). A fake tier that no one actually uses is transparent and undermines credibility.
- **Missing at least one feature the mainstream buyer needs.** The constraint is what pushes the growing customer up to the middle tier as she outgrows the entry. Common constraints: seat count caps, feature caps (no API, no integrations, no SSO), usage caps (a small quota), branding constraint (vendor branding on outputs), no team features.
- **Priced low enough to be honest.** If the middle tier is $500 / month, the entry tier at $400 / month says "we don't really want you here" — buyers can smell the coercion. Common practice: entry tier priced at 20-40% of middle, or free (freemium) if the model supports it.
- **Protects against low-end competitor entry.** If a competitor undercuts at the low end, the entry tier keeps the vendor's brand present in that space; without it, the vendor cedes the entire low-price segment.

### Why the stripped anchor matters — the low-end price war defence

Founders often argue for skipping the entry tier: "we don't want low-value customers, they distract from the ICP." This is not wrong on the customer-quality argument. But the entry tier isn't primarily *for* the low-end buyer — it is *for the vendor's defence of the middle tier*.

Without an entry tier, the vendor's cheapest option is the middle tier's price. When a low-cost competitor enters the category with a $19 / month product, the vendor has no answer — she cannot introduce a cheaper option without repricing the middle, which is destructive. With an entry tier already in place at (say) $29 / month, the vendor has a natural response: adjust the entry tier without touching the middle, keep the ICP steered to the middle, and let the low-end competitor eat the low-end segment without pulling the middle down.

This is the same logic Marriott (or Toyota, or almost any product line) uses when they ship a cheap sub-brand that no marketer really wants to serve — the sub-brand exists so the flagship doesn't have to discount. Practitioners in SaaS pricing (see Wharton / Kellogg case writing on segment defence in tiered pricing; OpenView pricing benchmarks) frame this as "the flanking product" or "the fighter brand" tier.

Whether the entry tier is *free* (freemium) or *paid* (a real low tier) is a separate strategic choice, largely governed by the sales motion (mod-107):

- **PLG products** where free → paid conversion is the primary loop tend toward *free* entry tiers.
- **Sales-led products** where every customer requires human attention tend toward *paid* entry tiers to filter out the tourists.
- **Hybrid motions** (PLG-with-sales-assisted-expansion) often ship both: a free tier for developer entry and a paid entry tier for team formalisation.

The freemium-vs-paid entry choice is Chapter 4's neighbour concern (pricing metric implications) and Chapter 5's experiment (which converts better in the specific ICP).

### Feature-fit vs. axis-based tier construction

There are two dominant ways to distribute features across tiers:

**Feature-fit tiering.** Each tier gets a coherent bundle of features that fit a *specific segment*. Entry tier = solo user's feature set. Middle tier = mainstream team's feature set. Premium tier = enterprise-team's feature set. The bundles are opinionated: "if you're a team, this is the tier for you."

**Axis-based tiering.** Each tier turns up the dial on one or more shared axes — seat count, usage quota, feature depth. Entry = up to 5 seats. Middle = up to 50 seats. Premium = unlimited. Or entry = 10K API calls, middle = 100K, premium = unlimited. Bundles are formulaic: "same product, more of it."

Almost all successful B2B SaaS packaging is *both* — a feature-fit split at the tier boundaries plus axis-based dials within each tier. Purely axis-based packaging (only "how much") fails because premium buyers won't pay 3× just for more seats. Purely feature-fit packaging (only "what") fails because buyers get frustrated when their team of 15 has to move to premium just because the middle capped at 10 seats.

The working practice:

- **Tier boundaries** are drawn by feature-fit (which capabilities cluster together for which segments).
- **Within-tier expansion** is driven by axis-based dials (seat count, usage, workspaces) that let a customer grow inside a tier before hitting the boundary that forces her to upgrade.

This structure means the *pricing metric* (Chapter 4) is the within-tier dial, and the *tier composition* is the feature-fit split. The two are complementary; both have to be designed.

### The tier-composition worksheet

Before naming prices, the founder writes a **tier-composition worksheet** — a matrix that lists every product capability against the three tiers and marks which tier it belongs to. The worksheet forces the founder to be explicit about tier boundaries and prevents the "feature crept into the wrong tier" mistake.

Template:

```
                                  | Entry | Middle | Premium |
--------------------------------- | :---: | :----: | :-----: |
Core capability 1 (must-have)      |   ✓   |   ✓    |   ✓     |
Core capability 2 (must-have)      |   ✓   |   ✓    |   ✓     |
Team feature 1 (roles / perms)     |       |   ✓    |   ✓     |
Team feature 2 (shared workspace)  |       |   ✓    |   ✓     |
Integration set (mainstream)       |   —   |   ✓    |   ✓     |
Integration set (enterprise)       |       |        |   ✓     |
SSO / SAML                          |       |        |   ✓     |
Advanced audit + compliance        |       |        |   ✓     |
API access                          |   —   |  rate  |  full   |
Priority support                    |       |        |   ✓     |
On-prem deploy                      |       |        |   ✓     |
Custom SLA                          |       |        |   ✓     |
Dedicated CSM                       |       |        |   ✓     |
                                    |       |        |         |
Seat cap                            |  ≤5   |  ≤50   | unlim.  |
Usage cap (per pricing metric)     | small |  large | unlim.  |
Support level                       | docs  | email  | phone+  |
```

Every capability is placed in one column (with the ✓s marking which tier gets it), and the axis-based dials (seat cap, usage cap, support level) are the within-tier expansion dials.

The worksheet exposes design questions the founder has to answer:

- **Which capability is a "must-have" for every tier vs. a differentiator?** Only put in every tier what the entry tier's *smallest legitimate use case* needs to succeed.
- **Which capability creates the tier boundary?** The specific feature that, when a buyer needs it, forces the upgrade. Team features usually create the entry → middle boundary; SSO and enterprise integrations usually create the middle → premium boundary.
- **Which capability is decorative?** Features that appear in the worksheet but do not affect any buyer's tier choice can often be removed from the marketing without loss.

### The naming and price display convention

The three tiers need names. Naming conventions vary; the industry has clustered around a few:

- **Descriptive of team size:** "Starter / Team / Business" or "Personal / Team / Enterprise."
- **Descriptive of feature richness:** "Basic / Pro / Premium" or "Standard / Plus / Ultimate."
- **Descriptive of business shape:** "Free / Team / Enterprise."

The specifics matter less than the *consistency* — the same tier plays the same role on the pricing page, in the sales conversation, and in the CRM. "Enterprise" that means "custom deal" on the pricing page and "$99 tier" in the CRM is confusing to everyone.

Price-display conventions that reinforce the anchor effect:

- **Show all three tiers on the pricing page** with the middle tier visually highlighted ("Most Popular," a coloured border, a subtle badge). The anchor effect requires that all three tiers are visible together.
- **Show annual and monthly pricing** with the annual clearly cheaper per month. Annual pricing improves cash flow and retention; the price display is where the discount is anchored.
- **Show the premium tier's price** — do not hide it behind "Contact us for pricing" unless the product is genuinely custom-only. Hiding the premium price defeats the ceiling-raising effect (the middle looks cheap by comparison only if the buyer can see the comparison).
- **Do not stack more than 4 features vertically per tier on the pricing page.** Overloaded pricing pages defeat comparison. The comparison chart below the tier cards can have every feature; the tier cards themselves should be scannable.

### Anti-patterns in tier construction

Common tier-composition mistakes and their consequences:

- **The bloated middle.** The middle tier has every enterprise feature except SSO. Result: premium is only chosen by buyers who need SSO, and premium ARPU is much lower than it should be because the middle is over-featured.
- **The anaemic middle.** The middle tier is missing team features the mainstream buyer needs (roles, shared workspaces, integrations). Buyers who should be middle-tier customers are forced up to premium (which they resent, pushing on churn) or stuck at entry (which caps ARPU).
- **The hollow entry.** The entry tier is so stripped that no real buyer would use it — 1 user, 100 rows, no export. It exists on paper only. Buyers see through it and it undermines the whole packaging's credibility.
- **The parallel-universe premium.** The premium tier is a different product built for a different segment (enterprise), priced 20× the middle. It doesn't function as a ceiling raiser because buyers don't mentally compare it to the middle. Usually the fix is either splitting into two products or moving toward enterprise-only pricing at that tier.
- **The linear seat pack.** Entry = 5 seats @ $10, middle = 50 seats @ $10, premium = 500 seats @ $10. All three tiers do the same thing, priced only by volume. Fails compromise effect (there is no middle; there is only "how much"), fails ceiling raiser (premium is just more of the same), fails stripped protector (entry is the same product, just less).
- **The features-only, no-quotas structure.** Entry has 2 features, middle has 5, premium has 12. No caps on seats, usage, or anything else. The product cannot expand a customer inside a tier because there are no dials to turn up; every expansion is a tier upgrade, which is discontinuous and produces churn risk at the boundary.
- **The everything-and-the-kitchen-sink premium.** The premium tier's feature list is so long the buyer cannot scan it. The comparison to the middle is illegible; the anchor effect requires legible comparison. Working practice: premium's marginal feature list (things it has that the middle doesn't) is at most 4-6 items.
- **The tier-boundary-that-slides.** Sales reps routinely include premium features in middle deals as concessions. Six months later the middle tier de facto includes SSO. The pricing pack has drifted. Fix: the packaging matrix is a policy, not a suggestion; concessions that break the tier boundary should require founder-level approval, and repeat concessions should trigger a re-package rather than continued exception-granting.

### How packaging interacts with the sales motion

The three-tier packaging works differently across sales motions (mod-107):

- **PLG / self-serve.** The three tiers exist on the pricing page; the buyer picks one and pays with a credit card. The compromise effect operates purely through the pricing page's visual design. Freemium at the entry is the standard pattern.
- **SDR-AE inside sales.** The three tiers are the *starting anchors* in the sales conversation. The AE positions the middle tier by default and up-sells to premium or down-sells to entry depending on buyer signals. Pricing page shows all three; the closing contract usually maps to one of them.
- **Enterprise MEDDPICC.** The published premium tier is the *anchor for the enterprise negotiation*. The closing contract is a custom-terms deal that starts from the premium tier's structure and negotiates seat count, features, and price bespoke. The published tier prices set the *reference the buyer starts from*.

The three-tier structure is more visible in PLG (where the buyer picks self-serve) and less visible in enterprise (where the closing contract may look very different from any published tier). But the ceiling-raiser and stripped-protector logic still applies — the published prices set the buyer's mental reference *before* the negotiation.

## Concrete example — Loomly's three-tier pricing pack

Loomly, continuing from Chapters 1-2, packages the value-derived anchor into three tiers.

**Middle tier — "Team":**
- $12/repo/month (annual, ~$14.4K/year for a 100-repo team; matching Chapter 2's derivation).
- Feature set: dependency-graph accuracy (top-ranked Max-Diff feature), GitHub Actions integration (rank 2), PR-time scanning (rank 3), Slack alerting (rank 4), historical trends (rank 5), monorepo support (rank 6), unlimited team seats, priority routing, GitHub-only.
- Positioned as: "Most teams start here. Full dependency-graph tooling for teams of 20-200 engineers on GitHub."
- Named "Team" in pricing page copy; visually highlighted with "Most Popular" badge.

**Premium tier — "Business":**
- $28/repo/month (annual, ~$33.6K/year for a 100-repo team; 2.3× the middle tier, inside the 2-4× band).
- Middle-tier features plus: SSO / SAML, GitLab and Bitbucket support (multi-VCS), on-prem deploy option, public API + Terraform provider, custom SLA (99.9% uptime with credits), dedicated CSM, quarterly executive business review, priority support (phone + Slack Connect).
- Positioned as: "For teams with SSO / compliance requirements or multi-repo-host environments. Includes premium support and CSM."
- Named "Business" in pricing page copy.
- Expected mix: 10-15% of new customers (mostly enterprise-adjacent mid-market).

**Entry tier — "Starter":**
- $4/repo/month (annual, ~$1.2K/year for a 25-repo team; ~30% of middle tier's per-repo price; matches Chapter 1's Van Westendorp PMC).
- Feature set: dependency-graph accuracy, GitHub Actions integration (rate-limited), PR-time scanning (limited to 10 PRs/day), no Slack alerting, no historical trends beyond 7 days, seat cap ≤ 10, single repo host (GitHub only), community support (Discord + docs).
- Positioned as: "For teams under 10 engineers with basic dependency-graph needs, or for teams evaluating Loomly before upgrading."
- Named "Starter" in pricing page copy.
- Expected mix: 15-25% of new customers (mostly small teams, or foothold-stage evaluators who upgrade within 6-12 months).

**Free tier?** Loomly deliberately does *not* ship a free tier. The sales motion (mod-107) is SDR-AE inside sales at $10K+ ACV; the free tier would attract self-serve users who consume support without converting, and the pricing metric (per-repo scan, which has a hosting cost) makes freemium expensive to sustain at scale. The entry tier at $4/repo serves the "foothold" role a free tier would serve in a PLG motion.

**Tier-composition worksheet extract:**

```
                                        | Starter | Team | Business |
--------------------------------------- | :-----: | :--: | :------: |
Dependency-graph accuracy               |    ✓    |  ✓   |    ✓     |
GitHub Actions integration              |  rate*  |  ✓   |    ✓     |
PR-time scanning                        |   10/d  |  ✓   |    ✓     |
Slack alerting                          |         |  ✓   |    ✓     |
Historical trends (retention)           |   7d    | 90d  |   3yr    |
Monorepo support                        |         |  ✓   |    ✓     |
GitLab support                          |         |      |    ✓     |
Bitbucket support                       |         |      |    ✓     |
Priority routing                        |         |  ✓   |    ✓     |
SSO / SAML                              |         |      |    ✓     |
On-prem deploy                          |         |      |    ✓     |
Public API + Terraform                  |         |      |    ✓     |
Custom SLA                              |         |      |    ✓     |
Dedicated CSM                           |         |      |    ✓     |
Priority support                        |         |      |    ✓     |
                                        |         |      |          |
Seat cap                                |   ≤10   | unl. |   unl.   |
Repo cap                                |   ≤25   | unl. |   unl.   |
Support                                 |  comm.  | email|  phone   |
```

**Coherence check.** Middle-tier "Team" is priced at the value-derived anchor and contains every feature the mainstream ICP needs (mod-104's mid-market persona). Premium-tier "Business" adds features that are structurally different (SSO, other VCS, on-prem, dedicated CSM) — the middle-tier buyer does not want most of these, so the tier does not tempt the mainstream. Entry-tier "Starter" is stripped enough that a real 30-engineer team could not use it (seat cap of 10 + repo cap of 25) but a 5-engineer team foothold can. The stripped anchor protects "Team" from a low-price competitor without cannibalising it.

## Common failure patterns

- **The "starter / pro / enterprise" three-pack authored by intuition.** Three names picked, three prices picked, no thinking about which tier anchors, which raises the ceiling, which protects the middle. The tiers are three independent products masquerading as a system.
- **One-tier pricing at seed stage that becomes hard to change later.** The founder ships a single $99 / month plan because "packaging is premature." Twelve months later, when the enterprise buyer arrives, there is no premium tier to sell them and no stripped tier to defend against a low-cost entrant. Working practice: even at seed stage, the three-tier *structure* is worth authoring, even if only one tier is initially marketed publicly.
- **The middle tier that no one picks.** Adoption data shows 70% pick entry, 25% pick premium, 5% pick middle. The middle is either underpriced (buyers who could pay more are drawn to entry), overpriced (buyers who could afford middle are pushed to entry), or missing features the mainstream buyer needs (pushing her to premium). All three are fixable with the tier-composition worksheet.
- **Premium tier that too many people pick.** Adoption data shows > 20% pick premium at scale. Usually means the middle tier has feature gaps that force upgrades (SSO in the middle would solve it) or the premium is under-priced relative to the middle (raise premium 20% and re-check adoption).
- **The freemium-that-doesn't-convert.** Free tier has 10× the paid tier's user base and converts at 0.5%. Either the free tier is too generous (nothing forces upgrade) or the paid tier's incremental value is not legible from inside the free tier. Fix: the free-to-paid conversion feature is a specific artifact — the *upgrade trigger* — that has to be designed, not assumed.
- **No entry tier because "we want to focus on ICP."** Vendor loses low-end segment entirely; a competitor enters at $19 / month and starts eating the small-team market and building brand there; three years later the competitor has moved up and is competing for the vendor's middle-tier customers. Working practice: entry tier is a defensive move, not a customer-acquisition move.
- **Everyone-tier packaging with 8 tiers.** Vendor tries to cover every segment with its own tier. Buyers can't compare; sales reps can't explain; the pricing page is a wall of options. Three tiers plus custom is the working ceiling. If the product truly needs 8 tiers, it's probably 2-3 products with 3 tiers each, not one product with 8.
- **Sliding tier boundaries via sales concessions.** Reps include SSO in middle-tier deals to close them. Six months later the middle tier de facto has SSO and the premium tier's value is diluted. Fix: policy discipline on tier concessions; concessions above threshold require founder approval; repeat concessions trigger a re-package.
- **Custom pricing with no anchor.** Enterprise deals are all "let's talk." The buyer has no reference; the AE has no anchor; the closing prices are all over the map (some $80K, some $300K for similar deals). Publishing the premium tier price gives every enterprise negotiation an anchor to start from.
- **Naming tiers so buyers don't know which is which.** "Silver / Gold / Platinum" or "Bronze / Sapphire / Emerald" — buyers cannot map these to their situation. Descriptive names ("Starter / Team / Business") communicate who the tier is *for*, which is what the buyer needs.

## Summary

- **Good / better / best packaging** is the three-tier structure that dominates B2B SaaS pricing because it exploits the compromise effect (Simonson) and extremeness aversion — buyers preferentially pick the middle when three options are visible.
- Each tier plays a specific **role**: the **middle** is the *anchor* (feature-complete-for-ICP, priced at the value-derived anchor, positioned as the default); the **top** is the *ceiling raiser* (2-4× the middle, real premium features, small mix); the **bottom** is the *stripped anchor* (real but constrained, low price, protects the middle from low-end price competition).
- The **stripped anchor's** primary job is not to win low-end customers — it is to defend the middle tier from a low-end competitor entrance without repricing the flagship. Freemium vs. paid entry is a strategic choice driven by the sales motion.
- Tier construction uses both **feature-fit** (which capabilities cluster for which segment — draws the tier boundaries) and **axis-based dials** (seat count, usage cap — enables in-tier expansion). Purely axis-based fails to justify premium pricing; purely feature-fit fails to enable expansion without tier upgrade.
- The **tier-composition worksheet** — a capability × tier matrix — is the artifact the founder authors before naming prices. It exposes the "which feature creates the boundary" and "which feature is decorative" questions that intuitive packaging skips.
- Premium tier composition (SSO, enterprise integrations, dedicated support, on-prem, custom SLA) should be structurally different from the middle — not just "more of the same" — so premium buyers see it as a different tier for a different need, not an upsell trick.
- **Price display** conventions that support the anchor effect: three tiers visible together, middle visually highlighted ("Most Popular"), premium price shown (not hidden behind "Contact us"), annual / monthly split shown, tier cards scannable (≤4 features vertically).
- **Anti-patterns** — bloated middle, anaemic middle, hollow entry, parallel-universe premium, linear seat-pack, sliding tier boundaries via sales concessions, custom-pricing-with-no-anchor.
- The three-tier structure interacts with the sales motion (mod-107). In PLG, the tiers work directly on the pricing page. In sales-led motions, the tiers are the starting anchors in the sales conversation. In enterprise, the published premium tier is the anchor for the bespoke negotiation.
- Output of this chapter is the **tier-composition worksheet + three tier prices + the coherence check** that becomes half of the pricing pack (Chapter 6). The other half — the pricing metric, Chapter 4 — determines *what dimension* the price scales along inside each tier.
