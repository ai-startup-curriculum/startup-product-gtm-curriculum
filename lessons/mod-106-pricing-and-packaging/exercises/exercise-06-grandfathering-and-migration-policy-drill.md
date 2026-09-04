# Exercise 06 — Grandfathering and Migration Policy Drill

**Estimated time:** 2 hours
**Chapter link:** [`05-price-experiments-and-grandfathering.md`](../05-price-experiments-and-grandfathering.md)
**Prerequisite:** Chapter 5 read end-to-end (specifically the grandfathering section); a pricing change (real or hypothetical) you would apply to existing customers — from Exercise 03's tier composition, Exercise 04's metric decision, or Exercise 05's plan-tier experiment; a working list of ~10-30 named existing customers (real if you have them, or a plausible representative sample if pre-launch) that the migration would affect.

## Problem statement

Chapter 5 named the failure modes: ad-hoc grandfathering (case-by-case decisions producing a mosaic of pricing regimes); silent price migrations (customer discovers change on next invoice); grandfathering forever without sunset (three years later 40 customers still on legacy pricing no one remembers); grandfathering used as retention bribery (customer threatens churn to get old price); no lock-in period offered (30-day notice causes churn spike). The remedy is a **pre-committed grandfathering policy** — one rule, applied uniformly, communicated to every affected customer in writing, tracked in the CRM as a cohort with a defined sunset date.

This exercise trains you to **author the grandfathering policy + the migration communication + the tracking discipline for one specific pricing change** end-to-end. The output is the artifact that answers "what happens to our existing 40 customers when we ship v3.2?" in one page — including the policy, the per-customer migration path, the communication, and the sunset tracking.

The failure mode this exercise exists to catch: **the founder ships new pricing, doesn't decide the grandfathering policy up front, and applies case-by-case decisions to the first 5 renewals. By month 6 the customer base has 4 different pricing regimes no one can enumerate, the finance team spends 3 quarters reconciling, and customers who paid the "new" price feel gouged when they hear a peer got grandfathered.**

## Requirements

Deliver a folder `exercise-06/` with:

- `part-a-policy-selection-and-rationale.md` — the four-policy trade-off analysis and the specific policy chosen with justification.
- `part-b-migration-communication-and-tracking.md` — the customer email, the CRM tagging scheme, the sunset date, the finance reconciliation plan.
- `part-c-edge-cases-and-anti-patterns.md` — the edge-case handling matrix + the Chapter 5 anti-pattern teardown.

### Part A — Policy selection and rationale (45 min)

Deliver `part-a-policy-selection-and-rationale.md`.

**A1 — The pricing change scope (10 min).** Name the specific change requiring a grandfathering decision:

- **What's changing** — the specific tier / metric / price change. Reference the source exercise (E03 tier composition, E04 metric, E05 plan-tier experiment) or the hypothetical.
- **Direction and magnitude** — price up or down; by how much; for which tier / customer segment.
- **Whose bill would change** — how many existing customers, what fraction of ARR, what their current-vs-new bill would look like. Include a small worked example: "Customer X currently pays $10K/year on 100 repos at $10/repo flat; under new pricing (volume tier at $12 → $10 → $8), same customer would pay ~$8K/year — decrease. Customer Y pays $5K/year on 40 repos, would pay $5.76K/year — increase."
- **The unaffected customers** — who's not affected by this change and why (segmentation, tier, timing).

**A2 — Four-policy trade-off analysis (20 min).** Chapter 5's four policies. Score each against your specific change:

| Policy | Trust impact | ARR impact (12 mo) | Complexity | When it fits |
|---|---|---|---|---|
| Full grandfather — indefinite | High preservation; low friction | Low (legacy base never migrates) | Low (no ongoing decisions) | Small legacy cohort; change is minor; brand-loyalty at stake |
| Full grandfather — sunset window | Preservation with a bounded end | Medium (migrated at renewal + sunset date) | Medium (CRM tracking; per-customer sunset dates) | Modal choice for well-run transitions |
| Partial grandfather — feature or metric only | Complex to explain; sometimes fine | Depends on the specific partition | High (two co-existing pricing systems) | Tier composition changed, price not — or vice versa |
| No grandfather — immediate migration | High risk of churn spike; only if change is trivial or product substantially changed | High immediate | Low (one-time change) | Rare; use only when the old pricing is demonstrably unsustainable |

For each of the four, write:

- **Would this policy fit our change? Yes / partial / no + one-sentence reason.**
- **Estimated 12-month ARR impact vs. status quo** — a rough band, not a point (Chapter 5's discipline).
- **The specific risk this policy creates** — churn, trust event, complexity, revenue-left-on-table.

**A3 — Pick the policy (10 min).** State the specific policy you're picking with a written justification. If sunset-window (the modal choice), name:

- **The sunset window length** (typically 12-24 months from launch; Chapter 5's modal is "current contract term + 12 months").
- **The migration trigger** (renewal date, calendar date, or the earlier of the two).
- **The lock-in offer** (Chapter 5: existing customers should have the option to renew at their current price for one more term as good-faith preservation).
- **What happens if a customer requests early migration** (they get the new pricing at their next renewal; they do not get retro-refund on the current period).
- **What happens if a customer's usage grows past their current tier's cap during the grandfather period** (edge case — usually the new pricing applies to the incremental usage; state your rule).

**A4 — Board / investor framing (5 min).** One paragraph explaining the policy to a board member — what ARR-impact deferral means for the pricing revision's headline number, when the deferral clears, why the trust preservation is worth the deferral. This is the "the pricing pack shipped v3.2 and its full ARR impact will land over 12 months of grandfather sunset" framing that avoids the board misreading Q1 ARR as "the price change didn't work."

### Part B — Migration communication and tracking (45 min)

Deliver `part-b-migration-communication-and-tracking.md`.

**B1 — Existing-customer email (15 min).** Draft the actual email that goes to every affected existing customer. Content:

- **What's changing** — one paragraph in the customer's language, not internal pricing jargon.
- **What this means for their bill** — their specific current bill vs. their bill under new pricing at their next renewal. If per-customer personalisation isn't possible for the mass mailing, offer a self-serve preview ("log in to see your projected new bill" or "your account manager can walk you through it").
- **When the change takes effect for them** — the specific date at their renewal, plus the sunset date if applicable.
- **What they can do** — lock in current pricing for one more term (Chapter 5's lock-in offer), migrate now to new pricing (if they'll benefit), or do nothing (migrated at sunset).
- **Who to contact** — a named person (account manager, CS lead, or founder at seed) with an email or Calendly link.
- **The FAQ** — 3-5 anticipated questions and answers. Common: "Am I being grandfathered?" / "Why are you changing pricing?" / "Can I extend my grandfather?" / "What if I want to upgrade a tier under my current pricing?"

The email is written; not sketched. Any customer-facing communication that ships as a fill-in-the-blank template later inherits errors — write it now.

**B2 — Public / community communication (10 min).** If the change is public (usually a pricing-page change is), draft:

- **The pricing page banner or note** — "Existing customers keep current pricing until {date}; see the migration policy for details."
- **The blog / community post** (or a note that no public post is planned) — one paragraph on the change, one paragraph on the grandfather policy, one paragraph on the reasoning.
- **The sales-team briefing** — what AEs / CS say when a customer asks. The specific script.

**B3 — CRM tagging and cohort scheme (10 min).** Chapter 5's tracking discipline: three cohorts at minimum after a change.

- **"Grandfathered — old pricing"** — customers who signed under old pricing and are still on it.
- **"Grandfathered — migrated early"** — customers who voluntarily migrated to new pricing before sunset.
- **"Migrated at sunset"** — customers who migrated at their scheduled sunset date.
- **"New — new pricing"** — customers who signed after the change.

Define:

- **The CRM field or column** that holds the tag.
- **When and how each customer transitions between tags** — the automation (or manual process) that reassigns.
- **The reports that read the tags** — per-cohort ARPU, retention, count. Chapter 5's cohort tracking depends on these tags being correct.
- **What happens if the tag is missing** — default to flagged-for-review, not silently one or the other.

**B4 — Finance reconciliation plan (5 min).** The specific reconciliation the finance team will do:

- **The sunset schedule** — a table listing every grandfathered customer's sunset date. Should be zero-length at the sunset window's end.
- **The monthly reconciliation** — "at end of each month, finance runs the report of grandfathered customers whose sunset date has passed; any that have not migrated get escalated."
- **The revenue attribution** — how ARR is attributed to old-pricing vs. new-pricing cohorts in the monthly finance report.
- **The de-grandfathered cohort verification** — a quarterly check that the "old pricing" cohort is actually shrinking on schedule.

### Part C — Edge cases + anti-pattern teardown (30 min)

Deliver `part-c-edge-cases-and-anti-patterns.md`.

**C1 — Edge-case handling matrix (15 min).** For each edge case, name the policy:

- **Customer requests longer grandfather than the standard window.** — do you extend? Under what conditions (multi-year prepay, strategic account, referrer)? If you extend, is the extension standardised (max +12 months for named strategic accounts) or bespoke (case-by-case is Chapter 5's ad-hoc-grandfathering trap; avoid)?
- **Customer requests early migration to get new lower price (if the change is a price drop for their segment).** — allowed? On the standard renewal cycle only, or immediate credit?
- **Customer's usage grows past their current tier's cap during grandfather.** — new pricing applies to incremental usage? Or full tier upgrade at old pricing until sunset?
- **Customer's contract auto-renewed under old pricing 2 weeks before the change ships.** — do they get grandfathered for their current term + sunset, or does the sunset date apply from the change's ship date regardless?
- **Customer downgrades a tier during grandfather.** — new pricing applies to the downgraded tier, or old pricing continues?
- **Customer wants to negotiate a permanent extension in exchange for a case study or reference.** — is this a category of exception you allow, and if so with what threshold (founder / VP-level approval; documented in the pack)?
- **Customer threatens to churn if not grandfathered.** — Chapter 5's specific anti-pattern (grandfathering as retention bribery). What's the response?

Every edge case has a stated policy, not "we'll figure it out." Case-by-case is what Chapter 5's grandfathering trap warns against.

**C2 — Chapter 5 grandfathering-anti-pattern teardown (15 min).** Chapter 5 names five specific grandfathering anti-patterns. For each, verify your Part A / B policy does not fire:

```
Anti-pattern                              | Does your policy fire? | Evidence
----------------------------------------- | ---------------------- | ---------
1. Case-by-case grandfathering            | Y/N + evidence
2. Forgotten grandfathered customers      | Y/N + evidence
3. Grandfathering as retention bribery    | Y/N + evidence  
4. No lock-in period offered              | Y/N + evidence
5. Silent grandfathering                  | Y/N + evidence
   (customer never told)                  |
```

For each `Y`, name the specific policy change required before ship.

For each `N`, cite the specific line of your Part A / B that rules the anti-pattern out — not "we thought about it."

## Starter guidance

- **The policy is picked before the change ships, not during the first renewal.** Chapter 5's cardinal grandfathering rule. If you're picking the policy at the first renewal, you've already lost — the first three customers set precedent that hardens into "case-by-case."
- **Sunset-window is the modal choice for a reason.** Chapter 5's practical experience: full-indefinite leaves ARR permanently on the table; no-grandfather triggers churn spikes; partial is complex. Sunset (12-24 months) balances trust preservation with ARR capture. Deviate only when your change has a specific reason to.
- **The email is written, not templated.** Every fill-in-the-blank template ships with the placeholder somewhere. Write the actual email for a real (or representative) customer. Personalise per customer at send time, but the base text is real.
- **The lock-in offer is what makes the grandfather trustworthy.** Chapter 5: existing customers should have the option to renew at their current price for one more term. Skipping this makes the sunset feel forced.
- **CRM tagging is the finance team's ability to answer "how many customers are on old pricing" a year from now.** Without the tags, the answer is "we don't know," which is a Chapter 5 forgotten-grandfathered-customers failure. Tags are cheap; forgotten cohorts are expensive.
- **Case-by-case grandfathering is the specific anti-pattern.** Every "just this one time" extension makes the next sales rep's decision harder. If you allow extensions, standardise the conditions (multi-year prepay, strategic account with $X ARR, named exception list); document in the pack.
- **The retention-bribery response is scripted.** Chapter 5's specific failure: customer threatens churn, sales rep offers grandfathering, cascade begins. Author the response now: "Grandfathering isn't a churn-retention tool; if the pricing doesn't work for you, let's find the right tier / feature fit instead." Then honour it in the moment.
- **Silent grandfathering is a trust event.** If you're grandfathering a customer, tell her explicitly ("your account is on pre-2026 pricing until {date}") — later discovery is worse than the news itself.
- **The finance reconciliation plan is what stops the grandfathered cohort from becoming a forever cohort.** A monthly report of "who's past sunset but not migrated" — even a spreadsheet at seed — is the difference between clean migration and forgotten customers.
- **The board framing matters at Series A and beyond.** A pricing change with a 12-month grandfather sunset has a 12-month ARR deferral; the board needs to understand this or they misread the first quarter as failure. One paragraph (A4) up front prevents the misread.
- **This exercise pairs with Exercise 05.** Exercise 05 designs the price experiment; this exercise handles what happens to existing customers when the experiment (or a pack revision) affects them. A pack revision usually needs both.
- **Do not use grandfathering to mask an unwelcome change.** If the new pricing is unwelcome enough that a 24-month grandfather is the only way to prevent revolt, the change itself is wrong — go back to Exercises 02 / 03 / 04 and revise.

## Acceptance criteria

Your submission is complete when:

- [ ] Part A1 names the specific pricing change, its direction and magnitude, whose bill changes and by how much, with a small worked example.
- [ ] Part A2 evaluates all 4 Chapter 5 grandfathering policies against the specific change with a fit assessment, 12-month ARR impact band, and specific-risk statement for each.
- [ ] Part A3 picks a specific policy with written justification including sunset window (if sunset), migration trigger, lock-in offer, early-migration rule, and usage-growth-during-grandfather rule.
- [ ] Part A4 includes the one-paragraph board / investor framing on ARR-impact deferral.
- [ ] Part B1 is a fully drafted existing-customer email (not a template) with what / when / what-you-can-do / contact / FAQ.
- [ ] Part B2 covers public / community communication (pricing-page banner, blog post or a decision not to publish, sales-team briefing script).
- [ ] Part B3 defines at least 3 CRM cohort tags with transition rules, reports that read them, and a default-flagged-for-review policy on missing tags.
- [ ] Part B4 specifies the sunset schedule, monthly reconciliation, revenue attribution, and quarterly de-grandfathered-cohort verification.
- [ ] Part C1 states a specific policy for at least 6 named edge cases including the retention-bribery scenario.
- [ ] Part C2 tests the policy against all 5 Chapter 5 grandfathering anti-patterns with fire status + evidence.
- [ ] Any anti-pattern that fires has a specific policy change to apply before the change ships.
- [ ] The whole policy fits on 2-3 pages (excluding the drafted email); compression is a discipline signal.

## Common ways this exercise goes wrong

- **The case-by-case trap.** Founder says "we'll grandfather the strategic accounts and case-by-case the rest." Fix: policy is a rule, not a menu. Standardise exception conditions; document in the pack.
- **The no-communication trap.** New pricing lands; existing customers discover it on the next invoice. Trust event. Fix: Part B1's email drafted before launch, sent on Day 1 of the change.
- **The no-lock-in trap.** Sunset window is 12 months but customers cannot lock in current pricing for one more term. Feels forced. Fix: Chapter 5's lock-in offer is standard; include it explicitly.
- **The forever-grandfather trap.** Policy is "customers keep old pricing forever, or until they upgrade." Two years later ARR from old-pricing base is materially below current; no one flags it because it's "just the way things are." Fix: sunset window with a hard date, tracked monthly.
- **The no-CRM-tagging trap.** No cohort tag on the customer record. Finance team cannot answer "who's on old pricing" a year later. Fix: B3's tagging scheme with default-flagged-for-review on missing tags.
- **The retention-bribery cascade.** First customer threatens churn; founder offers grandfathering; other customers hear; every renewal becomes a grandfathering negotiation. Fix: C1's retention-bribery response script.
- **The bespoke-per-customer-negotiation trap.** Every customer's migration is negotiated separately. Fifteen renewals in, no two customers have the same terms. Finance team spends 3 quarters reconciling. Fix: one policy, applied uniformly, with a small enumerated exception list (if any).
- **The silent-grandfathering trap.** Founder grandfathers some customers but doesn't tell them. Later they hear a peer got the new (lower) price. Trust event. Fix: every grandfathered customer is told explicitly + given the sunset date.
- **The public-communication-is-a-slack-message trap.** Change announced to the sales team on Slack; no pricing-page update; no blog post; no customer email. Discovery is chaotic. Fix: B2's public communication + B1's customer email are launched together on Day 1.
- **The finance-reconciliation-that-never-runs trap.** Sunset schedule exists as a spreadsheet nobody opens. Six months post-sunset, customers still on old pricing. Fix: B4's monthly reconciliation is on someone's calendar with an owner.
- **The extension-cascade trap.** First customer requests extension; founder grants case-by-case; word spreads; every customer requests extension; policy becomes de facto full-indefinite. Fix: extensions have standardised conditions with founder-level approval; repeat exceptions trigger a policy revision, not more exceptions.
- **The usage-grew-past-tier-during-grandfather ambiguity trap.** Customer on grandfathered $10/repo pricing grows from 50 to 150 repos during the grandfather period. Founder didn't decide the rule. Fix: C1's edge-case matrix names the rule (new pricing applies to incremental usage, or full tier upgrade — pick one).
- **The customer-facing-email-is-two-paragraphs trap.** Email is vague; customers cannot answer "so what changes for me?" from reading it. Fix: B1's email includes their specific bill change (or a way to see it), the specific date, and specific options.
- **The board-doesn't-know-about-the-deferral trap.** Q1 ARR post-change is flat because grandfathering deferred the impact; board reads flat ARR as "pricing change failed." Fix: A4's board framing communicates the deferral up front.
