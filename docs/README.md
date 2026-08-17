# Documentation Database

Controlled documentation store for the **Customer Support Portal Implementation** programme.

This database provides a versioned, auditable home for initiation, governance, and delivery-baseline artefacts. Later artefacts (charter, WBS, backlog approach, quality gates, release governance) must reference controlled document IDs and versions from this store.

## Structure

| Path | Purpose |
|------|---------|
| `controlled-documents/REGISTRY.md` | Master index of controlled documents (templates and records) |
| `controlled-documents/templates/` | Reusable controlled-document templates |
| `controlled-documents/records/` | Issued controlled documents (project-specific instances) |
| `registers/` | Risk, issue, decision, and change registers |
| `schemas/` | Machine-readable schemas for structured controlled fields |

## Traceability rules

1. Every controlled document must carry: document ID, title, owner, version, status, review date, approval evidence, and change history.
2. Project records must be created from an approved template version and must cite that template ID/version.
3. Scope, stakeholder, assumption, dependency, and decision fields must remain structured so charter and governance artefacts can inherit them consistently.
4. Register references (risk, issue, decision, change) are mandatory link fields even when registers are still empty placeholders.
5. Human workshops, interviews, and formal approvals remain human-only activities outside AI-prepared drafts.

## Current controlled templates

| Document ID | Title | Version | Status |
|-------------|-------|---------|--------|
| `TMPL-INIT-REC-001` | Initiation Record Template | `1.0.0` | Approved for use |
