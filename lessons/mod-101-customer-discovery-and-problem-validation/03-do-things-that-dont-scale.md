# Do Things That Don't Scale — Recruiting the First Ten

## Motivation

The IDEA-stage founder's most common recruiting failure is to reach for an *analytic* solution — post a survey, buy a research panel, wait for inbound — when the correct move is a *manual* one: **write to twenty people you can already reach, get on the phone with the ones who reply, and follow up personally.**

Paul Graham's essay *Do Things That Don't Scale* is the canonical statement of this discipline ([Graham 2013](https://paulgraham.com/ds.html)). His observation: startups fail to launch not because founders can't build, but because they wait for growth to happen on its own instead of doing the un-scalable manual work that gets the first users. The essay's most cited line is about Airbnb going door-to-door in New York re-shooting listing photos — the point is not the photos, it is that **the founders were the growth mechanism** until there was enough traction to justify a mechanism.

At the discovery stage, the un-scalable work is **recruiting and running the first ten interviews yourself, one at a time, by hand.** This chapter is about how to do it.

## Core concepts

### Why manual recruiting is the right first move

Three reasons the manual path beats the "scalable" path at n=10:

- **You do not know what you are looking for yet.** A survey requires you to have already picked the right questions. At n=10, half your questions will be wrong. A live conversation lets you follow the thread; a survey does not.
- **The recruiting process teaches you where your customer lives.** If the only way you can find your ICP is by asking your co-founder's friends, you have just learned that you do not yet have a real distribution channel — a fact that survey infrastructure hides from you.
- **The response rate on a personal ask from a founder is dramatically higher than the response rate on a cold survey link.** You are not scaling anything at this stage. You are learning. Manual scales just fine for ten.

### The five recruiting channels for the first ten

Rank-order these by ease and use them roughly in this order. The rule is: **exhaust each channel before moving to the next.**

1. **People you already know who fit the ICP.** Your former colleagues, your co-founder's network, ex-classmates. Fast, high-trust, easy to schedule. Bias risk (they may want to help you); mitigate by asking them past-tense behaviour questions from Chapter 2.
2. **Warm introductions from those first interviewees.** At the end of every interview, ask for two referrals ("who else do you know who runs invoicing like you do?"). This is how the first ring compounds to the second and third ring.
3. **Public communities where the ICP hangs out.** Slack groups, subreddits, industry forums, LinkedIn groups, Discord servers, conference Slacks. Post an ask in the community rules-compliant way — read the rules, ask a mod first, do not spam.
4. **Direct outreach to strangers who visibly fit the ICP.** LinkedIn Sales Navigator, GitHub profiles, conference speaker lists, podcast guest lists. A short, specific ask ("I'm researching X, would you spend 20 minutes on the phone next week?") converts surprisingly well when it is honestly a research ask, not a disguised sales pitch.
5. **Paid panels (only if 1–4 exhausted).** Services that recruit interviewees for a stipend (User Interviews, Respondent, and similar). Fast but expensive per unit and lower signal — you are paying strangers to talk to you and screening quality matters. Reserve for when you have exhausted the warmer channels or you need a specific hard-to-reach segment.

The order matters: **each channel down the list is cheaper on your reputation and more expensive on money or time.** Founders often invert this and start with paid panels because it feels less awkward than asking a friend — that is a symptom of not being willing to do the un-scalable thing.

### The interview ask itself

Whatever channel you use, the ask has the same shape. Keep it short.

> **Subject:** Research on [specific workflow] — 20 minutes?
>
> Hi [name],
>
> I'm researching how [ICP description — "high-volume freelance consultants" or "engineering managers at 50–200-person companies"] handle [specific workflow — "chasing late invoice payments" or "reviewing PRs across time zones"]. Not selling anything — I'm trying to understand what people actually do today.
>
> Would you spend 20 minutes on a call next week? Happy to work around your schedule. In return I'll share what I've learned across the other interviews — you'll get a preview of the pattern.
>
> — [Founder name]

Five properties this ask has and cheap variants do not:

- **Specific ICP language.** You are telling them why *they* were asked, not "we're doing research".
- **Specific workflow.** You are telling them what the conversation is about, so they can decline if it is not for them.
- **An explicit disclaimer that this is not a sales pitch.** This matters because your default social read is "founder + 20 minutes = pitch".
- **A specific time bound (20 minutes).** Open-ended time is scary; a bounded ask converts.
- **A concrete return** — you will share what you have learned. Most people will take a research call for free if you make the exchange feel two-sided.

### Handling the interview channel — phone, video, or in person

For the first ten, prefer **live voice over async**. Async written responses lose the follow-up-"why?" mechanic entirely.

- **In person** if you can — coffee, their office, a conference. Highest information. Rare unless you happen to be co-located with the ICP.
- **Video call** as the default. You can read their face, share a Figma sketch if you need to (solution interview only), and record for transcription with permission.
- **Phone** if that is what they prefer. Fine — you lose the face but keep the voice.
- **Written / async DM** as a fallback only. You will lose the ability to ask "why?" and the ability to hear hesitation. If you must use it, at least ask a single narrow question at a time.

**Always ask permission to record.** Say why — "so I can pay attention instead of taking notes" — and offer to send them the recording. Refusal is fine; take notes by hand instead.

### Following up personally

The un-scalable follow-up is as important as the un-scalable ask.

- **Send a personal thank-you within 24 hours.** Reference something specific they said. This is not a template.
- **Keep them in the loop.** When you ship an MVP, send a personal note; when you make a decision based on their input, tell them. These become your first design partners.
- **Ask for the referral again.** Not on the same email as the thank-you — separately, a week later, when you have a specific ask.

At n=10, following up personally with ten people costs less than an hour a week. At n=100 it is a job. That is fine — by n=100 you have earned the right to a scalable system.

### When to stop

The un-scalable phase ends when **the signal from your next interview is no longer moving your beliefs.** This is the practical operationalisation of Blank's rule from Chapter 1: *once you can predict what the next problem interview will say, move on.*

Concretely, three exit criteria — any one of them is enough to move to the next stage:

1. **Predictive saturation.** Before the interview, you can write down what they will say about the current-state workflow, the top pain, and the workaround, and after the interview you were right on all three. That means you have the pattern.
2. **You have your first ten paying-adjacent commitments.** Ten people who have said yes to something real — a design-partner LOI, a pre-order, a paid pilot, a scheduled hands-on prototype session. These become the seed of Customer Validation (Blank's second step, covered in mod-105).
3. **You have exhausted the ICP within reach and are getting no signal.** This is a bad-news exit — it means the segment you can reach does not have the problem you thought they had. Re-select the segment (a mini-pivot inside the loop) and restart, or re-examine whether the problem exists at all.

**Do not** stop because you are tired of manual work. That is a signal to push through, not to stop.

## Concrete example — the first ten in practice

A founder building a code-review tool for engineering managers at 50–200-person companies:

- **Week 1.** Lists 15 people in her personal network who fit the ICP (former colleagues who are now EMs). Sends the ask email to all 15. 8 reply, 6 schedule for the following week.
- **Week 2.** Runs the 6 interviews. Follows up personally with a thank-you and a specific ask for referrals; 4 of the 6 refer at least one person. Now has 5 warm-intro leads for week 3.
- **Week 3.** Runs 4 of those 5 interviews. Also posts in an engineering-leadership Slack she is a member of ("would love 20 min with EMs at 50–200-person companies about their PR review workflow — DM me"). 3 people DM her; she schedules 2 more.
- **Week 4.** Runs the remaining 2 interviews. Total: 12 interviews in 4 weeks, all from personal network + one warm-community post. Zero paid panel spend.

By interview 10 she noticed the same top complaint in every conversation ("PR reviews are async and time-zone-sensitive; nobody is accountable for the review latency"). By interview 12 she could predict what the next EM would say about it. **That is her signal to move to solution interviews.**

## Common failure patterns

- **Waiting for a landing page to convert cold traffic.** You have not shipped anything yet. There is no traffic. Cold-traffic waiting is a form of not-doing-the-work.
- **Reaching for the paid panel first.** Symptom of not being willing to ask friends. Costs money and gets you strangers with lower signal.
- **Never asking for referrals.** Skips the compound that turns 10 interviews into 25 in a month.
- **Interviewing anyone who will talk to you.** If they do not fit the ICP, the interview does not count. Screen the recruit — one clarifying question before you schedule ("just to confirm — you are running 30+ invoices a month, is that right?") saves a wasted hour.
- **Refusing to move on once you have the pattern.** The mirror of the previous chapter's "problem-interview infinity loop" — once the next interview stops moving your beliefs, you are procrastinating.

## Summary

- The IDEA-stage default is **do the un-scalable thing** ([Graham 2013](https://paulgraham.com/ds.html)). At n=10, manual recruiting beats scalable systems on speed, cost, signal, and side-effect learning.
- Recruit in order: **personal network → warm referrals → communities → cold direct outreach → paid panels.** Exhaust each before moving down.
- Keep the ask short, specific, honestly non-sales, time-bounded, and with a concrete return.
- Prefer **live voice** over async; ask permission to record.
- Follow up personally. Ask for referrals every time.
- Exit when your beliefs stop moving, when you have ten real commitments, or when you have exhausted the reachable ICP with no signal.
