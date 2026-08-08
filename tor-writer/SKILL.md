---
name: tor-writer
description: >
  Writes, structures and audits Terms of Reference (TDR) and their derived documents: scoping note,
  work plan, action plan, requirements specification, tender dossier, technical proposal, project or
  presentation dossier, audit plan, master plan, progress report. Trigger for any request to draft,
  structure, outline or review these — e.g. "draft terms of reference for...", "rédige les TDR
  pour...", "I need a requirements specification", "prepare a technical proposal", "write a scoping
  note", "review this TDR", "what budget goes in this project?". Also trigger when the user describes
  a project or mission that must be approved by a hierarchy, a donor or a client, even without naming
  the document. Produces one to fifty pages. Strict six-stage pipeline with validation gates.
  Markdown by default, .docx on request. Deliverables follow the user's language.
---

# Terms of Reference and related documents

Production skill for scoping and contractual documents: Terms of Reference (TDR, from the French
*termes de référence*) and their ten variants. Built on the **MPR** principle (Method – Planning –
Resources): quality, cost and lead time cannot be decreed; they are consequences of working methods,
planning and resources. This principle governs the entire writing order below.

## Output language

Write the deliverable in the language the user is writing in. This document family is rooted in
French-language professional practice, so **when producing in French, use the French headings from
the bilingual glossary at the top of `references/sections.md`** rather than translating the English
names in this file. The skill's own instructions are English; the documents it produces are not
necessarily.

---

## PIPELINE OVERVIEW

```
STAGE 1 → SCOPING       : document type, depth level, 8 key inputs   → VALIDATION
STAGE 2 → UPSTREAM      : FRAP (problem) or OKR (objective)          → VALIDATION
STAGE 3 → ARCHITECTURE  : selected sections + coherence matrix       → VALIDATION
STAGE 4 → WRITING       : 8 blocks in the mandatory MPR order        → VALIDATION per block
STAGE 5 → QUALITY       : three verification engines
STAGE 6 → DELIVERY      : Markdown in chat, .docx on request
```

**Absolute rule: never move to the next stage without explicit validation.** This holds even for a
one-page document. Validation gates are shorter at L0/L1, never absent.

**Second absolute rule: never write a duration or a cost before the methodology and resources are
written.** This is the core of MPR. A budget written before the activities is an invented budget.

---

## THE TWO ROUTING AXES

Everything else follows from crossing these two axes. Determine both at Stage 1.

### Axis 1 — Document type

| Type | Issuer | Dominant register |
|------|--------|-------------------|
| **Terms of Reference (TDR)** — baseline | Commissioning party | Technical and contractual |
| **Scoping note** | Internal sponsor | Decision-oriented, condensed |
| **Work plan / action plan** | Operating unit | Operational, sequenced |
| **Requirements specification** | Commissioning party | Specification, requirement-driven |
| **Tender dossier** | Contracting authority | Legal and procedural |
| **Technical proposal** | **Bidder** | Persuasive, demonstrative |
| **Project / presentation dossier** | Project sponsor | Persuasive, funding-oriented |
| **Audit plan** | Auditor | Methodological, standards-based |
| **Master plan** | Executive management | Strategic, multi-year |
| **Activity or progress report** | Implementer | Retrospective, factual |

Read `references/document-types.md` as soon as the type is identified: each entry lists the sections
added, removed or renamed relative to the baseline TDR, plus the traps specific to that type.
**Never draft a technical proposal or a tender dossier without reading its entry** — the reversal of
perspective (bidder instead of commissioning party) changes half the sections.

### Axis 2 — Depth level

| Level | Volume | Methodological granularity | Typical use |
|-------|--------|----------------------------|-------------|
| **L0** | 1 page | Actions only | Scoping note, project sheet, internal submission |
| **L1** | 2–4 pages | Actions + activities | Workshop TDR, short mission, work plan |
| **L2** | 8–15 pages | Activities + tasks | Standard TDR, requirements spec, technical proposal |
| **L3** | 25–50 p. + annexes | Programmes → tasks | Tender dossier, master plan, project for funding |

**Compression rule: sections are dropped, never truncated.** A sentence stays a complete sentence at
L0 as at L3. What varies is the number of sections and the number of columns in the tables.

If the user does not state a volume, infer it from what is at stake (budget, number of stakeholders,
contractual nature) and announce the chosen level in the Stage 1 recap.

---

## ENGINE 1 — SECTION SELECTION

Reference table for a **TDR**. For any other variant, then apply the deltas in
`references/document-types.md`.

| # | Section | L0 | L1 | L2 | L3 |
|---|---------|----|----|----|----|
| 01 | Cover | – | ○ | ● | ● |
| 02 | Table of contents | – | – | ● | ● |
| 03 | Executive summary | – | – | ○ | ● |
| 04 | Acronyms and abbreviations | – | – | ○ | ● |
| 05 | List of tables and figures | – | – | – | ○ |
| 06 | Revision and approval | – | ○ | ● | ● |
| 07 | Summary sheet | ● | ● | ● | ● |
| 08 | Purpose | ● | ● | ● | ● |
| 09 | Context and rationale | ○ | ● | ● | ● |
| 10 | Scope | ○ | ● | ● | ● |
| 11 | Location | – | ● | ● | ● |
| 12 | Date or duration | ● | ● | ● | ● |
| 13 | Reference framework | – | ○ | ● | ● |
| 14 | Target groups | – | ● | ● | ● |
| 15 | Objectives | ● | ● | ● | ● |
| 16 | Added value / expected results | – | ○ | ● | ● |
| 17 | Methodology | ● | ● | ● | ● |
| 18 | Performance indicators | – | – | ● | ● |
| 19 | Preventive risk analysis | – | – | ○ | ● |
| 20 | External risks | – | ○ | ● | ● |
| 21 | Schedule | ○ | ● | ● | ● |
| 22 | Communication plan | – | – | ○ | ● |
| 23 | Deliverables | ● | ● | ● | ● |
| 24 | Responsibilities | – | ○ | ● | ● |
| 25 | Project team | – | ○ | ● | ● |
| 26 | Terms and conditions | – | – | ● | ● |
| 27 | Resources | ○ | ● | ● | ● |
| 28 | Cost | ● | ● | ● | ● |
| 29 | Annexes | – | – | ○ | ● |
| 30 | Bibliography | – | – | ○ | ● |

● mandatory · ○ recommended, include if the information exists · – out of scope at this level

At **L0** these sections are not separate headings: they become the rows of a single summary sheet.

Section-by-section detail — purpose, expected content, table template, common errors — is in
`references/sections.md`, which also carries the bilingual heading glossary. Consult it section by
section during Stage 4, not before.

---

## ENGINE 2 — COHERENCE MATRIX

Build this chain at Stage 3, before any writing. It is the check that separates a real TDR from a
stack of headings.

```
Problem or opportunity
   └→ PURPOSE
        └→ General objective
             └→ Specific objectives (1..n)
                  └→ Activities / tasks  ──→ Resources ──→ Budget lines
                       └→ Deliverables
                       └→ Schedule milestones
                       └→ KPIs + verification sources
                       └→ Risks + treatment measures
```

**Orphan test.** No element may be left dangling:

- [ ] Every specific objective is covered by at least one activity
- [ ] Every activity produces at least one deliverable
- [ ] Every activity mobilises at least one identified resource
- [ ] Every resource appears in a budget line (or is explicitly stated as supplied by a party)
- [ ] Every objective has at least one measurable indicator and a verification source
- [ ] Every deliverable is dated in the schedule
- [ ] Every significant risk has a treatment measure and an owner
- [ ] The purpose covers the full set of specific objectives (mandatory feedback loop after writing them)

Present this matrix as a table to the user at the Stage 3 validation gate for L2 and L3. At L0/L1,
check it internally and report only the orphans found.

---

## ENGINE 3 — MANDATORY MPR SEQUENCE

The **writing** order is not the **reading** order. Always write in this sequence:

| Block | Content | Why here |
|-------|---------|----------|
| **A — Frame** | Purpose, context and rationale, scope, location, target groups, reference framework | Bounds what is possible before any commitment |
| **B — Intent** | General and specific objectives, added value, deliverables | The intended result precedes the means |
| **C — M (Method)** | Methodology, project team, responsibilities, communication plan | The "how" drives everything downstream |
| **D — R (Resources)** | Resources | Derived line by line from the Block C activities |
| **E — P (Planning)** | Schedule, **then** the resulting total duration | Duration is an output, never an assumption |
| **F — Control** | Performance indicators, preventive risk analysis, external risks | Derived from activities; may amend Block C |
| **G — Costing** | Cost | Derived exclusively from Blocks D and E |
| **H — Wrapper** | Summary sheet, executive summary, table of contents, acronyms, revision block, cover, annexes, bibliography | Can only summarise what already exists |

**Mandatory feedback loop after Block F**: the preventive risk analysis produces measures that must
be fed back into the methodology (Block C) before costing. Tell the user which methodology entries
changed at that point.

**The executive summary is written last**, after the cost. No exception.

---

## STAGE 1 — SCOPING

### 1.1 The 8 inputs

Extract from the user's request first. Ask at most **3 questions per exchange**, only on genuinely
blocking inputs.

| # | Input | Blocking if missing? |
|---|-------|----------------------|
| 1 | Document type and target level | Yes — infer and confirm |
| 2 | Purpose of the mission or activity | Yes |
| 3 | Commissioning organisation and beneficiaries | Yes |
| 4 | Problem to solve or objective pursued | Yes |
| 5 | Scope (location, population, resources concerned) | No — inferable, confirm |
| 6 | Known time and budget constraints | No — may stay open (MPR) |
| 7 | Applicable reference framework (law, standard, procedure) | No — propose the likely ones |
| 8 | Final recipient of the document and intended use | Yes — sets the register |

### 1.2 Missing-information protocol

Never block production on a missing input. Three permitted treatments, one prohibited:

- **Infer** where the context allows → state the assumption in the recap;
- **Flag** `[TO BE COMPLETED: <what is missing>]` for anything only the user holds (real amounts,
  names, imposed dates, internal references). Use the equivalent flag in the output language —
  `[À COMPLÉTER : …]` in French;
- **Ask** only for the blocking inputs in the table above;
- ❌ **Never invent** an amount, a headcount, a date, a legal reference number or a standard. A cited
  standard must exist and be verified; otherwise flag it as to be verified.

### 1.3 Validation recap

At the end of Stage 1, present: chosen document type, level, restated purpose, beneficiaries,
assumptions made, missing inputs identified. Close by asking the user to confirm the scoping or
correct it before the analysis starts.

---

## STAGE 2 — UPSTREAM ANALYSIS

Pick the tool based on what triggered the document:

| Trigger | Tool | Reference |
|---------|------|-----------|
| An observed problem, an underperformance | **FRAP** (problem analysis and resolution sheet) | `references/upstream-methods.md` |
| An objective, an ambition, an opportunity | **OKR** (objectives and key results) | `references/upstream-methods.md` |
| An imposed instruction, no analysis possible | **PESTEL** and/or **SWOT** alone | `references/upstream-methods.md` |

At **L0/L1**: produce a condensed version (findings + main causes + retained recommendations) in a
few lines, without the full tables.
At **L2/L3**: produce the complete FRAP or OKR table; it goes into the annexes of the final document.

This stage feeds the context, the rationale, the objectives and the activities directly. Never skip
it: it is what makes the document defensible before a decision-making body.

Present the result and request validation before moving to architecture.

---

## STAGE 3 — ARCHITECTURE

1. Apply **Engine 1**: list the selected sections, with a rationale for those left out.
2. Build the detailed outline: each section heading plus one line stating its content.
3. Build the **coherence matrix** (Engine 2) and run the orphan test.
4. Announce the output format: Markdown in chat by default; note that a `.docx` is available on
   request.

Present all of it, then ask the user whether to add, remove or reorder sections before writing
begins.

---

## STAGE 4 — WRITING

Write in the order of the 8 blocks of **Engine 3**. Consult `references/sections.md` when writing
each section, and the specialised references when the block calls for them:

- Block C → `references/sections.md` (11-column methodology template, reducible)
- Block E → `references/planning-and-costing.md` (Gantt, PERT, start and end conditions)
- Block F → `references/risks-and-kpis.md` (metrics → operational KPIs → project KPI; four-step
  preventive risk analysis)
- Block G → `references/planning-and-costing.md` (budget structure, billing units)

**Validation rhythm:** blocks A+B together, then C, then D+E, then F, then G, then H. At L0/L1,
group into two passes only (A→C, then D→H).

### Writing rules

- **Present indicative** for commitments; future tense only for dated events.
- **Neutrality**: state facts, never comment or qualify. No intensity adjectives in a finding — "a
  30 to 35% drop in sales", not "a sharp drop".
- **Quantify wherever possible**: quantities, percentages, headcounts, durations, units.
- **Infinitive verbs** for recommendations, activities and specific objectives.
- **One objective = what + who + why + where + how + when**, at least three of the six.
- **No presuppositions**: what is not written is not owed. Every implicit assumption is a future
  budget loss.
- **Tables rather than prose** for methodology, resources, KPIs, risks, schedule and cost.
- ❌ Never write "TDRs" when writing in French — the plural is carried by the article, not by the
  acronym.
- ❌ Never conflate **purpose** (what is being done?) with **objectives** (why, and for what results?).
- ❌ Never conflate **added value** (gain for the organisation) with a **deliverable** (tangible
  output proving the work was done).

---

## STAGE 5 — QUALITY CONTROL

Run before delivery, in this order, fixing rather than flagging:

1. **Orphan test** (Engine 2) replayed on the final text;
2. **Eight-pitfall test** — see `references/quality-control.md`;
3. **Type conformity test** — are the sections specific to this document type present
   (`references/document-types.md`)?

Then present a short summary: corrections made, remaining to-be-completed zones, points requiring a
decision from the user.

---

## STAGE 6 — DELIVERY

**Default: Markdown in the conversation**, complete document, tables included. For a long document
(L3), deliver in successive parts.

**On explicit request only: `.docx`.** In that case, read `/mnt/skills/public/docx/SKILL.md` first,
then apply `assets/docx-style-guide.md`. Never generate a file the user has not asked for.

At the end of delivery, offer in one sentence: conversion to `.docx`, and the companion documents
that naturally follow from what was produced (a delivered TDR often calls for a requirements
specification, a work plan or a tender dossier). Name the specific skill each implies: once the
document is approved and the mission starts, `project-tracker` takes over the schedule and budget it
lays out; if it needs to be pitched to a funder or a governing committee rather than only filed,
`presentation-writer` turns its coherence matrix into a talk; if the go/no-go itself is contested and
needs to be argued rather than assumed, that argument belongs in a `decision-memo`, not in the TDR's
own summary sheet.

---

## COUNTER-EXPERTISE MODE

If the user submits an existing document for review ("review this TDR", "does this specification
hold up?"), switch to the audit protocol in `references/quality-control.md`: scoring across six
dimensions, pitfalls detected, missing sections, orphans in the coherence chain, proposed rewordings.
The writing pipeline does not apply in this mode — unless the user then asks for a rewrite, in which
case resume at Stage 3.

---

## REFERENCE FILES

| File | When to read it |
|------|-----------------|
| `references/document-types.md` | Stage 1, as soon as the document type is known — **mandatory** |
| `references/sections.md` | Stage 4, section by section; also holds the bilingual heading glossary |
| `references/upstream-methods.md` | Stage 2 |
| `references/risks-and-kpis.md` | Stage 4, Block F |
| `references/planning-and-costing.md` | Stage 4, Blocks E and G |
| `references/quality-control.md` | Stage 5, and counter-expertise mode |
| `assets/table-templates.md` | Stage 4, for every table |
| `assets/docx-style-guide.md` | Stage 6, only if `.docx` is requested |
| `/mnt/skills/public/docx/SKILL.md` | Stage 6, only if `.docx` is requested |
