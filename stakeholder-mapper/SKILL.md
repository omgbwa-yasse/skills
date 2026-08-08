---
name: stakeholder-mapper
description: >
  Maps the stakeholders of a project, a decision, or an organisational change by power and
  interest, and derives a differentiated engagement strategy from it. Trigger for "map the
  stakeholders for...", "who do I need to convince for this project", "prepare my engagement
  strategy for...", "who has power over this decision". Often a preparatory step for
  presentation-writer (advocacy, funding dossier) or negotiation-prep. Writes in the language the
  user is writing in.
---

# Stakeholder mapping

Map the way a practitioner who knows that real power does not always follow the org chart: a budget
controller with no leadership title can block a project a director supports. The failure to avoid:
ranking stakeholders by title rather than by actual influence on the decision.

## Before anything else: pick the depth

Match effort to the scale of what's being mapped. Three modes:

| Mode | When | What it looks like |
|---|---|---|
| **Rapid** | "Who do I need to convince for X" with a handful of obvious people involved | A short list with power/interest called out in one line each. In the conversation. |
| **Standard** | A project or change with a real stakeholder set to manage | Full grid across the four quadrants, with an engagement plan per high-power stakeholder. |
| **Deep** | A contested decision, a reorganisation, or a project with stakeholders across multiple organisations | Standard plus a RACI matrix, explicit anticipation of opposition from the high-power/low-interest quadrant, and a milestone-based review schedule for the map itself. |

## Identifying stakeholders

List anyone or any group who **affects** the project (can help or block it) or who **is affected**
by it (bears its consequences), even without a direct reporting line — suppliers, end users, support
functions, staff representatives depending on context.

## Assessing power and interest

For each stakeholder, two independent axes:

- **Power (real influence on the decision)** — budgets they control, approvals they can grant or
  withhold, informal leadership, ability to block even without formal authority. Assess actual
  influence, not just title.
- **Interest (how much the project changes their work or goals)** — high if the project directly
  transforms their day-to-day or their priorities, low if it only touches them at the margin.

Ground the assessment in observable facts (past decisions, budgets held, support secured), not
impression — the same discipline an SBI feedback rests on concrete situations.

`references/assessment-method.md` has the evidence sources for each axis in detail, a structured
scoring pass for Standard/Deep mode, and how to handle a stakeholder you can't directly assess.

## The four quadrants and their strategy

| | Low interest | High interest |
|---|---|---|
| **High power** | **Keep satisfied** — stay informed, avoid leaving them out of the loop | **Manage closely** — regular engagement, involve them in decisions, priority communication |
| **Low power** | **Monitor** — minimal effort, check periodically that nothing has changed | **Keep informed** — keep them updated, listen, but don't over-invest steering time |

**Do not freeze the map.** Reposition stakeholders at key milestones — power and interest shift as
the project progresses (an initial high-power sponsor can lose availability; a low-interest user
group can grow concerned as rollout approaches).

## Turning it into an action plan

1. **Match channel and frequency to each quadrant.** Regular one-on-one contact for "manage
   closely," a periodic summary note for "keep informed," an occasional check-in for "monitor."
2. **Anticipate opposition from the "high power / low interest" quadrant.** A stakeholder unconcerned
   today but able to block can activate if the project touches something they were unaware of —
   check this risk explicitly rather than dismissing them because they look indifferent.
3. **Turn the map into a communication plan and, where relevant, a RACI matrix** — who decides, who
   is consulted, who is informed, at each project milestone. If a RACI is built, hold one rule
   strictly: exactly one Accountable per activity or deliverable. Several people simultaneously
   marked Accountable is the single most common way a RACI collapses — a decision that turns out to
   belong to no one in particular.

`references/raci-guide.md` covers how quadrants map (imperfectly) onto RACI roles, the common
collapse patterns beyond the single-Accountable rule, and a worked example.

## The non-negotiables

**Power is assessed on real influence, never on title alone.** The most common error of a rushed
mapping is overlaying the quadrant onto the org chart.

**Every high-power stakeholder has a named engagement plan**, not just a box on the grid — the grid
alone changes nothing if it does not lead to a differentiated action.

**The map is revisited at milestones**, not fixed once at kickoff — treating it as frozen is the most
common cause of losing support along the way without anyone seeing it coming.

## Where this feeds next

The map itself does not decide anything — it tells you who to involve in a decision, not what to
decide. When the mapping surfaces a real choice to make (which stakeholders to prioritise, how to
respond to an opposed high-power actor), take it to `decision-memo`. When a specific high-power
stakeholder needs to be brought to agreement rather than simply informed, that is a negotiation — use
`negotiation-prep`.

## Output

- **In the conversation** — a quick mapping, advice on a specific stakeholder.
- **`.md`** — the full grid with an engagement plan, to evolve at the project's milestones.

`assets/table-templates.md` has ready-to-copy tables for the power/interest grid and, for Deep mode,
a RACI matrix.

Whatever the format, a Standard or Deep map always contains: power and interest assessed on stated
evidence rather than title, and a named engagement plan for every high-power stakeholder.

## Working with what the user gives you

**They give you an org chart and ask for the map.** Don't just transpose titles into power scores —
ask (or flag as an assumption) who actually controls budget, approvals, or informal influence, since
that is frequently not the same list as the org chart's senior names.

**They only want to know about one specific person.** Skip the full grid — place that one stakeholder
on the two axes with the evidence behind each rating, and give the matching engagement strategy
directly.

**They come back after a milestone to update an existing map.** Don't rebuild it from scratch — ask
what's changed for the stakeholders already on it, and check specifically whether anyone in the
high-power/low-interest quadrant has moved, since that's the quadrant most likely to shift
unnoticed.

## A note on limits

This skill produces a mapping and an engagement strategy; it does not itself resolve the conflicts a
mapping surfaces. Where a high-power stakeholder's opposition reflects a substantive disagreement
rather than a communication gap, say so and point to `negotiation-prep` or `decision-memo` rather than
treating more frequent updates as the fix.
</content>
