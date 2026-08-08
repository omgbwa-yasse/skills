# Planning and costing

Used at Stage 4, Blocks E and G. MPR reminder: **duration and cost are outputs, never starting
assumptions.**

---

## PART 1 — SCHEDULE

### 1.1 Two ways to determine duration

| Method | Description | Recommendation |
|--------|-------------|----------------|
| **Top-down** | Fix a desired duration first, then build a method that fits inside it | ⚠️ Discouraged — real constraints eventually assert themselves |
| **Bottom-up (MPR)** | Leave duration blank, define methodology → resources → schedule, then derive duration from the chart | ✅ Apply by default |

If the user imposes a duration from the outset (donor constraint, statutory deadline), treat it as a
**constraint**, not as data: build the bottom-up schedule, then state the gap explicitly if there is
one, together with the adjustment options (reduce scope, add resources, parallelise).

### 1.2 Minimum schedule data

1. Sequence number
2. Programme, action, activity or task
3. Duration

Sequencing itself derives from the **start and end conditions** defined in the methodology. Those
conditions may not appear on the chart, but they govern the order.

**Rule**: interdependent activities that follow one another sit on the same timeline; independent
activities run in parallel.

### 1.3 Text template for a schedule

For a Markdown rendering, use a period × activity matrix:

| # | Activity | W1 | W2 | W3 | W4 | W5 | W6 | Owner |
|---|----------|----|----|----|----|----|----|-------|
| 01 | … | ██ | ██ | | | | | |
| 02 | … | | ██ | ██ | ██ | | | |

Match the time unit to the project: days, weeks, months, quarters.

### 1.4 PERT

Program Evaluation and Review Technique: a scheduling tool that organises tasks as a network. It
exposes the connections between tasks, execution times and interdependencies, and identifies the
critical path — the sequence where any delay pushes back the end of the project.

Prefer it when interdependencies are numerous and the central question is "what blocks what?".

### 1.5 Gantt chart

The most readable representation of progress: tasks listed in the left-hand column, time units along
the header row, each task shown as a horizontal bar whose position and length give start, duration
and end.

Prefer it for communicating to decision-makers and for tracking execution.

*Historical note, usable in training material*: the first chart of this kind was developed in the
1890s by the Polish engineer Karol Adamiecki; the version produced fifteen years later by the
American Henry Gantt is the one that prevailed under his name.

### 1.6 When project management software is in use

If the user works with MS Project, GanttProject or an equivalent, the schedule, resource description
and cost sections are generated automatically as the project data is entered. Say so: the skill then
produces the **structure and the input data**, not the chart.

---

## PART 2 — COSTING

### 2.1 Mandatory precondition

Before opening the budget table, reread the whole document from the context through to the resources.
Recommend that the user have this part reviewed by a more experienced third party: it is the section
where an error costs the most and is hardest to correct.

### 2.2 Resource categories

| Category | Content |
|----------|---------|
| Human resources | Experts, technicians, support staff, occasional providers |
| Material resources | Equipment, consumables, vehicles |
| Property resources | Premises, rooms, land, accommodation |
| Informational resources | Data, licences, documentation, subscriptions |
| Financial resources | Only where mobilised as a project asset: cash grants, working capital, financial exchanges |

### 2.3 Budget line structure

| Category | Ref. | Item and specifications | Billing unit | Unit price | Quantity | Total |
|----------|------|-------------------------|--------------|------------|----------|-------|

Common billing units: **person-day**, **person-month**, **unit**, **lump sum**, **day**,
**kilometre**, **page**, **session**.

The choice of unit is not neutral: a lump sum shifts the overrun risk to the provider, a day rate
leaves it with the commissioning party. Point this out when the amount is significant.

### 2.4 Totals to produce

1. Total excluding tax
2. Breakdown of applicable taxes
3. Total including tax
4. Currency, explicitly stated

Add where relevant: breakdown by funding source, by specific objective, or by budget year
(multi-year projects).

### 2.5 Integrity rules

- ❌ **Never invent a unit price.** Provide the complete structure and flag the unit price
  as to be completed. A plausible but false budget is more dangerous than an incomplete
  one, because it will be reused as is.
- ✅ Every resource in section 27 must appear in the budget, or carry an explicit note that it is
  supplied by the commissioning party.
- ✅ Every budget line must be traceable to an activity in the methodology. An orphan line is either
  padding or the sign of a forgotten activity.
- ✅ Handle contingencies explicitly: a dedicated line with a stated percentage, or an acknowledged
  statement that there is none.

### 2.6 Final budget coherence check

- [ ] The total is consistent with the duration derived from the schedule (no expert billed 60 days
      on a 30-day assignment)
- [ ] Human resource quantities match the levels of effort in section 25
- [ ] Travel costs match the locations in section 11
- [ ] Deliverable production costs (printing, reproduction, hosting) are included
- [ ] The total is consistent with the order of magnitude stated in the summary sheet
