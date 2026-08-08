# OKR worked examples

Contrasted pairs across functions — the common mistake and its fix.

## Sales team

**Weak:** Objective: "Increase revenue." KR: "Close more deals."
Problem: the objective is a metric, not an aspiration ("where do we want to go") and the KR is an
activity ("close more deals" says nothing about how many, or what counts as done).

**Better:** Objective: "Become the team clients recommend without being asked." KRs: "Net Promoter
Score from 32 to 45," "Reduce average time-to-first-response from 48h to 12h," "Cut contract renewal
friction — renewal cycle from 6 weeks to 2."

Notice the objective no longer mentions revenue directly — it's a qualitative aspiration that
revenue growth is expected to follow from, which leaves room for the team to find the actual levers
rather than being handed a number to hit by any means.

## Engineering / platform team

**Weak:** Objective: "Support the company's growth objective." KR: "Ship the new API."
Problem: this is the strict-cascade failure — a platform team forced to phrase its objective as a
shrunk copy of a company-level growth objective it doesn't directly drive. The KR is an activity
(shipping is binary, says nothing about whether it worked).

**Better:** Objective: "Make the platform a non-issue for product teams building on it." KRs: "Cut
median API response time from 800ms to 200ms," "Reduce platform-caused incident count from 6/quarter
to 2," "Self-service onboarding for a new service — from 2 weeks of platform-team involvement to 2
days."

The connection to company growth is real (a faster, more reliable platform lets product teams ship
faster) but it's not forced into the objective's wording — it stays in the alignment map instead
(see `references/alignment-method.md`).

## Support / operations team (often the hardest to write well)

**Weak:** Objective: "Improve support quality." KR: "Answer tickets faster."
Problem: both lines are vague enough to mean almost anything, and "answer faster" could be gamed by
rushing responses at the cost of resolution quality.

**Better:** Objective: "Turn support into a reason customers stay, not a reason they leave." KRs:
"First-contact resolution rate from 61% to 75%," "CSAT on closed tickets from 4.1 to 4.5," "Cut
ticket reopen rate from 18% to under 10%."

Three KRs that can't all be gamed simultaneously by one distorting tactic (rushing tickets would hurt
resolution rate and CSAT even if it helped a raw speed metric) — a useful check when picking KRs.

## A full team's quarterly set

> **Objective 1: Make the platform a non-issue for product teams building on it.**
> - KR: median API response time 800ms → 200ms
> - KR: platform-caused incidents 6/quarter → 2
> - KR: self-service onboarding 2 weeks → 2 days
>
> **Objective 2: Reduce the operational cost of running our own infrastructure.**
> - KR: cloud spend per transaction down 20%
> - KR: on-call pages per week from 14 to under 5
>
> Grade at period end: 0.7, 0.5, 0.9, 0.4, 0.8 — average 0.66, in the target 0.6-0.7 zone.

Four objectives would already be at the upper edge of what's manageable; five or six per team per
quarter is the "too many" pattern SKILL.md's review checklist flags.
</content>
