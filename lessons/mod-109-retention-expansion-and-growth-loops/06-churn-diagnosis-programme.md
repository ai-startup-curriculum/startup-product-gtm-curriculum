# Churn Diagnosis — Voluntary vs. Involuntary

## Motivation

Founders treat churn as a single number — *"we churned 3% of accounts this month"* — and route it to a single owner ("customer success will handle it"). This is the operating equivalent of running one temperature gauge for a car engine. Different failures produce heat at different points; the diagnostic engine has to disaggregate.

Churn splits into two structurally different categories that require different remediations, different owners, and different metrics:

- **Voluntary churn** — the customer *chose* to leave. The product did not meet expectations, a competitor beat you, the buyer's budget changed, the champion left, the use case ended. Remediation is product, positioning, packaging, and CS motion work.
- **Involuntary churn** — the customer's *payment failed*. Card expired, card declined, invoice unpaid, bank rejected the ACH pull. The customer often did not choose to leave and does not know they left. Remediation is a **dunning programme**, card-update flows, and billing-system work.

The two are quantitatively meaningful. Practitioner writing (ProfitWell / Recurly / ChartMogul / Baremetrics) consistently reports that involuntary churn accounts for a large fraction of gross churn in subscription businesses — commonly cited ranges are 20–40% of total churn depending on payment mix, geography, and product ([ProfitWell / Paddle — churn writing](https://www.paddle.com/resources); [Recurly — payment recovery research](https://recurly.com/research/); [ChartMogul — churn analysis writing](https://chartmogul.com/blog/)). A team that improves involuntary-churn recovery by half — a fully-tractable engineering-and-billing-workflow project — can lift NRR by several percentage points without touching product or pricing.

<!-- needs-research: pin specific involuntary-churn-as-percentage-of-total-churn ranges to a current Recurly / ProfitWell / ChartMogul study; the numbers above are working practitioner ranges that shift by payment mix (credit card vs. ACH vs. invoicing), geography, and product. -->

This chapter names the two categories precisely, walks the sub-categorisation inside each, and describes the diagnosis programme that turns "we lost N accounts" into "we lost N accounts, decomposed by cause, with a remediation queue and a saved-vs.-lost analysis."

## Core concepts

### The voluntary / involuntary split — precise definitions

**Voluntary churn.** The customer took an intentional action to leave. Concrete forms:

- Explicit cancellation via the product's cancel flow.
- Non-renewal at the end of a contract term.
- Downgrade to a lower tier or fewer seats (a *partial* voluntary churn).
- Migration to a competitor.
- Business event: bankruptcy, acquisition, restructuring, project ending.

**Involuntary churn.** The customer's subscription lapsed for a payment or billing reason without their explicit choice to cancel. Concrete forms:

- Credit card expired and not updated.
- Card charge declined (insufficient funds, fraud rules, issuer decline).
- ACH / bank transfer failed.
- Invoice went unpaid past the grace period.
- Currency / geography change caused billing failure.
- Failed 3D-Secure / SCA authentication in card processing.

**The critical operational rule:** these two must be *separately tracked from day one* in the billing system. Every churned account has a category (voluntary or involuntary) and a sub-category (specific reason). If your billing system dumps both into the same "cancelled" bucket, you cannot run this chapter.

Modern billing systems (Stripe Billing, Chargebee, Recurly, Zuora, Paddle) all support this categorisation natively; the work is to make sure the field is populated and that the CRM roll-up preserves it.

### Voluntary churn — the sub-categorisation and remediation map

Voluntary churn decomposes into several sub-reasons, each of which routes to a different remediation:

| Sub-reason | Signal | Route |
|---|---|---|
| **Product mismatch** — user found the product did not solve the job | Exit-survey free-text mentions missing capability, poor fit, unexpected complexity | mod-101 discovery re-audit; product roadmap |
| **Competitor won** — user moved to a specific alternative | Exit-survey names a competitor; win-loss analysis | mod-103 positioning; mod-107 sales-motion |
| **Price / budget** — customer cannot or will not pay | Exit-survey mentions cost; downgrade pattern precedes cancel | mod-106 pricing; packaging tiering; discounting policy |
| **Champion left** — the buyer who signed the deal left the company | Exit-survey mentions role change; account activity drops before cancel | mod-104 buyer / champion mapping; multi-threading playbook |
| **Use case ended** — the project or workflow the product served is over | Exit-survey mentions "no longer needed"; usage drops in a specific surface | Segment-level PMF re-audit; ICP re-audit |
| **Onboarding failure** — user never activated (Chapter 5) | Cancel within first 30–60 days; magic-moment threshold never crossed | Chapter 5 activation programme; magic-moment re-diagnosis |
| **Consolidation** — customer moved to a competing bundle or platform | Exit-survey mentions specific bundle (Microsoft, Google, Salesforce); often paired with product-mismatch note | Positioning against the bundle; enterprise motion re-audit |

Two operational notes:

- Route by the **primary reason**, not the polite one on the exit form. A customer often says "budget" when the real reason is "the product isn't good enough to justify the budget." Look at the pre-cancel signals (usage decline, downgrade pattern) — they usually corroborate or contradict the stated reason.
- **Voluntary churn is where product and GTM meet.** Almost every voluntary-churn reason routes to a specific upstream module (101, 103, 104, 106, 107, 108). The routing map above is what makes churn a *diagnostic instrument* rather than a lagging KPI.

### Involuntary churn — a distinct workflow with its own playbook

Involuntary churn is fundamentally a **billing-workflow problem**, not a product problem, and the remediation is a specific set of engineering and operations investments called a **dunning programme**. A dunning programme is the ordered sequence of automated retries, notifications, and self-serve remediation flows that recover subscriptions after a payment failure.

Standard dunning programme components (built into all modern billing systems and documented in practitioner writing — [Stripe — payment recovery docs](https://stripe.com/docs); [Recurly research](https://recurly.com/research/); [ProfitWell / Paddle — churn recovery writing](https://www.paddle.com/resources)):

**1. Smart retry logic.** Automated re-attempts of failed charges on a schedule tuned to card-network behaviour. Retrying immediately after a decline usually fails again; retrying 3–5 days later at a different time of day, adjusted for the specific decline code, often succeeds. Modern billing systems (Stripe, Recurly, Chargebee) implement machine-learned retry timing; teams can tune the retry cadence to their payment mix.

**2. Card update flows.** In-product surface where the customer can update payment method. Should be reachable in <= 2 clicks from any product page — because a customer whose card expired and who has already forgotten about your product will not hunt for the billing page.

**3. Dunning notifications.** Email cadence to the billing contact (and, for high-value accounts, the champion or admin) at each retry, with a direct link to the card update flow. Escalation cadence: gentle at first retry, more direct at second, "your subscription will be cancelled in N days" at third.

**4. Pre-emptive card-update prompts.** For cards approaching expiration (60–30 days out), an in-product prompt or email suggesting an update *before* the failure occurs. This is the highest-ROI intervention because it never enters the retry cycle.

**5. Automatic card updater services.** Both Visa and Mastercard offer "account updater" services that push new card numbers to merchants when the underlying card is reissued (expired, lost, replaced). Enabling these in your billing system silently prevents a large fraction of card-expiry failures.

**6. Grace-period policy.** How many days after a payment failure does the subscription remain active while retries and dunning run? Common practice is 14–21 days. Too short and you churn recoverable customers; too long and you accumulate write-offs.

**7. Escalation to human touch for high-ACV accounts.** A payment failure on a $200/month subscription can run through fully automated dunning. A payment failure on a $20,000/month enterprise account gets a phone call from CS the same day; the mid-market band gets a personalised email from CS within 48 hours. Segment the dunning programme by ACV.

A team that ships a dunning programme with the seven components above typically recovers 40–70% of involuntary-churn revenue that would otherwise be lost — a well-documented practitioner range across ProfitWell / Recurly / ChartMogul writeups.

<!-- needs-research: pin the recovery-rate percentage for dunning programmes to the current Recurly / ProfitWell benchmark; recovery rate is highly sensitive to card-vs-invoice payment mix and geography, and the range cited above is a working practitioner range. -->

### Saved-vs.-lost analysis — the meta-metric for the churn programme

Once voluntary and involuntary churn are separately tracked and remediated, the programme needs its own scorecard. The core metric is **saved-vs.-lost analysis**:

- For every account that entered a churn-risk state (cancelled, failed payment, downgraded, health-score dropped below threshold, entered exit survey), was it ultimately saved or lost?
- Saved = subscription retained (either resumed after retry / dunning / save call, or upgraded back after downgrade).
- Lost = subscription terminated permanently.
- **Save rate** = saved / (saved + lost), computed per bucket.

The saved-vs.-lost analysis produces buckets that are the programme's operating dashboard:

| Bucket | Save mechanism | Save rate benchmark |
|---|---|---|
| **Involuntary — payment recovered via retry** | Smart retry logic + card updater | 20–40% of failed charges (varies) |
| **Involuntary — payment recovered via customer card update** | Dunning email → card update flow | 30–50% of dunning-cycle attempts |
| **Involuntary — payment recovered via CS phone call** | Manual outreach for high-ACV | 60–80% of touched accounts |
| **Voluntary — save call by CS** | Retention specialist calls at intent to cancel | 10–25% of touched accounts |
| **Voluntary — downgrade instead of cancel** | Retention flow offers a lower tier | Variable; depends on tier design |
| **Voluntary — win-back cadence** | Post-cancel email sequence 30 / 90 / 180 days later | Low single digits typically |

<!-- needs-research: benchmark save-rate ranges above are working practitioner numbers; pin against a current Recurly / ProfitWell / ChartMogul study. -->

**Segment by ACV.** A CS save call on a $200/month account is not economical; a save call on a $20k/month account is essential. The saved-vs.-lost analysis has to segment by ACV band so the programme knows where to invest human touch.

**Segment by voluntary sub-reason.** A "product mismatch" cancel is unlikely to be saved by a discount; a "price" cancel might be. Save-rate by sub-reason tells you which retention intervention actually works on which reason.

### Exit surveys with signal — the specification

Most exit surveys are useless. They are optional, they are long, they get filled in by a self-selecting minority, and the free-text answers are terse and polite. A useful exit survey has a specific structure:

- **In-flow, not post-cancel.** Ask *before* the cancellation completes, on the cancel-confirmation page, as part of the cancel flow. Post-cancel surveys have single-digit response rates; in-flow surveys clear 60–80%.
- **One required question, one open free-text.** The required question is a categorical drop-down of the sub-reasons from the voluntary-churn map above (with an "other" that opens a free-text). The open free-text is *"tell us more about why you're leaving — this goes directly to the founder."*
- **Founder signature.** Sign the exit-survey with a real founder's email address. Customers write more when they believe a human reads it.
- **Reply cadence.** For accounts above a threshold (e.g., ARR > $5k), the founder or the CS lead replies to the free-text within 48 hours. The reply is not a save attempt; it is a listening call. A meaningful fraction of these turn into save calls anyway, but the goal is to understand.
- **Weekly aggregation.** All exit-survey responses aggregated weekly, categorised by sub-reason, with any qualitative themes noted. The aggregated read is a standing item in the weekly GTM meeting.

The exit survey is the **primary customer-listening instrument for the churn programme**. mod-101's discovery discipline (Mom Test, ask about the past, ask about behaviour not opinion) applies to the founder's reply-cadence conversations — an exit survey is a discovery interview conducted at the moment the customer has the strongest reason to be honest.

### The churn programme as a monthly operating cadence

Concretely, a working churn programme runs on a monthly cadence with three roll-ups:

**1. Voluntary-churn read.** Every voluntary churn categorised by sub-reason. Sub-reason totals compared to trailing 3 and 6 months. Any sub-reason moving materially (say, 30% up or down) opens a diagnostic ticket routed to the relevant upstream module.

**2. Involuntary-churn read.** Every involuntary churn categorised by failure type (expired, declined, etc.). Recovery rate per stage of the dunning programme. Trend against trailing periods.

**3. Saved-vs.-lost roll-up.** Per bucket, save rate for the period. Compared against benchmark. Any bucket underperforming opens a diagnostic ticket routed to the relevant playbook owner.

The output of each monthly read is a **churn scorecard** (usually a subsection of the Chapter 7 retention + expansion scorecard) with the sub-reason breakdown, the dunning recovery rate, and one or two remediation actions in flight.

### Anti-patterns — where the churn number lies

- **Reporting a single churn rate.** Aggregate voluntary + involuntary as one number. Loses all diagnostic value.
- **Reporting "logo churn" only.** Small vs. large customer weighting invisible; the loss of one large enterprise account looks like the loss of one small SMB account.
- **Not instrumenting the categorisation in the billing system.** Every churn dropped into "cancelled" bucket. Cannot decompose.
- **Optional post-cancel exit survey.** Single-digit response rate; garbage data.
- **Exit-survey free-text nobody reads.** Signal thrown away.
- **No dunning programme.** Involuntary-churn recovery rate is 0%. The single highest-ROI churn intervention in most subscription businesses is left on the table.
- **Uniform dunning cadence across all ACVs.** Enterprise accounts get a robot email; SMB accounts get a phone call. Both are wrong.
- **CS comp'd only on renewals, not on saves.** Save motion under-invested.
- **Treating "downgrade" as save.** A downgrade is *partial* churn (downgrade ARR — Chapter 2). Save-vs.-lost analysis has to model downgrades as their own bucket.
- **"Win-back" campaigns to customers who churned six months ago.** Low return; risk of spam. Focus save-rate work on the in-flow moment.

## Concrete example — the code-review-tool churn programme

Return to the code-review-tool book from Chapters 1–3. The team is at Series-A, NRR = 110%, GRR = 78%. GRR of 78% is weak; the team runs the Chapter 6 diagnostic to figure out why.

**Total churn in Q1 2026.** 12 accounts, $340k ARR.

**Categorisation from the billing system + exit surveys:**

| Category | Sub-reason | Accounts | ARR |
|---|---|---|---|
| Involuntary | card expired, not updated | 4 | $56k |
| Involuntary | card declined (fraud rule) | 2 | $28k |
| Voluntary | competitor won (GitHub Copilot / Graphite) | 2 | $88k |
| Voluntary | champion left | 2 | $76k |
| Voluntary | price / budget | 1 | $42k |
| Voluntary | onboarding failure (cancel in first 45 days) | 1 | $50k |

**Read.**

- **Involuntary churn is 6 of 12 accounts (50%) and $84k / $340k ARR (25%).** Higher than expected because the team has no dunning programme — every card-expired failure went straight to cancel. Recovery rate: 0%. Fix: ship a dunning programme this quarter. Expected recovery: 40–60% of the $84k ($34–50k ARR recovered).
- **Voluntary — competitor won: 2 accounts, $88k.** The two losses were to Copilot's review features and Graphite's stacked-diff workflow. Route to mod-103 positioning re-audit and win-loss analysis; roadmap conversation about the stacked-diff gap.
- **Voluntary — champion left: 2 accounts, $76k.** Multi-threading failure — the accounts had one champion each and no second contact when the champion moved on. Route to mod-104 buyer / champion mapping; ship a multi-threading playbook in the CS onboarding.
- **Voluntary — price: 1 account, $42k.** Downgrade attempt was rejected. Route to mod-106 packaging conversation.
- **Voluntary — onboarding failure: 1 account, $50k.** Cancelled in first 45 days; never crossed the Chapter 5 magic-moment threshold. Route to Chapter 5 activation programme; investigate why the account did not activate.

**Programme in flight.**

- Dunning programme (retry logic + card update flow + email cadence + card updater services + CS phone call for accounts > $5k / mo). Owner: eng lead + head of CS. Ship date: end of Q2. Target: recover 50% of involuntary-churn ARR by Q3.
- Multi-threading playbook for CS onboarding (require a second contact in the account within 30 days of signup). Owner: head of CS. Ship date: end of Q2.
- Win-loss analysis on the two competitor losses (structured interviews with both customers). Owner: founder. Ship date: end of Q2. Feeds into mod-103 positioning re-audit.
- Chapter 5 activation programme re-diagnosis (why did the onboarding-failure account not activate). Owner: product lead. Ship date: end of Q2.

**Save-rate scorecard target for next quarter:**

| Bucket | Save-rate target |
|---|---|
| Involuntary — retry recovery | 30% (from 0%) |
| Involuntary — card update via email | 40% (from 0%) |
| Involuntary — CS phone call for accounts > $5k / mo | 65% (new) |
| Voluntary — save call (competitor mentioned) | 15% (new) |
| Voluntary — downgrade instead of cancel | offered on all cancel flows (new) |

That reads as a designed programme with owners, dates, and targets — not a "we should really do something about churn" placeholder.

## Common failure patterns

- **"Our churn is 3%."** Single number, no decomposition. Cannot act.
- **Involuntary churn treated as "the customer left."** No dunning programme; recovery rate 0%. Highest-ROI intervention left on the table.
- **Exit survey optional, post-cancel.** No signal.
- **No categorisation field in billing system.** Cannot decompose.
- **Uniform CS response across all ACV bands.** Enterprise churn goes uncalled; SMB churn gets over-invested touch.
- **Not routing voluntary sub-reasons to upstream modules.** Churn is a data point instead of a diagnostic.
- **Downgrade treated as save.** It is partial churn; separate bucket.
- **"Champion left" treated as unavoidable.** It is a multi-threading failure. Preventable at the mod-104 layer.
- **No save-rate scorecard.** Programme has no metric; investment is not measured.
- **Founder does not read exit-survey free-text.** Signal ignored; positioning drift and product-mismatch drift never surface.

## Summary

- **Churn splits into voluntary and involuntary.** They are structurally different and require different remediation. Track separately from day one in the billing system.
- **Voluntary churn decomposes into sub-reasons** — product mismatch, competitor won, price, champion left, use case ended, onboarding failure, consolidation. Each routes to a specific upstream module.
- **Involuntary churn is a billing-workflow problem** with a well-defined remediation: the **dunning programme** — smart retry, card update flow, dunning notifications, pre-emptive prompts, card updater services, grace-period policy, ACV-segmented human touch.
- **Saved-vs.-lost analysis** is the programme's scorecard — save rate per bucket, benchmarked and trended.
- **Exit surveys with signal** are in-flow, one required question + one free-text, signed by the founder, read weekly.
- **The programme runs on a monthly cadence** with a decomposed churn read and a saved-vs.-lost roll-up.
- **The most common failure mode is treating churn as a single number.** Decomposition is the whole point.
