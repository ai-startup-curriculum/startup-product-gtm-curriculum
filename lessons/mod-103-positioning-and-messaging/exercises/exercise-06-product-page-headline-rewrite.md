# Exercise 06 — Product-Page Headline Rewrite

**Estimated time:** 3 hours
**Chapter links:** [`06-messaging-derivation.md`](../06-messaging-derivation.md), [`07-shipping-the-positioning-artifact.md`](../07-shipping-the-positioning-artifact.md), [`03-three-positioning-failure-modes.md`](../03-three-positioning-failure-modes.md)
**Depends on:** Exercise 01 (Dunford five-component positioning) and Exercise 05 (beachhead selection) — both are the raw material this exercise derives from.
**Prerequisite reading:** Chapter 6 (~30 min); Chapter 7's "Artifact 3" section (~10 min).

## Problem statement

Chapter 6 named the derivation protocol from locked positioning to buyer-facing words, and Chapter 7 named the ship deliverable — **three hero variants**, each leading with a different Chapter 2 component, each traceable to the positioning document, A/B-tested against the operating funnel metric. This exercise ships that artifact.

The failure mode this exercise exists to catch: **the founder rewrites the hero from personal taste rather than deriving it from the positioning; the new hero tests marginally better than the old one but neither reflects the actual strategic choice; six months later the team is on the fifth hero and no closer to a defensible message-market fit.** The derivation discipline is what turns hero rewrites from copywriting exercises into positioning tests.

You will take one live product page, diagnose it against Chapter 3's three failure modes, then derive three replacement hero variants from your Exercise 01 positioning and Exercise 05 beachhead. You will annotate each variant with the component it leads on, the alternative it distinguishes against, and the beachhead-segment reader it addresses. Finally you will produce the A/B test plan — sample size, minimum detectable effect, success metric, test duration — that would let the team ship the rewrite instrumented.

## Requirements

Deliver a folder `exercise-06/` with:

- `part-a-page-teardown.md` — the current hero + full-fold diagnosis of the existing product page.
- `part-b-three-variants.md` — three hero variants (headline + subhead + primary CTA + component lead + traceability annotation), plus optional above-the-fold layouts.
- `part-c-ab-test-plan.md` — the instrumentation and test plan for the rewrite.
- `part-d-derivation-audit.md` — the traceability audit that shows each variant is *derived*, not invented.

### Part A — Current-hero teardown (30 min)

Pick the target page. In priority order:

- **Your own startup's live product-page hero** (preferred) — you'll ship the rewrite.
- **A public startup's live hero** — pick a company whose Exercise 01 positioning you can reconstruct with high confidence (or one whose positioning-doc / narrative is public via a founder interview or Lenny's Newsletter feature).
- **The Loomly running-example** — extend Chapter 6's variants rather than restating them; produce genuinely new variants.

Whichever you pick, produce `part-a-page-teardown.md` containing:

1. **The URL and date accessed.** If it's your own page, the branch or preview URL is fine. Include a screenshot.
2. **The current hero verbatim** — headline + subhead + primary CTA + any secondary CTA / social proof. Copy the words exactly, do not paraphrase.
3. **The Chapter 3 diagnostic tree walk** — Q1 (category identifiable?) → Q2 (attributes / value?) → Q3 (right alternatives?). Show your work at each branch. If more than one mode fires, name each.
4. **The five-component read of the current page.** Fill in Chapter 2's five components based only on what the page says (no charitable interpretation). Include a `Not stated` line for any component the page does not articulate.
5. **The gap.** In one paragraph, name where the current hero diverges from your Exercise 01 positioning + Exercise 05 beachhead. If you're using your own page and the current hero is *already* aligned with the positioning, the gap paragraph names the *messaging* problems (mode fired, surface constraint violated) that a rewrite would address.

### Part B — Three hero variants (75 min)

Per Chapter 6 and Chapter 7, always three, never one. Each variant leads with a *different* Chapter 2 component so that the A/B test reveals which framing your beachhead responds to.

For each variant, deliver:

- **Headline** — one line, 5-12 words. Follows the Chapter 6 template shapes (value + best-for; enemy-of-status-quo; verb-outcome + attribute / category). Avoids the Chapter 6 anti-templates (category-only, comparative-superlative-only, "AI-powered X", founder-monologue).
- **Subhead** — 1-2 lines, 15-30 words. Fills what the headline didn't (attribute if headline was value; best-for if headline was attribute; value if headline was enemy-of-status-quo). Answers the reader's silent next question: *"okay, but what does this actually do, and is it for me?"*
- **Primary CTA** — 2-4 words. Derived from the sales motion (PLG → "Sign up free"; SDR-AE → "Talk to sales"; enterprise → "Get a demo"). Note which motion the CTA implies.
- **Component lead** — which of the five Chapter 2 components this variant leads with. Not two components — one primary lead per variant.
- **Traceability annotation** — one line naming: (a) which specific Exercise 01 component text produced the headline, (b) which specific Component 1 alternative this variant distinguishes against, (c) which specific Exercise 05 beachhead-segment characteristic the variant targets.

Recommended distribution across the three variants:

- **Variant 1** — leads with **value** (Component 3). The safest default; usually the highest-converting for cold inbound traffic.
- **Variant 2** — leads with **unique attribute** (Component 2). Good for a technically-oriented audience where the attribute is instantly legible.
- **Variant 3** — leads with **enemy-of-status-quo** or **promised-land framing** (Component 3 as pain, drawn from the Exercise 03 narrative Part 3). Good for a beachhead audience already primed by the narrative.

Optionally, sketch a rough above-the-fold layout for each variant (headline placement, image / visual, primary vs. secondary CTA, social proof strip). This is optional; the written variant is required.

### Part C — A/B test plan (45 min)

Per Chapter 7's Artifact 3 deliverable shape, produce `part-c-ab-test-plan.md`:

- **Success metric.** The operating funnel metric — usually demo-request rate, trial-signup rate, click-through to secondary content, or (for enterprise pages) "contact-us" form submission. Pick one; do not pick three. Include a one-sentence rationale for why this metric is the right one for the beachhead's sales motion.
- **Baseline.** The current hero's performance against the success metric. If you're using your own page, cite the last 30-90-day rate. If a public page, state the assumption you're making about the baseline and mark it `<!-- needs-research -->`.
- **Minimum detectable effect (MDE).** The relative uplift the test needs to prove to be actionable. Typical MDE for hero-copy tests is 20-40% relative — smaller effects are hard to detect with early-stage traffic volumes and hard to trust with the noise. Cite the calculator you used or the sample-size logic.
- **Sample size target.** Unique-visitor sample per variant, computed from the baseline + MDE + statistical-power targets (typically 80% power, 95% confidence). Show the calculation or cite the calculator ([evanmiller.org/ab-testing/sample-size.html](https://www.evanmiller.org/ab-testing/sample-size.html) is a common one).
- **Test duration.** Sample-size-target ÷ weekly-unique-visitor rate = duration in weeks. Include a floor (usually 2 weeks) to smooth day-of-week variance and a ceiling (usually 4-6 weeks) beyond which the test is either underpowered for the traffic or answering a question that has drifted.
- **Segmentation.** Which visitor segments the test result should be broken out by. At minimum: source (organic / paid / direct / referral), device (desktop / mobile), whether the visitor is in the beachhead segment (if you have firmographic enrichment).
- **The "not-a-positioning-test" caveat.** Per Chapter 6 — one round of losing hero variants is a losing hero variant, not a broken positioning. Three consecutive rounds of all-losing variants triggers Chapter 3's failure-mode diagnostic. State this in the test plan explicitly so the team doesn't over-interpret one A/B result as a positioning indictment.

### Part D — Derivation audit (30 min)

Chapter 6's key discipline: **messaging is derived from positioning, not invented.** The derivation audit is what proves it.

Produce `part-d-derivation-audit.md` as a table:

| Variant | Headline claim | Positioning source (Exercise 01 component text) | Alternative distinguished against (Exercise 01 Component 1) | Beachhead-segment reader (Exercise 05 memo) |
|---|---|---|---|---|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |

Every cell must be non-empty. Cell "Positioning source" must quote or reference specific text from the Exercise 01 positioning document — not a summary or a founder-narrated version. If a variant's headline claim cannot be traced to a specific line in Exercise 01, it is *invented*, not *derived* — and the variant must be either rewritten to derive properly or dropped.

Close the audit with the Chapter 6 "same story, different surface" consistency check: pick one Exercise 03 strategic-narrative claim (e.g., a Part 3 promised-land signal) and show how it appears — in surface-appropriate compression — in each of the three hero variants. If the narrative claim does not appear on any of the three, name the drift.

## Starter guidance

- Read Chapters 6 and 7's Artifact 3 sections before starting. Chapter 6 has the derivation templates; Chapter 7 has the ship discipline.
- **The single most common failure of this exercise is the "invented variant" — a headline that sounds clever but doesn't trace to the positioning.** The derivation audit in Part D is designed to catch this. If Part D's "Positioning source" cell is empty for any variant, the variant is not derived; rewrite it.
- **Do not lead all three variants with the same component.** The three-variant rule exists to force exploration of the space. If Variants 1, 2, and 3 all lead with value, cut two and rewrite them to lead with attribute and enemy-of-status-quo respectively.
- **The CTA is not a copywriting decision.** Chapter 6 argues the CTA is a sales-motion signal — "Sign up free" implies PLG; "Talk to sales" implies SDR-AE; "Get a demo" implies enterprise. Pick the CTA that matches your beachhead's sales motion; do not pick "Sign up free" if your beachhead requires a $50k ACV enterprise sale.
- **Do not test more than three variants.** The impulse to test five or six is real; the traffic volume at pre-Series-A does not support statistical power on that many arms. Three arms is the practical limit; if you have five candidate variants, cut to three by picking the ones that lead with the most distinct components.
- **The MDE conversation is where most A/B tests go wrong.** A team that tests for a 5% relative uplift on 200 weekly visitors per variant will run for six months and never find significance. Compute the sample size honestly; if the number is bigger than 8 weeks of traffic, either raise the MDE (only care about big effects) or pause the test until traffic is higher.
- **The consistency check in Part D is where the "same story, different surface" discipline lives or dies.** If the Exercise 03 promised-land slide says one thing and the three hero variants all say something else, the messaging has drifted from the narrative. Reconcile — usually the hero is wrong and the narrative is the source of truth, but occasionally the hero is right and it's the narrative slide that was authored casually.
- **The rewrite is *not* the point.** Shipping the rewrite instrumented — with a test plan a team can execute — is the point. A cleverer headline with no test plan is not the deliverable Chapter 7 named.
- If you are pre-launch and have no baseline, mark it `<!-- needs-research -->` and note in Part C that the test plan is provisional pending live traffic; still produce the plan.
- **Sensitivity to the beachhead.** If your Exercise 05 beachhead is a specific vertical (say, devtools/observability), the hero should be legible *to that segment first* — even if that means it reads slightly narrower than "everyone." A hero written for the general TAM is written for no one. The beachhead is the primary reader.

## Acceptance criteria

Your submission is complete when:

- [ ] Part A has the URL, date, screenshot, verbatim current hero, and a full Chapter 3 diagnostic tree walk with modes fired named.
- [ ] Part A includes the five-component read of the current page (with `Not stated` where the page doesn't articulate a component) and a one-paragraph gap analysis vs. your Exercise 01 positioning and Exercise 05 beachhead.
- [ ] Part B has three hero variants, each with headline + subhead + primary CTA + component lead + traceability annotation.
- [ ] Each of the three variants leads with a *different* Chapter 2 component (not all three leading with value).
- [ ] Every headline is ≤ 12 words. Every subhead is ≤ 30 words. Every CTA is ≤ 4 words. No variant violates the Chapter 6 anti-templates (category-only, comparative-superlative-only, "AI-powered X", customer-quote-only, founder-monologue).
- [ ] Part C names one success metric (with rationale), the baseline (or `needs-research` marker), the MDE, the sample-size target with computation shown or calculator cited, the test duration with floor/ceiling, and the segmentation cuts.
- [ ] Part C includes the "not-a-positioning-test" caveat naming when a losing test should trigger the Chapter 3 diagnostic vs. when it's just one variant.
- [ ] Part D's derivation audit table is populated for all three variants — no empty cells. Every "Positioning source" cell references specific Exercise 01 text; no variant is invented.
- [ ] Part D includes the "same story, different surface" consistency check tying the variants to at least one Exercise 03 narrative claim.
- [ ] The three variants collectively read as *the same product, three framings* — not three different products. If someone reading only the three variants (without the positioning behind them) would guess three different companies, the derivation has broken down.

## Common ways this exercise goes wrong

- **The "clever hero" trap.** A headline the founder likes that doesn't trace to the positioning. Part D exists to catch this; be honest.
- **Three value-lead variants.** Cut two, rewrite to lead with attribute and enemy-of-status-quo. Three variants of the same component is one variant three times.
- **Category-only hero.** "Developer productivity. Reimagined." Says nothing about value, best-for, or alternative. Rewrite.
- **AI-powered retrofit.** Adding "AI-powered" to a headline without a specific attribute is 2026 decoration. If the AI does something specific, name the specific thing.
- **Comparative-superlative hero.** "The smartest / fastest / simplest X" is Chapter 3 Mode 2. Name the underlying attribute; the "smartest" is the derived effect, not the hero copy.
- **CTA that contradicts the sales motion.** "Sign up free" on a page selling a $50k ACV enterprise product misroutes the visitor. Match the CTA to the motion.
- **No test plan.** The rewrite without the test plan is a copywriting exercise, not the ship artifact.
- **MDE set at 5%.** At pre-Series-A traffic levels, this is a test that will never conclude. Raise the MDE or pause the test.
- **Derivation audit with empty cells.** Every cell in Part D must be populated; empty cells mean the variant is invented.
- **Same story = same words.** The "same story, different surface" test does not mean the surfaces use identical words — it means the surfaces carry the same *claim* in surface-appropriate compressions. A hero can compress a promised-land claim into 8 words; a deck slide can spend a full slide on it; a cold-email hook can compress it into a phrase.
- **Shipping only one variant.** The Chapter 7 discipline is three; one variant is a founder's opinion, three is a test.
- **Reading a single-round losing test as a positioning failure.** One round of losing variants is one round of losing variants. Three rounds is the trigger for Chapter 3's diagnostic. State this in Part C so the team doesn't overreact.
