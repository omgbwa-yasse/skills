# Techniques B.1–B.12 — identification and scenario methods

Read the entries for the techniques you have selected. Each gives what it is for, what it needs, how to run it, and where it fails.

Contents: [B.1 Brainstorming](#b1-brainstorming) · [B.2 Structured and semi-structured interviews](#b2-structured-and-semi-structured-interviews) · [B.3 Delphi technique](#b3-delphi-technique) · [B.4 Check-lists](#b4-check-lists) · [B.5 Preliminary hazard analysis](#b5-preliminary-hazard-analysis-pha) · [B.6 HAZOP](#b6-hazop) · [B.7 HACCP](#b7-hazard-analysis-and-critical-control-points-haccp) · [B.8 Environmental and toxicity assessment](#b8-environmental-and-toxicity-risk-assessment) · [B.9 SWIFT](#b9-structured-what-if-technique-swift) · [B.10 Scenario analysis](#b10-scenario-analysis) · [B.11 Business impact analysis](#b11-business-impact-analysis-bia) · [B.12 Root cause analysis](#b12-root-cause-analysis-rca)

---

## B.1 Brainstorming

**What it is.** Free-flowing structured conversation among knowledgeable people to surface failure modes, hazards, decision criteria, or treatment options. True brainstorming is not just "a group discussion" — it uses specific devices to make each person's thinking trigger the next person's.

**When to use.** Identification, at any stage of the process or life cycle. Strongest where imagination matters most: new technology, no historical data, novel problems needing novel solutions. Works standalone or as the front end of another technique.

**Needs.** A team with knowledge of the organisation, system, or process. A facilitator who can start the conversation, keep it moving, redirect when a line is exhausted, and capture what emerges.

**How to run it (formal version).**
1. Facilitator prepares prompts and triggers suited to the context beforehand.
2. Objectives and rules are stated at the start.
3. The facilitator opens a line of thought; participants generate as many issues as possible. No debate at this stage about whether an item belongs on the list or what a statement means — that inhibits flow. Accept everything, criticise nothing, move fast so ideas trigger lateral thinking.
4. The facilitator opens a new direction when one is exhausted or the discussion drifts too far.
5. Evaluation and grouping happen afterwards, as a separate activity.

Informal brainstorming skips the preparation and structure; useful but less defensible.

**Produces.** Depends on the phase — at identification, typically a list of risks and the controls currently believed to be in place.

**Strengths.** Encourages imagination, so it finds new risks and novel solutions. Involves stakeholders and improves communication. Quick and cheap to set up.

**Limitations.** Participants may lack the knowledge to contribute usefully. Being unstructured, it cannot demonstrate comprehensiveness — you cannot show all risks were considered. Group dynamics distort it: dominant voices crowd out quieter people with better ideas. Mitigations: anonymous computer brainstorming or a chat forum, which also defuses political sensitivities; or nominal group technique, where ideas go to a moderator anonymously before group discussion.

**When Claude runs this alone.** Simulate the breadth honestly — generate from multiple distinct perspectives (operator, attacker, maintainer, customer, regulator, supplier, new joiner) rather than one voice. Then say explicitly that a real workshop with the named stakeholders would surface risks no desk exercise can.

---

## B.2 Structured and semi-structured interviews

**What it is.** Individual interviewees work through a prepared question set designed to make them view the situation from a particular angle and identify the risks visible from there. Semi-structured adds freedom to follow what emerges.

**When to use.** Where a group session is impractical, or where free discussion in a group is inappropriate for the people or the subject — sensitive topics, hierarchical dynamics, dispersed teams. Most often for identification or for assessing existing control effectiveness. A good route for stakeholder input at any project stage.

**Needs.** Clear interview objectives, a list of interviewees drawn from relevant stakeholders, a prepared question set.

**How to run it.** Build questions that are open-ended where possible, simple, in the interviewee's own vocabulary, and each covering one issue only. Prepare follow-ups for clarification. Do not lead the interviewee. Hold responses flexibly so the interviewee can take you somewhere you had not planned to go — that is often where the useful material is.

**Produces.** Stakeholder views on the subject.

**Strengths.** Gives people time for considered thought. One-to-one allows depth a group session cannot reach. Reaches more stakeholders in total than a single workshop.

**Limitations.** Time-consuming for the facilitator to gather many opinions this way. Bias is preserved rather than corrected, because there is no group challenge. Loses the cross-triggering of imagination that makes brainstorming productive.

---

## B.3 Delphi technique

**What it is.** A structured procedure for reaching a reliable consensus among experts. The essential feature — often lost when the name is used loosely — is that experts contribute individually and anonymously while seeing the group's evolving views between rounds.

**When to use.** Any phase, any life cycle stage, wherever an expert consensus is needed and status, personality, or politics would distort an open discussion. Particularly good for estimating probabilities or consequences where no data exists.

**Needs.** A set of questions or options requiring consensus, and a panel of genuine experts.

**How to run it.**
1. Form a team to run and monitor the process.
2. Select the expert panel (one or more panels).
3. Develop the round-1 questionnaire; test it before sending.
4. Send it to panellists individually.
5. Analyse and combine the responses, then circulate the aggregated result back to the panel.
6. Panellists respond again in light of the group view. Repeat until convergence.

**Produces.** Convergence toward consensus, plus a visible record of where consensus was not reached — which is itself valuable information about uncertainty.

**Strengths.** Anonymity means unpopular but correct opinions get expressed. All views carry equal weight, defusing dominant personalities. Participants take ownership of the outcome. No need to assemble people in one place at one time.

**Limitations.** Labour-intensive and slow — multiple rounds take weeks. Panellists must be able to express themselves clearly in writing.

---

## B.4 Check-lists

**What it is.** Lists of hazards, risks, or control failures compiled from experience — previous assessments, past failures, industry codes, standards.

**When to use.** Identification of hazards and risks, or assessment of control effectiveness. Any life cycle stage. Most valuable as a completeness check **after** an imaginative technique has been run, not as the primary method.

**Needs.** Enough prior knowledge to select or build a relevant, ideally validated list.

**How to run it.** Define the scope of the activity. Select a check-list that genuinely covers that scope — and match the list to the purpose, since a list of standard controls cannot identify new hazards. Step through each element of the process or system and check each item's presence and adequacy.

**Produces.** Depending on phase: a list of risks, or a list of inadequate controls.

**Strengths.** Usable by non-experts. A well-built list packages wide expertise into a simple instrument. Ensures common problems are not forgotten.

**Limitations.** Inhibits imagination. Covers known knowns only — not known unknowns, and certainly not unknown unknowns. Encourages tick-box behaviour where the goal becomes completing the list rather than understanding the system. Observation-based, so it misses what is not readily visible.

---

## B.5 Preliminary hazard analysis (PHA)

**What it is.** A simple inductive method to identify the hazards, hazardous situations, and events that could cause harm in a given activity, facility, or system.

**When to use.** Early in a project, when design details and operating procedures barely exist — often as a precursor to further study or to inform design specification. Also useful on existing systems to prioritise hazards for deeper analysis, or where circumstances rule out a more extensive technique.

**Needs.** Information about the system, and whatever design detail is available and relevant.

**How to run it.** Build a list of hazards and generic hazardous situations by working through the system's characteristics: materials used or produced and their reactivity; equipment employed; the operating environment; layout; and the interfaces between system components. Add a qualitative analysis of the consequences and probabilities of unwanted events to flag which risks need further assessment. Update through design, construction, and testing as new hazards appear. Present as tables or trees.

**Produces.** A list of hazards and risks, plus recommendations: acceptance, recommended controls, design specification requirements, or requests for more detailed assessment.

**Strengths.** Works with limited information. Puts risk on the table early, while design change is still cheap.

**Limitations.** Preliminary by definition — not comprehensive, and it does not tell you in detail how risks are best prevented.

---

## B.6 HAZOP

**What it is.** Hazard and operability study: a structured, systematic examination of a planned or existing product, process, procedure, or system, using guidewords to question how the design intent might not be achieved at each step. Qualitative, team-based, run through facilitated workshops. The team is also expected to propose treatments.

HAZOP and FMEA both identify failure modes, causes, and consequences, but from opposite directions: FMEA starts from failure modes; HAZOP starts from unwanted outcomes and deviations from intent, and works back to causes.

**When to use.** Originally chemical process systems, now extended to mechanical and electronic systems, procedures, software, organisational change, and even contract design and review. Widely used for software design review; applied to safety-critical instrument control and computer systems it is sometimes called CHAZOP. Best run at detailed design, when a full diagram exists but changes are still practicable. Can be phased across a developing design with different guidewords per stage. Possible during operation, but changes are expensive by then.

**Needs.** Current information on the system, process, or procedure, plus the design intent and performance specification. Typically drawings, specification sheets, flow sheets, process control and logic diagrams, layout drawings, operating, maintenance, and emergency procedures. For non-hardware HAZOP, any document describing the functions and elements — organisational diagrams, role descriptions, a draft contract, a draft procedure.

**How to run it.**
1. Nominate someone with the responsibility and authority to run the study and to ensure resulting actions get completed.
2. Define objectives and scope.
3. Establish the guideword set.
4. Form a multidisciplinary team including design and operations staff with the expertise to judge the effect of deviations. Include at least one person not involved in the design under review.
5. Collect the documentation.
6. In workshop: split the system into smaller elements or sub-processes to make review tractable.
7. Agree the design intent for each sub-element. Apply each guideword in turn to postulate deviations with undesirable outcomes.
8. For each undesirable outcome, agree cause and consequences, and propose prevention or mitigation.
9. Document the discussion and agree specific treatment actions with owners.

**Guidewords.** Standard technical set: *no/not* (none of the intended result achieved, or the intended condition absent), *more/higher* (quantitative increase), *less/lower* (quantitative decrease), *as well as* (something additional), *part of* (something missing from a composite), *reverse/opposite* (e.g. backflow), *other than* (something completely different happens), *compatibility* (material, environment). Apply them to parameters such as physical properties, physical conditions (temperature, pressure, speed), the specified intention of a component (e.g. information transfer), and operational aspects.

For human error, use an analogous set: *too early*, *too late*, *too much*, *too little*, *too long*, *too short*, *wrong direction*, *wrong object*, *wrong action*.

Customise guidewords to the domain. For an information system, parameters might be data flow, access, integrity, timing, and volume.

**Produces.** Minutes recording, for each review point: guideword used, deviation, possible causes, consequences, actions, and the person responsible. Any deviation that cannot be corrected gets its risk assessed.

**Strengths.** Systematic and thorough. Brings in a multidisciplinary team including people with real operational experience and those who will carry out the treatments. Generates solutions, not just findings. Applies to a wide range of systems. Handles human error causes and consequences explicitly. Creates a written record demonstrating due diligence.

**Limitations.** Slow and expensive when done in detail. Requires a high level of documentation or specification. Tends to find detailed solutions rather than challenge fundamental assumptions — a phased approach mitigates this. Focuses on design detail and can miss wider or external issues. Constrained by the design as drafted and by the scope the team was given. Relies heavily on the designers, who may struggle to be objective about their own design.

**Reference standard.** IEC 61882, *Hazard and operability studies (HAZOP studies) – Application guide*.

---

## B.7 Hazard analysis and critical control points (HACCP)

**What it is.** A structure for identifying hazards and placing controls at every relevant point in a process, so that risk is minimised by control throughout rather than by inspecting the end product.

**When to use.** Developed for food safety (originally for NASA), now standard across the food chain, and extended to pharmaceuticals and medical devices. The underlying principle — identify what can affect output quality, define the points where critical parameters can be monitored and hazards controlled — generalises to other technical and information systems.

**Needs.** A process or flow diagram, information on the hazards that could affect quality, safety, or reliability of the output, and information on how those hazards can be controlled. Note that HACCP consumes hazard identification rather than performing it, so it usually needs another technique upstream.

**How to run it — the seven principles.**
1. Identify hazards and the preventive measures for them.
2. Determine the critical control points (CCPs) — the points where each hazard can be controlled or eliminated.
3. Establish critical limits for each CCP: the parameters within which it must operate for the hazard to be controlled.
4. Monitor those critical limits at defined intervals.
5. Establish corrective actions for when the process moves outside its limits.
6. Establish verification procedures.
7. Implement record-keeping and documentation for each step.

**Produces.** A hazard analysis worksheet listing, for each process step: the hazards that could be introduced, controlled, or worsened there; whether they present a significant risk and the justification for that judgement; possible preventive measures; and whether monitoring or control can be applied at that step (i.e. whether it is a CCP). Plus a HACCP plan listing every CCP with its critical limits, monitoring activities (what, how, when, by whom), corrective actions on deviation, and verification and record-keeping activities.

**Strengths.** A structured process producing documented evidence for quality control as well as reduced risk. Focuses on the practicalities of where and how hazards can actually be prevented. Controls risk throughout rather than relying on final inspection. Identifies hazards introduced by human action and where they can be caught.

**Limitations.** Depends on hazards being identified, their risks defined, and their significance understood as inputs — usually requiring another technique first. Acting only when limits are breached can miss gradual drift in control parameters that is statistically significant well before the limit is crossed.

**Reference standard.** ISO 22000, *Food safety management systems*.

---

## B.8 Environmental and toxicity risk assessment

**What it is.** Assessment of risk to plants, animals, and humans from exposure to environmental hazards. It analyses the hazard and how it affects the target population, the pathways by which the hazard reaches a susceptible target, and combines the two into an estimate of the likely extent and nature of harm.

**When to use.** Exposure of populations to chemicals, micro-organisms, or introduced species. More broadly, the **pathway analysis** component — mapping the routes by which a target might be exposed to a source of risk — adapts to a very wide range of risk areas well outside health and environment, and is particularly good at showing where controls can be inserted. Consider it wherever a hazard must travel a route to reach what it harms: contamination, information leakage, supply chain contamination, malware propagation.

**Needs.** Good data on the nature and properties of the hazards, the susceptibility of the target population, and how the two interact — normally from laboratory or epidemiological research.

**How to run it.**
1. **Problem formulation** — set the scope: which target populations and hazard types are of interest.
2. **Hazard identification** — identify all possible sources of harm to the target within scope, from expert knowledge and literature review.
3. **Hazard analysis** — understand the hazard and how it interacts with the target. For chemical exposure this covers acute and chronic toxicity, genotoxicity, carcinogenicity, teratogenicity. Compare the magnitude of effect (response) against the amount of exposure (dose) and determine the mechanism where possible. Note the No Observable Effect Level (NOEL) and No Observable Adverse Effect Level (NOAEL), which are sometimes used as acceptability criteria. Dose-response curves are usually derived from animal tests or cultured tissue. For micro-organisms or introduced species, use field data and epidemiological studies.
4. **Exposure analysis** — how a hazardous substance or its residues could reach a susceptible target, and in what amount. This is where pathway analysis sits: the routes the hazard might take, the barriers that might stop it, and the factors influencing exposure level.
5. **Risk characterisation** — combine hazard and exposure analysis to estimate the probabilities of particular consequences across all pathways. Where hazards or pathways are numerous, screen first and run the detailed work on the higher-risk scenarios.

**Produces.** The level of risk from exposure of a particular target to a particular hazard in context — quantitatively (e.g. probability of developing a condition over a period given a specified exposure), semi-quantitatively (a risk index), or qualitatively (a level, or a description of likely effects with supporting data).

**Strengths.** Produces a detailed understanding of the problem and the factors that increase risk. Pathway analysis shows precisely where controls can be improved or added.

**Limitations.** Needs good data, which is often unavailable or highly uncertain. Extrapolating from high-dose animal studies to low-dose human effects requires model choices, and several competing models exist. Where the target is an ecosystem and the hazard is not chemical, directly relevant data is often thin.

---

## B.9 Structured "what-if" technique (SWIFT)

**What it is.** A simpler, faster alternative to HAZOP. A systematic team study using prompt words or phrases, combined with "what-if" questions, to explore how a system, item, organisation, or procedure would be affected by deviations from normal operation. Runs at a higher level with less granularity than HAZOP.

**When to use.** Designed for chemical and petrochemical plant, now applied broadly to systems, procedures, and organisations. Particularly good for examining the consequences of **change** — which risks are altered or created. One of the four techniques applicable across the whole process, which makes it a strong default when one technique must do everything.

**Needs.** A careful definition of the system, procedure, item, or change before starting. External and internal context established through interviews and document review by the facilitator. The subject is normally split into nodes or key elements, though rarely to HAZOP's level of granularity. A carefully selected team representing all stakeholders where possible, plus people with experience of similar systems or changes.

**How to run it.**
1. Facilitator prepares a prompt list of words or phrases beforehand — standard or purpose-built for comprehensive coverage.
2. In the workshop, discuss and agree the context and scope.
3. Ask participants to raise and discuss: known risks and hazards; previous experience and incidents; existing controls and safeguards; regulatory requirements and constraints.
4. Drive discussion by combining a "what-if" phrase with a prompt word: *"what if…"*, *"what would happen if…"*, *"could someone or something…"*, *"has anyone or anything ever…"*. The aim is to push the team into scenarios, causes, consequences, and impacts.
5. Summarise each risk; consider the controls in place.
6. Confirm and record the risk description, causes, consequences, and expected controls with the team.
7. Have the team judge whether controls are adequate and effective and agree a statement of control effectiveness. Where it is less than satisfactory, define treatment tasks and potential additional controls.
8. Pose further "what-if" questions as the discussion opens new ground.
9. Facilitator uses the prompt list to monitor coverage and introduce issues the team has not raised.
10. Rank the resulting actions by priority using a qualitative or semi-quantitative risk assessment that accounts for existing controls and their effectiveness.

**Produces.** A risk register with risk-ranked actions, which becomes the basis of a treatment plan.

**Strengths.** Applies to almost anything — plant, system, situation, organisation, activity. Minimal team preparation. Fast: major risks emerge within the session. Systems-oriented, so participants examine how the system responds to deviation rather than only the consequences of component failure. Identifies improvement opportunities and success-enhancing actions, not only threats. Involving the people accountable for controls and treatments reinforces their ownership. Produces the register and treatment plan almost as a by-product. Can feed identified risks into a subsequent quantitative study.

**Limitations.** Needs an experienced, capable facilitator. Careful preparation is essential or the team's time is wasted. If the team's experience base is too narrow, or the prompt list not comprehensive, risks get missed. The high-level application may not reveal complex, detailed, or correlated causes — that is what HAZOP is for.

---

## B.10 Scenario analysis

**What it is.** Development of descriptive models of how the future might turn out, used to identify risks by exploring the implications of possible developments. Sets of scenarios — best case, worst case, expected case — support consequence and probability analysis and act as a form of sensitivity analysis.

Scenario analysis cannot predict the probability of major shifts, but it can examine consequences and help build the strength and resilience to adapt.

**When to use.** Policy decisions, strategy, and long-horizon planning, as well as review of existing activities. Contributes to all three assessment components. Works for threats and opportunities, short and long term. With short horizons and good data, scenarios extrapolate from the present; with long horizons or weak data it becomes more imaginative, sometimes called futures analysis. Useful where positive and negative outcomes are distributed unevenly across space, time, or groups.

**Needs.** A team that between them understands the nature of relevant change and can think forward without simply extrapolating the past. Access to literature and data on changes already underway.

**How to run it.**
1. Establish the team and communication channels; define the context, problem, and issues.
2. Identify the nature of changes that could occur. This requires research into major trends and their probable timing, plus imaginative thinking. Consider: external changes such as technology; decisions due soon whose outcomes could vary; how stakeholder needs might shift; macro-environment changes such as regulation and demographics — some inevitable, some uncertain. Note that a change may itself be the consequence of another risk.
3. List local and macro factors or trends, then rank them twice: by **importance** and by **uncertainty**. Concentrate on those that are both most important and most uncertain.
4. Map key factors against each other to reveal where scenarios can be developed.
5. Propose a series of scenarios, each turning on a plausible change in parameters.
6. Write a "story" for each — how you get from here to there. Plausible detail makes scenarios usable.
7. Test the original question or proposal against each scenario: how successful would this policy or activity be here? Use "what if" questions on the model assumptions, allowing for significant but predictable factors.
8. Modify the proposal where a scenario shows it to be fragile.
9. Identify **leading indicators** that show a scenario is starting to materialise. Monitoring these creates the opportunity to change strategy in time — this step is what converts scenario analysis from an interesting exercise into a management tool.
10. Because scenarios are only slices of possible futures, make some attempt to express the probability of each occurring.

**Produces.** Usually no single best-fit scenario, but a clearer view of the range of options and how to adjust course as indicators move.

**Strengths.** Takes a genuine range of futures into account, rather than high/medium/low forecasts that assume the future follows past trends. Valuable where current knowledge is thin or the horizon is long.

**Limitations.** Under high uncertainty some scenarios will be unrealistic. Depends on data availability and on the analysts' ability to build realistic, probe-able scenarios. As a decision tool it is dangerous when scenarios lack foundation, data is speculative, or unrealistic results are not recognised as such.

---

## B.11 Business impact analysis (BIA)

**What it is.** Analysis of how key disruption risks would affect operations, and identification and quantification of the capability needed to manage them. It produces an agreed understanding of: which business processes, functions, and resources are critical and how they interdepend; how disruptive events would affect the capacity to achieve critical objectives; and what capability is needed to manage a disruption and recover to agreed operating levels.

**When to use.** Determining the criticality and recovery timeframes of processes and their supporting resources — people, equipment, information technology. Also for mapping interdependencies between processes, internal and external parties, and supply chain links. The foundation of business continuity planning.

**Needs.** A team to do the analysis and develop the plan. Information on objectives, environment, operations, and interdependencies. Detail on activities and operations: processes, supporting resources, relationships with other organisations, outsourcing arrangements, stakeholders. Financial and operational consequences of losing critical processes. A prepared questionnaire and a list of interviewees across relevant areas.

**How to run it.** Questionnaires, interviews, structured workshops, or a combination. Key steps:

1. Confirm the key processes and outputs, based on the risk and vulnerability assessment, to determine criticality.
2. Determine the consequences of disruption to each critical process, in financial and operational terms, over defined periods. The time dimension is essential — an outage costs differently at one hour, one day, and one week.
3. Identify interdependencies with key internal and external stakeholders, including mapping the nature of supply chain dependencies.
4. Determine currently available resources and the essential minimum needed to keep operating at an acceptable level after a disruption.
5. Identify alternative workarounds and processes, in use or planned. New ones may need developing where resources are inaccessible or insufficient during disruption.
6. Determine the **maximum acceptable outage (MAO)** for each process — the longest period the organisation can tolerate losing that capability — based on the consequences and the function's critical success factors.
7. Determine the **recovery time objective (RTO)** for specialised equipment or IT: the time within which recovery is targeted.
8. Confirm the current level of preparedness of each critical process — redundancy, spare equipment, alternate suppliers.

**Produces.** A prioritised list of critical processes and their interdependencies; documented financial and operational impacts of losing them; the supporting resources they need; and outage timeframes with associated IT recovery timeframes.

**Strengths.** Produces genuine understanding of which processes let the organisation keep meeting its objectives, and what resources they require. Creates the opportunity to redesign operations for resilience.

**Limitations.** Participants completing questionnaires or attending workshops may lack the knowledge needed. Group dynamics can distort the analysis of a process. Recovery expectations are frequently simplistic or over-optimistic — RTOs are routinely stated as what is wanted rather than what is achievable, and should be challenged. Obtaining an adequate understanding of the organisation's operations is genuinely difficult.

---

## B.12 Root cause analysis (RCA)

**What it is.** Analysis of a loss that has already occurred, to prevent recurrence. Also called root cause failure analysis or loss analysis — RCA typically addresses asset losses from failures, loss analysis financial or economic losses from external factors or catastrophes. The point is to reach the original causes rather than treating the immediately obvious symptoms. Corrective action is not always fully effective, so continuous improvement is usually needed.

**When to use.** Most often on a single major loss, but also across many losses to find where systemic improvement is possible. Broad areas of application: safety-based RCA for accident investigation and occupational health and safety; failure analysis for reliability and maintenance in technological systems; production-based RCA in manufacturing quality control; process-based RCA for business processes; system-based RCA combining these for complex systems, applied in change management, risk management, and systems analysis.

**Needs.** All the evidence gathered from the failure or loss. Data from similar past failures. Results of any tests run to check specific hypotheses.

**How to run it.**
1. Appoint a group of experts with the specific expertise needed to analyse this failure.
2. Establish the scope and objectives.
3. Gather data and evidence from the failure.
4. Perform a structured analysis to determine the root cause.
5. Develop solutions and make recommendations.
6. Implement the recommendations.
7. Verify that the implemented recommendations worked.

**Structured analysis methods to use at step 4:** the "5 whys" (repeatedly asking why to peel away layers of cause and sub-cause); FMEA; fault tree analysis; Ishikawa/fishbone diagrams; Pareto analysis; root cause mapping.

**The causal ladder.** Evaluation of causes typically progresses from the physical causes that are evident first, to human-related causes, and finally to underlying management or systemic causes. Stopping at the physical cause produces a fix that does not prevent recurrence. Stopping at "human error" is worse — it usually names a symptom of a system that made the error likely. Push to causes the involved parties can actually control or eliminate, because only those support effective corrective action.

**Produces.** Documentation of data and evidence gathered; the hypotheses considered; a conclusion on the most likely root causes; recommendations for corrective action.

**Strengths.** Applicable experts working as a team. Structured analysis. All likely hypotheses considered. Documented results. Forces final recommendations.

**Limitations.** The required experts may not be available. Critical evidence may be destroyed in the failure itself or lost during clean-up. The team may not get enough time or resources to evaluate the situation fully. Recommendations may not be implementable in practice.
