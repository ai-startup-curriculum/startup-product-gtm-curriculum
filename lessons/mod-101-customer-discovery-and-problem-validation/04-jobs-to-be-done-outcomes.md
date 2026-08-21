# Jobs-to-be-Done — Outcomes That Reject Solutions

## Motivation

After you have run twenty problem interviews, you will have twenty transcripts of things people said. What you will *not* have — unless you impose a vocabulary — is a **testable list**. You will have "people are frustrated" and "they use a spreadsheet" and "they'd like it to be faster". You will not have a set of statements that let you look at a proposed solution and ask: *does this satisfy an outcome our interviewees said was important, and are they currently underserved on it?*

Jobs-to-be-Done (JTBD) is the vocabulary that gives you that testable list. It comes from two overlapping traditions:

- **Anthony Ulwick's Outcome-Driven Innovation (ODI)** — a highly structured version that produces literal outcome statements you can measure ([Strategyn — ODI overview](https://strategyn.com/jobs-to-be-done/); [Ulwick's HBR article "Turn Customer Input into Innovation" (2002)](https://hbr.org/2002/01/turn-customer-input-into-innovation)).
- **Clayton Christensen's Milkshake / Forces-of-Progress framing** — a narrative version popularised by Christensen and his co-author Bob Moesta ([Christensen — HBR "Know Your Customers' Jobs to Be Done" (2016)](https://hbr.org/2016/09/know-your-customers-jobs-to-be-done); [Christensen — *Competing Against Luck* (2016)](https://www.claytonchristensen.com/books/competing-against-luck/)).

Both traditions share the same central move: **the customer is not buying a product; they are hiring it to do a job.** A job has a functional dimension (get me somewhere) and often emotional / social dimensions (feel competent, look responsible to my team). The job is stable — how it gets done changes. Nokia's job (stay in touch with people) is the same as WhatsApp's; the product that gets hired changed.

This chapter teaches you to translate a discovery corpus into (a) a list of jobs, (b) a set of forces acting on the customer, and (c) a set of outcome statements — and to use those outcomes to reject solutions that do not serve them.

## Core concepts

### The job statement — Christensen's shape

Christensen's canonical job statement has three parts: **a situation**, **a motivation**, and **an expected outcome**. The template:

> When _[situation]_, I want to _[motivation / job]_, so I can _[expected outcome]_.

Example (from a code-review-tool discovery):

> **When** an engineer has been waiting more than a day for a PR review, **I want to** know who is accountable for the review latency, **so I can** either escalate to them or reassign the reviewer without becoming the person who nags.

That statement has three properties useful downstream:

- It is **product-agnostic.** It does not name a technology or a solution shape. Any of ten different products could hire in against it.
- It **includes the situation** — so you know when the job triggers.
- It **includes the ultimate expected outcome** — so you know what "done" looks like from the customer's side, not from yours.

### The Ulwick outcome statement — the measurable version

Ulwick's ODI produces a stricter statement — a **desired outcome** worded so you can measure it. The template ([Strategyn — Outcome-Driven Innovation](https://strategyn.com/jobs-to-be-done/)):

> _[direction of improvement]_ the _[metric]_ of _[unit of measure]_ _[context]_.

Examples:

> - **Minimise** the **time** it takes to **identify who owns a stalled PR review**.
> - **Minimise** the **likelihood** of **an invoice going unpaid past 30 days**.
> - **Increase** the **frequency** with which **the team knows the review is done without checking Slack**.

Every ODI statement uses a verb of direction (minimise / increase), a metric (time, likelihood, frequency, effort, error rate), and a unit of measure and context. You should be able to look at any proposed feature and score it on how much it moves that metric.

Ulwick's next move is to survey each outcome on **two dimensions**:

- **Importance to the customer** — how much does this outcome matter?
- **Satisfaction with current solutions** — how well does today's tool handle it?

An outcome that is **high-importance and low-satisfaction is underserved** — that is where opportunity lives. An outcome that is high-importance and high-satisfaction is served — do not compete on it. An outcome that is low-importance regardless of satisfaction is not worth the feature.

This "opportunity = importance − satisfaction" heuristic is the reason ODI can *reject* solutions: **if a proposed solution moves only served or unimportant outcomes, it does not deserve to be built.** That rejection power is what most founders' feature backlogs are missing.

### The four forces — Moesta / Christensen "forces of progress"

The Christensen/Moesta camp has a separate move that complements the ODI outcomes: **the four forces that act on any purchase decision.** These come from the "Milkshake" tradition and Moesta's Re-Wired Group research ([Christensen HBR 2016](https://hbr.org/2016/09/know-your-customers-jobs-to-be-done); [Bob Moesta — *Demand-Side Sales 101* (2020)](https://www.rewiredgroup.com/books)).

| Force | Direction | What it is | Interview question that surfaces it |
|---|---|---|---|
| **Push of the situation** | pushing toward change | The pain of the current-state. What made you look for something new? | "What was the moment you started looking for a different way?" |
| **Pull of the new solution** | pushing toward change | The attractiveness of what they moved to. Why this specific option? | "Once you decided to change, what pulled you to what you chose?" |
| **Anxiety about the new** | resisting change | Fear, uncertainty, risk of the new solution failing. | "What worried you about switching? What almost made you stop?" |
| **Habit of the current** | resisting change | Comfort with the existing tool, sunk cost, learned workflow. | "What did you like about the old way? What did you miss?" |

Change happens when push + pull **exceeds** anxiety + habit. That inequality gives you a *diagnostic*: for the segment that switched, what were the specific push events? For the segment that considered but did not switch, what specific anxieties dominated? Both are actionable for your positioning (mod-103) and for your ICP scoping (mod-104).

The forces framework is the reason you ask about the **switch moment** — the specific hour a person moved from tolerating the current state to actively searching for something new. That moment carries most of the useful information.

### The translation pipeline — from transcripts to a testable list

The mechanical work of this module is turning a stack of interview notes into a JTBD artifact. Here is the pipeline.

1. **Read each transcript once with a highlighter.** Highlight every phrase that describes a specific action the person took, a specific pain they felt, or a specific outcome they wanted. Ignore opinions.
2. **Extract candidate jobs.** Write each highlighted phrase as a Christensen-shape sentence: *when [situation], I want to [motivation], so I can [outcome].* Ignore duplicates for now.
3. **Cluster the candidates.** Two candidates that describe the same underlying job — even in different words — become one. This is where the interview corpus (Chapter 6) pays off: you can point at the source lines that justify the cluster.
4. **Convert each cluster's outcome into an ODI outcome statement.** *Direction + metric + unit + context.* This is the testable list.
5. **For each outcome, note importance and satisfaction from the corpus.** You may not have a formal survey — the interview language is enough at this stage. High-importance-low-satisfaction outcomes get starred.
6. **Note the forces per switch story.** For every interviewee who switched (or considered switching), record push, pull, anxiety, habit in one line each.

The output of this pipeline is the JTBD half of the discovery report (Chapter 7).

### Using outcomes to reject a solution

The moment you have a scored outcome list, you can score any proposed solution against it. The rule:

> A solution that does not move any high-importance-low-satisfaction outcome does not deserve to be built.

Two example rejections:

- **Rejected**: an AI-generated weekly PR-review summary email. Scored against the outcomes list, the top outcome ("minimise the time it takes to identify who owns a stalled PR review") is not moved — a weekly summary is too infrequent. Reject: build something else.
- **Rejected**: a Slack bot that sends a "you have a PR to review" nudge. Scored against the outcomes list, it moves the top outcome slightly (reviewer notified sooner) but the current satisfaction on that outcome was already medium. The rejection is not absolute — but it moves less than a proposal that automatically reassigns after N hours, which moves the top outcome dramatically.

The point is not that the list gives you a solution — it gives you a *filter*. Solutions still come from creativity; the filter tells you which ones to bother building.

## Concrete example — a small JTBD extract

From a small discovery corpus for the code-review-tool example:

**Jobs (Christensen shape):**

> - When an engineer's PR has been waiting more than a day, I want to know who is accountable for the review latency, so I can either escalate or reassign without becoming the team's nag.
> - When I onboard a new junior engineer, I want their first three PRs reviewed within four hours regardless of time zone, so they do not lose momentum in their first week.
> - When I run the weekly team sync, I want an accurate read of review latency and reviewer load, so I can rebalance the roster before it becomes a personnel issue.

**Outcomes (Ulwick shape):**

> - **Minimise** the **time** it takes to **identify the owner of a stalled PR review**. *Importance: high; current satisfaction: low. → underserved, star.*
> - **Minimise** the **median hours-to-first-review** for **new-hire PRs**. *Importance: high; current satisfaction: low. → underserved, star.*
> - **Increase** the **accuracy** of the **weekly review-latency read** shown to the manager. *Importance: medium; current satisfaction: medium. → served enough, deprioritise.*

**Forces (from three switch stories):**

> - *Push*: "I had a junior engineer sitting for two days waiting on a review — I lost him for the sprint."
> - *Pull*: "The tool we picked auto-reassigned after 24h — that was the killer feature."
> - *Anxiety*: "I was worried it would spam the team and they'd disable notifications."
> - *Habit*: "We'd been on GitHub-only for years; adding another tool felt like process debt."

The starred outcomes let this founder immediately reject two of the four features on her current backlog (weekly summary, generic notify-me nudge) and prioritise the two that map to the starred outcomes (owner-identification, auto-reassignment).

## Common failure patterns

- **Job statements that name your product.** *"When a user opens our dashboard, they want to..."* — that is a product statement, not a job statement. Rewrite without the product.
- **Outcomes with no metric.** *"Users want a better experience"* — meaningless. Every outcome must have a direction, a metric, a unit, and a context.
- **Confusing solutions with jobs.** *"They want a Slack integration"* — a Slack integration is a solution. The job underneath is *"be notified in a channel I already watch, so I don't miss it."*
- **Skipping the importance-satisfaction scoring.** Without it, you have a list of outcomes but no way to reject solutions. The filter is the whole point.
- **Treating the switch-story as the same conversation as the problem interview.** The forces come from *switch* stories specifically — people who *did* move (or considered it and did not). Problem interviews without a switch moment still teach you the current-state pain but not the four forces.

## Summary

- The customer is not buying a product; they are hiring it to do a job. Jobs are stable across products.
- Christensen's job statement: **when [situation], I want to [motivation], so I can [outcome].** Product-agnostic and situation-anchored.
- Ulwick's outcome statement: **direction + metric + unit + context.** Testable and rejectable.
- Score outcomes on **importance × satisfaction**. High-importance-low-satisfaction is the opportunity; solutions that do not move those outcomes should be rejected.
- The four forces (**push, pull, anxiety, habit**) explain *why* someone switched or did not. Push + pull must exceed anxiety + habit for change to happen ([Christensen HBR 2016](https://hbr.org/2016/09/know-your-customers-jobs-to-be-done); [Bob Moesta / Re-Wired Group](https://www.rewiredgroup.com/books)).
- The whole point of the JTBD vocabulary is that it lets a corpus of interviews function as a **filter that rejects solutions**, not just a list of things people said.
