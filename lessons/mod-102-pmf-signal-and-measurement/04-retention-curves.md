# Reading a Cohort Retention Curve

## Motivation

The single most reliable *behavioural* PMF signature is a **cohort retention curve that flattens** at a segment-appropriate level rather than decaying to zero. The Sean Ellis survey (Chapter 3) is a declarative snapshot; the retention curve is the behavioural record. When they agree, you have strong evidence. When they disagree, retention usually wins — declarative survey answers can be polite; usage is what people actually did.

This chapter teaches you to read a retention curve the way an early-stage GTM operator has to: cohort correctly, choose the right cadence (DAU / WAU / MAU), find the flattening or its absence, distinguish the "smiling" curve from the "frowning" curve, and treat a leaky curve as a **PMF failure** rather than a marketing failure.

## Core concepts

### The vocabulary — cohort, retention, curve

- **Cohort.** A set of users grouped by a shared start event, typically the week or month they first signed up or first activated. Cohorting is what separates a retention curve from an aggregate active-user chart; the aggregate hides all the leaks.
- **Retention.** The fraction of a cohort that is still active in a subsequent period, measured against a defined "active" event. If 1,000 users signed up in the week of 2026-08-03 and 220 of them were still active in the week of 2026-08-31, W4 retention for that cohort is 22%.
- **Retention curve.** A plot of cohort retention across periods — usually X = periods since signup, Y = % of cohort still active — with one line per cohort or one line for the pooled average.

The definitions of *active* and *period* are the load-bearing choices. Get them wrong and every curve you produce lies.

### DAU / WAU / MAU — pick the cadence that matches your usage pattern

The unit of active — daily, weekly, or monthly — has to match the product's natural usage cadence. Using the wrong cadence produces curves that look either falsely flat or falsely leaky.

- **DAU (daily active users).** Correct for products a user opens every workday or every day — chat, email, social, dashboards checked hourly. Retention read at D1 / D7 / D30. Slack, Superhuman, Instagram sit here. Reading MAU on a daily-cadence product will hide daily churn under a monthly average.
- **WAU (weekly active users).** Correct for tools a user touches a few times per week — code-review tools, project-management tools, sales CRMs, most B2B SaaS. Retention read at W1 / W4 / W12. Reading DAU on a weekly-cadence product will look catastrophically leaky because a user active on Mon/Wed/Fri looks "churned" on Tue/Thu.
- **MAU (monthly active users).** Correct for tools with genuine monthly cadence — invoicing, expense filing, quarterly-review software, tax tools. Retention read at M1 / M3 / M6 / M12. MAU on a weekly-cadence product hides all mid-month churn.

The rule of thumb from Reforge / Balfour ([Brian Balfour — "The Never Ending Road to Product/Market Fit"](https://brianbalfour.com/essays/product-market-fit); [Reforge writing on retention analytics](https://www.reforge.com/blog)) is: **pick the cadence that matches the median use case of your ICP, not the cadence that produces the prettiest chart.** The Amplitude and Mixpanel product docs on cohort analysis lay out the same tradeoff ([Amplitude — "The Amplitude Guide to Retention"](https://amplitude.com/blog/product-retention); [Mixpanel — Retention analysis docs](https://docs.mixpanel.com/docs/reports/retention)).

### Defining "active" — the second load-bearing choice

"Active" cannot mean "logged in." Logins are noise; the retention question is *did the user get value?* Define active as an **action** the product exists to enable — the one that, if it happened, means the user did the thing they came for.

Examples:

| Product | "Active" event |
|---|---|
| Slack | Sent at least one message |
| Superhuman | Sent at least one email |
| Loom | Recorded and shared at least one video |
| A code-review tool | Received or acted on at least one auto-nudge |
| A CRM for founder-led sales | Updated at least one opportunity stage |
| An invoicing tool | Sent at least one invoice |

Choosing an action that is too easy (opened the app) inflates retention; too hard (closed a deal) understates it. The right event is the **narrowest action that reliably corresponds to the user experiencing value**. This is often the same event you cohort by for "activation" (the user's first-time achievement of that action).

### Reading the curve — the flattening signature

Three curves cover 95% of what you see. Learn the shape.

**The "PMF" curve — flattens.** After an initial drop, the curve stops decaying and settles at a floor above zero. That floor is the fraction of the cohort that has hired the product for something recurring. The floor level is segment-dependent — 20% for a consumer app can be excellent, 60% for a mission-critical B2B tool can be weak — but the *shape* is the signal. Flattening is Andreessen's "customers buying just as fast as you can make it" made visible over time.

```
retention
1.0 |*
    | *
0.8 |  *
    |   *
0.6 |    *
    |     * *
0.4 |         * * *
    |               * * * *
0.2 |                       * * * * * * * *  <- floor holds
    |________________________________________
       W0  W1  W2  W3  W4  W6  W8  W12  W16
```

**The "no PMF" curve — decays to zero.** The curve trends toward zero and never stops. Every additional week loses some fraction of the remaining cohort. There is no floor; there is only the exit. This is the pure-curiosity or pure-marketing-driven signup pattern.

```
retention
1.0 |*
    | *
0.8 |  *
    |    *
0.6 |     *
    |       *
0.4 |         *
    |            *
0.2 |               *
    |                  * *
0.0 |                      * * * * * * * *
    |________________________________________
       W0  W1  W2  W3  W4  W6  W8  W12  W16
```

**The "smile" curve — flattens, then rises.** After an initial drop, the curve stabilises, then *increases* — cohort retention in month 12 is higher than in month 3. This is a hallmark of products where deeper usage compounds: the users who stayed are getting *more* engaged, or previously-inactive users are being resurrected by product improvements. Chamath Palihapitiya and the Facebook growth-team writing popularised this shape as a strong-PMF signature ([Andrew Chen — "The Cold Start Problem" and related essays on retention](https://andrewchen.com/); [Andrew Chen — "The Power User Curve"](https://andrewchen.com/power-user-curve/)).

Two additional shapes are worth naming:

- **The "frown" — decays after an initial flat.** The curve holds at a floor for a period, then starts eroding — perhaps a competitor shipped, perhaps the segment matured out of the pain, perhaps a change to your product broke value. This is PMF *loss*. Chapter 1's "PMF is a system state, not a milestone" is the theoretical claim; the frown is what the loss looks like in the data.
- **The "cliff" — a sudden drop at a fixed period.** The curve is fine until Wn, then falls off. Usually indicates a specific product-side event: the free-trial ends at N=14 days, a paywall activates, an email digest cadence produces churn. Diagnose the specific period and the specific event.

### Segments dominate — never trust the pooled curve alone

The single most-common analytical mistake at Chapter 4's level of rigour is reading the **pooled** cohort curve (all users, all cohorts, one line) and taking its shape as the state.

Two curves reliably lie:

- **Cross-cohort pooling.** Ten weekly cohorts pooled together will look flatter than any individual cohort actually is, because the surviving-forever users of the oldest cohort dominate the pooled tail. Always plot cohorts as separate lines.
- **Cross-segment pooling.** Enterprise users retaining at 60% and consumer freemium users retaining at 8% pooled together average out to a middling curve that describes neither reality. Segment first — the two lines tell two completely different stories.

The rule: **cohort by signup week AND segment by ICP tier.** If either operation produces a curve that changes shape versus the pool, do not trust the pool.

### The retention curve is the PMF ground truth

When the Sean Ellis survey and the retention curve disagree, the retention curve is usually right. Survey answers can be:

- Polite (people who used the product once said "somewhat disappointed" rather than "not disappointed" out of kindness).
- Aspirational (people who *want* to be the kind of person who uses the product answered as if they did).
- Sampled from a non-representative slice (Chapter 3 discussed this at length).

Usage is much harder to fake. A user who has opened the product every week for twelve weeks is delivering behavioural evidence that survives sampling and social-desirability effects.

That said: retention curves can lie in the other direction too — a product that only lives inside a workflow the user is *forced* to use (mandated by their employer, dependency on a bigger system) can show flat retention without pull. That is why the survey and the curve are cross-checks; not substitutes.

### Leaky curves are PMF failures, not marketing failures

The founder read of a leaky retention curve is often: *"our top of funnel is fine — we need to fix acquisition and retention will follow."* This is almost always wrong.

- If you 10× the top of the funnel through a leaky retention curve, you 10× the churn out the bottom. Your CAC rises (the marginal new user is worse than the average existing user), your LTV falls (churn cuts the lifetime), and the net effect of the marketing spend is negative.
- Retention is a *product-fit* problem. The users are leaving because the product does not deliver enough value at the point where they would come back. No amount of top-of-funnel spend fixes that.

The correct order: **fix the retention curve first (PMF), then scale acquisition.** This is Rachleff's value-hypothesis-before-growth-hypothesis rule from Chapter 1, expressed as an operating discipline against the retention chart.

### Benchmark ranges — with heavy caveats

Retention benchmarks are noisy — they depend on cadence, segment, definition of active, and industry. Use them as coarse orientation, not targets. The two publicly available reference points to know:

- **B2B SaaS monthly retention.** Widely-cited practitioner benchmarks put strong SaaS at **≥95% monthly logo retention** for mid-market and enterprise segments at scale; below 90% is usually a fit or product problem, not a customer-success problem. See OpenView and SaaStr's benchmark writeups for context (returned to in depth in mod-109 and mod-110).
- **Consumer / freemium retention.** The public research from Andrew Chen and others on consumer apps suggests the median D30 retention across mobile apps is in the mid-single-digits; strong consumer PMF sits at D30 ≥ 25% ([Andrew Chen — "New data shows losing 80% of mobile users is normal, and why the best apps do better"](https://andrewchen.com/new-data-shows-why-losing-80-of-your-mobile-users-is-normal-and-that-the-best-apps-do-much-better/)).

Read benchmarks as *shape orientation*, not verdicts. A product that looks weak on a benchmark can be strong in its niche; a product that looks strong on a benchmark can still be leaking in the segment you care about. The **flattening shape** of your own cohort curve is the strongest signal you have.

## Concrete example — the code-review-tool cohort read

Return to the running code-review-tool with 340 active teams and the Chapter 3 segment splits. The team pulls weekly cohorts from 2026-06-01 forward. "Active" is defined as *"the team acted on at least one auto-nudge or reassignment this week"*.

**Pooled curve — all teams, all cohorts:**

```
W0: 100%
W1: 68%
W2: 51%
W3: 40%
W4: 33%
W6: 27%
W8: 24%
W12: 22%
```

Read as-is: appears to flatten around 22–24%. Founder is tempted to call this a working PMF signature.

**Segmented — mid-market (50–200 eng, distributed):**

```
W0: 100%
W1: 88%
W2: 82%
W3: 78%
W4: 75%
W6: 72%
W8: 71%
W12: 70%
```

That is a **strong flattening at ~70%** — a segment-strong PMF signature for a WAU cadence B2B tool. The main-benefit statement is real; the retention confirms it.

**Segmented — small-teams (<20 eng):**

```
W0: 100%
W1: 45%
W2: 26%
W3: 14%
W4: 8%
W6: 4%
W8: 2%
W12: 1%
```

A **classic decay to zero** — no PMF, no floor. The pooled curve's "22% floor" is an artifact of the mid-market segment dragging the pool up while the small-teams segment approaches zero. The pool number was a lie.

**Segmented — enterprise (500+ eng, single-BU pilot):**

```
W0: 100%
W1: 92%
W2: 88%
W3: 75%
W4: 50%
W6: 35%
W8: 25%
W12: 18%
```

A curve that looks flat for the first three weeks (the pilot period during which champions push adoption) then decays sharply — the *pilot-with-no-post-pilot-value* signature. Route: revisit the enterprise-motion assumption (Chapter 6 "wrong product" for this segment; mod-107 for whether the motion itself matches ACV).

Three segments; three different curves; three different routes. The pooled curve made all three look like a mediocre average. This is why segmenting is non-negotiable.

## Common failure patterns

- **Reading the pooled curve.** Everything above is why. Segment first.
- **Wrong cadence.** WAU on a daily product hides intra-week churn; DAU on a weekly product shows fake decay. Match cadence to ICP usage pattern.
- **"Active" defined as login.** Logins are noise. Choose an action that means value received.
- **Reading absolute retention percentages against wrong benchmarks.** 20% D30 is bad for a Slack-cadence product and excellent for a consumer freemium mobile app. Segment- and cadence-adjusted comparison only.
- **Believing the recent-cohort curve when data is thin.** A cohort that started three weeks ago cannot tell you anything about W12 retention. Wait for the data or read from the older cohorts.
- **Ignoring the smile.** Some products' strongest PMF signature is a curve that *rises* after the initial floor. If you cut off the reporting window at W4, you never see it.
- **Blaming marketing when retention leaks.** The users you already acquired are churning out. More users at the top do not fix that; they magnify it.

## Summary

- **Cohort correctly** — by signup week and by ICP segment. Never read the pooled curve alone.
- **Match cadence to ICP usage** — DAU for daily products, WAU for a-few-times-a-week products, MAU for monthly workflows. Amplitude / Mixpanel docs cover the tradeoffs.
- **"Active" is an action, not a login.** Choose the narrowest action that reliably means value received.
- **The PMF signature is a flattening curve** at a segment-appropriate floor. Decay-to-zero is no PMF; the "smile" that rises after a floor is very strong PMF.
- **Retention is the ground truth** when it disagrees with the survey; usage is harder to fake than declaration.
- **A leaky retention curve is a PMF failure, not a marketing failure.** Fix the curve before scaling the funnel.
