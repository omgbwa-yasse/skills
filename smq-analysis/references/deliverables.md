# Deliverables: structures and templates

Read before producing a gap matrix, an audit report, a non-conformity sheet, or a management-review
dossier.

**Contents:** [Gap analysis matrix](#gap-analysis-matrix) · [Rating scale](#rating-scale) · [Internal audit report](#internal-audit-report) · [Non-conformity and corrective-action sheet](#non-conformity-and-corrective-action-sheet) · [Management review dossier](#management-review-dossier) · [Process sheet](#process-sheet)

---

## Gap analysis matrix

One line per requirement, not per clause — a clause contains several distinct requirements, and
merging them into one line hides gaps.

| Column | Content |
|---|---|
| Clause | Precise number, down to the sub-clause when relevant (7.2 d, 9.3.2 e) |
| Requirement | A short restatement of what is required |
| Applicable | Yes / No + justification if no |
| Current situation | What actually exists — factual |
| Evidence examined | Document, interview, observation. Blank = not evaluated, not "compliant" |
| Level | See the scale below |
| Gap | Precisely what is missing |
| Action | What needs to be done |
| Owner | A named role |
| Deadline | |
| Priority | 1 to 3 |
| Status | To do / In progress / Done / Verified |

**In `.xlsx`** — read the `xlsx` skill first. Tab 1: scope, context, and method of the analysis.
Tab 2: the matrix, frozen header row, active filters, data validation on the Level, Priority, and
Status columns. Tab 3: the action plan sorted by owner and deadline. Tab 4: a summary by clause with
conformity rate.

---

## Rating scale

Four levels, stable from one piece of work to the next:

| Level | Meaning |
|---|---|
| **Conforming** | The requirement is met and evidence exists |
| **Partially conforming** | The arrangement exists but is incomplete, not deployed everywhere, or the evidence is lacking |
| **Non-conforming** | The requirement is not met |
| **Not evaluated** | No evidence has been examined |

"Not evaluated" is a level in its own right, not an admission of weakness. Folding it into
"conforming" out of optimism, or into "non-conforming" out of caution, distorts the analysis either
way.

Avoid numeric scoring (0 to 5, maturity percentages) unless explicitly requested: it gives a
qualitative judgement the appearance of a measurement, and an overall conformity rate hides the fact
that a single major nonconformity blocks certification regardless of the overall score.

---

## Internal audit report

```
1. Identification
   — scope, audit criteria (clauses + internal documents), dates,
     auditors, auditees, audit plan reference
2. Method and sampling
   — sources consulted, sample size and selection method,
     limits of the audit
3. Summary
   — overall assessment, number of findings by category,
     strengths, points of vigilance
4. Findings
   — one per block: category, clause, requirement, evidence, gap
5. Strengths
   — effective arrangements worth maintaining or spreading elsewhere
6. Conclusion
   — is the QMS conforming, effectively implemented, and maintained
     across the scope audited (the wording from 9.2.1)
7. Expected follow-up
   — response deadlines, follow-up arrangements
```

Strengths are not a courtesy: they identify practices that can be transferred to other processes,
which is what 10.1 calls for.

---

## Non-conformity and corrective-action sheet

Structure aligned with 10.2.1, each section corresponding to a sub-clause.

```
REFERENCE / DATE / RAISED BY
Source: internal audit · external audit · customer complaint ·
        inspection · incident · other

1. DESCRIPTION OF THE NONCONFORMITY              [10.2.2 a]
   Requirement concerned (clause or internal requirement)
   Evidence / factual finding
   Gap

2. IMMEDIATE CORRECTION                          [10.2.1 a]
   Action to control and correct the occurrence
   Handling of consequences (customer informed? product segregated?)
   Owner / date

3. ROOT-CAUSE ANALYSIS                           [10.2.1 b.1, b.2]
   Method used (5 whys, Ishikawa, fault tree)
   Root cause(s) retained

4. EXTENSION CHECK                               [10.2.1 b.3]
   Do similar nonconformities exist elsewhere?
   Could they occur elsewhere?
   Finding of the search — including if the result is negative

5. CORRECTIVE ACTION                             [10.2.1 c]
   Action eliminating the cause
   Owner / deadline / resources

6. UPDATE TO RISKS AND THE QMS                   [10.2.1 e, f]
   Risks and opportunities to update?
   QMS change needed?

7. EFFECTIVENESS VERIFICATION                    [10.2.1 d]
   Effectiveness criterion defined in advance
   Verification date (after implementation)
   Result observed
   Closure: date / owner
```

Sections 4, 6, and 7 are the ones almost always missing from sheets actually used in practice — and
they're what distinguishes a corrective action from a plain correction. Never close a sheet without
section 7 filled in with an observed result.

---

## Management review dossier

Agenda mirroring 9.3.2, in the standard's order, so completeness can be checked:

```
INPUTS                                                      [9.3.2]
a) Status of actions from previous reviews
b) Changes in relevant external and internal issues
c) QMS performance and effectiveness — as TRENDS:
   1) customer satisfaction and feedback from interested parties
   2) degree to which quality objectives have been met
   3) process performance and conformity of products and services
   4) nonconformities and corrective actions
   5) monitoring and measurement results
   6) audit results
   7) performance of external providers
d) Adequacy of resources
e) Effectiveness of actions taken to address risks and opportunities
f) Opportunities for improvement

OUTPUTS — decisions and actions related to:                 [9.3.3]
a) opportunities for improvement
b) any need for changes to the QMS
c) resource needs
```

Two points of vigilance. Item c) requires **trends**, not point-in-time values: present the evolution
across several periods. The minutes must contain **decisions**, not just findings — a management
review with no recorded decision does not satisfy 9.3.3, whatever the quality of the data presented.

---

## Process sheet

A complete sheet answers the eight questions from 4.4.1:

```
Process name / Pilot
Purpose — what it's for, for whom

Inputs                     → activities →          Outputs
Suppliers (upstream)                                Customers (downstream)

Interactions — upstream and downstream processes, nature of the exchanges

Resources: human, material, informational
Competence required
Responsibilities and authorities

Control criteria and methods
Performance indicators — definition, target, frequency, owner

Process risks and opportunities, and associated actions

Documented information: to maintain / to retain

Process evaluation and improvement arrangements
```

Adapt the level of detail to the process's criticality. A three-page sheet for a low-stakes support
process is a maintenance cost with no payoff — and becomes a source of internal nonconformities as
soon as it falls out of date.
</content>
