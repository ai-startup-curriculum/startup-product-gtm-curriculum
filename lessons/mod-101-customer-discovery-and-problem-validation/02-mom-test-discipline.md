# The Mom Test — Interviews That Produce Information

## Motivation

The single most common way early-founder interviews fail is that **the founder asks the interviewee to evaluate the idea, and the interviewee — being polite — says something encouraging.** The founder walks away energised, updates the deck, keeps building. The information content of the interview is zero.

Rob Fitzpatrick's *The Mom Test* is a book about how to run these conversations so that they produce information rather than compliments. The name refers to the observation that even your mother — the person most predisposed to be kind to you — will accidentally give you useless information if you ask her about your idea; the fix is not to trust her less, it is to **ask about her life instead of your idea** ([Fitzpatrick 2013 — book site](https://www.momtestbook.com/); [author's own summary talk](https://www.momtestbook.com/blog)).

This chapter is the operating discipline for the interview turn itself. It is what makes any interview from Chapter 1 — problem, solution, or product — produce useful data.

## Core concepts

### The three Mom Test rules

Fitzpatrick reduces the whole book to three rules a founder can hold in their head mid-conversation:

1. **Talk about their life, not your idea.**
2. **Ask about specifics in the past, not opinions about the future.**
3. **Talk less and listen more.**

That is the whole discipline. Every technique below is a consequence of one of those three.

### Why "would you use this?" is a bad question

The single most damaging question in an early-founder's toolkit is some variant of **"would you use this?"** or **"would you pay for this?"**. Two problems:

- **It asks for a prediction about future behaviour.** Humans are notoriously bad at predicting how they will behave in a hypothetical. The academic literature calls this the intention-behaviour gap; the founder version is "everyone said they'd pay and no one bought."
- **It puts the interviewee in the position of grading your idea.** Politeness dominates. You get "yes, that sounds great" from people who will never use it and "hmm, interesting" from people who would.

Fitzpatrick's replacement: **ask about the past.** The past is real; opinions about the future are cheap.

| Bad — opinion about the future | Good — specifics in the past |
|---|---|
| "Would you use a tool that automates invoice chasing?" | "Walk me through the last invoice you had to chase. When was it? How did you chase it?" |
| "Would you pay $50/month for this?" | "What are you currently paying for tools that touch this workflow? What do you use them for?" |
| "Do you think X is a big problem?" | "How often did X come up for you in the last month? What did you do the last time?" |
| "Would this be better than what you use today?" | "Tell me about your current tool. Where does it work well? Where does it not? What was the last time it broke down?" |

### The founder-fishing questions to strike from your vocabulary

These questions look useful and are not. Recognise them and delete them from your script.

- **"Would you..."** anything. Kill this word for the entire interview.
- **"Do you think..."** anything. You are asking for an opinion; you want a behaviour.
- **"Wouldn't it be great if..."** You are pitching. You will get a compliment.
- **"How much would you pay?"** They will invent a number, and it will be a fantasy number. If you need pricing signal, run a mod-106 willingness-to-pay study (Van Westendorp / Gabor-Granger).
- **"If we built X, would you buy it?"** The single worst question. Compound of all three.

### Compliments are a warning, not a signal

When you hear "That's a great idea", **that is data that your interview has drifted into pitch mode**, not data that the idea is good. Fitzpatrick's move: politely deflect the compliment back to their life. *"Thanks — but tell me more about how you handle X today."*

The general test: **would this same interviewee have said the same thing to a founder pitching a completely different product?** If yes, the response is noise.

### Asking why — the follow-up that carries the interview

The single most useful follow-up in a discovery interview is **"why?"** — asked without a leading frame.

- Interviewee: "We switched to Notion for that last year."
  - Bad follow-up: "Because the alternatives were bad, right?" (leading; will get agreement)
  - Good follow-up: "Why? What happened that made you switch?"
- Interviewee: "We just live with it."
  - Bad follow-up: "Would you switch if there was a better tool?" (opinion about the future)
  - Good follow-up: "Why? What have you tried?"

**Why-questions get you at motivation**, which is the JTBD-level information Chapter 4 (Jobs-to-be-Done) will teach you to extract systematically. Without motivation, you have facts about behaviour but not the *reason for the behaviour* — and the reason is what tells you whether your solution shape maps to their world.

### The three critical questions to test whether a problem is real

Fitzpatrick offers a diagnostic set of three past-tense questions that separate a real problem from a nice-to-have complaint. Run them at some point in every problem interview:

1. **"When was the last time this came up for you?"** — recency. If they cannot name a recent instance, the problem is not urgent.
2. **"Walk me through what you did about it."** — behaviour. If they did nothing, the problem is not worth doing anything about.
3. **"What did that cost you? (Time, money, missed opportunity, workaround.)"** — magnitude. If the cost is trivial, they will not pay to fix it.

A problem that passes all three (recent, they took action, non-trivial cost) is a candidate to build for. A problem that fails any one of them is a problem you should stop building for.

### The commitment ladder — the closest you get to a "would you pay"

Instead of asking "would you pay?", **watch what they will commit to right now.** Every interview should end with an ask for a small piece of commitment appropriate to the stage; the pattern of who accepts and who declines is much better data than any hypothetical.

| Stage | Ask at end of interview |
|---|---|
| Early problem interview | "Can I follow up in two weeks? If a tool for this existed, I'd want to show it to you." |
| Later problem interview | "Would you introduce me to two other people who have this same problem?" |
| Solution interview | "If we built a prototype, would you spend 30 minutes testing it? Can we schedule that now?" |
| Late solution / early product interview | "We're going to charge for this. Would you pre-commit — pay a deposit, sign a design-partner LOI, put a card down for early access?" |

Money > time > name > nothing. When the ask is real and the answer is no, you have learned more than any "would you use this" ever teaches you. Fitzpatrick calls the vague-yes answer that does not translate into commitment a **"fluff"** answer — it feels like validation and produces nothing.

## Concrete example — a Mom-Test rewrite

**Founder's original draft script (bad):**

> 1. Do you think managing invoices is a pain?
> 2. Would you use an AI tool that automates invoice chasing?
> 3. What would you pay for something like this?
> 4. Do you think other consultants would find this useful?

Every question is future-tense opinion. Every answer will be polite noise.

**Mom-Test rewrite (good):**

> 1. Walk me through how you handled invoicing last month, from the day you finished the work through the day you got paid.
> 2. When was the last time an invoice was paid late? Tell me the story.
> 3. What did you do about it? How long did you spend? Did you use any tool, or was it manual?
> 4. If it happens again next month, will you do the same thing, or something different? Why?
> 5. What are you paying today for the tools that touch this workflow?
> 6. (End) Who else do you know who runs invoicing like this? Can I ask you to introduce me to two of them?

Every question is about the past, about their life, and grounded in specifics they can actually remember.

## Common failure patterns

- **Interviewer talks more than the interviewee.** If the transcript shows you talking >30% of the time in a problem interview, you were pitching. Fitzpatrick's rule of thumb: talk less than the interviewee talks, by a wide margin.
- **The interview never leaves the founder's frame.** If every question starts with "we're building..." or "we think that...", the interview is a pitch. Reset by asking about something concrete they did yesterday.
- **The founder edits away the bad news.** After a hard interview, the temptation is to hear the polite parts and forget the "we solved this with a spreadsheet three years ago" moment. The corpus discipline in Chapter 6 exists to prevent this.
- **Vague statements get transcribed as strong signal.** "Yeah, that could be interesting" becomes "prospect confirmed interest" in the founder's memo. It did not. It was fluff.

## Summary

- Three rules: **their life, not your idea; past specifics, not future opinions; listen more than you talk.**
- Strike **"would you..."**, **"do you think..."**, and **"how much would you pay..."** from your vocabulary. They produce compliments, not information.
- Ask **"why?"** as your default follow-up. Motivation is what you are actually collecting.
- Every problem interview should test recency, behaviour, and cost — the three questions that separate a real problem from a nice-to-have.
- Compliments are a warning that the interview drifted into pitch mode. Deflect back to their life.
- Replace hypothetical willingness-to-pay with a **real commitment ask** at the end of every interview. Money > time > name > nothing.
