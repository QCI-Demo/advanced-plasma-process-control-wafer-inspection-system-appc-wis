# Initiation Record Template

| Field | Value |
|-------|-------|
| **Document ID** | `TMPL-INIT-REC-001` |
| **Title** | Initiation Record Template |
| **Document type** | Controlled reusable template |
| **Document owner** | Project Management Office (PMO) |
| **Version** | `1.0.0` |
| **Status** | Approved for use |
| **Review date** | 2027-01-17 |
| **Classification** | Internal — Controlled Document |
| **Schema** | `docs/schemas/initiation-record.schema.json` |
| **Machine-readable blank** | `TMPL-INIT-REC-001-initiation-record-v1.0.0.json` |

---

## 1. Purpose

This template establishes a **versioned, reusable initiation-record structure** so later artefacts (charter, governance baseline, WBS, registers, release model) can inherit consistent metadata, scope boundaries, stakeholder fields, assumptions, dependencies, decision references, and approval status.

An initiation record prepared from this template is a **traceable input** to the charter and governance baseline. It does **not** substitute for stakeholder decisions. Live workshops, interviews, and approvals are **human-only** activities and must be completed by designated business stakeholders.

---

## 2. Document control (mandatory)

Complete all fields before circulating a record for review.

| Field | Instructions | Value (fill when issuing a record) |
|-------|--------------|------------------------------------|
| Document ID | Project-prefixed controlled ID (e.g. `CSP-IR-001`) | |
| Title | Clear record title including project name | |
| Document owner | Named human owner (role + name) | |
| Version | Semantic version `MAJOR.MINOR.PATCH` | |
| Status | Use controlled vocabulary from the registry | |
| Review date | Next mandatory human review date (ISO date) | |
| Effective date | Date the approved version becomes effective (or `Pending`) | |
| Classification | e.g. Internal — Controlled Document | |
| Template reference | This template ID + version used to create the record | `TMPL-INIT-REC-001` / `1.0.0` |

### 2.1 Approval evidence (mandatory)

| Approver role | Approver name | Decision | Date | Evidence reference |
|---------------|---------------|----------|------|--------------------|
| Executive sponsor | | Pending / Approved / Rejected / Deferred | | Link or artefact ID |
| Product Owner / Business owner | | Pending / Approved / Rejected / Deferred | | |
| Project Manager | | Pending / Approved / Rejected / Deferred | | |

**Approval notes:**  
_State that AI-prepared content is not approval. Record how/where written human approval will be captured._

**Evidence links:**  
- _Meeting minutes / signed form / email approval artefact IDs_

### 2.2 Change history (mandatory)

| Version | Date | Author | Summary of change |
|---------|------|--------|-------------------|
| 0.1.0 | YYYY-MM-DD | | Initial draft from template |

---

## 3. Project identity

| Field | Value |
|-------|-------|
| Project name | |
| Epic / programme workstream | |
| Related story / request | |
| Proposed schedule start | |
| Proposed schedule end | |
| Schedule confirmation notes | Subject to formal confirmation during initiation |

---

## 4. Objectives (structured)

| ID | Objective statement | Success measure |
|----|---------------------|-----------------|
| OBJ-001 | | |

---

## 5. Scope (structured)

**MVP boundary summary:**  
_One paragraph describing what the initial release will and will not deliver._

### 5.1 In-scope capabilities

| ID | Capability | Notes |
|----|------------|-------|
| SCP-001 | | |

---

## 6. Exclusions / out-of-scope (structured)

Items listed here remain **deferred** unless separately approved through change control.

| ID | Excluded item | Rationale | Re-entry control |
|----|---------------|-----------|------------------|
| EXC-001 | | | Requires approved CR in Change Register |

---

## 7. Assumptions (structured)

| ID | Assumption | Owner | Impact if false | Validation method |
|----|------------|-------|-----------------|-------------------|
| ASM-001 | | | | Human workshop / interview / written confirmation |

---

## 8. Constraints (structured)

| ID | Constraint | Type | Owner |
|----|------------|------|-------|
| CON-001 | | Schedule / Resource / Technical / Regulatory / Financial / Operational / Other | |

---

## 9. Stakeholders (structured)

| ID | Stakeholder group | Named individuals (if known) | Interest | Decision authority | Engagement mode |
|----|-------------------|------------------------------|----------|--------------------|-----------------|
| STK-001 | | | | | Asynchronous review / staged workshop / formal approval |

---

## 10. Dependencies (structured)

| ID | Dependency | Type | Owner | Needed by | Status |
|----|------------|------|-------|-----------|--------|
| DEP-001 | | Internal / External / Technical / Organizational | | | Identified / Confirmed / At Risk / Resolved / Deferred |

---

## 11. Decisions (structured)

### 11.1 Recorded / proposed initiation decisions

| ID | Question | Proposed position | Decision owner | Status | Decision register ref |
|----|----------|-------------------|----------------|--------|-----------------------|
| DEC-001 | | | | Proposed / Accepted / Rejected / Superseded | |

### 11.2 Unresolved decisions

| ID | Question | Decision owner | Needed by | Blocking impact | Decision register ref |
|----|----------|----------------|-----------|-----------------|-----------------------|
| UND-001 | | | | | |

---

## 12. Register references (mandatory links)

Every initiation record must link the four governance registers, even if they are placeholders.

| Register | Register ID | Path | Version | Notes |
|----------|-------------|------|---------|-------|
| Risk Register | | `docs/registers/...` | | |
| Issue Register | | `docs/registers/...` | | |
| Decision Register | | `docs/registers/...` | | |
| Change Register | | `docs/registers/...` | | |

---

## 13. Approval status summary

| Field | Value |
|-------|-------|
| Baseline ready? | Yes / No |
| Human approval required? | **Yes** (always for baseline) |
| Scheduled approval window | |
| Notes | This record is a traceable input only; it does not constitute stakeholder approval. |

---

## 14. Issuance instructions (for authors)

1. Copy this template markdown **and** the companion JSON blank into `docs/controlled-documents/records/`.
2. Assign a new controlled document ID; do not reuse IDs.
3. Set status to `Draft — AI Prepared` or `Draft — Pending Human Review` until humans approve.
4. Populate all mandatory structured sections; leave unresolved items explicit rather than inventing decisions.
5. Link the four registers and cite this template ID/version in document control.
6. Update `docs/controlled-documents/REGISTRY.md`.
7. Route to designated human stakeholders for workshops, interviews, and written approval evidence.
8. Only after recorded human approval may status become `Approved` or `Baseline`.

---

## Template change history

| Version | Date | Author | Summary |
|---------|------|--------|---------|
| 1.0.0 | 2026-08-17 | AI Employee (asynchronous preparation) | Initial controlled initiation-record template with mandatory metadata, structured initiation fields, and register reference links |
