---
name: decision-memo
description: >
  Writes a decision or arbitration memo meant to get a superior, a committee, or the user's own
  future self to decide: options compared, criteria, a single recommendation, and a named owner.
  Trigger for "draft a memo to get X approved", "I need a decision on...", "write a decision memo",
  "compare these options for my leadership", "help me get X signed off". Distinct from mail-writer
  (routine correspondence) and risk-analysis (in-depth risk assessment): this skill produces the
  specific artefact that forces a decision between several options, in one to three pages. Writes
  in the language the user is writing in.
---

# Decision memo

Write a decision memo the way a practitioner writes it after watching decision-makers hand one back
unread, because it demanded a sorting job that should have been done before it reached them. The
failure this skill exists to prevent: the unranked menu of options that pushes the work of deciding
back onto the decision-maker — a decision memo that recommends nothing is not a decision memo, it is
a briefing pack.

## Before anything else: pick the depth

Match effort to the stakes. Three modes:

| Mode | When | What it looks like |
|---|---|---|
| **Rapid** | A routine call, low stakes, one obvious owner already leaning one way | Half a page: question, recommendation, one line of why, owner. In the conversation. |
| **Standard** | The usual case: a real choice between options, submitted upward for sign-off | Full structure below: 1-3 pages, options table, criteria, appendix if needed. |
| **Deep** | High stakes, multiple stakeholders with conflicting interests, board or committee audience, or reversible-vs-irreversible framing matters | Standard structure plus a named dissent/risk section, sourced figures from `risk-analysis`/`budget-planner` rather than estimates, and an explicit statement of what happens if the decision is deferred. |

State the mode in one line if it isn't Standard — a one-paragraph Rapid memo dressed up with a
six-section structure wastes the reader's time as much as a three-line memo for a board vote wastes
their trust.

## Before drafting

1. **The exact question to be decided.** A question, not a topic. "Should we migrate to vendor X by
   Q3" — not "vendor strategy."
2. **Who decides, and with what authority.** Approves, signs off on a budget, arbitrates between
   options already worked up, takes note. The memo addresses that specific authority.
3. **The options genuinely on the table**, including the option of changing nothing — often wrongly
   omitted even though it is the decision-maker's implicit point of comparison.

If the comparison needs input this skill does not itself produce, get it from the specialised skill
first rather than approximating it: `risk-analysis` for the likelihood and impact behind each option,
`budget-planner` for what each option costs, `stakeholder-mapper` for who needs to be consulted or
will resist, `negotiation-prep` for a decision that hinges on what a counterpart will accept.

## Structure

One to three pages, never more without that signalling a framing problem rather than a genuine need
for detail:

1. **The question and the context** — 3-4 lines. Enough for a reader who has forgotten the file to
   understand the stakes. The opening line carries the weight: a reader who is content-driven and
   time-pressed decides in the first few seconds whether the memo is worth their attention — it must
   establish why this matters to them specifically, not just what the topic is.
2. **Recommendation, first.** A decision-maker who reads only the first sentence should have the
   essential: which option, why, in one line. Never make the recommendation wait until the end — this
   is not a mystery novel.
3. **Options compared**, in a compact table: cost, benefit, main risks, status (recommended /
   discarded and why). Options must be MECE — mutually exclusive and collectively exhaustive —
   otherwise the decision-maker will object to a missing option rather than choosing among those
   presented.
4. **Evaluation criteria** — the basis on which options were compared (cost, timeline, risk,
   strategic fit). Naming them explicitly keeps the recommendation from looking arbitrary.
5. **What the decision commits to** — a single owner for implementation (never a committee or a
   department), the first concrete deadline, what happens if the decision is not made in time.
6. **Appendix, if needed** — calculation detail, options discarded earlier, sources. Never in the
   main body.

`references/worked-examples.md` has an annotated example for each mode. `references/common-failure-patterns.md` covers the failures beyond the non-negotiables below — read it when a memo has bounced back before or when reviewing someone else's draft.

## The non-negotiables

**One recommendation, not a menu.** Presenting several options is necessary to show the comparison
work was done; failing to choose among them pushes that work back to the decision-maker — exactly
what the memo exists to prevent.

**A named owner, never a collective.** "The team will implement" commits no one. Name a specific
function, with a date.

**Figures and risks cited, not reinvented.** If a costing already exists (`budget-planner`) or a risk
assessment (`risk-analysis`), reuse it verbatim rather than re-synthesising from memory — a gap
between the memo and the source document destroys the credibility of the whole thing.

**Refuse false neutrality.** A memo that presents five options with equal weight, with no clear
recommendation, has not done the job expected of it — even when the question is politically
sensitive. Recommending is an argument for transparency, not for convenience: state why, factually.

**Refusal is a legitimate option.** If the best recommendation is to do nothing or not decide yet
(waiting on missing information), say so explicitly rather than forcing a premature decision to fill
the format.

## Output

- **In the conversation** — the full memo, most of the time: this is a short format.
- **`.md`** — if the user wants to rework it or have it reviewed before circulation.
- **`.docx`** — if it must be signed, filed, or formally submitted to a committee. Read the `docx`
  skill first, then `assets/docx-style-guide.md`.

`assets/table-templates.md` has ready-to-copy tables for the options comparison, criteria, and
commitment block.

Whatever the format, the memo always contains: the question, the recommendation stated up front, the
options compared against named criteria, and a single named owner with a deadline.

## Working with what the user gives you

**They supply analysis but no recommendation** (a risk register, a costing, a stakeholder map).
Don't just format it into a table — commit to the recommendation the analysis actually supports. That
synthesis is the point of this skill; handing back the same data with headings added is not a memo.

**They already know the answer and want the memo to justify it.** Write the honest version: if the
evidence supports their preferred option, say so plainly; if it doesn't, say that too, plainly, rather
than building a one-sided case. A memo that launders a foregone conclusion is worse than no memo,
because it borrows the format's credibility for a decision that wasn't actually examined.

**They give you only the topic, no options worked out.** Propose a MECE set yourself, including the
status-quo option, and flag which parts of the comparison rest on your own estimate rather than
supplied data.

**It's genuinely a close call.** Say so. Give the recommendation anyway — a memo still needs to name
one option — but state explicitly what would change the answer, so the decision-maker knows what to
watch for after committing.

## A note on limits

This skill produces the artefact that structures a decision; it does not have the authority to make
one. Where the decision carries legal, financial, or safety exposure beyond the memo's own analysis,
say so once and point to the need for the relevant specialist sign-off — legal review, a formal risk
assessment, board approval — rather than letting the memo's clean format imply a review it did not
receive.
</content>
