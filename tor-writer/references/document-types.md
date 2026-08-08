# Document typology — deltas from the baseline TDR

Each entry states what changes relative to the Terms of Reference described in SKILL.md:
perspective, sections added, removed, renamed, and type-specific traps. Read only the entry for the
chosen type. For French headings, use the glossary at the top of `sections.md`.

**Contents**
1. [Terms of Reference — baseline](#1-terms-of-reference--baseline)
2. [Scoping note](#2-scoping-note)
3. [Work plan / action plan](#3-work-plan--action-plan)
4. [Requirements specification](#4-requirements-specification)
5. [Tender dossier](#5-tender-dossier)
6. [Technical proposal](#6-technical-proposal)
7. [Project / presentation dossier](#7-project--presentation-dossier)
8. [Audit plan](#8-audit-plan)
9. [Master plan](#9-master-plan)
10. [Activity or progress report](#10-activity-or-progress-report)

---

## 1. Terms of Reference — baseline

*French: termes de référence (TDR).*

**Issuer**: the commissioning party. **Recipient**: the implementer, a bidder, a hierarchy.
**Register**: technical and contractual, third person, present indicative.

This is the structure described in SKILL.md. No delta. All other types derive from it.

**Main trap**: terms of reference state what must be obtained, not how the provider must proceed in
detail. Too much methodological prescription kills competition between bids and shifts
responsibility for the result onto the commissioning party.

---

## 2. Scoping note

*French: note de cadrage.*

**Issuer**: internal sponsor. **Recipient**: a hierarchy that must decide quickly.
**Typical level**: L0 to L1. **Target length**: 1 to 3 pages.

**Sections retained**: summary sheet, purpose, condensed context, objectives, main activities,
deliverables, duration, overall budget, decision requested.

**Section added**:

| Section | Content |
|---------|---------|
| **Decision requested** (*décision attendue*) | State explicitly what the recipient must approve: a budget, a launch, an appointment, a direction. A note with no explicit request produces no decision. |

**Sections removed**: table of contents, acronyms, list of tables and figures, communication plan,
terms and conditions, annexes, bibliography, preventive risk analysis.

**Main trap**: a scoping note is not a shortened TDR, it is a decision instrument. If the reader does
not know by the end what they are being asked to settle, the note has failed.

---

## 3. Work plan / action plan

*French: plan de travail / plan d'action.*

**Issuer**: operating unit. **Recipient**: team and supervisor. **Typical level**: L1 to L2.

**Sections reinforced**: methodology (becomes the core of the document, at task level), schedule,
responsibilities, deliverables, performance indicators.

**Sections added**:

| Section | Content |
|---------|---------|
| **Prioritisation** (*priorisation*) | Impact / effort / priority table (impact ÷ effort), descending order. See `upstream-methods.md`. |
| **Monitoring arrangements** (*modalités de suivi*) | Frequency of progress reviews, reporting format, who consolidates. |

**Sections removed or reduced**: context cut to a reminder, executive summary, terms and conditions,
reference framework (unless mandatory), communication plan (merged into monitoring arrangements).

**Main trap**: a work plan without start and end conditions per activity is only a list. Those
conditions are what make the schedule hold.

---

## 4. Requirements specification

*French: cahier des charges.*

**Issuer**: commissioning party. **Recipient**: suppliers, integrators, service providers.
**Typical level**: L2 to L3. **Register**: specification — every requirement must be verifiable.

**Sections added**:

| Section | Content |
|---------|---------|
| **Functional requirements** (*exigences fonctionnelles*) | What the solution must allow users to do, from a usage standpoint. One requirement = an identifier + a testable statement + a status (mandatory / desirable). |
| **Technical requirements** (*exigences techniques*) | Architecture, interoperability, security, performance and compatibility constraints. |
| **Service requirements** (*exigences de service*) | Warranty, maintenance, training, documentation, reversibility, skills transfer. |
| **Acceptance criteria** (*critères de recette*) | How satisfaction of each requirement is verified. Without this section, acceptance is arbitrary. |

**Sections transformed**: the methodology describes the procurement and acceptance process, not the
provider's activities. The resources section becomes the specification of the need.

**Main trap**: confusing a functional requirement (what it must do) with a technical one (how it is
built). Specifying technically what should have stayed functional eliminates valid solutions and
raises prices. Number the requirements (FR-01, TR-01…): they will be reused verbatim in bids and at
acceptance.

---

## 5. Tender dossier

*French: dossier d'appel d'offres (DAO).*

**Issuer**: contracting authority. **Recipient**: bidders. **Typical level**: L3 only.
**Register**: legal and procedural.

**Structure**: the tender dossier wraps the terms of reference or the requirements specification,
which becomes one of its parts.

**Sections added**:

| Section | Content |
|---------|---------|
| **Notice of invitation to tender** (*avis d'appel d'offres*) | Subject, funding source, procurement method, deadline date and time, place of submission. |
| **Instructions to bidders** (*règlement de la consultation*) | Eligibility conditions, composition of the envelopes, format of bids, validity period, collection and submission arrangements. |
| **Qualification criteria** (*critères de qualification*) | Legal, financial and technical capacity; required references; administrative documents. |
| **Evaluation criteria and scoring** (*critères d'évaluation et notation*) | Weighted technical / financial grid, minimum technical score, comparison method. **The grid must be published**: evaluating on undisclosed criteria is contestable. |
| **Price schedule template** (*cadre du bordereau des prix*) | Imposed structure of the price schedule, so bids are comparable. |
| **Draft contract and clauses** (*projet de marché*) | Penalties, advances, retention money, termination, dispute resolution. |
| **Standard forms** (*modèles de formulaires*) | Bid letter, attestations, guarantee template. |

**Main trap**: any ambiguity in a tender dossier is paid for in appeals or amendments. Check in
particular the consistency between the announced evaluation criteria, the documents requested and
the imposed price schedule. Remind the user that the dossier remains subject to the applicable
public procurement code, which this skill does not presume — flag it as to be verified.

---

## 6. Technical proposal

*French: offre technique / proposition de services.*

**Issuer**: the **bidder**. Perspective is inverted relative to every other entry.
**Recipient**: the commissioning party that issued the terms of reference or the requirements
specification. **Typical level**: L2 to L3. **Register**: demonstrative and persuasive, first person
plural.

**Sections transformed**:

| TDR section | Becomes, in the proposal |
|-------------|--------------------------|
| Context and rationale | **Understanding of the assignment** — restate the client's need to prove it is understood, and point out what the terms of reference omitted |
| Objectives | **Results we commit to deliver** |
| Methodology | **Proposed approach** — the section that wins the contract: phases, methods, tools, differentiating value |
| Project team | **Proposed team** — named profiles, CVs in annex, level of effort per expert |
| Cost | **Financial offer** — often in a separate envelope; follow the imposed price schedule strictly |

**Sections added**:

| Section | Content |
|---------|---------|
| **Bidder profile** | Legal status, track record, capacity, accreditations. |
| **Comparable references** | Similar assignments: client, subject, amount, year, completion certificate. Decisive for scoring. |
| **Compliance matrix** | Table mapping each requirement of the terms of reference → response provided → page of the proposal. The single strongest scoring accelerator: the evaluator stops searching. |
| **Understanding of risks and proposed measures** | Demonstrates the bidder's maturity. |

**Sections removed**: revision and approval, internal communication plan, the full preventive risk
analysis (keep it in annex where it strengthens the bid).

**Main traps**: (1) copying the terms of reference instead of restating them — evaluators spot it
immediately and award no comprehension points; (2) proposing a generic methodology unconnected to
the client's context; (3) departing from the imposed price schedule, which can lead to outright
rejection.

---

## 7. Project / presentation dossier

*French: dossier de projet / dossier de présentation.*

**Issuer**: project sponsor. **Recipient**: donor, patron, sponsor, investment committee.
**Typical level**: L2 to L3. **Register**: persuasive, impact-oriented.

**Sections added**:

| Section | Content |
|---------|---------|
| **Project sponsor** | Legitimacy, experience, track record, governance. |
| **Problem statement and stakes** | Expanded, argued and quantified version of the context. |
| **Expected impact** | Quantified effects on beneficiaries: number, nature, time horizon. Goes further than the added value section of a TDR. |
| **Financing plan** | Breakdown by source: own contribution, grant requested, co-funding secured and pending. |
| **Sustainability after funding** | What survives once funding ends. Donors ask this systematically; sponsors often omit it. |
| **Logical framework** (institutional donors) | Overall objective / specific objective / results / activities × indicators / verification sources / assumptions. |

**Sections reinforced**: executive summary (often the only part read at first screening), target
groups, indicators, detailed budget.

**Main trap**: presenting activities rather than impact. A donor does not fund workshops, it funds a
measurable change. Every activity must be explicitly tied to an effect on beneficiaries.

---

## 8. Audit plan

*French: plan d'audit.*

**Issuer**: auditor or control function. **Recipient**: audited entity and commissioning party.
**Typical level**: L2.

**Sections transformed**: the reference framework becomes central — it is what grounds every
judgement. The objectives become audit objectives; the methodology becomes the audit approach.

**Sections added**:

| Section | Content |
|---------|---------|
| **Audit reference framework** | Enforceable texts, standards, procedures and good practices, precisely located. |
| **Audit field and limits** | What is covered and, explicitly, what is not. |
| **Work programme** | Per domain: control objective, planned tests, evidence to collect, sampling. |
| **Reporting arrangements** | Opening meeting, progress reviews, closing meeting, right of reply, final report. |
| **FRAP template** | The problem analysis sheet to be used for each finding. |

**Main trap**: a finding without a cited reference framework is only an opinion. Every anomaly must
be traceable to an identified and located requirement.

---

## 9. Master plan

*French: plan directeur.*

**Issuer**: executive management. **Horizon**: multi-year. **Typical level**: L3.

**Sections transformed**: objectives become strategic axes broken down into operational objectives;
methodology becomes a project portfolio; schedule becomes a multi-year roadmap with annual
milestones.

**Sections added**:

| Section | Content |
|---------|---------|
| **Baseline assessment** | Evidenced diagnosis of the current situation, supported by PESTEL and SWOT. |
| **Target vision** | The target situation at the horizon, described concretely and verifiably. |
| **Strategic axes** | 3 to 6 axes, each broken down into operational objectives then projects. |
| **Trajectory** | Multi-year sequencing: what happens in year 1, 2, 3, and why in that order. |
| **Governance and steering** | Governance bodies, frequency, dashboard, periodic revision of the plan. |

**Main trap**: a master plan that does not descend to identified and budgeted projects stays
declaratory. Every axis must yield at least one project carrying its own terms of reference.

---

## 10. Activity or progress report

*French: rapport d'activité ou d'étape.*

**Issuer**: implementer. **Register**: retrospective and factual, past tense.
**Typical level**: L1 to L2.

The report is the **mirror** of the terms of reference: it follows their structure and accounts,
section by section, for the gap between planned and delivered.

**Sections transformed**:

| TDR section | Becomes, in the report |
|-------------|------------------------|
| Objectives | Achievement level per objective, with its indicator |
| Methodology | Activities actually carried out, deviations and their justification |
| Schedule | Actual vs planned, causes of slippage |
| Deliverables | Deliverables produced, submission date, approval status |
| Risks | Risks that materialised, treatment applied, residual risks |
| Cost | Spent vs budgeted, execution rate, justification of overruns |

**Sections added**:

| Section | Content |
|---------|---------|
| **Highlights of the period** | What shaped the period, positively and negatively. |
| **Difficulties encountered** | Owned and documented, with how they were handled. |
| **Outlook and recommendations** | What is proposed next — often the seed of the following terms of reference. |

**Main trap**: a report that does not compare against the original terms of reference is not
auditable. Always present actuals against plan, including when the variance is unfavourable — an
explained variance protects its author, a concealed one does not.
