---
name: risk-analysis
description: Run a complete ISO/IEC 31010 risk assessment — establish the context, identify, analyse, evaluate, treat, and monitor risks — choosing deliberately among the 31 standard techniques (HAZOP, SWIFT, FMEA/FMECA, fault tree, event tree, bow tie, LOPA, Delphi, scenario analysis, business impact analysis, root cause analysis, Markov, Monte Carlo, Bayes nets, consequence/probability matrix, cost-benefit, MCDA and the rest). Use this whenever the user mentions risk assessment, risk analysis, a risk register, a risk matrix, threat or hazard analysis, failure modes, business continuity, mitigation or contingency planning, "what could go wrong", or asks to assess the safety, reliability, continuity, or exposure of any project, system, process, supplier, or decision — even when no technique is named and the standard is never mentioned. Also use to review an existing risk register, to pick the technique that fits a problem, and for any request to rate or rank risks. Domain-agnostic. Always write the assessment in English.
---

# Risk Analysis (ISO/IEC 31010)

Assess risk the way a competent practitioner does: define what you are assessing and against what criteria, find what can go wrong, work out how bad and how likely given the controls that actually exist, judge it against the criteria, decide what to do, and set up the monitoring that keeps the assessment alive.

The failure mode this skill exists to prevent is the plausible-looking risk table produced without context, criteria, or evidence — a 5×5 grid of invented numbers that looks rigorous and decides nothing. Every step below is there to stop that.

**Write all output in English**, regardless of the language of the request. Reply conversationally in the user's language if they wrote in another one, but the assessment itself, the register, headings, and technique names are English.

## Before anything else: pick the depth

Match effort to the decision at stake. Three modes:

| Mode | When | What it looks like |
|---|---|---|
| **Rapid** | Screening, a single decision, a short conversation, low stakes | Context in a short paragraph, one identification technique, qualitative scales, 5–15 risks, register + evaluation. Inline. |
| **Standard** | The usual case: a project, system, process, or supplier under real scrutiny | Full six-phase pass, 2–3 techniques chosen deliberately, controls assessed, 15–40 risks, treatment plan with owners. File deliverable. |
| **Deep** | Safety-critical, regulated, quantified, or contested | Multiple techniques including at least one structural (FTA/ETA/bow tie/Markov) or quantitative one, uncertainty and sensitivity analysis, explicit data provenance per risk. |

State which mode you are in at the top of the assessment. If the user's brief clearly warrants Deep but they have asked for something quick, do the Rapid pass and say plainly what a deeper analysis would add.

## The six phases

Follow them in order. Read `references/process.md` for the detail of each — what to ask, what to produce, and the traps. The summary:

1. **Establish the context** — external, internal, and process context, plus the risk criteria. Never skip this; the criteria decide every rating that follows. See "Non-negotiables" below.
2. **Identify risks** — what can happen and why. Comprehensive here or the whole assessment inherits the gap.
3. **Analyse risks** — assess the existing controls first, then consequences, then likelihood, then the level of risk. Record the uncertainty.
4. **Evaluate risks** — compare the level of risk against the criteria from phase 1 and decide: accept, treat, analyse further, or reconsider the activity.
5. **Treat risks** — choose treatment options, name owners and dates, state the residual risk and any secondary risks the treatment creates.
6. **Monitor and review** — indicators, triggers, and a review cadence, so the assessment does not silently go stale.

Documentation runs across all six, not at the end. Capture assumptions as you make them.

**Where this feeds next.** Phase 4 ("evaluate") is a decision point, not just a rating — accept,
treat, analyse further, or reconsider the activity is a choice someone has to make and own. When that
choice needs to be put to a decision-maker rather than settled by the assessor alone, write it up
with `decision-memo`, using this assessment's register as the evidence base rather than
re-summarising it from memory.

## Choosing techniques

Do not default to a brainstorm and a matrix. Choose from the 31 techniques on the evidence available and the question being answered, and say why you chose them. `references/technique-selection.md` has the applicability matrix (which technique serves which phase), the attributes table (complexity, uncertainty, resources, quantitative output), and selection heuristics. Read it whenever you are picking, and again when the user asks "which method should we use".

Then read the technique detail from whichever file covers your choices:

- `references/techniques-identification.md` — B.1–B.12: brainstorming, structured/semi-structured interviews, Delphi, check-lists, preliminary hazard analysis, HAZOP, HACCP, environmental & toxicity assessment, SWIFT, scenario analysis, business impact analysis, root cause analysis.
- `references/techniques-analysis.md` — B.13–B.26: FMEA/FMECA, fault tree, event tree, cause-consequence, cause-and-effect (Ishikawa), LOPA, decision tree, human reliability assessment, bow tie, reliability-centred maintenance, sneak analysis, Markov, Monte Carlo, Bayesian statistics and Bayes nets.
- `references/techniques-evaluation.md` — B.27–B.31 and evaluation criteria: FN curves, risk indices, consequence/probability matrix, cost-benefit analysis, multi-criteria decision analysis, plus ALARP and how to set tolerance thresholds.

Two or three complementary techniques usually beat one. A common, well-matched pairing: a structured identification technique (SWIFT, HAZOP, checklist) → a causal or functional technique (FMEA, bow tie, fault tree) → an evaluation technique (matrix, cost-benefit, MCDA). But justify the combination against the problem, not against this example.

## Non-negotiables

These are where assessments actually fail. Hold the line on all six.

**Context and criteria before ratings.** You cannot rate a consequence as "major" without a definition of major. Establish the consequence categories, the scales, and the tolerance thresholds first, and show them in the output. If the user has not supplied them, either ask (up to three targeted questions, no more) or propose an explicit, clearly labelled default set and invite correction — never rate silently against criteria you invented and did not show.

**Controls before likelihood.** The level of risk depends on whether the existing controls actually work. For each risk, name the controls in place, judge their effectiveness, and say whether that judgement rests on evidence or assumption. An assessment that skips this systematically understates risk, because it credits controls that exist on paper only. Distinguish inherent risk (no controls) from residual risk (controls working as described) and be explicit about which you are reporting — reporting both is best.

**Precision must not exceed the data.** Three ways to estimate likelihood: relevant historical data, predictive modelling (fault tree, event tree, simulation), and structured expert judgement. Say which you used per risk. Where the basis is judgement, do not dress the number up — "3 on a 1–5 scale, expert judgement, low confidence" is honest; "12.4% annual probability" from the same basis is not. Even fully quantified levels of risk are estimates; say so.

**Don't screen out frequent small losses.** Preliminary screening is legitimate and useful, but a low-consequence, high-frequency risk can carry a larger cumulative effect than the rare catastrophe that dominates attention. Check for cumulative effects before setting anything aside, and record what you screened out and why.

**Surface the uncertainty.** State what you don't know: missing data, contested assumptions, model limitations, ranges that swamp the point estimate. Where the ranking depends on an assumption that could reasonably be otherwise, run a quick sensitivity check and say which risks change position. An assessment that admits its weak points is more useful than one that hides them.

**Risk statements must be causal.** "Data loss" is a label, not a risk. Write each risk as **source or cause → event → consequence on a stated objective**, e.g. "Single unreplicated database host (cause) fails during peak load (event), making the service unavailable for 4–12 hours and breaching the 99.5% availability commitment (consequence on objective)." Vague statements produce vague treatments.

## Output

The deliverable format is decided per request, not by default. Infer it from what the user asked for; if it is genuinely ambiguous and the assessment is substantial, ask once.

- **In-conversation** for rapid screening, a handful of risks, exploratory discussion, or "what are the risks of X" asked in passing.
- **`.md` file** for a full written assessment where the user wants something to keep or edit.
- **`.xlsx` register** when the artefact is the register itself — a living, sortable, filterable list to be maintained. Read the `xlsx` skill first.
- **`.docx` report** when it is a formal deliverable for a client, committee, board, or regulator. Read the `docx` skill first.
- **Both** when the request implies a formal report backed by a maintainable register.

`references/deliverables.md` has the risk register column schema, the report structure, and the default rating scales. Read it before producing any register or report.

Whatever the format, the assessment always contains: the context and criteria used, the techniques chosen and why, the risk register, the evaluation against criteria, the treatment plan with owners, the monitoring arrangements, and a stated list of assumptions and limitations.

## Working with what the user gives you

**They supply an existing register.** Do not rewrite it wholesale. Audit it against the six phases and report what is missing — usually context and criteria, control effectiveness, causal risk statements, and monitoring. Then upgrade it, preserving their IDs and wording where sound.

**They supply thin information.** Say what you are assuming and mark those risks as assumption-based. A useful assessment built on stated assumptions beats an interrogation. Ask at most three questions, and only where the answer would genuinely change the analysis.

**They ask about one specific risk.** Skip the register. Run the relevant phases on that risk — causes, controls, consequences, likelihood, evaluation, treatment — and keep the discipline of the non-negotiables.

**They name a technique.** Use it, and read its reference section rather than working from memory. If it is a poor fit for their question, use it anyway and note what it will and will not tell them, plus what would complement it.

## A note on limits

This skill produces structured risk assessment, not certification, regulatory sign-off, or professional engineering, medical, legal, or financial advice. Where an assessment touches life safety, regulated activity, or a domain with mandatory prescribed methodologies, say so and point to the need for a qualified practitioner and the applicable sector standard. That caveat belongs once, at the end, stated plainly — not repeated through the document.
