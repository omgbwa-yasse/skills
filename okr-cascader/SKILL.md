---
name: okr-cascader
description: >
  Translates strategic objectives into measurable team-level OKRs (Objectives and Key Results), and
  checks their alignment without forcing a plain top-down copy. Trigger for "translate our strategic
  objectives for the team", "help me write our OKRs", "check the alignment of these team
  objectives", "our OKRs don't match the strategy". Extends tor-writer (which uses OKR occasionally
  at project scoping) to a recurring, quarterly use for team or leadership steering. Writes in the
  language the user is writing in.
---

# Translating objectives (OKR)

Translate objectives the way a practitioner who knows that strict cascading — reproducing the
level-above objective while shrinking it — reliably fails for teams whose work does not map
directly onto the metric one level up. A support or design team forced to copy a revenue objective
loses in clarity what it gains in apparent compliance. The principle that works better: **align, do
not cascade** — preserve the strategic intent by grounding it in each team's reality, not by copying
it mechanically.

## Before anything else: pick the depth

Match effort to the scope of the exercise. Three modes:

| Mode | When | What it looks like |
|---|---|---|
| **Rapid** | Phrasing one objective or one Key Result, or a quick sanity check on a single OKR | A one-line fix or check, in the conversation. |
| **Standard** | A team's quarterly OKR set, drafted from scratch or reviewed | Full objective + 2-4 key results per objective, checked against the three defects below. |
| **Deep** | Multiple teams' OKRs need cross-checking for alignment, or a cascade has visibly broken down organisation-wide | Standard for each team plus an explicit alignment map showing which team OKRs connect to which shared priorities, and where the connection is deliberately team-specific rather than forced. |

## Building an OKR

**Objective** — qualitative, inspiring, fits in one sentence. Answers "where do we want to go," not
"how much." Phrased broadly enough to leave room for the team translating it: an overly specific
strategic objective ("Enable advanced analytics in the product") forces teams that do not contribute
to it directly into an artificial justification — prefer a broader objective ("Become the reference
solution for reporting") that lets each team find its own contribution. Avoid verbs that describe a
steady state rather than a change — "maintain market position," "keep hiring," "continue doing X" —
they set no real endpoint; prefer a phrasing with a clear finish line.

**Key Results** — 2 to 4 per objective, quantified, verifiable without ambiguity of interpretation.
Measure an outcome, not an activity: "Cut average processing time from 5 to 3 days," not "Roll out a
new processing workflow" (that is an activity, not an outcome — it can be completed without moving
the metric at all).

`references/okr-examples.md` has contrasted weak/better pairs across sales, engineering, and support
functions, plus a full team's graded quarterly set.

**Limit the set and grade honestly.** 3 to 5 objectives per period, each with roughly 3 key results —
beyond that, teams over-extend and effort dilutes. Grade each key result on a 0–1.0 scale at period
end; a team that lands consistently at 1.0 was not ambitious enough, a team landing around 0.6–0.7
set a genuinely stretching target. Treat a low grade as information to refine the next cycle's OKRs,
not as a failure to penalise — punishing low grades quietly re-trains teams to sandbag their targets.

## Translating without cascading

1. **The level above provides context, not a copied objective.** Share the previous period's results
   and the chosen direction; let each team draft its own OKRs from that context rather than assigning
   it a shrunk version of the objective above.
2. **Align through discussion, not automatic hierarchy.** Once team OKRs are drafted, check together
   where they connect to shared priorities and clarify ambiguous areas — alignment is built, not
   mechanically derived from an org chart.
3. **Do not go beyond two levels.** Organisation → team is enough for most structures; going down to
   a third level (individual) dilutes clarity without a proportionate gain.
4. **A majority aligned, a minority team-specific.** A split where most team OKRs visibly connect to
   shared priorities, and the rest reflect team-specific needs, produces a more robust system than a
   100% cascade that stifles local initiative.

`references/alignment-method.md` walks through this five-step process in practice, with a worked
alignment map and a concrete test for whether a cascade has gone one level too far.

## Reviewing an existing set of OKRs

Three defects to check for, in this order:

1. **A Key Result that describes an activity, not an outcome.** Test: "if we do X but the measured
   outcome doesn't change, is the KR still met?" If yes, it is an activity disguised as an outcome.
2. **A team objective forced to resemble the level-above objective.** Signals a strict cascade that
   was poorly digested — check whether the objective genuinely reflects the team's work or was
   bolted on for form's sake.
3. **Too many OKRs for one period.** Beyond 3-4 objectives per team per quarter, prioritisation failed
   upstream — everything becomes a priority again, so nothing is.

## The non-negotiables

**Every Key Result must be measurable without ambiguity of interpretation** — a KR that needs a
subjective judgement call to say whether it was met is not a good KR.

**A strategic objective is never mechanically translated for a team whose link to it is indirect.**
If the connection looks forced, say so and propose a team objective that reflects its real
contribution, even if it reads as less directly tied to the top.

**Any mid-period change to a higher-level OKR is flagged explicitly** to the teams depending on it —
a silent upstream change makes all the downstream translation work moot without anyone knowing it.

## Output

- **In the conversation** — help phrasing an OKR, a quick review of an existing set.
- **`.md`** or **`.xlsx`** — the period's OKR grid, with the alignment thread to shared priorities, to
  keep and update quarterly.

`assets/table-templates.md` has ready-to-copy tables for the OKR grid, alignment map, and the
outcome-vs-activity test.

Whatever the format, a Standard or Deep set always contains: key results that pass the outcome-vs-
activity test, and a stated link (or deliberate non-link) to the priorities above.

## Working with what the user gives you

**They give you a list of activities and call them OKRs.** Don't just reformat them under
"Objectives" and "Key Results" headers — run the outcome-vs-activity test on each one first, and flag
which ones are actually a project plan wearing OKR labels.

**They want every team's OKRs to visibly roll up to the company objective.** Push back gently: that's
the strict-cascade failure mode this skill exists to prevent. Ask instead what direction and context
each team was given, and check alignment through discussion rather than forcing a textual match.

**They only have last quarter's grades, no new OKRs yet.** Use the grades as the input, not the
output — a team that graded consistently at 1.0 needs more ambitious objectives next cycle; one that
graded near 0 across the board needs the targets or the context questioned before repeating them.

## A note on limits

This skill produces objective-setting content; it does not resolve an underlying prioritisation or
resourcing conflict between teams. Where OKRs keep failing because two teams are structurally
competing for the same limited resource, say so once — that is a resourcing decision for
`decision-memo`, not something better OKR phrasing will fix.
</content>
