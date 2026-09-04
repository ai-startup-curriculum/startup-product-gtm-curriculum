# Exercise 02 — PLG Activation Event and PQL Authoring

**Estimated time:** 3 hours
**Chapter link:** [`02-plg-motion-design.md`](../02-plg-motion-design.md)
**Prerequisite:** Chapter 2 read end-to-end; a product with (or plausibly could ship) a free tier or self-serve entry point; access to at least a stub of product-analytics data (real events from Amplitude / PostHog / Mixpanel / your own event log preferred; a hand-authored plausible dataset acceptable for a first-pass drill — label as simulated). If your motion decision from Exercise 01 is *not* PLG-primary or PLG-layered, you may still run this exercise as a "what would the PLG top-of-funnel look like" thought experiment.

## Problem statement

Chapter 2 named PLG as a five-piece motion — activation event, PQL definition, in-product upgrade prompts, sales-assist trigger, expansion trigger — and named the failure mode: a founder ships a free tier, watches sign-ups accumulate, and calls it PLG without ever defining the load-bearing pieces. The chapter's central instruction: activation is *derived from cohort analysis*, not chosen; the PQL is *account-level*, not user-level; both are *instrumented* before they can be tuned.

This exercise trains you to **author the first two pieces** of the PLG motion — the activation event and the PQL definition — grounded in real (or simulated-and-labelled) cohort data. Upgrade prompts, sales-assist trigger, and expansion trigger are deferred to the module's lab (which assembles all five). Part C separately writes the instrumentation plan for both artifacts, because instrumentation is what turns a defined-on-paper motion into a running-in-production one.

The failure mode this exercise exists to catch: **the founder writes an activation event like "user signed up" or "user completed onboarding" (which are registration proxies, not value experiences), and writes a PQL like "user replied to sales email" (which is user-level and sales-assist-triggered, not product-signal-derived), and installs an in-product upgrade motion on top of both — producing a free-to-paid conversion rate of 1-2% and no diagnostic to explain it**.

## Requirements

Deliver a folder `exercise-02/` with three files:

- `part-a-activation-event.md` — the cohort analysis, the activation event derivation, the named event with instrumentation spec.
- `part-b-pql-definition.md` — the PQL formula, the threshold tuning, the routing decision.
- `part-c-instrumentation-plan.md` — the event schema, the dashboards, the review cadence.

### Part A — Derive the activation event from cohort data (75 min)

Deliver `part-a-activation-event.md`.

**A1 — Cohort definition (10 min).** Define the sign-up cohort you're analysing:

- **Time window** — e.g., "sign-ups from the last 8 weeks with at least 4 weeks of post-signup runway."
- **Cohort size** — the count of users in the cohort. If the count is < 100, note it and treat conclusions as directional; if < 30, the cohort is too small for defensible discrimination — either wait for more sign-ups or simulate additional users transparently.
- **Retention definition** — the specific state "still active" means. Chapter 2's default: "logged in at week 4 with at least one product event fired." Tune to your product but state the definition explicitly.

**A2 — Retained vs. churned split (15 min).** Segment the cohort into two buckets and report per-bucket counts. If simulating, label the simulation and describe the plausible retention distribution you're generating (Chapter 2's OpenView benchmark for early-stage B2B PLG is 15-30% retained at week 4; use this as a sanity band for simulated data).

**A3 — Candidate action list (10 min).** Enumerate 5-10 candidate in-product actions that could plausibly serve as the activation event:

- One-time actions (invited a teammate, created a project, connected an integration, imported a dataset).
- Repeated actions (crossed N of something, hit a threshold).
- Multi-step sequences (completed setup + invited teammate + created content).

Draw candidates from what your product actually does; do not pick actions that would require product work to instrument.

**A4 — Discrimination analysis (20 min).** For each candidate action, report:

- Fraction of retained users who hit the action within the first 7 days.
- Fraction of churned users who hit the action within the first 7 days.
- Discrimination ratio (retained fraction ÷ churned fraction). Higher is better; > 3 is a strong candidate.

Present as a table. If you have real data, cite the query or the analytics tool. If simulated, note it.

**A5 — Leading-indicator check (10 min).** For the top 2-3 candidates by discrimination ratio, check whether the action fires early enough to be actionable:

- Median time-to-first-hit among retained users. If > 14 days, the action is a lagging indicator; not useful for onboarding intervention.
- Fraction of retained users who hit the action in days 1-3. Should be > 50%; if not, the action fires too late.

**A6 — Named activation event (10 min).** Pick the single best candidate. Write a 4-6 line spec:

```
Event name: {Activated}
Trigger definition: {precise action or state that fires the event; enumerate all conditions}
Time window: {within X days of signup}
Cohort-analysis basis: {retained-vs-churned discrimination ratio + leading-indicator numbers from A4/A5}
Naming discipline: {this exact name is used across product, growth, sales, dashboards}
Anti-pattern check: {confirm it is not a registration proxy; confirm it is not a lagging retention outcome}
```

### Part B — Author the PQL definition (60 min)

Deliver `part-b-pql-definition.md`.

**B1 — Account aggregation (10 min).** Define how your PQL rolls user-level events up to account-level. Chapter 2's rule: PQL is account-level, not user-level. Author:

- **Account definition** — usually inferred from email domain + optional CRM-enrichment company match. Note edge cases (personal-email sign-ups, contractors, freemium abuse) and how you handle them.
- **Cross-user event aggregation** — how you count "activated users at account," "projects at account," "seats at account," etc.

**B2 — Composite PQL formula (15 min).** Author the PQL as an AND of 3-5 conditions per Chapter 2's shape:

```
PQL = (activated users at account ≥ N)
      AND (usage indicator crossed threshold T — projects / seats / API calls / whatever your product's usage metric is)
      AND (firmographic fit — company size / industry match ICP)
      AND (behavioural fit — activated user has admin / owner / paying role, or has invited others)
```

Each condition must have a specific threshold candidate and a stated rationale. Do not copy Chapter 2's Loomly numbers verbatim; the formula's *shape* generalises, the *thresholds* do not.

**B3 — Threshold tuning against close rate (15 min).** From historical (or simulated) sign-up → close data covering at least 60-90 days:

- Apply your candidate PQL formula retroactively to the historical cohort.
- Report the count of accounts that would have PQL'd, the count of those that closed, and the resulting close rate.
- Now vary each threshold (± 1 on the count-of-users, ± 20% on the usage threshold, tighter / looser firmographic filter) and re-report the close rate. Present as a small table.
- Pick the threshold set whose close rate lands in Chapter 2's healthy zone: > ~25% close rate on sales-assist calls means the PQL is defensibly tight; < 10% means it's too loose; > 60% means it's likely too tight and leaving conversion on the table.

If you don't have historical close data, run the same table against simulated conversion (say, "assume 5% baseline close rate on any account, 3× multiplier for each condition met") and label the simulation clearly.

**B4 — Routing decision (10 min).** Chapter 2's two PQL paths:

- **PQL → in-product upgrade prompt** — for accounts below the sales-assist ACV threshold. Automated; no human touch.
- **PQL → sales-assist queue** — for accounts above the sales-assist ACV threshold. Human touch with a defined SLA.

Author your threshold. What is the account's inferred ACV (from seat count × per-seat price, or usage estimate × per-usage price, or firmographic-band → tier)? Above what ACV does the PQL route to sales-assist versus staying in the in-product prompt path?

**B5 — PQL spec artifact (10 min).** Compress B1-B4 into a single reference spec:

```
# PQL Spec — {product} — {date}

## Account definition
{how accounts are inferred and aggregated}

## Formula
PQL = (condition 1) AND (condition 2) AND (condition 3) AND (condition 4)

## Thresholds
- {condition 1}: N ≥ ...
- {condition 2}: T ≥ ...
- {condition 3}: ...
- {condition 4}: ...

## Historical close rate
- {N accounts PQL'd, close rate X%, healthy-zone check}

## Routing
- ACV < ${threshold}: in-product upgrade prompt (Chapter 2 archetype: paywall / value-realisation / social-proof)
- ACV ≥ ${threshold}: sales-assist queue (SLA: X hours, playbook: light-touch)
```

### Part C — Instrumentation plan (45 min)

Deliver `part-c-instrumentation-plan.md`.

**C1 — Event schema (15 min).** For the activation event and the PQL, name the tracking events you need. Structure per event:

- Event name (in your product analytics tool's convention).
- Trigger location in code (front-end / back-end).
- Required properties (user ID, account ID, timestamp, event-specific context).
- Destination systems (product analytics → CRM via CDP; alerting; dashboards).

Every property has a type and a rationale.

**C2 — Dashboards (15 min).** Name the dashboards you will actually look at every week:

- **Activation-rate dashboard** — weekly cohort activation rate, plotted over the last 8-12 weeks with a rolling trend.
- **PQL-count dashboard** — weekly PQLs fired, by account inferred-ACV bucket.
- **PQL-conversion dashboard** — % of PQLs that converted to paid, by routing path (in-product prompt vs. sales-assist) and by rolling week.
- **Sales-assist SLA dashboard** — per-PQL response time; hold the median under 4 business hours per Chapter 2 benchmark.

Each dashboard names its data source, its refresh cadence, and the owner (usually the founder at seed; growth engineer / RevOps at Series A).

**C3 — Review cadence (10 min).** Name the operating rhythm — who looks at what on which day:

- Daily glance (founder / growth): activation-rate trend; PQL count.
- Weekly review (founder + sales-assist): PQL-conversion by path; SLA compliance; upgrade-prompt performance if instrumented.
- Monthly retro: activation-event discrimination re-checked (has the ratio drifted? has the leading-indicator property changed?); PQL threshold re-tuned against fresh close-rate data.

**C4 — Anti-decoration guardrails (5 min).** Name 3-5 things you will *not* claim from this instrumentation without further work — e.g., "this instrumentation doesn't tell me why users churn between signup and activation," "the PQL close rate isn't a causal estimate; it's a correlation," "the SLA dashboard measures response time, not conversion effect of fast response." Guarding against overclaim is what keeps the instrumentation diagnostic rather than theatrical.

## Starter guidance

- **Activation is a *leading* indicator of retention, not retention itself.** "Active at day 30" is retention. "Invited a teammate + created a project + first useful output in the first 7 days" is a leading indicator that predicts retention. If your candidate event fires only after retention is already observable, look for the earlier action that predicted it.
- **Registration proxies are not activation.** "User signed up," "user completed onboarding," "user verified email" are activities the user was going to do anyway. Activation has to involve the user experiencing the *product's core value* — the "aha moment" that separates users who understand the product from those who signed up out of curiosity.
- **The discrimination ratio is what matters.** An event that fires for 80% of users regardless of retention isn't discriminating anything. An event that fires for 70% of retained users and 15% of churned users has a discrimination ratio of ~4.7 — that's a strong candidate. Any candidate with a ratio below 2.5 is probably not the activation event.
- **PQL is account-level; enforce it in the aggregation step.** Users adopt; accounts buy. A PQL that fires per-user against a company with 20 individual free-tier users produces 20 uncoordinated sales-assist reach-outs, most of them to the wrong person. Aggregate to account before firing, always.
- **The firmographic condition in the PQL formula is what keeps the sales-assist queue clean.** Without it, the queue fills with free-tier startups that will never pay $10K-$50K/year; sales-assist time burns on the wrong accounts. Every PQL should require ICP-fit at the account level, not just any activated user at any company.
- **Threshold tuning is empirical, not aesthetic.** Chapter 2's Loomly Example uses ≥ 2 activated users because ≥ 3 dropped the PQL count by 40% but only improved close rate by 6%. That is the shape of the decision — pick the tightest threshold that keeps the close rate above your healthy floor, without dropping the volume below what your sales-assist capacity can serve.
- **Do not copy other companies' PQL formulas verbatim.** Notion's PQL, Figma's PQL, Slack's PQL are outputs of their specific product cohorts, their specific ICPs, and their specific ACV structures. Their *shape* generalises (an AND of 3-5 signals); their *thresholds* do not.
- **Instrumentation before optimisation.** Chapter 2's most-repeated anti-pattern is "we shipped the PLG motion but nobody measures the funnel." Every PQL, every activation event, every upgrade prompt, every sales-assist SLA — first-class dashboard from day 1. If it's not measured, it's not tunable.
- **The sales-assist ACV threshold is a business decision, not a formula.** Chapter 2's default: sales-assist starts at ~$5K ACV and continues to ~$50K ACV. Your specific threshold depends on the cost of a sales-assist call (~30-45 minutes of a $100K-OTE rep's time = ~$50-100 loaded cost per call), your close rate on that call, and the ACV upside. Model it explicitly rather than picking a round number.
- **The routing decision changes what the PQL *does*, not what it *is*.** A PQL below the sales-assist threshold triggers in-product prompts; a PQL above it triggers a sales-assist reach-out. Same PQL, different downstream action. Do not maintain two separate PQL definitions.

## Acceptance criteria

Your submission is complete when:

- [ ] Part A defines a specific sign-up cohort with time window, cohort size (with under-100 caveat if applicable), and retention definition.
- [ ] Part A enumerates 5-10 candidate actions and reports a discrimination-ratio table (retained-hit-rate / churned-hit-rate) for each.
- [ ] Part A runs a leading-indicator check on the top 2-3 candidates (median time-to-first-hit; fraction hit in days 1-3).
- [ ] Part A names a single activation event with a full spec (name, trigger definition, time window, cohort basis, anti-pattern check).
- [ ] Part B defines account aggregation rules (email-domain inference, cross-user event aggregation, edge-case handling).
- [ ] Part B authors a composite PQL formula as an AND of 3-5 conditions, each with a specific threshold and rationale.
- [ ] Part B runs a threshold-tuning table against historical (or simulated-and-labelled) sign-up→close data, showing the close rate at each threshold candidate.
- [ ] Part B names the sales-assist ACV threshold and describes the routing decision (in-product prompt vs. sales-assist queue).
- [ ] Part B ships a PQL spec artifact in the given structure.
- [ ] Part C names the event schema (event name + trigger + properties + destinations) for both the activation event and the PQL.
- [ ] Part C names the 4 dashboards (activation-rate / PQL-count / PQL-conversion / SLA) with data source, refresh cadence, and owner.
- [ ] Part C names the review cadence (daily / weekly / monthly) with owner per rhythm.
- [ ] Part C lists 3-5 anti-decoration guardrails — claims the instrumentation cannot support.
- [ ] Any simulated data is labelled `simulated` at the top of the file and the outputs treated as mechanics demonstrations rather than fielded findings.
- [ ] Any factual claim (a benchmark rate, a company's stated activation number) that is not from your own data or from Chapter 2's cited sources is flagged `<!-- needs-research: ... -->` rather than invented.

## Common ways this exercise goes wrong

- **Activation-is-registration trap.** Part A's activation event is "user signed up" or "user completed onboarding." Discrimination ratio is ~1 (both cohorts hit it). Fix: pick an event that only retained users hit — value-experience-based, not registration-based.
- **Cohort-too-small trap.** Part A runs discrimination against a 15-user cohort; ratios are noise. Fix: cohort ≥ 30 minimum; ≥ 100 for defensible discrimination; if not, wait or simulate transparently.
- **PQL-user-level trap.** Part B's PQL fires per individual activated user. Sales-assist reaches out to 4 different users at the same company uncoordinated. Fix: aggregate to account explicitly in B1; PQL condition sums across users at the same account.
- **PQL-formula-plucked trap.** Part B's PQL formula is picked from a blog post about Figma or Notion, not derived from your own product's data. Thresholds don't match your product's actual conversion pattern. Fix: run B3's threshold tuning against your own data (or simulated-and-labelled); pick thresholds that hit the healthy close-rate zone.
- **PQL-close-rate-outside-healthy-zone trap.** Part B's chosen thresholds produce a 5% close rate (too loose) or an 80% close rate (too tight). Fix: adjust thresholds and re-check; the tuning process is what B3 exists for.
- **Routing-collapse trap.** Part B routes every PQL to sales-assist, or every PQL to in-product prompts. Either the sales-assist queue burns on low-ACV accounts or high-ACV accounts get automated prompts with no human bridge. Fix: name the ACV threshold; PQLs above it go to sales-assist, below it to prompts.
- **Instrumentation-later trap.** Part C is skipped or hand-waved. Motion is defined on paper but not observable in production. Fix: Part C is required; without it the motion is a slide, per Chapter 2.
- **Dashboard-decoration trap.** Part C names dashboards but doesn't name the review cadence or owner. Dashboards exist but nobody looks at them. Fix: C3's cadence names who looks at what on which day.
- **No-guardrails trap.** Part C ships without the anti-decoration section. Founder over-claims from the instrumentation ("PQL close rate is 32%, so fast SLAs cause conversion" — no, that's correlational). Fix: force the guardrails list; name what the instrumentation cannot tell you.
- **Sales-assist-SLA-in-days trap.** Part C's SLA is "next business day" or "within 48 hours." Chapter 2's benchmark is 2-4 hours for 2× the conversion. Fix: SLA is stated in business hours, aggressively; if capacity does not exist, either narrow the PQL threshold to reduce volume or add capacity.
- **Simulated-data-passed-as-real trap.** Part A or B runs on simulated data without labelling it. Downstream reader treats the discrimination ratios or close rates as fielded findings. Fix: label simulation clearly at the top of the file and in every table caption.
- **Never-refresh trap.** Instrumentation runs but the monthly retro never happens; activation-event discrimination drifts over 6 months as the product changes and nobody notices. Fix: C3's monthly cadence explicitly re-checks the activation event against fresh cohort data.
