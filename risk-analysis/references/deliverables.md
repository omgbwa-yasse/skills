# Deliverables: register schema, report structure, default scales

Read before producing a register or a report.

Contents: [Risk register schema](#risk-register-schema) · [Register in xlsx](#producing-the-register-as-xlsx) · [Report structure](#report-structure) · [Default scales](#default-scales) · [Worked risk entry](#worked-risk-entry)

---

## Risk register schema

The register is the core artefact. Columns below are the full set; drop what the mode does not warrant, but never drop the control effectiveness, assumption, or owner columns — those are what separate a register from a list.

| Column | Contents |
|---|---|
| ID | Stable identifier, e.g. `R-01`. Never renumber; retired risks keep their ID. |
| Category | From the context, e.g. operational, financial, regulatory, safety, security, environmental, strategic. |
| Risk statement | **Cause → event → consequence on a named objective.** One sentence, specific. |
| Objective affected | Which stated objective this threatens. |
| Identified by | Technique and/or source. |
| Existing controls | Named, concrete. "Controls in place" is not an entry. |
| Control effectiveness | Effective / Partially effective / Ineffective / Unknown — plus the basis for the judgement. |
| Inherent consequence | Rating without controls, per the consequence scale. |
| Inherent likelihood | Rating without controls, per the likelihood scale. |
| Inherent risk level | From the matrix or formula. |
| Residual consequence | Rating with controls working as described. |
| Residual likelihood | Rating with controls working as described. |
| Residual risk level | From the matrix or formula. |
| Likelihood basis | Historical data / predictive model / expert judgement — and the source. |
| Confidence | High / Medium / Low, on the rating as a whole. |
| Evaluation | Against the criteria: accept / treat / analyse further / escalate / reconsider activity. |
| Treatment option | Avoid / remove source / change likelihood / change consequence / share / retain. |
| Treatment actions | Specific actions, not intentions. |
| Owner | Named role or person. |
| Due date | |
| Target residual level | What the treatment is expected to achieve. |
| Secondary risks | New risks the treatment introduces. |
| Indicator (KRI) | Measurable signal with a threshold that triggers action. |
| Review trigger | Events mandating reassessment. |
| Review date / next review | |
| Assumptions | What this rating depends on being true. |

For Rapid mode, a workable reduction: ID, risk statement, existing controls, control effectiveness, residual consequence, residual likelihood, residual level, evaluation, treatment, owner, assumptions.

---

## Producing the register as xlsx

Read the `xlsx` skill first. Then:

- Sheet 1 **Context & criteria** — scope, objectives, exclusions, the consequence scale, the likelihood scale, the matrix, and the tolerance thresholds. The register is uninterpretable without this sheet; it goes first, not in an appendix.
- Sheet 2 **Risk register** — one row per risk, frozen header, filters on, columns sized to be readable.
- Sheet 3 **Treatment plan** — actions, owners, dates, status. Sortable by owner and by date, since this is the sheet people actually work from.
- Sheet 4 **Assumptions & limitations**.
- Optional Sheet 5 **Heat map** — count of risks per matrix cell.

Use data validation dropdowns on the rating columns so the register stays consistent as it is maintained. Conditional formatting on risk level, but keep it legible in monochrome — colour alone must not carry the meaning.

---

## Report structure

For a `.docx` or `.md` assessment report:

```
1. Executive summary
   — what was assessed, the headline findings, the top risks, and what is being asked of the reader
2. Scope and objectives
   — what is in scope, what is explicitly excluded, and the decision this supports
3. Context
   — external, internal, and process context; stakeholders consulted
4. Risk criteria
   — consequence scales, likelihood scales, level-of-risk method, tolerance thresholds, and their source
5. Method
   — techniques used and why; who participated; data sources
6. Risk identification
   — how identification was carried out and what it covered
7. Risk analysis
   — controls assessment, consequence and likelihood analysis, levels of risk; the register (or a pointer to it)
8. Risk evaluation
   — comparison against criteria; which risks require treatment; risks near the threshold
9. Risk treatment
   — treatment plan with options, owners, dates, residual risk, and secondary risks
10. Monitoring and review
   — indicators, triggers, cadence, and responsibilities
11. Assumptions, limitations, and uncertainty
   — what this assessment does not cover and where its conclusions are fragile
Appendices — register, technique working papers, scales
```

Section 11 is the one that gets cut under time pressure and the one most worth keeping. An assessment that names its own weak points can be relied on; one that does not, cannot.

Keep the executive summary to one page and free of jargon. The reader who only reads that page should come away with the right picture.

---

## Default scales

Use these only when the user has none and cannot supply them, and label them clearly as proposed defaults to be adapted. Anchors must be rewritten to the user's context — the bands below are placeholders, not recommendations.

**Consequence (5 levels).** Define each level across the consequence categories in play. Illustrative structure:

| Level | Financial | Operational | Regulatory / legal | Reputational |
|---|---|---|---|---|
| 1 Insignificant | Absorbed in normal budget | Negligible disruption, no customer impact | Minor internal non-conformance | No external awareness |
| 2 Minor | Small unbudgeted cost | Short disruption, limited customer impact | Reportable, no penalty | Local or short-lived comment |
| 3 Moderate | Material unbudgeted cost | Significant disruption to a service | Formal finding, remediation required | Sustained negative coverage in the sector |
| 4 Major | Substantial loss requiring reallocation | Extended outage of a critical service | Enforcement action, penalty | National coverage; client or partner loss |
| 5 Catastrophic | Threatens financial viability | Loss of core capability | Loss of licence or authorisation to operate | Lasting damage to standing |

For safety, health, or environmental categories, define levels against harm, not money.

**Likelihood (5 levels), over a stated period — default 12 months:**

| Level | Descriptor | Indicative frequency |
|---|---|---|
| 1 | Rare | Not expected within 10 years |
| 2 | Unlikely | Expected within 5–10 years |
| 3 | Possible | Expected within 2–5 years |
| 4 | Likely | Expected within 1–2 years |
| 5 | Almost certain | Expected at least annually |

**Level of risk.** Design the matrix deliberately rather than by multiplication, and weight consequence more heavily at the top end. A defensible 5×5 assignment:

| | L1 Rare | L2 Unlikely | L3 Possible | L4 Likely | L5 Almost certain |
|---|---|---|---|---|---|
| **C5 Catastrophic** | High | High | Extreme | Extreme | Extreme |
| **C4 Major** | Medium | High | High | Extreme | Extreme |
| **C3 Moderate** | Low | Medium | Medium | High | High |
| **C2 Minor** | Low | Low | Low | Medium | Medium |
| **C1 Insignificant** | Low | Low | Low | Low | Medium |

**Response bands:**

| Level | Requirement |
|---|---|
| Extreme | Immediate action; escalate to senior accountable owner; treatment plan before proceeding |
| High | Treatment required with named owner and date; management attention |
| Medium | Treat where cost-effective; monitor against indicators; periodic review |
| Low | Accept and monitor; no treatment required beyond maintaining existing controls |

**Control effectiveness:**

| Rating | Meaning |
|---|---|
| Effective | Designed appropriately, operating as intended, and demonstrable with evidence |
| Partially effective | Designed appropriately but with gaps in operation or coverage, or evidence incomplete |
| Ineffective | Not designed for the risk, not operating, or demonstrably failing |
| Unknown | Not tested or evidenced — treat as a finding in its own right, not as a neutral rating |

---

## Worked risk entry

The standard to write to:

> **R-07 · Operational / Security**
>
> **Risk:** The single unreplicated primary database host (cause) suffers a hardware or storage failure during a period of high load (event), making the customer portal unavailable for an estimated 8–24 hours and breaching the contractual 99.5% monthly availability commitment for approximately 40 enterprise clients (consequence — affects the service continuity and contractual compliance objectives).
>
> **Existing controls:** Nightly full backup to off-site object storage, retained 30 days. Host-level monitoring with paging alerts. Vendor hardware support contract, next-business-day response.
>
> **Control effectiveness:** *Partially effective.* Backups exist and are monitored for completion, but restoration has not been tested end to end within the last 18 months, so the 8–24 hour recovery estimate is an assumption rather than a measured figure. Next-business-day vendor response does not meet the availability commitment on its own.
>
> **Inherent:** C4 Major × L4 Likely = **Extreme**. **Residual:** C4 Major × L3 Possible = **High**.
>
> **Likelihood basis:** Expert judgement informed by three storage-related incidents across the estate in the past four years. Confidence: Medium.
>
> **Evaluation:** Above the tolerance threshold for the service continuity category (threshold: Medium). Treatment required.
>
> **Treatment:** *Change the consequence* — implement streaming replication to a warm standby with automated failover, and establish quarterly restoration testing with a documented recovery time. **Owner:** Head of Infrastructure. **Due:** 30 November. **Target residual:** C3 × L3 = Medium.
>
> **Secondary risks:** Automated failover introduces the possibility of split-brain and of spurious failover during transient network faults; both need explicit configuration and testing before the mechanism is trusted (raised as R-19).
>
> **Indicator:** Replication lag exceeding 60 seconds sustained for 5 minutes; storage SMART error count trend. **Review trigger:** any storage incident, or a change in the availability commitment. **Next review:** February.
>
> **Assumptions:** Client contracts carry service credits but no termination right at this availability level — to be confirmed with Legal; if termination rights exist, the consequence rating rises to C5.
