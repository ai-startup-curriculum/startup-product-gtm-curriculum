# Solution and Product Interviews

## Motivation

Chapter 1 named the three interview stages; Chapters 2–4 went deep on the discipline for the *problem* stage (Mom Test, recruiting, JTBD). This chapter walks the mechanics of the two later stages — **solution interviews** and **product interviews** — because their failure modes are different from the problem stage and the moves that keep them honest are different too.

The temptation with both later stages is the same: **to slip back into pitch mode.** In a solution interview it feels natural to show your favourite mock and ask "which would you prefer?"; in a product interview it feels natural to walk them through a happy-path demo and ask "isn't that great?" Both destroy the information content of the conversation. This chapter gives you the specific moves that keep them honest.

## Core concepts

### The solution interview — what it is for

A solution interview happens **after** you have enough problem interviews to be confident that the problem is real, recent, painful, and worth-paying-for-to-fix. You have candidate job statements and starred outcomes from Chapter 4. Now you want to test: **does a solution shape of this kind register with these people, and which shape do they gravitate to?**

What it is not:

- Not a demo of a built product (that is a product interview).
- Not a pitch of your idea (that is a sales call).
- Not a survey ("which of these three do you like most?" — meaningless, they will pick the middle one out of politeness).

The failure mode it exists to catch: **wrong solution shape.** The problem is real but the shape you were going to build does not map to how the user would actually act — either it does not fit their existing workflow, or it does not match the mental model they have of the problem, or it lands on the wrong side of the buy-vs-build wall for their org.

### The three-artifact test

The move that keeps a solution interview honest: **bring 2–3 different solution artifacts, not one.** Show them all. Ask which the interviewee reaches for, and — critically — ask **why**.

- If you show one artifact, you will get politeness ("yeah, that could work").
- If you show three artifacts, the differences between the three become the data. Which does the interviewee describe most quickly? Which do they immediately try to hand back? Which do they modify with a counter-proposal ("well, if it did X instead...")?

The artifacts do not need to be built. Sketches on paper, a Figma mock, a competitor's screenshot with an annotation, a workflow diagram — all work. What matters is that the artifacts differ on a **dimension you care about** (e.g., in-workflow vs. dashboard; automated vs. human-triggered; per-user vs. per-team).

### The interview shape — solution stage

Approximate script for a 30-minute solution interview:

1. **(2 min) Re-anchor the problem in their words.** *"Last time we talked, you told me about the PR that sat for two days and lost your junior's sprint. Is that still the sharpest example, or has something worse happened since?"* — grounds the conversation in their reality, not your solution.
2. **(5 min) One more problem question.** New data — the situation has moved on since last time; something else may now be sharper. This is your last chance to catch a wrong-problem before you spend the rest of the interview on solutions.
3. **(15 min) Show 2–3 artifacts in random order.** For each: "Tell me what you see. Would this land in your world? Why or why not? What would you change?" Do not pitch. Do not explain how it works — let them read it. If they cannot read it in 60 seconds without your narration, the artifact is too complex; that itself is data.
4. **(5 min) Commitment ask.** *"If we built a working version of the one you liked most, would you be a design partner? What would that mean in practice for your team?"* — Chapter 2's commitment ladder, one rung up.
5. **(3 min) Referral ask + close.** *"Who else on your team, or at another company, should I show this to?"*

### The product interview — what it is for

A product interview happens **after** you have shipped something — an MVP, a landing-page prototype, a working alpha. The user actually touches it. The question is now: **does the built thing deliver on the promise, in the shape it was built, when a real user meets it fresh?**

What it is not:

- Not a usability test in the narrow HCI sense (Nielsen-style task success measurement — that is a different, adjacent discipline you can layer in later; see [Nielsen Norman Group's usability testing 101](https://www.nngroup.com/articles/usability-testing-101/) for that literature). At the IDEA stage, you are testing the promise before the polish.
- Not a training session. If they cannot use it without you narrating, you have a UX problem you would otherwise not have noticed.
- Not a satisfaction survey. "Do you like it?" measures nothing.

The failure mode it exists to catch: **wrong shipping order** — a shape that works in a mock but fails in software, an integration that is table-stakes but you saved it for v2, a workflow that looked linear in Figma but is nonlinear in the real user's hands.

### The think-aloud protocol

The single most useful move in a product interview is the **think-aloud protocol**, borrowed from usability research: **ask the user to narrate what they are seeing, thinking, expecting, and doing, out loud, as they go.**

> *"I'm going to give you a task and ask you to just try to do it. As you go, please talk out loud — tell me what you're seeing, what you expected, what you're going to try next, and what confuses you. I'm not going to help unless you're really stuck. If you don't know what to do, that's the most useful thing to tell me."*

This produces the highest-value data in a product interview. Two rules for the interviewer:

- **Do not help unless they are truly stuck** (more than 60–90 seconds without moving forward). Every intervention destroys a piece of data.
- **Do not explain.** If they misread a button label, that is data; do not correct them. If they cannot find the feature, that is data; do not tell them where it is.

The Nielsen Norman Group has published extensively on the mechanics of think-aloud; the primary source is Nielsen's original writing on the method ([Jakob Nielsen — "Thinking Aloud: The #1 Usability Tool"](https://www.nngroup.com/articles/thinking-aloud-the-1-usability-tool/)).

### The task list — pre-defined, not ad-hoc

Do not just say "play with it and tell me what you think". You will get a tour of the UI, not a test of the promise. Instead, define **3–5 tasks** that map directly to the starred outcomes from Chapter 4:

- *"You just noticed your junior's PR has been open for 30 hours. Show me what you'd do."*
- *"You want to know which of your reviewers are behind on their queue. Show me what you'd do."*
- *"Set the review-latency threshold for your team to 24 hours."*

Each task should be phrased in the user's language, not yours (no "click the escalation button" — that is the answer). Order them from simple to complex. Watch for the point where they get stuck — that is the shipping-order problem.

### The interview shape — product stage

Approximate script for a 45-minute product interview:

1. **(3 min) Baseline questions.** *"Since we last talked, what has changed in how you handle [workflow]? Any new tools?"* — makes sure the underlying situation has not shifted out from under you.
2. **(2 min) Set up the think-aloud protocol.** Explicit ask. Explain the "don't help" rule. Ask permission to record.
3. **(30 min) Run 3–5 pre-defined tasks.** Watch, do not talk. Note every hesitation, every misread, every question they ask you (which will tell you what should be in-product but is not).
4. **(5 min) Post-hoc questions — retro.** *"What surprised you? What did you expect to be there and wasn't? What was the first thing you noticed?"* Their fresh-eyes answer to these three is uniquely valuable at n=1; you will not hear it the same way from any repeat user.
5. **(3 min) Commitment ask.** *"Would you keep using this next week? What would we need to change for you to keep it in your team's stack?"* If the answer is "not yet, because X", X is your next-sprint spec.
6. **(2 min) Close + referral.**

## Concrete example — one solution interview, one product interview

**Solution interview — code-review-tool founder, week 7.**

Founder sketches three artifacts:

- (a) A separate dashboard with a "review queue" per person.
- (b) A GitHub-native inline bot that auto-reassigns a review after 24h without action.
- (c) A weekly Slack digest with per-team review-latency stats.

The interviewee (an EM) glances at (a) and says "another dashboard is another thing I'd have to remember to look at". Reaches for (b) immediately: "if this just did it, I wouldn't have to nag anyone — that's the whole thing." Waves off (c): "I don't need the report; I need the fix."

Founder writes down: *inline > dashboard > digest, for at least one EM. Ask 4 more EMs the same way.* If the pattern holds across five interviews, the founder has just rejected the dashboard shape and can spend engineering time on the auto-reassign bot instead.

**Product interview — same founder, week 12.**

The auto-reassign bot exists as a working MVP. Founder sits with an EM who has installed it in her org. The pre-defined tasks:

1. Set the reassignment threshold for one team to 24 hours.
2. Look up who was reassigned to whom this week.
3. Turn off reassignment for one team you don't want it on.

Task 1 works. Task 2 fails — the "activity" view exists but the EM cannot find it (she looks in Settings, in Slack, in the GitHub check tab; the founder had it under "Insights" in the product's own dashboard). **That is a wrong-shipping-order finding: the activity view needs to live inside GitHub, not in a separate dashboard, because that is where the user is when the question occurs to them.**

Task 3 works but the EM says "I wouldn't turn it off, I'd want to just tune the threshold per team" — a spec extension.

The founder now has a v-next spec grounded in real user behaviour, not in her assumptions.

## Common failure patterns

- **Solution interview with only one artifact.** You will get politeness. Bring at least two, preferably three.
- **Explaining the artifact.** Let them read it. If they can't, that is your data.
- **Product interview narrated by the founder.** If you demo, they will react to the demo. They will not react to the product. Hand over the keyboard.
- **Skipping the think-aloud setup.** Without an explicit ask to narrate, users go silent and you lose almost all the data.
- **Helping too fast.** Every rescue costs you a data point. Sit through the silence.
- **Confusing a satisfied user with a retained user.** "Yeah I liked it" is not usage. Retention shows up in cohort curves — the topic of mod-102, not this module.

## Summary

- Solution interviews catch **wrong solution shape**. Bring 2–3 artifacts and ask which the interviewee reaches for and why. Do not explain; let them read.
- Product interviews catch **wrong shipping order**. Hand over the keyboard, use the **think-aloud protocol**, run pre-defined tasks that map to starred outcomes.
- The commitment ask escalates each stage: at problem interviews they promise a follow-up; at solution interviews they promise design-partner time; at product interviews they promise continued use, a paid pilot, or a signed LOI.
- Both later stages have the same anti-pattern as the problem stage: **the founder narrating instead of the user acting**. The moves in this chapter are designed to force the user's action to be the data.
