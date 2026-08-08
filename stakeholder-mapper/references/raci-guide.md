# RACI guide

Detail on the matrix SKILL.md recommends building for Deep mode, once the power/interest map is in
place.

## The four roles

- **Responsible** — does the work. Can be more than one person for a given activity.
- **Accountable** — owns the outcome and answers for it. Exactly one per activity or deliverable —
  this is the rule SKILL.md already flags as the most commonly broken.
- **Consulted** — provides input before the decision or the work is finalised, two-way communication.
- **Informed** — told after the fact, one-way communication, no input expected.

## Building it from the stakeholder map

The power/interest quadrants translate roughly, but not automatically, onto RACI roles:

- **Manage closely (high power, high interest)** → usually Accountable or Consulted, depending on
  whether they own the outcome or just need input.
- **Keep satisfied (high power, low interest)** → usually Informed, sometimes Consulted on the
  specific pieces that touch their concern — rarely Accountable, since low interest suggests they
  don't want the day-to-day ownership.
- **Keep informed (low power, high interest)** → Informed, sometimes Consulted if their domain
  knowledge is valuable even without formal authority.
- **Monitor (low power, low interest)** → Informed at most, often not on the matrix at all for minor
  activities.

Don't apply this mapping mechanically — a low-power, high-interest specialist can still be the right
Responsible for a technical piece of work even though their quadrant suggests limited engagement.

## Common failure patterns

**Too many Accountables.** Already flagged in SKILL.md as the single most common collapse. Symptom:
a decision stalls because two people each assumed the other would make the final call.

**Everyone Consulted, no one Responsible.** A matrix where every stakeholder is marked C on every
row produces consultation fatigue and no forward motion — reserve Consulted for the activities where
that person's input genuinely changes the outcome.

**Accountable and Responsible collapsed into the same overloaded person.** Technically fine in a
small team, but in a larger one it's often a sign that authority hasn't actually been delegated — the
same senior person is both doing the work and owning the outcome for everything, which doesn't scale
and creates a bottleneck.

**RACI built once, never checked against reality.** A matrix that was accurate at kickoff can become
wrong within weeks as roles shift. Tie its review to the same milestone cadence as the stakeholder
map itself.

## A minimal worked example

| Activity | Responsible | Accountable | Consulted | Informed |
|----------|-----------------|------------------|-----------|----------|
| Draft the technical design | Engineering lead | Engineering lead | Security team | Product manager |
| Approve the budget | Finance analyst | Finance director | Project sponsor | Engineering lead |
| Sign off on go-live | QA lead | Project sponsor | Engineering lead, Support lead | All stakeholders |
</content>
