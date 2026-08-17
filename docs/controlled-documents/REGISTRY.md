# Controlled Document Registry

Master index for the documentation database. Update this registry whenever a controlled template or record is created, revised, superseded, or withdrawn.

## Templates

| Document ID | Title | Version | Status | Owner | Review Date | Path |
|-------------|-------|---------|--------|-------|-------------|------|
| TMPL-INIT-REC-001 | Initiation Record Template | 1.0.0 | Approved for use | Project Management Office (PMO) | 2027-01-17 | `templates/TMPL-INIT-REC-001-initiation-record-v1.0.0.md` |

## Issued records

| Document ID | Title | Template Ref | Version | Status | Owner | Review Date | Path |
|-------------|-------|--------------|---------|--------|-------|-------------|------|
| CSP-IR-001 | Customer Support Portal — Initiation Record | TMPL-INIT-REC-001 @ 1.0.0 | 0.1.0 | Draft — Pending Human Review | Project Manager (designate) | 2026-10-05 | `records/CSP-IR-001-customer-support-portal-initiation-record-v0.1.0.md` |

## Register artefacts

| Register ID | Title | Version | Status | Path |
|-------------|-------|---------|--------|------|
| CSP-REG-RISK-001 | Risk Register | 0.1.0 | Placeholder | `../registers/CSP-REG-RISK-001-risk-register.md` |
| CSP-REG-ISSUE-001 | Issue Register | 0.1.0 | Placeholder | `../registers/CSP-REG-ISSUE-001-issue-register.md` |
| CSP-REG-DEC-001 | Decision Register | 0.1.0 | Placeholder | `../registers/CSP-REG-DEC-001-decision-register.md` |
| CSP-REG-CHG-001 | Change Register | 0.1.0 | Placeholder | `../registers/CSP-REG-CHG-001-change-register.md` |

## Status vocabulary (controlled)

| Status | Meaning |
|--------|---------|
| Draft — AI Prepared | Asynchronous draft prepared for human review; not an approved baseline |
| Draft — Pending Human Review | Circulated for stakeholder review; no formal approval yet |
| In Review | Formal review cycle underway |
| Approved | Human owner has recorded approval evidence |
| Baseline | Approved and frozen as a governance baseline |
| Superseded | Replaced by a later controlled version |
| Withdrawn | No longer valid for use |
| Approved for use | Template authorised for creating new controlled records |
| Placeholder | Register shell awaiting population |

## Change control note

Any change that expands MVP scope to include deferred integrations (CRM, monitoring-system, survey, SLA-automation, additional channels) requires an approved change request recorded in `CSP-REG-CHG-001` before the initiation record or charter baseline may be updated.
