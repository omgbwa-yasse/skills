---
name: regulatory-watch
description: >
  Structures a recurring regulatory or standards watch process: monitoring scope, review cadence by
  source type, an actionable alert format, a watch log. Trigger for "set up our regulatory watch
  on...", "how do we track changes to standard X", "structure our monitoring process", "which
  sources should we watch for...". Provides the methodological framework and templates; it does not
  itself monitor sources continuously — the tracked scope must be checked at each use. Links with
  smq-analysis and risk-analysis, which cite the relevant frameworks. Writes in the language the
  user is writing in.
---

# Regulatory and standards watch

Structure a watch process the way a practitioner who knows that unfiltered monitoring produces alert
fatigue: a team flooded with notifications eventually ignores all of them, which defeats the purpose
of the whole setup. Guiding principle: watching detects, qualified analysis interprets — two
distinct steps, never merged.

**Limit of this skill.** This skill structures the process and produces the watch deliverables
(scope, alert sheets, log); it does not monitor sources in real time. If the user wants continuous
automated monitoring, point them to a page-tracking tool or a dedicated regulatory feed, and use
this skill to frame what needs to be configured in it.

## Before anything else: pick the depth

Match effort to what's being set up. Three modes:

| Mode | When | What it looks like |
|---|---|---|
| **Rapid** | Qualifying one alert someone already spotted | The five-field alert sheet below, in the conversation. |
| **Standard** | Setting up watch for one organisation on a defined set of frameworks | Full scope definition, source list with owners, calibrated cadence per source, a watch log. |
| **Deep** | Multiple frameworks across a regulated multi-site organisation, or watch that must itself withstand certification audit | Standard plus explicit escalation paths per framework, cross-references to where each framework is cited in `smq-analysis` or `risk-analysis`, and a defined review cycle for the scope itself (frameworks change; the list of what's watched needs its own periodic check). |

## Defining the scope

1. **List the applicable frameworks** — standards (ISO 9001, sector-specific), legal texts,
   sector regulations, contractual requirements from clients or principals. Draw on `smq-analysis`
   and `risk-analysis` if a framework is already cited there for the organisation being tracked.
2. **Identify sources per framework** — standards bodies, official gazettes, trade associations,
   regulators. At least one source per framework, with its URL and its usual publication frequency.
3. **Name an owner per scope** — who receives and qualifies alerts for that framework; without a
   named owner, alerts pile up unprocessed.

`references/source-types.md` has where to actually look for sources, by framework category
(standards, legislation, sector regulation, contracts, internal policy) — read it when scoping is
more than a one-line list of already-known sources.

## Calibrating the review cadence

Do not apply the same frequency to everything — calibrate it to the nature of the change being
tracked:

| Nature of the change | Cadence |
|---|---|
| Text already in force, compliance action under way | Near-real-time monitoring (alert on publication) |
| Text still a proposal, in consultation or legislative debate | Weekly or bi-weekly review |
| A standard's revision cycle (ISO and equivalents) | Quarterly review |

A watch process that applies real-time urgency to everything produces the alert fatigue that makes
the whole setup ineffective; reserve urgency for the changes that genuinely warrant it.

## Qualifying a detected alert

Every change spotted produces a short sheet, never a raw forward of the source text:

| Field | Content |
|---|---|
| Framework and text concerned | Precise reference, publication or deadline date |
| What changes | One or two factual sentences |
| Who is affected in the organisation | Department, process, activity concerned |
| Action required | None, to monitor, to bring into compliance — with a deadline if applicable |
| Action owner | A named function |

Automated change detection is reliable and cheap; interpreting what the change actually means and
what it requires remains a qualified judgement a tool cannot make alone. This sheet is where that
judgement is made and recorded.

## Watch log

A chronological register of every qualified alert, consultable and traceable over time — useful for
internal audit (`smq-analysis`) to demonstrate that the regulatory watch required by the relevant
clause is actually operating, not just declared.

`references/escalation-design.md` covers the three-tier escalation pattern for Deep mode — how an
alert moves from the watch owner to the affected function to leadership, and how to set the
threshold for each tier without either bottlenecking on leadership or triggering escalation fatigue.

## The non-negotiables

**No alert forwarded without being qualified.** Passing on a raw text without stating what changes
and who is affected simply shifts the watch work onto the recipient instead of doing it.

**The review cadence is written down and justified per scope**, not left to informal judgement by
whoever is watching — otherwise the least-watched frameworks silently drift into neglect.

**Every required action has a deadline and a named owner**, on the same principle as a meeting
decision log — a qualified alert with no follow-up owner is only of documentary value.

## Output

- **In the conversation** — scoping the watch, help qualifying a one-off alert.
- **`.xlsx`** — the watch log and source register, living and meant to be kept up to date. Read the
  `xlsx` skill first.

`assets/table-templates.md` has ready-to-copy tables for the source register, cadence calibration,
alert sheet, and watch log.

Whatever the format, a Standard or Deep setup always contains: a named owner per scope, and a cadence
that's written down and justified rather than left to informal judgement.

## Working with what the user gives you

**They forward you a raw regulatory text and ask "does this affect us."** Don't just summarise the
text — run it through the qualification fields (what changes, who's affected, action required) before
answering, since an unqualified summary is exactly the raw-forward failure this skill exists to
prevent.

**They want to watch "everything relevant" with no defined scope.** Push back gently — ask what
frameworks actually apply to their organisation first (or draw on `smq-analysis`/`risk-analysis` if
already established there), since an unbounded scope is how alert fatigue starts.

**They already have a watch log but it's just a list of links.** Don't add to it as-is — retrofit the
qualification fields onto the existing entries first, or flag that the log as it stands can't
demonstrate an operating watch process to an auditor.

## A note on limits

This skill structures the watch process; it does not itself constitute legal or regulatory advice,
and the interpretation recorded in an alert sheet is not a substitute for qualified legal review where
the stakes warrant it. Say so once where a change carries real compliance exposure, rather than
letting the sheet's clean format imply a legal sign-off it did not receive.
</content>
