# Outbound at Seed Scale — the Founder as the First SDR

## Motivation

Outbound at seed scale is not the same activity as outbound at Series-B scale. Series-B outbound is a machine — Predictable-Revenue-tradition SDRs feeding AEs, running proven cadences against target-account lists built by an SDR manager, tuned by a RevOps team, and instrumented against benchmarks the CMO reports monthly (mod-107 Chapter 3 develops that machine). Seed outbound is a *founder* — writing the target-account list against her memory of the last 50 customer conversations, hand-crafting the first 20-touch sequence, sending it herself, replying herself, discovering what does and does not land, and rewriting the cadence three times before it produces its first predictable meeting. The two activities share vocabulary and share the eventual endpoint; they are otherwise almost different jobs.

Founders regularly fail at seed outbound by trying to run the Series-B machine at seed scale. They hire an SDR before the founder herself has written a cadence that works, load Salesforce and Outreach before knowing which sequence variant lands, buy Apollo enrichment against a target-account list built from lazy firmographic filters, and run a 12-touch cadence templated from a public blog post — with the result that the SDR produces zero pipeline in six months, the founder concludes "outbound doesn't work for our market," and the runway shortens by a couple hundred thousand dollars of over-invested tooling and salary. The seed-outbound half of the motion — the founder herself, cold-emailing hand-curated accounts with hand-written personalisation, learning what the ICP actually responds to — was never run.

The failure mode this chapter exists to catch: **the founder either (a) does not run outbound at seed because "we're not ready for sales yet", missing the six months of raw customer signal that outbound produces, or (b) tries to run outbound at Series-B scale immediately, hiring SDRs and buying tooling before the cadence has been validated by the founder herself — producing an SDR who cannot recover the founder's un-transferred pattern-knowledge, a cadence tuned to the wrong pain, and a target-account list that filters the ICP into a shape the product does not fit.**

This chapter builds the seed-outbound motion in the shape it actually works: the founder as the first SDR, the hand-curated target-account list, the personalised sequence, the response-rate expectations, the cadence discipline, and — critically — the *transition* from founder-run outbound to the SDR-AE motion mod-107 Chapter 3 develops. The two chapters are paired: mod-107 Chapter 3 is what you graduate *to*; this chapter is what you graduate *from*, and the graduation only works if the founder has run the seed-scale version herself long enough to know what to hand off.

## Core concepts

### The tradition — Predictable Revenue at seed scale

The operating tradition of modern outbound is Aaron Ross's *Predictable Revenue* (2011) — the role-split, the cadence discipline, the metric instrumentation — developed in mod-107 Chapter 3 as the mid-market SDR-AE motion. The tradition is the target endpoint of the seed-outbound programme; it is not the seed-outbound programme itself.

At seed scale, three modifications to the Predictable Revenue playbook are load-bearing:

**Modification 1 — the founder is the first SDR.** Kazanjy's *Founding Sales* (2021) is the practitioner text for this modification, which is itself grounded in Paul Graham's "Do Things That Don't Scale" and Steve Blank's customer-development tradition ([Kazanjy — *Founding Sales*, free web edition](https://foundingsales.com/); [Graham 2013 — "Do Things That Don't Scale"](https://paulgraham.com/ds.html)). Ross's *Predictable Revenue* implicitly assumes the specialised SDR — a rep whose sole job is prospecting — is on staff; at seed scale that rep does not exist, and the founder has to run the prospecting job herself for the first 3-9 months. The founder-as-SDR modification produces the un-transferable pattern knowledge that later SDR hires will inherit — the objections, the winning subject lines, the ICP tells, the accounts that respond and the ones that do not.

**Modification 2 — the list is hand-curated, not enrichment-generated.** At Series-B scale the SDR loads 500-account lists from Apollo / ZoomInfo / LinkedIn Sales Nav and runs cadences against them at volume. At seed scale, running the same volume against a machine-generated list burns the founder's time and produces near-zero response rate because the list has no signal of buying context beyond firmographics. The seed-outbound list is 100-300 accounts, each one hand-added by the founder based on a specific signal — company-in-hiring, recently-funded, using an adjacent-tool, mentioned-in-a-community-post, on-a-competitor's-customer-list, referred-by-an-existing-customer. Hand-curation is what makes 100 seed touches produce more meetings than 1,000 machine-generated touches.

**Modification 3 — personalisation is deep, and the founder writes the copy.** mod-107 Chapter 3's Level-1/2/3 personalisation gradient tiers accounts at scale, with Level-3 (deeply personalised) reserved for the top of the list. At seed scale, **every touch is Level 3** — the founder writes each cold email as a one-off, referencing the specific signal that put the account on the list, and the response rate is 5-20× the templated-outbound baseline. Ross's high-volume templated approach is a scale-stage motion; seed scale runs on hand-crafted volume that stays inside the founder's capacity for personalisation.

The three modifications produce a seed-outbound motion that looks nothing like the Series-B SDR machine on the surface — no cadence tool at first, no CRM cadence, no benchmarks against Outreach.io's State of Sales report — but that is producing exactly the raw material the Series-B machine will eventually be built from. The transition (developed at the end of this chapter) is the hand-off from founder-run seed outbound to the mod-107 Chapter 3 SDR-AE motion.

### The target-account list — the hand-curation discipline

The target-account list is the load-bearing input to seed outbound. A bad list produces a low reply rate no cadence tuning can fix; a good list produces reply rates the practitioner benchmarks call impossible ("15% response rate on cold email is unrealistic"; it is unrealistic on a machine-generated list of 500 firmographic-filter accounts; it is routinely achieved on a hand-curated list of 100 signal-selected accounts).

The seed-outbound list is built against a **signal-selection discipline**, not a firmographic-filter discipline. Every account on the list has at least one of the following signals attached to it — logged in the founder's CRM or spreadsheet as the reason the account is on the list.

**Category A — buying-context signals (highest priority).**
- Recently funded (Series A/B/C within the last 6 months — funding announcement signals budget and growth). Sources: Crunchbase, PitchBook, [TechCrunch](https://techcrunch.com/), announcement filings.
- Hiring for a role adjacent to the pain (e.g. Loomly's ICP hires platform engineers, SREs, DevEx leads). Sources: LinkedIn Jobs, [YC job board](https://www.workatastartup.com/), company careers pages.
- Recently changed executive leadership in the buyer's function (new VP Eng, new Head of Platform). New leadership brings tool-review budgets. Sources: LinkedIn, press releases.
- Reported publicly on the specific pain the product solves (blog post, conference talk, podcast interview). This is the strongest signal available — the buyer has already publicly named the problem.

**Category B — usage / tool signals.**
- Uses a specific adjacent tool the founder's product integrates with or replaces (detectable via BuiltWith, Wappalyzer, GitHub search, StackShare, job-post keyword scraping).
- Has open-source infrastructure the product improves against (detectable via GitHub — repos that match a pattern, or usage of specific dependencies).
- Attends events / communities the founder participates in (attendee lists from past conferences, member lists from communities the founder is in).

**Category C — network / referral signals.**
- Referred by an existing customer.
- Second-degree LinkedIn connection to the founder or an early customer.
- Alumni-network overlap with the founder or team.

**Category D — firmographic signals (necessary but not sufficient at seed).**
- Matches the mod-104 Layer-1 firmographic ICP (company size, industry, geography, funding stage).

An account with only Category D signal is a machine-generated-list account and is deprioritised at seed. An account with Category A + Category D signal is a top-of-list account and warrants the deepest Level-3 personalisation. The list-building discipline pays off in reply rate directly: **hand-curated seed lists produce 10-25% reply rates on the top-tier signal-selected slice; machine-generated firmographic-only lists produce 1-3%**. The 5-10× reply rate difference is the difference between "outbound is producing meetings" and "outbound doesn't work for our market".

**Target list size at seed.** Working guidance: **100-300 accounts on the active list at any time.** Fewer than 100 and the founder runs out of accounts before the cadence produces enough meetings to validate; more than 300 and the personalisation quality collapses under the founder's capacity limit. Weekly cadence: add 10-30 new signal-selected accounts, retire 10-30 that completed the cadence without response (to the nurture list), keep the active list bounded.

### The sequence — cadence structure at seed scale

The seed-outbound cadence is *shorter and more personalised* than the mid-market Series-B cadence, because at seed the founder is writing every touch by hand and the top-of-tier accounts have already committed to seeing the outreach when the first email lands.

Working structure for a seed-outbound cadence (calibrated against Kazanjy, Josh Braun, Sam Blond, and Kellen Casebeer practitioner writing; adjust to the ICP and the response signals):

```
Touch 1 (Day 1) — Cold email #1 (deeply personalised opener, one clear ask)
Touch 2 (Day 3) — LinkedIn connection request (no message, or 1-line note)
Touch 3 (Day 6) — Cold email #2 (different angle, references touch 1 lightly)
Touch 4 (Day 10) — LinkedIn direct message (short, references the email thread)
Touch 5 (Day 14) — Cold email #3 (short, "am I reaching the right person?" or a specific reference to a new signal)
Touch 6 (Day 21) — Breakup email (short, professional close: "no follow-up if this isn't a priority now")
```

Six touches over three weeks. Not twelve touches over six weeks. The seed-outbound cadence is deliberately shorter because:

- The founder cannot sustain 12 personalised touches × 200 accounts / month = 2,400 hand-written touches monthly. Six touches × 100 accounts is 600 monthly — within the founder's capacity.
- A hand-personalised touch has a much higher chance of landing on touches 1-3 than a templated touch does; the diminishing returns on touches 4+ set in earlier at higher personalisation levels.
- The founder's time is more valuable to spend on responding to the meetings the first three touches produce than on grinding through touches 7-12 on non-responders.

**The three cold-email angles.** The three emails should attack the pain from three angles, not repeat the same pitch three times. Working angles (from the Josh Braun / Sam Blond practitioner writing):

- **Angle 1 — the pain framing.** Email 1 opens with the specific pain the founder believes the account has, references the signal that put them on the list, and asks a specific question that would confirm or deny the pain. Not "would you be interested in a demo"; a real question the answer to which the founder wants to know.
- **Angle 2 — the outcome framing.** Email 2 (touch 3) opens with the outcome the product produces for similar customers, references a specific case (customer name if permission granted; anonymised if not), and asks whether the outcome would matter to their team. Different reader-anchor than email 1.
- **Angle 3 — the reaching-the-right-person framing.** Email 3 (touch 5) is short and asks whether the recipient is the right person for the conversation, or whether there is someone else in the org better positioned to answer. This surfaces the champion / user / buyer separation (mod-104's buyer-user-champion split) and often produces the introduction rather than the direct meeting.

**The break clause.** Every cadence has an explicit final touch — a short professional close ("if this isn't a priority for you right now, no follow-up from me — happy to reconnect if things change"). Cadences without a break clause fatigue the account, hurt the founder's domain reputation, and produce diminishing marginal returns past touch 6. The break clause is not optional.

### Personalisation at seed scale — the ten-minute rule

At Series-B scale, personalisation is tiered because the SDR cannot afford Level-3 personalisation across a 500-account list. At seed scale the founder can afford Level-3 across the entire active list, provided she budgets **at most 8-12 minutes per touch on personalisation research + writing**. Below 8 minutes the personalisation is superficial ("noticed you're hiring — thought you might be interested in..."); above 12 minutes the founder's time constraint bites and volume collapses.

The 10-minute personalisation template — a scaffold, not a script:

1. **1 minute — pull up the account.** Website, blog, LinkedIn company page, GitHub org, most-recent 3 tweets or blog posts from the buyer or an adjacent team member. Look for what has changed or been announced in the last 90 days.
2. **2 minutes — identify the signal-hook.** The single specific thing you can reference that shows the account you are not blasting a template — a job post, a blog post, a talk they gave, a GitHub repo they open-sourced, a customer they onboarded, a funding round. The signal-hook is what turns "hi, I noticed your company" into "hi, I noticed you're hiring for a platform engineer to build a service catalogue and just open-sourced your CODEOWNERS enforcement tool".
3. **2 minutes — connect the signal to the pain.** One sentence that connects the signal-hook to the specific pain the founder believes the account has and the product addresses. "Hiring for a platform engineer and open-sourcing your CODEOWNERS tool suggests you're solving the ownership-drift problem in-house — that's the problem we built Loomly to solve for teams past 50 engineers."
4. **3 minutes — write the ask.** Short, specific, low-commitment. Not "book a demo"; more like "would a 15-minute call to compare notes with our approach be useful?" or "if useful, happy to send you the internal writeup on how we handle the four failure modes we've seen — reply and I'll send it over".
5. **1 minute — subject line + review + send.** Subject line references the signal-hook where possible ("re: your CODEOWNERS tool"); 3-second scan for tone; send.

Ten minutes per email × 100 emails / month × 3 emails per sequence = ~50 hours of founder time per month on outbound writing. Add LinkedIn touches (1-2 minutes each) and reply handling (~2 minutes per non-meeting reply, ~15 minutes per meeting booking), and the founder is at 60-80 hours/month on outbound at active list of 100. That is a real founder commitment (roughly 15-20 hours/week) and is inside the "founder-led outbound" minimum viable investment from Chapter 1.

### Response-rate expectations at seed scale

Seed-outbound response rates on a well-curated list with Level-3 personalisation dramatically outperform the templated-outbound benchmarks. Working ranges (calibrated against the practitioner data — working ranges, not laws; every ICP shifts them):

| Metric | Templated Series-B baseline (Level 1) | Templated Series-B mid-tier (Level 2) | Hand-personalised seed (Level 3, all touches) |
|---|---|---|---|
| **Open rate** | 30-50% | 30-50% | 45-65% |
| **Reply rate** | 1-3% | 3-8% | 8-20% |
| **Positive-reply rate** (of replies) | 20-30% | 25-40% | 40-60% |
| **Meeting-booked rate** (per touch) | 0.3-1% | 1-3% | 3-8% |
| **Meeting-held rate** (of booked) | 60-80% | 60-80% | 70-85% |

<!-- needs-research: pin response-rate benchmarks against current Outreach.io / SalesLoft / QuotaPath State of Sales reports or Kazanjy's Founding Sales published numbers; the ranges above are working practitioner defaults -->

Two facts to name from the table.

**Fact 1 — seed outbound is not "harder" than Series-B outbound; it is a different math.** The reply rate is *higher* than templated outbound because the personalisation is deeper and the list is signal-selected. The volume is much lower — 100 touches / week vs. 1,000+ — but the reply rate more than makes up for it in absolute meeting count.

**Fact 2 — the founder's reply-rate is a diagnostic on the ICP + positioning, not on the cadence.** If the founder's hand-personalised outbound is producing <5% reply rate on a well-curated signal-selected list, the failure is upstream — the ICP is wrong (mod-104), the positioning does not connect (mod-103), or the pain is not as acute as the founder believes. Fix the upstream problem before blaming the cadence. If the reply rate is 8-20% but the meeting-to-opportunity conversion is <30%, the ICP is right but the demo is not landing — fix mod-105 Chapter 4's demo before scaling outbound further.

### Cadence discipline — what to instrument at seed

At seed the founder is running the cadence in a spreadsheet or a lightweight CRM (HubSpot, Attio, Close, Airtable). Full Salesforce + Outreach + Apollo + Gong stack is over-investment; the founder needs to instrument only enough to answer the Chapter 2 four-gate diagnosis and to hand off the pattern-knowledge to the future SDR hire.

The minimum-viable instrumentation:

- **Account list** with signal-hook per account.
- **Touch log** per account (touch number, date, channel, subject-line variant if email, response state).
- **Reply state** — no response, positive-reply, negative-reply, meeting-booked, meeting-held, out-of-office, wrong-person, unsubscribe.
- **Opportunity linkage** — when a meeting produces an opportunity, link to the CRM record so first-touch attribution is preserved.
- **Weekly summary** — touches sent, opens (if tracked), replies, positive replies, meetings booked, meetings held. Rolling 4-week average to smooth noise.

The instrumentation stack does not require a cadence tool at seed. Gmail + a text-expander tool + a spreadsheet + HubSpot's free tier is sufficient for the first 3-6 months. Buying Outreach or SalesLoft *before* the founder has 3 months of hand-run outbound is over-investment — the tool encodes cadences the founder has not yet validated, adds configuration overhead, and produces a false confidence that the cadence is working because the tool is running.

The cadence tool is added when: (a) the founder has 3+ months of validated cadence data, and (b) the founder is hiring the first SDR to hand the cadence off to. The tool encodes what the founder learned; the founder does not learn from the tool.

### The transition — from founder-run outbound to the SDR-AE motion

The seed-outbound programme is not the endpoint; it is the *precursor* to the SDR-AE motion in mod-107 Chapter 3. The transition happens on the schedule mod-107 Chapter 3 lays out — but this chapter is where the transition is *earned*.

Six readiness signals (mod-107 Chapter 3 lists these against the founder-led-sales motion; they apply identically to the founder-run outbound motion):

- The founder has personally run outbound long enough to have **20-30 booked meetings from cold outbound**, at a reply rate consistent with the seed benchmarks above.
- The **reply-to-meeting and meeting-to-opportunity conversion rates are stable** — quarter-over-quarter consistency, not first-quarter novelty.
- The **cadence structure is written down** — a document that a stranger could read and run a passable version of tomorrow. Includes: target-account list criteria, signal-selection rules, six-touch cadence template with the three angle variants, personalisation scaffold, break-clause template, reply-handling scripts.
- The **objections the buyer raises** in reply are known and answered — the founder has heard the same 5-10 objections and has a defensible response to each.
- The **signal-selection criteria are characterised** — the founder can describe which signal-hook types produce the highest reply rate for this ICP and which are dead-ends; the SDR will inherit criteria, not build them blind.
- The founder has become the **bottleneck on capacity, not knowledge** — the calendar is fully absorbed by outbound writing + meeting execution; the constraint is her time, not her insight into what to write.

When all six signals are present, the founder hires the first SDR (per mod-107 Chapter 3's SDR-after-AE sequence — after the first AE is ramping, not before). The SDR inherits the target-account list, the cadence template, the signal-selection rules, the objection-and-response scripts. The founder shifts from cadence execution to cadence coaching + strategic-account hand-run + closing.

**When the transition should be delayed.** If one of the six signals is missing, the transition is premature — hiring the SDR produces a rep who cannot draw on the founder's un-transferred pattern knowledge and fails to reproduce the founder's reply rate. The delay is not a failure; it is protecting the SDR hire from being set up to fail. Extend the founder-run programme another quarter; re-check the six signals.

**What the transition changes in the cadence itself.** The SDR-run cadence looks more like mod-107 Chapter 3's 12-touch, tiered-personalisation structure than the seed 6-touch all-Level-3 cadence, because the SDR is running larger volume across a wider tier list. The seed cadence's Level-3 approach persists at the top-of-list tier (the SDR runs Level 3 on the top 50 accounts, matching what the founder was doing); Level 2 fills the middle 200; Level 1 covers the long tail. The founder retains the top-30 Level-3 tier for herself (or hands it to an AE, per mod-107 Chapter 3), because those accounts convert at the highest rate and the founder's touch produces the highest reply rate the org can generate.

## Concrete example — Loomly's Q1 outbound cadence

Loomly's Q1 portfolio (Chapter 1): primary = founder-led outbound; ACV band $12-24K; ICP = 50-150-engineer B2B SaaS on GitHub; buyer / user / champion = VP Eng / EM / platform engineer. Jane (founder) has just closed 22 deals from mod-105 founder-led sales and hired her first AE and first SDR (per mod-107 Chapter 3). At the seed-outbound → SDR-AE-transition boundary, Jane is running the seed-outbound motion herself for the top-30 tier while the SDR runs the mid-tier cadence.

**Step 1 — Build the target-account list.** Jane's active list is 220 accounts across four signal categories:

- **Category A (buying context, 60 accounts):** 40 recently funded (Series A/B in last 6 months, on Loomly's ICP profile); 20 hiring for a platform-engineer or SRE role visible on their careers page.
- **Category B (tool signal, 80 accounts):** 60 with public GitHub orgs matching the "monorepo-with-Terraform" pattern; 20 with public blog posts mentioning stale-service or CODEOWNERS-drift problems.
- **Category C (network, 40 accounts):** 25 referrals from existing customers; 15 second-degree LinkedIn connections through Jane's own network.
- **Category D-only (firmographic-only, 40 accounts):** these are the low-priority tail — 50-150-engineer B2B SaaS with GitHub presence but no other signal. Jane keeps these on the list at Level-2 personalisation only, and only if the higher-signal tiers are running out of accounts.

Signal-hook logged in HubSpot per account; total hand-curated additions per week: 15-25.

**Step 2 — Design the top-30 tier cadence (Jane runs).** Top 30 accounts by signal strength (all Category A + Category B combined). Jane runs the six-touch cadence with fully hand-written Level-3 personalisation per touch.

Touch 1 (Day 1) example, to a VP Eng at a Series-B DevOps company that just posted a "Head of Platform Engineering" role and open-sourced a CODEOWNERS-enforcement CLI:

> Subject: re: your CODEOWNERS enforcement tool
>
> Hi Mira,
>
> Saw you open-sourced `codeowners-check` last week and are hiring a Head of Platform Engineering to build out your service catalogue — congrats on the funding round.
>
> The pattern in your tool (enforcing CODEOWNERS at PR-time and failing the check when the entry is stale) is exactly the failure mode we built Loomly around at ~50-engineer B2B SaaS orgs. We've seen four ways this breaks at scale — the two that surprise most teams are (1) ownership-drift when a service's owning team is renamed, and (2) the CI-cost blow-up when the check runs on every PR against a monorepo.
>
> If it's useful, happy to send you our internal writeup on how our customers handle those two — reply and I'll send it over. If you'd rather talk it through, 15 minutes on my calendar here: [link]
>
> — Jane

Signal-hook: the open-sourced tool + the hiring signal + the recent funding. Ask: low-commitment (send-the-writeup, alternative to demo booking). No pitch of Loomly's features — the pitch is the shared expertise ("we've seen four ways this breaks").

Touch 3 (Day 6) — outcome-framing angle. Touch 5 (Day 14) — right-person-framing angle. Touch 6 (Day 21) — professional breakup.

**Step 3 — Design the mid-tier cadence (SDR runs).** 180 accounts across the mid-tier (Categories A + B without top-signal, and network). SDR runs a Level-2 templated cadence — the same six-touch shape but with the personalisation limited to signal-hook substitution rather than fully hand-written per email. Founder-authored templates for each of the three angles; SDR customises the signal-hook and the ask per account. ~5 minutes per email vs. Jane's 10.

**Step 4 — Instrument.** HubSpot dashboard tracks: touches/week per rep, reply rate, positive reply rate, meetings booked, meetings held, opportunities passed to AE, closed-won. Weekly Monday standup: Jane + AE + SDR review the week's numbers, discuss which signal-hooks produced highest reply rate, adjust the following week's list weighting.

**Step 5 — Q1 outcomes.** By end of Q1 (12 weeks, ~2,400 touches combined across Jane top-30 tier + SDR mid-tier):
- Top-30 tier (Jane): 30 accounts × 6 touches × ~3 cadence rotations = ~540 touches. Reply rate: 22% (67 replies). Positive-reply rate: 55% (37 positive replies). Meetings booked: 24. Meetings held: 20. Opportunities passed to AE: 12. Closed-won: 4 deals, $76K new ARR.
- Mid-tier (SDR + Jane oversight): 180 accounts × 6 touches × ~1.7 rotations = ~1,860 touches. Reply rate: 8% (149 replies). Positive-reply rate: 30% (45 positive replies). Meetings booked: 24. Meetings held: 19. Opportunities passed to AE: 11. Closed-won: 3 deals, $50K new ARR.
- Combined: 7 closed-won, $126K new ARR (matches Chapter 2's example).

**Step 6 — Diagnose (Chapter 2's four gates).** As Chapter 2 walked: the top-30 tier passes Gate 1 (ICP-fit) cleanly and Gate 4 (attribution) cleanly; Gate 2 (CAC) is contaminated by the small overall sample (Gate 3), and the correct decision is to extend the cadence another quarter before scaling to a second SDR.

**Step 7 — What Jane learns.** The 12 weeks produce specific, transferable knowledge:
- **Signal-hook ranking.** Category A funding-signal produces the highest reply rate (28%); Category B open-source-signal is second (24%); Category B hiring-signal is third (18%); Category C network is high (35%) but volume-limited. Category D-only is a dead-end (3% reply, no positive replies). SDR's next-quarter list weighting shifts accordingly.
- **Angle ranking.** The "shared-expertise" opening (touch 1, Angle 1 — pain framing) outperforms the "outcome-framing" opening (touch 3, Angle 2 — outcome framing) at 2× reply rate. Jane rewrites touch 3 to also lead with a shared-expertise anchor.
- **Objection catalogue.** Five objections recur in the replies: "we build this in-house"; "we're on GitLab, not GitHub"; "the pain is real but not a priority this quarter"; "the security review is a barrier"; "we use [competitor]". Jane writes response scripts for each; SDR inherits.
- **Break-clause responses.** ~15% of accounts that reach the breakup email reply — often positively ("actually, let's talk in Q2 when we have budget"). Break clause is retained.

All four of these become the pattern-knowledge that the SDR hire in Q2 (or the second SDR in Q3, per the Chapter 2 diagnosis) will inherit — inputs to the cadence document that mod-107 Chapter 3 assumes exists.

## Common failure patterns

- **Skip-founder-run-outbound trap.** Founder hires the SDR immediately, expecting the SDR to figure out the cadence, the list criteria, and the objection responses. SDR produces zero pipeline in six months. Fix: founder runs seed outbound for 3-9 months first; hire the SDR only after the six readiness signals are present.
- **Machine-generated-list trap.** Founder buys a 5,000-account Apollo export against firmographic filters; runs cadences against the whole list; reply rate is 0.4%; concludes "outbound doesn't work". Fix: hand-curated list of 100-300 accounts against signal-selection criteria; volume comes from reply rate, not touch count.
- **Templated-personalisation trap.** Founder uses a "personalisation token" template ("hi {{first_name}}, I noticed {{company_name}} is a {{industry}} company") — the personalisation is superficial; reply rate is 1-2%. Fix: real signal-hook per account; the personalisation names something specific the recipient did, not something the enrichment tool auto-filled.
- **12-touch-at-seed trap.** Founder runs 12-touch cadences at seed because the mid-market playbook does; cannot sustain the volume at Level-3 personalisation; touches 7-12 are visibly fatigued; recipients complain. Fix: 6 touches at seed; volume comes from list quality, not touch count.
- **No-break-clause trap.** Founder runs cadences without a defined final touch; accounts get emailed indefinitely; domain reputation degrades; deliverability collapses. Fix: every cadence has a professional close.
- **Single-angle-repetition trap.** Founder writes touches 1, 3, and 5 as three variants of the same pitch. Recipient sees the third variant as the same email again; reply rate does not increase with additional touches. Fix: three distinct angles (pain, outcome, right-person); each opens with a different reader-anchor.
- **Ask-a-demo-in-touch-one trap.** Founder opens touch 1 with "would you like to book a 30-minute demo?" — too high-commitment for a cold contact. Reply rate 0.5%. Fix: low-commitment ask in touch 1 (a specific question, a "send you the writeup" offer); demo ask escalates only after positive engagement.
- **Tool-before-motion trap.** Founder buys Outreach, Apollo, Gong, ZoomInfo in month 1 — $30K+/year of tooling — before running a single cadence. Configuration overhead consumes month 1; motion has not been validated when the second month begins. Fix: minimum-viable stack (Gmail + text-expander + spreadsheet + free HubSpot) for the first 3 months; upgrade tooling when the founder is validated and about to hand off to the SDR.
- **Founder-still-writing-past-hand-off trap.** Founder hires SDR, continues personally writing all touches — SDR has nothing to do. Fix: after hand-off, the SDR owns the mid-tier cadence fully; the founder retains only the top-30 tier and specific referral-tier accounts.
- **Discount-the-hand-personalised-numbers trap.** Founder sees 18% reply rate on Level-3 hand-personalised outbound; concludes "this only worked because I'm the founder". True — and *therefore* the SDR should inherit the same list-signal + template-angle discipline, not the same volume expectation. Fix: the SDR's Level-3 reply rate will be 60-80% of the founder's (still 10-15%); volume compensates for the delta.
- **Skip-the-cadence-document trap.** Founder runs outbound for 6 months, hires SDR, hands off "here's how I do it" verbally. SDR has no reference document; the pattern-knowledge does not transfer. Fix: cadence document (list criteria, template angles, signal-hook ranking, objection scripts) is written *before* the SDR arrives; it is the SDR's primary onboarding artifact.
- **Confuse-outbound-with-spam trap.** Founder mass-emails 2,000 contacts against a broad list; recipients report spam; the founder's domain reputation degrades. Fix: signal-selection + Level-3 personalisation + 100-300 active list. Outbound is not spam because the personalisation is real and the ask is aligned to a specific signal the recipient exhibited.
- **Reply-handling-latency trap.** Founder gets a positive reply Tuesday morning; responds Thursday afternoon; the account has cooled. Fix: reply-handling SLA is ≤4 business hours during the seed-outbound phase; the founder's calendar reserves reply-handling time daily.

## Summary

- Seed outbound is *not* Series-B outbound run smaller. It is the founder personally running a hand-curated, Level-3-personalised, shorter-cadence programme against a signal-selected 100-300 account list — inside the **Predictable Revenue** tradition but with three seed-scale modifications: **founder-as-first-SDR**, **hand-curated list**, and **deep-personalisation-across-all-touches**.
- **Target-account list is signal-selected, not firmographic-filtered.** Categories: (A) buying-context — funding, hiring, leadership change, public pain-signal; (B) tool signals — adjacent tools, GitHub presence, community participation; (C) network — referrals, second-degree connections; (D) firmographic — necessary but not sufficient.
- **List size at seed: 100-300 active accounts.** Fewer produces cadence-underrun; more collapses personalisation quality.
- **Six-touch cadence over three weeks**, three distinct angles (pain / outcome / right-person), each fully hand-written by the founder at Level-3 personalisation. Explicit break-clause on touch 6.
- **10-minute personalisation budget per touch** — 1 min pull-up + 2 min signal-hook + 2 min pain-connection + 3 min ask + 1 min subject/review/send. Below 8 min the personalisation is superficial; above 12 min the founder's volume collapses.
- **Reply rates at seed scale: 8-20% on hand-curated Level-3.** These are 5-10× the templated-outbound baselines — the numbers make outbound math work at seed even at 100-account list scale.
- **Sub-5% reply rate is a diagnostic on the ICP + positioning, not on the cadence.** Fix mod-104 or mod-103 before scaling outbound further.
- **Minimum-viable instrumentation at seed: Gmail + text-expander + spreadsheet + HubSpot free tier.** Full Outreach / Apollo / Gong stack is over-investment before the cadence is validated.
- **Six readiness signals for transition to the mod-107 Chapter 3 SDR-AE motion**: 20-30 booked meetings from cold outbound; stable reply and conversion rates; written cadence document; known-and-answered objections; characterised signal-selection criteria; capacity-not-knowledge bottleneck. All six present before hiring the SDR.
- **The SDR inherits the cadence document**, not the founder's brain. The document is what makes the transition producible; without it the SDR restarts from scratch and the pattern-knowledge is lost.
- **After transition**, the SDR runs the mid-tier Level-2 templated cadence; the founder retains the top-30 Level-3 tier + specific referral-tier accounts. Chapter 3's inbound motion feeds the top of the same funnel; Chapter 6's paid motion sits parallel with different attribution characteristics.
