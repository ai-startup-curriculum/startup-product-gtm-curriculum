# Designing a Product-Led-Growth Motion

## Motivation

Product-led growth (PLG) is not "we have a free trial" and it is not "we let users sign up on the website." PLG is a *motion design* in the same sense that inside sales is a motion design: it has stages, hand-offs, artifacts, and instrumentation, and each of those has to be built deliberately. The distinguishing property of PLG is that the *product itself* runs most of the funnel — acquisition, activation, upgrade, and often expansion happen inside the product, with humans (sales-assist, customer success) intervening only at specific triggered moments. A PLG motion without a defined **activation event**, without a rigorous **product-qualified-lead (PQL) definition**, without **in-product upgrade prompts** that fire at the right moment, and without a **sales-assist trigger** with a clear entry criterion is not a PLG motion — it is a self-serve website with hope attached.

The failure mode this chapter exists to catch: **the founder ships a free tier, watches sign-ups accumulate, watches the paid-conversion rate flat-line at 1-2%, concludes "PLG isn't working," and either bolts a heavyweight sales team onto the top of the funnel or gives up on the motion entirely.** In every case the actual root cause was that the motion was under-designed — no clear activation event, no PQL definition that a sales-assist rep could route on, no in-product upgrade prompt that surfaced at the moment of realised value, no expansion trigger that fired when the account crossed a headcount or usage line. The failure was not the motion; it was the fact that no motion was ever built.

This chapter builds the five load-bearing pieces of a PLG motion: **activation event**, **PQL definition**, **in-product upgrade prompts**, **sales-assist trigger**, and **expansion trigger**. The playbooks it draws from are Wes Bush's *Product-Led Growth* (2019) and the OpenView Partners PLG research (their annual PLG Index and benchmark reports). Neither the book nor the reports are decoration — they are the operating literature the modern PLG discipline runs on, and both are cited inline. The chapter also cross-references the retention and growth-loop work in mod-109 (which develops the *durability* half of PLG); this chapter is the *acquisition-through-upgrade* half.

## Core concepts

### What PLG is and is not

PLG's operating definition (Wes Bush, *Product-Led Growth*, 2019): a go-to-market strategy that **uses the product itself as the primary vehicle for acquisition, activation, conversion, and expansion**. The buyer discovers the product organically or through referral, signs up herself, experiences value inside the product, and upgrades to paid — with the sales conversation happening either in-product (an upgrade prompt at a paywall) or on a light-touch sales-assist call triggered by product behaviour.

Three things PLG explicitly is *not*:

- **PLG is not a free trial.** A 14-day free trial that ends in a "book a demo to continue" wall is *inside sales with a lead-magnet trial* — the sales conversation is still the primary conversion mechanism; the product is a demo aid. In a PLG motion the buyer can complete the purchase without ever talking to a human.
- **PLG is not "no sales team."** Mature PLG companies (Slack, Figma, Notion, Datadog, GitLab, Atlassian) all have sales teams; they just enter the funnel differently. Sales in a PLG motion is triggered by product signals, not by SDR outbound cold calls, and it operates on accounts that have already self-served to a demonstrated value moment.
- **PLG is not automatic revenue.** A PLG motion requires the same rigour of instrumentation, cohort measurement, and iteration that an SDR-AE motion requires. The instruments are different (activation funnels, cohort retention, feature adoption) but the discipline is not.

PLG's structural advantage — when it fits — is that acquisition cost per customer is close to zero (marginal customer arrives through the product, not through an SDR), which allows the motion to work at ACVs a human-touch motion cannot support. Its structural constraint is that the *product* has to be capable of running the funnel — a product where value is not experienced in the first session, or where activation requires configuration only a solutions engineer can do, cannot run a PLG motion no matter how nice the free-tier landing page looks.

### The five load-bearing pieces

A PLG motion is made of five parts. Every one is required; missing any of them produces the "flat 1-2% conversion" pattern from the motivation section.

1. **Activation event** — the specific in-product moment that indicates the user has experienced the product's core value for the first time.
2. **PQL definition** — the *account-level* signal that says the account has reached a state where a paid conversation is likely to convert.
3. **In-product upgrade prompts** — the specific in-product surfaces that convert an activated user or PQL-eligible account into a paid customer without human intervention.
4. **Sales-assist trigger** — the specific PQL signal that hands the account to a human sales-assist rep, and the criteria that define what the rep does when she arrives.
5. **Expansion trigger** — the specific in-product events that drive expansion revenue (seat additions, usage upgrades, feature-tier upgrades) after the account is paid.

The five pieces sit in a linear pipeline; each hands off to the next; each has a defined artifact.

```
    +-----------+     +-----------+     +---------------+     +-------------+     +----------+
    |acquisition| --> | ACTIVATION| --> |PRODUCT-QUALIFIED| -> |UPGRADE PROMPT| -> |EXPANSION |
    | (organic  |     |  event    |     |    LEAD (PQL)  |    |or SALES-ASSIST|    | trigger  |
    |  or paid) |     |           |     |                |    |               |    |          |
    +-----------+     +-----------+     +---------------+     +-------------+     +----------+
                          ^                    |                    |
                          |                    |                    v
                          |             (accounts route            paid state
                          |              to sales-assist            reached
                          |              or to product upgrade)     via product
                          |
                     mod-109 owns
                     the retention
                     half from here
```

The rest of this chapter develops each of the five.

### 1 — Activation event

**Definition.** The activation event is the *specific, instrumented, in-product moment* at which the user has experienced the product's core value for the first time. It is a single event — one action, one state change, one milestone — that separates users who "get it" from users who signed up and bounced.

**Examples from public writing:**

- Slack's often-cited activation heuristic — "a team sends 2,000 messages" — surfaces in company writing and press interviews from co-founder Stewart Butterfield around 2015-2017. <!-- needs-research: primary-source citation for the specific 2,000-messages threshold — locate the original Butterfield interview or Slack investor materials rather than relying on secondary quotation -->
- Facebook's early-2010s activation heuristic — "7 friends in 10 days" — is discussed in Chamath Palihapitiya's growth-team retrospectives. <!-- needs-research: primary-source citation for the specific "7 friends in 10 days" number — Chamath's own writing or a first-person source, not a secondary retelling -->
- Figma's activation is typically framed around "collaborated on a file with a second user" — the multi-player moment that distinguishes Figma from a single-player design tool. <!-- needs-research: primary-source citation for Figma's stated activation criterion — company blog, founder talks, or investor documents -->

These specific numbers are less important than the *pattern*: an activation event is a single, measurable, product-native moment that predicts retention. The founder's job is to find her product's equivalent.

**How to find the activation event for a specific product.** Bush's playbook (and Amplitude's growth playbook, and Reforge's Growth Series curriculum, and Casey Winters's writing on Greylock's blog) all converge on the same method:

1. **Cohort retained users vs. churned users** — take a cohort of sign-ups from N weeks ago; segment into retained (still active at week N) and churned (not active at week N).
2. **Find the in-product actions that discriminate the two cohorts** — actions where retained users hit the action at a much higher rate than churned users. Candidates: "invited a teammate," "created a project," "connected an integration," "reached 1,000 records," "shared a document."
3. **Test predictive power** — for each candidate action, check: what fraction of users who hit the action are retained at week N? A candidate action with 80%+ retention among users who hit it and <20% retention among users who don't is a strong activation-event candidate.
4. **Test the leading-indicator property** — the activation event has to happen *early* enough to be actionable. An activation event that fires at day 30 is post-hoc; an event that fires in day 1-3 is a lever the onboarding motion can pull. If the leading candidate doesn't fire early, look for a proxy action that predicts it.

The output is a single, defined event — "user created 2 projects and invited 1 teammate in the first 7 days" — with a defined operating name ("Activated") that the growth team, the product team, and the sales team all use identically.

**Instrumentation.** The activation event needs to be a *first-class metric*, tracked per cohort, exposed on a dashboard the founder looks at weekly. If activation is defined but not measured, the motion cannot be tuned — every onboarding change is guesswork rather than optimisation.

**Common activation-event failure modes:**

- **Activation defined too late.** "User has been active for 30 days" is not an activation event — it is a retention outcome. Activation has to be a *leading* indicator of retention, not a lagging one.
- **Activation defined by proxy.** "User signed up" or "user completed onboarding" is not activation — it is registration. Activation has to reflect *value experience*, which usually means an action that produces an output the user wants.
- **Activation not measured.** Team debates activation quarterly without ever plotting the activation rate per weekly cohort. Fix: put activation on the same dashboard as sign-ups and MRR; look at it every week.
- **Activation event doesn't discriminate cohorts.** The proposed event fires for 90% of sign-ups regardless of retention. Fix: the event is too easy; re-select something that separates retained from churned users.

### 2 — Product-qualified lead (PQL) definition

**Definition.** The PQL is the *account-level* signal that says the account has reached a state where a paid conversation — either automated via an upgrade prompt or human via sales-assist — is likely to convert. Where activation is *user-level* and *value-experience*-driven, the PQL is *account-level* and *purchase-likelihood*-driven.

**Why account-level, not user-level.** In a B2B PLG motion, individual users adopt the product but *accounts* buy it. A single retained user does not indicate a paying-account opportunity — she indicates a *paying user*, which may be a $12/month personal plan, not a $2,400/month team plan. A PQL is the signal that the *account* (a domain, a workspace, a company inferred from email domain and enrichment) has crossed into "we should try to convert this to paid."

**The PQL formula.** OpenView's PLG Playbook and Wes Bush's *Product-Led Growth* both frame the PQL as a *composite score* built from several signals. A working formula for a mid-market B2B PLG product looks like:

```
PQL = (activated users at account ≥ N)
      AND (usage indicator crossed threshold — projects, seats, API calls)
      AND (firmographic fit — company size, industry match ICP)
      AND (behavioural fit — activated user has admin / paying role)
```

Concretely: "the account has 3+ activated users, has created 5+ projects, has a company email domain matching an ICP-fit company of 50-500 employees, and one of the activated users has an admin or owner role."

That specific formula is a starting point, not a universal template. Every PLG product's PQL is tuned to that product's own retention data, its own ICP, and its own ACV structure. The formula's *shape* — an AND of several conditions across activation, usage, firmographics, and buyer role — is what generalises.

**Threshold tuning.** The thresholds (3 users, 5 projects, 50-500 employees, admin role) are hyperparameters. Bush's playbook suggests iterating them against actual close rates: pull the last 90 days of sign-ups, apply candidate thresholds retroactively, measure the close rate for each candidate threshold. A threshold that produces a 25%+ close rate on sales-assist calls is defensible; a threshold that produces 3-5% is too loose (too much sales time on unqualified accounts); a threshold that produces 60%+ is likely too tight (leaving conversion on the table).

**PQL routing.** The PQL is not itself a sale — it is a *routing decision*. Two paths:

- **PQL → in-product upgrade prompt.** For low-ACV PLG (< ~$5K ARR per account), the PQL fires an in-product prompt (contextual banner, upgrade CTA at a paywall, email nurture) with no human involved. The account converts through the product or does not.
- **PQL → sales-assist queue.** For mid-market PLG ($5K-$50K ARR per account), the PQL fires an alert to a sales-assist rep, who reaches out with a low-friction message ("we noticed your team has crossed X — would a 20-minute walkthrough of the team plan be useful?"). The sales-assist call has an explicit script tied to the PQL condition that fired.

Both paths need to be designed; running only the in-product prompt path caps conversion; running only the sales-assist path burns sales time on accounts that would have converted in-product without help.

**Common PQL-definition failure modes:**

- **PQL is user-level, not account-level.** Team routes every activated user to sales-assist. Sales-assist calls one user at a company that already has 20 users at the account, most of them unaware. Fix: aggregate to account before firing.
- **PQL threshold set by intuition.** Team picks "3 users" because it "feels right." Close rate is 4%. Fix: iterate thresholds against actual close-rate data.
- **PQL fires too late.** The PQL condition requires so many signals that by the time it fires the account has already exhausted the free tier and churned. Fix: PQL should fire while there is still runway on the free / low tier for the sales-assist conversation to land.
- **PQL fires too early.** The PQL condition is "user signed up with a company email." Sales-assist calls every sign-up; conversion is negligible. Fix: PQL requires actual product engagement, not just registration.

### 3 — In-product upgrade prompts

**Definition.** In-product upgrade prompts are the surfaces inside the product that convert an activated user or PQL-eligible account to paid, without human intervention.

**The four upgrade-prompt archetypes** (drawn from the OpenView PLG research and cross-referenced against public product surfaces from Notion, Figma, Linear, Superhuman, and Datadog):

- **Paywall prompt.** User hits a feature or usage limit gated by the paid tier — "you've used 3/3 free projects; upgrade to Team for unlimited." The prompt is contextual (surfaces at the moment of blocked action), specific (names the limit and the tier), and one-click (the upgrade path is a Stripe checkout, not a "contact us" form).
- **Value-realisation prompt.** User completes an action that demonstrates value (finished a report, invited teammates, connected an integration) and a contextual banner surfaces: "you're getting a lot out of the free tier — here's what Team adds." Value-realisation prompts fire at moments of *positive* affect, which convert better than paywall prompts at moments of *frustration*.
- **Social-proof prompt.** User's account has multiple co-workers on the free tier; a prompt suggests "your team has 4 users on individual plans — consolidate to Team for centralised billing and admin." Social-proof prompts work at the account-level rather than the user-level and often route the conversation to the admin / owner user rather than the discovering user.
- **Expansion prompt.** Existing paid user hits a limit or feature gate at a higher tier; prompt offers upgrade to a bigger plan. Expansion prompts belong to the expansion-trigger section below but share the upgrade-prompt shape.

**Design discipline for upgrade prompts** (Bush's chapter on "the upgrade prompt" and OpenView's "in-product growth" research converge here):

- **Fires at the moment of realised value or realised need**, not at time-based intervals ("you've been a user for 14 days — please upgrade"). Time-based prompts convert at 1-3%; contextual prompts convert at 10-25%.
- **Contextual specificity.** "Upgrade to Team" is generic. "You've hit the 3-project limit; upgrade to Team to unlock unlimited projects and start Project #4 right now" is specific and immediate.
- **Progressive disclosure.** First prompt is a low-friction banner; second is a modal; third is an email; fourth is a sales-assist reach-out. Do not lead with the modal; do not lead with the sales-assist call.
- **A/B test the prompt copy, position, and trigger.** Upgrade prompts are the highest-leverage A/B test surface in the product; a 2× improvement in prompt conversion doubles the whole motion's revenue with zero change to acquisition. Test regularly; document what worked and what didn't.
- **Instrumentation.** Every prompt has to log impression → click → convert. If the funnel is not instrumented per prompt, optimisation is blind.

**Common upgrade-prompt failure modes:**

- **All prompts are paywall prompts.** Every upgrade path is "you hit a limit; upgrade or leave." Product feels adversarial; conversion is capped. Fix: mix in value-realisation and social-proof prompts.
- **Prompts require a sales conversation to complete.** "Upgrade to Team" opens a "contact sales" form. Not PLG. Fix: upgrade path is one-click Stripe checkout for the self-serve tier; sales-assist is a separate, PQL-triggered path.
- **Prompts fire at time-based intervals.** "14 days into your account — please upgrade" fires regardless of engagement. Users who never activated are asked to pay; users who activated are asked at a random moment. Fix: prompts are triggered by product events, not calendar events.
- **No instrumentation.** Team ships prompts; nobody measures conversion per prompt. Team can't distinguish which prompt is carrying the motion. Fix: log every prompt's funnel.

### 4 — Sales-assist trigger

**Definition.** The sales-assist trigger is the specific PQL condition that hands the account to a human sales-assist rep, plus the specific playbook the rep runs when the account arrives.

**Why sales-assist exists in a PLG motion.** A pure self-serve motion caps ACV at what a user will put on a credit card without talking to anyone — typically $500-$5K per customer per year. Above that ACV, the buyer (usually a VP or director, not the individual user) wants a conversation before signing. Sales-assist is the mechanism that bridges the product-adopted user to the budget-owning buyer without breaking the PLG shape of the motion — the sales conversation *supports* the product-led purchase decision rather than *replacing* it.

**Sales-assist vs. inside sales.** The two look similar (both involve humans talking to prospects) but the entry criteria are different:

- **Sales-assist** enters the account *after* the account has self-served to a PQL state — usage exists, activated users exist, product value is demonstrated. The sales-assist rep's job is to bridge to the buyer, answer procurement questions, help the account choose the right tier, and remove friction from a purchase the account is already leaning toward.
- **Inside sales** (Chapter 3's SDR-AE motion) enters the account *before* self-serve, prospecting cold from a target-account list, running discovery and demo cycles for buyers who have not yet used the product.

Sales-assist reps close at 3-5× the rate of inside-sales reps against the same buyer, because they are working with an account that has already demonstrated intent — but they only exist because the PLG motion generated the intent-signal in the first place.

**Sales-assist trigger design:**

- **The trigger is a PQL condition** — the same PQL that routes to the in-product upgrade prompt, filtered by an ACV threshold. "PQL fires with 10+ activated users at an account matching a 500+-employee ICP" routes to sales-assist; "PQL fires with 3 activated users at a small startup" routes to in-product prompts.
- **The trigger has a defined SLA** — sales-assist reaches out within X hours of the PQL firing. Fast SLAs (2-4 hours) convert at 2× the rate of slow SLAs (24-48 hours), from the OpenView benchmark set.
- **The reach-out is templated but personalised** — the message references what the account has actually done in the product ("we noticed your team has connected 4 integrations and created 20 projects; would a 20-minute walkthrough of the Team tier be useful?"). This is not cold email; the personalisation is drawn from product signals.
- **The rep runs a light-touch playbook** — a 15-30 minute call, half of which is answering the account's questions (procurement, security, pricing), the other half of which is confirming the tier fit and closing the transaction. The full SPICED / MEDDIC discipline from mod-105 is over-invested for sales-assist calls; a lighter script (Situation, Fit, Next Step) is appropriate.
- **The hand-off from sales-assist to close is fast** — the account signs on the call or within 3-5 business days. A sales-assist call that turns into a 6-week enterprise cycle is a signal the account should have routed to the enterprise motion (Chapter 4) instead.

**Common sales-assist-trigger failure modes:**

- **Sales-assist reaches out to every sign-up.** Not a trigger — a firehose. Reps burn on unqualified accounts; PLG conversion collapses because the sales conversation replaces the product-led one. Fix: sales-assist reaches out only on PQL, and only on PQLs above the ACV threshold.
- **Sales-assist doesn't reach out at all.** PQLs fire and are ignored; accounts that would have converted with a 15-minute call are lost. Fix: sales-assist is a real role with a real SLA and a real quota.
- **Sales-assist reach-out is generic cold email.** Message says "hi, saw you signed up, want a demo?" — no reference to product usage. Fix: reference specific in-product signals; personalisation is the point.
- **Sales-assist tries to run full enterprise discovery on a $10K deal.** Reps run 60-minute discoveries with SPICED coverage on accounts that would have converted with a "sure, here's a 15-minute walkthrough." Fix: lighten the playbook for the sales-assist tier; the account has already demonstrated intent.

### 5 — Expansion trigger

**Definition.** Expansion triggers are the in-product events that drive expansion revenue after an account is paid — seat additions, tier upgrades, usage-tier upgrades, cross-product adoption.

**Why expansion belongs in the motion design.** For a PLG motion to work at mid-market ACV, the median customer's revenue has to grow over time — the account that lands at $2K/year and stays at $2K/year cannot amortise even a light sales-assist touch. Expansion (mod-109 develops this in depth) is what turns a low-ACV land into a mid-market or enterprise annualised revenue over 2-3 years. The expansion triggers designed here are the *product-side* half; the *sales-side* half (customer-success outreach, executive-business-review cadence) lives in mod-109.

**The four expansion-trigger archetypes:**

- **Seat expansion trigger.** Account crosses a seat threshold (10 users, 25 users, 50 users) that maps to a higher tier or higher per-seat price. Prompt surfaces to the admin at the crossing moment: "your team has grown to 25 seats — the Growth tier is priced to fit teams at your size."
- **Usage expansion trigger.** Account crosses a usage threshold (API calls, GB stored, workflow runs, records) that triggers overage billing or an upgrade path to a higher usage tier. Overage should be transparent (billing dashboard shows overage accruing) and the upgrade should be one-click.
- **Feature expansion trigger.** Account tries to use a feature gated by a higher tier (SSO, advanced audit logs, priority support, custom SLA). The gate is contextual and the upgrade path is offered inline.
- **Cross-product expansion trigger.** Account with product A crosses into a workflow where product B is complementary; product B's landing surface is offered in-product ("teams using [product A] often add [product B] for [reason] — try it free for your account").

**Expansion instrumentation.** Every expansion trigger has to log the same funnel as an acquisition prompt: impression → click → convert (or contact sales, if the expansion routes to a human path). Expansion revenue as a percentage of total revenue, and net revenue retention (NRR) — mod-109's core metric — are the outputs the expansion triggers move. If NRR is under 100%, the expansion triggers are under-designed regardless of what the acquisition funnel looks like.

**Common expansion-trigger failure modes:**

- **No expansion triggers.** Team focuses on acquisition; expansion revenue is 0%. NRR sits at 85-90% (paid customers churn as fast as expansion adds). Fix: instrument at least one seat expansion trigger and one usage / feature expansion trigger before scaling acquisition further.
- **Expansion triggers require a sales call to complete.** Every seat addition or tier upgrade opens a "contact sales" form. Not PLG. Fix: self-serve expansion path for common upgrades; sales-assist only for cross-tier expansions above the sales-assist ACV threshold.
- **Expansion triggers surface without warning.** Account gets hit with an overage bill at end of month with no in-product signal that overage was accruing. Buyer feels blindsided; churns at renewal. Fix: overage signals need to be visible in real time, not a monthly billing surprise.

### The playbooks — Wes Bush and OpenView

The two operating playbooks this chapter draws from:

- **Wes Bush — *Product-Led Growth* (2019).** The canonical modern text on PLG motion design. Bush frames PLG through the "Model → Strategy → Execution" (MSE) framework and develops each of the five pieces above at book length. Bush's ProductLed.com is his firm's ongoing operating site; the book is the primary source and the site publishes updated playbooks and benchmark data. <!-- needs-research: pin the specific ProductLed.com URLs cited in resources.md against publicly-linkable pages rather than paywalled content -->
- **OpenView Partners — PLG Index and Product-Led Growth research.** OpenView (Blake Bartlett and team) publishes an annual PLG Index and multiple longform reports on PLG benchmarks, PQL definitions, sales-assist economics, and expansion motion. OpenView's research is the primary benchmark source practitioners cite for PLG-motion KPIs (activation rates, PQL close rates, sales-assist SLAs, NRR by ACV band). <!-- needs-research: pin the specific OpenView PLG-Index URL for the current year; the report is published annually and the URL changes -->

Both playbooks converge on the five-piece structure this chapter uses. Neither is decoration; the module treats them as required reading before the exercises in this module are attempted seriously.

### Instrumentation stack

A PLG motion cannot be run without instrumentation. The working stack (per Bush, OpenView, Amplitude's growth playbook, and standard practice) is:

- **Product analytics** (Amplitude, Mixpanel, Heap, PostHog) — instruments the activation event, the PQL conditions, and the in-product prompt funnels at the event level. Cohort retention and feature-adoption views are built here.
- **CRM** (HubSpot, Salesforce, Attio) — holds account-level records; receives PQL events as records; routes to sales-assist.
- **Customer data platform** (Segment, RudderStack) — the source-of-truth event bus between product analytics and CRM.
- **In-product-prompt tool** (Pendo, Appcues, Chameleon, or in-house) — ships and A/B-tests upgrade prompts without a code deploy.
- **Billing** (Stripe, Chargebee, Metronome) — one-click self-serve upgrade path; overage handling; grandfathering.

At seed stage, the stack can start with a simpler subset (PostHog + HubSpot + Stripe + Chameleon is a common early combination), but every piece of the stack has to exist in some form; missing any of them opens a blind spot the motion cannot compensate for. The stack decision is a Chapter 5 topic — the CRM stage / qualification thread — but this chapter flags the instrumentation dependency because PLG motion design without instrumentation is a slide, not a motion.

## Concrete example — Loomly designs a PLG top-of-funnel

Loomly's motion decision from Chapter 1 was SDR-AE-primary with a PLG top-of-funnel layer. The PLG layer's job is not to close its own deals; it is to feed activated accounts into the SDR-AE motion at higher velocity and lower CAC than pure cold outbound. The five-piece design:

**1 — Activation event.** Loomly cohorts its first 500 free-tier sign-ups over 8 weeks; segments retained (still active at week 4) vs. churned. The action that most discriminates the two: *"connected a GitHub repo and had ≥3 dependency-graph scans completed within 7 days of sign-up."* Users who hit that event retained at 72%; users who did not retained at 11%. The activation event is named *"Scanned"* and instrumented in Amplitude.

**2 — PQL definition.** The account-level PQL formula, tuned against 90 days of sign-ups:

```
PQL = (activated users at account ≥ 2)
    AND (account has ≥ 5 repos connected)
    AND (email domain matches ICP — 50-500-employee B2B SaaS on GitHub)
    AND (at least one activated user has admin role in GitHub org)
```

The threshold "≥ 2 activated users" was picked over "≥ 3" because "≥ 3" reduced the PQL count by 40% but only improved close rate by 6% — too tight. The threshold "≥ 5 repos connected" was picked because accounts below 5 repos rarely converted to paid regardless of user count.

**3 — In-product upgrade prompts.** Three prompts in v1:

- **Paywall prompt.** Fires when account tries to connect a 4th repo on the 3-repo free plan. Modal: "you've hit the 3-repo limit. Upgrade to Team ($6/repo/month) to connect unlimited repos and add SSO." One-click Stripe upgrade.
- **Value-realisation prompt.** Fires when account's dependency-graph scan surfaces its first blocked-dependency alert. Banner: "your graph just caught a blocking issue. Team plan gives you Slack alerting so you don't have to check the dashboard." Click through to upgrade or dismiss.
- **Social-proof prompt.** Fires when account has 3+ activated users on individual free trials at the same email domain. Modal to the account admin: "4 people at Acme are using Loomly individually. Consolidate to the Team plan for centralised billing and admin."

All three prompts logged in Amplitude (impression → click → convert); A/B tested monthly.

**4 — Sales-assist trigger.** PQL fires + account's inferred ACV is > $8K (based on repo count × $6/repo/month) → alert to Jane (founder acting as sales-assist rep at seed; will become a dedicated sales-assist role when the motion scales). SLA: reach out within 4 hours during business hours. Message references specific product usage: *"Hi [name] — noticed your team at Acme has connected 12 repos and had 8 blocking-issue alerts fire this week. Would a 20-minute walkthrough of the Team plan be useful?"* Playbook on the call: 5 min introduction and usage recap, 10 min tier walkthrough and pricing, 5 min next step (close now or send a proposal). Not a full SPICED discovery — the account has already discovery'd itself through 6 weeks of product use.

**5 — Expansion trigger.** Two triggers in v1:

- **Seat/repo expansion.** Account crosses 20 repos on the $6/repo/month tier → suggest the $5/repo/month usage-tier discount, which requires a 40-repo commitment. Self-serve upgrade path in Stripe.
- **Feature expansion.** Account tries to enable SSO on the Team tier (not included) → prompt to upgrade to Enterprise tier ($12/repo/month, includes SSO + audit logs + priority support). Above the sales-assist ACV threshold → routes to Jane's sales-assist queue.

**Instrumentation stack.** PostHog (product analytics), Attio (CRM), Stripe (billing), Chameleon (in-product prompts), Segment (event bus). Total tooling budget: ~$800/month at seed scale.

**Interaction with the SDR-AE motion.** The PLG layer is subordinate. A PQL that fires above the sales-assist ACV threshold routes to sales-assist (Jane); a PQL from an account on the SDR-AE target list also alerts the SDR (who calls the VP Eng with the product-usage story as the opener); a PQL from an off-ICP account does not fire any human alert and is served only by in-product prompts. The two motions do not compete; the PLG layer is a signal-generator for the SDR-AE motion, and the SDR-AE motion closes the deals that the PLG layer alone cannot bridge to the VP-Eng buyer.

## Common failure patterns

- **"We have a free tier, so we do PLG" — the label-without-motion trap.** Team ships a free tier, does not define an activation event, does not build a PQL, does not instrument upgrade prompts, and reports the motion as "PLG." Six months later free-to-paid conversion is 1.5% and nobody knows why. Fix: build all five pieces; a free tier is a *pre-requisite* for PLG, not the motion itself.
- **Activation event defined by executive committee, not by cohort analysis.** Team debates the "aha moment" in a strategy off-site; picks whatever the CEO says feels right. Never checked against retention data. Fix: cohort analysis on real users; activation event is derived, not chosen.
- **PQL is user-level.** Every activated user gets a sales-assist reach-out; the same account gets 4 uncoordinated emails to 4 different users; the account's admin never gets called; conversion collapses. Fix: aggregate to account-level before firing PQL alerts.
- **Sales-assist runs enterprise discovery.** Rep books a 60-minute SPICED discovery on a $10K sales-assist deal that would have converted on a 15-minute walkthrough. The over-invested motion signals to the account that the tool is heavier than it appeared; the buyer becomes cautious; the deal slips. Fix: sales-assist has a light playbook (Situation, Fit, Next Step); full SPICED / MEDDIC is Chapter 3 / 4 territory.
- **In-product prompts converted to "contact sales" forms.** Team fears leaving revenue on the table; adds a "talk to sales" CTA to every upgrade path. Self-serve conversion drops because users who would have swiped a card are asked to schedule a meeting instead. Fix: self-serve upgrade is one-click for the tier and ACV range the sales-assist SLA does not cover.
- **Instrumentation missing.** Motion is built; nobody knows what the activation rate is by cohort, what the PQL-to-close rate is, what the prompt-conversion rate is per prompt. Optimisation is blind. Fix: activation, PQL, prompt-conversion, sales-assist SLA, sales-assist close rate, and NRR are all first-class dashboards from day one.
- **Expansion triggers deferred.** Team ships the acquisition motion, promises to "worry about expansion next quarter." NRR sits at 85%; the churn treadmill eats the acquisition. Fix: at least one expansion trigger has to ship alongside the acquisition motion.
- **Confused motion — PLG on top, enterprise underneath.** Free tier and self-serve upgrade at the front; every deal above $10K funnelled to a 6-week MEDDIC cycle regardless of PQL depth. The two motions confuse the sales team, the marketing team, and the customer. Fix: sales-assist tier and enterprise tier are two different motions with different playbooks, different reps, and different CRM stages; the account routes to one based on the PQL and the ACV threshold.
- **Copy-paste PQL formula from a public blog post.** Team adopts Notion's or Figma's PQL formula wholesale; the formula does not fit the product or the ICP; PQL fires with wrong precision and recall. Fix: PQL formula is *derived* from the product's own cohort data; other companies' formulas are inputs to the derivation, not templates to import.
- **Sales-assist SLA measured monthly.** Team reports "average sales-assist response time was 26 hours last month." The account that PQL'd 26 hours ago has moved on. Fix: measure per-account response time; hold the SLA at the account level, not the aggregate.

## Summary

- **PLG is a motion design**, not a label for "we have a free tier." It has five load-bearing pieces: activation event, PQL definition, in-product upgrade prompts, sales-assist trigger, expansion trigger. Missing any piece breaks the motion.
- **Activation event** — the *single, instrumented, in-product moment* that indicates the user has experienced core value. Derived from cohort analysis (retained vs. churned users), not chosen by intuition. Named, instrumented, dashboarded.
- **PQL** — the *account-level* signal that says the account is in a state where a paid conversation will convert. Composite of activated users, usage threshold, firmographic fit, and buyer-role signal. Thresholds tuned against actual close-rate data.
- **In-product upgrade prompts** — paywall, value-realisation, social-proof, expansion archetypes. Contextual, specific, one-click. A/B tested continuously; instrumented per prompt.
- **Sales-assist trigger** — PQL + ACV-threshold combination that routes accounts to a human sales-assist rep with a defined SLA (4 hours during business hours is the working benchmark) and a light-touch playbook. Different role and different playbook from inside sales (Chapter 3).
- **Expansion trigger** — seat, usage, feature, cross-product archetypes; drives NRR. Self-serve upgrade path for the common cases; sales-assist for the ACV-crossing cases. mod-109 develops the retention half.
- The playbooks: **Wes Bush** (*Product-Led Growth*, 2019, and ProductLed.com) and **OpenView Partners** (PLG Index and PLG research). Both converge on the five-piece structure; both are cited in resources.md.
- **Instrumentation stack** — product analytics + CRM + CDP + in-product-prompt tool + billing. Missing any piece opens a blind spot; PLG without instrumentation is a slide, not a motion.
- PLG is often a **layer** in a stacked motion — it feeds accounts to sales-assist or enterprise motions when the ACV crosses the threshold. The layering is deliberate; each layer has a defined entry and exit.
- The **failure modes** — "label without motion," "activation by committee," "user-level PQL," "sales-assist runs enterprise discovery," "in-product prompts turned into contact-sales forms" — are all diagnosable at the funnel-instrumentation level. If the instrumentation exists, the failure has a defined step it is happening at.
- Chapter 3 develops the **SDR-AE inside-sales motion** — the human-led motion that PLG feeds into for mid-market ACV; Chapter 4 develops the enterprise motion; Chapter 5 threads qualification through the CRM for whichever motion(s) the company runs.
