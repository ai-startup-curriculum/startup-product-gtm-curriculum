# Exercise 03 — Inbound Topic Strategy Authoring

**Estimated time:** 3 hours
**Chapter link:** [`03-inbound-content-and-seo.md`](../03-inbound-content-and-seo.md)
**Prerequisite:** Chapter 3 read end-to-end; Exercise 01 completed (a portfolio that names inbound as either the primary or the experimental — if it names neither, run this exercise as a *speculative* topic strategy for the "not now" list against a future re-evaluation trigger); a mod-104 ICP scorecard (buyer / user / champion split); a mod-103 positioning statement.

## Problem statement

Chapter 3 named the most common inbound failure: **the founder — usually a technical founder without a marketing background — hires a "content agency" or a junior content writer, ships fourteen 1,200-word blog posts on generic industry topics, publishes them on a subdomain nobody links to, checks Google Search Console at week 12, sees zero rankings, and concludes "SEO doesn't work for us".** The actual failure is that no methodology was ever applied — the topics were wrong (top-of-funnel generic instead of bottom-of-funnel specific), the depth was wrong (1,200-word summaries instead of first-hand 10× pieces), the cluster was wrong (spread across ten topics instead of concentrated on one), and distribution was missing entirely.

This exercise trains you to **author a real inbound topic strategy** — the pillar page, the 12-month cluster plan, the distribution plan per piece, and the attribution setup — the way a technical founder actually has to run it. Not the fourteen-generic-posts version; the pillar + cluster + distribution + attribution version that produces the 6-12 month compounding curve.

The failure mode this exercise exists to catch: **the founder writes a "content strategy" that reads as a list of blog-post titles with no cluster coherence, no BOFU discipline, no 10× depth commitment, no distribution plan, and no attribution — then wonders 8 months later why the traffic is flat.**

## Requirements

Deliver a folder `exercise-03/` with five files:

- `part-a-cluster-selection.md` — the topical cluster choice with rationale.
- `part-b-pillar-outline.md` — the pillar page structure at outline depth (not the finished piece).
- `part-c-cluster-map.md` — 15-25 cluster piece titles with BOFU/MOFU/TOFU tagging.
- `part-d-distribution-plan.md` — the distribution flywheel plan per piece.
- `part-e-attribution-setup.md` — the attribution stack + first-quarter measurement plan.

### Part A — Cluster selection (30 min)

Deliver `part-a-cluster-selection.md`.

**A1 — Candidate clusters (10 min).** List 3-5 candidate topical clusters your product could plausibly own. Each candidate is a narrow topical domain — not "DevOps" but "detecting stale services in monorepos"; not "sales" but "founder-led-sales cadence at seed stage". For each candidate, note:

- The 2-3 core queries the cluster addresses.
- The buyer role that types those queries (per mod-104 buyer/user/champion split).
- The current top-3 ranking pages on the anchor query (Google or an SEO tool if available).
- One-sentence reason your product / founder has unique depth on this cluster.

**A2 — Cluster scoring (10 min).** Against each candidate, score three dimensions on a 0-3 scale:

- **Depth of unique first-hand experience** — does the founder have first-hand data, customer stories, and opinionated stances the competition cannot copy? (3 = deep original data; 0 = no more than any competitor has.)
- **BOFU query fit** — do the queries in the cluster indicate active evaluation intent (buyer looking for a solution shape) rather than casual awareness? (3 = every query is BOFU; 0 = queries are TOFU / awareness.)
- **Competition depth** — how good is the current top-3? A weak top-3 (thin generic posts) is a green cluster to attack; a strong top-3 (authored by domain experts with fresh data) is red. (3 = weak top-3, easy to 10×; 0 = strong top-3 with recent updates.)

Composite = sum. Highest composite wins for pillar cluster selection.

**A3 — Pick the primary cluster (10 min).** Name the primary cluster. Write a paragraph that:

- Cites the composite score.
- Confirms the cluster is narrow enough (one problem domain, not a category); Chapter 3's warning against spreading across 10 topics is the anchor.
- Names why the founder can author this cluster with first-hand depth (Chapter 3's Reason 2 for BOFU-first).
- Names the cluster's rough 12-month scope: 1 pillar + 15-25 cluster pieces + 1-3 case studies.
- If applicable, notes any adjacent cluster that will be deferred to year 2 or later (do not run two clusters at seed).

### Part B — Pillar page outline (30 min)

Deliver `part-b-pillar-outline.md`. Do NOT write the full pillar. Author the outline at enough depth that a writer with mid-domain expertise could produce a first draft from it.

**B1 — Pillar page metadata (5 min).**
- Working title (3,000-6,000-word range).
- Anchor query the pillar targets.
- Author byline (real name; must be someone with visible credentials).
- Estimated first-draft time investment.

**B2 — Pillar structure (20 min).** Outline in H2 / H3 depth:

- **H2 — problem framing.** What is the problem, why does it matter, how does the reader recognise she has it. Grounded in the queries the reader typed to arrive here.
- **H2 — the taxonomy.** The 3-5 distinct approaches / solutions / patterns the reader is choosing between. For each, a short summary.
- **H2 — deep-dive per approach.** For each of the 3-5 taxonomy items: how it works, when it fits, when it fails, what data or evidence supports the assessment. This is the 10× depth section — the section the competition's top-3 doesn't have.
- **H2 — the failure modes.** The specific ways the problem gets solved wrong in practice. First-hand examples where possible. This is where the founder's opinionated stance surfaces.
- **H2 — a running example.** A specific implementation the reader can inspect — GitHub repo, code snippets, a downloadable artifact, or a live demo.
- **H2 — how to choose.** A decision-shape summary: given your specific constraints, here is which approach fits. This is the section the LLM will cite when answering the anchor query.
- **H2 — related pieces.** Links to the 15-25 cluster pieces (in early drafts, placeholders; in the published version, real internal links).

**B3 — 10× checklist (5 min).** For each of the six 10× criteria (Chapter 3):

- First-hand data or measurement — where in the outline does it live?
- Running example the reader can inspect — where?
- Opinionated stance — where?
- Named author with credentials — confirmed?
- Depth calibrated to the query — is the pillar depth ~4,000-6,000 words on a query that warrants it?
- Regularly updated — commit to quarterly refresh (date the pillar's "last updated" field).

### Part C — Cluster map — 15-25 pieces (45 min)

Deliver `part-c-cluster-map.md`.

**C1 — Cluster piece list (30 min).** Author 15-25 cluster piece titles. Each entry includes:

- Working title.
- Type (walkthrough / comparison / failure-mode / opinionated-take / customer-case-study / how-to / benchmark).
- Anchor query the piece targets.
- BOFU / MOFU / TOFU tag (per Chapter 3's funnel-stage tagging).
- Target word count (2,000-4,000 typical for cluster pieces).
- Author assignment (founder / contract writer / customer-authored).
- Publish month (Month 1 through Month 12).
- Prerequisite (does this piece depend on the pillar being live, or another cluster piece existing?).

**C2 — Funnel balance check (5 min).** Compute the funnel-stage balance:

- % BOFU
- % MOFU
- % TOFU

Chapter 3's seed-stage default: 60-80% BOFU, 10-20% MOFU, 10-20% TOFU. If your balance skews TOFU-heavy, name the reason (usually: founder is defaulting to awareness content the founder cannot uniquely author). Fix by rebalancing.

**C3 — Publish cadence check (5 min).** Compute the pieces-per-month rate:

- Total pieces / 12 months = per-month cadence.

Chapter 3's minimum: weekly for the first 6 months. If your cadence is monthly or less, the corpus will be too small to reach the 15-25-piece topical-authority threshold in a 12-month window; either raise the cadence or accept the exercise as a 24-month rather than 12-month plan (name the choice).

**C4 — Cluster-coherence check (5 min).** Confirm every cluster piece is either in the primary cluster or is a directly-adjacent piece that internal-links back to the pillar. Any piece that does not fit the cluster is either (a) a candidate for a future secondary cluster (deferred) or (b) a piece that dilutes the current cluster's topical authority (deleted from the plan).

### Part D — Distribution plan (30 min)

Deliver `part-d-distribution-plan.md`. Chapter 3's rule: 30-50% of time budget on distribution, not on writing. A published piece with no distribution effort produces ~200 lifetime views; the same piece with active distribution produces 5,000-50,000. Distribution is what enables the organic tail.

**D1 — Distribution flywheel design (15 min).** For each of Chapter 3's five distribution spokes, name the specific plan:

- **Owned social.** Which platforms (founder's personal Twitter / LinkedIn / Bluesky / YouTube)? Founder's follower count on each. Committed post-per-new-piece cadence (single link-drop vs. thread vs. carousel).
- **Cross-posting.** Which technical platforms (HN / Lobsters / dev.to / r/programming / r/devops / specific niche subreddits)? Which pieces are candidates for which platforms (curation matters — thought-leadership pieces to LinkedIn; utility pieces to HN; deep-dive walkthroughs to Lobsters)?
- **Newsletter syndication.** Name 3-5 target newsletters in your ICP's information graph. For each, note whether a relationship exists yet (yes/warming/cold). Committed outreach cadence to build the missing relationships.
- **Community-native contribution.** Which Slacks / Discords / forums does the founder already participate in? What is the ratio of participation to link-dropping (a founder who is present as a community member can share her pieces contextually; a founder who is not can not)?
- **Format repurposing.** For each pillar piece, what repurposes are planned (Twitter thread, YouTube walk-through, conference talk, webinar, podcast interview)?

**D2 — Distribution per-piece plan (10 min).** For 3-5 example pieces from Part C, walk through the specific distribution plan the piece will get:

- Piece title.
- Publication date.
- Owned-social plan (specific posts, dates).
- Cross-post plan (specific platforms, dates, curation notes).
- Newsletter outreach plan (specific newsletters, offer type).
- Community-native plan (which conversations to reference the piece in).
- Repurposes (thread, YouTube, talk).

The purpose of the per-piece plan is to make distribution real — a plan at the flywheel level without a per-piece translation stays theoretical.

**D3 — Time budget check (5 min).** Estimate:
- Weekly writing time (author + editor).
- Weekly distribution time (owned social, cross-post, newsletter outreach, community, repurposing).

Chapter 3's ratio: 30-50% on distribution. If your weekly plan has 20 hours on writing and 3 hours on distribution, the ratio is wrong; rebalance.

### Part E — Attribution setup (15 min)

Deliver `part-e-attribution-setup.md`.

**E1 — Attribution stack (10 min).** Name specifically:

- The CRM or dashboard where inbound attribution is tracked (HubSpot / Attio / Salesforce / spreadsheet).
- The self-reported source field's location on every conversion form (blog signup, demo request, download form). Confirm it is free-text, not a dropdown (dropdowns bias to top-of-list options).
- The UTM parameter template for every published link (`utm_source`, `utm_medium`, `utm_campaign`, `utm_content`).
- The first-touch and last-touch attribution reports the CRM will produce.
- The LLM-referrer categorisation (`chat.openai.com`, `perplexity.ai`, `claude.ai`, `gemini.google.com`) as a first-class source.
- The 10-deal quarterly reconstruction check as a scheduled review.

**E2 — Q1 measurement targets (5 min).** For the first 90 days of the inbound programme, name:
- Pieces published (target from Part C's cadence).
- Newsletter placements (target from Part D's outreach).
- HN / cross-post submissions (target).
- Sign-ups attributed to inbound (target — likely low, this is Q1 of a 6-12 month curve).
- Demo requests attributed to inbound (target).
- Chapter 2 Gate 3 window-elapsed at Q1-end (should be ~25% of a 12-month window).

## Starter guidance

- **The cluster is the load-bearing decision.** A 15-25 piece corpus on one cluster ranks. The same 15-25 pieces spread across five clusters do not. Chapter 3's most common trap is spreading across topics — resist even when the founder's own interests span multiple domains.
- **BOFU first, always.** 60-80% of your Part C plan should be BOFU. A cluster map that leads with "The Complete Guide to X" (TOFU) and defers the "How to Detect X in Y" (BOFU) pieces to month 8 is inverted. Publish the BOFU pieces first; they convert; they teach you what the ICP responds to; and their traffic feeds the future TOFU pieces' backlink profile.
- **10× is not a slogan.** For every cluster piece in Part C, ask: what does this piece contain that the current top-3 for the query does not? If the honest answer is "nothing", either the piece needs to be re-scoped with a first-hand claim, or it is not worth writing. Chapter 3's Helpful-Content-update argument: content that is not 10× no longer ranks.
- **Named author with credentials matters more than founders think.** E-E-A-T signals are now dominant Google ranking factors. Every piece has a real author byline; the author has a public profile (LinkedIn, Twitter, GitHub, personal site) that establishes credentials in the cluster's domain. Anonymous or ghost-written pieces will not rank.
- **The distribution plan (Part D) is where most content programmes fail silently.** A founder can spend 20 hours writing a piece and 30 minutes cross-posting it, then wonder why traffic is 200. Chapter 3's ratio: 30-50% of time on distribution. If your writing:distribution ratio is 10:1, rebuild.
- **Newsletter relationships are a 6-12 month investment.** Newsletter authors don't syndicate cold offers from unknown founders. Build the relationship first — read the newsletter, comment on posts, share the author's writing, guest-post if invited. By month 6-9, an ask to feature your pillar page has context and lands. Chapter 3's Bytes.dev / Console.dev / SRE-Weekly examples are canonical.
- **The self-reported source field is not optional.** Chapter 3's attribution challenge 1 (the branded-search close) and challenge 2 (the LLM-cited close) both require self-reported source to resolve. A form without this field is a form producing 30-50% wrong attribution. Add it before any inbound piece publishes.
- **LLM referrers are a first-class source now.** Ignore them at your peril — a growing fraction of inbound-attributable pipeline routes through `chat.openai.com` / `perplexity.ai` / `claude.ai` / `gemini.google.com`. If you don't categorise them, they show up as "direct" and inbound gets under-credited.
- **This exercise's output is a 12-month plan, not a first-month plan.** The compounding math (Chapter 3) requires the full 12 months to produce meaningful signal. Committing to the plan is what makes the investment defensible; a plan that only covers month 1-3 is a plan that will be re-litigated every 90 days.

## Acceptance criteria

Your submission is complete when:

- [ ] Part A picks a primary topical cluster from 3-5 scored candidates with a written rationale citing depth + BOFU-query-fit + competition-depth scores.
- [ ] Part A confirms the cluster is narrow enough (one problem domain), the founder can author with first-hand depth, and the 12-month scope is 1 pillar + 15-25 cluster pieces.
- [ ] Part B outlines the pillar page at H2/H3 depth including problem framing, taxonomy, deep-dive per approach, failure modes, running example, how-to-choose, related pieces; commits to author byline + quarterly refresh.
- [ ] Part B walks the 10× checklist against the outline (first-hand data + running example + opinionated stance + named author + calibrated depth + refresh commitment all present).
- [ ] Part C authors 15-25 cluster piece titles with type + query + BOFU/MOFU/TOFU + word count + author + publish month + prerequisite.
- [ ] Part C confirms funnel balance is 60-80% BOFU, publish cadence supports the 15-25 pieces in 12 months, and every piece is cluster-coherent.
- [ ] Part D names the distribution plan across all five flywheel spokes (owned social, cross-post, newsletter, community, repurposing) with per-piece example plans for 3-5 pieces.
- [ ] Part D confirms the time budget ratio is 30-50% on distribution vs. writing.
- [ ] Part E names the attribution stack (CRM, self-reported source field, UTM template, first-touch + last-touch reports, LLM-referrer categorisation, quarterly reconstruction check) and Q1 measurement targets aligned to Chapter 2's Gate 3 window.
- [ ] Any factual claim (a keyword-volume estimate, a ranking benchmark, a specific competitor's article count) that is not cited to Chapter 3 or a public SEO tool output is flagged `<!-- needs-research: ... -->`.

## Common ways this exercise goes wrong

- **Generic-topics trap.** Cluster is "SEO" or "growth marketing" instead of a specific problem domain. No topical authority accumulates because the cluster spans too broadly. Fix: narrow the cluster to one problem the product solves better than any competitor.
- **TOFU-heavy trap.** Part C is 60% "What is X" / "Top 10 Y trends" pieces. The pieces don't convert; the founder cannot uniquely author them (competing with generic industry sources); Google's Helpful-Content update discounts them. Fix: 60-80% BOFU. TOFU is deferred until BOFU is producing pipeline.
- **1200-word-minimum trap.** Every piece in Part C is 1,200 words. This is the length that Google's Helpful Content update explicitly discounts; it is the length content agencies default to; it is not calibrated to the depth of the query. Fix: word count is calibrated per query — pillars 4,000-6,000, cluster pieces 2,000-4,000, only utility how-to pieces at 800-1,500.
- **No-named-author trap.** Author field says "The Loomly Team" or is empty. E-E-A-T signals absent. Fix: real author byline on every piece; author page with bio and credentials.
- **Content-agency-outsource trap.** Part C names "content agency" as the author for 20 of 25 pieces. Content agencies produce generic pieces without first-hand data. Fix: founder authors the pillar and 30-50% of cluster pieces; agency amplifies (formatting, editing, publishing) rather than substituting.
- **Distribution-plan-as-afterthought trap.** Part D reads "we will cross-post to HN and share on Twitter" without a per-piece plan, without newsletter relationships identified, without repurposing named. Fix: per-piece distribution plan is real; newsletter relationships are named and status-tracked; repurposing is committed per pillar piece.
- **Attribution-stack-not-instrumented trap.** Part E is a paragraph on "we track inbound in HubSpot" without the self-reported source field, without a UTM template, without LLM-referrer categorisation. Fix: all five elements of the attribution stack are named specifically before any piece publishes.
- **12-month-plan-that-really-runs-3-months trap.** Part C authors 25 pieces but the publish cadence in Part D is monthly. In 12 months, only 12 pieces will ship, below the 15-25 topical-authority threshold. Fix: cadence supports the piece count; adjust one or the other.
- **Cluster-coherence-drift trap.** Cluster piece list drifts into adjacent domains ("since we're writing about stale services, let's also cover CI/CD pipelines and Kubernetes operators"). Cluster loses coherence. Fix: adjacent-domain pieces defer to secondary cluster (year 2); the current 12-month plan holds the cluster tight.
- **Publish-first-worry-about-refresh-later trap.** Part B commits to shipping the pillar but does not commit to the quarterly refresh cycle. Pillar goes stale after 12-18 months; ranking drifts. Fix: refresh cycle is on the calendar from month 4 onwards; refresh cadence quarterly on top-20 pieces (Chapter 3 refresh discipline).
- **Skip-the-10×-check trap.** Every cluster piece is authored assuming it will be 10× without a per-piece check. Some pieces are 10×; others are indistinguishable from existing top-3. Fix: 10× checklist per pillar and per cluster piece; if a piece cannot pass, either re-scope or defer.
