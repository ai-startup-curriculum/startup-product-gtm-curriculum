# The Disqualification Checklist — Naming Who Is *Not* the ICP

## Motivation

Chapter 2 named the two-layer scoring model — firmographic criteria and behavioural criteria, each weighted, some marked "must-have." This chapter develops the must-have half into its own first-class artifact: **the disqualification checklist**.

The reason it deserves its own chapter is that the discipline is inverted. A qualification list names *who to say yes to*; a disqualification list names *who to say no to*. Founders write the first list eagerly and the second list reluctantly. The result is an ICP that reads like a warm invitation and closes deals at 15% instead of 35%, because the AE — trained to look for yes-signals — hedges on every deal that has a mixed profile and stays in the pipeline forever.

The failure mode this chapter exists to catch: **the pipeline is 3× the size it should be, the close rate is half what it should be, and the average sales cycle length is twice what it should be, because no deal ever gets a clean "not our ICP — moving on" verdict.** Every deal stays open. Every deal absorbs AE time. Every deal gets a "let me think about it" from a buyer who was never going to buy, and the AE follows up for three months.

A disqualifier is the specific artifact that gives the AE permission — and the operating discipline — to close-lost early, cleanly, and without escalation. The checklist is the thing that makes the ICP a *filter* instead of a wish.

## Core concepts

### The definition — a disqualifier is a criterion that hard-fails the deal *regardless of other criteria*

A disqualifier is not "a weak fit" or "a signal that the deal is harder." A disqualifier is a criterion whose failure is *sufficient by itself* to close the deal lost, no matter how strong the fit is on every other axis.

The test: **if this criterion fails, is the deal dead — even if every other criterion is a perfect score?** If yes, it is a disqualifier. If the answer is "the deal is harder but still winnable," it is a should-have (weight 2 or 3), not a disqualifier.

The distinction is operational. A should-have miss produces an *in-with-caveat* deal — the AE continues the cycle, names the gap as a known risk, and prices / structures around it. A disqualifier miss produces an *out* deal — the AE ends the cycle at the discovery call with a clean close-lost verdict.

The mistake founders make: treating everything as a "signal" instead of naming the two-to-four hard-stop criteria that produce clean closes. Everything gets weighted; nothing hard-fails; every deal drags.

### Why disqualifiers save more than they lose

The founder anxiety about disqualifiers is asymmetric — "what if we disqualify a deal that would have closed?" — and the counter is asymmetric too. A disqualifier that eliminates a real deal costs the ACV of that deal. A missing disqualifier that keeps a doomed deal in the pipeline for three months costs the AE-hours the deal absorbs, plus the *opportunity cost* of the deals the AE did not work because they were servicing the doomed one, plus the pipeline-forecast distortion the doomed deal introduces.

At a typical SEED-stage motion, an AE running 25 active opportunities can afford to close-lose the wrong ones in the first call. An AE running 60 active opportunities because nothing ever gets disqualified is running a broken motion — the extra 35 are absorbing time and producing nothing. The disqualification checklist is what shrinks the pipeline back to the working set.

The reference frame from Andy Raskin, Kazanjy (mod-105), and April Dunford is the same: **"no" is a full-value answer**. A fast "no" is worth the price of a slow "yes" because it frees the AE to work the next real deal. The checklist enforces the fast "no."

### The four disqualifier archetypes

Every disqualifier on a well-authored checklist fits one of four archetypes. Naming the archetype is what keeps the checklist from becoming an anxiety list.

**Archetype 1 — the whole-product gap disqualifier.** The prospect requires a product surface you do not have and will not ship in the sales-cycle window. Common examples: SSO / SCIM for a product that does not have them; SOC 2 Type II for a security-conscious buyer at a product that only has Type I; HIPAA / GDPR-DPA for a regulated buyer; a specific integration (Snowflake, GitHub Enterprise Server, Okta) the product does not support. The disqualifier is the *product surface missing*, not the buyer.

Whole-product gap disqualifiers usually come with a "revisit when" clause — "revisit when SSO ships" — that goes on a nurture list. The deal is not lost forever; it is out of scope *today*.

**Archetype 2 — the ACV / budget-authority disqualifier.** The prospect's buying-motion posture cannot support the ACV. Common examples: "purchases > $10k require a formal RFP" (against an ACV of $25k with no RFP capability); "no departmental budget for tools" (against a product priced above the departmental threshold); "procurement gates all software purchases through a legal review that takes 90 days" (against a 30-day sales cycle target).

ACV disqualifiers are the ones founders resist most because "we could downsell" or "we could work through procurement." Both are usually false economies at SEED — the downsell breaks the pricing anchor for future deals, and working through 90-day procurement burns AE-quarters on a deal that closes at a discount.

**Archetype 3 — the pain-severity disqualifier.** The prospect does not have the pain the product solves, or has it at insufficient severity to motivate a purchase. Common examples: no metric owner (no one on the buyer's side has a KPI tied to the outcome the product moves); no active pain (the buyer is "thinking about it" but has no pressing reason to act this quarter); the pain is real but has been priced in ("we live with it, we've built workarounds").

Pain-severity disqualifiers are the hardest to write cleanly because "no active pain" is not a Layer-1 firmographic — it surfaces only in conversation. The remedy is a specific behavioural question ("what happens in your organisation if this problem is still unsolved in six months?") that either produces a specific consequence or produces a shrug. The shrug is the disqualifier.

**Archetype 4 — the beachhead-scope disqualifier.** The prospect sits outside the current beachhead segment (mod-103 Chapter 5) even if it might be in-scope for a future segment. Common examples: enterprise prospect when the beachhead is mid-market; healthcare prospect when the beachhead is B2B SaaS devtools; APAC prospect when the beachhead is US / EU.

Beachhead-scope disqualifiers are the ones the mod-103 not-now list already committed to. Enforcing them at the ICP disqualifier level is the ICP's job — it prevents the AE from taking a "we could just work this one deal" exception that breaks the beachhead commitment across the board. Chapter 6 develops the ICP-level enforcement of the beachhead choice.

Two to four disqualifiers is the working range for a SEED-stage ICP — typically one whole-product-gap, one ACV, one pain-severity, and one beachhead-scope. Fewer than two and the checklist under-filters; more than five and the AE loses track and starts hedging.

### Anti-signals — the softer signal set

A disqualifier is a hard stop. An anti-signal is a soft warning: "this deal is harder than it looks; if you see two of these, escalate to the founder before spending another five hours." Anti-signals are useful to name explicitly but they are not disqualifiers.

Common anti-signals:

- **"We're looking at a few options and want to see demos of each."** The buyer is not seriously buying; they are gathering intel or building an internal committee's paperwork. Individually a mild negative; combined with "no budget assigned yet," strong reason to slow the AE's investment.
- **"We're a small team, this is a side project for the eng manager."** Suggests low urgency, no metric ownership, and a champion who does not have the political capital to close.
- **"We used [alternative] before and it didn't work."** Sometimes because the alternative was genuinely wrong; often because the buying process was not real the first time either.
- **"We have to loop in security / legal / IT / finance before signing."** Load-bearing signal for cycle length and drop-off; frequently overlooked by AEs who don't want to think about it.
- **"The person we're talking to is not the decision-maker but promises to bring it back to the CEO."** The champion-without-authority pattern (Chapter 4).

The rule with anti-signals: **any single one is a caveat; two or more is a "reconsider whether this is really in ICP" check.** They belong on the scorecard as a separate section, not folded into the weighted-criteria layer.

### Ranked reasons a "no" is more valuable than a "maybe"

Founder-led sales (mod-105) and first-hire sales training both hinge on the same insight: an early clean "no" is worth more than a late murky "maybe." The disqualifier discipline enforces the early clean "no" by providing named criteria the AE can point at. The value stack:

1. **Free AE time.** The single largest cost of a doomed pipeline. An AE working 25 real deals closes more than one working 60 mostly-doomed deals.
2. **Honest forecast.** The founder / CEO can forecast the quarter honestly only if the pipeline is honest. A pipeline padded with doomed deals distorts the forecast and hides real gaps.
3. **Sales-cycle-length signal.** The average cycle time is a metric-level input to the demand-gen and hiring plan. Cycle time inflated by doomed deals that eventually close-lose at week 12 is uninterpretable.
4. **Close-rate signal.** The close rate on real deals is a leading indicator of PMF durability (mod-102) and pricing (mod-106). If the close rate is dragged down by unqualified deals, both signals are lost.
5. **Buyer's time.** The buyer who is not going to buy also has better things to do than a five-touch sales cycle they will exit at proposal. A clean early "we don't think this is a fit — here's a peer product that might be" is the ethical answer as well as the operational one.

### The "revisit when" clause — disqualifiers that unlock over time

Not every disqualifier is permanent. Some — especially Archetype 1 (whole-product-gap) and Archetype 4 (beachhead-scope) — have a specific unlock condition that turns the "out" into a "revisit."

The disqualifier authoring pattern:

```
Disqualifier: Company enforces SSO across engineering tools; product does not yet support SSO.
Action on hit: close-lost with reason code "unshipped SSO"; add to SSO-launch nurture list.
Unlock condition: SSO ships (target: Q3).
Revisit trigger: automated email to the champion 2 weeks after SSO launch.
```

The unlock condition serves two purposes: it makes the disqualifier a *conditional* out (which is emotionally easier to enforce because the deal isn't lost forever), and it feeds mod-108's nurture-list discipline. Every hard "no" today with an unlock condition becomes a warm re-open when the unlock condition trips.

The pattern breaks when disqualifiers with no plausible unlock — pain-severity disqualifiers where the buyer has no urgency, ACV disqualifiers where the buyer literally cannot spend at the price point — get an aspirational "revisit when the CEO changes" unlock. That is not an unlock; that is refusing to close-lose. If the disqualifier has no plausible timed unlock, close it out cleanly.

### The checklist ships as part of the ICP scorecard — not separately

A common failure is to author the disqualification checklist as its own document, separate from the ICP scorecard. The AE ends up with two artifacts, uses one, forgets the other. The disqualification checklist is a **section of the one-page ICP scorecard** (Chapter 7's format) — the section labeled *Must-haves* or *Disqualifiers* — physically adjacent to the qualification criteria.

The reason is operational: the AE is scoring in real time. If the disqualifiers live on a different page (or worse, in a different tool), the AE will not check them until the "wrap-up" step, by which time the AE has already invested 45 minutes in a deal that could have been closed at minute 5. Putting the disqualifiers physically adjacent to the qualifying criteria makes the check the first step in the flow.

### Enforcement — the AE has to be *authorised* to disqualify

The subtlest failure mode: the disqualification checklist exists, but the AE is not authorised to actually close-lose a deal against it. Every "out" has to be re-approved by the founder or sales leader. The AE, unwilling to bring 40% of their pipeline into a weekly review as "close-lost," instead marks the deals as "long-cycle" and the pipeline stays inflated.

The remedy: **the ICP disqualification checklist explicitly authorises the AE to close-lose in the first-call verdict against a named disqualifier.** The founder / sales leader reviews the reason codes weekly (Chapter 7's operating cadence), but does not require pre-approval for individual close-losses. The AE's judgment against the named criteria is the authorisation.

This is a governance choice the founder makes when shipping the ICP artifact. Without it, the checklist is theatre — the criteria exist, the AE knows them, and nobody enforces them.

## Concrete example — Loomly's disqualification checklist

Extending the Chapter 2 Loomly ICP with a disqualification checklist:

### Disqualifiers (must-haves — failing any is a first-call close-lose)

| # | Disqualifier | Archetype | Discovery question | Action on hit | Unlock condition |
|---|---|---|---|---|---|
| D1 | Not using GitHub as primary code host (GitLab / Bitbucket / Perforce / self-hosted) | Whole-product gap | "What's your primary code host — GitHub, GitLab, or something else?" | Close-lost, reason "unsupported code host" | Multi-host support ships (not on roadmap) |
| D2 | No metric owner for engineering throughput or cycle time | Pain-severity | "Does anyone on the engineering leadership team have a throughput or cycle-time metric they report up?" | Close-lost, reason "no metric owner" | None — this is a permanent disqualifier for the current ICP |
| D3 | Purchases at ACV ≥ $12k require formal RFP or 90+ day procurement | ACV / budget-authority | "For tools in this budget range — say $10-25k a year — how does the purchase process work?" | Close-lost, reason "procurement-gated"; refer to Loomly Enterprise waitlist | Enterprise motion + procurement-support ships (Series-A gate) |
| D4 | Enterprise-scale (> 500 engineers) | Beachhead-scope | Filter at list-build; verify on call ("how many engineers overall?") | Close-lost, reason "outside beachhead"; add to enterprise waitlist | Enterprise product-surface ships (SSO, SCIM, audit logs — target: Series-A) |

Four disqualifiers, spanning all four archetypes. The AE is authorised to close-lose against any single one in the first-call verdict; the founder reviews the weekly reason-code roll-up.

### Anti-signals (soft warnings — one is a caveat; two escalate)

- The engineering leader we're talking to describes the pain in the third person ("our team feels this pain") rather than the first ("I feel this pain").
- The company has adopted no new engineering-productivity tool in the past 24 months.
- The conversation with the champion has not surfaced who the economic buyer is (VP Eng, CTO, or CEO).
- The prospect has explicitly said "we're just gathering information."

None of these hard-fails the deal. Any two together triggers a mid-cycle re-qualification: does this deal still belong in the pipeline?

### Contrast — the pre-disqualifier Loomly pipeline

Before the disqualification checklist was authored, Loomly's founder was running the following pipeline pattern:

- 60 active opportunities in Salesforce, all in "discovery" or "demo" stage.
- Average cycle length: 74 days.
- Close rate at proposal: 22%.
- Reason codes on close-lost: "unresponsive," "chose competitor," "budget."

After the checklist:

- 28 active opportunities. 32 previously-active deals were closed-lost in first-call re-qualification against the four disqualifiers.
- Average cycle length: 32 days (measured on the disqualifier-passing set).
- Close rate at proposal: 41%.
- Reason codes on close-lost: named disqualifier archetype (whole-product gap, ACV, pain-severity, beachhead-scope) plus specific criterion.

Same product. Same AE. The checklist is what changed. (Numbers are illustrative of the pattern; treat as an example not a benchmark.)

## Common failure patterns

- **No disqualification section.** ICP has only positive criteria; no deal ever hard-fails; pipeline inflates; close rate drops. The most common failure and the most costly.
- **Everything weighted, nothing disqualifying.** The scorecard has weights but no must-haves. A deal that fails on every axis still scores 30% and stays in the pipeline as "long cycle." Disqualifiers must exist as hard stops.
- **Disqualifiers as separate document.** The checklist lives in a Notion page, the scorecard lives in Salesforce, the AE checks one and forgets the other. Put them adjacent on the one-page artifact.
- **Disqualifiers the AE is not authorised to enforce.** The checklist exists but every close-lost needs founder sign-off; the AE gives up and marks deals as "long-cycle." Explicit AE authorisation is required.
- **Disqualifiers without discovery questions.** The AE cannot enforce a disqualifier without a specific question to ask. Each disqualifier needs the exact 15-word question that surfaces the answer.
- **Aspirational "revisit when" that never trips.** "Revisit when the CEO changes" is not an unlock condition. If the disqualifier has no plausible unlock, close it cleanly and stop maintaining the nurture list.
- **Confusing anti-signals with disqualifiers.** A caveat is not a hard stop. Keep the two sections separate; the AE actions them differently.
- **Over-disqualifying.** Six or seven disqualifiers is too many — the AE loses track, or every deal fails at least one. Two to four is the working range.
- **Disqualifier that is really a beachhead question dressed as pain-severity.** "Company doesn't run continuous deployment" for a product that could probably serve monthly-deploy shops if it wanted to is a beachhead-scope disqualifier, not a pain-severity one. Naming the archetype correctly matters for the "revisit when" clause.
- **Founder overriding the AE's disqualifier calls in weekly review.** If every AE close-lost gets re-opened by the founder, the AE stops enforcing. The founder's job is to review the *criteria*, not the individual decisions.

## Summary

- A **disqualifier** is a criterion that hard-fails the deal regardless of other criteria. The test: if this criterion fails, is the deal dead even if every other criterion is a perfect score?
- **Two to four disqualifiers** is the working range for a SEED-stage ICP — typically one each of the four archetypes.
- The **four disqualifier archetypes**: whole-product gap (Archetype 1), ACV / budget-authority (Archetype 2), pain-severity (Archetype 3), beachhead-scope (Archetype 4).
- **Anti-signals** are soft warnings — any single one is a caveat, two or more triggers a mid-cycle re-qualification. Keep them separate from disqualifiers.
- Every disqualifier has (a) a **specific discovery question** the AE can ask, (b) a **reason code** for close-lost, and (c) either an **unlock condition** (revisit trigger) or an explicit "no unlock — permanent for this ICP" note.
- The disqualification checklist **ships as a section of the one-page ICP scorecard**, physically adjacent to the qualifying criteria. Separate documents get forgotten in real-time scoring.
- The AE must be **explicitly authorised** to close-lose against a named disqualifier without founder pre-approval. Without the authorisation, the checklist is theatre.
- The pipeline benefit is **asymmetric**: a fast clean "no" frees AE time, honestifies the forecast, sharpens cycle-length and close-rate signals, and respects the buyer's time. A missing disqualifier costs three months of AE-hours per doomed deal.
- Chapter 4 develops the **buyer / user / champion persona split**, which turns out to be where a whole additional class of disqualifiers lives — "no economic buyer identified" is a common late-stage killer that a persona-anchored ICP catches early.
