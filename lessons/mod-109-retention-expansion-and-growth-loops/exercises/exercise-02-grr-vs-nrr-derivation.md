# Exercise 02 — GRR vs NRR Derivation

**Estimated time:** 3 hours
**Chapter link:** [`02-grr-vs-nrr.md`](../02-grr-vs-nrr.md)
**Prerequisite reading:** [David Skok — "SaaS Metrics 2.0"](https://www.forentrepreneurs.com/saas-metrics-2/) (~30 min); [OpenView — Expansion SaaS Benchmarks (most recent)](https://openviewpartners.com/expansion-saas-benchmarks/) (skim, ~20 min); [SaaStr — NRR benchmarks writeups](https://www.saastr.com/) (search for NRR / GRR benchmarks; ~15 min); [Bessemer — State of the Cloud](https://www.bvp.com/atlas) (skim, ~15 min)

## Problem statement

Chapter 2 fixed the formulas and named the benchmark bands. This exercise makes you *compute both numbers correctly on a real (or realistic) book*, spot the failure modes founders trip on, and produce the segment decomposition an outside underwriter would demand.

You will:

1. Derive GRR and NRR by hand on a provided small book that contains every failure mode Chapter 2 warned about — cohort drift, multi-year paper, involuntary-vs.-voluntary conflation, downgrade booked as churn, currency change. Fix each and produce the correct numbers.
2. Compute GRR and NRR for a real (or realistic hypothetical) book of your own — with cohort decomposition, four-movement roll-up, and segment split (ARR tier, cohort year).
3. Read the numbers against the benchmark bands and produce the one-paragraph verdict that would appear in scorecard section 2.

The exercise trains the metric integrity a Series-B underwriter will demand — the exact decomposition, the exact segmentation, the exact benchmark call-out.

## Requirements

Deliver a folder `exercise-02/` with:

- `part-a-provided-book-fix.md` — the correction pass on the provided book, including a table of "what the founder reported" vs. "what the numbers should be after fix" and the specific failure mode each fix addresses.
- `part-b-your-book-derivation.md` — the GRR / NRR derivation for a chosen startup, in the shape of scorecard section 2.
- Optionally: a spreadsheet with the movement decomposition (linkable from either write-up).

### Part A — Fix a broken book (75 min)

Below is a synthetic book of 8 customers over one year, presented as a founder's incoming "GRR / NRR" report. Each line contains one or more Chapter 2 failure modes; your job is to identify each and produce the correct numbers.

**The founder's summary as reported:**

> "Cohort of 8 customers as of 2025-01-01, starting ARR = $1,020,000.
> Ending ARR = $1,240,000. NRR = 1,240,000 / 1,020,000 = 121.6%. Clears the Series-A bar comfortably. GRR: 'roughly 90%.'"

**The underlying customer-by-customer detail:**

| # | Customer | 2025-01 ARR | 2025-12 ARR | Movement detail |
|---|---|---|---|---|
| 1 | Acme Corp | $180,000 | $240,000 | Added 20 seats mid-year; renewed at same per-seat price. |
| 2 | Beta Ltd | $80,000 | $60,000 | Downgraded from Pro to Standard tier in July after champion pushback on price. |
| 3 | Gamma Inc | $150,000 | $150,000 | Renewed flat. |
| 4 | Delta LLC | $60,000 | $0 | Started missing invoices in Q2; card expired in Q3 and never updated; officially cancelled Q4. Billing system marks as "cancelled — non-payment". |
| 5 | Epsilon Co | $40,000 | $130,000 | Signed a 3-year contract in Q1 for $390k total. Reported as "$390k new ARR in Q1" by sales team. |
| 6 | Zeta AG | $120,000 (EUR-priced, $ equivalent) | $160,000 ($) | Renewed at same EUR price; USD strengthened, so $ equivalent is higher. |
| 7 | Eta SA | $90,000 | $60,000 | Was on the annual plan; reduced seats in Q3, then cancelled in Q4. Founder reported as "$90k churn". |
| 8 | Theta Group | $300,000 | $440,000 | Renewed flat + bought new "Enterprise Security" cross-sell module in Q4. |
| **New Logos** | Iota, Kappa | — | +$100,000 combined | Two new customers acquired in Q3, included in "ending ARR". |

For each customer's movement, name the specific failure mode(s) at play (from Chapter 2's "failure modes" list) and the fix. Then produce the correct four-movement decomposition and the correct GRR and NRR.

Structure your write-up as:

1. **Per-customer failure-mode identification.** One row per customer showing (reported movement) → (correct movement) → (failure mode name).
2. **Corrected four-movement decomposition table.** Starting ARR, Expansion ARR, Downgrade ARR, Churned ARR (with involuntary-vs.-voluntary split), New ARR excluded.
3. **Corrected GRR and NRR** with the formula and the arithmetic.
4. **Benchmark read.** Which band does the corrected GRR / NRR fall into? Which was the founder's mis-reported number vs. the truth?

### Part B — Derive GRR / NRR for a real (or realistic hypothetical) book (75 min)

Pick a startup — yours, one you know well, or the code-review-tool example from the chapter.

Deliver `part-b-your-book-derivation.md` in the shape of scorecard section 2:

1. **Cohort locked at.** Specific date, specific customer count, specific Starting ARR.
2. **Four-movement decomposition.** Every ARR change in the cohort is in exactly one of: Expansion, Downgrade, Churned, or excluded (New ARR only for logos acquired mid-period).
3. **Involuntary-vs.-voluntary split** on Churned ARR (per Chapter 6 vocabulary — Chapter 6 exercise unpacks this in detail, but the decomposition starts here).
4. **GRR and NRR** with the formula and the arithmetic.
5. **Segment decomposition.** Minimum two cuts — ARR tier (e.g. enterprise / mid-market / SMB) and one other (cohort year, product line, or segment). Per-cut GRR and NRR.
6. **Benchmark read.** For each cut, the applicable benchmark band, and whether the number is above / at / below.
7. **Verdict.** One paragraph — is the book durable, compensating, or leaking? Where does the strongest segment mask a weaker one? Is expansion doing heavy lifting?

Length: 1–2 pages. Do not exceed 2. Mark hypothetical numbers as such and justify plausibility against the Chapter 2 benchmark ranges.

### Part C — Reflection (30 min)

A short closing paragraph:

- Of the failure modes Chapter 2 named, which do you think would be most likely to slip through in your own book if you did not do the exercise?
- If you were the incoming Series-B partner reading your Part B write-up, what one question would you push on hardest? (Segments hidden? Expansion masking churn? Multi-year contract paper? Involuntary churn treated as unavoidable?)
- What billing / CRM instrumentation would you add to make the Chapter 2 metric-integrity discipline automatic rather than an occasional exercise?

## Starter guidance

- Chapter 2's formulas are the operating manual. Read the "definitions — the exact formulas" section end to end before starting Part A.
- Every corrected number in Part A is defensible; every reported number in Part A contains a specific mistake. The exercise is not "find one bug"; it is "audit the whole book."
- For Part A, the failure modes to look for include (but are not limited to): multi-year paper as year-one ARR (Epsilon); currency change not normalised (Zeta); downgrade booked as full churn (Eta); involuntary churn not separated (Delta); "new ARR" included in NRR denominator (Iota / Kappa new logos).
- For Part B, cohort-lock discipline is 80% of the work. If your Starting ARR silently changes between periods, no downstream number is defensible.
- If you have real book data, do not skimp on the four-movement decomposition — this is the exact table every SaaS underwriter will build for themselves in diligence.
- If hypothetical, choose plausible-for-your-segment numbers. A per-seat pricing SMB motion producing NRR = 145% is not plausible; an enterprise sales-assisted motion at NRR = 92% while claiming strong PMF is not plausible. Cross-check against Chapter 2's benchmark ranges.

## Acceptance criteria

Your submission is complete when:

- [ ] Part A identifies the specific failure mode(s) in every customer row.
- [ ] Part A's corrected four-movement decomposition sums correctly and excludes new logos.
- [ ] Part A's corrected GRR is materially lower than the founder's "roughly 90%" (the multi-year paper, currency change, downgrade-as-churn, and involuntary-vs.-voluntary failures all inflate the founder's number).
- [ ] Part A's corrected NRR corrects for the new-logo inclusion in the founder's headline (the founder's 121.6% collapses when Iota + Kappa are removed from the numerator).
- [ ] Part B has a locked cohort at a specific date and a specific Starting ARR that never silently changes.
- [ ] Part B's four-movement decomposition sums correctly and excludes new logos.
- [ ] Part B has ≥2 segment cuts with per-cut GRR and NRR.
- [ ] Part B's verdict paragraph names whether the book is durable, compensating, or leaking, and cites the numbers.
- [ ] Part C reflection names a likely-to-slip failure mode, an underwriter-side question, and an instrumentation upgrade.

## Common ways this exercise goes wrong

- **Reporting only NRR (the "good number") without GRR.** Chapter 2's central discipline. If you skip GRR, the whole exercise fails.
- **Including new logos in the cohort.** New ARR is excluded from GRR and NRR. Chapter 2 said this repeatedly.
- **Booking multi-year contract paper as year-one ARR.** Epsilon in Part A is designed to catch this — the correct year-one ARR is contract value ÷ contract years.
- **Treating involuntary churn (Delta) the same as voluntary.** Chapter 2 flagged this as a metric-integrity failure and Chapter 6 unpacks the remediation. In Part A, Delta should be flagged as involuntary and Part B's decomposition should split involuntary from voluntary.
- **Currency-driven "expansion" (Zeta).** A EUR-priced customer whose $ equivalent went up is not expansion. Normalise before computing.
- **Downgrade booked as full churn (Eta).** Booking $90k churn when the customer downgraded to $60k and then churned $60k inflates churn and hides the downgrade signal.
- **Segment decomposition skipped.** An aggregate GRR / NRR without segment split is not defensible in diligence.
- **Verdict without the "compensating vs. compounding" language.** The Chapter 2 read is *"NRR clears bar but GRR is weak — expansion is compensating."* Learning to write that verdict is the whole exercise.
