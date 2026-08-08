# Techniques B.27–B.31 and evaluation criteria

Techniques for turning a level of risk into a decision, plus the criteria structures they compare against.

Contents: [B.27 FN curves](#b27-fn-curves) · [B.28 Risk indices](#b28-risk-indices) · [B.29 Consequence/probability matrix](#b29-consequenceprobability-matrix) · [B.30 Cost-benefit analysis](#b30-cost-benefit-analysis) · [B.31 MCDA](#b31-multi-criteria-decision-analysis-mcda) · [ALARP and tolerance criteria](#alarp-and-tolerance-criteria)

> Note on sourcing: the extract of IEC/FDIS 31010 supplied by the user ends partway through B.26. The entries below for B.27–B.31 are written from the Annex A classification tables (which cover all 31 techniques) and standard practice, not from the Annex B text. They are consistent with the standard's treatment but are not transcriptions of it — worth saying if the user is working to a strict compliance requirement, in which case point them to the published Annex B.

---

## B.27 FN curves

**What it is.** A graphical representation of the probability of an event causing at least a given level of harm to a given number of people — plotted as cumulative frequency F (events per year with N or more fatalities, or casualties, or other units of harm) against N, usually on log-log axes.

**When to use.** Societal risk, where the concern is not just expected harm but the aversion society holds toward single events causing many casualties. Standard in land use planning around hazardous installations, transport safety, and major hazard regulation. Also used to compare the risk profiles of alternative designs or sites, and to display historical data alongside predicted risk.

**Needs.** Frequency and consequence data for a range of accident scenarios — typically the output of quantified event tree or consequence modelling. A defined harm unit and population at risk.

**How to run it.** Enumerate the accident scenarios with their frequencies and the number affected in each. Sort by consequence magnitude and compute the cumulative frequency of events with N or more affected. Plot F against N on log-log axes. Compare against tolerability lines where a regulator or the organisation has defined them — typically an unacceptable line above, a broadly acceptable line below, and an ALARP region between.

The slope of the tolerability line encodes risk aversion: a slope steeper than −1 means society weights a single 100-fatality event more heavily than a hundred single-fatality events, which is usually the intent.

**Produces.** A curve showing the whole risk profile rather than a single expected value, compared against tolerance criteria.

**Strengths.** Displays the full distribution of outcomes, so high-consequence/low-probability events remain visible instead of being averaged away. Directly comparable against published societal tolerability criteria. Effective for communicating risk profile to regulators and the public.

**Limitations.** Needs substantial quantified data across many scenarios. Restricted in practice to harm that can be counted in consistent units, usually fatalities — it does not accommodate multi-dimensional consequence. The position of tolerability lines is a policy judgement, not a technical fact, and different jurisdictions place them differently. Aggregating to a single curve hides which scenarios drive which part of it.

---

## B.28 Risk indices

**What it is.** A semi-quantitative measure of risk derived by scoring a set of contributing factors and combining them with a formula. The index is an ordinal score, not a measure of risk in physical units.

**When to use.** Ranking a large number of similar risks quickly and consistently — sites, assets, suppliers, applications, chemicals, projects. The value is comparability across a portfolio, when running a full analysis on each item would be disproportionate. Common instances include environmental contamination indices, supplier risk scores, and vulnerability scoring in information security.

**Needs.** A set of factors known to drive the risk, a scoring scale for each, and a combination rule. The underlying model matters more than the arithmetic: an index is only as good as the causal understanding embedded in its factor selection and weights.

**How to run it.** Identify the factors that drive risk in this class of item. Define a scale and clear anchors for each. Set weights reflecting relative importance. Score each item. Combine by the defined rule. Validate the index against known cases where possible — if items you know to be high risk do not score high, the model is wrong, and this check is skipped far more often than it should be.

**Produces.** A comparable score per item, supporting ranking and threshold-based triage.

**Strengths.** Fast and cheap once built. Consistent across many items and many assessors. Communicates simply. Supports triage — the top of the ranking gets a proper assessment.

**Limitations.** The index is ordinal, so arithmetic on it is largely meaningless: an item scoring 40 is not twice as risky as one scoring 20. Results are highly sensitive to the choice of factors and weights, which are usually judgement, and the resulting number conceals that judgement behind an appearance of objectivity. Validation is frequently omitted. Indices built for one context transfer badly to another. Use for ranking, not for deciding tolerability in absolute terms.

---

## B.29 Consequence/probability matrix

**What it is.** A grid combining categories of consequence with categories of likelihood, with each cell assigned a level of risk. The most widely used risk tool in existence, and the most widely misused.

**When to use.** Ranking risks and screening them for further analysis or treatment, especially where many risks must be compared and quantification is neither possible nor warranted. Effective for communicating results to management audiences. Applicable across every phase of assessment, from identification through to evaluation.

**Needs.** Defined consequence scales with anchors, defined likelihood scales with a stated time period, and a defined rule for what each cell means in terms of action.

**How to build it properly.**
1. Define consequence levels with **anchors that mean something in the context** — not "moderate", but "financial loss of X to Y, or service outage of 4 to 24 hours, or a reportable incident with no lasting harm". Where multiple consequence categories are in play, define the level for each category, and take the highest applicable when rating a risk.
2. Define likelihood levels with an explicit **time period** and, where possible, a frequency band — "expected to occur once or more per year" beats "likely".
3. Decide the grid size. 5×5 is conventional; 4×4 or 3×3 is often more honest when the underlying discrimination is coarse.
4. Assign a risk level to each cell — and design the cell assignment deliberately rather than by multiplying the row and column indices. A catastrophic consequence at low likelihood usually warrants more attention than the product suggests, which is why well-designed matrices are asymmetric.
5. Define what each risk level requires: who must be informed, who must approve acceptance, what timescale treatment must follow.

**Produces.** A level of risk per risk, and a visual distribution of the portfolio.

**Strengths.** Fast and easy to use. Provides rapid ranking into significance bands. Immediately intelligible to non-specialists. Works with qualitative and semi-quantitative input alike.

**Limitations, which are serious and worth stating in the output.**
- The scales are ordinal; multiplying positions on them produces a number without consistent meaning. Two risks in the same cell can demand entirely different responses.
- **Risks with very different characters land in the same cell.** A frequent minor loss and a rare severe one can share a rating while requiring opposite treatments. Analyse those categories separately (see `process.md` §3.2).
- Combining multiple consequence categories into one rating loses information about which objective is threatened.
- Range compression: a "catastrophic" band spanning everything above a threshold hides differences that matter enormously at the extreme.
- It cannot aggregate risks — several tolerable risks that could materialise together may be jointly intolerable, and the matrix will not show it.
- Ratings depend heavily on the rater. Without well-anchored scales and calibration, different assessors place the same risk in different cells; with them, agreement improves markedly.

The matrix is a communication and triage instrument. Do not let it be the whole assessment.

---

## B.30 Cost-benefit analysis

**What it is.** Comparison of the expected costs of a treatment against its expected benefits, both discounted to present value where they occur over time, to decide whether a treatment is worth undertaking and which treatment to prefer.

**When to use.** Justifying or declining treatment spend; choosing between treatment options; supporting ALARP arguments, where the question is explicitly whether the cost of further reduction is disproportionate to the benefit gained. Applicable qualitatively (listing costs and benefits without monetising) or quantitatively.

**Needs.** Treatment costs — capital, operating, and disruption during implementation. Expected benefit, normally the reduction in expected loss: (inherent risk expected loss) minus (residual risk expected loss). A discount rate and a time horizon where effects run over years.

**How to run it.** Establish the baseline expected loss without treatment. Estimate the expected loss with treatment in place. Take the difference as the gross benefit. Subtract the full cost of the treatment, including ongoing operating cost, which is routinely omitted and often dominates. Compute net benefit or a benefit-cost ratio. Test sensitivity to the probability estimates, which are usually the weakest input. Where several treatments are candidates, rank by benefit per unit cost rather than by absolute benefit.

**Produces.** A net benefit or ratio per treatment option; a defensible basis for a spend or no-spend decision.

**Strengths.** Makes the trade-off explicit rather than implicit. Allows comparison across unrelated treatments competing for the same budget. Provides the reasoning that governance bodies and regulators expect for a decision not to treat.

**Limitations.** Requires monetising consequences, which is contentious for safety, health, environmental, and reputational harm, and can be actively inappropriate — cost-benefit reasoning should not be used to justify tolerating a risk that is intolerable in principle. Expected-value framing under-weights catastrophic and irreversible outcomes. Highly sensitive to probability estimates that are often little more than judgement. Discounting systematically diminishes harms that fall on future periods and future people; say so where relevant. Distributional effects are invisible — who bears the cost and who receives the benefit rarely appears in the ratio.

---

## B.31 Multi-criteria decision analysis (MCDA)

**What it is.** A structured method for comparing options against multiple criteria that cannot be reduced to a single unit. Options are scored on each criterion, criteria are weighted, and the weighted scores are combined into an overall ranking.

**When to use.** Choosing between treatment options, designs, sites, or suppliers where the relevant criteria include things money does not capture well — safety, environmental impact, reputation, staff wellbeing, strategic fit, implementation feasibility — alongside cost. The natural complement to cost-benefit analysis where monetisation would distort the decision.

**Needs.** A defined set of options. A set of criteria that are relevant, non-overlapping, and collectively sufficient. A scoring scale per criterion. Weights, ideally elicited from the decision makers rather than assumed by the analyst.

**How to run it.** Define the options and criteria. Score each option against each criterion on a consistent scale, normalising where criteria use different units. Elicit weights — pairwise comparison and swing weighting are the standard methods, and both are better than asking people to distribute 100 points. Compute weighted scores and rank. Then, critically, run a sensitivity analysis on the weights: if the top-ranked option changes under a plausible alternative weighting, the analysis has not settled the question and should say so.

**Produces.** A ranking of options with the reasoning visible, plus an explicit record of the value judgements — the weights — that produced it.

**Strengths.** Handles genuinely multi-dimensional decisions without forcing everything into money. Makes value judgements explicit and debatable rather than buried. Supports group decision-making by separating factual scoring from value weighting. The structure itself often improves the discussion regardless of the number that comes out.

**Limitations.** The result is only as good as the criteria and weights, both of which are judgements that can be gamed, consciously or not, to produce a predetermined answer. Correlated criteria double-count. Compensatory aggregation lets a strong score on one criterion offset an unacceptable score on another, which is wrong where a criterion has a hard threshold — apply thresholds as filters before scoring. Weight elicitation is harder than it looks and is often done carelessly.

---

## ALARP and tolerance criteria

**The three-band structure.** The most useful general framing for evaluation:

- **Unacceptable region** — risk is intolerable whatever the benefit, except in extraordinary circumstances. The activity must be changed or stopped.
- **Tolerable region** — risk is accepted only if it has been reduced as far as reasonably practicable, and only in return for the benefit the activity delivers. This is where most real decisions live.
- **Broadly acceptable region** — risk is negligible; no further action required beyond maintaining existing controls and monitoring.

**ALARP — as low as reasonably practicable.** In the middle band, costs and benefits of further reduction can be compared directly. For higher risks within that band, the position shifts: the potential for harm must be reduced until the cost of further reduction becomes **grossly disproportionate** to the safety benefit gained. The asymmetry is deliberate — the burden of proof sits with not doing more, and it gets heavier as risk rises.

An ALARP argument must be documented to be worth anything: what options were considered, what each would cost, what reduction each would achieve, and why the ones not adopted were judged grossly disproportionate. "We considered it and decided it was too expensive" is not an ALARP demonstration.

**Setting thresholds.** Sources for tolerance criteria, in rough order of authority: legal and regulatory limits; sector standards, including safety integrity levels; contractual obligations; published societal risk criteria; organisational risk appetite statements; and, last, analyst judgement. Where the criterion is judgement, label it as such and get it agreed before rating, not after.

**Practical cautions.**
- A threshold expressed only as a matrix cell colour is not a criterion. State what the boundary means in real terms.
- Different consequence categories usually warrant different tolerance. An organisation may accept far more financial risk than safety risk; make that asymmetry explicit rather than letting one grid imply equivalence.
- Tolerance held by others — regulators, clients, communities, employees — can be far lower than the organisation's own, and their view frequently governs the outcome. Factor it into the evaluation rather than discovering it afterwards.
- Where a risk sits near a threshold, or where its position depends on a contested assumption, say so rather than forcing it to one side.
