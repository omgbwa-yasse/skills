# Quality control and counter-expertise

Two uses: Stage 5 of the pipeline (checking a document just written), and counter-expertise mode
(auditing a document submitted by the user).

---

## PART 1 — CHECKING A PRODUCED DOCUMENT (Stage 5)

### 1.1 Orphan test

Replay the Engine 2 coherence matrix on the final text, not on the outline. Fix, do not merely flag.

- [ ] Every specific objective is covered by at least one activity
- [ ] Every activity produces at least one deliverable
- [ ] Every activity mobilises at least one identified resource
- [ ] Every resource appears in a budget line or is declared as supplied
- [ ] Every objective has an indicator and a verification source
- [ ] Every deliverable is dated in the schedule
- [ ] Every significant risk has a measure and an owner
- [ ] The purpose covers the full set of specific objectives

### 1.2 Eight-pitfall test

The eight most frequent defects of real TDRs, turned into applicable tests:

| # | Pitfall | Test |
|---|---------|------|
| 1 | Lack of clarity or precision | Does each objective carry at least three of the six elements what/who/why/where/how/when? Is every quantity numbered? |
| 2 | Errors and misstatements | Spelling and semantic review; check in particular for inversions between purpose and objectives, causes and consequences, deliverables and added value |
| 3 | Inconsistency between elements | Has the orphan test (1.1) passed in full? Is the budget consistent with duration and headcount? |
| 4 | Unrealistic objectives or requirements | Is the duration derived from the schedule compatible with the resources allocated? Can a provider on this market actually meet the requirements? |
| 5 | Stakeholders not involved | Do the real needs of end users appear, or only those of the commissioning party? Did the target-groups section produce methodological consequences? |
| 6 | Insufficient time or resources to prepare | Are to-be-completed zones left on structural elements? Are they listed for the user? |
| 7 | Technical / functional requirements confused | Does a requirement describe a use need or impose a solution? Any unjustified technical specification must be restated as functional |
| 8 | Vague constraints | Does the scope state its exclusions? Are start and end conditions set? Are the commissioning party's obligations written down? |

### 1.3 Type conformity test

Are all the sections specific to this document type present (see `document-types.md`)? Is the register
right — persuasive for a proposal or a project dossier, neutral for a TDR, retrospective for a
report? Is the issuer's perspective held from start to finish?

### 1.4 Closing summary

After correction, report in a few lines: corrections made, remaining to-be-completed zones ranked by
criticality, points requiring a decision from the user, and — where applicable — the tensions found
between constraints (imposed duration vs resources, budget vs scope).

---

## PART 2 — COUNTER-EXPERTISE MODE

Audit protocol for an existing document submitted by the user. Do not rewrite spontaneously:
diagnose first, offer the rewrite afterwards.

### 2.1 Scoring grid — 100 points

#### D1 — Section completeness (0–20)

| Score | Criterion |
|-------|-----------|
| 17–20 | Every section expected for this type and level is present and substantive |
| 11–16 | One or two recommended sections missing, with no structural consequence |
| 6–10 | A mandatory section is missing (scope, deliverables, resources, cost…) |
| 0–5 | Several mandatory sections missing — the document is not usable as it stands |

#### D2 — Coherence chain (0–25)

| Score | Criterion |
|-------|-----------|
| 21–25 | No orphans: purpose, objectives, activities, deliverables, resources, cost and indicators connect without a break |
| 14–20 | One or two minor orphans |
| 7–13 | Clear break between two links (e.g. activities without resources, deliverables absent from the schedule) |
| 0–6 | Sections juxtaposed with no demonstrable link |

#### D3 — MPR realism (0–20)

| Score | Criterion |
|-------|-----------|
| 17–20 | Duration and cost are visibly derived from the methodology and resources |
| 11–16 | Partial derivation, some lines not traceable |
| 6–10 | Budget and deadline set a priori, methodology built afterwards |
| 0–5 | No demonstrable relationship between method, resources, deadline and cost |

#### D4 — Risk treatment (0–15)

| Score | Criterion |
|-------|-----------|
| 13–15 | Internal risks analysed per task with measures; external risks distinguished and treated |
| 9–12 | Risks listed with measures, but not broken down by activity |
| 5–8 | Generic risk list with no measures |
| 0–4 | No risk section, or internal and external risks conflated |

#### D5 — Precision of requirements and scope (0–10)

| Score | Criterion |
|-------|-----------|
| 9–10 | Scope bounded with exclusions, requirements verifiable, reference framework cited and located |
| 6–8 | Scope clear but requirements partly subjective |
| 3–5 | Scope vague, requirements not testable |
| 0–2 | Neither scope nor requirements identifiable |

#### D6 — Drafting quality and defensibility (0–10)

| Score | Criterion |
|-------|-----------|
| 9–10 | Neutral, quantified language, readable structure, document defensible as is before a committee |
| 6–8 | Readable but with subjective phrasing or redundancy |
| 3–5 | Frequent ambiguities, undefined jargon, errors of meaning |
| 0–2 | Barely comprehensible without its author |

### 2.2 Interpretation

| Score | Verdict | Recommended action |
|-------|---------|--------------------|
| 85–100 | ✅ Solid | Cosmetic adjustments only |
| 70–84 | ✅ Acceptable | Fix the flagged points before transmission |
| 55–69 | ⚠️ Fragile | Deficient sections must be redone |
| 40–54 | ⚠️ Insufficient | Structured rewrite from the architecture stage (Stage 3) |
| 0–39 | ❌ Not usable | Restart from scoping (Stage 1) |

### 2.3 Report format

Deliver the report in the user's language, using the same headings as the rest of the document set.

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
COUNTER-EXPERTISE REPORT — [Document title]
Type identified: [type]        Level: [L0–L3]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

D1 — Section completeness            : XX/20
D2 — Coherence chain                 : XX/25
D3 — MPR realism                     : XX/20
D4 — Risk treatment                  : XX/15
D5 — Requirements and scope precision : XX/10
D6 — Drafting quality                : XX/10
                                       ──────
TOTAL SCORE                           : XX/100
VERDICT: [Solid / Acceptable / Fragile / Insufficient / Not usable]

STRENGTHS
  • [precise observation, with the section it refers to]

COHERENCE BREAKS DETECTED
  • [orphan found → concrete consequence at execution]

MISSING OR DEFICIENT SECTIONS
  • [section → what must go in it]

PROPOSED REWORDINGS
  • [current wording] → [proposed wording]

MAIN RISK IF THE DOCUMENT GOES OUT AS IT STANDS
  • [one sentence, the most likely consequence]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

Close by asking the user whether to rework the document on this basis — and if yes, resume the
pipeline at Stage 3.

### 2.4 Audit posture

Be critical and precise, never complacent: a document wrongly approved costs more than one that is
sent back. But always tie each criticism to a concrete execution consequence rather than to a matter
of taste — that is what makes the audit acceptable to its recipient.
