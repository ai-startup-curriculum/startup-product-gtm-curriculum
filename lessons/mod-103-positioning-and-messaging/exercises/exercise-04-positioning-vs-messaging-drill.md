# Exercise 04 — Positioning vs. Messaging Drill

**Estimated time:** 3 hours
**Chapter links:** [`01-positioning-vs-messaging.md`](../01-positioning-vs-messaging.md), [`06-messaging-derivation.md`](../06-messaging-derivation.md), [`03-three-positioning-failure-modes.md`](../03-three-positioning-failure-modes.md)
**Prerequisite reading:** Chapters 1, 3, and 6 read end-to-end (~90 min).

## Problem statement

Chapter 1 fixed the distinction that governs the whole module: **positioning is a strategic choice about which market context the product wins in; messaging is the tactical derivation into specific words on specific surfaces.** Positioning changes on a two-to-five-year cadence; messaging changes weekly. Broken positioning shows up as a messaging problem — the funnel underperforms, the team rewrites the hero, three consecutive rewrites move nothing, and the team is on the third tagline of the quarter with no way to name why.

This exercise trains the diagnostic muscle to name the correct cadence — *is this a positioning issue or a messaging issue?* — on real, ambiguous cases. It also trains the derivation muscle in the other direction — given a locked positioning, derive three messaging surfaces (a hero, a deck opener, a cold-email opener) that carry the same claim in surface-appropriate compressions.

The exercise has three parts: a classification drill (12 scenarios, each labelled positioning-problem / messaging-problem / both), a derivation drill (one positioning → three messaging surfaces), and a change-cadence audit (a hypothetical team's last-quarter positioning + messaging changes, judged against the Chapter 1 change-frequency table).

## Requirements

Deliver a folder `exercise-04/` with:

- `part-a-classification.md` — the 12-scenario classification drill.
- `part-b-derivation.md` — one positioning source → three derived messaging surfaces.
- `part-c-cadence-audit.md` — the change-cadence audit of a hypothetical team's last quarter.

### Part A — Classification drill (60 min)

For each of the 12 scenarios below, classify the *root cause* of the described symptom as:

- **P** — positioning problem (the strategic choice about market context is wrong; Chapter 3's failure modes fire).
- **M** — messaging problem (the positioning is defensible; the specific words on a specific surface are underperforming).
- **B** — both (the positioning is broken *and* the current messaging is compounding the failure).

For each scenario, produce (a) the classification, (b) a one-sentence justification citing the specific signal in the scenario, and (c) the specific next action — for P and B classifications, which Chapter 2 component to rebuild; for M classifications, which surface to rewrite and what to test.

Do not be tempted to classify everything as P. Real distributions are mixed; part of the exercise is calibration.

#### Scenarios

1. A B2B SaaS company's product-page hero has been rewritten three times in the last quarter — each rewrite tested against the previous with a 4-week A/B — and demo-request rate is unchanged. The competitor set on the "why us" page is the same three enterprise incumbents; win-loss analysis shows 70% of losses are "no decision" (status quo) rather than to the named competitors.

2. A PLG dev-tool company's "Sign Up Free" CTA is under-performing (3.2% CTR vs. 5.1% category benchmark) on the hero. The rest of the page — headline, subhead, feature strip — has strong engagement (scroll depth, time-on-page, secondary CTA click-through). The company shipped the current positioning ~14 months ago and has not touched it since.

3. A vertical-SaaS startup for dental practices has a hero that reads "The AI-native operating system for modern dentistry." Search traffic is zero; the sales team reports prospects on discovery calls ask "so, are you like a scheduling tool or a CRM or…?"

4. An analytics-tooling company's cold-email open rate has dropped from 22% to 9% over eight weeks. Subject lines are the same; recipient list has expanded from the beachhead segment (10-person data teams at Series-B fintechs) to include broader mid-market marketing analytics teams as well.

5. A code-review-automation startup has a strong hero — value + best-for compressed cleanly — but the pitch-deck opener slide reads "[Company] — the smartest code review platform." Prospects in first-meeting feedback report "the deck felt like a pitch, but the website felt like an argument for why we should care."

6. A HR-tech company's homepage headline is "The Employee Experience Platform." Bounce rate on the homepage is 78%; time-to-first-click is 42s. The founder ran a Dunford five-component workshop 18 months ago; the resulting positioning-document names "employee experience platform" as the category and the primary buyer as VP People, and buyers on discovery calls consistently mistake the product for a comms tool.

7. A fintech SaaS's product-page hero has been the same for 18 months: "Save 40% on transaction costs. Trusted by 500+ companies." Recent A/B test of a variant leading with a specific attribute ("Route each payment through the cheapest rail — automatically") beat the original by 34% in demo-request rate.

8. A category-creating startup ("developer productivity fabric") has run the multi-year Play Bigger-style category-design campaign — funded analyst briefings, executive-level content, sponsored conferences, a category page indexed on Google. Search volume for the category label is up 8× in 18 months. The team is now considering rewriting the hero to a simpler "developer productivity platform" because the sales team says "prospects are confused by 'fabric'."

9. A vertical-B2B startup for veterinary practices ran a Chapter 3 diagnostic on the hero and diagnosed Mode 2 ("we're better"). The hero was rewritten to name a specific attribute ("Automated recall reminders that catch 3× more overdue vaccinations"). Six weeks post-launch, demo-request rate is unchanged.

10. A messaging-tooling company launched a new pricing model six weeks ago (per-message-billed instead of per-seat). The hero copy still describes the product in per-seat terms; the pricing page reflects the new model. Sales team reports first-call confusion: "prospects come in expecting per-seat and are surprised when we describe billing."

11. A startup's positioning document (v3, dated three months ago) names manual spreadsheets and homegrown Python scripts as the primary competitive alternatives. The current hero copy compares the product to two direct competitors ("faster than X, cheaper than Y"). Win-loss reports show 12 of 15 recent losses were "we're going to keep using our spreadsheet."

12. A well-positioned dev-tool company (defensible five-component doc, credible narrative deck, clean beachhead) is running six ad variants across three channels. All six variants underperform relative to their organic-visitor conversion baseline. Two of the variants use hero copy that contradicts the positioning-doc's category label; four use hero copy that is directly quoted from the positioning doc.

### Part B — Derivation drill (75 min)

Take **one** locked positioning as input. You may use:

- Your own startup's Exercise 01 five-component positioning (preferred).
- The Loomly running-example positioning from Chapters 2 and 7.
- A public startup's positioning that you can reconstruct with high confidence from their site (in that case, note the source and any inferences you had to make).

Whichever you pick, produce a `part-b-derivation.md` that begins with the input positioning summarised in the Chapter 7 one-page format (or a link to your Exercise 01 output), then derives three messaging surfaces:

#### B1 — Product-page hero (three variants)

Per Chapter 6, three variants, each leading with a different component:

- **Variant 1** — leads with **value** (Chapter 2 Component 3).
- **Variant 2** — leads with **unique attribute** (Component 2).
- **Variant 3** — leads with **enemy of status quo** / promised-land framing (drawn from the Chapter 4 narrative or Component 3 value framed as a pain the buyer already recognises).

Each variant = headline (5-12 words) + subhead (15-30 words) + primary CTA (2-4 words). For each variant, one sentence naming which component it leads with and which alternative from Component 1 it distinguishes against.

#### B2 — Pitch-deck opener (slides 1-3)

Per Chapter 6, the deck opener is the strategic-narrative shift → enemy → promised land compressed into three slides. Deliver:

- **Slide 1 title** (5-10 words, names the shift) + one-line body + one-line speaker note.
- **Slide 2 title** (names the enemy worldview) + one-line body + one-line speaker note.
- **Slide 3 title** (names the promised land) + one-line body + one-line speaker note.

The product does not appear in slides 1-3. If it does, rewrite.

#### B3 — Cold-outbound opening line

Per Chapter 6, the cold-email opener is one sentence (occasionally two) that establishes relevance + hooks the value. Deliver **two variants**:

- **Variant 1** — anchored on a specific trigger event (funding round, hiring push, product release, published writing). Name the trigger you're anchoring to.
- **Variant 2** — anchored on a specific segment signal (job title, company stage, technology in stack). Name the segment signal.

For each, one sentence naming why the buyer would keep reading past the first line.

#### The consistency check

After deriving all three surfaces, run the Chapter 6 "same story, different surface" test. In a short summary (100-200 words):

- Pick one specific claim from your input positioning (e.g., "engineering managers stop being the pager for stalled reviews").
- Show how the claim appears — in surface-appropriate compression — on each of the three surfaces (hero variant, deck opener promised-land slide, cold-email hook).
- If the claim does *not* appear consistently, name where the drift is and which surface you would rewrite to fix it.

### Part C — Change-cadence audit (45 min)

The following is a hypothetical team's changelog for the last quarter. Audit it against Chapter 1's change-frequency table (positioning changes rarely; messaging changes weekly).

For each entry, classify as (a) a *positioning* change, (b) a *messaging* change, or (c) *neither* (mission / brand / operational). Then judge the cadence — is the team iterating at the right frequency, or are they treating positioning as messaging (repositioning quarterly) or messaging as positioning (never changing hero copy)?

#### The team's last-quarter changelog

| Week | Change |
|---|---|
| 1 | Rewrote hero copy on product page (variant test vs. previous; new variant leads with "faster deployments" claim). |
| 2 | Changed primary category label on the homepage from "developer productivity platform" to "engineering intelligence" (updated in nav, footer, meta description). |
| 3 | Ran A/B test on primary CTA text ("Get a demo" vs. "Talk to sales"). |
| 4 | Updated pitch deck with new "why now" slide (referencing recent GitHub-Copilot adoption stats). |
| 5 | Changed the "best-for" description on the product page from "for engineering managers" to "for engineering leaders" (including VPs and directors). |
| 6 | Added a new comparison-page comparing the product to a new competitor that launched last month. |
| 7 | Ran A/B test on hero subhead (three variants). |
| 8 | Rebranded — new logo, new colour palette, new fonts across all surfaces. |
| 9 | Updated the mission statement in the footer and About page ("empowering every engineering team to ship faster" → "the standard for engineering leadership"). |
| 10 | Changed the primary pricing metric on the pricing page from "per seat" to "per active user." |
| 11 | Rewrote the pitch-deck opener slide (the "shift" slide) to name a different underlying shift than the previous quarter's version. |
| 12 | Ran A/B test on sales-email subject line for cold outbound (four variants). |
| 13 | Announced a new segment focus in an All-Hands ("we are now focused on 100-500-engineer companies in fintech and healthtech; deprioritising the SMB devtools segment we started in"). |

Produce `part-c-cadence-audit.md` with:

1. A table classifying each entry as P (positioning), M (messaging), or N (neither).
2. A summary paragraph (150-250 words) reading the pattern:
   - How many positioning changes did the team make? How many messaging changes? Are the cadences appropriate?
   - Which entries would you flag as *actual positioning shifts* that the team should have treated with higher deliberation (documentation, versioning, downstream artifact rebuild)?
   - Which entries are theatre — cosmetic changes labelled as "positioning" that are actually just messaging or brand?
   - What would you have done differently if you were the CMO / founder running this quarter?

## Starter guidance

- Read Chapters 1 and 6 end-to-end before starting. The change-frequency table (Chapter 1) and the derivation protocol (Chapter 6) are the operating rubrics.
- **Part A calibration:** in a real portfolio of 12 real scenarios, expect roughly a 4/4/4 split across P / M / B — not "everything is positioning." If your Part A answers are all P, you're over-diagnosing.
- The clearest signal for a *messaging* problem is: the positioning has been recently defended (Dunford workshop, discovery corpus fresh, category label matches buyer language) *and* only one or two surfaces are underperforming while others convert. The clearest signal for a *positioning* problem is: multiple surfaces underperform simultaneously *and* the changes to individual surfaces move nothing.
- **Part B derivation:** the "always three variants" rule is not a formality. If you find yourself writing three variants that all lead with the same component, you have not explored the space — cut two and rewrite them to lead with different components. The variants are the exploration.
- **Part B consistency check:** if the claim in the deck's promised-land slide contradicts the hero, either the positioning has drifted (rare — treat it as a versioning event) or one of the surfaces was written without deriving from the positioning source (common — rewrite that surface).
- **Part C:** the change-cadence audit is a diagnostic; the team in the scenario is loosely modelled on the average early-stage startup, which under-iterates messaging and over-iterates positioning simultaneously. If your audit's read is "this team is thrashing", you have named the correct pattern.
- The point of Part C is not to be scolding. Some entries in the changelog are legitimate — Week 8's rebrand, Week 10's pricing metric change, Week 13's segment focus shift each have plausible cases for being deliberate strategic moves. The audit's job is to name which ones deserved that deliberation and which ones were casual.
- If a Part A scenario looks ambiguous, name the ambiguity and pick the most-likely classification. There is not a single canonical answer; the exercise is the reasoning, not the label.

## Acceptance criteria

Your submission is complete when:

- [ ] Part A classifies all 12 scenarios (P / M / B) with a one-sentence justification citing the specific signal and a specific next action (Chapter 2 component to rebuild for P/B; specific surface + test for M).
- [ ] Part A shows calibration — not all 12 scenarios classified as the same type. If the classification skews heavily one way, one sentence in the summary explains why the specific set of scenarios warranted that skew.
- [ ] Part B begins with the input positioning (either linked to Exercise 01, transcribed from the running Loomly example, or reconstructed from a real startup with sources noted).
- [ ] Part B1 has three hero variants, each with headline + subhead + CTA, each leading with a different Chapter 2 component labelled explicitly.
- [ ] Part B2 has three deck-opener slides (shift / enemy / promised-land) with titles, bodies, and speaker notes. The product name does not appear on any of the three.
- [ ] Part B3 has two cold-outbound opening lines with trigger / segment-signal anchors named.
- [ ] Part B ends with the "same story, different surface" consistency check — one claim traced across the three surfaces, with any drift explicitly named.
- [ ] Part C classifies all 13 changelog entries (P / M / N) with a one-line rationale each.
- [ ] Part C's summary paragraph reads the pattern — cadence appropriateness, which entries deserved higher deliberation, which were theatre, what the audit would do differently.
- [ ] The submission distinguishes cleanly between the two directions of the mistake — treating positioning as messaging (repositioning weekly) *and* treating messaging as positioning (never touching the hero). Both patterns appear in the changelog; both are named.

## Common ways this exercise goes wrong

- **Classifying every Part A scenario as positioning.** The over-index on positioning is itself a diagnostic error. Some funnels really do have messaging problems on top of defensible positioning; if you cannot name any messaging-only cases, re-read Chapter 6.
- **Part A justifications that repeat the scenario.** The justification is the signal. "The team rewrote the hero three times and nothing moved" is the scenario; "three consecutive hero variants underperforming with the same underlying positioning is Chapter 3's diagnostic trigger for a positioning problem, not a hero problem" is the justification.
- **Part B variants that all lead with the same component.** The three-variant rule exists to force exploration. If all three are value-leading, you have written one variant three times.
- **Part B deck-opener with the product on slide 1.** If the product appears in slides 1-3, the deck-opener is a product-feature deck with narrative window-dressing. Rewrite.
- **Part B cold-outbound anchored on nothing specific.** "Hi, I saw your company and thought…" is not a trigger. If the opener would apply to any recipient, it is not a cold-outbound opener; it is a template.
- **Part B consistency check that doesn't actually test consistency.** The check is "same claim, different surface-appropriate compression." If the three surfaces make three different claims, the derivation broke down and the exercise is to name where.
- **Part C confusing brand for positioning.** Week 8's rebrand is a brand change (visual identity) — it is only a positioning change if it changed the *five components*. Distinguish carefully.
- **Part C treating every messaging change as trivial.** Some messaging changes (Week 7's hero subhead A/B) are healthy; if the team never runs those tests, they are also failing the discipline. Cadence read requires naming both under- and over-iteration.
- **Part C making the summary a scorecard.** The summary is a pattern-read, not a grade. Focus on the *pattern* the changelog reveals and what a founder should learn from it.
- **Not marking `needs-research`.** If you cited a benchmark number ("category CTR benchmark is 5.1%") in Part A that you cannot source, mark it `needs-research` rather than presenting it as authoritative.
