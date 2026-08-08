# The six-phase process in detail

Contents:
1. [Establish the context](#1-establish-the-context)
2. [Risk identification](#2-risk-identification)
3. [Risk analysis](#3-risk-analysis)
4. [Risk evaluation](#4-risk-evaluation)
5. [Risk treatment](#5-risk-treatment)
6. [Monitoring and review](#6-monitoring-and-review)
7. [Documentation and communication](#7-documentation-and-communication-runs-throughout)
8. [Life cycle timing](#8-life-cycle-timing)

---

## 1. Establish the context

This phase sets the boundaries and the yardstick. Everything downstream is measured against what you decide here, which is why an assessment that skips it produces ratings that mean nothing.

Four things to pin down.

### External context

The environment the organisation operates in: regulatory and legal requirements, the competitive and market situation, economic and financial conditions, the political and social setting, technology trends, and the perceptions and expectations of external stakeholders. Identify the key drivers and trends that bear on the objectives at stake.

### Internal context

Capabilities and resources, knowledge and expertise available, how information flows and how decisions get made, the objectives and the strategies meant to achieve them, governance and accountability structures, policies and processes, standards and reference models already adopted, and the organisational culture. Internal stakeholders and their interests belong here.

### Process context

The scope and terms of the assessment itself:

- Accountabilities and responsibilities — who owns the assessment, who signs it off, who owns the resulting actions.
- Scope boundaries — what is in, what is explicitly out. Name the exclusions; unnamed exclusions look like oversights later.
- Extent in time and place — which phase of the project, which sites, what horizon.
- Relationships to other projects, activities, and assessments.
- The methodologies and techniques to be used, and why.
- How the assessment's own performance will be judged.
- The decisions and actions the assessment must support. An assessment with no decision attached to it is an artefact, not an input.
- Any scoping or framing studies needed first.

### Risk criteria

The decisive part, and the part most often skipped.

- **Consequence categories** — which types of consequence count. Typically some subset of: safety and health, financial, operational and service continuity, legal and regulatory, environmental, reputational, strategic, data and privacy. Choose the ones that matter for these objectives; do not carry all eight out of habit.
- **Consequence scale** — how each category is measured, with anchors. "Major financial" needs a number or a band; "major reputational" needs a description of what it looks like (national coverage? loss of a licence? a named client leaving?).
- **Likelihood scale** — how probability is expressed: qualitative bands, frequencies over a stated period, or numerical probabilities. Give the period explicitly — "likely" is meaningless without "within the next 12 months".
- **How consequence and likelihood combine** into a level of risk, and whether the combination is a matrix, a formula, or a judgement.
- **Tolerance thresholds** — the level at which a risk requires treatment, and the level at which it is acceptable without treatment. This is the threshold the whole evaluation phase turns on.
- **Whether and how combinations of risks are considered** — several tolerable risks materialising together may not be tolerable.

Criteria can be drawn from agreed objectives, contractual or specification requirements, published data sources, industry norms such as safety integrity levels, legal and regulatory obligations, and stakeholder expectations. Where they come from a source, cite it.

`references/deliverables.md` gives usable default scales to adapt when the user has none.

### Stakeholder involvement

Involving stakeholders early helps define the context accurately, brings in the expertise needed for identification and analysis, ensures different views inform the evaluation, and — critically — secures support for the treatment plan. Note who was consulted and who was not; an assessment produced by one person in isolation should say so.

### Trap to avoid

Producing scales and thresholds without showing them. If the assessment contains a "High" rating anywhere, the reader must be able to find what High means without asking.

---

## 2. Risk identification

The question: **what can happen, and why?**

Identification is where completeness is won or lost. A risk not identified here is not analysed, not treated, and not monitored. Be systematic, and use a technique rather than free association.

### What to look for

- Sources of risk and their causes, including causes that are not immediately visible.
- Events, situations, and circumstances — including things that fail to happen when they should.
- Tangible and intangible consequences, immediate and delayed.
- The existing controls, since a control failure is itself a source of risk.
- Interactions and dependencies — one event can have multiple consequences and hit multiple objectives; consequences of one risk can be causes of another.
- Cumulative and secondary effects on connected systems, activities, and organisations.
- Opportunities as well as threats, where the context frames risk as two-sided.

Include risks whether or not their source is under the organisation's control. External and uncontrollable risks still need treatment, usually through preparedness rather than prevention.

### Structuring the sweep

Work through a deliberate structure rather than by inspiration. Useful frames, chosen to suit the subject:

- By **process step** or system component (suits HAZOP, FMEA, HACCP).
- By **objective** — what could stop each stated objective being met.
- By **source category** — people, process, technology, external, legal, financial, environmental.
- By **stakeholder** — what could go wrong for each affected group.
- By **life cycle phase** — design, build, transition, operate, decommission.

Combine a generative technique (brainstorming, SWIFT, scenario analysis) with a confirmatory one (check-lists) — the first finds the unfamiliar, the second catches the omissions. Check-lists alone address only the known knowns and encourage box-ticking; they should follow the imaginative technique, not replace it.

### Writing the risk statement

Format: **cause/source → event → consequence on a named objective.**

Weak: "Cybersecurity risk."
Better: "Unpatched public-facing VPN appliance (cause) is exploited for initial access (event), exposing client records and triggering mandatory breach notification plus an estimated 3–5 day service outage (consequence, affecting the confidentiality and availability objectives)."

Give every risk a stable ID at this point. Group into categories from the context. Record the identification technique used and who took part.

---

## 3. Risk analysis

The question: **how bad, how likely, and how well is it currently controlled?**

Analysis develops the understanding of the risk. It has five parts and they go in this order.

### 3.1 Controls assessment — do this first

The level of risk depends directly on the adequacy and effectiveness of the controls that exist. Three questions per risk:

- What controls exist for this risk?
- Are they capable of treating it down to a tolerable level?
- Do they operate as intended in practice, and can that be demonstrated when required?

The third question is the one that catches paper controls. Answer it honestly: if the evidence is a policy document rather than an audit result or a test, say so.

Rate control effectiveness on a simple scale — for instance Effective / Partially effective / Ineffective / Unknown, or a 1–5 scale. High precision is rarely warranted, but recording the judgement matters, because it tells you whether effort is better spent improving an existing control or introducing a different treatment altogether. "Unknown" is a legitimate and informative rating; use it rather than guessing.

### 3.2 Consequence analysis

Determine the nature and magnitude of impact, assuming the event has occurred.

- Take account of the controls that reduce consequences (as distinct from those that reduce likelihood).
- Relate consequences back to the stated objectives, in the categories set in the context.
- Consider both immediate consequences and those that emerge after time has passed.
- Consider secondary consequences on connected systems, activities, equipment, and organisations.
- Analyse high-consequence/low-probability and low-consequence/high-probability risks separately. Their treatments differ, and averaging them together hides both.

Depth ranges from a sentence describing the outcome to quantitative modelling or vulnerability analysis, depending on mode and data.

### 3.3 Likelihood analysis

Three approaches; they can be combined, and you should say which you used:

- **Historical data** — identify comparable past events and extrapolate the frequency. The data must be relevant to this type of system, organisation, and operating standard. Where historical frequency is very low, the estimate is very uncertain; zero past occurrences does not mean zero future probability, and should never be recorded as such.
- **Predictive techniques** — fault tree analysis, event tree analysis, simulation. Used where historical data is absent or inadequate. Derive the probability from the system's failure and success states, combining component, human, and organisational data. Make explicit allowance for common-mode failures, where several components fail together from a single cause; ignoring them is the classic way these models come out optimistic.
- **Structured expert judgement** — a systematic process, not a casual guess. Formal methods that reduce bias include the Delphi technique, paired comparisons, category rating, and absolute probability judgements. Draw on all available historical, system-specific, experimental, and design information.

Always attach the time window: probability of what, over what period.

### 3.4 Level of risk

Combine consequence and likelihood into the level of risk, using the method set in the context. Three families:

- **Qualitative** — significance levels such as high/medium/low, evaluated against qualitative criteria. Every term used must be defined and the basis for each criterion recorded. This is the right choice when data is poor; it is not a lesser option, provided the definitions are explicit.
- **Semi-quantitative** — numerical rating scales for consequence and likelihood combined by formula. Scales may be linear, logarithmic, or otherwise; state which. Beware the arithmetic: multiplying ordinal scale positions produces a number that looks measured and is not, and a 5×1 does not carry the same meaning as a 1×5 even though the product is equal.
- **Quantitative** — practical values for consequences and probabilities producing a level of risk in units defined in the context. Full quantification is often impossible or unwarranted — missing information, absent data, human factors, or simply disproportionate effort. Comparative semi-quantitative or qualitative ranking by knowledgeable specialists remains effective in those cases.

Express the level of risk in whatever terms suit that risk and aid evaluation. Sometimes the honest expression is a probability distribution over a range of consequences rather than a single level.

### 3.5 Preliminary screening, uncertainty, and sensitivity

**Screening.** Risks may be screened to focus resources on what matters, using criteria defined in the context. Screening decides one of three things per risk: treat without further assessment; set aside as insignificant; or take forward to detailed assessment. Document the initial assumptions and results — including what was set aside. Guard against screening out low-level risks that occur frequently and accumulate.

**Uncertainty analysis.** Determine the variation or imprecision in the results arising from variation in the parameters and assumptions. Address both data uncertainty and model/method uncertainty. State the completeness and accuracy of the analysis as fully as you can.

**Sensitivity analysis.** Determine how much the level of risk moves when individual inputs change. This identifies which data needs to be accurate and which does not much matter — useful both for interpreting the result and for deciding where to spend effort on better data. Name the parameters the analysis is sensitive to and the degree of sensitivity.

---

## 4. Risk evaluation

The question: **is this tolerable, and does it need treatment?**

Evaluation compares the levels of risk found in analysis against the criteria established in the context, and turns that comparison into a decision. It is a distinct step from analysis; do not collapse them.

Possible outcomes per risk:

- Take no action — the risk is acceptable as it stands.
- Consider treatment options.
- Undertake further analysis to understand the risk better.
- Maintain the existing controls and change nothing else — an active decision, not a default.
- Reconsider or discontinue the activity generating the risk.

Decisions should reflect the wider context, including tolerance held by parties other than the organisation itself — regulators, clients, the public, staff.

Common threshold structures:

- **Simple threshold** — risks above a level require treatment, below it are accepted.
- **Three-band** — an upper band where the risk is intolerable whatever the benefit, a lower band where it is negligible, and a middle band where costs and benefits are weighed against opportunities.
- **ALARP** ("as low as reasonably practicable"), used in safety applications: in the middle band, costs and benefits are compared directly; in the high band, the potential for harm must be reduced until the cost of further reduction is grossly disproportionate to the safety benefit gained. See `techniques-evaluation.md`.

Where risk levels come out close to the threshold, say so rather than forcing a side. Where the ranking is sensitive to a contested assumption, note which risks would move.

Record for each risk: the level, the criterion it was compared against, the evaluation outcome, and the reasoning where the call was not obvious.

---

## 5. Risk treatment

The question: **what do we do about it, and what is left afterwards?**

### Options

Selecting a treatment means balancing implementation cost and effort against the benefit obtained, considering legal, regulatory, and other requirements such as social responsibility and environmental protection. The options, which can be combined:

- **Avoid** — do not start or do not continue the activity that gives rise to the risk.
- **Remove the source** — eliminate the cause rather than managing its effects.
- **Change the likelihood** — preventive controls, redundancy, process change, training, maintenance.
- **Change the consequence** — detective and mitigating controls, containment, backups, recovery capability, contingency plans.
- **Share** — contracts, insurance, partnerships, outsourcing. Note that sharing transfers financial exposure but rarely transfers accountability or reputational consequence; say so where relevant.
- **Retain by informed decision** — accept the risk knowingly, with the acceptance recorded and owned.

Pursuing an opportunity (taking on risk deliberately for gain) is a legitimate seventh option where the context frames risk as two-sided.

### Requirements for each treatment

- Named owner — a role or person, not a department.
- Target date.
- Resources required.
- The expected residual risk after the treatment is in place, rated on the same scales.
- **Secondary risks introduced by the treatment.** New controls create new failure modes; a failover system adds failover-failure risk; encryption adds key-loss risk. Assessments that omit this consistently overstate the benefit of treatment.
- How completion will be verified, and how the treatment's effectiveness will be checked afterwards.

Where the residual risk still exceeds the tolerance threshold, say so explicitly and escalate rather than quietly rounding it down.

### Prioritisation

Rank treatments by risk reduction per unit of cost and effort, not by risk level alone — a modest reduction achieved cheaply on a medium risk can beat an expensive marginal improvement on a high one. Cost-benefit analysis and MCDA are the formal techniques for this; see `techniques-evaluation.md`.

---

## 6. Monitoring and review

The question: **how will we know when this assessment stops being true?**

Assessments decay. Circumstances change, controls degrade, new information arrives, treatments are implemented, and events occur. Build the monitoring in rather than treating it as an afterthought.

For the risks:

- **Indicators (KRIs)** — measurable signals that a risk is becoming more likely or more severe. Prefer leading indicators (rising error rates, staff turnover in a key team, growing backlog) over lagging ones (incidents already occurred). Attach a threshold that triggers action.
- **Triggers for reassessment** — specific events that mandate a fresh look: a major incident, a scope or design change, a regulatory change, loss of a key supplier or person, a control failure.
- **Review cadence** — proportionate to the risk level and volatility. High risks reviewed more often than low ones.

For the assessment itself:

- Verify that assumptions still hold and that the context has not shifted.
- Check that treatments were actually implemented and that they work — implementation is not the same as effectiveness.
- Detect changes in the external and internal context, including changes to the risk criteria themselves.
- Capture emerging risks not present at the time of assessment.
- Learn from events, near misses, successes, and failures, and feed that back into the register.

Assign monitoring responsibilities explicitly, and record the review date and the next review date on the register itself.

---

## 7. Documentation and communication (runs throughout)

Record as you go, not at the end. The assessment record should let a reader who was not there reconstruct how you reached the conclusions:

- Objectives and scope, including exclusions.
- The risk criteria and their source.
- Techniques used, and why they were chosen.
- Who participated, and what expertise they brought.
- Data sources and their limitations.
- Assumptions made, flagged where they are load-bearing.
- Results, and the reasoning behind non-obvious judgements.
- Uncertainties and the sensitivity of conclusions to them.
- Constraints on the assessment itself — time, access, data, expertise.

Consider the sensitivity of the document. A detailed risk register is a map of an organisation's weaknesses; note where circulation should be restricted, particularly for security, safety, or commercially sensitive risks.

Communication should reach both the people who own the risks and the people affected by them, in a form each can act on. A board summary and a working register are different documents.

---

## 8. Life cycle timing

Risk assessment is not a one-off. Where relevant to the subject, note what each phase demands:

- **Concept and definition** — identify feasibility-threatening risks early; supports the decision to proceed. Little data, so preliminary hazard analysis, scenario analysis, and expert judgement dominate.
- **Design and development** — the cheapest point to eliminate risk by design. HAZOP, FMEA, fault tree analysis. Design changes are still practicable here; later they are expensive.
- **Construction, build, or implementation** — verify that assumptions from design hold in reality; catch risks introduced during build.
- **Commissioning and transition** — transition-specific risks, often the highest-exposure window and frequently under-assessed.
- **Operation and maintenance** — ongoing monitoring, control effectiveness verification, incident learning, RCM.
- **Change** — any significant change re-opens the assessment for the affected scope. SWIFT is well suited to change assessment.
- **Decommissioning and disposal** — end-of-life risks including data, environmental, contractual, and knowledge loss. Routinely forgotten; check for it.
