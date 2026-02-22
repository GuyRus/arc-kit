# Australian Government Secure by Design Assessment

> **Template Status**: Beta | **Version**: [VERSION] | **Command**: `/arckit.secure`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-[PROJECT_ID]-SECD-v[VERSION] |
| **Document Type** | Secure by Design Assessment |
| **Project** | [PROJECT_NAME] (Project [PROJECT_ID]) |
| **Classification** | [PUBLIC / OFFICIAL / OFFICIAL:Sensitive / PROTECTED / SECRET / TOP SECRET] |
| **Status** | [DRAFT / IN_REVIEW / APPROVED / PUBLISHED / SUPERSEDED / ARCHIVED] |
| **Version** | [VERSION] |
| **Created Date** | [YYYY-MM-DD] |
| **Last Modified** | [YYYY-MM-DD] |
| **Review Cycle** | [Monthly / Quarterly / Annual / On-Demand] |
| **Next Review Date** | [YYYY-MM-DD] |
| **Owner** | [OWNER_NAME_AND_ROLE] |
| **Reviewed By** | [REVIEWER_NAME] on [YYYY-MM-DD] or [PENDING] |
| **Approved By** | [APPROVER_NAME] on [YYYY-MM-DD] or [PENDING] |
| **Distribution** | [DISTRIBUTION_LIST] |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| [VERSION] | [YYYY-MM-DD] | ArcKit AI | Initial creation from `/arckit.secure` | [PENDING] | [PENDING] |

## Document Purpose

This assessment summarises the system’s security posture and readiness for delivery and operations. It is used to:

- align security decisions with Australian Government obligations and organisational security policy
- surface security and privacy risks early, with clear owners and remediation actions
- support assurance activities (e.g., internal security sign-off, accreditation/ATO readiness, IRAP readiness where required)
- provide an evidence index that can be re-used across governance forums and delivery gates

---

## Executive Summary

**System**: [SYSTEM_NAME]

**Service Type**: [Public-facing / Staff-facing / Mixed / API / Data platform]

**Data/Information Classification**: [PUBLIC / OFFICIAL / OFFICIAL:Sensitive / PROTECTED / SECRET / TOP SECRET]

**Overall Security Posture**: [Strong / Adequate / Needs Improvement / Inadequate]

**Control Area Scorecard**:

| Control Area | Status | Notes |
|---|---|---|
| Governance, risk, assurance | [✅/⚠️/❌/N/A] | [Notes] |
| Identity, access, privilege | [✅/⚠️/❌/N/A] | [Notes] |
| Data protection and privacy | [✅/⚠️/❌/N/A] | [Notes] |
| Platform/network/endpoint | [✅/⚠️/❌/N/A] | [Notes] |
| Secure engineering/supply chain | [✅/⚠️/❌/N/A] | [Notes] |
| Logging/monitoring/detection | [✅/⚠️/❌/N/A] | [Notes] |
| Incident response/resilience | [✅/⚠️/❌/N/A] | [Notes] |
| Cloud shared responsibility | [✅/⚠️/❌/N/A] | [Notes] |

**Essential Eight (ASD) Maturity**:

- **Current**: [0 / 1 / 2 / 3 / Unknown]
- **Target**: [0 / 1 / 2 / 3]

**Assurance / Accreditation Readiness**:

- **Internal security sign-off**: [Ready / Not ready / In progress]
- **Accreditation / ATO approach** (if applicable): [Defined / Not defined]
- **IRAP assessment** (if required): [Not required / Planned / In progress / Completed]

**Privacy & Data Protection Readiness**:

- **Personal information processed**: [Yes / No]
- **Privacy impact assessment (PIA)**: [Completed / In progress / Not started / N/A]
- **Notifiable Data Breaches (NDB) readiness**: [Ready / Not ready / In progress]

**Top Findings (Highest Priority)**:

| # | Finding | Impact | Priority | Owner | Target Date |
|---|---------|--------|----------|-------|------------|
| 1 | [Finding] | [Impact] | [Critical/High] | [Name/Role] | [YYYY-MM-DD] |
| 2 | [Finding] | [Impact] | [Critical/High] | [Name/Role] | [YYYY-MM-DD] |
| 3 | [Finding] | [Impact] | [High/Medium] | [Name/Role] | [YYYY-MM-DD] |

**Top Risks (Security/Privacy)**:

| Risk ID | Risk | Likelihood | Consequence | Rating | Treatment |
|--------|------|------------|-------------|--------|-----------|
| [R-001] | [Risk] | [L/M/H] | [L/M/H] | [L/M/H/VH] | [Mitigate/Transfer/Accept/Avoid] |

---

## 1. System Overview

### 1.1 Scope And Boundaries

- **In scope**: [Applications, services, environments, integrations]
- **Out of scope**: [Explicit exclusions]
- **Trust boundaries**: [Where identity, networks, and data cross boundaries]
- **Dependencies**: [Shared platforms, COTS/SaaS, identity provider, networks]

### 1.2 Users And Access Patterns

- **User groups**: [Public users / Staff / Partners / Admins / Machine identities]
- **Authentication**: [IDP/SSO details]
- **Authorisation**: [RBAC/ABAC, privileged roles]
- **Admin access model**: [Break-glass, PAM, JIT access]

### 1.3 Data, Information, And Records

- **Data types**: [PII, financial, health, classified, telemetry]
- **Classification & handling**: [Summary of classification and handling requirements]
- **Data residency**: [Australia / Approved jurisdictions / Mixed]
- **Retention & disposal**: [Policy references, archival, deletion]

### 1.4 Hosting And Delivery Model

- **Hosting**: [Cloud / On-prem / Hybrid]
- **Cloud provider/services** (if applicable): [AWS/Azure/GCP/Other]
- **Environment separation**: [Dev/Test/Prod]
- **Deployment approach**: [CI/CD, IaC, release cadence]

### 1.5 Third Parties And Supply Chain

- **Third-party services**: [List]
- **Supplier roles**: [Build/Operate/Support]
- **Data sharing**: [Inbound/outbound, agreements]

---

## 2. Compliance And Assurance Scope

This assessment is structured to remain useful across agencies, while allowing mapping to organisation-specific policy and control catalogues.

### 2.1 Core Australian Government Security Expectations (Reference Set)

Assess the system against:

- **ASD Essential Eight** maturity requirements (current and target)
- **Agency security policy** and any mandatory control sets derived from:
  - Protective Security Policy Framework (PSPF) domains (governance, information, personnel, physical) as applicable
  - Australian Government Information Security Manual (ISM) aligned controls as applicable
- **Cloud security** expectations (shared responsibility, tenancy, logging, key management), and **IRAP** readiness where required by the delivery context
- **Privacy Act 1988 (APPs)** obligations for personal information handling, and readiness for the **Notifiable Data Breaches (NDB) scheme**

### 2.2 Security Assurance Gates (Tailor To Project)

| Gate | When | Output Evidence |
|------|------|----------------|
| Security architecture review | [Discovery/Alpha/Beta] | [Architecture diagrams, control decisions, threat model] |
| Secure SDLC evidence | [Alpha/Beta] | [Pipeline checks, code review approach, SAST/DAST/SCA evidence] |
| Penetration testing | [Beta/Pre-live] | [Report, remediation plan, retest evidence] |
| Accreditation / ATO (if required) | [Pre-live] | [Security risk assessment, residual risk acceptance, sign-offs] |
| IRAP assessment (if required) | [Pre-live / Cloud onboarding] | [IRAP report, remediation evidence] |
| Operational readiness | [Pre-live] | [Monitoring, incident response, DR, runbooks] |

---

## 3. Evidence Inventory (What We Used)

| Evidence | Location | What It Informed |
|----------|----------|------------------|
| Requirements | `projects/[PROJECT]/ARC-[ID]-REQ-v*.md` | NFR-SEC, NFR-A, NFR-R, integration and data requirements |
| Principles | `projects/000-global/ARC-000-PRIN-v*.md` | Approved platforms, guardrails, compliance expectations |
| Risk register | `projects/[PROJECT]/ARC-[ID]-RISK-v*.md` | Threats, mitigations, risk appetite and residual risk |
| Privacy assessment | `projects/[PROJECT]/ARC-[ID]-PIA-v*.md` | APP risks, mitigations, data handling constraints |
| Architecture diagrams | `projects/[PROJECT]/diagrams/ARC-[ID]-DIAG-*.md` | Trust boundaries, data flows, deployment topology |
| ADRs | `projects/[PROJECT]/decisions/ADR-*.md` | Decision rationale, trade-offs, risk acceptance |
| External security reports | `projects/[PROJECT]/external/*` | Vulnerability findings, pen test results, audit evidence |

### 3.1 Evidence Quality Rubric (How To Judge Strength)

Use this rubric to avoid “paper compliance”:

- **Strong evidence**: implemented control + measurable telemetry + operational process + test results (e.g., config baselines, CI checks, scan results, runbooks, drills).
- **Medium evidence**: implemented control + partial telemetry/process (e.g., logging configured but no alert runbooks or no retention tested).
- **Weak evidence**: intention statements only (e.g., “we will do MFA later”) without designs, decisions, or delivery backlog actions.

---

## 4. Secure By Design Assessment (Control Areas)

> Use the statuses consistently: ✅ Achieved / ⚠️ Partially Achieved / ❌ Not Achieved / N/A.

### 4.1 Governance, Risk, And Assurance

**Status**: [✅/⚠️/❌/N/A]

**What to look for (examples)**:

- security roles and decision rights are clear (including risk acceptance)
- security risks are tracked, treated, and re-assessed as the architecture changes
- assurance gates are defined (and evidence is planned or completed)
- supplier assurance requirements are defined (and checked)

**Evidence**:
- [Links/artefacts]

**Findings**:
- [Finding]

**Actions**:
- [Action] (Owner: [Role], Due: [YYYY-MM-DD])

**Minimum evidence to cite (examples)**:

- risk register entries that cover security and privacy risks (and owners)
- a security decision/approval pathway (who can accept residual risk)
- assurance plan / gates (design review, pen test, IRAP readiness if required)
- supplier assurance requirements (contractual clauses, attestations, assurance reports)

**Checklist (examples)**:

- [ ] Security decision rights and escalation are documented (incl. residual risk acceptance)
- [ ] Security risks are tracked with treatments and review cadence
- [ ] Assurance gates exist and are scheduled (and not left to the end)
- [ ] Third-party assurance requirements exist (and are verified)
- [ ] Exceptions/waivers process exists and is auditable

### 4.2 Identity, Access, And Privilege Management

**Status**: [✅/⚠️/❌/N/A]

**What to look for (examples)**:

- MFA is enforced for users and administrators as appropriate
- privileged access is controlled (PAM, JIT/JEA, break-glass)
- service accounts and secrets are managed and rotated
- access is reviewed and removed promptly when no longer required

**Evidence**:
- [Links/artefacts]

**Findings**:
- [Finding]

**Actions**:
- [Action] (Owner: [Role], Due: [YYYY-MM-DD])

**Minimum evidence to cite (examples)**:

- identity provider integration and MFA enforcement scope
- privileged admin model (PAM/JIT/break-glass) and audit trail
- access review process and deprovisioning SLAs
- secrets management approach (vault/KMS, rotation, separation of duties)

**Checklist (examples)**:

- [ ] MFA enforced for all interactive users (scope stated, exceptions justified)
- [ ] Privileged access is time-bound and logged (break-glass tested)
- [ ] Service accounts are minimised, scoped, and rotated
- [ ] Access reviews are scheduled and evidenced
- [ ] AuthN/AuthZ decisions are recorded (ADR or equivalent)

### 4.3 Data Protection And Privacy

**Status**: [✅/⚠️/❌/N/A]

**What to look for (examples)**:

- data classification and handling controls are implemented (including sharing constraints)
- encryption is used appropriately and keys are managed (KMS/HSM, rotation, access separation)
- retention and disposal are defined and implemented
- APP-related controls are addressed (collection minimisation, access/correction processes, notices)
- NDB response and notification readiness is defined

**Evidence**:
- [Links/artefacts]

**Findings**:
- [Finding]

**Actions**:
- [Action] (Owner: [Role], Due: [YYYY-MM-DD])

**Minimum evidence to cite (examples)**:

- data classification decisions and handling requirements
- encryption approach (at rest/in transit) and key management model
- data sharing agreements and disclosure controls (where applicable)
- retention/disposal implementation evidence (not just policy)
- PIA findings and mitigations linked to delivery actions

**Checklist (examples)**:

- [ ] Data classification and handling rules are documented and implemented
- [ ] Encryption is used appropriately and keys are protected/rotated
- [ ] Data minimisation is applied (collection, fields, retention, access)
- [ ] Data sharing/disclosure is governed (purpose, controls, logging)
- [ ] NDB process is defined and exercised (roles, triage, comms)

### 4.4 Platform, Network, And Endpoint Security

**Status**: [✅/⚠️/❌/N/A]

**What to look for (examples)**:

- hardened baselines are defined and applied (OS, containers, Kubernetes, endpoints)
- patching cadence and vulnerability management are defined and measurable
- network segmentation and boundary protection are implemented (including egress control)
- environments are separated and production access is controlled and audited

**Evidence**:
- [Links/artefacts]

**Findings**:
- [Finding]

**Actions**:
- [Action] (Owner: [Role], Due: [YYYY-MM-DD])

**Minimum evidence to cite (examples)**:

- hardened baselines and configuration-as-code (where applicable)
- patching and vulnerability management metrics and SLAs
- network segmentation and boundary controls (including egress)
- environment separation and production access controls

**Checklist (examples)**:

- [ ] Secure baselines exist for OS/container/K8s/endpoints (and are enforced)
- [ ] Vulnerability scanning is scheduled and coverage is known
- [ ] Patch SLAs exist and are measured (exceptions tracked)
- [ ] Network boundaries, egress, and segmentation are documented and implemented
- [ ] Production access is controlled, logged, and reviewed

### 4.5 Secure Engineering And Supply Chain

**Status**: [✅/⚠️/❌/N/A]

**What to look for (examples)**:

- secure coding practices and peer review are consistent
- automated checks exist in CI/CD (SAST, SCA, secrets scanning, IaC scanning)
- dependency and container/image provenance is addressed (signing, SBOM, pinning)
- third-party and open source risks are identified and managed

**Evidence**:
- [Links/artefacts]

**Findings**:
- [Finding]

**Actions**:
- [Action] (Owner: [Role], Due: [YYYY-MM-DD])

**Minimum evidence to cite (examples)**:

- secure SDLC practices and security requirements in stories/acceptance criteria
- CI/CD controls (SAST/DAST/SCA, secrets scanning, IaC scanning)
- dependency management (pinning, provenance, SBOM where appropriate)
- supplier security expectations and verification evidence

**Checklist (examples)**:

- [ ] Security requirements are included in delivery artefacts (REQ/backlog/ADRs)
- [ ] CI/CD includes automated security checks with defined “fail the build” rules
- [ ] Secrets scanning prevents credential leakage
- [ ] Dependency and container/image scanning is implemented and acted on
- [ ] SBOM/provenance approach is defined for higher-risk systems

### 4.6 Logging, Monitoring, And Detection

**Status**: [✅/⚠️/❌/N/A]

**What to look for (examples)**:

- security-relevant logs are defined, retained, and protected from tampering
- alerting is actionable, with on-call / triage expectations
- monitoring covers identity, network, platform, and application layers
- vulnerability scanning and testing is scheduled and tracked

**Evidence**:
- [Links/artefacts]

**Findings**:
- [Finding]

**Actions**:
- [Action] (Owner: [Role], Due: [YYYY-MM-DD])

**Minimum evidence to cite (examples)**:

- logging design (what is logged, where, retention, access controls)
- detection and alerting rules with on-call/triage process
- monitoring coverage across identity/network/platform/app layers
- test evidence: alert drills, log integrity checks, incident simulations

**Checklist (examples)**:

- [ ] Security-relevant events are logged (auth, admin, data access, changes)
- [ ] Logs are protected from tampering and have defined retention
- [ ] Alerts are actionable (owners, runbooks, SLOs)
- [ ] Vulnerability scanning and pen tests are scheduled and tracked
- [ ] Monitoring is validated (test alerts, game-days, tabletop exercises)

### 4.7 Incident Response And Resilience

**Status**: [✅/⚠️/❌/N/A]

**What to look for (examples)**:

- incident response playbooks exist for common scenarios (credential compromise, ransomware, data exfiltration)
- roles, escalation, and communications are defined (internal and supplier)
- backups are protected and recoverable; recovery objectives are defined and tested
- post-incident reviews drive measurable improvements

**Evidence**:
- [Links/artefacts]

**Findings**:
- [Finding]

**Actions**:
- [Action] (Owner: [Role], Due: [YYYY-MM-DD])

**Minimum evidence to cite (examples)**:

- incident response plan and playbooks (incl. escalation and communications)
- backup and restore evidence (frequency, encryption, restore tests)
- recovery objectives (RTO/RPO) and DR test outcomes
- post-incident review process and improvement backlog

**Checklist (examples)**:

- [ ] Incident playbooks exist for likely scenarios and are exercised
- [ ] Backups are encrypted, protected (including from ransomware), and restore-tested
- [ ] RTO/RPO are defined and validated via exercises
- [ ] Evidence retention supports investigations and NDB decision-making

### 4.8 Cloud Security And Shared Responsibility (If Applicable)

**Status**: [✅/⚠️/❌/N/A]

**Cloud Model**: [IaaS/PaaS/SaaS/N/A]

**What to look for (examples)**:

- shared responsibility boundaries are explicit (provider vs agency vs supplier)
- cloud identity is integrated with enterprise identity and is least-privileged
- guardrails exist for networks, IAM, encryption, and logging
- the approach to IRAP (if required) is defined early and tracked as part of delivery

**Evidence**:
- [Links/artefacts]

**Findings**:
- [Finding]

**Actions**:
- [Action] (Owner: [Role], Due: [YYYY-MM-DD])

**Minimum evidence to cite (examples)**:

- shared responsibility model for cloud services and suppliers
- cloud IAM guardrails, network guardrails, encryption defaults, logging defaults
- tenancy isolation approach and environment separation
- IRAP expectations and readiness plan (where required)

**Checklist (examples)**:

- [ ] Cloud identity is least-privileged and integrated with enterprise identity
- [ ] Guardrails exist for networking, IAM, encryption, logging, and tagging
- [ ] Tenant/environment isolation is defined and tested
- [ ] IRAP readiness is planned early (if required) and tracked

### 4.9 Vulnerability And Patch Management (Recommended Detail)

**Status**: [✅/⚠️/❌/N/A]

**Vulnerability scanning frequency**: [Daily / Weekly / Monthly]

**Coverage**: [What is scanned and what is excluded]

**Vulnerability management process**:

- [ ] prioritisation approach exists (severity + exploitability + exposure)
- [ ] remediation SLAs exist (and are measurable)
- [ ] exceptions process exists for unfixable/accepted risks
- [ ] metrics and reporting exist (trend, backlog, time-to-remediate)

**Patch management process**:

- [ ] patch assessment and testing approach exists
- [ ] deployment cadence exists for different asset classes
- [ ] emergency patching process exists
- [ ] patch compliance is measured and reported
- [ ] rollback procedures exist

**Gaps/Actions**:
- [Action]

### 4.10 Third-Party And Supply Chain Risk (Recommended Detail)

**Status**: [✅/⚠️/❌/N/A]

**Key third parties**:

| Vendor | Service | Data Access | Risk Level | Key Controls / Evidence |
|---|---|---|---|---|
| [Vendor] | [Service] | [None/Read/Write/Admin] | [L/M/H] | [Evidence] |

**Supplier assurance**:

- [ ] security requirements exist in contracts and SOWs
- [ ] subcontractors are identified and governed
- [ ] supplier access is controlled and logged
- [ ] incident notification and cooperation requirements are defined

**Open source software (OSS)**:

- [ ] dependency inventory maintained (SBOM where appropriate)
- [ ] vulnerability scanning in CI/CD
- [ ] license compliance checks (where required)
- [ ] upgrade/patching plan exists for critical dependencies

**Gaps/Actions**:
- [Action]

### 4.11 Backup, Restore, And Disaster Recovery (Recommended Detail)

**Status**: [✅/⚠️/❌/N/A]

**Backup method**: [Snapshots / Replication / 3-2-1 / Other]

**Backup controls**:

- [ ] backups are automated and monitored
- [ ] backups are encrypted and access-controlled
- [ ] backups are protected against ransomware (immutability / separation)
- [ ] restore tests are performed and evidenced

**RTO**: [X hours]  
**RPO**: [X hours]

**Last restore test**: [YYYY-MM-DD]  
**Last DR exercise**: [YYYY-MM-DD]

**Gaps/Actions**:
- [Action]

### 4.12 Secure SDLC And DevSecOps (Recommended Detail)

**Status**: [✅/⚠️/❌/N/A]

**Secure SDLC controls**:

- [ ] security requirements in stories/acceptance criteria
- [ ] threat modelling performed for key flows/trust boundaries
- [ ] code review includes security considerations
- [ ] SAST implemented
- [ ] DAST implemented (where applicable)
- [ ] SCA (dependency scanning) implemented
- [ ] secrets scanning implemented
- [ ] IaC scanning implemented (where applicable)

**Build integrity**:

- [ ] build artefacts are immutable and traceable
- [ ] signing and provenance approach exists (where appropriate)

**Gaps/Actions**:
- [Action]

### 4.13 Overall Assessment Summary (Optional)

**Strengths**:
- [Strength]

**Critical gaps / blockers**:
- [Gap]

**Overall risk rating**: [Low / Medium / High / Very High]

---

## 5. ASD Essential Eight Assessment

> Record current and target maturity. Use maturity levels 0-3.

| Mitigation Strategy | Current Maturity | Target Maturity | Evidence | Gaps / Actions |
|---------------------|------------------|----------------|----------|----------------|
| Application control | [0/1/2/3] | [0/1/2/3] | [Evidence] | [Actions] |
| Patch applications | [0/1/2/3] | [0/1/2/3] | [Evidence] | [Actions] |
| Configure Microsoft Office macro settings | [0/1/2/3] | [0/1/2/3] | [Evidence] | [Actions] |
| User application hardening | [0/1/2/3] | [0/1/2/3] | [Evidence] | [Actions] |
| Restrict administrative privileges | [0/1/2/3] | [0/1/2/3] | [Evidence] | [Actions] |
| Patch operating systems | [0/1/2/3] | [0/1/2/3] | [Evidence] | [Actions] |
| Multi-factor authentication (MFA) | [0/1/2/3] | [0/1/2/3] | [Evidence] | [Actions] |
| Regular backups | [0/1/2/3] | [0/1/2/3] | [Evidence] | [Actions] |

**Essential Eight Notes**:

- coverage scope (end-user devices vs servers vs cloud identities) must be stated
- maturity targets should align to business impact and data classification

---

## 6. Privacy And Data Protection (If Applicable)

### 6.1 Personal Information Handling Summary

- **Personal information processed**: [Yes / No]
- **PIA status**: [Completed / In progress / Not started / N/A]
- **Key APP obligations addressed**:
  - [APP 1 governance and notices]
  - [APP 3 collection minimisation]
  - [APP 5 notices]
  - [APP 6 use/disclosure and data sharing]
  - [APP 11 security]
  - [Access and correction processes]

### 6.2 Notifiable Data Breaches (NDB) Readiness

- **Incident classification** includes “eligible data breach” assessment: [Yes/No]
- **Notification approach** (OAIC and affected individuals, as required): [Defined/Not defined]
- **Supplier notification SLAs**: [Defined/Not defined]

**Gaps/Actions**:
- [Action] (Owner: [Role], Due: [YYYY-MM-DD])

---

## 7. Threat Model Summary (Recommended)

**Key threat actors**:

- [Actor]

**Key threats and attack paths**:

| Threat | Impact | Existing Mitigations | Residual Risk | Actions |
|--------|--------|----------------------|--------------|---------|
| [Threat] | [Impact] | [Mitigations] | [L/M/H] | [Actions] |

---

## 8. Recommendations And Delivery Plan

### 8.1 Prioritised Actions

| Priority | Timeframe | Actions |
|----------|-----------|---------|
| Critical | 0-30 days | [Actions] |
| High | 1-3 months | [Actions] |
| Medium | 3-6 months | [Actions] |
| Low | 6+ months | [Actions] |

### 8.2 Ownership And Tracking

- actions must be tracked in delivery tooling (backlog/risk register)
- acceptances of residual risk must be explicit (who, when, why)

---

## 9. Appendix

### 9.1 Glossary

- **ATO**: Authority to Operate (or equivalent internal security accreditation decision)
- **IRAP**: Information Security Registered Assessors Program
- **ISM**: Australian Government Information Security Manual
- **PSPF**: Protective Security Policy Framework

### 9.2 References

- [Link/Reference: agency security policy]
- [Link/Reference: Essential Eight maturity model guidance]
- [Link/Reference: ISM control catalogue (internal reference)]

---

**Generated by**: ArcKit `/arckit.secure`
**Generated on**: [YYYY-MM-DD HH:MM] UTC
**ArcKit Version**: [VERSION]
**Project**: [PROJECT_NAME] (Project [PROJECT_ID])
**AI Model**: [AI_MODEL]
