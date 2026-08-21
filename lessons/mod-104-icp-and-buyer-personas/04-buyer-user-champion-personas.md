# Buyer, User, Champion — The Three Personas an ICP Needs at Enterprise ACV

## Motivation

Chapters 1-3 built a company-level ICP: firmographic + behavioural criteria plus a disqualification checklist. The ICP tells the AE *which company* to pursue. It does not tell the AE *which humans in that company* to talk to. At consumer or PLG ACVs — a $15/month product an individual signs up for in five minutes — that gap does not matter; the buyer, the user, and the champion are all the same person. At the enterprise-ACV end of the spectrum — a $150k contract that requires legal review, procurement approval, and a security assessment — the buyer, the user, and the champion are almost always **three different people**, and an ICP that identifies only the company is guaranteed to lose deals late.

The failure mode this chapter exists to catch: **the AE runs a full sales cycle with the wrong human, closes to "we love it, we just need to bring it to our VP" at week 8, discovers the VP has other priorities, and the deal dies at proposal.** The AE was talking to the *user* (the engineer who would use the product every day) and the *champion* (the technical lead who wanted the product) but never met the *buyer* (the VP who owns the budget and signs the contract). The company-level ICP said "yes"; the persona layer would have said "who is the economic buyer, and have you met them?"

This chapter names the three personas, the specific role each plays in enterprise-shaped sales cycles, the questions the AE asks to identify each, and the failure modes that come from missing any one of them. It also names the ACV threshold below which the three-persona discipline is over-engineered — because a $500/month PLG product bought by an individual engineer does not need a champion-mapping workshop.

## Core concepts

### The three personas — one-line definitions

- **Buyer persona.** The person who *signs the contract and owns the budget*. Titled: VP Eng, CFO, CIO, CTO, Head of Ops, Director of Sales — whichever function owns the P&L line the ACV lands on. Cares about: business outcome, risk, budget-vs-value math, defensibility to their own boss. Rarely uses the product day-to-day.
- **User persona.** The person who *uses the product day-to-day* to do their job. Titled: Software Engineer, Sales Rep, Marketing Manager, Support Agent, Analyst. Cares about: does this help me do my job faster / better / less painfully; does adopting this cost me time I don't have; does my team already use something I would have to abandon.
- **Champion persona.** The person who *advocates for the product internally* — sells the buyer on approving the purchase, runs the cross-functional coordination, defends the choice in the security / legal / procurement gauntlet. Sometimes titled Engineering Manager, Team Lead, Head of X, Senior Engineer, or Ops Lead. Cares about: does this make *my team* better, does the credit for the win come to me, is the vendor going to make me look good.

The critical property is that these are **role definitions, not seniority definitions.** An engineering manager can be the champion (advocating internally to the VP Eng buyer) *or* the buyer (if they own the budget line) *or* the user (if they use the tool day-to-day themselves). The persona is defined by the *role in the buying process*, not by the title. Naming the person before naming the role produces a mislabeled persona set that misleads the AE.

### Why all three matter at enterprise ACV

A $150k contract at a 500-engineer company passes through the following gates:

1. A user tries the product (self-serve or in a demo) and reports back to their team lead.
2. A champion decides the product is worth advocating for and starts building an internal case.
3. The champion pitches the buyer, who evaluates the business case against the budget line.
4. The buyer conditionally approves, subject to security review, procurement approval, and legal review.
5. The purchase closes.

Miss the user, and step 1 fails — no bottoms-up traction, no pilot users to reference in the champion's pitch. Miss the champion, and step 2 fails — the buyer is being pitched cold by an outside AE and has no internal advocate to shepherd the deal through the internal gates. Miss the buyer, and step 3 fails — the champion pitches an approval that never comes, because the buyer is not aligned, has other priorities, or has a budget freeze the champion did not know about.

At mid-market ACV ($10k-$50k) the three roles sometimes collapse: a single VP might be user, champion, and buyer simultaneously. At enterprise ACV they are always distinct. **The distinguishing test: does the person who says "we want to buy this" have unilateral authority to sign a $100k contract without any other approval?** If yes, they are the buyer (and probably also the champion). If no, there is a separate buyer somewhere, and the AE has to find them.

### The three views — what each persona wants

Each persona has a different value story. A pitch that lands for the user leaves the buyer cold; a pitch that closes with the buyer feels like abstract corporate-speak to the user; a pitch that recruits the champion is not the pitch that closes the buyer. The AE has to run three parallel value stories, tuned to each audience.

**The user's value story** — day-to-day workflow improvement.
- Frame: "here is what your job looks like today; here is what it looks like with us; here is the specific task you save 20 minutes on."
- Evidence: hands-on demo of the product, ideally with the user's own data or workflow.
- Objections: "I already have a tool that does most of this"; "learning a new tool costs me time this quarter"; "my team wouldn't adopt it."
- The user's endorsement moves the deal forward *bottom-up*: the champion cites "the engineers already tried it and love it" as evidence to the buyer.

**The champion's value story** — team-level outcome + personal credit.
- Frame: "here is the metric your team owns; here is the improvement across the team you can present to your VP; here is the case study you'll be the hero of."
- Evidence: aggregate metrics from similar teams, a reference from a champion at a peer company, and a co-authored internal deck the champion can present to their leadership.
- Objections: "I don't have time to run an evaluation"; "what if I champion this and it doesn't deliver — I look foolish"; "how will I justify this to my VP against other priorities."
- The champion's activation moves the deal forward *laterally*: the champion runs the internal coordination — coordinating pilots, wrangling security, aligning stakeholders — that the AE cannot do from outside the org.

**The buyer's value story** — business outcome + budget defence.
- Frame: "here is the P&L or KPI line you own; here is the specific number that moves; here is the ROI math that survives a CFO conversation."
- Evidence: ROI model with named assumptions, an anchor case study from a similarly-sized peer company, a security / legal / compliance package that pre-empts the standard objections.
- Objections: "I don't have budget for this quarter"; "we have three other priorities ahead of this"; "prove the ROI before I sign, not after."
- The buyer's approval closes the deal.

An AE running only one of these three pitches — usually the user pitch, because founders start there — closes deals only when all three personas happen to be the same person. In enterprise motions that is never.

### Naming the personas explicitly — the ICP artifact carries all three

The one-page ICP scorecard (Chapter 7) has a section for each persona with the following structure:

```
Buyer persona
Title(s): VP Engineering; Head of Developer Productivity; occasionally CTO at < 200-engineer companies
Reports to: CTO or CEO
Owns metric: engineering throughput, developer productivity, cycle time
Budget authority: yes, at ACV ≤ $50k without additional sign-off
Discovery question to identify: "who owns the budget for engineering tooling at your company?"
Value story: {2-3 bullets tuned to this persona}
Common objections: {2-3 bullets}

User persona
Title(s): Senior Software Engineer; Engineering Manager (small teams)
Reports to: Engineering Manager or Director of Engineering
Uses product: daily, average 15-30 min per day
Discovery question to identify: "who on the team currently owns keeping PRs moving?"
Value story: {2-3 bullets}
Common objections: {2-3 bullets}

Champion persona
Title(s): Engineering Manager; Team Lead; Senior Engineer with team-productivity mandate
Reports to: VP Engineering or Director of Engineering
Motivation: team's cycle-time metric appears in their performance review
Discovery question to identify: "who on your team would benefit most from cycle-time going down?"
Value story: {2-3 bullets}
Political capital: has the ear of the buyer; can get a meeting on the calendar within a week
```

Each persona has three critical fields the AE uses in real time: **the discovery question** to identify who fills the role at the specific target company, **the value story** to present to that person, and **the objections** that person is most likely to raise.

The AE's job in a discovery call is not to sell but to **map the personas at the target company** — turn the ICP's generic persona description into specific named humans at the specific prospect. By the end of the first discovery call, the AE should be able to answer: *at Acme Corp, who is the buyer? who is the champion? who is the user?* Names. Titles. Reporting relationships. Budget authority. If the AE cannot fill in those blanks after the first call, the second call's objective is to fill them.

### The champion-without-authority trap

The single most-lethal enterprise-sales failure mode: the AE finds a champion — an engineer or engineering manager who loves the product, uses the pilot enthusiastically, is a great meeting to be in — and treats the champion as the buyer. The champion says "let me take this back to my VP" and the deal dies six weeks later because the VP is not aligned, has other priorities, has never met the AE, and has no reason to fight for the champion's request.

The pattern is enticing because the champion is a friendly, engaged, easy-to-work-with human, and the buyer is often a distant, harder-to-schedule, more skeptical figure. It is more comfortable to spend AE-hours with the champion than to work through the champion to reach the buyer. Every enterprise sales methodology (SPICED, MEDDIC, MEDDPICC — mod-105 develops these) names this failure and instruments against it. MEDDIC's "E" (Economic Buyer) is exactly this discipline: identify the economic buyer, meet them by proposal stage, or the deal is not closable.

The remedy is the ICP persona split with an enforcement rule: **a deal cannot advance past the "demo" stage without the buyer being identified by name, or the deal is downgraded and the AE re-scopes the conversation to reach the buyer.** The champion is essential but insufficient.

### The ACV threshold — when the three-persona discipline is over-engineered

The three-persona split is essential at high ACV and over-engineered at low ACV. Rough thresholds:

- **PLG / self-serve ACV ($0 - $2k/year).** Buyer, user, and champion are usually one person. The ICP persona section collapses to a single "user" persona. The value story is the user pitch. There is no separate champion; adoption inside a team happens organically as the initial user brings peers into the product. Deferring to mod-107 (motion design) — the sales motion here is product-led, not people-led.
- **SMB / mid-market low ACV ($2k - $25k).** Buyer and champion often collapse into one person (a departmental head with departmental budget). User is often a distinct persona. The ICP persona section covers user and buyer/champion. Sales cycle is manageable with two personas.
- **Mid-market to enterprise ACV ($25k - $250k).** All three personas distinct. The ICP persona section is fully developed. Sales cycle requires explicit navigation across the three. This is where the discipline of this chapter is load-bearing.
- **Enterprise ACV ($250k+).** All three personas distinct *and* often multiplied: multiple buyers (VP Eng + CIO), multiple champions (multiple team leads), multiple user personas by role. The ICP persona section may need to expand to a buying-committee map (a stakeholder matrix). This is where MEDDPICC's "Decision Process" and "Paper Process" fields become the primary instruments.

The ACV threshold is not fixed. A $10k product sold to a healthcare hospital with an eight-week procurement and IT-security review has enterprise-shaped complexity even at mid-market ACV. Read the *shape of the buying process*, not just the price tag.

### Personas are not marketing personas

A related-but-different artifact is the *marketing persona* — the fictional-composite target reader for content, "Marketing Mary" with a stock photo, a fictional biography, and a list of "pain points." Marketing personas are useful for demand-gen content briefs and are not what this chapter is about.

The differences:

- **ICP personas name the *role in the buying process*** — buyer, user, champion. Marketing personas name the *content audience* — a fictional composite reader of a specific content asset.
- **ICP personas resolve to *actual named humans* at the target company** — "at Acme Corp, the buyer is Sarah Chen, VP Eng." Marketing personas remain composites.
- **ICP personas have *discovery questions* to identify them.** Marketing personas have *demographic and psychographic* attributes for content targeting.

The two are complementary. mod-108 (demand generation) uses marketing personas to brief content and paid campaigns; mod-104 uses ICP personas to run the sales cycle. Both can and should exist without confusing them.

## Concrete example — Loomly's three personas

Extending Chapter 1-3's Loomly ICP with the persona section:

### Buyer persona

- **Titles**: VP Engineering; occasionally CTO at < 100-engineer companies where CTO owns eng ops.
- **Reports to**: CEO or CTO.
- **Owns metric**: engineering throughput; cycle time; a specific board-facing "engineering velocity" KPI.
- **Budget authority**: yes, unilateral at ACV ≤ $50k. Above $50k, CFO co-sign.
- **Discovery question**: "who owns the budget for engineering-productivity tools at your company?"
- **Value story**: (1) engineering-throughput metric moves 15-25% within a quarter (cite Loomly's aggregate customer data — `<!-- needs-research: verify the 15-25% number against actual customer telemetry -->`); (2) reduces manager-hours-per-week spent chasing stalled PRs; (3) creates a defensible board-slide narrative on "how we made engineering faster this quarter."
- **Common objections**: (1) "we should build this ourselves"; (2) "this looks like Slack Reminders with extra steps"; (3) "why now — what's the urgency."

### User persona

- **Titles**: Senior Software Engineer; Staff Engineer; Engineering Manager (of small teams).
- **Reports to**: Engineering Manager or Director of Engineering.
- **Uses product**: passively (receives targeted nudges) rather than actively (opens a dashboard). Estimated: < 5 min per day of active interaction.
- **Discovery question**: "who on the team currently notices and pings people about stalled PRs?"
- **Value story**: (1) fewer Slack pings from the manager; (2) targeted nudges only when the user's own review is genuinely holding something up; (3) does not require adopting a new tool or workflow.
- **Common objections**: (1) "another notification I have to manage"; (2) "I'll get pinged constantly"; (3) "I already use Slack Reminders for this."

### Champion persona

- **Titles**: Engineering Manager; Team Lead of a 5-15-person team.
- **Reports to**: VP Engineering or Director of Engineering.
- **Motivation**: personally responsible for team cycle time; the metric appears in their quarterly review; a "we shipped 30% faster" narrative is career-relevant.
- **Discovery question**: "on your team, who is personally responsible for keeping PR-cycle-time low?"
- **Value story**: (1) turns the manager's own weekly manual PR-review into an automated process; (2) generates weekly report the manager can share with their VP without extra work; (3) attributes the throughput improvement to a specific action the manager championed.
- **Political capital**: has the ear of the VP Eng (weekly 1:1); can typically get a $10-25k tool approved with a strong pilot.

### The AE's real-time application

On a discovery call with a company that passes the Chapter 2 firmographic filter, the AE's persona-mapping work in the first 20 minutes:

1. **Identify who's on the call** (usually the champion — engineering managers are the most-receptive first meeting).
2. **Ask the buyer-identification question**: "who owns the budget for tools like this at your company?" — the answer names the buyer or confirms the person on the call is also the buyer.
3. **Ask the user-identification question**: "who on the team would actually receive the nudges from a tool like this?" — the answer confirms the user persona and often surfaces the pilot-team scope.
4. **Ask the champion-motivation question** *if* the person on the call is the champion: "how would rolling out something like this land for you personally — is throughput something you're accountable for?"
5. **Confirm next steps**: if the champion is on the call and the buyer is a different person, the AE's next-step ask is "can we schedule a 30-minute follow-up with your VP once you've had a chance to try it out?" — this is the champion-to-buyer handoff.

By the end of the first call, the AE has three names (buyer, champion, user) or knows which names are missing and what the plan is to get them. That is the persona layer functioning as an operating instrument.

## Common failure patterns

- **Company-level ICP only, no persona layer.** Deals close for the wrong ACV or die at the buyer stage because the AE never mapped the personas. The most common enterprise-sales failure.
- **Champion treated as buyer.** The AE spends the cycle with a friendly engineering manager who has no budget authority; the deal dies at "let me take this back to my VP" at week 8.
- **Single value story presented to all personas.** The user pitch delivered to the buyer feels irrelevant; the buyer pitch delivered to the user feels abstract. Three parallel value stories, tuned to each persona.
- **Persona defined by title, not role.** An "engineering manager" is not automatically the champion; the role depends on the buying process. Define personas by role in the buying process, then map titles that typically fill that role.
- **Persona layer at PLG ACV.** A three-persona split for a $15/month product is over-engineered ceremony. Match the persona depth to the ACV / buying-process complexity.
- **Missing user persona at enterprise ACV.** Enterprise buying without user endorsement rolls out and fails at adoption; the buyer gets angry; the deal churns at renewal even if it closed at signing. User validation is not optional at enterprise.
- **Discovery questions missing.** Each persona needs the specific question the AE asks to identify who at the target company fills that role. Without the question, the mapping is guessed.
- **ICP artifact has no "who did we map at Acme Corp" template.** The persona section is generic (buyer titles, discovery questions) but there's no place in CRM or the deal-review artifact to record the *specific* mapped humans at each account. Add the account-specific mapping.
- **Marketing personas confused with ICP personas.** "Marketing Mary with two dogs and a Peloton" is a content brief input, not an ICP persona. Keep them separate; both are legitimate.
- **Buyer identified but never met.** MEDDIC's Economic Buyer failure: the AE knows the buyer's name but never gets the meeting. A named-but-unmet buyer is worse than an unnamed one because it produces false confidence. The deal-review discipline: buyer must be *met*, not merely *named*, by proposal stage.

## Summary

- The **ICP has three personas**, not one: **buyer** (signs the contract, owns the budget), **user** (uses the product day-to-day), **champion** (advocates internally, runs coordination). At enterprise ACV these are always three different people.
- Each persona has a **different value story**: the user wants day-to-day workflow improvement, the champion wants team-level outcome plus personal credit, the buyer wants business outcome plus budget defence. Three parallel pitches, tuned per audience.
- Personas are defined by **role in the buying process**, not by title. The same title can fill different personas across companies; the AE identifies the role first, then the human.
- Each persona in the ICP artifact carries three real-time fields: **the discovery question** to identify who at the target company fills the role, **the value story** to present to them, and **the common objections** they raise.
- The **champion-without-authority trap** is the most-lethal enterprise-sales failure: AE treats a friendly champion as the buyer, deal dies at "let me take this back to my VP." Deal-stage discipline: buyer must be met by proposal.
- The **ACV threshold** governs how much persona depth to build. PLG collapses all three into one; mid-market often collapses buyer and champion; enterprise separates all three and often multiplies them into a stakeholder matrix.
- **Marketing personas are a different artifact** — fictional content-brief composites for mod-108 demand-gen. Do not confuse them with ICP personas, which resolve to real named humans at target accounts.
- Chapter 5 develops the **three-axis scoring** — ICP-fit vs ACV-fit vs timing-fit — that turns the ICP + personas into a real-time lead-scoring instrument the AE uses on inbound and outbound leads.
