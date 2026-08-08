# Designing the escalation path

For Deep mode: how an alert moves from detection to action across an organisation, not just how it's
qualified (covered in SKILL.md's core method).

## The three-tier pattern

**Tier 1 — the watch owner.** Receives the raw signal, runs the qualification fields (what changes,
who's affected, action required). Most alerts stop here: no action needed, or a minor action the
owner can assign directly.

**Tier 2 — the function affected.** For anything requiring action, the qualified alert goes to
whoever owns the affected process or activity — not back to whoever raised it originally. This is
where the domain judgement happens: the watch owner knows the regulatory text changed, the function
owner knows what it actually takes to comply.

**Tier 3 — leadership or governance.** Reserved for alerts with material compliance exposure,
significant cost, or cross-functional impact — not every alert needs to reach this tier, and routing
everything there defeats the purpose of having tiers at all. A useful test: would failing to act on
this alert plausibly produce a finding in an external audit or a genuine legal exposure? If yes, it
belongs at tier 3.

## Setting the threshold for tier 3

Define this once, with input from whoever would actually receive tier-3 escalations — not left to
each watch owner's individual judgement call in the moment, which produces inconsistent escalation
over time. Typical criteria: a deadline within a fixed number of weeks, an estimated cost above a
threshold, or explicit mention of enforcement risk in the source text.

## Avoiding escalation fatigue at each tier

The same alert-fatigue risk named in SKILL.md's opening principle applies within the escalation
chain, not just at initial detection — a tier-3 recipient who receives frequent low-material alerts
will start deprioritising all of them, including the one that matters. Audit the actual tier-3 volume
periodically; if it's running high, the threshold in the previous section needs tightening, not the
recipient's attention.

## Linking to `smq-analysis` for audit readiness

Where the watch process itself needs to demonstrate operation to a certification auditor (per the
"internal audit" pointer in SKILL.md), the escalation design is part of what's being demonstrated —
an auditor checking regulatory-watch effectiveness will look for evidence that alerts requiring
action actually reached someone with authority to act, not just that they were logged. Keep the
escalation record (who received what, when) as part of the watch log, not as a separate, harder-to-
produce trail.

## When the escalation path itself needs an owner

The scope review mentioned in SKILL.md's Deep-mode row (frameworks change; the list of what's watched
needs its own periodic check) applies equally to the escalation design — a tier-3 recipient who's
left the organisation, or a threshold that hasn't been revisited in years, silently breaks the whole
chain without anyone noticing until an alert that should have escalated didn't.
</content>
