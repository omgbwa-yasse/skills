---
name: project-tracker
description: >
  Tracks the operational progress of a project already underway: progress dashboard, detailed
  schedule, calendar updates, periodic status report, managing gaps between planned and actual,
  decision and blocker log. Trigger for "where does the project stand", "update the schedule",
  "prepare the progress update", "track this project", "we've fallen behind on...", "list the
  blockers". Distinct from tor-writer, which scopes and plans a project before it launches (TDR,
  initial work plan): this skill takes over once the project is under way, based on the initial plan
  produced by tor-writer if available. Writes in the language the user is writing in.
---

# Operational project tracking

Track a project the way a competent project manager does: systematically compare planned to actual,
name variances without softening them, and turn every delay or blocker into a decision rather than a
mere observation. The failure this skill exists to prevent is the dashboard that lists activities as
"in progress" indefinitely, never saying what's blocking them or who needs to decide.

**Link with `tor-writer`.** When an initial work plan, schedule, or logframe exists (produced by
`tor-writer` or supplied by the user), use it as the tracking baseline — never recreate a schedule
from scratch if an original exists. If no initial plan exists, say so: tracking a project with no
starting reference measures nothing, it only describes a state.

## Identifying the request

| Request | Expected output |
|---|---|
| **One-off progress update** | A synthetic status: done / in progress / upcoming / blocked, in one page |
| **Schedule update** | A revised calendar, with variances flagged against the previous version |
| **Periodic status report** | A structured document: progress, budget spent, risks, decisions needed |
| **Handling a delay or blocker** | Diagnosis of the cause, catch-up options, downstream impact |
| **Project log** | A chronological register of decisions, milestones reached, blockers resolved |

Do not produce a full report when only a one-off status is requested — state in one line which kind
of output is being produced.

## Before taking stock

1. **The baseline.** What is being compared against: the initial schedule, the last update,
   commitments made to a third party (client, donor)? Without a dated baseline, "behind schedule"
   means nothing.
2. **The useful granularity.** Track at activity level for a team check-in, at milestone level for a
   steering committee — don't push operational detail up to an audience that doesn't need it, and
   don't drown a team that does need it in a summary.
3. **What is blocked and awaiting a decision**, as distinct from what is simply progressing more
   slowly than planned. The two call for different handling.

## The non-negotiables

**Planned and actual, always side by side.** No status line means anything in isolation. "Task in
progress" says nothing without the planned end date next to it.

**Name the variance, don't dress it up.** A milestone missed by two weeks is a milestone missed by
two weeks — not "slightly shifted." Downplaying a delay delays the catch-up decision and worsens the
final gap.

**Every blocker has an owner and a decision deadline**, never just a description. "Blocked on legal
sign-off" with no statement of who decides and by when is not an actionable tracking item, it's a
complaint.

**Distinguish execution delay from scope creep.** A project running late because the work takes
longer than planned does not call for the same treatment as a project that has grown along the way
(activities added with no revision to schedule or budget). Name which of the two situations is at
play before proposing a catch-up plan.

**Downstream impact before the fix.** Before proposing how to catch up on a delay, state what it
pushes downstream: which later milestones are threatened, which external commitment (delivery,
contractual deadline) is affected. A catch-up fix with no impact assessment treats the symptom.

**Budget follows the same logic as the schedule.** Actual vs. planned at the same date, not actual
vs. total budget — a project that has spent 40% of the budget at 30% of the way through the schedule
is not "on track" even though 40% is less than 100%.

## Method

`references/tracking-method.md` — how to build a dashboard (columns, meaningful vs. cosmetic colour
coding), how to handle a missed milestone (diagnose the cause before the catch-up plan), how to keep
a decision log that stays usable over time.

`references/status-report-structure.md` — the structure of the periodic status report, calibrated by
audience (team, steering committee, donor/client), with the RAG (Red / Amber / Green) framework and
its explicit switch-over criteria — not a colour code left to the subjective judgement of whoever
fills in the table.

## Output

Decided case by case, never by default.

- **In the conversation** — a one-off status, an answer to "where do we stand," a diagnosis of an
  isolated blocker.
- **`.md`** — a status report the user wants to keep or circulate in writing.
- **`.xlsx`** — a dashboard or living schedule, to be filtered and updated over time. Read the `xlsx`
  skill first.
- **`.docx`** — a formal status report for a steering committee, a donor, or a client. Read the
  `docx` skill first.

## Limits

This skill produces tracking and reporting; it does not replace a project-management tool (fine-
grained scheduling with dependencies, workload allocation) once a project is complex enough to need
one. Flag this if the volume of activities and dependencies exceeds what a table or a text-based
schedule can usefully represent.
</content>
