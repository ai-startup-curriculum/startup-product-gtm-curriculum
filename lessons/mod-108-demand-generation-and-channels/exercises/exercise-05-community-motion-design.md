# Exercise 05 — Community Motion Design

**Estimated time:** 3 hours
**Chapter link:** [`05-community-motion-design.md`](../05-community-motion-design.md)
**Prerequisite:** Chapter 5 read end-to-end; Exercise 01 completed (a portfolio that names community as either the primary, the experimental, or the explicitly-deferred-to-mod-109 slot — if deferred, run this exercise as the *early-adopter cohort* design that is still compatible with seed stage); a mod-104 ICP scorecard; a mod-105 founder-led-sales pack (the first 10-30 customers are the recruitment pool for the cohort); a mod-109 retention outline if available (community's primary business outcome is retention, and the exercise's Signal-4 cohort-tagging feeds mod-109).

## Problem statement

Chapter 5 named the community motion as a business function with specific SPACES outcomes (Spinks) and specific operating conditions (Wenger — shared domain, community, practice). It distinguished the **four sub-motions** — early-adopter cohort, community-led content, developer relations, event-led — because each has a different time-to-signal window, different critical-mass threshold, and different failure mode. It named the **four instrumentation signals** — active-member ratio, reply-to-post ratio, sourced-revenue attribution, retention delta — that separate a working community from an empty room, and the **vanity metrics to reject** (total member count, follower count, RSVP count). And it named the three structural reasons community is the slowest to seed (critical-mass, trust-building, founder-participation-rhythm) and the one reason it is the strongest to retain (switching cost is social).

The failure mode: the founder spins up a Slack with no sub-motion named, no SPACES outcome specified, no founder-participation rhythm scheduled, and no instrumentation. Twelve weeks later the Slack has 60 members, 2 posts in the last 30 days, no reply-to-post ratio, and the founder concludes "community doesn't work for our market" — when in fact no community was ever designed.

This exercise trains you to **design a working seed-stage community motion** — pick the specific sub-motion (default: early-adopter cohort), name the SPACES outcomes it is designed against, write the founder's weekly / monthly / quarterly / annual cadence, pick the platform, name the four instrumentation signals and their targets, draft the first six weeks of anchor posts and office-hour agendas, and commit the decision to a one-page community operating document the shape Chapter 5's Loomly example implies.

The failure mode this exercise exists to catch: **the founder opens a Slack, invites 40 people, posts three times, then goes quiet for six months — because the community motion was never designed, only started.** The specific countermeasure: a written sub-motion choice + SPACES outcomes + founder cadence + instrumentation + first-six-weeks content plan, committed before the Slack / Discord / Discourse workspace is provisioned.

## Requirements

Deliver a folder `exercise-05/` with five files:

- `part-a-sub-motion-and-spaces.md` — the sub-motion choice + SPACES outcomes + why-not-the-other-three.
- `part-b-platform-and-recruitment.md` — the platform decision + the cohort recruitment plan (or the member recruitment plan for a public sub-motion).
- `part-c-operating-cadence.md` — the founder's weekly / monthly / quarterly / annual cadence.
- `part-d-instrumentation.md` — the four signals + their targets + the review rhythm.
- `part-e-operating-document.md` — the one-page community operating document + first six weeks of anchor posts.

### Part A — Sub-motion choice + SPACES outcomes (30 min)

Deliver `part-a-sub-motion-and-spaces.md`.

**A1 — Pick the sub-motion (10 min).** Chapter 5's four sub-motions are **(1) early-adopter cohort**, **(2) community-led content**, **(3) developer relations (DevRel)**, **(4) event-led**. For a seed-stage startup the **default is sub-motion 1 (early-adopter cohort)** unless the product is DevRel-native (an SDK, API, or developer-tool-first product sold to individual developers or platform teams). State:

- The sub-motion you are designing (one of the four).
- Why this one and not the other three — three sentences each explaining why the other three are deferred, rejected, or inappropriate at seed.
- If you are deviating from the default (picking sub-motion 2, 3, or 4 at seed), name the DevRel-native condition or the equivalent justification. Deviations without justification are the "wrong-sub-motion trap" from Chapter 5.

**A2 — SPACES outcomes (15 min).** Chapter 5 (via Spinks) names six SPACES outcomes a community can produce: **Support, Product, Acquisition, Contribution, Engagement, Success**. A community designed against all six produces none well. Pick **one primary and one secondary SPACES outcome** this community will be designed against. For each:

- Name the outcome (one of the six).
- Describe in 2-3 sentences what producing this outcome looks like in your product's context (specific artifacts, specific behaviours, specific business lift).
- Name the measurement signal from Part D that will prove it is firing.

The default pairing for an early-adopter cohort at seed is **Product + Success** (feedback loop + customer outcomes), with Acquisition (referrals) as a bonus; the default pairing for sub-motion 2 is **Contribution + Acquisition**; for DevRel it is **Acquisition + Contribution**; for event-led it is **Acquisition + Engagement**. If your pairing deviates from these defaults, explain why.

**A3 — Explicit non-outcomes (5 min).** Name the SPACES outcomes this community is explicitly **not** designed to produce at seed, with one sentence each on why. The common seed mistake is "support" — founders expect community to do product support, discover it is not optimised for it, and conclude the community is failing. A seed-stage early-adopter cohort may happen to produce support as a side effect, but should not be designed against it.

### Part B — Platform decision + recruitment plan (30 min)

Deliver `part-b-platform-and-recruitment.md`.

**B1 — Platform decision (10 min).** Match the platform to the sub-motion per Chapter 5's rules:

- **Cohort → Slack** (chat; small group; existing relationships; informal).
- **Community-led content → forum (Discourse / Circle / Bettermode)** (long-lived threads; searchability; slower pace).
- **DevRel → Discord** (developer-accepted; voice channels; threaded structure).
- **Open public community → subreddit** (free; discoverable; sacrifices control).
- **Support-adjacent → GitHub Discussions** (repo-integrated; poor conversational UX for community-of-practice).

Name the platform you are choosing and 2-3 sentences on why that platform's shape matches your sub-motion. If you are choosing Slack for a sub-motion 2 content-community (common mistake per Chapter 5), name the reason — and expect to migrate to a forum within 12 months.

**B2 — Recruitment plan (20 min).** Different sub-motions need different recruitment plans.

- **For an early-adopter cohort (sub-motion 1):** list 15-30 named customers / design-partners / high-engagement users you will invite. For each: who they are (role + company), why you are inviting them (depth of usage, strategic fit, willingness to engage), and what you expect them to contribute (feedback, case-study material, referrals). The recruitment is **named and personal**, not an open invite link.
- **For a public community (sub-motion 2 or 3):** name the seed-member strategy — the first 50-100 members who will set the community's tone. Where will they come from (existing customers, personal network, speakers at adjacent events, authors of adjacent open-source projects)? What is the one-sentence pitch for joining? What is the invitation mechanism (personal DM, newsletter announcement, speaker-at-event hand-off)?
- **For an event-led sub-motion (sub-motion 4):** name the first three events (owned or sponsored), the format of each (meetup / workshop / conference talk), and the audience target. Events do not have "members" in the same way; the recruitment is attendance-at-first-event + follow-up conversion to the broader community.

In every case: name the **target size at week 12** (floor and ceiling). For a cohort: 15-30 active members. For a public sub-motion 2 community: 50-150 members at week 12 (critical mass is 50 active minimum per Chapter 5). For a DevRel programme: 3-5 artifacts shipped + a Discord with 100+ members. For event-led: first owned event completed with 20-50 attendees, or 2-3 sponsored-event talks delivered.

### Part C — Operating cadence (45 min)

Deliver `part-c-operating-cadence.md`. Chapter 5's four cadence elements are **weekly / monthly / quarterly / annual**. Design all four.

**C1 — Weekly rhythm (15 min).** For the sub-motion you picked, write the founder's weekly commitment. Working defaults from Chapter 5:

- **Cohort weekly rhythm:** (a) 60-minute office-hours session on a persistent weekday / time (e.g., Wednesday 3pm ET), video-based, open to any cohort member; (b) one weekly "anchor post" — a substantive question or thought-piece from the founder that invites member response; (c) 3-5 direct-message check-ins per week with specific cohort members. Total time: ~5 hours/week.
- **Public community weekly rhythm:** 30-60 minutes posting on relevant conversations (member questions, ecosystem news); 1 monthly "founder AMA" or "roadmap session" (schedule in C2 below); event participation as opportunities arise.
- **DevRel weekly rhythm:** 1 tutorial or sample app or SDK improvement shipped per 2-3 weeks; Discord presence 30 min/day; 1 external talk / workshop / podcast per month.
- **Event-led weekly rhythm:** rotates with event calendar — pre-event prep, event delivery, post-event follow-up.

For each weekly element, name:
- **Day + time** (unmissable, same slot every week).
- **Duration** (actual hours — be honest about the sustainable commitment).
- **Format** (video call / written post / DM).
- **Backup rule** — what happens if the founder is sick, travelling, or in a board meeting? (Default: notify the community a week in advance; move the slot or run it async; do not skip silently.)

The **sustained-not-sporadic** rule from Chapter 5: 5 hours/week every week for 12 months beats 15 hours/week for 8 weeks followed by 4 months of silence. Pick a volume you can sustain.

**C2 — Monthly ritual (10 min).** Pick one or two recurring monthly events:

- **Roadmap transparency post** — a 3-paragraph writeup of what shipped last month, what is coming next month, what got de-prioritised. First-of-the-month default.
- **Member spotlight thread** — highlight a member's usage story (with permission), with a specific question that invites others to share theirs.
- **Monthly community call** — webinar-format Zoom, 45 minutes, one specific topic, recorded and posted back to the community.
- **Monthly "what's shipping" demo** — short live-demo of new product capabilities to the cohort.

Pick 1-2 that fit the sub-motion. For each: specific day of the month, format, time commitment, who runs it.

**C3 — Quarterly moment (10 min).** Larger event once a quarter. Working defaults:

- A virtual half-day summit or workshop series.
- An in-person regional meetup where customer density exists.
- A case-study release ("how three customers implemented X") with cohort member spotlights.

Pick one. Specify format, target attendance, prep lead time, cost (rough), who presents / hosts.

**C4 — Annual moment (10 min).** The calendar anchor. Working defaults:

- A small company-hosted annual conference / summit (physical or virtual).
- An offsite for the most active cohort members (5-15 people, 1-2 days).
- An annual-awards or recognition moment (community MVPs, top contributors) tied to a company-wide product release.

Pick one. Name the date (quarter + target month), the format, the attendance target, and what you want members to remember about it 12 months later. The annual moment is what generates the case-study and word-of-mouth material for the following year.

### Part D — Instrumentation (30 min)

Deliver `part-d-instrumentation.md`. Chapter 5's four signals + their targets.

**D1 — Reproduce the four signals and their targets (10 min).** For each signal, write: definition + measurement source + target at week 12 and week 24 + what the signal tells you (health / peer-to-peer / business / retention).

| # | Signal | Definition | Source | Target wk 12 | Target wk 24 | What it tells you |
|---|---|---|---|---|---|---|
| 1 | **Active-member ratio** | % of registered members who posted in last 30 days | Platform analytics | 20-40% (cohort) OR 5-15% (public) | same | Community health; <5% = empty room |
| 2 | **Reply-to-post ratio** | % of member-authored posts that get a non-founder / non-employee reply within 24h | Platform analytics / manual review | >50% | >60% | Peer-to-peer condition; <30% = broadcast channel |
| 3 | **Sourced-revenue attribution** | New-logo revenue first-touched (or community-member tagged) through the community | CRM + community-member tag | — (early signal only) | at least 1-2 closed deals attributable | Business outcome; validates the community has acquisition SPACES |
| 4 | **Retention delta** | 12-month logo retention of community-member cohort minus non-member cohort | CRM cohort analysis | Not meaningful yet | +5-15 pp | Retention outcome; validates the community has Engagement / Success SPACES |

Adjust the targets to the sub-motion. For a cohort: Signal 1 target is 20-40% (fewer lurkers); Signal 4 is not meaningful until the cohort has 6+ months of tenure. For a public sub-motion 2 community: Signal 1 target is 5-15%; Signal 4 is the primary end-state measure that matures at 18-24 months.

**D2 — Vanity metrics to explicitly reject (5 min).** From Chapter 5: total registered members, total lifetime messages, follower count, RSVP count. Name each one and the one-sentence reason it is not the primary metric for your community. If any of these appears on an internal dashboard, it has a "leading indicator only" annotation beside it.

**D3 — Community-member tag + CRM integration (10 min).** The load-bearing instrumentation. Specify:

- The CRM field: `community_member: boolean` on the Account or Contact object (name the specific object).
- The populating mechanism: when a known email is active in the community in a given 30-day window, the flag is set true; when inactive for 90 days, the flag is set false. Specify the sync frequency (manual weekly, Zapier, API).
- The reporting view: a saved CRM report that shows the community-member cohort's revenue, retention, and expansion vs. the non-member control, same period, same firmographic filter.
- The dashboard surface: where this report lives (HubSpot, Attio, Salesforce, Looker, spreadsheet) and who reviews it (founder weekly, GTM lead monthly).

**D4 — Review rhythm (5 min).** Who looks at the four signals, how often, and what triggers an action?

- Weekly: founder looks at Signals 1 and 2 (active-member ratio + reply-to-post ratio). If either goes below the floor for two consecutive weeks, flag as "community-health incident" and investigate.
- Monthly: founder looks at Signal 3 (sourced revenue attribution) + the trend on Signals 1 and 2.
- Quarterly: four-gate diagnosis on the community motion (Chapter 2 + Chapter 7). Signal 4 (retention delta) reviewed starting Q3 of the community's life, once a cohort has enough tenure to measure.

### Part E — Operating document + first six weeks of anchor posts (45 min)

Deliver `part-e-operating-document.md`.

**E1 — One-page operating document (30 min).** Write the artifact a VP-Community or future Head of Community inherits. Structure:

```
# Community Operating Document — {product} — {version, date}

## Sub-motion
- {sub-motion 1/2/3/4}
- Rationale: {why this one, from Part A1}

## SPACES outcomes
- Primary: {outcome, from Part A2}
- Secondary: {outcome, from Part A2}
- Explicitly not-outcomes: {from Part A3}

## Platform
- {Slack / Discord / Discourse / Circle / Reddit / GitHub}
- Workspace / server / forum URL: {TBD at launch}
- Rationale: {from Part B1}

## Membership
- Target composition: {who is in the room — specific profile}
- Target size at week 12: {range}
- Recruitment mechanism: {from Part B2}
- Entry criterion: {how members are vetted or invited; invitation-only vs. open}

## Operating cadence
- Weekly: {office hours day + time; anchor post day; DM check-ins}
- Monthly: {ritual + day + format + owner}
- Quarterly: {event + target quarter + format + attendance target}
- Annual: {anchor event + target month + attendance target}

## Founder commitment
- Hours/week for first 12 months: {sustainable number — 5-10 for cohort, 7-12 for public}
- Backup rule: {how absence is handled; no silent skips}
- Hand-off criteria: {when a Head of Community takes over primary ownership}

## Instrumentation
- Signal 1 — active-member ratio: target {X%}; measured {weekly}; source {platform analytics}
- Signal 2 — reply-to-post ratio: target {X%}; measured {weekly}; source {manual review or platform}
- Signal 3 — sourced revenue: target {at least N closed deals/quarter attributable}; measured {monthly}; source {CRM + community_member tag}
- Signal 4 — retention delta: target {+X pp at 12mo}; measured {quarterly starting Q3 of community life}; source {CRM cohort analysis}
- Vanity metrics to reject: {list}

## Review rhythm
- Weekly: {who looks at what}
- Monthly: {who looks at what}
- Quarterly: {four-gate diagnosis slot}

## Common failure patterns to avoid
- {3-5 of the Chapter 5 traps most relevant to this community design, with the fix beside each}

## Version history
- v1 — {date} — {author} — {summary}
```

**E2 — First six weeks of anchor posts (15 min).** Draft the first six weekly anchor posts the founder will publish. For each week:

- **Week** (1-6).
- **Topic / theme** (specific question or thought-piece).
- **Opening line** (hook — the first sentence members will see).
- **Expected member response shape** (what question / contribution / artifact are you inviting?).
- **Fallback** — if the post gets zero replies in 24 hours, what is the founder's follow-up (a specific DM to 2-3 members asking what they think; a related sub-question posted a day later; a direct ask of the quietest active cohort members)?

The first six anchor posts set the tone. Posts that read like company announcements train the community to be a broadcast surface; posts that read like genuine questions from a peer-expert train it to be a community of practice. Chapter 5's rule: ratio of founder-posts to member-posts should be 1:5 or lower in a healthy community — the anchor posts are the founder's share.

## Starter guidance

- **Pick one sub-motion. Do not try to run two.** Chapter 5's Loomly example launches sub-motion 1 at seed and defers sub-motion 2 to Series A, intentionally. A seed-stage founder trying to run cohort + public community + DevRel + events at once produces four undercapitalised motions and no critical mass on any.
- **Default to the early-adopter cohort unless the product is DevRel-native.** The cohort is the fastest to signal (2-6 months), the highest-value feedback loop at pre-PMF and immediately post-PMF, and the recruitment pool is already identifiable (the first 10-30 customers from mod-105). Public sub-motions have 12-24 month windows and critical-mass conditions that are not realistic to build before PMF.
- **Name a specific SPACES pair. Do not list all six.** A community designed against all six SPACES outcomes is a community designed against none — the operating decisions (platform, cadence, instrumentation) differ depending on whether you are optimising for Product + Success or Contribution + Acquisition. Pick two; design against two.
- **Sustained-not-sporadic beats intensive-then-silent.** 5 hours/week every week for 12 months is the trust-building floor. 20 hours/week for 8 weeks followed by 2 months of silence breaks the founder-participation condition and the community's tone does not recover. Pick a volume you can sustain unfailingly.
- **Office-hours on a persistent slot is the single highest-leverage ritual.** A recurring Wednesday 3pm ET Zoom that runs every Wednesday for 18 straight months is what the trust-building condition rests on. Office hours that move around the calendar, get cancelled when the founder is busy, or get downgraded to "we'll do them when I have time" are not office hours — they are a founder's calendar.
- **Instrument before you launch, not after.** Signals 1-4 are hard to backfill if the community-member CRM tag was not populated from day one. Part D's instrumentation plan is a precondition for the launch, not an afterthought. If the CRM integration is not ready, delay the launch by two weeks and get it ready.
- **Match the platform to the sub-motion.** The most common and most expensive community mistake is "we chose Slack because that's what we use internally" and then wanting a long-lived content archive 12 months later. Slack is for cohorts; forums are for content-community archives; Discord is for DevRel. Choose at launch; migration is painful.
- **The 12-month window is a fact, not a challenge.** Public sub-motions do not fire measurable business outcomes before month 12. If the community is on the "not now" list through Series A, that is a defensible decision; what is not defensible is running a public community for 8 months, calling it a failure, and killing it before the trust-building condition could have fired.
- **Do not hire a community manager in month 2.** The founder is the community's primary voice for the first 12-18 months. A community manager scales the operations *after* the founder's participation has established the tone. Hiring too early substitutes the manager's voice for the founder's, members lose the reason they joined, and the community atrophies.
- **Retention delta is the end-state metric; do not measure it too early.** Signal 4 is the business-defensible outcome at the quarterly and annual cadence, but it is not measurable at week 12 — the cohort has not been in the community long enough. Report it starting at month 6 of the community's life, with full confidence at month 12.
- **Do not confuse your Twitter presence with your community.** Founder-presence on someone else's platform (Twitter, industry Slacks, CNCF Slack) is a form of inbound / content (Chapter 3), not a community motion. An owned community exists because of the company and has founder-defined norms.

## Acceptance criteria

Your submission is complete when:

- [ ] Part A picks a specific sub-motion (one of the four) and justifies why not the other three in 2-3 sentences each.
- [ ] Part A names a primary + secondary SPACES outcome pair and the specific business-lift signal each produces; names 1-2 explicit non-outcomes.
- [ ] Part B matches the platform to the sub-motion per Chapter 5's rules (or justifies the deviation).
- [ ] Part B specifies the recruitment mechanism — for a cohort: a named 15-30 person list with role / company / why / expected contribution; for a public sub-motion: a seed-member strategy for the first 50-100 members.
- [ ] Part B specifies the target community size at week 12 (floor and ceiling) consistent with the sub-motion's critical-mass requirements.
- [ ] Part C writes the founder's weekly rhythm with specific day / time / duration / format, honestly sustainable, with a backup rule.
- [ ] Part C writes 1-2 monthly rituals, a quarterly moment, and an annual moment, each with format + target + owner.
- [ ] Part D reproduces the four instrumentation signals with definitions, sources, and week-12 / week-24 targets adjusted for the sub-motion.
- [ ] Part D names the vanity metrics to reject (total members, lifetime messages, follower count, RSVP count) with a one-sentence reason each.
- [ ] Part D specifies the `community_member` CRM tag mechanism (populating, sync frequency, saved report, dashboard surface, review rhythm).
- [ ] Part E writes the one-page operating document in the structured format (sub-motion / SPACES / platform / membership / cadence / founder commitment / instrumentation / review rhythm / failure patterns / version history).
- [ ] Part E drafts the first six weeks of anchor posts (week + topic + opening line + expected response shape + fallback) that read like peer-questions, not company announcements.
- [ ] Any factual claim (a specific critical-mass threshold not matching Chapter 5's defaults, a specific retention-delta benchmark, a specific attendance target) that is not cited to Chapter 5 or a practitioner reference is flagged `<!-- needs-research: ... -->`.

## Common ways this exercise goes wrong

- **No-sub-motion trap.** Part A says "we are doing community" without picking one of the four. The operating decisions in Parts B-E are then internally contradictory (Slack platform + content-archive expectations; cohort recruitment + public-community critical-mass targets). Fix: name sub-motion 1, 2, 3, or 4 explicitly before Part B.
- **All-six-SPACES trap.** Part A2 lists all six SPACES outcomes as "we expect the community to produce". The operating decisions optimise for none. Fix: pick exactly two — primary + secondary — and name the explicit non-outcomes.
- **Slack-for-everything trap.** Part B1 chooses Slack regardless of sub-motion. If the sub-motion is community-led content, the 12-month archive value is unsearchable; migration to Discourse will be forced in year 2. Fix: match the platform to the sub-motion (cohort → Slack; content → forum; DevRel → Discord).
- **Open-invite-link trap.** Part B2's recruitment plan is "we'll share a Slack invite link in our newsletter" with no named recruitment list. For a cohort, this is wrong (cohort recruitment is named and personal). For a public sub-motion, it is incomplete (the first 50-100 members set the tone and need to be hand-recruited, not sourced from an open link). Fix: name the recruitment mechanism specifically for the sub-motion.
- **Unsustainable-cadence trap.** Part C commits to 20 hours/week of founder time on the community. Three weeks in, the founder cannot sustain it, cadence degrades to 2 hours/week, trust condition does not build. Fix: pick a volume you can honestly sustain for 12 months (5-10 hours/week for a cohort; 7-12 for a public community); schedule the backup rule for the weeks you cannot run.
- **Movable-office-hours trap.** Part C's weekly rhythm says "office hours when I have time" or "monthly roadmap post approximately". The persistent-slot discipline (Chapter 5) is what builds the member-expectation. Fix: specific day + time + "unmissable except as per the backup rule".
- **No-anchor-posts trap.** Part E does not draft the first six anchor posts. Founder launches the community with no content pipeline, posts nothing in the first week, members (who were just invited) see an empty room, engagement does not start. Fix: six weeks of anchor posts drafted and queued before the community launches.
- **Announcement-posts trap.** The six anchor posts in Part E read like company announcements ("v2.3 is out!", "we raised a Series A!", "new feature shipped"). Trains the community to be a broadcast channel. Fix: founder-posts are questions / thought-pieces that invite member response, not announcements.
- **No-instrumentation trap.** Part D is a paragraph of intent ("we'll track engagement") with no CRM tag, no saved report, no measurement cadence. Twelve months later the founder cannot defend community ROI in a board pack. Fix: `community_member` CRM tag + saved report + review rhythm specified before launch.
- **Vanity-metric trap.** Part D's primary metric is "total members" (currently 820, hooray). Zero signal on health, peer-to-peer, revenue, or retention. Fix: the four signals from Chapter 5 are the primary metrics; total members is a leading indicator, not an outcome.
- **Kill-before-12-months trap.** Operating document says "we'll evaluate the community at month 6 and kill it if it's not working". For a public sub-motion (2, 3, or 4), 6 months is diagnostic-invisible — the trust-building and critical-mass conditions have not fired. Fix: evaluation window matches the sub-motion's time-to-signal (2-6 mo for cohort; 12-24 mo for public).
- **Confuse-founder-presence-with-owned-community trap.** The exercise describes the founder's Twitter activity, participation in CNCF Slack, and conference talks as "our community motion". That is a form of inbound / content, not community. Fix: an owned community has a defined platform, member list, cadence, and norms; founder presence elsewhere is Chapter 3 territory.
- **Hire-a-community-manager-at-month-2 trap.** The operating document hands primary voice to a hired community manager in the first quarter. Founder's voice disappears; members lose the anchor; community atrophies. Fix: founder is the primary voice for 12-18 months; a Head of Community takes over primary ownership once the tone is set and the cadence is sustaining.
- **Support-desk-in-disguise trap.** The exercise's SPACES primary is "Support" (peer help) and the Slack channel structure is bug-reports / feature-requests / help. The community becomes a product-support surface; peer-to-peer conversation is near zero; Signal 2 (reply-to-post ratio with non-founder replies) collapses. Fix: Support is explicitly a non-outcome at seed per Chapter 5's rule; design against Product + Success + Acquisition for a cohort or Contribution + Acquisition for a public community.
