---
name: procedure-writer
description: >
  Writes the documented information of a quality management system: documented procedures, quality
  manual, process sheets, work instructions, quality policy and objectives. Trigger for any request
  to write — not analyse or audit — a quality document: "write the procedure for...", "write the
  quality manual", "formalise process X", "document this work instruction", "help me write the
  quality policy". Complements smq-analysis (which audits and assesses ISO 9001 compliance) without
  replacing it: this skill produces the document, smq-analysis checks its compliance once written.
  Writes in the language the user is writing in.
---

# Writing quality documents

Write documented information the way a competent practitioner does: start from what actually happens
on the ground, not from what would be ideal on paper. The most frequent failure is not the absence of
a procedure but a procedure copy-pasted from a generic template, followed by no one because it does
not describe the real work — and which becomes a non-conformity in its own right at the first audit.

**Link with `smq-analysis`.** This skill writes; `smq-analysis` assesses ISO 9001 compliance and
audits. If a gap analysis or an audit has already identified what's missing, start from that finding
rather than reopening the diagnosis. If the user asks for both an audit and a write-up, audit first
with `smq-analysis`.

## Identifying the document to produce

| Document | Content | Typical length |
|---|---|---|
| **Quality policy** | Leadership commitment, direction, framework for objectives | 1 page |
| **Quality objectives** | Measurable targets, consistent with the policy, broken down by function | 1 page or a table |
| **Quality manual** | Overview of the QMS, scope, how processes connect — no longer mandatory since 2015, produce only if the user explicitly asks or it's an expected practice in their sector | Variable |
| **Process sheet** | One sheet per process: purpose, input/output data, actors, indicators, risks | 1-2 pages per process |
| **Documented procedure** | Description of a recurring activity: who does what, when, with what supporting record | 1-4 pages |
| **Work instruction** | Detailed operating method for a specific task, for whoever performs it | 1 page, often illustrated |

Do not produce a quality manual by default: it has not been a requirement of the standard since 2015.
Propose it only if the context justifies it (sector custom, a client or certifier requirement, an
explicit request).

## Before writing

Three things to establish, inferring them from the request as far as possible — ask only the
questions that genuinely change the document, never more than three:

1. **The actual process or activity.** How does this happen today, concretely — not how it should
   happen. A document that describes a non-existent ideal practice will never be followed.
2. **The actors and their roles.** Who triggers, who executes, who checks, who approves. An unnamed
   role is an activity that won't get done.
3. **The right level of formality.** See `references/proportionality.md`: how heavy the document
   needs to be depends on the organisation's size, the activity's complexity, and the competence of
   the people performing it — never on a standard template applied without judgement.

## The non-negotiables

**Describe, don't prescribe the ideal.** A procedure documents what is supposed to happen and is
actually followed in practice. If the gap between the real and the desired is significant, flag it to
the user rather than writing fiction — documenting an impracticable practice manufactures a
non-conformity in advance.

**Every activity has a named actor, never "the department" or "someone."** A generic role makes no
one accountable. Name the function (not the person, except in a very small organisation).

**Distinguish what is kept up to date from what is retained.** A procedure and a process sheet are
kept up to date (living documents); the records they produce (filled-in forms, minutes) are retained
as evidence. The document itself should state which records it produces and where they are kept.

**A procedure references the documents it uses or produces**, without copying them: forms, linked
work instructions, other upstream/downstream procedures. Cite, don't duplicate — duplication is the
leading cause of outdated documents that contradict their original.

**Format serves readability, not aesthetics.** A flowchart or a sequential table for a chain of steps
with branches; structured text for a policy or an objective. See `references/document-templates.md`
for the templates.

**Version from the first draft onward.** Version number, date, author, approver, revision history —
even for a document intended for quick revision. A quality document with no version identification is
not under control in the sense of clause 7.5.

## Method

`references/writing-method.md` — how to gather information from the user when the real process isn't
yet clear, how to structure a process sheet (purpose, PRS — Pilot/Resources/Support —, input/output
data, indicators, risks, interactions), and the most frequent pitfalls (an over-detailed procedure, a
vague role, no exception cases).

`references/document-templates.md` — ready-to-use templates for each document type listed above: the
standard procedure structure, the process-sheet outline, a typical flowchart, the quality-manual
canvas.

`references/proportionality.md` — how to calibrate the level of detail to the organisation's size and
complexity, with contrasted examples (a 5-person structure vs. an industrial group) for the same
activity.

## Output

Decided case by case, never by default.

- **In the conversation** — a short policy, a simple process sheet, a question about a document's
  structure.
- **`.md`** — a document the user wants to keep or rework.
- **`.docx`** — a procedure, quality manual, or sheet meant to be circulated, signed, or filed in the
  official document-control system. Read the `docx` skill first.

## Limits

This skill writes quality documents; it does not certify their compliance. Once a document is
written, have its ISO 9001 compliance checked by `smq-analysis` before distribution if certification
or external audit is at stake.
</content>
