# Techniques B.13–B.26 — function, control, and statistical analysis

Read the entries for the techniques you have selected.

Contents: [B.13 FMEA / FMECA](#b13-fmea-and-fmeca) · [B.14 Fault tree analysis](#b14-fault-tree-analysis-fta) · [B.15 Event tree analysis](#b15-event-tree-analysis-eta) · [B.16 Cause-consequence analysis](#b16-cause-consequence-analysis) · [B.17 Cause-and-effect analysis](#b17-cause-and-effect-analysis-ishikawa) · [B.18 LOPA](#b18-layers-of-protection-analysis-lopa) · [B.19 Decision tree analysis](#b19-decision-tree-analysis) · [B.20 Human reliability assessment](#b20-human-reliability-assessment-hra) · [B.21 Bow tie analysis](#b21-bow-tie-analysis) · [B.22 Reliability-centred maintenance](#b22-reliability-centred-maintenance-rcm) · [B.23 Sneak analysis](#b23-sneak-analysis-and-sneak-circuit-analysis) · [B.24 Markov analysis](#b24-markov-analysis) · [B.25 Monte Carlo simulation](#b25-monte-carlo-simulation) · [B.26 Bayesian statistics and Bayes nets](#b26-bayesian-statistics-and-bayes-nets)

---

## B.13 FMEA and FMECA

**What it is.** Failure modes and effects analysis identifies the ways components, systems, or processes can fail to fulfil their design intent. It establishes: all potential failure modes of the parts of a system (a failure mode being what is observed to fail or perform incorrectly); the effects those failures have on the system; the mechanisms of failure; and how to avoid the failures or mitigate their effects.

FMECA extends FMEA by ranking each identified failure mode by importance or criticality. The criticality analysis is usually qualitative or semi-quantitative, but can be quantified using actual failure rates.

**Variants.** Design (or product) FMEA for components and products; System FMEA for systems; Process FMEA for manufacturing and assembly; Service FMEA; Software FMEA. Applicable during design, manufacture, or operation.

**Needs.** Understanding of the system and its components in enough detail to identify how each part can fail. Drawings, process flow, functional breakdown. For quantified criticality, failure rate data.

**How to run it.**
1. Define the scope and boundary of the system, and break it into components, elements, or process steps.
2. For each item, define its function and its design intent.
3. Identify every way it could fail to deliver that intent — the failure modes.
4. For each failure mode, identify the mechanism (why it fails) and the effects, both local and on the wider system.
5. Identify the existing controls: those that prevent the failure and those that detect it.
6. Rate each failure mode. Common semi-quantitative scheme: severity (S) of the effect, occurrence (O) of the cause, detection (D) — the chance the failure escapes detection before it does damage. The **risk priority number** is S × O × D.
7. Rank and select failure modes for treatment; define corrective actions with owners; re-rate the residual.

**Produces.** A tabulated register of failure modes with causes, effects, existing controls, ratings, and actions.

**Strengths.** Highly systematic — its exhaustiveness is the point. Works at component level where responsibility is clear and fixes are concrete. Widely understood, so results travel well. Feeds naturally into fault tree analysis and maintenance planning.

**Limitations.** Analyses single-point failures well and combinations badly — two individually tolerable failures that together cause an outage will not appear. Effort scales with component count and becomes punishing on large systems. RPN arithmetic is a known weak point: multiplying ordinal scales gives numbers with no consistent meaning, and a severity-10/occurrence-1 failure and a severity-2/occurrence-5 failure can score similarly while demanding entirely different responses. Read RPN as a sorting aid, never as a measurement, and always look at severity separately. Depends on the analyst knowing the failure modes in the first place.

---

## B.14 Fault tree analysis (FTA)

**What it is.** A deductive technique that starts from one specified undesired event — the **top event** — and works backwards to identify and organise all the factors that could contribute to it, represented as a logic tree of causal factors linked by AND and OR gates. Factors can be hardware failures, human errors, or any other relevant events.

**When to use.** Qualitatively, to identify causes and pathways to a failure. Quantitatively, to calculate the top event's probability from the probabilities of the causal events. At design stage to find potential causes of failure and choose between design options; at operating stage to see how major failures occur and which pathways matter most; and after a failure, to display how events combined to produce it.

**Needs.** For qualitative work: understanding of the system, its failure causes, and how it can fail technically; detailed diagrams help. For quantitative work: failure rate or failed-state probability data for every base event in the tree.

**How to run it.**
1. Define the top event. This may be a failure itself, or a broader outcome of that failure — if you analyse the outcome, the tree will include a section on mitigation of the failure.
2. Identify the immediate causes or failure modes that could lead to the top event.
3. Analyse each of those to identify what could cause it.
4. Continue to successively lower system levels until further analysis stops being productive — in a hardware system, usually the component failure level. The lowest-level events are the **base events**.
5. Where probabilities can be assigned to base events, calculate the top event probability. **Validity condition:** for each gate, all inputs must be both necessary and sufficient to produce the output event. Where this cannot be shown, the tree is not valid for probability analysis, though it may still be a useful display of causal relationships.
6. Simplify with Boolean algebra to handle duplicate failure modes appearing in several places.
7. Identify the **minimal cut sets** — the individual separate pathways to the top event — and calculate each one's influence.

Beyond simple trees, use software: it handles repeated events, computes minimal cut sets, and supports consistency, correctness, and verifiability.

**Produces.** A picture of how the top event can occur, showing interacting pathways where two or more events must occur together; a list of minimal cut sets with their probabilities where data exists; the probability of the top event.

**Strengths.** Disciplined and highly systematic, yet flexible enough to cover human interactions and physical phenomena alongside hardware. The top-down approach keeps attention on the effects that matter for the top event. Especially good for systems with many interfaces and interactions. The picture makes system behaviour intelligible. Cut set analysis exposes simple failure pathways in very complex systems, where a particular combination of events would otherwise be overlooked.

**Limitations.** Uncertainty in base event probabilities propagates into the top event probability, which can be very large where base data is poor — though a well-understood system supports high confidence. Where causal events are not bounded, it can be impossible to know whether all important pathways are included (the classic example: enumerating all ignition sources for a fire top event), and probability analysis then is not possible. It is a **static** model — time interdependencies are not addressed. It handles **binary states only** (failed / not failed). Human error modes can appear in a qualitative tree, but failures of degree or quality, which is what most human error looks like, do not fit. Domino effects and conditional failures are awkward to include.

**Reference standards.** IEC 61025, *Fault tree analysis*; IEC 60300-3-9, *Dependability management — Risk analysis of technological systems*.

---

## B.15 Event tree analysis (ETA)

**What it is.** The forward-looking counterpart of FTA. A graphical technique representing the mutually exclusive sequences of events that follow an initiating event, branching according to whether each mitigating system functions or fails. Applicable qualitatively and quantitatively.

**When to use.** Modelling the range of outcomes from a single initiating event, and quantifying the frequency of each. Excellent for assessing whether layers of mitigation actually cover the outcomes, and for showing the consequences of a mitigation failing.

**Needs.** A defined initiating event with a known or estimated frequency. Identification of every mitigating system, barrier, or intervention in the sequence, with the probability that each functions.

**How to run it.**
1. Define the initiating event and its frequency.
2. Identify, in chronological order, each system, barrier, or human intervention that could alter the outcome.
3. Draw a branch at each: functions (with probability p) or fails (1−p). Order matters — barriers must appear in the order they act.
4. Trace every pathway to its outcome and describe that outcome.
5. Multiply the initiating frequency by the branch probabilities along each path to get the frequency of each outcome.
6. Check the outcome frequencies sum sensibly against the initiating frequency.

Worked shape: a fire starting at 10⁻² per year, branching on whether the sprinkler system works and whether the alarm activates, yields distinct outcome branches (controlled fire with alarm, controlled fire without alarm, uncontrolled fire, and so on) each with its own annual frequency.

**Produces.** A picture of every outcome pathway from the initiating event, with frequencies; identification of which barrier failures drive the worst outcomes.

**Strengths.** Displays potential scenarios following an initiating event and the influence of each system on the outcome, in an intuitive form. Accounts for timing and sequence — dependencies and domino effects that a fault tree cannot capture. Shows graphically where mitigation is thin.

**Limitations.** Needs all potential initiating events identified by some other technique first — miss an initiator and you miss everything downstream of it. Handles only success/failure of each system, so partial success and degraded operation are hard to represent. Any pathway is conditional on the events that came before it, and dependencies between systems along the path (a shared power supply, a shared operator) are easy to overlook and will make the numbers optimistic. Trees become large fast.

---

## B.16 Cause-consequence analysis

**What it is.** A combination of fault tree and event tree analysis. It starts from a critical event and works backwards with fault tree logic to the causes, and forwards with event tree logic to the consequences. Its distinguishing feature is that it allows **time delays** to be incorporated, which neither parent technique handles.

**When to use.** Where an event has both a complex causal structure and a branching set of consequences, and where sequence and timing matter — process safety, emergency response, systems where the time available for intervention is decisive.

**Needs.** Understanding of the system, its failure modes, and its mitigating systems; the inputs of both FTA and ETA.

**How to run it.** Define the critical (initiating) event. Build the fault tree beneath it to establish causes and their probability. Build the event tree above it to establish consequence pathways, incorporating time delays where a mitigating action must occur within a window. Combine to produce consequence frequencies.

**Produces.** A diagram spanning causes through to consequences, with the frequency of each outcome.

**Strengths.** Covers the whole causal chain in one model. Handles time dependencies and sequential mitigation that FTA cannot. Well suited to systems where multiple mitigation layers act in sequence.

**Limitations.** More complex to build and to communicate than either parent technique. Inherits the data demands of both. Not suited to problems where causes and consequences are poorly bounded.

---

## B.17 Cause-and-effect analysis (Ishikawa)

**What it is.** A structured method for identifying possible causes of an undesirable event or problem, organising contributory factors into broad categories so all hypotheses get considered. It does **not** identify actual causes — those can only be established by real evidence and empirical testing. Displayed as a fishbone (Ishikawa) diagram or, sometimes, a tree.

**When to use.** Best at the start of an analysis, to broaden thinking about possible causes and establish hypotheses that can then be tested more formally. Use it when you need to identify the possible root causes of a specific effect, sort out the interactions among factors affecting a process, or analyse an existing problem so corrective action can be taken. Frequently used as a method within root cause analysis.

**Needs.** Expertise and experience from the participants, or a previously developed model.

**How to run it.**
1. State the effect to be analysed and put it in a box. It may be negative (a problem) or positive (an objective).
2. Determine the main categories of cause. For a system problem these might be people, equipment, environment, processes — but choose them to fit the context.
3. Fill in possible causes under each category, with branches and sub-branches showing relationships.
4. Keep asking "why?" or "what caused that?" to extend the chains.
5. Review all branches for consistency and completeness, and check each cause actually bears on the main effect.
6. Identify the most likely causes from team judgement and available evidence.

The tree form resembles a fault tree but usually runs left to right. It cannot be quantified into a head-event probability, because its entries are possible contributory factors rather than failures with known probabilities.

**Produces.** A fishbone or tree diagram of possible and likely causes — which must then be verified and tested empirically before recommendations follow.

**Strengths.** Brings relevant experts together in a structured way. Considers all likely hypotheses. Graphical and easy to read. Highlights where further data is needed. Works on positive effects too, and a positive framing tends to increase ownership and participation.

**Limitations.** The team may lack the necessary expertise. Not a complete process — it needs to sit inside a root cause analysis to produce recommendations. It is really a display technique for brainstorming rather than a standalone analysis. Separating causes into categories at the outset means interactions **between** categories get under-examined — equipment failure caused by human error, or human error caused by poor design, sit awkwardly in a single-category structure. Quantification is generally invalid, because contributory factors interact in complex ways.

---

## B.18 Layers of protection analysis (LOPA)

**What it is.** A semi-quantitative method for estimating the risk of an undesired event and judging whether the protective measures are sufficient. A single cause-consequence pair is selected, the layers of protection between them are identified, and an order-of-magnitude calculation determines whether protection reduces risk to a tolerable level.

**When to use.** Qualitatively to review the protection layers between a hazard and an outcome; normally semi-quantitatively to add rigour to screening, typically **after** a HAZOP or preliminary hazard analysis. Provides the basis for specifying independent protection layers and safety integrity levels for instrumented systems under IEC 61508 and IEC 61511. Helps allocate risk-reduction resources by showing the reduction each layer contributes.

**Needs.** Basic information on hazards, causes, and consequences (as from a PHA); information on controls in place or proposed; initiating cause frequencies; protection layer failure probabilities; consequence measures; and a definition of tolerable risk.

**How to run it.** With a team of experts:
1. Identify initiating causes for the undesired outcome; obtain data on frequencies and consequences.
2. Select a single cause-consequence pair.
3. Identify the layers of protection that prevent the cause reaching the consequence, and analyse their effectiveness.
4. Identify which of them are **independent protection layers (IPLs)** — not all protection layers qualify.
5. Estimate the probability of failure on demand of each IPL.
6. Combine the initiating cause frequency with the failure probabilities of each IPL and with any conditional modifiers (for example, whether a person will be present to be harmed) to get the frequency of the undesired consequence. Work in orders of magnitude.
7. Compare the calculated risk against tolerance levels to decide whether further protection is required.

**What counts as an IPL.** A device, system, or action capable of preventing the scenario reaching its undesired consequence, **independent** of the causal event and of every other protection layer in the scenario. Qualifying examples: design features; physical protection devices; interlocks and shutdown systems; critical alarms with manual intervention; post-event physical protection; emergency response systems. **Procedures and inspections are not IPLs** — a common and consequential error.

**Produces.** Recommendations for further controls and an assessment of their effectiveness in reducing risk. One of the standard techniques for SIL assessment of safety-instrumented systems.

**Strengths.** Much less time and resource than fault tree analysis or full quantitative risk assessment, while far more rigorous than qualitative judgement. Focuses resources on the most critical protection layers. Identifies operations and systems with insufficient safeguards. Concentrates on the most serious consequences.

**Limitations.** Handles one cause-consequence pair and one scenario at a time, so complex interactions between risks or between controls fall outside it. Quantified risks may not account for common-mode failures — the shared cause that defeats several layers at once. Does not suit very complex scenarios with many cause-consequence pairs or varied consequences affecting different stakeholders.

**Reference standards.** IEC 61508 (all parts), *Functional safety of electrical/electronic/programmable electronic safety-related systems*; IEC 61511, *Functional safety – Safety instrumented systems for the process industry sector*.

---

## B.19 Decision tree analysis

**What it is.** A sequential representation of decision alternatives and outcomes that accounts for uncertainty. Similar in structure to an event tree, but it starts from an initial decision as well as from chance events, and models the pathways resulting from both the events that may occur and the decisions that may be made.

**When to use.** Managing project risks and, more generally, selecting the best course of action under uncertainty. The graphical form also helps communicate the reasoning behind a decision — often as valuable as the calculation.

**Needs.** A plan with identified decision points. Information on the possible outcomes of each decision and on the chance events that could affect them, with probabilities and outcome values.

**How to run it.** Start from the initial decision — say, proceed with option A rather than option B. As each option unfolds, different events occur and further predictable decisions arise; lay these out in tree form. Estimate the probability of each event and the cost or utility of each pathway's final outcome. The best decision pathway is the one with the highest expected value, computed as the product of all conditional probabilities along the pathway and the outcome value.

Distinguish decision nodes (you choose) from chance nodes (the world chooses) in the diagram; conflating them is the most common construction error.

**Produces.** A logical analysis of the risk showing the options available, and an expected value for each possible path.

**Strengths.** Clear graphical representation of a decision problem's structure. Enables calculation of the best pathway.

**Limitations.** Large trees become too complex to communicate. There is a real tendency to oversimplify the situation in order to fit it into a tree — and expected-value reasoning implicitly assumes risk neutrality, which is rarely appropriate where a bad outcome is catastrophic or irreversible. Say so when the expected value and the prudent choice diverge.

---

## B.20 Human reliability assessment (HRA)

**What it is.** Assessment of the impact of humans on system performance, used to evaluate the influence of human error on the system.

Many processes contain the potential for human error, especially where the operator has little time to decide. The probability of problems developing far enough to become serious may be small — but sometimes human action is the only defence preventing an initial failure from progressing to an accident. Major accidents in which critical human error drove a catastrophic sequence stand as a warning against risk assessments that look only at hardware and software. HRA also highlights errors that impede productivity, and reveals how errors and hardware or software failures can be **recovered** by operators and maintenance staff — recovery being as important to model as error.

**When to use.** Qualitatively, to identify the potential for human error and its causes so that error probability can be reduced. Quantitatively, to supply human failure data into fault tree analysis or other techniques.

**Needs.** Information defining the tasks people are supposed to perform; experience of the errors that occur in practice and the potential for error; expertise in human error and its quantification.

**How to run it.**
1. **Problem definition** — which human involvements are being assessed.
2. **Task analysis** — how the task will be performed, and what aids support performance.
3. **Human error analysis** — how task performance can fail: what errors can occur, and how they can be recovered.
4. **Representation** — how those errors integrate with hardware, software, and environmental events so that overall system failure probabilities can be calculated.
5. **Screening** — where the number of interactions is large, screen to focus on those that matter.
6. **Quantification** — assign error probabilities, accounting for performance-shaping factors: time pressure, workload, training, fatigue, interface design, procedures, stress, and organisational culture.
7. **Impact assessment and error reduction** — identify where design, procedure, training, or interface change would reduce error probability or improve recovery.

**Produces.** A list of errors that could occur with their causes; error probabilities for input to other models; identification of where recovery is possible; recommendations for error reduction.

**Strengths.** Brings human factors into an assessment that would otherwise implicitly assume perfect operators. Structured and, at its best, quantifiable. Often reveals productivity problems alongside safety ones.

**Limitations.** Human variability is far harder to model than component failure, and error probability data has wide uncertainty bounds. Results are sensitive to performance-shaping factor judgements. Considerable expertise is needed to do it properly. Poorly applied, it can slide into blaming operators for what are really design and organisational failures — keep the analysis pointed at the conditions that make error likely.

---

## B.21 Bow tie analysis

**What it is.** A simple diagrammatic way of describing and analysing the pathways of a risk from hazards through to outcomes, and of reviewing the controls on each side. It can be understood as a fault tree analysing the causes of an event — represented by the knot of the tie — joined to an event tree analysing its consequences.

**When to use.** Where a clear picture of the pathways and controls around a central event is more useful than a full quantitative model, and where the audience includes people who will not read a fault tree. Excellent for communicating control ownership: every barrier on the diagram has someone accountable for it. Widely used in safety, security, and operational risk.

**Needs.** A defined top event, understanding of its causes and consequences, and an inventory of controls.

**How to run it.**
1. Place the **top event** at the knot — the moment of loss of control, not the consequence.
2. To the left, identify the **threats or causes** that could produce it.
3. To the right, identify the **consequences** that could follow.
4. On each left-hand pathway, place the **preventive barriers** that stop that cause reaching the top event.
5. On each right-hand pathway, place the **mitigating barriers** that limit that consequence.
6. Identify **escalation factors** — conditions that could defeat a barrier — and the controls on those.
7. Assign an owner to every barrier, and rate each barrier's effectiveness.

**Produces.** A single readable diagram of causes, controls, event, and consequences, with barrier ownership and effectiveness — the clearest artefact in the toolkit for showing where protection is thin.

**Strengths.** Immediately intelligible to non-specialists. Shows preventive and mitigating controls in one view. Makes barrier gaps visible. Supports accountability by attaching an owner to each barrier. Less effort than a full FTA/ETA pair.

**Limitations.** Cannot depict complex combinations of causes as a fault tree can — AND logic in particular is lost in the simplified form. Handles one top event at a time. The apparent completeness of the picture can be misleading when barriers share a common failure cause that the diagram does not show. Semi-quantitative at best.

---

## B.22 Reliability-centred maintenance (RCM)

**What it is.** A method for identifying the policies that should be implemented to manage failures, so as to achieve the required safety, availability, and economy of operation efficiently and effectively for all types of equipment.

**When to use.** Defining a maintenance regime for physical assets, and reviewing an existing one. Also useful for asking whether current maintenance actually addresses the failure modes that matter, which is frequently not the case.

**Needs.** Understanding of the equipment, its functions and performance standards, its failure modes and their consequences, and the maintenance options available.

**How to run it.** For each significant asset, answer in sequence: What are its functions and required performance standards? In what ways can it fail to fulfil them? What causes each failure? What happens when each failure occurs? How does each failure matter — safety, environmental, operational, or economic consequence? What can be done to predict or prevent each failure? What should be done if no suitable preventive task exists (redesign, run to failure, scheduled discard)?

Maintenance tasks resulting will be predictive (condition-based), preventive (scheduled restoration or discard), detective (failure-finding for hidden failures), or a decision to run to failure where that is economically rational and safe.

**Produces.** A maintenance policy per failure mode, with justification, and identification of failure modes requiring redesign rather than maintenance.

**Strengths.** Directs maintenance effort at consequence rather than at equipment criticality alone. Covers the whole assessment process, from identification through evaluation. Often reduces maintenance cost while improving availability, by eliminating tasks that address failure modes that do not matter.

**Limitations.** Resource-intensive on large asset bases. Needs good failure data and equipment knowledge. Focused on physical equipment, so it transfers poorly to organisational or information risk.

**Reference standard.** IEC 60300-3-11, *Dependability management — Reliability centred maintenance*.

---

## B.23 Sneak analysis and sneak circuit analysis

**What it is.** A methodology for identifying design errors. A **sneak condition** is a latent hardware, software, or integrated condition that can cause an unwanted event to occur or inhibit a desired event, and which is **not caused by component failure**. Sneak conditions are characterised by their random nature and their ability to escape detection through even rigorous standardised system testing. They can cause improper operation, loss of availability, programme delays, or injury and death.

**When to use.** Design review of systems where an unintended path — electrical, logical, or procedural — could produce an unwanted outcome even though every component works exactly as specified. Historically electrical and electronic systems; the concept transfers to software logic, permission models, and workflow design, where an unintended sequence produces an unintended state.

**Needs.** Detailed design documentation — circuit diagrams, code, logic specifications, procedural definitions — at a level allowing paths to be traced.

**How to run it.** Reduce the design to topological network trees or path structures. Compare each pattern against known sneak patterns (typically: sneak paths, where current or control flows along an unintended route; sneak timing, where events occur in an unexpected order; sneak indications, where a display misleads the operator; and sneak labels, where labelling induces incorrect action). Trace each path for unintended function, and report the conditions found with recommended design corrections.

**Produces.** A list of sneak conditions and design errors, with recommendations.

**Strengths.** Finds a class of problem that failure-based techniques structurally cannot, because nothing has failed. Catches design errors that survive testing.

**Limitations.** Requires very detailed design documentation and specialist expertise. Labour-intensive. Contributes to identification only, so it must be paired with other techniques for analysis and evaluation. Little value for systems that are not path-structured.

---

## B.24 Markov analysis

**What it is.** Sometimes called state-space analysis. Commonly used for repairable complex systems that can exist in multiple states, including various degraded states. It models the system as a set of states and the transition rates between them, then solves for the probability of being in each state.

**When to use.** Where the assumption that FTA makes — binary states, no repair, no time dependence — is too coarse. Systems with redundancy, repair, standby, or degraded operating modes. Availability and downtime calculations.

**Needs.** Definition of all the system states, transition rates between them (failure rates and repair rates), and the Markov property: the probability of the next state depends only on the current state, not on the history that reached it. Where that assumption fails, so does the model.

**How to run it.** Enumerate the states the system can occupy (fully operational, degraded modes, failed). Define the transitions between states and their rates. Build the transition matrix. Solve for state probabilities — steady-state for long-run availability, or time-dependent for a defined mission period. Derive the metrics that matter: availability, mean time between failures, expected downtime, probability of being in a failed state at a given time.

**Produces.** State probabilities over time or at steady state; system availability and reliability metrics.

**Strengths.** Handles repair, redundancy, and degraded states that static techniques cannot. Time-dependent, so it answers questions about availability rather than only about failure probability. Well-supported by software.

**Limitations.** The Markov assumption is a genuine restriction — where transition probability depends on how long the system has been in a state, or on its history, the model is wrong rather than merely approximate. The state space explodes combinatorially with system size, quickly becoming unmanageable. Requires transition rate data and specialist expertise. Results are opaque to non-specialists, which limits their usefulness in decision forums unless carefully translated.

**Reference standard.** IEC 61165, *Application of Markov techniques*.

---

## B.25 Monte Carlo simulation

**What it is.** A method for establishing the aggregate variation in a system that results from variation in its inputs, where each input has a defined distribution and the inputs relate to the output through defined relationships. It works by sampling the input distributions repeatedly and recording the resulting output, building up the output distribution empirically.

**When to use.** Where analytical techniques cannot deliver relevant results, or where there is uncertainty in the input data and therefore in the outputs. Standard applications: uncertainty in financial forecasts, investment performance, project cost and schedule forecasts, business interruption, and staffing requirements. In practice this is the technique of choice for "what is the realistic range of project cost or duration".

**Needs.** A model relating inputs to outputs. A distribution for each uncertain input — triangular and beta distributions are common in risk work, because they can be specified from a minimum, most likely, and maximum estimate that experts can actually supply. Enough iterations for the result to converge.

**How to run it.** Build the model. Assign a distribution to each uncertain input, choosing the distribution type to reflect the nature of the uncertainty rather than convenience. Run many iterations, sampling each input from its distribution and computing the output. Track convergence — a small number of runs gives a result that should not be trusted; tens of thousands of iterations is routine and cheap. Analyse the output distribution, and analyse the relationship between inputs and outputs to see which inputs drive the variation.

**Produces.** A single value, a probability or frequency distribution, or identification of the model functions with the greatest impact on the output. Typically used to give either the probability of a defined outcome arising, or the value at a stated confidence level — a cost with less than a 10% chance of being exceeded, or a duration that is 80% certain to be exceeded. Examining input-output relationships shows the relative significance of the factors at work and identifies the best targets for reducing uncertainty.

**Strengths.** Can in principle accommodate any input distribution, including empirical distributions from observation of related systems. Models are relatively simple to build and extend. Any real influence or relationship can be represented, including subtle effects such as conditional dependencies. Sensitivity analysis identifies strong and weak influences. The input-output relationship is transparent, so models are understandable. Provides a measure of the accuracy of its own result. Software is readily available and inexpensive.

**Limitations.** Accuracy depends on the number of simulations performed — less of a constraint than it once was. It relies on being able to represent parameter uncertainty by a valid distribution, and choosing a distribution because it is convenient rather than because it fits is the standard way these models go wrong. Large, complex models challenge the modeller and can make it hard for stakeholders to engage with the process. The technique may not adequately weight high-consequence/low-probability events, so an organisation's risk appetite may not be reflected in the analysis — check the tail explicitly rather than reading only the mean and the P80.

**Reference standards.** IEC 61649, *Weibull analysis*; IEC 62551, *Analysis techniques for dependability – Petri net techniques*; ISO/IEC Guide 98-3 (GUM).

---

## B.26 Bayesian statistics and Bayes nets

**What it is.** The premise is that already-known information (the prior) can be combined with subsequent measurement to establish an overall probability (the posterior). In simple form: P(A|B) = P(A)P(B|A) / P(B).

Bayesian statistics differs from classical statistics in not assuming that distribution parameters are fixed — parameters are treated as random variables. A Bayesian probability is most easily understood as a degree of belief in an event, as against the classical view grounded in physical evidence. Because it rests on a subjective interpretation of probability, it provides a natural basis for decision thinking, and for Bayes nets.

**Bayes nets** use a graphical model to represent a set of variables and their probabilistic relationships: nodes are random variables, and arrows link a parent node to a child node, where the parent directly influences the child.

**When to use.** Widely used and increasingly accessible thanks to software tools. Applications span medical diagnosis, image modelling, genetics, speech recognition, economics, space exploration, and search. Valuable anywhere unknown variables must be inferred from structural relationships and data. Bayes nets can learn causal relationships, giving understanding of a problem domain, and can predict the consequences of intervention. In risk work, they are the right choice when evidence arrives incrementally and beliefs must be updated, and when expert judgement must be combined with sparse data.

**Needs.** Similar to a Monte Carlo model. For a Bayes net: define the system variables; define the causal links between them; specify conditional and prior probabilities; add evidence to the net; perform belief updating; extract the posterior beliefs.

**The counter-intuitive result to remember.** Take a screening test where 1% of the population has the condition, the test is positive 98% of the time for those who have it, and positive 10% of the time for those who do not. A positive result raises the probability of having the condition from 1% to roughly 9% — meaning that even after a positive test, the condition remains unlikely. The false-positive rate among the large negative population dominates. Exactly this structure appears in risk work whenever a detection control is applied to a rare event: alerts, fraud screening, anomaly detection, audit sampling. If an assessment credits a detection control without doing this arithmetic, it is probably overstating the control's value.

**Produces.** The same range of outputs as classical statistics — point estimators, confidence intervals — plus, for Bayes nets, posterior distributions. The graphical output gives an easily understood model, and the data can be readily modified to explore correlations and parameter sensitivity.

**Strengths.** All that is needed is knowledge of the priors. Inferential statements are easy to understand. Bayes' rule is the only machinery required. It provides a principled mechanism for using subjective belief in a problem — which is what most risk assessment actually runs on.

**Limitations.** Defining all the interactions in a Bayes net for a complex system is genuinely problematic, and the number of conditional probabilities required grows fast with the number of parents per node. Results depend on the accuracy of the priors; a badly chosen prior propagates through everything downstream. There is no universally accepted method for selecting priors, and the choice is open to challenge — state it explicitly and test the sensitivity of the conclusion to it.
