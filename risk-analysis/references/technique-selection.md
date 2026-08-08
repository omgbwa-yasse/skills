# Choosing the right technique

Read this before selecting techniques, and whenever the user asks which method suits their problem. Always state your choice and the reason for it in the assessment.

Contents:
1. [The four selection factors](#1-the-four-selection-factors)
2. [Applicability matrix](#2-applicability-matrix)
3. [Resource and output profile](#3-resource-and-output-profile)
4. [Selection by situation](#4-selection-by-situation)
5. [Combining techniques](#5-combining-techniques)
6. [Selection traps](#6-selection-traps)

---

## 1. The four selection factors

Weigh these four against each other. There is no universally best technique; there is a technique that fits this problem, this data, and this budget.

**Availability of resources.** The skills and experience of the team, the time and budget available, the organisation's constraints, and whether the necessary data exists or would have to be generated. A technique nobody in the room can run properly produces worse output than a simpler one run well.

**Nature and degree of uncertainty.** How much is known, and how good is that knowledge. Where uncertainty is high — novel systems, sparse data, contested models — techniques resting on structured judgement and imagination (Delphi, scenario analysis, SWIFT) outperform techniques that demand data the situation cannot supply. Where the system is well understood and instrumented, quantitative techniques earn their cost.

**Complexity.** Simple, decomposable systems suit component-level techniques (FMEA, check-lists). Complex systems with interacting parts, feedback, degraded states, or human involvement need techniques that model the interactions (fault tree, event tree, Markov, Bayes nets, HRA). Applying a component technique to a complex system produces a comprehensive list of small failures and misses the emergent ones.

**Whether quantitative output is needed.** Some decisions require a number — insurance, capital allocation, safety integrity levels, regulatory thresholds. Many do not, and reaching for a quantitative technique without the data to feed it manufactures false precision. Ask what the decision actually needs before choosing.

Two further practical constraints: whether the technique's results can be verified or audited, and whether any legislation or sector standard prescribes a particular methodology. Prescribed methods override preference.

---

## 2. Applicability matrix

How each technique serves each phase. **SA** = strongly applicable, **A** = applicable, **NA** = not applicable.

| # | Technique | Identify | Consequence | Probability | Level of risk | Evaluate |
|---|---|---|---|---|---|---|
| B1 | Brainstorming | SA | NA | NA | NA | NA |
| B2 | Structured / semi-structured interviews | SA | NA | NA | NA | NA |
| B3 | Delphi technique | SA | NA | NA | NA | NA |
| B4 | Check-lists | SA | NA | NA | NA | NA |
| B5 | Preliminary hazard analysis (PHA) | SA | NA | NA | NA | NA |
| B6 | HAZOP | SA | SA | A | A | A |
| B7 | HACCP | SA | SA | NA | NA | SA |
| B8 | Environmental / toxicity risk assessment | SA | SA | SA | SA | SA |
| B9 | SWIFT (structured "what-if") | SA | SA | SA | SA | SA |
| B10 | Scenario analysis | SA | SA | A | A | A |
| B11 | Business impact analysis (BIA) | A | SA | A | A | A |
| B12 | Root cause analysis (RCA) | NA | SA | SA | SA | SA |
| B13 | FMEA / FMECA | SA | SA | SA | SA | SA |
| B14 | Fault tree analysis (FTA) | A | NA | SA | A | A |
| B15 | Event tree analysis (ETA) | A | SA | A | A | NA |
| B16 | Cause-consequence analysis | A | SA | SA | A | A |
| B17 | Cause-and-effect analysis (Ishikawa) | SA | SA | NA | NA | NA |
| B18 | Layers of protection analysis (LOPA) | A | SA | A | A | NA |
| B19 | Decision tree analysis | NA | SA | SA | A | A |
| B20 | Human reliability assessment (HRA) | SA | SA | SA | SA | A |
| B21 | Bow tie analysis | NA | A | SA | SA | A |
| B22 | Reliability-centred maintenance (RCM) | SA | SA | SA | SA | SA |
| B23 | Sneak analysis / sneak circuit analysis | A | NA | NA | NA | NA |
| B24 | Markov analysis | A | SA | NA | NA | NA |
| B25 | Monte Carlo simulation | NA | NA | NA | NA | SA |
| B26 | Bayesian statistics and Bayes nets | NA | SA | NA | NA | SA |
| B27 | FN curves | A | SA | SA | A | SA |
| B28 | Risk indices | A | SA | SA | A | SA |
| B29 | Consequence/probability matrix | SA | SA | SA | SA | A |
| B30 | Cost-benefit analysis | A | SA | A | A | A |
| B31 | Multi-criteria decision analysis (MCDA) | A | SA | A | SA | A |

Read the matrix as guidance on fit, not permission. "SA" for identification does not mean the technique is sufficient on its own; brainstorming is strongly applicable to identification and contributes nothing to analysis, which is exactly why it needs a partner technique.

Note the shape of it: the broadly applicable techniques (B8, B9, B13, B22) cover the whole process and are the safest default when one technique must do everything. The identification-only cluster (B1–B5) is cheap and always needs a follow-on. The quantitative cluster (B14, B24, B25, B26) is narrow and expensive and only pays off with data.

---

## 3. Resource and output profile

Approximate profiles to weigh cost against what you get back. Treat these as orientation, not fixed values — the same technique run at screening depth and at certification depth differ by an order of magnitude.

**Low resource demand, qualitative output:** check-lists, brainstorming, preliminary hazard analysis, structured interviews, cause-and-effect analysis, consequence/probability matrix.

**Moderate resource demand, qualitative to semi-quantitative output:** Delphi, SWIFT, scenario analysis, root cause analysis, business impact analysis, FMEA/FMECA, bow tie analysis, decision tree, risk indices, cost-benefit analysis, MCDA.

**High resource demand, semi-quantitative to quantitative output:** HAZOP (thorough application), HACCP, environmental and toxicity assessment, fault tree analysis, event tree analysis, cause-consequence analysis, LOPA, human reliability assessment, reliability-centred maintenance, sneak analysis, Markov analysis, Monte Carlo simulation, Bayes nets, FN curves.

**Can produce genuinely quantitative output when fed adequate data:** FTA, ETA, cause-consequence, LOPA, Markov, Monte Carlo, Bayes nets, FN curves, HRA, decision tree, cost-benefit analysis, environmental/toxicity assessment, FMECA with failure rate data.

**Tolerates high uncertainty and sparse data well:** Delphi, scenario analysis, SWIFT, brainstorming, preliminary hazard analysis, structured interviews, Bayes nets (which are built to combine prior belief with new evidence).

**Degrades badly under sparse data — avoid unless the data exists:** Monte Carlo, Markov, quantitative FTA/ETA, FN curves, LOPA with quantified layers. These will still produce a confident-looking number from bad inputs, which is precisely the danger.

---

## 4. Selection by situation

Start from the problem, not the technique.

| The situation | Consider |
|---|---|
| Novel system or technology, no precedent, no data | Brainstorming, Delphi, scenario analysis, preliminary hazard analysis |
| Well-documented process with defined design intent | HAZOP (detailed), SWIFT (systems level, faster) |
| Components or products that can fail in identifiable ways | FMEA; FMECA when criticality ranking is needed |
| One specific undesired outcome; want all the ways it could happen | Fault tree analysis |
| One initiating event; want the range of outcomes it could lead to | Event tree analysis |
| Both directions at once, plus the controls on each side | Bow tie analysis; cause-consequence analysis where timing matters |
| An incident already happened; prevent recurrence | Root cause analysis (5 whys, Ishikawa, Pareto, fault tree, root cause mapping) |
| Continuity, recovery times, critical process dependencies | Business impact analysis |
| Human error is central | Human reliability assessment; HAZOP with human-error guidewords |
| Verifying whether protective layers are sufficient | LOPA |
| Repairable system with multiple degraded states | Markov analysis |
| Aggregating many uncertain inputs into an output distribution | Monte Carlo simulation |
| Updating belief as new evidence arrives; causal networks | Bayesian statistics and Bayes nets |
| Choosing between options with uncertain outcomes | Decision tree analysis; MCDA where criteria are multiple and non-monetary |
| Justifying spend on treatment | Cost-benefit analysis; ALARP reasoning |
| Ranking many risks quickly for a management audience | Consequence/probability matrix; risk indices |
| Societal or multi-fatality risk against tolerance lines | FN curves |
| Maintenance policy for equipment | Reliability-centred maintenance |
| Process where hazards must be controlled at specific points | HACCP |
| Latent design conditions not caused by component failure | Sneak analysis |
| Exposure of people or ecosystems to a hazardous agent | Environmental / toxicity assessment with pathway analysis |
| Consensus needed from dispersed or unequal-status experts | Delphi technique |
| Long-horizon strategy under deep uncertainty | Scenario analysis |
| Assessing a change to an existing system | SWIFT, with HAZOP for the changed portion if safety-critical |

---

## 5. Combining techniques

Complex applications usually need more than one technique. Design the combination so each covers the others' blind spots.

Reliable pairings:

- **Generative + confirmatory** for identification: brainstorming or SWIFT to find the unfamiliar, then a check-list to catch the omissions. Order matters — the check-list last, or it anchors thinking and suppresses discovery.
- **Identification + causal structure + evaluation**: SWIFT or HAZOP → FMEA or bow tie → consequence/probability matrix. The everyday backbone.
- **Fault tree + event tree** joined at the event = bow tie, or cause-consequence analysis when time delays and sequencing matter.
- **Qualitative screening + quantitative deep dive**: preliminary hazard analysis or a matrix to triage, then FTA, Markov, or Monte Carlo on the few risks that justify the cost.
- **Expert judgement + structure**: Delphi to elicit inputs, feeding a Bayes net, FMEA, or fault tree that gives the judgement a structure to sit in.
- **Analysis + decision**: any analysis technique → cost-benefit analysis or MCDA to select among treatment options.

---

## 6. Selection traps

**Defaulting to matrix-and-brainstorm.** It is the right answer surprisingly often, but choose it, and say why, rather than arriving at it by inertia.

**Quantifying because quantification looks rigorous.** A Monte Carlo run on invented distributions is less honest than a well-defined qualitative rating, and much harder for a reader to challenge.

**Applying a component technique to an emergent problem.** FMEA on a complex socio-technical system yields a long list of component failures and misses the interaction that actually causes the outage.

**Using check-lists as the only identification technique.** They address known knowns, inhibit imagination, encourage box-ticking, and are observation-based, so they miss what is not readily visible.

**Ignoring a prescribed methodology.** Some sectors and regulators mandate specific techniques. Check before choosing, and follow the requirement.

**Choosing a technique the team cannot run.** HAZOP without a trained facilitator, or Bayes nets without someone who understands conditional independence, produces output that carries the technique's authority without its rigour.
