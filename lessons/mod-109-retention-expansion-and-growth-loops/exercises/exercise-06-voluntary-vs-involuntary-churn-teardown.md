# Exercise 06 — Voluntary vs. Involuntary Churn Teardown

**Estimated time:** 3 hours
**Chapter link:** [`06-churn-diagnosis-programme.md`](../06-churn-diagnosis-programme.md)
**Prerequisite reading:** [ProfitWell / Paddle — churn recovery and dunning writing](https://www.paddle.com/resources) (~30 min); [Recurly Research — payment recovery](https://recurly.com/research/) (~20 min); [ChartMogul — churn analysis writing](https://chartmogul.com/blog/) (search "involuntary" and "dunning"; ~20 min); [Stripe — payment recovery / smart retries docs](https://stripe.com/docs/billing/subscriptions/overview) (~20 min); [Baremetrics — dunning and cancellation flow writing](https://baremetrics.com/blog) (~15 min)

## Problem statement

Chapter 6 said churn is not one number — it is at least two (voluntary vs. involuntary) and inside each, a sub-categorisation that routes to a different remediation and often to a different upstream module. This exercise makes you *tear down* a provided churn book, produce the sub-decomposition, and author both a dunning programme (for the involuntary side) and a save-vs.-lost scorecard (for the whole programme).

You will:

1. Tear down a provided quarterly churn book that has been reported as a single number, decompose it by voluntary / involuntary, sub-categorise inside each, and route each sub-reason to the right upstream module or programme.
2. Author a dunning programme with the seven Chapter 6 components, scoped by ACV band.
3. Design a save-vs.-lost scorecard with save-rate targets per bucket.
4. Repeat the same for a real (or realistic hypothetical) startup of your own, in the shape of scorecard section 7.

The exercise trains the diagnostic discipline that turns "we churned 3%" into a monthly-cadence programme with owners, targets, and specific remediation in flight.

## Requirements

Deliver a folder `exercise-06/` with:

- `part-a-provided-book-teardown.md` — the teardown of the provided churn book.
- `part-b-dunning-programme.md` — the dunning programme with seven Chapter 6 components.
- `part-c-save-vs-lost-scorecard.md` — the save-vs.-lost scorecard with targets per bucket.
- `part-d-your-startup.md` — the churn programme for a chosen startup, in scorecard-section-7 shape.

### Part A — Tear down a provided churn book (60 min)

**"Meridian Data"** — a synthetic mid-market analytics platform. The founder's Q2 2026 board update contains one line about churn:

> "Q2 churn: 4.2% of accounts. Slightly elevated vs. Q1 (3.6%). CS team is on it."

The underlying detail (which the founder has not decomposed) is below. 18 accounts churned in Q2, representing $612k ARR.

| # | Account | Q2 ARR | Cancellation trigger | Notes |
|---|---|---|---|---|
| 1 | Aster Corp | $48k | Card expired; 3 automated retries all failed; account went to "cancelled — non-payment" after 21-day grace period. | Champion still active in product a week before payment failure. |
| 2 | Boreal Ltd | $30k | Explicit cancel via product UI. Exit-survey free-text: "Moved to Metabase — cheaper and good enough for our stage." | On base tier; 8 seats. |
| 3 | Cirrus AG | $120k | Non-renewal at end of annual contract. Renewal conversation attempted twice by CSM; primary contact left the company in Q1, no second contact was multi-threaded. | Original champion was VP Data; new VP arrived Q2 and standardised on Looker. |
| 4 | Delphi LLC | $22k | Card declined (fraud rule). No dunning email fired due to a missing SendGrid integration bug — the customer received no notice. Reached out to support 6 weeks later; account had been cancelled. | High-usage account until the failure. |
| 5 | Eos Inc | $88k | Explicit cancel. Exit-survey: "The product does what we hoped, but the price for the seats we need is too much. Would stay at half the price." | 24 seats; asked for a downgrade first, was told no lower tier existed. |
| 6 | Ferro Corp | $54k | Non-renewal. Exit-survey: "We never really got it running the way we wanted. Onboarding was hard; we used it for one dashboard and let the trial expire into the annual." | Signup 380 days ago; had two active users out of 12 seats. |
| 7 | Gemini SA | $42k | Bank ACH transfer failed (insufficient funds); customer never responded to dunning emails; cancelled at grace period end. | EU customer; account had been active for 2 years. |
| 8 | Helio Group | $18k | Explicit cancel. Exit-survey blank. Support ticket 30 days prior mentioned "connecting to Snowflake keeps timing out." | Never used the product after initial setup. |
| 9 | Ilex Co | $36k | Explicit cancel. Exit-survey free-text: "Consolidating on Salesforce Data Cloud as part of the enterprise Salesforce contract." | Cancelled 90 days into a co-terms with Salesforce buy. |
| 10 | Juno Ltd | $24k | Card expired. Auto-updater not enabled in billing; would have caught the reissued card. Retries failed; cancelled. | Active until failure. |
| 11 | Kelp Corp | $16k | Explicit cancel. Exit-survey: "The project we bought this for wrapped up in Q1." | Single-project use case; no expansion attempted. |
| 12 | Lyra Inc | $60k | Non-renewal. Exit-survey: "Champion (Head of Data) left in April; new Head of Data prefers a different tool from her previous company." | No second contact in the account. |
| 13 | Mira AG | $24k | Card expired; retry succeeded on day 5 after email prompt. **Saved.** Do not count against churn. | Included in the founder's "18 churned" list in error. |
| 14 | Nyx LLC | $12k | Explicit cancel. Exit-survey: "We're a small team; the tool has features we don't need. Also expensive for us." | 3 seats; on the mid-market tier which is priced for 10+. |
| 15 | Onyx SA | $30k | Card declined (issuer decline). CS phoned within 24 hours; card updated on the call. **Saved.** | Included in the founder's list in error. |
| 16 | Pyra Corp | $9k | Explicit cancel. Exit-survey: "Product does its job. We just don't have budget to renew — company-wide freeze." | Small account. |
| 17 | Quon Ltd | $75k | Downgraded from Pro ($75k/yr) to Standard ($45k/yr) in Q2. Founder reported the full $75k as "churned"; the correct movement is $30k downgrade, not $75k churn. | Account still active. |
| 18 | Rho Inc | $16k | Explicit cancel. Exit-survey: "Cancelled the trial after 45 days; never activated. Onboarding videos didn't help; we didn't find the value." | Never crossed a plausible activation threshold. |

Deliver `part-a-provided-book-teardown.md` with:

1. **Corrected churn total.** Removing the two saved accounts (Mira, Onyx) and correcting the Quon downgrade-vs-churn misclassification. State the corrected number of churned accounts and the corrected churned ARR.
2. **Voluntary vs. involuntary split.** Per the corrected list, split each account. State counts and ARR for each side.
3. **Sub-categorisation table.** Every account assigned to a Chapter 6 sub-reason (product mismatch, competitor won, price / budget, champion left, use case ended, onboarding failure, consolidation, or one of the involuntary types).
4. **Routing table.** Each sub-reason routed to the responsible upstream module or programme (mod-101 discovery re-audit, mod-103 positioning, mod-104 champion mapping / multi-threading, mod-106 packaging, mod-107 sales motion, Chapter 5 activation programme, Chapter 6 dunning programme, etc.).
5. **The one-paragraph read.** In the voice of Chapter 6's monthly-cadence read: *what does this quarter's decomposed churn actually say about the state of the business?*
6. **The founder's misreports.** Enumerate every specific misreport in the founder's Q2 board line (two saved accounts counted as churn; one downgrade booked as churn; involuntary-vs-voluntary conflated; no sub-reason decomposition). Chapter 6's metric-integrity discipline.

### Part B — Author the dunning programme (45 min)

Deliver `part-b-dunning-programme.md` scoped to Meridian's book with the seven Chapter 6 components:

1. **Smart retry logic.** Retry cadence tuned to card-network behaviour. Distinct treatment for hard vs. soft declines. Name the billing-system feature (Stripe Smart Retries / Recurly ML retries / Chargebee dunning) or the equivalent custom logic.
2. **Card update flow.** In-product surface reachable in ≤ 2 clicks; email link deep-linked to the update flow.
3. **Dunning notification cadence.** Email sequence at each retry with escalation. Templates in the appendix (short — 3 sample subject lines + one full email body is enough).
4. **Pre-emptive card-update prompts.** Trigger at 60 and 30 days pre-expiry.
5. **Automatic card updater services.** Enable Visa Account Updater and Mastercard Automatic Billing Updater in the billing system.
6. **Grace-period policy.** Choose a period (typical 14–21 days) with rationale.
7. **ACV-segmented human touch.** Enterprise (> $10k/mo) gets a CS phone call within 24 hours; mid-market ($1–10k/mo) gets a personalised email within 48 hours; SMB (< $1k/mo) runs fully automated.

Include:

- **Owner** — engineering lead + head of CS + billing-ops.
- **Ship date** — a specific target.
- **Expected recovery target** — based on the Meridian Q2 involuntary-churn ARR, what dollar amount would you expect to recover in a full quarter with the programme in place. State the practitioner-benchmark range you're pinning the estimate to.

<!-- needs-research: the specific dunning-recovery percentage benchmarks vary by payment mix (card vs. ACH), geography, and product. Cite the current Recurly / ProfitWell / ChartMogul range applicable to Meridian's profile (US-based mid-market card-primary payment mix). -->

### Part C — Save-vs.-lost scorecard (30 min)

Deliver `part-c-save-vs-lost-scorecard.md` with a save-rate scorecard for Meridian's programme going forward. Chapter 6's six-bucket table is the template:

| Bucket | Save mechanism | Current save rate | Target save rate | Rationale for target |
|---|---|---|---|---|
| Involuntary — retry recovery | Smart retry + card updater | | | |
| Involuntary — card update via email | Dunning email → in-product update flow | | | |
| Involuntary — CS phone call (> $10k/mo) | Manual outreach for high-ACV | | | |
| Voluntary — save call (retention specialist) | Human touch on intent-to-cancel | | | |
| Voluntary — downgrade instead of cancel | Retention flow offers a lower tier | | | |
| Voluntary — win-back (30 / 90 / 180 days post-cancel) | Post-cancel email cadence | | | |

Include:

1. Populated table with baseline (from Meridian's Q2 data — mostly 0% for buckets where the programme does not yet exist) and target (informed by Chapter 6 practitioner ranges).
2. **Owner per bucket.**
3. **A note on the "voluntary — downgrade instead of cancel" bucket** — Meridian's Nyx and Eos cases both explicitly asked for a lower tier; the absence of a tier is a mod-106 packaging problem. Route accordingly.
4. **Exit-survey redesign.** Chapter 6's spec — in-flow, one required categorical + one free-text, founder-signed, weekly aggregation, founder replies within 48h on accounts > $5k ARR.

### Part D — Your startup's churn programme (30 min)

Pick a startup — yours, one you know well, or a variant of Meridian.

Deliver `part-d-your-startup.md` in the shape of scorecard section 7:

1. **Corrected quarterly churn.** Voluntary vs. involuntary split, sub-categorisation, ARR-weighted.
2. **Routing.** Every sub-reason routed to the responsible upstream module or programme.
3. **Dunning programme.** In place / gap. If gap, ship date and owner.
4. **Save-vs.-lost scorecard.** Bucketed with baseline and target.
5. **Exit-survey design.** In-flow structure, founder signature, reply-cadence policy.
6. **Monthly cadence.** State the specific monthly-review meeting where the decomposed churn read is discussed and who owns it.

Length: 1–2 pages. Do not exceed 2.

### Part E — Reflection (15 min)

A short closing paragraph:

- Of the 18 accounts in Part A, which one was the most avoidable — meaning the specific Chapter 6 remediation (dunning, multi-threading, activation programme, packaging) would most cleanly have prevented the loss?
- For your Part D startup, what is the single billing-system instrumentation gap that most prevents the voluntary / involuntary split from being computable today?
- If you had one quarter of engineering + CS time to invest against churn, would you put it into the dunning programme, the save-call motion, the multi-threading playbook, or the activation programme — and why (based on your Part D decomposition)?

## Starter guidance

- Chapter 6's Table on voluntary sub-reasons is the routing key. Every sub-reason has an upstream owner; use the mapping literally.
- In Part A, remove the saved accounts (Mira, Onyx) before computing the corrected total — they should never have been in the "churned" list. Chapter 6's metric-integrity discipline.
- The Quon downgrade is the classic *downgrade-booked-as-full-churn* mistake from Chapter 2. Correct movement is $30k downgrade, not $75k churn.
- Delphi is the highest-value teachable moment on the involuntary side — the customer never received a dunning email due to an integration bug. This is a *programme-instrumentation failure*, not a customer failure. The whole account was recoverable.
- Cirrus and Lyra are both champion-left failures. Multi-threading playbook (Chapter 6 sub-reason routing → mod-104) prevents this; the account has one contact and no second-thread, so a role change kills the renewal.
- Ferro, Rho, and Helio are activation failures (never really used the product). Route to Chapter 5 activation programme re-diagnosis.
- Nyx and Eos are packaging failures — both explicitly asked for a lower tier that did not exist. Route to mod-106; consider adding a downgrade-instead-of-cancel option in the save flow (Chapter 6's separate bucket).
- Ilex is a consolidation loss to Salesforce Data Cloud. Chapter 6's consolidation sub-reason routes to positioning against the bundle (mod-103).
- Boreal is competitor won (Metabase). Route to mod-103 positioning + win-loss analysis.
- Kelp and Pyra are use-case-ended and budget-freeze losses — often unavoidable, but worth noting in the exit-survey aggregation so the segment mix is tracked.
- Do not over-invest human touch on small accounts. Chapter 6's ACV-segmented dunning rule — a $200/mo SMB failure runs fully automated; a $10k/mo enterprise failure gets a phone call.
- For Part D, if your billing system does not populate a categorisation field on cancellations, the split is not computable — name that as the load-bearing instrumentation gap.

## Acceptance criteria

Your submission is complete when:

- [ ] Part A removes the two saved accounts (Mira, Onyx) from the churn total and corrects the Quon downgrade-vs-churn misclassification.
- [ ] Part A splits every corrected-list account into voluntary or involuntary with a Chapter 6 sub-reason.
- [ ] Part A routes every sub-reason to the responsible upstream module or programme.
- [ ] Part A enumerates the founder's Q2 board-line misreports (saved-as-churned, downgrade-as-churn, voluntary-vs-involuntary conflation, no decomposition).
- [ ] Part B specifies all seven Chapter 6 dunning components with owner, ship date, and expected recovery target (with practitioner-benchmark citation for the recovery range).
- [ ] Part B's ACV-segmented human touch specifies a distinct treatment for enterprise / mid-market / SMB.
- [ ] Part C's save-vs.-lost scorecard has baseline and target for each of the six buckets, with per-bucket owner.
- [ ] Part C addresses the missing "downgrade instead of cancel" tier as a mod-106 packaging routing.
- [ ] Part C's exit-survey design is in-flow (not post-cancel), founder-signed, with the 48-hour reply cadence on accounts > $5k.
- [ ] Part D provides a corrected quarterly churn split, routing table, dunning-programme status, save-vs.-lost scorecard, exit-survey design, and monthly-cadence owner.
- [ ] Part E reflection names the most-avoidable account (likely Delphi or one of the champion-left / activation-failure accounts), a billing-system instrumentation gap, and a defended one-quarter investment priority.

## Common ways this exercise goes wrong

- **Reporting the founder's number as-is.** Chapter 6's entire discipline is decomposition. If you did not correct the saved-as-churned and downgrade-as-churn errors, you missed the point.
- **Voluntary / involuntary not separated.** The two halves have different remediations. Aggregating them destroys the diagnostic.
- **All voluntary sub-reasons collapsed into "customer left."** No routing possible; no programme actionable.
- **No dunning programme even proposed.** The single highest-ROI intervention on the involuntary side. Chapter 6's core.
- **Uniform ACV treatment in dunning.** Enterprise phone-call for $200 SMB accounts is uneconomical; automated email for $20k enterprise accounts is negligent.
- **Save-vs.-lost scorecard as a single number.** Bucket it per Chapter 6's table.
- **Downgrade treated as save.** Partial churn per Chapter 2; separate bucket per Chapter 6.
- **Exit survey optional, post-cancel.** Single-digit response rate; no signal.
- **Champion-left treated as unavoidable.** Multi-threading (mod-104) prevents it.
- **Onboarding-failure churn (Ferro / Rho / Helio) treated as separate from the Chapter 5 activation programme.** They are the same problem; the activation programme is the remediation.
- **No monthly cadence in Part D.** Programme without a review meeting is not a programme.
- **Ignoring the packaging routing on Nyx / Eos.** Both explicitly asked for a tier that did not exist. This is a mod-106 packaging failure, not a CS failure.
