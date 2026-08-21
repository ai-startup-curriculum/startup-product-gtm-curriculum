# The Dunford Five-Component Positioning Frame

## Motivation

Chapter 1 fixed the vocabulary — positioning is the strategic choice, messaging is the tactical derivation. This chapter is the operating instrument for authoring the strategic choice.

April Dunford's *Obviously Awesome* proposed a five-component frame — competitive alternatives, unique attributes, value, best-for characteristics, market category — that reduces positioning from a mystified craft to a defensible checklist. The frame is load-bearing: every failure mode Chapter 3 diagnoses is a failure at one specific component, and every downstream artifact (Chapter 4's narrative, Chapter 6's messaging, Chapter 7's positioning document) is a derivation from a five-component authoring.

The frame is not a template you fill in blindly. Each component has a defensibility bar that the *default* answer will fail. This chapter walks each component, names what "defended" looks like, and names the default the component is designed to reject.

## Core concepts

### The five components

Dunford's frame ([April Dunford — *Obviously Awesome: How to nail product positioning so customers get it, buy it, love it* (2019)](https://www.aprildunford.com/obviously-awesome); see also [April Dunford — "The 5 Building Blocks of Positioning"](https://www.aprildunford.com/blog)):

1. **Competitive alternatives** — what the customer *would use instead of you* if you did not exist. This is not "our direct competitors from the analyst's magic quadrant." It is *the actual alternative the buyer names when you ask them what they would do without your product*.
2. **Unique attributes** — the features / capabilities / properties that only your product has, or that your product has to a materially different degree than the named alternatives. Not "our list of features" — the ones that are *unique to you against the alternatives named above*.
3. **Value** — what those unique attributes actually deliver for the customer. Value is **derived** from the attributes; it is not asserted independently. Every claimed value must trace back to at least one unique attribute.
4. **Best-for characteristics** — the specific customer characteristics (firmographic, behavioural, technical, use-case) that predict the customer will care most about the value. Not "our target market"; the *characteristics* that make a customer a strong fit for this particular value proposition.
5. **Market category** — the mental shelf the customer already has in their head that you file yourself under. The category name determines who the customer compares you to, which price band they anchor to, and which buyer they route the decision to.

The components are ordered deliberately. Alternatives → attributes → value → best-for → category. Each depends on the ones above; changing one forces you to re-check the rest.

### Component 1 — competitive alternatives (the load-bearing input)

The single most-mishandled component. Founders name the direct competitors from their pitch deck ("Salesforce, HubSpot, Zoho") — the products in the same category with a similar feature set. The buyer, on the day they decide whether to buy, is not choosing between you and Salesforce. They are choosing between you and:

- **A spreadsheet** — the most common competitive alternative in B2B SaaS. If your buyer is currently running the workflow in Excel or Google Sheets, that is the alternative you must be *obviously better than* for the deal to close. Compare against Salesforce and you lose; compare against a spreadsheet and you win.
- **A homegrown script or internal tool** — the second-most-common in developer / infrastructure products. Someone on the buyer's team wrote 200 lines of Python that mostly works. The buyer will not adopt your product unless it is *materially better than the homegrown option plus the cost of maintaining it*.
- **The status quo of doing nothing** — the buyer has a problem, has been living with it, and is not motivated to change. The alternative is inaction. This is the alternative most sales calls actually die against; the buyer says "let me think about it" and the sale never closes.
- **A generic tool used in a specific way** — Notion used as a CRM; Airtable used as a project tracker; Slack used as an incident-response tool. If the buyer's team has cobbled together a workflow inside a horizontal tool, that stack is the competitive alternative.
- **A different-category tool being used instead of yours** — Zoom being used as a video-recording tool because "we already have Zoom." Loom is not competing with other video-recording tools; it is competing with Zoom-in-recording-mode.
- **A consultant or agency** — the buyer is currently paying humans to do the work. Your tool competes with the consultant's line item; the buyer will not switch unless the tool clearly reduces total cost including switching cost.
- **The direct in-category competitors** — Salesforce, HubSpot, Zoho. These are often the *least common* alternative the buyer actually considers. Founders over-index on them because they are named in analyst reports.

**How to defend the component:** interview five to ten actual buyers (from your discovery corpus in mod-101 or your Sean Ellis very-disappointed cohort in mod-102) and ask, verbatim: *"If our product did not exist, what would you do instead?"* The words they use are your competitive alternatives set. If the answers converge on "we'd stay on the spreadsheet," you have your load-bearing alternative — and the rest of your positioning must be *obviously better than a spreadsheet for this use case*.

**The default this component rejects:** the direct-competitor list from the pitch deck. Positioning against the wrong alternatives is Chapter 3's first failure mode (obvious-but-underwhelming).

### Component 2 — unique attributes

Once alternatives are named, unique attributes are the properties **you** have that the **named alternatives** do not. The scope of "unique" is defined *against the alternatives*, not against the universe of all software.

Examples of what qualifies:

- **Capabilities** — "we do X"; a workflow step or a feature the alternatives cannot perform.
- **Technology properties** — "we run in the customer's VPC"; "we retain zero data"; "we work with any LLM provider" — often the load-bearing attribute for security-conscious buyers when the alternative is a SaaS product that does not.
- **Data / integration surface** — "we integrate natively with X"; "we support the specific edge case Y" — often the load-bearing attribute for buyers whose alternative is a horizontal tool that supports the general case but not the edge.
- **Delivery model** — "we deploy in a day, not a quarter"; "we require zero engineering to set up" — often decisive when the alternative is an enterprise tool with a six-month implementation.
- **Pricing structure** — "we charge per workflow, not per seat"; often decisive when the alternative's pricing model does not fit how the buyer creates value.

Examples of what does *not* qualify:

- **"Ease of use."** Every product claims this. Unless you can point to a specific structural reason your product is easier — a shorter onboarding flow, a different mental model, an eliminated integration — the claim is not defensible. Compared against a spreadsheet, "easier" is not a unique attribute; it is a claim.
- **"Enterprise-grade security."** Table stakes in most B2B categories. If the alternatives all have SOC 2 and SSO, "we have SOC 2 and SSO" is not a unique attribute.
- **"AI-powered."** In 2026 this is category background; the buyer assumes it. It is not an attribute unless "AI-powered" solves a specific problem the alternatives leave un-solved, in which case the *specific problem solved* is the attribute, not the "AI-powered" label.
- **Founder qualifications.** "The team is from Google" is not an attribute of the product.

**How to defend the component:** for each candidate attribute, write down which named alternative from Component 1 lacks it. If you cannot name the specific alternative it is unique against, the attribute is not defensible. If every alternative also has it, the attribute is table-stakes, not a differentiator.

**The default this component rejects:** the marketing-page feature list. Feature lists are undifferentiated; the discipline is to name the small handful of attributes that are actually unique relative to the *named* alternatives.

### Component 3 — value (derived from attributes)

Value is the customer-facing consequence of each unique attribute. Every value claim must trace back to at least one attribute — otherwise it is founder aspiration, not positioning.

The trace looks like:

- Unique attribute: "we run inside the customer's VPC" →
- Value: "your security team does not need to approve a new data-processor agreement, so the deal closes in weeks not quarters" →
- Buyer characteristic that makes this valuable: "your organisation has a security review process that adds 12+ weeks to any new SaaS purchase" (this becomes an input to Component 4, best-for).

Or:

- Unique attribute: "our pricing is per-workflow instead of per-seat" →
- Value: "your bill grows with your usage, not with your headcount, so you can roll out to the whole team without a budget conversation" →
- Buyer characteristic: "your team has variable / seasonal usage and can't defend per-seat pricing to finance" (best-for input).

The critical discipline: **you cannot claim value without a named attribute behind it.** "We save you time" is not a value statement; it is a slogan. "Because our data model natively supports X, workflows that took 40 clicks in Y take 3 clicks in ours — a 3-minute task becomes a 15-second task" is a value statement — attribute traced to numeric consequence.

**How to defend the component:** for each value bullet, write the attribute → value → buyer-consequence chain in one sentence. If the chain cannot be written, the value is unsourced and must be dropped.

**The default this component rejects:** value claims asserted independently of attributes. "We make sales teams more productive" is a slogan; "because our data-entry flow is 60% shorter than Salesforce's for the specific case of logging a call, an AE saves 20 minutes per day" is a value statement.

### Component 4 — best-for characteristics

Not every customer will care about your value equally. Best-for characteristics name the specific customer traits that predict a customer will care most.

Best-for is *not* the ICP as it exists in mod-104 — that module builds a scoreable ICP scorecard with disqualification criteria. Best-for is narrower: **the characteristics that make the value proposition maximally resonant.** Written as filters:

- **Firmographic** — industry, company size, revenue band, geography. "50-200-engineer B2B SaaS companies with distributed teams."
- **Situational** — the buyer is in a specific state that makes the pain acute. "Companies that have just hit an engineering-productivity KPI in a board meeting"; "companies whose eng org has grown 3× in 12 months."
- **Technical** — the buyer's tech stack makes the value especially high or the switching cost especially low. "Teams already using GitHub" (not GitLab or Bitbucket) — because our integration surface is GitHub-native.
- **Behavioural** — the buyer's team already exhibits a behaviour that suggests the value is legible to them. "Teams where the eng manager already runs a weekly PR-stalledness review manually" — they will recognise the workflow instantly.

The best-for list is used as a *positive filter* for messaging (target the buyers most likely to convert) and as an *input to the ICP* (mod-104). It is also the input to the Chasm beachhead selection (Chapter 5) — the first segment to serve is the one where the best-for characteristics are all present with high intensity.

**How to defend the component:** for each characteristic on the list, write a one-sentence reason why customers *with* that characteristic care more about the value than customers *without* it. If no reason surfaces, the characteristic is decoration.

**The default this component rejects:** the "everyone who wants X" over-broad market. "Any B2B company with a sales team" is a market size, not a best-for characteristic. Positioning that names a broad TAM as best-for is positioning that has not made a choice — and Chapter 5 will unpack why refusing to choose is more expensive than choosing wrong.

### Component 5 — market category

The market category is the mental shelf. When the buyer thinks "we should look into X-type products," which category name comes to mind, and are you on that shelf?

Category matters because it determines:

- **Who the buyer compares you to.** File yourself in "CRM" and you're compared to Salesforce; file yourself in "revenue intelligence" and you're compared to Gong and Clari. Same product, different comparison set, different sales cycle, different price band.
- **What price the buyer anchors to.** Categories have price bands. "Note-taking apps" anchor to $10/user/month; "enterprise knowledge management" anchors to $50/user/month; "productivity infrastructure" anchors higher. Move your category and your price ceiling moves.
- **Which buyer inside the organisation the decision routes to.** "Analytics tools" route to the data team; "revenue intelligence" routes to the CRO; "customer success platforms" route to the VP CS. Same product, different buyer, different sales motion.
- **How the buyer searches for you.** SEO, analyst reports, peer conversations — the buyer looks under the category label. If you're not on that shelf, you are invisible in the search.

Category selection has three flavours:

- **File yourself in an existing category** — often the safest choice; the buyer already knows the shelf exists, the price band is understood, the sales motion is known. Downside: you are one of many products on that shelf, and you must earn attention against strong incumbents.
- **File yourself in an adjacent existing category** — sometimes the differentiation of your positioning is that you *belong on a different shelf than your obvious competitors do*. Salesforce is "CRM"; you're "revenue intelligence" — same buyer, different shelf, different price anchor, less crowded.
- **Create a new category (category design)** — expensive, slow, and rarely the right move; the [Play Bigger](https://www.playbigger.com/) crowd advocates it, but even Play Bigger notes that category creation is a multi-year, capital-intensive campaign. For most startups, the correct move is file-into-existing or shift-to-adjacent, not create-new.

**How to defend the component:** ask five prospects — after describing the product — "if you were to look into products like this, what category name would you search for on Google?" The words they use are your candidate category names. Diverge from them at your peril.

**The default this component rejects:** category invention without capital. Category creation ("we invented the 'developer productivity fabric' category") without a multi-year cross-team campaign to install that vocabulary in the buyer's head lands nowhere. The buyer never adopts the vocabulary; the messaging is illegible; the deal never routes to the right buyer.

### The failure mode this frame exists to catch — "default positioning"

Dunford's term for what happens when a startup does not deliberately position: **the product ends up positioned as a slightly-different version of the founder's most-obvious competitor, filed under the most-obvious category, sold to the most-obvious buyer.** Nothing about the positioning is chosen; everything about it is inherited. The result is a product page that reads as "Salesforce but cheaper," a sales cycle that is compared unfavourably to Salesforce feature-by-feature, and a pricing conversation that anchors on Salesforce's per-seat number.

Default positioning is the null hypothesis. Every founder starts there. The five-component frame is what pulls the positioning away from default.

Each component defended against its default:

| Component | The default | What "defended" looks like |
|---|---|---|
| Alternatives | The direct in-category competitors | The alternative the buyer actually names when asked "what would you do without our product?" (usually a spreadsheet, a script, the status quo, or a horizontal tool used in a specific way) |
| Attributes | The full marketing feature list | The 3-5 properties that are unique against the *named* alternatives |
| Value | Assertion ("we save you time") | Attribute → consequence chain, one sentence, ideally with a number |
| Best-for | "Everyone with problem X" | 3-5 characteristics that predict high value; each with a one-sentence reason |
| Category | The obvious in-industry label | The shelf the buyer actually uses; ideally one that shifts you off the crowded incumbent shelf without inventing a new one |

## Concrete example — Loomly's five-component positioning, defended

Return to Loomly (the PR-nudge tool from Chapter 1), authored under Positioning A ("code-review nudge tool for engineering managers").

**Competitive alternatives:**
- Manual Slack pings from the engineering manager ("hey, PR-482 has been stale for 2 days, can you review?")
- Weekly engineering-manager standups where stalled PRs are reviewed by hand
- Generic Slack apps (Reminder Bot, PullReminders) that fire a notification on a fixed cadence without knowing whether the reviewer is the right person
- The status quo of "we just don't do anything and reviews stall"

**Unique attributes (against those alternatives):**
- Reviewer-selection logic: watches CODEOWNERS + prior review history + current-week load and nudges the *right* reviewer, not just "someone." (Alternatives: manual pings don't scale beyond ~15 open PRs; Reminder Bot pings the PR author or a random assignee.)
- Load-balancing: nudges are throttled so senior reviewers don't get 40 requests a day. (Alternatives: no such throttling.)
- Escalation ladder: PRs stalled >72h auto-escalate to a fallback reviewer, then to the engineering manager. (Alternatives: manual chase.)

**Value (traced to each attribute):**
- *Attribute: reviewer-selection* → *Value: engineering managers stop being the pager for stalled reviews; median review-cycle time drops from 3.2d to 1.1d in beta customers.* [<!-- needs-research: cite the specific study or beta cohort the median figure comes from before publishing verbatim -->]
- *Attribute: load-balancing* → *Value: senior reviewers are not over-taxed; team reviewer distribution flattens; new reviewers on-ramp faster because reviews get to them.*
- *Attribute: escalation ladder* → *Value: no PR falls through the cracks past 72 hours, so the "PR stuck for two weeks" incident doesn't happen.*

**Best-for characteristics:**
- Engineering teams of **20-100 engineers** — small enough that a single tool can cover the whole org; large enough that manual nudging has broken down.
- **Distributed / async-first teams** — reviewer coordination breaks worst when everyone isn't in a shared timezone.
- Teams **already using GitHub** — the integration surface is GitHub-native; teams on GitLab, Bitbucket, or Gerrit are not best-for today.
- Teams where **the engineering manager has explicitly named "PR cycle time" as a KPI** — the value proposition is immediately legible.

**Market category:**
- Primary: **engineering-manager productivity tools** — the shelf that already exists in the buyer's mind alongside Linear, Jellyfish, LinearB.
- Secondary (adjacent): **developer experience / DevEx tooling** — the DORA-metrics-adjacent shelf that shifts the buyer conversation from "engineering managers" to "engineering platform leaders."
- Not: **engineering intelligence / analytics platforms** — that shelf anchors to a different price band ($15-30/eng/mo) and routes to a different buyer (VP Eng, not eng manager). Positioning C from Chapter 1 would file here instead.

The defended positioning fits on a page. Every component is defensible — the founder can, on demand, name a specific customer conversation or a specific product property behind the claim.

## Common failure patterns

- **Naming the direct competitors as the alternatives.** Salesforce is not the alternative; the spreadsheet the buyer is currently using is. Interview five customers with the "what would you do without us" question before you commit.
- **Undifferentiated attribute lists.** Every enterprise SaaS company claims "enterprise-grade security" and "easy to use." Unless the attribute is unique against the *named* alternatives, it is not a unique attribute.
- **Value without attributes.** "We save you time" is not a value proposition. "Because we ship X, task Y takes Z% less time" is.
- **Best-for that names a TAM instead of characteristics.** "All B2B companies" is a TAM. "Companies with a distributed engineering team of 20-100 whose engineering manager tracks PR cycle time" is a best-for.
- **Category invention without the capital to install it.** Category creation is a multi-year campaign. Startups without that runway should file into an existing shelf or shift to an adjacent one.
- **Skipping component 1 because "we know our market."** The whole frame depends on Component 1. If it is wrong, every downstream component is wrong. The interview discipline exists to prevent founder-invention here.
- **Treating this as a workshop artifact.** The five-component positioning is a *living document*; it is revisited when the customer conversation surfaces new alternatives, when a new competitor enters the market, or when the product ships an attribute that changes the value equation. See Chapter 7's dated / signed / versioned discipline.
- **Positioning the whole company as one thing when the product has multiple lines.** Multi-product companies position each product separately, then the *company* is positioned as the intersection. Startups rarely have this problem; enterprise SaaS routinely does.

## Summary

- The Dunford frame has **five components in order**: competitive alternatives → unique attributes → value (derived) → best-for characteristics → market category.
- **Competitive alternatives** are what the buyer would do without you — usually a spreadsheet, a homegrown script, the status quo, or a horizontal tool, *not* the direct-competitor list from your pitch deck.
- **Unique attributes** are properties you have that the *named alternatives* lack. Scope of "unique" is against the alternatives, not the universe.
- **Value** is derived from attributes; every value claim traces to a named attribute through an attribute → consequence chain.
- **Best-for characteristics** are the specific customer traits that predict the customer will care most about the value. Not the TAM; a filter over it.
- **Market category** is the mental shelf; it determines who you're compared to, what price you can anchor to, and which buyer the decision routes to. File into existing before you invent new.
- The frame exists to reject **default positioning** — the null hypothesis where the product inherits its alternatives, attributes, category, and buyer from the most obvious in-industry incumbent. Every component has a specific default it is designed to reject.
- Every component must be **defensible** — a specific customer conversation or product property behind each claim. Chapter 3 diagnoses the failure modes when a component is not defended.
