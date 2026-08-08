---
name: smq-analysis
description: Analyses, designs, audits, and improves a quality management system under ISO 9001:2015 — gap analysis, internal audit, process mapping, documented information, non-conformities and corrective actions, management review, certification readiness. Trigger as soon as the topic is QMS, ISO 9001, quality management, quality assurance, quality manual, quality policy or objectives, documented procedure, quality record, quality audit, audit finding, non-conformity, corrective action, CAPA, management review, customer satisfaction, control of external providers, process approach, PDCA — and also when someone asks whether their organisation is ready for certification, what a specific clause requires, how to document a process, or how to respond to a gap raised by an auditor. Applies to any organisation regardless of size or sector, including services, software, and the public sector. Writes in the language the user is writing in.
---

# Quality management system analysis (ISO 9001:2015)

Treat a QMS the way a competent practitioner does: start from what the standard actually requires,
look for evidence before concluding, and calibrate how heavy the system is to the organisation's size
and complexity.

Two symmetrical failure modes to avoid. The first: producing a complacent conformity assessment, made
of unsupported "conforms," which collapses at the first certification audit. The second, even more
frequent: demanding things ISO 9001:2015 does not ask for — a quality manual, six mandatory documented
procedures, a management representative, separate preventive actions. All of that disappeared in
2015. See the full list in `references/clause-requirements.md`.

**Language.** Write in the language of the request. Official terminology exists in both French and
English; use whichever the request is in ("informations documentées" / *documented information*,
"prestataire externe" / *external provider*, "éléments de sortie" / *outputs*) and give the
equivalent in parentheses the first time if the user is working in a bilingual context.

## Identifying the request

Six types of work, which call for different deliverables:

| Type | Trigger | Expected output |
|---|---|---|
| **Gap analysis** | "where do we stand against ISO 9001?" | A clause-by-clause matrix: requirement, current situation, gap, action, priority |
| **Internal audit** | "prepare/run an audit on process X" | Audit plan, questions, findings classified with evidence, report |
| **QMS design** | "we're starting from scratch", "help me document" | Process map, policy, objectives, document structure |
| **Non-conformity / corrective action** | "the auditor raised a gap", "we have a complaint" | Root-cause analysis, correction vs. corrective action, evidence of effectiveness |
| **Management review** | "prepare the management review" | Agenda aligned with 9.3.2, input data, expected decisions |
| **One-off question** | "what does clause 8.4 require?" | A direct answer, without running the full apparatus |

Do not run a full gap analysis when the user asks what a clause requires. State the type of work
engaged in one line, then do it.

## The six non-negotiables

**Evidence before verdict.** A conformity judgement rests on a document consulted, an observation, an
interview, or a record — cited. "Seems compliant" is not a finding. When no evidence has been
supplied, don't rule: say what would need to be examined to rule. An audit built on assumptions is
worse than no audit at all, because it gives false assurance.

**The requirement before the interpretation.** Cite the clause number, restate the requirement, then
only apply it to the case. Never invent a requirement absent from the standard, and never harden a
recommendation ("should") into an obligation ("shall"). This distinction is structural: only "shall"
is auditable.

**Distinguish *maintain* from *retain*.** "Maintaining documented information" means a living
document, kept up to date (policy, objectives, scope). "Retaining documented information" means fixed
evidence of what happened (review results, evidence of competence, audit findings). Conflating the two
produces either an unmaintainable document system or a lack of traceability. The full inventory is in
`references/documented-information.md`.

**Proportionality is in the standard, not a leniency.** The extent of documented information
legitimately varies with the organisation's size, the complexity of its processes, and people's
competence. A five-person firm and an industrial group can both satisfy the same requirements with
very different systems. Systematically proposing the heaviest setup is an analytical error, not
prudence.

**Findings are classified, and every finding is built the same way.** Major non-conformity / minor
non-conformity / opportunity for improvement / observation. Every non-conformity states three things:
the requirement (clause), the evidence (what was observed), the gap (how the evidence fails to meet
the requirement). A finding missing any of these three is not defensible to the auditee.

**Correction is not corrective action.** A correction addresses the occurrence; a corrective action
eliminates the cause to prevent recurrence. The standard also requires checking whether similar
non-conformities exist elsewhere or could occur — the step that's systematically forgotten, and the
one that distinguishes a system that learns from one that patches.

## The clauses

`references/clause-requirements.md` covers clauses 4 through 10 requirement by requirement, with what
to ask, what evidence to look for, and the most common gaps for each. Read it for any gap analysis,
any audit, and any question about a specific clause.

Overall structure, worth keeping in mind: **4 Context** (issues, interested parties, scope,
processes) · **5 Leadership** (commitment, customer focus, policy, roles) · **6 Planning** (risks and
opportunities, objectives, changes) · **7 Support** (resources, competence, awareness, communication,
documented information) · **8 Operation** (operational planning, customer requirements, design,
external providers, production, release, non-conformities) · **9 Performance evaluation** (monitoring
and measurement, customer satisfaction, internal audit, management review) · **10 Improvement**
(non-conformity and corrective action, continual improvement).

These clauses read within the PDCA cycle: 4 and 5 set the frame, 6 and 7 plan, 8 does, 9 checks, 10
acts. The through-line: context (4.1, 4.2) feeds risks and opportunities (6.1), which feed process
control (4.4, 8.1), whose effectiveness is evaluated (9.1) and improved (10). An analysis that treats
the clauses as an independent list misses the point — see `references/process-approach.md`.

## Analysis and audit method

`references/gap-audit-method.md`: how to run a gap analysis, an audit programme and plan, evidence-
gathering techniques, sampling, classifying and writing findings, follow-up. Read before any audit or
gap analysis.

`references/process-approach.md`: process mapping, turtle diagram, SIPOC, PDCA, the risk-based
approach, and how the clauses connect.

`references/deliverables.md`: structures for the gap matrix, the audit report, the non-conformity
sheet, the management-review dossier, and rating scales. Read before producing any deliverable.

## Link with risk analysis

Clause 6.1 requires determining risks and opportunities, without imposing a formal method or a risk
register — ISO 9001 does not require applying ISO 31000. Actions must be **proportionate to the
potential impact on the conformity of products and services**, which is the proportionality criterion
to apply.

When the user wants to go beyond the required minimum, or already has the `risk-analysis` skill
(ISO/IEC 31010), lean on it for identification and evaluation, then bring the result back to the 6.1
frame: what actions, how they're integrated into the QMS's processes, how their effectiveness is
evaluated. Don't impose a formal register on an organisation whose informal approach already satisfies
the requirement — that is a gap frequently raised wrongly.

## Output

Decided case by case, never by default. Infer it from the request; if there's genuine ambiguity on
substantial work, ask once.

- **In the conversation** — a question about a clause, a quick opinion, exploratory discussion.
- **`.md`** — a written analysis the user wants to keep or rework.
- **`.xlsx`** — a gap-analysis matrix, audit programme, non-conformity register: anything that lives
  and gets filtered. Read the `xlsx` skill first.
- **`.docx`** — an audit report, procedure, process manual, dossier intended for a client, management,
  or a certification body. Read the `docx` skill first.

## Limits

This skill produces quality analysis and documentation. It does not deliver certification, a
certification body's opinion, or a guaranteed outcome in a third-party audit. Regulated sectors apply
additional frameworks — IATF 16949 (automotive), AS/EN 9100 (aerospace), ISO 13485 (medical devices),
ISO 17025 (laboratories) — which add requirements and sometimes change their interpretation; flag this
when the context warrants it. A brief mention, at the end of the deliverable, without repeating it.
</content>
