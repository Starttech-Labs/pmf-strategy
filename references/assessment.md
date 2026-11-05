# Assessing product-market fit

Source: “Measuring PMF Deliberately,” growth, retention, engagement, and NPS lessons, original lines 3047–3604. Data-quality safeguards and explicit verdict labels below are implementation guidance added to the source framework.

## Define what is being measured

Establish segment, time window, user/account unit, natural usage frequency, and the core action that represents delivered value. Specify event definitions, cohort entry, time zone, eligibility, and data coverage before calculating. Request the minimum missing data; do not invent retention from signups or testimonials.

For marketplaces, measure both sides at their respective natural frequencies and examine their dependence on each other. For B2B, the course emphasizes end-user retention; additionally inspect account adoption, buyer renewal, and revenue concentration when relevant to the business decision. Many employees in one customer account are not independent buying decisions.

## Retention: does the product keep delivering value?

Group users by entry cohort and segment. For each elapsed period, calculate the proportion of the original eligible cohort performing the core action. State the retention convention; period retention and rolling “returned at any later time” retention are different. Leave unobserved future cells missing, not zero. Report cohort sizes and age alongside curves; compare equally mature cohorts.

The course suggests hundreds of users and at least six natural usage periods as a starting point for interpretation. These are heuristics, not confidence guarantees, and a large aggregate does not fix tiny segment cohorts.

| Cohort pattern | Interpretation | Next move |
|---|---|---|
| Trending toward zero | Promised value is not persisting | Revisit problem, audience, benefits, and alternatives using broad validation. |
| Gradually declining | Some resonance, continuing leakage | Investigate churn causes and segment differences; test specific improvements. |
| Durable nonzero plateau | Evidence of retained value for this segment | Check plateau level against economics and verify across mature cohorts; test sustainable growth. |
| Smile / returning users | Reactivation may strengthen retention | Check seasonality and instrumentation; understand what brings users back. |

No universal plateau percentage proves PMF. A tiny plateau may be uneconomic; a short apparent plateau may disappear. Avoid hiding deteriorating recent cohorts behind an old average.

For annual or rarer use, retention may take too long to guide near-term decisions. Use delivered outcomes, engagement during the active journey, and sustainable acquisition as provisional evidence, and explicitly state that repeat-use evidence is immature. Do not judge annual use by daily activity.

## Growth: can this segment be acquired sustainably?

Plot **new users per period**, not cumulative registrations, by segment and channel. Use a consistent cadence and enough periods to distinguish a trend from a launch spike. The source discusses monthly additions and at least six natural usage periods; select a window appropriate to the product and seasonality.

Its growth labels refer to the curve of new-user additions:

- Declining: investigate launch effects and channel exhaustion.
- Flat additions: cumulative users can grow, but acquisition is not compounding.
- Increasing additions (“linear” in the course): volume is promising; test sustainability.
- Accelerating additions (“superlinear”): strong volume, still subject to economics and retention.

The source requires increasing, sustainable additions for its PMF growth criterion. State this criterion explicitly rather than treating these labels as universal business definitions. A curve alone does not prove that a growth loop caused it. Check spending, channel mix, incentives, and seasonality.

### Economics

For a consistent acquisition unit and cohort:

`CAC = attributable acquisition cost / acquired units`

`payback months = CAC / monthly gross profit per acquired unit`

With stable average monthly revenue, gross profit can be approximated by `monthly revenue × gross margin fraction`. For irregular revenue or material churn, use cumulative cohort contribution over time instead of extrapolating a constant. Include incentives for both parties, content production/distribution, integration development/fees, advertising/agency costs, or sales costs as applicable. Ensure CAC and revenue use the same user/customer/account denominator.

The source's illustrative payback is $100 / ($15 × 0.80) = 8.33 months. It suggests 6–18 months for new products, varying by customer type, and potentially longer for established organizations. Assess actual runway, cash collection, uncertainty, and margins rather than certifying sustainability from that range alone. Zero or negative contribution means no finite positive payback.

The source also uses `sales revenue / sales-team cost` over a consistent period, with >1 as a sales-efficiency signal. This is a coarse screen, not proof of profitability: inspect margin, sales-cycle lag, revenue recognition, renewal, and fully attributed acquisition cost.

Organic viral and user-generated content loops may have low marginal acquisition cost; verify operating, moderation, infrastructure, and incentive costs instead of assuming they are free.

## Engagement: an early warning

Use the same core action as retention. The course suggests an initial read after two natural periods; history before those periods may be needed to distinguish new from resurrected users. Track **action counts**, not merely user counts.

For each period, separate new, retained base, expansion, resurrection, contraction, and churn. A clear accounting convention is: for users active in consecutive periods, retained base is the smaller action count; expansion or contraction is the difference. New and resurrected contribute their current actions; churn contributes the prior actions lost. Identify resurrection using earlier history.

`quick ratio = (new + expansion + resurrected actions) / (contraction + churned actions)`

Use positive magnitudes for losses; exclude the retained base from this change ratio. If losses are zero, report “no observed losses” (and gains), rather than silently dividing by zero; if both are zero, the ratio is undefined. Verify current actions reconcile with previous actions plus gains minus losses.

The course treats ≤1.5 as concerning and uses 4 as a healthy example. These are diagnostic heuristics. Heavy acquisition can mask weak existing-user engagement even with a high ratio. Inspect the components, and confirm with retention when possible. Resurrection may reflect natural episodic use rather than a broken habit.

## Verdict and recommendation

Use plain-language verdicts such as **insufficient evidence**, **PMF not yet demonstrated**, **promising segment-level signals**, or **strong evidence of PMF for this segment**. These are reporting labels, not a proprietary score.

Provide a compact table of segment, retention evidence, growth/economics evidence, data limitations, and verdict. Strong PMF evidence requires both retained value and sustainable growth in the same segment and relevant period; an exceptional signal in one cannot compensate for failure in the other. Keep low-frequency conclusions provisional where repeat-use evidence is missing.

Distinguish absent evidence from contrary evidence. Interviews, NPS themes, and PMF surveys help explain outcomes and prioritize learning; they do not replace behavioral evidence. Identify the limiting factor, the next corrective action, and the observation that would change the verdict. Improve weak retention before recommending broad acquisition scaling.
