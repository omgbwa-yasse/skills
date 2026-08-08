---
name: presentation-writer
description: >
  Structures and writes the content of oral presentations and visual dossiers: a report-back deck, a
  funding or advocacy dossier for a donor, a project pitch, a presentation to a leadership committee
  or a client. Trigger for "prepare a presentation for...", "make me a pitch for this project", "I
  need to present this to leadership", "turn this dossier into slides", "prepare the deck for the
  donor". Complements tor-writer: a TDR or project dossier produced by tor-writer is often the raw
  material for the oral presentation that must convince an audience to approve or fund it — this
  skill takes that last step. Produces a slide-by-slide content outline in Markdown; conversion to
  .pptx on request. Writes in the language the user is writing in.
---

# Presentation and advocacy

A presentation is not a shortened document: it is a different object, built to be heard once, in a
fixed amount of time, by an audience who does or does not decide to act. The most frequent failure
is the document-as-presentation — a TDR or a report sliced into pieces and pasted onto slides,
unreadable out loud and redundant with the source document the audience has (or hasn't) read.

**Link with `tor-writer`.** When a TDR, a project dossier, or a scoping note already exists, use it
as raw material — do not re-analyse the substance. Extract the essentials: tor-writer's coherence
matrix (problem → objective → activities → results) directly gives the throughline for a report-back
or advocacy presentation.

## Identifying what's being asked for

| Type | Goal | Typical length | Number of slides |
|---|---|---|---|
| **Project pitch** | Convince in minimal time | 3-5 min | 5-8 |
| **Funding dossier / advocacy** | Secure a commitment (budget, agreement, funding) | 10-20 min | 12-20 |
| **Report-back / progress report** | Inform and be accountable | 15-30 min | 10-15 |
| **Leadership committee presentation** | Get a decision made | 5-15 min + questions | 6-10 |
| **Training / workshop** | Transfer a skill | Variable | Variable, outside this skill's detailed scope |

Ask for the available time and the audience if they aren't given — these are the two parameters that
determine everything else, and guessing them wrong is costly (a 20-slide presentation for 5 available
minutes will never be shown in full).

## Before structuring

1. **The audience and its decision-making power.** What can it do after the presentation: approve a
   budget, validate a direction, simply take note? The conclusion must target exactly that power.
2. **What the audience already knows.** Don't re-explain context to a committee that knows it by
   heart; don't assume it's known to a donor discovering the topic.
3. **The single message that must remain if everything else is forgotten.** A presentation without
   this central message becomes an unranked list of slides.

## The non-negotiables

**One idea per slide.** A title that states that idea as a sentence ("Processing time doubled in a
year," not "Delays"), and content that demonstrates it — not both at once.

**The spoken word carries the explanation, the slide carries the proof.** A dense slide read aloud
loses the audience: they read faster than anyone talks. The slide shows the figure, the diagram, the
comparison; the speaker explains the link.

**Narrative structure before slides.** Build the sequence of messages first (see
`references/narrative-structures.md`), then populate it with content. Going straight to slides
without a structure produces a stack, not an argument.

**The ask is explicit and placed where the audience expects it.** A funding dossier that never
clearly states the amount requested and what it produces does not get a decision. Place it early
(funding dossier, advocacy) or at the end (report-back) depending on the type — see
`references/narrative-structures.md`.

**Anticipate objections rather than absorb them.** For a leadership committee or a donor, prepare 2-3
expected questions and their answers as reserve slides (appendix), not in the main body — this keeps
the main thread clean without leaving the speaker exposed if a question comes up.

**Figures are sourced and consistent with the source document.** If the content comes from a TDR or a
report produced by `tor-writer` or `risk-analysis`, never invent a different figure for the
presentation — reuse it exactly, or explicitly flag the discrepancy and why.

## Narrative structures

`references/narrative-structures.md` gives the slide-by-slide outline for each of the five types in
the table above: which sections, in what order, where to place the ask, how to open and close. Choose
the right structure before writing the content — do not improvise the order.

## Visual content

`references/visual-content.md` covers the choice between text, table, chart, and diagram for each
type of message (comparison, evolution, breakdown, process, structure), slide-density rules, and the
pointer to the `dataviz` skill as soon as a data chart is needed — read `dataviz` before designing a
chart, do not improvise colours or shape.

## Output

Decided case by case, never by default.

- **In the conversation** — a Markdown content outline, slide by slide (title, key message, content,
  speaker note), for a short pitch or a quick review.
- **`.md`** — a full outline the user wants to rework or have reviewed.
- **`.pptx`** — a presentation ready to project. Read the `pptx` skill first if available; otherwise
  produce the detailed Markdown outline and flag that final formatting remains to be done in the
  user's presentation tool.

Always deliver content slide by slide, with, for each one, the key message in one sentence and a note
on what the speaker says — not just the on-screen text.
</content>
