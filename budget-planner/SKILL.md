---
name: budget-planner
description: >
  Builds and tracks the budget of a department, a division, or a project: a justified line-by-line
  budget, execution tracking, variance analysis and reforecasting. Trigger for "prepare the budget
  for...", "help me justify this budget line", "we have a budget variance to explain", "reforecast
  the budget", "compare actual spend to budget". Links with project-tracker (schedule tracking) for
  the budget side of project follow-up, and with decision-memo when a budget arbitration needs to be
  decided. Writes in the language the user is writing in.
---

# Budget planning and tracking

Build a budget the way a practitioner who knows that automatically rolling over last year's budget
hides obsolete lines and locks in outdated priorities. The guiding principle, borrowed from
zero-based budgeting: every line justifies itself by the outcome it funds, not by the fact that it
already existed.

## Before anything else: pick the depth

Match effort to the size and stakes of the budget. Three modes:

| Mode | When | What it looks like |
|---|---|---|
| **Rapid** | Justifying one line, a quick variance question, a small team budget | A short answer or a handful of lines with outcomes stated. In the conversation. |
| **Standard** | A department or project budget for a planning cycle | Full line-by-line build with decision units, plus regular variance tracking. |
| **Deep** | A multi-team or multi-year budget, one under real scrutiny (board, funder), or a structural variance requiring reforecast | Standard plus explicit zero-basing rationale per decision unit, a reforecast with the three required elements, and figures sourced for a `decision-memo` if the arbitration exceeds the budget owner's authority. |

## Building a budget

1. **Start from zero, at least for discretionary lines.** Never roll over a line without asking what
   it actually funds and whether that remains a priority. Reserve strict zero-basing for
   discretionary spend, and do it periodically rather than on every line every year — applying it
   everywhere would create a disproportionate justification burden.
2. **Break the budget into decision units.** Group spending by team, programme, or initiative rather
   than by accounting category alone — this makes it possible to arbitrate on what each unit
   produces, not just on its amount.
3. **Every line states the outcome it funds**, not just the amount: "Sales training — 3 sessions, 15
   people, goal: cut new-hire ramp-up time by X months" — not "Training: €8,000."
4. **Fund the best returns first**, once decision units have been compared against each other — a
   budget that spreads evenly across lines with no arbitration has not done the prioritisation work.
5. **Standardise line granularity** so the budget stays legible and comparable year over year — avoid
   one line itemised to the euro next to a neighbouring line lumped into a single allowance.

`references/zbb-method.md` breaks the five steps above into the fuller REBUILD framework, with a
note on when the full version is overkill and a lighter two-step pass suffices.

## Tracking execution

**Compare actual to budget at the same date**, never actual to the full-year budget. A budget 40%
spent after 30% of the year has elapsed is off track, even though 40% is still below 100%.

**Name the variance — favourable or unfavourable — with its cause.** A favourable variance
(under-spend) is not automatically good news — it can signal an activity running late rather than a
genuine saving. Always check which of the two is actually happening before qualifying the variance.

**Distinguish a one-off variance from a structural drift.** An isolated overrun on one line is fixed
with a reallocation; an overrun that repeats month after month signals that the initial budget was
miscalibrated and calls for a reforecast rather than a line-by-line adjustment.

**Review variance on a regular cadence**, not only at period end. Lightweight governance — a monthly
variance review, a quarterly reforecast decision, a clear escalation path for significant variances
— is enough in most contexts and avoids discovering a drift too late.

`references/variance-playbook.md` works through five variance causes (timing, one-off, structural,
volume-driven, scope creep) to a specific action each — read it before deciding how to treat a
variance, not just whether it's favourable or unfavourable.

## Reforecasting

When a structural variance is identified: rebuild the projection to completion from the actual
spend rate, not from hoped-for catch-up. Present three things: the new projected total, what
explains it, and the options (reallocate, cut scope, request a supplement) — following the pattern
of a `decision-memo` if the arbitration exceeds the budget owner's level of authority.

## The non-negotiables

**No line without the outcome it funds.** An amount alone, with no precise purpose, cannot be
arbitrated or justified if questioned.

**Variance is always compared at the same date, never to the full-year total before year-end.** This
is the most frequent and most misleading error in budget tracking.

**A reforecast assumption rests on the actual observed rate**, not on a hoped-for target —
reforecasting on what is wished for rather than what is happening reproduces the same variance next
round.

## Output

- **In the conversation** — a one-off variance analysis, help justifying a line.
- **`.xlsx`** — the budget or tracking spreadsheet, living and meant to be updated over time. Read the
  `xlsx` skill first.
- **`.md`** or **`.docx`** — a reforecast memo or a formal budget dossier for approval. For `.docx`,
  read the `docx` skill first, then `assets/docx-style-guide.md`.

`assets/table-templates.md` has ready-to-copy tables for the budget build, variance tracking, and
reforecast summary.

Whatever the format, a Standard or Deep budget always contains: every line tied to a stated outcome,
and — once tracking starts — variance compared at the same date, never against the full-year total.

## Working with what the user gives you

**They give you last year's budget and ask to "update it."** Don't just adjust the numbers — ask what
each discretionary line still funds and whether it remains a priority; a budget update that skips
this reproduces exactly the automatic-rollover failure this skill exists to prevent.

**They report a variance without a cause.** Don't accept "we're under budget" or "we're over" as a
finished analysis — ask or infer whether it's a timing effect, a one-off, or a structural drift before
recommending any action, since the three call for different fixes.

**They only have a total, not a line-by-line build.** Work backward: ask what the total is meant to
cover and break it into decision units before treating any part of it as fixed — a lump sum with no
outcome attached can't be tracked or defended later.

## A note on limits

This skill produces budget planning and tracking; it is not accounting, tax, or financial-audit
advice, and its numbers are not a substitute for the organisation's official financial records. Where
a budget decision has accounting, tax, or statutory reporting implications beyond internal planning,
say so once and point to the need for finance or audit sign-off.
</content>
