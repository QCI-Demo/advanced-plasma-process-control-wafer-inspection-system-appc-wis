# Customer Support Portal — Initiation Record

| Field | Value |
|-------|-------|
| **Document ID** | `CSP-IR-001` |
| **Title** | Customer Support Portal — Initiation Record |
| **Document type** | Controlled initiation record |
| **Document owner** | Project Manager (designate) — human owner confirmation required |
| **Version** | `0.1.0` |
| **Status** | Draft — Pending Human Review |
| **Review date** | 2026-10-05 |
| **Effective date** | Pending human approval |
| **Classification** | Internal — Controlled Document |
| **Template reference** | `TMPL-INIT-REC-001` @ `1.0.0` |
| **Schema** | `docs/schemas/initiation-record.schema.json` |
| **Machine-readable companion** | `CSP-IR-001-customer-support-portal-initiation-record-v0.1.0.json` |

> **Governance notice:** This record is an asynchronous, AI-prepared **traceable input** to the charter and governance baseline. It does **not** substitute for stakeholder decisions. Live workshops, interviews, and approvals are **human-only** and must be completed by designated business stakeholders outside this AI-assigned work.

---

## 1. Document control

### 1.1 Approval evidence

| Approver role | Approver name | Decision | Date | Evidence reference |
|---------------|---------------|----------|------|--------------------|
| Executive sponsor | _Designate — human confirmation required_ | Pending | — | Pending written approval |
| Product Owner / Support SME | _Designate — human confirmation required_ | Pending | — | Pending written approval |
| Project Manager | _Designate — human confirmation required_ | Pending | — | Pending written approval |
| Availability-critical reviewer | Chloe Zhang | Pending | — | Formal baseline review scheduled during October availability |

**Approval notes:**  
No baseline is in force until written human approval evidence is recorded. Chloe Zhang’s limited early availability requires asynchronous preparation and staged reviews, with formal baseline approval scheduled during her October availability.

**Evidence links:**  
- _To be added:_ review-meeting minutes, signed approval form, or controlled email approval artefact IDs

### 1.2 Change history

| Version | Date | Author | Summary of change |
|---------|------|--------|-------------------|
| 0.1.0 | 2026-08-17 | AI Employee (asynchronous preparation) | Initial draft from TMPL-INIT-REC-001 v1.0.0 capturing proposed MVP boundary, stakeholders, assumptions, constraints, dependencies, deferred integrations, and unresolved decisions |

---

## 2. Project identity

| Field | Value |
|-------|-------|
| Project name | Customer Support Portal Implementation |
| Epic | Project Initiation, Governance, and Delivery Baseline |
| Related story | Document MVP boundaries, stakeholders, and initiation decisions |
| Proposed schedule start | 2026-10-05 |
| Proposed schedule end | 2027-03-26 |
| Schedule notes | Approximately 24 weeks; subject to formal confirmation during initiation |

### 2.1 Project purpose (context)

Deliver a secure, centralized, user-friendly customer support portal that replaces fragmented support interactions across email, phone, spreadsheets, and disconnected tools, becoming the governed system of record for customer support requests.

---

## 3. Objectives

| ID | Objective statement | Success measure |
|----|---------------------|-----------------|
| OBJ-001 | Establish a controlled asynchronous initiation baseline for MVP scope, stakeholders, decision owners, assumptions, constraints, and dependencies | CSP-IR-001 reviewed by designated humans and linked from the charter |
| OBJ-002 | Provide customers a consistent digital channel to submit, track, and communicate on support requests | MVP capabilities in §5 accepted into the charter baseline |
| OBJ-003 | Provide support operations with structured workflows, RBAC, workload visibility, and service-performance reporting foundations | Reporting/dashboard MVP scope accepted; deferred analytics remain out of scope pending change control |
| OBJ-004 | Preserve clear change-control boundaries for deferred integrations | CRM, monitoring, survey, SLA-automation, and additional channels explicitly excluded unless approved via CSP-REG-CHG-001 |

---

## 4. Scope — proposed MVP boundary

**MVP boundary summary:**  
The initial release delivers customer request management, ticket workflow management, role-based access control, ticket communication, email and/or in-app notifications, searchable knowledge resources, and operational reporting/dashboards. Integrations and automations listed in §5 remain **out of MVP** unless separately approved through change control.

### 4.1 In-scope capabilities

| ID | Capability | Notes |
|----|------------|-------|
| SCP-001 | Customer request management | Request creation, attachment upload, request history, status tracking, and reopening where permitted |
| SCP-002 | Ticket workflow management | Categorization, prioritization, assignment, status transitions, escalation handling, resolution, closure, and audit history |
| SCP-003 | Role-based access control | Access for customers, support agents, team leads, and administrators |
| SCP-004 | Ticket communication | Customer–agent comments/updates with an auditable conversation record |
| SCP-005 | Notifications | Email and/or in-app notifications for material events (creation, assignment, comments, status changes, resolution, closure) |
| SCP-006 | Knowledge resources | Searchable help articles, FAQs, and guidance for customer self-service |
| SCP-007 | Reporting and dashboards | Ticket volume, backlog, workload, priorities, resolution performance, and service-level trends |

### 4.2 Core workstreams (delivery context)

| Workstream | Ownership (named groups) |
|------------|--------------------------|
| Portal development | Technical Lead; Full-Stack Developers |
| User and access management | Technical Lead; Full-Stack Developers; DevOps/Security Engineer |
| Ticket management and workflows | Business Analyst/Support SME; UX Designer; Development team |
| Notifications and integrations | Full-Stack Developers; DevOps/Security Engineer |
| Reporting and dashboards | Business Analyst/Support SME; Full-Stack Developers |
| Quality assurance and release readiness | QA Engineers; Product Owner/Support SME; Project Manager; business approvers |

---

## 5. Exclusions — deferred unless change-controlled

| ID | Excluded item | Rationale | Re-entry control |
|----|---------------|-----------|------------------|
| EXC-001 | CRM integration | Future-phase capability; not required to establish portal system of record for MVP | Approved CR in `CSP-REG-CHG-001` before scope inclusion |
| EXC-002 | Monitoring-system integration | Future-phase operational integration; deferred from MVP | Approved CR in `CSP-REG-CHG-001` |
| EXC-003 | Customer satisfaction survey integration | Future-phase feedback mechanism; deferred from MVP | Approved CR in `CSP-REG-CHG-001` |
| EXC-004 | SLA automation | Future-phase automation beyond reporting trends; deferred from MVP | Approved CR in `CSP-REG-CHG-001` |
| EXC-005 | Additional support-channel integrations | MVP focuses on the portal channel; other channels deferred | Approved CR in `CSP-REG-CHG-001` |
| EXC-006 | Identity-provider integration beyond MVP RBAC needs | May be introduced in future phases; confirm during human design reviews | Approved CR in `CSP-REG-CHG-001` if beyond MVP access model |
| EXC-007 | Enhanced analytics beyond MVP dashboards | Continuous-improvement vision; not MVP | Approved CR in `CSP-REG-CHG-001` |
| EXC-008 | Knowledge-base governance improvements beyond searchable articles/FAQs | Future-phase governance maturity | Approved CR in `CSP-REG-CHG-001` |

---

## 6. Assumptions

| ID | Assumption | Owner | Impact if false | Validation method |
|----|------------|-------|-----------------|-------------------|
| ASM-001 | Designated business stakeholders will complete workshops, interviews, and written approvals outside AI preparation | Executive sponsor / Project Manager | Baseline cannot be approved; charter remains blocked | Human confirmation during staged October reviews |
| ASM-002 | Chloe Zhang can participate in formal baseline approval during October 2026 availability | Chloe Zhang / Project Manager | Approval window slips; schedule re-baseline required | Calendar confirmation by Project Manager |
| ASM-003 | MVP can deliver value without CRM, monitoring, survey, SLA-automation, or additional-channel integrations | Product Owner / Support SME | Scope pressure; requires change requests or re-prioritization | Human scope workshop |
| ASM-004 | Email and/or in-app channels are sufficient for MVP notifications | Technical Lead / Product Owner | Notification design rework; possible external dependency | Design review |
| ASM-005 | Existing support operating model can adopt portal workflows with training during UAT/release prep | Business Analyst/Support SME | Adoption risk; extended hypercare or process redesign | SME interview / UAT planning |
| ASM-006 | Repository will retain requirements, decisions, risks, test evidence, and approved changes as the audit trail | Project Manager | Governance gaps; auditability weakened | PMO process confirmation |

---

## 7. Constraints

| ID | Constraint | Type | Owner |
|----|------------|------|-------|
| CON-001 | Chloe Zhang has limited early availability; initiation must be asynchronous with staged reviews | Resource | Project Manager |
| CON-002 | Formal baseline approval targeted to October 2026 availability window | Schedule | Executive sponsor |
| CON-003 | Practical baseline schedule target is 2026-10-05 through 2027-03-26 (~24 weeks), pending confirmation | Schedule | Project Manager |
| CON-004 | Deferred integrations must not be implemented as silent scope creep | Operational | Product Owner / Project Manager |
| CON-005 | Delivery must retain governed artefacts in the project repository | Regulatory | PMO / Project Manager |
| CON-006 | Solution must support secure, role-based access and auditable ticket lifecycle | Technical | Technical Lead / DevOps/Security Engineer |

---

## 8. Stakeholders

| ID | Stakeholder group | Named individuals (if known) | Interest | Decision authority | Engagement mode |
|----|-------------------|------------------------------|----------|--------------------|-----------------|
| STK-001 | Executive sponsor | _Designate_ | Strategic outcomes, funding, baseline approval | Approve/reject initiation baseline and major scope changes | Staged review; formal October approval |
| STK-002 | Product Owner / Support SME | _Designate_ | MVP boundary, workflow fitness, acceptance | Own product scope decisions; contribute to baseline | Asynchronous review + workshops |
| STK-003 | Availability-critical business stakeholder | Chloe Zhang | Timing of formal baseline approval | Participate in/confirm October approval window | Asynchronous prep now; formal review in October |
| STK-004 | Project Manager / PMO | _Designate_ | Schedule, registers, change control, traceability | Maintain controlled documents; escalate unresolved decisions | Asynchronous preparation and cadence |
| STK-005 | Technical Lead & Full-Stack Developers | _Team designate_ | Feasibility of MVP scope and architecture | Technical recommendations; not sole business approvers | Design reviews |
| STK-006 | DevOps / Security Engineer | _Designate_ | Access, notifications infrastructure, security posture | Security/ops constraints on scope | Technical review |
| STK-007 | Business Analyst / Support SME | _Designate_ | Process mapping, reporting needs | Requirements clarity inputs | Interviews/workshops (human-only) |
| STK-008 | UX Designer | _Designate_ | Usability of portal journeys | Design recommendations | Design reviews |
| STK-009 | QA Engineers | _Team designate_ | Testability, quality gates, release readiness | Quality gate evidence | Test planning after baseline |
| STK-010 | Support agents, team leads, administrators (operational users) | _Represented via SME_ | Day-to-day workflow fitness | Feedback; not initiation approvers | Later UAT (human-only) |
| STK-011 | Customers (end users of portal) | _Represented via Product Owner_ | Request submission, tracking, communication experience | Feedback via PO; not initiation approvers | Later UAT / research (human-only) |

---

## 9. Dependencies

| ID | Dependency | Type | Owner | Needed by | Status |
|----|------------|------|-------|-----------|--------|
| DEP-001 | Human workshops/interviews to validate MVP boundary and assumptions | Organizational | Product Owner / Project Manager | Before baseline approval (Oct 2026) | Identified |
| DEP-002 | Written approval from designated approvers including Chloe Zhang’s October participation | Organizational | Executive sponsor / Project Manager | 2026-10 baseline window | Identified |
| DEP-003 | Confirmation of notification approach (email and/or in-app) and related platform prerequisites | Technical | Technical Lead | Design phase | Identified |
| DEP-004 | Access to controlled documentation database and register maintenance process | Organizational | PMO / Project Manager | Immediate | Confirmed (this repository) |
| DEP-005 | Downstream charter and governance baseline artefacts consuming this record | Internal | Project Manager | After IR review | Identified |
| DEP-006 | External CRM / monitoring / survey / SLA / additional-channel systems | External | Product Owner | Future phases only | Deferred |
| DEP-007 | Security/compliance review of RBAC and audit history approach | Organizational | DevOps/Security Engineer | Before UAT/release approval | Identified |

---

## 10. Decisions

### 10.1 Recorded / proposed initiation decisions

| ID | Question | Proposed position | Decision owner | Status | Decision register ref |
|----|----------|-------------------|----------------|--------|-----------------------|
| DEC-001 | What is the proposed MVP boundary? | Capabilities SCP-001–SCP-007 in §4; exclusions EXC-001–EXC-008 in §5 | Product Owner / Support SME + Executive sponsor | Proposed | `CSP-REG-DEC-001` / DEC-001 |
| DEC-002 | Which integrations are deferred from MVP? | CRM, monitoring-system, survey, SLA-automation, and additional-channel integrations are deferred unless approved via change control | Product Owner + Project Manager | Proposed | `CSP-REG-DEC-001` / DEC-001 |
| DEC-003 | How are stakeholder groups and decision owners defined for initiation? | Stakeholder table §8; approvals per §1.1 | Executive sponsor | Proposed | `CSP-REG-DEC-001` / DEC-002 |
| DEC-004 | What is the practical delivery window to propose? | 2026-10-05 through 2027-03-26, subject to confirmation | Project Manager + Executive sponsor | Proposed | `CSP-REG-DEC-001` / UND-002 |

### 10.2 Unresolved decisions (require human owners)

| ID | Question | Decision owner | Needed by | Blocking impact | Decision register ref |
|----|----------|----------------|-----------|-----------------|-----------------------|
| UND-001 | Confirm formal baseline approval timing during Chloe Zhang’s October availability | Chloe Zhang / Executive sponsor | Oct 2026 | Blocks baseline status transition | `CSP-REG-DEC-001` / UND-001 |
| UND-002 | Confirm or revise the 24-week schedule window | Project Manager + Executive sponsor | Oct 2026 baseline review | Blocks charter schedule baseline | `CSP-REG-DEC-001` / UND-002 |
| UND-003 | Name permanent human document owner, Product Owner, and Executive sponsor on this record | Executive sponsor / PMO | Before Approved status | Blocks approval evidence completion | `CSP-REG-DEC-001` |
| UND-004 | Confirm whether identity-provider integration is required inside MVP RBAC or remains deferred | Technical Lead + Product Owner + Security | Design phase / baseline refinement | May alter SCP-003 / EXC-006 | `CSP-REG-DEC-001` |

---

## 11. Register references

| Register | Register ID | Path | Version | Notes |
|----------|-------------|------|---------|-------|
| Risk Register | `CSP-REG-RISK-001` | `docs/registers/CSP-REG-RISK-001-risk-register.md` | `0.1.0` | Placeholder; populate in human risk workshop |
| Issue Register | `CSP-REG-ISSUE-001` | `docs/registers/CSP-REG-ISSUE-001-issue-register.md` | `0.1.0` | Placeholder |
| Decision Register | `CSP-REG-DEC-001` | `docs/registers/CSP-REG-DEC-001-decision-register.md` | `0.1.0` | Seeded with DEC/UND refs from this record |
| Change Register | `CSP-REG-CHG-001` | `docs/registers/CSP-REG-CHG-001-change-register.md` | `0.1.0` | Gate for deferred integration re-entry |

---

## 12. Approval status summary

| Field | Value |
|-------|-------|
| Baseline ready? | **No** |
| Human approval required? | **Yes** |
| Scheduled approval window | October 2026 (aligned to Chloe Zhang’s availability) |
| Notes | Traceable input only. Not a substitute for stakeholder decisions. Workshops, interviews, and approvals remain human-only. |

---

## 13. Handoff to charter / governance baseline

Downstream artefacts should inherit, by reference to `CSP-IR-001` v0.1.0 (or later approved version):

1. MVP in-scope capabilities (SCP-001–SCP-007)
2. Explicit deferred integrations (EXC-001–EXC-005 especially)
3. Stakeholder groups and decision authorities
4. Assumptions, constraints, and dependencies
5. Open decisions UND-001–UND-004
6. Register link set in §11
