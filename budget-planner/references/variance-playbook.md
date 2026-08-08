# Variance playbook

What to do once a variance is identified, organised by cause — the diagnosis SKILL.md asks for,
worked through to a specific action.

## Timing variance (favourable or unfavourable)

**Signature:** spend is ahead of or behind the pro-rata line, but the activity itself is on schedule
— an annual contract paid upfront, a seasonal spend concentrated in one quarter, a hire that started
a month later than planned.

**Action:** confirm the timing explanation against the actual schedule (don't just accept "it's
timing" as an answer — check it). If confirmed, no corrective action needed; note it so the next
period's reviewer doesn't re-flag the same, already-explained pattern.

## One-off variance

**Signature:** an isolated overrun or underrun on a single line, tied to a specific, non-recurring
event (an unplanned repair, a one-time legal cost, a grant that came in early).

**Action:** reallocate within the existing budget if the total is unaffected, or flag for approval
if it pushes the total over. Does not require a full reforecast — a reforecast is for structural
drift, not a single identifiable event.

## Structural drift

**Signature:** the same line overruns (or underruns) two periods running, with no one-off
explanation — the initial estimate itself was wrong.

**Action:** this is what triggers the reforecast in SKILL.md. Don't patch it a third time with
another reallocation; rebuild the projection from the actual observed rate and bring the three
required elements (new total, explanation, options) to whoever owns the budget.

## Volume-driven variance

**Signature:** a line tracks a business driver (transactions, headcount, units shipped) that itself
moved — the budget assumption on the driver was right or wrong, not the spending discipline.

**Action:** don't treat this as a spending problem to fix — check whether the per-unit rate is still
in line with plan even though the total isn't. If the per-unit rate holds, the variance is really a
forecasting-input problem (the volume assumption), and the fix is updating that assumption, not
tightening spending controls that were never the issue.

## Scope creep disguised as variance

**Signature:** the line overruns because the underlying activity grew (more features, more sites,
more scope) without a formal budget revision — common on project budgets tracked by `project-tracker`.

**Action:** don't reforecast silently to match the new scope — that erases the record that scope
changed. Name the scope change explicitly, and treat the budget revision as a decision (candidate
for `decision-memo` if it needs sign-off) rather than an automatic adjustment.

## Escalation thresholds (define once, apply consistently)

A variance below a small threshold (e.g. under 5% and under a fixed absolute amount) can usually be
noted and monitored without action. Above it, name a cause using this playbook before deciding
anything. Set the actual thresholds with the budget owner — they depend on the organisation's size
and risk tolerance — but write them down once so they don't shift silently report to report.
</content>
