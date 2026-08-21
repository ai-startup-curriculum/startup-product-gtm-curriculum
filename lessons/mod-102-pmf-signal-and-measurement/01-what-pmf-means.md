# What Product-Market Fit Means

## Motivation

Before you can measure product-market fit, you have to agree on what it *is*. Most founders inherit the term as a vague synonym for "things are going well" — which is why "we have PMF" and "we don't have PMF" get said about the same startup in the same week. The number one reason PMF discussions go nowhere is that the participants are quietly using different definitions.

This chapter fixes the vocabulary. It anchors two definitions (Andy Rachleff's and Marc Andreessen's), one operational read (Sean Ellis's "very disappointed" survey, unpacked in Chapter 3), and one structural read (cohort retention flattening, unpacked in Chapter 4). Everything else in the module rests on these.

## Core concepts

### The origin — Andy Rachleff and Don Valentine

Andy Rachleff — co-founder of Benchmark, later founder of Wealthfront — is the person who codified the term. Rachleff credits the underlying idea to Don Valentine (Sequoia); the compact phrase is Rachleff's own ([Andy Rachleff — "Product/Market Fit: What it really means, How to Measure it, and Where to find it"](https://www.wealthfront.com/blog/product-market-fit/); [Rachleff on the Wealthfront blog archive](https://www.wealthfront.com/blog/tag/andy-rachleff/)).

Rachleff's frame: a startup at inception has two hypotheses to test in order — a **value hypothesis** (does the product deliver value to the customer such that they will use / pay for it?) and a **growth hypothesis** (once value is proven, is there a repeatable, scalable way to acquire customers?). **PMF is the moment the value hypothesis is proven** — not the moment growth kicks in. Confusing the two collapses the whole search: you build growth machinery on top of a product that has not earned it, and you scale a leak.

### The pmarchive definition — Marc Andreessen

Marc Andreessen's 2007 essay "The Only Thing That Matters" is where the phrase went mainstream ([Marc Andreessen — "The Only Thing That Matters" (2007)](https://pmarchive.com/guide_to_startups_part4.html)). Two of Andreessen's sentences are the definitional core the industry still uses:

> *"Product/market fit means being in a good market with a product that can satisfy that market."*
>
> *"You can always feel when product/market fit isn't happening... And you can always feel product/market fit when it's happening. The customers are buying the product just as fast as you can make it — or usage is growing just as fast as you can add more servers. Money from customers is piling up in your company checking account. You're hiring sales and customer support staff as fast as you can. Reporters are calling because they've heard about your hot new thing and they want to talk to you about it. ... You start getting entrepreneur of the year awards from Harvard Business School. Investment bankers are staking out your house."*

The second passage is often quoted as if it were the definition. It is not. It is a **portrait of downstream symptoms** in the specific case where PMF has landed hard in a large market. Read plainly, it tells you what strong PMF *feels like* — but "waiting for the checking account to fill up on its own" is a terrible operating instrument because by the time it shows up, you have already burned the runway you needed to find out earlier.

The module treats Andreessen's frame as the north-star description of the *system state* PMF represents, and Rachleff's frame as the *hypothesis structure* you actually test to detect it.

### Two working definitions the module uses

The rest of the module operates on two compact working definitions. Keep both in your head; they detect the same underlying state from different angles.

- **Working definition 1 (behavioural / structural).** PMF is the state where **retention curves flatten** at a segment-appropriate level and **demand is pulling** — new users arrive faster than the team can consciously push them; existing users would find the product's removal painful; word-of-mouth substitutes for paid acquisition at the margin. Chapters 3 and 4 are the operating instruments.
- **Working definition 2 (survey / declarative).** PMF is the state where **≥40% of active users** answer "very disappointed" to Sean Ellis's *"how would you feel if you could no longer use this product?"* survey ([Sean Ellis — pmfsurvey.com](https://pmfsurvey.com/); [Sean Ellis — "Using Product/Market Fit to Drive Sustainable Growth" (2009)](https://web.archive.org/web/20101025110359/http://startup-marketing.com/using-product-market-fit-to-drive-sustainable-growth/)). Chapter 3 unpacks the instrument.

Both definitions collapse a wider distribution of "how would you know" into a working threshold. Both are lossy. Neither is a substitute for the other — the survey can register 40% while retention leaks (a passionate niche within a churning majority), and retention can flatten at a low level while the survey misses because the sample was drawn from all signups instead of active users. The module teaches you to run both and cross-check.

### PMF is a system state, not a milestone

The most common vocabulary error is treating PMF as a **binary milestone** — "we hit PMF in Q2." That framing has three problems the rest of the module will keep hitting:

- **It is not stable.** PMF can be lost — new entrants change the alternatives set, the market shifts, a bigger platform ships your feature, your segment matures out of the pain. Every PMF measurement has a shelf life ([Brian Balfour — "The Never Ending Road to Product/Market Fit"](https://brianbalfour.com/essays/product-market-fit)).
- **It is segment-specific.** You can have strong PMF in one ICP slice (mid-market design agencies) and no PMF at all in a slice you thought was the same (enterprise design departments). One aggregated number hides the split.
- **It is time-specific for cohort measurements.** A retention curve that flattened for 2023 signups can decay for 2025 signups if the market changed. PMF measured last year does not carry over.

Treat PMF as a **system state** that you continuously check — like credit rating, not like a birthday. The Superhuman engine (Chapter 5) is what this looks like operationally.

### The two error modes — false-positive and false-negative PMF

Both errors are expensive.

- **False-positive PMF.** You believe you have PMF and start scaling — hiring AEs, buying paid ads, running the growth playbook. Retention was actually leaking; the acquired users churn out; CAC exceeds LTV; you burn the round. This is the more common error at PRE-SEED / SEED because founders read anecdotal signal as PMF signal (Chapter 2 is the whole antidote).
- **False-negative PMF.** You believe you have not found PMF and keep pivoting. Retention was flattening in a real segment; you were about to compound; you abandon a working product for a rewrite. Less common, but Superhuman itself is a case study — Rahul Vohra's team measured 22% "very disappointed" and treated it as a pre-PMF signal to iterate against ([Rahul Vohra — "How Superhuman Built an Engine to Find Product/Market Fit", First Round Review](https://review.firstround.com/how-superhuman-built-an-engine-to-find-product-market-fit/)), rather than either declaring victory or pivoting away.

The point of measuring rigorously is that both errors cost real money. The Sean Ellis survey and the cohort retention read are cheap enough — hours, not months — that running both beats guessing.

## Concrete example — the same team, two definitions in tension

Imagine a team building a code-review tool. They have:

- 800 signups after a Product Hunt launch.
- 12 teams paying $200 / month each after month one.
- One founder-friend, a well-known engineering leader, tweeted about them.
- Weekly active teams: 45 in W1 (post-launch), 32 in W2, 21 in W3, 18 in W4, 17 in W5, 17 in W6.
- Sean Ellis survey (sent to all 800 signups): 12% "very disappointed".

Which of the following claims is defensible?

- **"We have PMF — a top engineering leader tweeted about us and we have paying customers."** No — Chapter 2 will show these are anecdotal signal, not PMF signal.
- **"We have PMF because 12 teams are paying."** No — 12 teams is either a small early-adopter cluster or a niche; neither implies market-scale pull.
- **"We do not have PMF because the survey came back at 12%."** Not yet — the survey was mailed to *all signups*, not active users. The instrument was mis-run (Chapter 3).
- **"We have flattening retention in the 17-team plateau."** Possibly — 17 teams retained from week 3 through week 6 is a small but real flattening signature (Chapter 4). Cohort by signup date, isolate the 17, resurvey *only* the actives, look at their main-benefit statements. Rachleff's "value hypothesis is proven for this segment" may be defensible for that plateau — but the launch-week 800 is a marketing artifact, not a PMF read.

The move is: **run the instruments cleanly on the right sample before making any claim.** Chapters 3–5 are that discipline.

## Common failure patterns

- **Using Andreessen's downstream symptoms as the definition.** "Reporters are calling" is an outcome of PMF landing in a large market during a media cycle. It is not evidence that a smaller team, in a smaller market, does not have PMF.
- **Conflating value hypothesis and growth hypothesis.** The founder has hired a growth lead before the retention curve flattens. Growth without retention scales the leak — every incremental dollar of CAC evaporates through churn.
- **Aggregating across segments to hide the split.** The company-wide Sean Ellis result is 22%. Inside the mid-market design-agency segment it is 51%. Inside the enterprise slice it is 6%. The 22% average hides both signals — the real PMF in one segment and the real anti-signal in the other.
- **Treating PMF as durable once achieved.** The market moves; a bigger platform copies the feature; a segment matures. Every PMF measurement has a shelf life; run the instruments on a cadence (Chapter 5), not once.

## Summary

- **Rachleff's frame:** a startup tests a **value hypothesis** before a **growth hypothesis**; PMF is the moment the value hypothesis is proven. Do not skip ahead.
- **Andreessen's frame:** *"a good market with a product that can satisfy that market"*; the downstream symptoms he lists are consequences of strong PMF landing in a large market, not the operating definition.
- The module uses two working definitions in parallel — **survey-declarative** (≥40% "very disappointed", on active users) and **behavioural-structural** (retention flattening + pull-based demand). Both are lossy; cross-check.
- PMF is a **system state, not a milestone** — it can be lost, it is segment-specific, and every measurement has a shelf life.
- Both **false-positive** (declare early, scale the leak) and **false-negative** (over-pivot away from real PMF) errors are expensive. Measurement is what makes the errors smaller.
