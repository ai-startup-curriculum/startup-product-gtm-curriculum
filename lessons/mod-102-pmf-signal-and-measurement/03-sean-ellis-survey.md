# The Sean Ellis Survey — Run It Properly

## Motivation

Sean Ellis's *"how would you feel if you could no longer use this product?"* survey is the single cheapest, most-portable PMF instrument the industry has. It costs an email, a form, and an afternoon of analysis. It produces a number that maps cleanly to a working threshold, plus free-text answers that tell you what to do next.

It is also **the instrument founders most consistently misuse.** They mail it to all signups instead of active users. They read a 22% "very disappointed" result as a definitive no. They skip the diagnostic free-text questions and end up with a percentage and no roadmap. They send it once and treat it as a one-shot measurement. Each of these errors turns a good instrument into a misleading one.

This chapter is the operating manual: who to sample, what to ask, what threshold to use, what the sub-40% diagnostics tell you, and the common misreads to avoid.

## Core concepts

### The origin — Sean Ellis, 2009 onward

Sean Ellis first described the survey and the 40% heuristic on his startup-marketing.com blog in 2009 ([Sean Ellis — "Using Product/Market Fit to Drive Sustainable Growth" (2009)](https://web.archive.org/web/20101025110359/http://startup-marketing.com/using-product-market-fit-to-drive-sustainable-growth/)); the tooling and current phrasing live at [pmfsurvey.com](https://pmfsurvey.com/). Ellis and co-authors returned to the framework at book length in *Hacking Growth* (2017), which unpacks the survey as one instrument inside a broader growth-experimentation cadence ([Sean Ellis and Morgan Brown — *Hacking Growth* (2017)](https://www.hackingrowth.com/)).

The single load-bearing sentence from Ellis's original writing is his 40% observation: across ~100 startups he surveyed, teams that reported **≥40% of active users answering "very disappointed"** were the ones on trajectories his advisory work classified as PMF-established. Below 40%, teams struggled to grow sustainably; above 40%, teams generally grew.

That 40% is a **heuristic threshold**, not a physical constant. Ellis has been explicit about this — it is a working line that separates two clusters he observed, not a law of nature. Some products cross into strong PMF at 30% (for reasons Chapter 5's Superhuman example unpacks); some products at 45% still have significant blockers to solve. Treat 40% as a decision boundary you review, not a target you hit.

### The exact question

Use Ellis's phrasing. Do not paraphrase.

> **How would you feel if you could no longer use \[Product\]?**
>
> - Very disappointed
> - Somewhat disappointed
> - Not disappointed (it isn't really that useful)
> - N/A — I no longer use \[Product\]

The four options matter. "Very disappointed" is the strong-positive bucket that anchors the 40% threshold. "Somewhat disappointed" is the ambivalent middle — big enough to matter, small enough to be a diagnostic segment (Chapter 5 targets this cohort specifically). "Not disappointed" is the negative segment; it lets you separate people who tried the product and found no value from people who never really tried at all. The N/A option surfaces churned users who would otherwise be silent in the response.

Do not add a five-point Likert scale, do not compress to yes/no, and do not swap "disappointed" for "sad" or "unhappy". The word "disappointed" carries a specific meaning — the sense of a loss you would notice — that is what the 40% calibration was built against.

### Sample selection — the most-broken step

The single most common execution error is running the survey against **all signups** instead of **active users**. If you mail 5,000 signups and 4,000 of them stopped using the product within 48 hours, the "not disappointed" count will dominate and the 40% number will be meaningless.

The sample must be **users who have experienced the product's value** — the population for whom the "could no longer use" question is coherent. Two working definitions, either is defensible:

- **Ellis's own recommendation:** users who have used the product **at least twice** within the last **two weeks**. This is a general-purpose active filter; adjust for your natural usage cadence.
- **Product-specific "activated" filter:** users who have hit your natural activation event at least once and used the product within a period appropriate for the product (e.g. sent one email through Superhuman; created and shared one Loom; deployed to production at least once). For most B2B SaaS at PRE-SEED / SEED this is the closer filter.

The exclusion rule matters as much as the inclusion. **Exclude** users who signed up and never activated, users who churned before the survey window, and users on completely different plans / SKUs where "could no longer use this" means different things.

Sample size: aim for **≥30 responses in the very-disappointed bucket** before treating the score as stable. That typically means surveying 100–300 active users; response rates in the 15–30% range are normal.

### The four diagnostic questions

The Sean Ellis instrument is not one question, it is **five**. The percentage is the score; the four free-text questions are the roadmap.

1. **What type of people do you think would most benefit from \[Product\]?** — This surfaces the *segment* that self-selects into your very-disappointed bucket. When 25 of 30 very-disappointed responses describe the same role or company shape, you have a segment. Feeds directly into mod-104 (ICP).
2. **What is the main benefit you receive from \[Product\]?** — This surfaces the **modal main-benefit statement** — the compressed value the users actually experience, in their own words. Feeds directly into mod-103 (positioning). If ≥50% of very-disappointed users cite the same benefit in language you can pattern-match, you have positioning gold.
3. **Have you recommended \[Product\] to anyone? If so, how did you describe it?** — This surfaces the *word-of-mouth* language and the referral behaviour. If ≥30% of very-disappointed users have already recommended, you have organic pull; if 0% have, the value is real but the shareability is weak (Chapter 6's "wrong distribution" mode).
4. **How can we improve \[Product\] for you?** — This surfaces the **top blockers**. The signal you want is not "what do the very-disappointed want next" — it is **"what do the *somewhat*-disappointed users say is missing?"** Because those users are close to the boundary; unblocking them is what moves them into the very-disappointed cohort. This is the Superhuman-engine hinge (Chapter 5).

Some versions of the instrument include a fifth question, **"what would you likely use as an alternative if \[Product\] were no longer available?"**. That surfaces the competitive alternatives set (mod-103 Dunford component 1). Include it if you have room; most implementations do.

### Reading the score — the four zones

| Zone | Score band | Working interpretation |
|---|---|---|
| **Sub-25%** | <25% very-disappointed | Pre-PMF. The main-benefit statements are diffuse, the "who is this for" answers contradict each other, the somewhat-disappointed cohort is small. Return to discovery (mod-101) and Chapter 5's engine. |
| **25–40%** | 25–40% very-disappointed | Approaching PMF. You have a segment and a benefit; the Superhuman engine (Chapter 5) is the fastest path from here. Do not scale acquisition yet. |
| **≥40%** | ≥40% very-disappointed | Working PMF. Retention curve (Chapter 4) should confirm. Growth investment is defensible; scaling ahead of retention confirmation is not. |
| **≥55%** | ≥55% very-disappointed | Strong PMF (in the sampled segment). You should feel the pull; the question shifts to distribution and scale, not fit. |

The bands are heuristic — treat them as a rough guide, not a rating. The Superhuman team started at 22%, spent months on the Chapter 5 engine, and crossed into the 58% band by hardening the main benefit and unblocking the somewhat-disappointed cohort ([Rahul Vohra — "How Superhuman Built an Engine to Find Product/Market Fit"](https://review.firstround.com/how-superhuman-built-an-engine-to-find-product-market-fit/)). A sub-40% score is a starting position, not a verdict.

### The segment split — never trust the aggregate alone

The aggregate number lies whenever segments have different fits. Two products can both score 30% aggregate very-disappointed and mean completely different things:

- **Product X:** 30% aggregate = 55% in mid-market design agencies (n=40), 5% in enterprise design departments (n=40). One real segment; one dead segment. Route: kill the enterprise motion, double down on the mid-market motion.
- **Product Y:** 30% aggregate = 30% across every segment. No PMF anywhere; a mediocre product across the board. Route: back to discovery and the four-failure-mode diagnostic (Chapter 6).

**Always segment.** At minimum: by primary firmographic (company size, industry), by role, by tenure on the product (users active <1 month vs. ≥3 months), and by plan / SKU if you have more than one. The segments that cross the 40% line define your ICP; the segments that stay under it define your anti-ICP (mod-104 disqualifiers).

### The cadence — not a one-shot measurement

Chapter 1's system-state framing implies the survey is not run once. Ellis and *Hacking Growth* recommend running it on a **cadence** — quarterly is typical for early-stage; more frequent if the product surface is changing weekly. Each run's job is to detect drift (a segment that has crossed a line since the last measurement) and to test whether the previous iteration's roadmap moved the number.

Compare **the same segment across time**, not the aggregate. A quarterly aggregate can be flat while your target segment climbs 20 points because a different segment declined 15 points; the aggregate hid both moves.

## Concrete example — a full survey run

Return to the code-review-tool. The team has 340 users who have opened at least three PRs in the last two weeks (their working "active" filter). They mail the survey to all 340.

**Response:** 89 responses (26% response rate).

**Aggregate score:** 22 of 89 (25%) very-disappointed. Aggregate is at the "approaching PMF" boundary — not enough to declare, not so bad they need to pivot.

**Segment split:**

| Segment | n (very-disappointed / total) | % very-disappointed | Verdict |
|---|---|---|---|
| Mid-market (50–200 eng), distributed teams | 15 / 27 | **56%** | Strong PMF signature |
| Small teams (<20 eng) | 4 / 30 | 13% | No PMF; per Chapter 6, likely wrong-market |
| Enterprise (500+ eng), single BU pilot | 3 / 32 | 9% | No PMF; likely wrong-product for the segment (needs different features) |

The aggregate 25% completely hides the mid-market 56%. Reading the aggregate would produce the wrong roadmap.

**Main-benefit free-text on the 15 very-disappointed mid-market users:** 11 of 15 wrote some version of *"finally know who to nudge without becoming the nag"* or *"cut the time-to-first-review on stale PRs"*. That is the modal benefit; it becomes the mod-103 positioning input.

**"How to improve" from the 22 somewhat-disappointed users** (across all segments): the top three blockers cluster as (a) *"no GitHub Enterprise support yet"*, (b) *"digest is too noisy — one Slack ping per stale PR is too much"*, (c) *"need per-team ownership rules, not global"*. Those three become the Superhuman-engine roadmap items (Chapter 5).

**"Who benefits most" free-text on the 15 very-disappointed:** 13 of 15 describe some form of "EM at a distributed 50–200-person eng org with time-zone-spread reviewers". This is the sharpened ICP for mod-104.

**Route** (per Chapter 6):
- Mid-market segment: **PMF found**; scale acquisition against this segment; harden the main benefit (Chapter 5).
- Small-teams segment: **wrong market**; deprioritise or explicitly disqualify from ICP.
- Enterprise segment: **wrong product for this segment** (missing enterprise features); park until GitHub Enterprise support ships and re-survey.

That is what a properly-run survey produces: a segmented score, an ICP definition, a positioning input, a roadmap, and clear routing decisions.

## Common failure patterns

- **Sampling all signups.** The most common single error. Filter to active users first. If the active pool is too small to sample from (<50 people), the answer is *keep pushing through mod-101* to grow the active pool, not lower the bar.
- **Reading the aggregate without segmentation.** The aggregate hides both the winning segment and the losing segment. Always split.
- **Skipping the free-text questions.** The score is a scoreboard; the free-text is the roadmap. A team that runs only the multiple-choice question knows their number and has no idea what to do next.
- **Reading "somewhat-disappointed" as neutral.** It is not. Somewhat-disappointed users are the highest-leverage roadmap cohort — they are one blocker away from very-disappointed. Their "how to improve" free-text is the single most valuable output of the entire instrument.
- **Rewriting the wording.** "Disappointed" is calibrated to the 40% threshold; every deviation loses the comparability. Do not "improve" the phrasing.
- **Running it once and never again.** Systems drift; competitors ship; the market moves. The instrument only earns its keep if it is re-run on a cadence.
- **Treating 40% as a birthday.** 40% is a threshold to cross, then keep measuring — not a milestone to celebrate and stop.

## Summary

- **Exact question:** *"How would you feel if you could no longer use \[Product\]?"* — four options — do not paraphrase.
- **Sample:** active users (used the product at least twice in the last two weeks, or equivalent product-specific "activated" filter). Exclude non-activated signups and churned users.
- **Threshold:** ≥40% "very disappointed" as a **working heuristic** for PMF; 25–40% approaching, <25% pre-PMF, ≥55% strong-PMF in that segment.
- **Ask all four diagnostic questions:** who benefits most (→ ICP), main benefit (→ positioning), have you recommended (→ pull signal), how to improve (→ roadmap, target the *somewhat*-disappointed cohort).
- **Always segment** — the aggregate hides both wins and losses.
- **Run on a cadence** — the score is a system-state read, not a one-shot measurement.
