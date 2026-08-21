# Growth Loops vs. the AARRR Funnel

## Motivation

For a decade the default mental model for startup growth was the AARRR "pirate metrics" funnel — **Acquisition, Activation, Retention, Referral, Revenue** — popularised by Dave McClure at 500 Startups ([Dave McClure — "Startup Metrics for Pirates"](https://500hats.typepad.com/500blogs/2007/09/startup-metrics.html), 2007). The funnel is still useful for a specific job: describing the sequence a *single user* traverses from first exposure to paying customer.

The failure mode is when founders and growth teams use it as a **growth model** — a mental picture of how the business grows over time. As a growth model, the funnel is wrong in a specific and expensive way: it treats each stage as an *independent* set of levers, so the operating discipline becomes "top-load the funnel with more acquisition and optimise each stage's conversion rate." That mental model gives you a linear machine where every unit of growth requires a proportional unit of paid acquisition input. It cannot produce compounding, and it treats retention as a downstream conversion rate rather than as the mechanism that produces the next unit of acquisition.

**Growth loops** — codified by Brian Balfour and the Reforge team ([Reforge — "Growth Loops are the New Funnels"](https://www.reforge.com/blog/growth-loops); [Brian Balfour — Four Fits essays](https://brianbalfour.com/four-fits-growth-framework)) — replace the funnel as the growth model. A loop is a closed system where the *output* of one iteration is the *input* of the next: users produce something (content, invites, revenue, data) that acquires more users, whose engagement produces more of that same output, and so on. The best-scaling companies of the last two decades are legible as loops, not funnels: Google's content loop (users create pages → pages rank → new users find them → some create pages), Slack's viral loop (users invite teammates → teammates create workspaces → more invites), Snowflake's usage loop (usage grows → billing grows → billing funds more product → more usage). Each loop compounds — the output feeds the input — in a way the funnel cannot describe.

This chapter names the four dominant loop archetypes, walks the diagnosis of *which loop the product supports* (and, critically, when the honest answer is *"none, and we should say so"*), and shows how to make the loop legible in the retention + expansion scorecard.

## Core concepts

### Why the funnel fails as a growth model

The AARRR funnel is a good user-journey diagram. As a growth model it makes three errors:

- **Linear input, linear output.** The funnel says: to double revenue, double top-of-funnel spend and hold conversion rates constant. This is true only if there is no mechanism by which existing customers or product usage produce *new* top-of-funnel — and the whole point of a compounding business is that such a mechanism exists.
- **Stage independence.** The funnel invites you to treat activation, retention, and referral as separate optimisation surfaces. In a real loop, they are coupled — the specific behaviour that retains a user is often the same behaviour that acquires the next one (invite, share, publish, transact).
- **Referral as a "leaky bucket" tail.** The funnel puts referral as the last stage almost as an afterthought — some fraction of retained users refer, and referrals flow back to acquisition. This under-weights the referral / loop dynamic; in loop-native businesses, the referral / self-acquisition flow is the *primary* growth engine, not the tail.

The funnel is useful as a **within-stage instrument** — for measuring per-stage conversion rates, per-stage cohorts, per-stage cycle times. It fails as a **cross-stage growth model** — the picture you use to decide where to invest the next dollar. Growth loops replace it at that model level, not at the instrument level.

### The loop primitive — input, action, output, feedback

Balfour's frame ([Reforge — "Growth Loops are the New Funnels"](https://www.reforge.com/blog/growth-loops)) defines a loop as a four-part cycle:

1. **Input** — a fresh user, a piece of content, a dollar of revenue, a data point. The starting condition of a single loop iteration.
2. **Action** — what the input does inside the product to produce the output. The user takes a value action; the content ranks; the revenue funds the next investment.
3. **Output** — the artifact the loop produces. Invites, more content, more revenue, more data.
4. **Feedback** — the output re-enters as the next iteration's input, closing the loop.

A working loop compounds. A broken loop does not — the output is produced, but does not become the next iteration's input (users are invited but do not accept; content is created but does not rank; revenue is produced but is not re-invested in the loop).

The **health of a loop** is measured by two numbers:

- **Loop conversion rate.** For each iteration, what fraction of outputs become the next iteration's inputs? Analogous to Reforge's "growth accounting" metric: for every new user, how many additional users does the loop produce? ([Reforge — Growth Loops](https://www.reforge.com/blog/growth-loops); [Andrew Chen — retention essays](https://andrewchen.com/)).
- **Loop cycle time.** How long does one iteration take? Viral loops on chat products cycle in hours; content loops on SEO cycle in months.

A loop is *net-productive* when `conversion rate ≥ 1 / (1 − retention rate)` — i.e., it produces enough output per iteration to overcome the churn of the inputs it consumed. When it clears that bar, growth compounds. When it does not, growth requires external input (paid acquisition, sales-hired outbound) — and the loop is a supporting motion, not the primary growth engine.

### The four dominant loop archetypes

Practitioner writing (Balfour / Reforge, Chen, Elena Verna) converges on roughly four loop archetypes that describe most modern SaaS + consumer growth motions. Each has canonical shape, canonical archetype companies, and canonical failure modes.

**1. Viral loop.**

- **Input:** an active user.
- **Action:** the user takes a product action that inherently exposes another person to the product — sends a link, invites a teammate, shares a doc, sends a message that is embedded in the product.
- **Output:** a new user (or a returning invited-user).
- **Feedback:** the new user becomes an active user and repeats the cycle.
- **Loop metric:** the **K-factor** — invites per active user × conversion rate of invites to active users. K > 1 is exponential; K between 0 and 1 is a decaying loop that amplifies but does not self-sustain; K = 0 is no loop.
- **Archetypes:** Slack (workspace invites), Zoom (meeting invites are effectively signup invites), Dropbox in its 2008 "double-sided referral" launch, WhatsApp (contact discovery).
- **When it fits:** products with an inherent multi-user collaborative action; products where the value is only realised when other users join; products whose primary use case *is* communication or sharing.
- **Common failure:** dressing up a solo-use product with a "refer a friend" button. Referral is a bolt-on incentive, not a loop; it does not compound and it produces low-fit users who churn quickly.

**2. Content loop.**

- **Input:** a user (or a piece of user-generated content, or an editorial content investment).
- **Action:** the input produces or attracts content that is discoverable by search engines, social feeds, or content-recommendation systems.
- **Output:** new users who discover the product through the content.
- **Feedback:** those users generate more content (or engage in ways that produce more content), and the cycle repeats.
- **Loop metric:** organic search traffic growth compounded per unit of content produced; long-tail search coverage; content-produced-per-user rate.
- **Archetypes:** Google (users create pages / businesses / reviews; searches surface them; new users arrive), YouTube (creators upload → viewers subscribe → some become creators), Stack Overflow (askers post questions → answerers respond → future Google searches surface the pair), Pinterest, Reddit, Zillow (listings), Yelp (reviews). In B2B SaaS, the closest analogues are HubSpot's content-marketing loop (blog + tools attract SMB marketers → become customers → some contribute case studies / referrals) and Notion's template gallery (users publish templates → discoverable → new users clone them).
- **When it fits:** products where users produce artifacts that are inherently indexable and useful to others; products with a content-native use case; markets where search and social intent are how buyers find solutions.
- **Common failure:** treating "we write blog posts" as a content loop. A content marketing programme is a *paid content investment* (a paid loop, arguably) — it becomes a *loop* only when users produce the content and the content produces the users. HubSpot's own blog is a hybrid — the editorial content is paid input, the case studies and community posts are the loop layer.

**3. Paid loop.**

- **Input:** a dollar of paid acquisition spend.
- **Action:** paid channels (search, social, display, retargeting) produce impressions and click-throughs; a fraction convert to paying customers.
- **Output:** revenue from the converted customer.
- **Feedback:** the revenue funds the next dollar of paid acquisition — but only if the payback period is short enough that the loop can sustain itself.
- **Loop metric:** **payback period in months** and **LTV / CAC ratio**. A paid loop is net-productive if payback < contribution-margin-adjusted runway and LTV/CAC clears the underwriting threshold (typically ≥ 3× — [Bessemer / SaaStr / David Skok benchmarks](https://www.forentrepreneurs.com/saas-metrics-2/)).
- **Archetypes:** direct-to-consumer subscription businesses (early Casper, Warby Parker in DTC-launch mode), transactional marketplaces at scale (early Airbnb paid acquisition), most B2C mobile app growth via App Store Ads / Facebook Ads.
- **When it fits:** products with high LTV, short payback, and where the paid channel produces high-fit users at a stable CAC.
- **Common failure:** running a paid loop at negative payback (LTV/CAC < 1) and calling it growth. This is *buying* revenue that costs more than it produces; the "growth" is a fundraise-subsidised burn. Also: running a paid loop before the retention curve flattens — the leaky-bucket arithmetic in Chapter 1 destroys the loop economics.

**4. Sales-assisted loop.**

- **Input:** a customer closed by the sales motion (mod-105 / mod-107).
- **Action:** the customer expands within their account (Chapter 3 expansion motion) and produces reference-able outcomes; the sales team runs mod-108 outbound into peer accounts using the reference; some accounts close.
- **Output:** the next customer, closed with a shorter sales cycle and higher conversion because the reference exists.
- **Feedback:** that customer produces the next reference and the next set of expansion outcomes.
- **Loop metric:** sales-cycle time compression on referenced deals vs. cold outbound; per-customer downstream logo influence (how many peer-accounts referenced this customer); expansion ARR per starting logo.
- **Archetypes:** enterprise SaaS motions where a marquee logo produces peer-account momentum (Salesforce in its early years; ServiceNow's Fortune 500 land-and-expand; many modern vertical SaaS motions). Also the founder-led community + sales motion where the community produces qualified pipeline (early Segment, Retool, Vercel).
- **When it fits:** enterprise or mid-market ACV where reference-selling meaningfully compresses cycle time; markets where buyer trust in peer-signal is high (regulated industries, high-consequence purchases).
- **Common failure:** claiming a "sales-assisted loop" when the reality is just "we do sales." A loop requires that the *output* (customers + expansion + references) meaningfully improves the *input economics* (next customer's cycle time and conversion rate). If a new-logo AE's cycle time and win rate are unchanged after two years of customer references, there is no loop — there is a sales motion.

### The composition question — one loop, or several

Real companies often have more than one loop. Reforge writes about this as a "growth model" — the composition of loops the business runs. Common compositions:

- **Slack:** Viral loop (dominant) + sales-assisted loop (for Enterprise Grid contracts).
- **Snowflake:** Sales-assisted loop (dominant) + usage-based expansion (which functions as a revenue loop — usage produces billing which funds the next round of expansion sales).
- **HubSpot:** Content loop (dominant) + sales-assisted loop (mid-market and up) + paid loop (SMB conversion).
- **Notion:** Viral loop (individual → team → workspace) + content loop (template gallery, user-generated tutorials) + sales-assisted loop (enterprise tier).

At Series-A, **most companies should have one primary loop that is operating and one secondary loop that is being invested in**. Trying to run all four is analogous to the mod-108 Chapter 1 anti-pattern of running six channels at 15% investment each — no loop reaches the investment threshold to work.

### Diagnosing which loop the product supports — and when the honest answer is "none"

This is where the module intersects harshly with founder wishful thinking. Not every product supports a loop; some businesses are honestly linear-funnel businesses that grow by outbound and never compound. That is not a failure — it is a fact about the market and the product — and pretending otherwise leads to failed loop investments that consume 12–18 months.

Diagnostic questions per loop:

**Viral loop diagnostic.**
- Does a single user take a value action that inherently exposes another person to the product? (Not "would they refer if we asked" — does the *value action* produce exposure?)
- Is the multi-user product experience better than the single-user experience? (Slack is; a solo note-taking app is not.)
- Is K-factor measurable in your existing data? Compute it: for each new user, how many other users did they cause to sign up in their first 30 days? If K < 0.1, there is no viral loop yet.

**Content loop diagnostic.**
- Do users produce artifacts that are indexable (by search, social, or in-product discovery) and useful to non-users?
- Is at least one type of user-produced artifact receiving external traffic (organic search, social shares, referrals) at meaningful volume?
- If you turned off editorial content investment tomorrow, would user-generated content continue to grow organic acquisition? If yes, there is a content loop. If not, there is a content marketing programme.

**Paid loop diagnostic.**
- Do the underlying unit economics support a paid loop? LTV / CAC ≥ 3× and payback ≤ 12–18 months (mid-market SaaS band per [David Skok](https://www.forentrepreneurs.com/saas-metrics-2/)) are working thresholds.
- Is there a paid channel where the CAC has been stable across at least 3–6 months of consistent spend (i.e., not the low-CAC honeymoon of a small-scale spend)?
- Is the retention curve flat in the segment the paid channel acquires? (Chapter 1: leaky bucket destroys paid economics.)

**Sales-assisted loop diagnostic.**
- Is the average sales cycle for a referenced deal materially shorter than for a cold-outbound deal? Compute both, actually.
- Is the win rate on referenced deals materially higher than on cold-outbound? Compute both.
- Does one closed customer meaningfully influence the pipeline for peer accounts (via reference, integration, or community)? Measurable via source-of-lead attribution.

**When none fires.** If every loop diagnostic comes back negative, the honest scorecard read is *"our growth engine is a linear funnel — outbound → close → renewal → outbound to next account, with modest organic tail from word-of-mouth."* This is a completely legitimate business model — most professional services firms, most vertical SaaS at early stage, and most bootstrapped B2B companies operate this way. The failure is not that the business is a funnel; the failure is *claiming a loop that does not exist* and investing 12–18 months in it anyway.

### The AARRR funnel is still useful — for its actual job

Do not throw the funnel away. It remains the right instrument for:

- **Per-stage conversion measurement.** What fraction of signups activate? Of activated users retain? Of retained users refer? These are legitimate operational metrics.
- **Cohort walkthrough diagnostics.** For a specific cohort, tracing where users drop is a funnel operation.
- **User-journey mapping.** The five stages are a compact vocabulary for describing what a single user does.

What the funnel is *not*: the picture you use to model whether the business compounds. That picture is a loop (or an honest funnel-and-outbound linear machine).

## Concrete example — the code-review-tool loop diagnosis

Return to the code-review-tool. The team is thinking through growth-loop investment for the next four quarters.

**Viral loop diagnostic.**

- The product is multi-user by definition (teams review each other's PRs). Users are added to teams, but the invite mechanism is admin-driven (an admin adds a new user via GitHub / Slack integration), not user-driven.
- K-factor computed against user-caused-invite data: 0.4 (each new user causes 0.4 new users within 30 days, mostly via admin adding the whole team when the champion adopts).
- **Diagnosis:** partial viral loop with K < 1 (amplifies but does not self-sustain). Investable if the product could shift admin-invite to user-invite (e.g., in-product "invite this reviewer" nudge when a mention is made to a non-user). Meaningful lever but not the primary loop.

**Content loop diagnostic.**

- Users do not produce indexable public artifacts as a byproduct of using the product. All content is internal to the customer's private code repo.
- The company runs a marketing blog with technical case studies and code-review best-practice writing — receives organic search traffic, but the content is editorial (paid input), not user-generated.
- **Diagnosis:** no content loop. There is a content marketing programme, which is a paid loop in disguise (spend on editorial → traffic → conversion). Do not claim a content loop.

**Paid loop diagnostic.**

- LTV / CAC: 2.1× (below the 3× band). Payback: 14 months (borderline).
- Paid channel (LinkedIn Ads on eng-manager targeting) has been running for 4 months at $12k/mo. CAC has drifted upward from $3.8k to $4.9k as spend scaled.
- Retention curve in paid-acquired cohorts is weaker than in outbound-acquired cohorts (Chapter 1 example).
- **Diagnosis:** paid loop is *not net-productive at current economics*. Chapter 1's channel-market-fit finding says the paid channel is acquiring lower-fit cohorts. Do not scale spend; either fix targeting or defund.

**Sales-assisted loop diagnostic.**

- Referenced-deal cycle time: 42 days. Cold-outbound cycle time: 78 days. Referenced deals are 46% faster.
- Referenced-deal win rate: 38%. Cold-outbound win rate: 22%. Referenced deals win at 1.7×.
- Two anchor customers (a well-known unicorn engineering org and a public developer-tools company) have influenced 11 named-peer opportunities in the past 6 months.
- **Diagnosis:** working sales-assisted loop. This is the primary loop the product supports at current stage. Invest in a formal reference programme, a customer-community programme, and case-study production tied to expansion outcomes.

**Verdict for the scorecard.**

- **Primary loop:** sales-assisted (working, measurable, invest).
- **Secondary loop:** partial viral (K = 0.4) — invest in shifting admin-invite to user-invite as a one-sprint experiment; re-measure K.
- **No content loop.** The content programme is a paid loop; treat it as such.
- **Paid loop is not net-productive at current economics.** Do not scale until CAC / LTV clears the underwriting bar.

That reads as a clean, honest loop diagnosis — one primary loop that the product supports, one secondary loop the product partially supports and the team can invest in, one explicit "no loop here" call, and one "not yet" verdict on a loop the unit economics do not support. The scorecard reads the same way; the roadmap allocation follows the loop diagnosis.

## Common failure patterns

- **Using AARRR as the growth model.** Fine as an instrument; wrong as a picture of how the business compounds. Use loops for the picture.
- **Claiming a viral loop when K < 0.1.** A "refer a friend" button is not a viral loop. Compute K on real data.
- **Claiming a content loop when the content is editorial-produced.** That is a content marketing programme (a paid loop in effect). Only user-produced content that acquires more users is a content loop.
- **Running a paid loop through a leaky retention curve.** Chapter 1's arithmetic destroys the economics. Fix retention first.
- **Claiming a sales-assisted loop when referenced deals don't materially outperform cold outbound.** If cycle time and win rate are the same, there is no loop — there is a sales motion.
- **Running all four loops at 25% investment each.** Loops require investment thresholds; four half-funded loops produce no working loops.
- **Refusing to name "no loop exists here."** Some businesses honestly do not have a compounding loop. Naming it is not a failure; pretending otherwise costs 12–18 months.
- **Skipping the loop metric.** A loop without a measurable conversion rate and cycle time is not a loop; it is a hope. Instrument the metric.
- **Using loop language to justify a strategy the metrics do not support.** If K is 0.4 and LTV/CAC is 1.5, saying "we're building for loops" does not fix the numbers. The metrics decide.

## Summary

- **The AARRR funnel is a user-journey instrument, not a growth model.** Fine for per-stage measurement; wrong as a picture of compounding growth.
- **Growth loops** (Balfour / Reforge) are the growth-model replacement. A loop is input → action → output → feedback where output re-enters as the next iteration's input.
- **Four dominant loop archetypes:** viral, content, paid, sales-assisted. Each has canonical shape, metric, archetype companies, and failure modes.
- **Loop health is measured by conversion rate and cycle time.** A loop is net-productive when conversion rate clears the churn threshold; otherwise growth requires external input.
- **Composition:** most companies run one primary loop and one secondary. Trying to run all four at Series-A produces no working loops.
- **The diagnostic question is which loop the product actually supports** — computed from real data (K-factor, user-generated content acquisition, paid unit economics, referenced-deal cycle time and win rate). The honest answer is often "one primary and none of the others" — sometimes "none of the four."
- **The AARRR funnel still has a job — per-stage conversion, cohort diagnostics, user-journey mapping.** Use it there; use loops for the growth model.
