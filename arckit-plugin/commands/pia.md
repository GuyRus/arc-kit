---
description: "Generate privacy impact assessment (PIA) pack aligned to OAIC guidance and the Privacy Act 1988 (APPs)"
---

You are helping an enterprise architect generate a **Privacy Impact Assessment (PIA)** pack following OAIC guidance (PIA Guide) and the Privacy Act 1988 / Australian Privacy Principles (APPs).

A PIA is a systematic assessment of a project to identify privacy impacts on individuals and set out recommendations to manage, minimise, or eliminate those impacts. Under APP 1, PIAs support “privacy by design”. The OAIC can also direct agencies to provide a PIA where a proposed activity or change may have a significant impact on privacy.

## User Input
```text
$ARGUMENTS
```

## Instructions

### Step 0: Read Available Documents

Scan the project directory for existing artefacts and read them to inform the PIA:

**MANDATORY** (warn if missing):
- `ARC-*-DATA-*.md` in `projects/{project}/` — Data model
  - Extract: Entities containing personal information and sensitive information (Privacy Act s 6(1)), retention/disposal (APP 11.3), cross-border disclosures (APP 8), data flows, data classifications
  - If missing: STOP and warn user to run `/arckit.data-model` first — a PIA should be based on a data model/inventory of personal information handling

**RECOMMENDED** (read if available, note if missing):
- `ARC-000-PRIN-*.md` in `projects/000-global/` — Architecture principles
  - Extract: Privacy by Design principles, data minimisation principles, security principles
  - If missing: warn that PIAs should be informed by Privacy by Design principles
- `ARC-*-REQ-*.md` in `projects/{project}/` — Requirements specification
  - Extract: DR (data requirements), NFR-SEC (security), NFR-C (compliance/privacy), and any requirements that materially affect individuals (eligibility/entitlements/sanctions)
- `ARC-*-STKE-*.md` in `projects/{project}/` — Stakeholder analysis
  - Extract: Data subject categories, vulnerable groups, power imbalance, and governance roles (service owner, privacy officer, security lead, data stewards)

**OPTIONAL** (read if available, skip silently if missing):
- `ARC-*-RISK-*.md` in `projects/{project}/` — Risk register
  - Extract: Data protection risks, privacy risks already identified
- `ARC-*-SECD-*.md` in `projects/{project}/` — Secure by Design assessment
  - Extract: Security controls relevant to data protection

**What to extract from each document**:
- **Data Model**: Personal/sensitive information categories, data subjects, retention/disposal, APP 8 cross-border disclosures, data flows
- **Principles**: Privacy by Design and data minimisation standards
- **Requirements**: Data requirements, privacy/security controls, and decision-impacting features
- **Stakeholders**: Data subjects, vulnerable groups, governance roles and approval pathways

### Step 0b: Check for External Documents (optional)

Scan for external (non-ArcKit) documents the user may have provided:

**Existing PIAs and supplier data handling agreements**:
- **Look in**: `projects/{project-dir}/external/`
- **File types**: PDF (.pdf), Word (.docx), Markdown (.md)
- **What to extract**: Previous PIA findings, contract terms and assurance artefacts, cross-border disclosure assessments (APP 8), incident response expectations (NDB), and any data flow diagrams
- **Examples**: `existing-pia.pdf`, `supplier-data-handling-agreement.pdf`, `privacy-notice.docx`

**Privacy policies and information handling standards**:
- **Look in**: `projects/000-global/policies/`
- **File types**: PDF, Word, Markdown
- **What to extract**: Organisational privacy policy, retention schedule, classification scheme
- **Examples**: `privacy-policy.pdf`, `data-retention-schedule.docx`, `data-classification.md`

**Enterprise-Wide Data Protection Standards**:
- **Look in**: `projects/000-global/external/`
- **File types**: PDF, Word, Markdown
- **What to extract**: Enterprise data protection standards, privacy impact templates, cross-project PIA benchmarks

**User prompt**: If no external data protection docs found, ask:
"Do you have any existing PIAs, supplier data handling agreements, or privacy policies? I can read PDFs directly. Place them in `projects/{project-dir}/external/` and re-run, or skip."

**Important**: This command works without external documents. They enhance output quality but are never blocking.

### Step 0c: Interactive Configuration

Before generating the PIA, use the **AskUserQuestion** tool to gather the assessment scope. **Skip if the user has already specified scope in their arguments.**

**Question 1** — header: `Scope`, multiSelect: false
> "What is the scope of this Privacy Impact Assessment (PIA)?"
- **Full system (Recommended)**: Assess all personal information handling across the system — recommended for new systems or major changes
- **Specific feature or module**: Assess a single feature that introduces new personal information handling or new risks (e.g., AI-assisted eligibility checks)
- **Specific data flow**: Assess a particular data flow (e.g., outsourcing, cross-agency sharing, overseas hosting/support)

**Question 2** — header: `Consultation`, multiSelect: false
> "How should data subject consultation be approached?"
- **Surveys (Recommended)**: Online questionnaires to affected user groups — scalable and documented
- **Interviews**: One-on-one or small group discussions — deeper insights for sensitive processing
- **Workshops**: Facilitated sessions with representative data subjects — collaborative and thorough
- **Not applicable**: Data subjects cannot reasonably be consulted (e.g., law enforcement, national security)

Apply the user's selections: the scope determines which data model entities and processing activities to assess. The consultation approach is documented in the Consultation section of the PIA.

### Step 1: Identify or Create Project

First, check for existing projects:

```bash
bash .arckit/scripts/bash/list-projects.sh --json
```

If the user specifies an existing project or the name matches, use that directory. Otherwise, create a new project:

```bash
bash .arckit/scripts/bash/create-project.sh --name "$PROJECT_NAME" --json
```

Parse the JSON output to get `project_id` and `project_path`.

### Step 2: Read Source Artifacts

Read all documents listed in Step 0 above. Use the extracted information for auto-population of the PIA template.

### Step 3: PIA Template Reading

Read the PIA template:

**Read the template** (with user override support):
- **First**, check if `.arckit/templates/pia-template.md` exists in the project root
- **If found**: Read the user's customized template (user override takes precedence)
- **If not found**: Read `.arckit/templates/pia-template.md` (default)

> **Note**: Read the `.arckit/VERSION` file and update the version in the template metadata line when generating.
> **Tip**: Users can customise templates with `/arckit.customize pia`

This template follows the OAIC PIA Guide structure (threshold assessment → information flows → compliance check → risk management → report and review).

### Step 4: OAIC Threshold Assessment (Automated)

Run a threshold assessment (OAIC PIA Guide Step 1) to decide whether a PIA is needed and how detailed it should be.

Score each indicator based on evidence in the data model, requirements, and stakeholders:

| Indicator | YES/NO | Evidence |
|----------|--------|----------|
| Personal information involved | [YES/NO] | Entities/attributes in `ARC-*-DATA-*.md` |
| Sensitive information involved (Privacy Act s 6(1)) | [YES/NO] | Data model classification |
| Large volume / aggregation / new central database | [YES/NO] | Volumes, scale, retention |
| Outsourcing or external service providers (incl. overseas) | [YES/NO] | Integrations, hosting, vendor model |
| Cross-agency/cross-sector sharing, matching, or combining datasets | [YES/NO] | INT requirements + data flows |
| New technology or new legislation required | [YES/NO] | AI/ML, biometrics, monitoring, etc. |
| Compulsory collection or power imbalance | [YES/NO] | Govt-citizen, employer-employee, etc. |
| Potential adverse outcomes for individuals | [YES/NO] | Eligibility/entitlements/sanctions impacts |

**PIA Decision Guidance**:
- If personal information is involved, a PIA is generally recommended.
- The greater the privacy scope and risk indicators above, the more comprehensive the PIA should be.
- Agencies may be directed by the OAIC to provide a PIA where an activity or change may significantly impact privacy.

Show the threshold results to the user and proceed to generate the PIA unless the user explicitly declines.

### Step 5: Generate PIA Report

**CRITICAL**: Use the **Write tool** to create the PIA report. These documents are typically 3,000-10,000 words and will exceed the 32K token output limit if you try to output the full document in the chat.

Generate the PIA report by:

1. **Detect version**: Before generating the document ID, check if a previous version exists:
   - Look for existing `ARC-{PROJECT_ID}-PIA-v*.md` files in the project directory
   - **If no existing file**: Use VERSION="1.0"
   - **If existing file found**:
     - Read the existing document to understand its scope
     - Compare against current data model and requirements
     - **Minor increment** (e.g., 1.0 → 1.1): Scope unchanged — refreshed risk scores, updated mitigations, corrected details
     - **Major increment** (e.g., 1.0 → 2.0): Scope materially changed — new data categories, new processing purposes, fundamentally different risk landscape
   - For v1.1+/v2.0+: Add a Revision History entry describing what changed from the previous version

2. **Auto-populate Document Control**:
   ```bash
   # Generate document ID
   DOC_ID=$(bash .arckit/scripts/bash/generate-document-id.sh {project_id} PIA v${VERSION})
   ```
   - Document ID: `{DOC_ID}` (e.g., ARC-001-PIA-v1.0)
   - Version: ${VERSION}
   - Status: DRAFT
   - Date Created: {current_date}
   - Assessment Date: {current_date}
   - Next Review Date: {current_date + 12 months}
   - Classification: OFFICIAL:Sensitive

3. **Populate the template sections (OAIC 10-step PIA flow)**:
   - Use the structure and headings in `.arckit/templates/pia-template.md`.
   - Treat the OAIC steps as the organising backbone: threshold → plan → describe → consult → flows → compliance → risks → recommendations → report → respond/review.
   - Remove or correct any non-Australian privacy terminology if it appears in source artefacts (e.g., “controller/processor”, “lawful basis”, “Article 35”). Translate into Privacy Act / APP terms and the project’s governance model.

   **Section 1: Threshold assessment (OAIC Step 1)**:
   - Copy threshold assessment results from Step 4
   - Explain why a PIA is appropriate and whether it is targeted vs comprehensive
   - If the entity is an Australian Government agency: note that the Commissioner may direct an agency to provide a PIA (Privacy Act 1988 s 33D)

   **Section 2: Plan the PIA (OAIC Step 2)**:
   - Identify roles (PIA lead, privacy, security, records/IM, legal/policy, service owner, vendor manager)
   - List inputs and evidence sources (data model, requirements, stakeholders, security, vendor artefacts)
   - Define deliverables (PIA report + action plan + notice changes)

   **Section 3: Describe the project/activity (OAIC Step 3)**:
   - Project overview, scope boundaries, and context
   - Individuals affected (including vulnerable groups) and any power imbalance
   - Legal/policy context and decision points where authority is unclear

   **Section 4: Consultation (OAIC Step 4)**:
   - Internal consultation outcomes (privacy, security, records/IM, legal/policy, service owner)
   - External consultation approach and findings (or rationale why not practicable)

   **Section 5: Information flows and lifecycle mapping (OAIC Step 5)**:
   - Map collection → storage → use → disclosure → retention → disposal/de-identification
   - Summarise inventory from the data model and call out gaps
   - Document all disclosures, including any overseas disclosure/access patterns (APP 8)

   **Section 6: Privacy analysis / compliance check (OAIC Step 6)**:
   - Complete an APP compliance matrix (at minimum: APP 1/3/5/6/8/10/11/12/13; add APP 2/4/7/9 where applicable)
   - For each APP obligation: record evidence, gaps, and actions
   - Include Notifiable Data Breaches (NDB) readiness: assessment within 30 days, notification as soon as practicable if eligible
   - Document retention and disposal approach (APP 11.3), including records/Archives constraints if relevant

   **Section 7: Privacy impacts and risk assessment (OAIC Step 7)**:
   - Identify privacy harms from the perspective of individuals (not only organisational risk)
   - Use a simple risk scale (Likelihood: Remote/Possible/Probable; Consequence: Minimal/Significant/Severe; Overall: Low/Medium/High)
   - Create `PIA-###` risks and link to related entries in `ARC-*-RISK-*.md` where appropriate

   **Section 8: Recommendations and action plan (OAIC Step 8)**:
   - Convert mitigations into specific actions with owners, due dates, and evidence of completion
   - If residual risk remains High: document escalation and acceptance decision/conditions

   **Section 9: Report and sign-off (OAIC Step 9)**:
   - Provide signature blocks for service owner, privacy, security, records/IM, and SRO
   - Document distribution and storage arrangements (classification-appropriate)

   **Section 10: Respond and review (OAIC Step 10)**:
   - Define implementation tracking, verification, and review triggers
   - For agencies: include register updates (PIA register + personal information holdings register) where applicable

   **Appendices (as applicable)**:
   - Cross-border disclosure assessment (APP 8)
   - NDB checklist
   - AI-specific addendum (where AI/ML or GenAI is in scope), including whether DTA AI impact assessment requirements apply

Write the complete PIA document to:

```
projects/{project_id}/ARC-{PROJECT_ID}-PIA-v${VERSION}.md
```

### Step 6: Risk Register Integration (Optional)

Ask the user:

```
📊 PIA generated with [N] risks identified.

Would you like to add PIA risks to the project risk register?
This will create/update: projects/{project_id}/ARC-*-RISK-*.md

[Y/N]
```

If YES:
1. Read `projects/{project_id}/ARC-*-RISK-*.md` (or create from template if it doesn't exist)
2. Add each PIA risk as a new entry with:
   - Risk ID: PIA-001, PIA-002, etc.
   - Category: "Privacy"
   - Source: "PIA Assessment"
   - Link back to PIA document
3. Update the risk register file

### Step 7: Summary Output

**IMPORTANT**: Do NOT output the full PIA document to the chat (it's too large). Instead, show a concise summary:

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
✅ PIA Generated Successfully
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

📄 Document: projects/{project_id}/ARC-{PROJECT_ID}-PIA-v{VERSION}.md
📋 Document ID: {document_id}
📅 Assessment Date: {date}
🔒 Classification: OFFICIAL:Sensitive

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
📊 Assessment Summary
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

**Threshold Assessment**: {summary of indicators} → {PIA scope recommendation}

**Processing Overview**:
- Data Subjects: {list data subject categories}
- Personal Information: {N} entities with personal information
- Sensitive Information: {YES/NO} ({categories if yes})
- APP Focus: {list key APPs impacted}
- Retention Period: {typical retention}

**Risk Assessment**:
- Total Risks Identified: {N}
  - 🔴 High: {N} (requires immediate action)
  - 🟠 Medium: {N} (requires mitigation)
  - 🟢 Low: {N} (accepted)

**Key Risks**:
1. PIA-001: {risk description} - {severity}
2. PIA-002: {risk description} - {severity}
3. PIA-003: {risk description} - {severity}

**Mitigations Proposed**: {N} technical, organisational, and procedural controls

**OAIC Engagement**: {PLANNED / NOT PLANNED / DIRECTED}

**Access & Correction (APP 12/13)**:
- ✅ Implemented: {pathways}
- ⚠️ Gaps: {gaps needing implementation}

**Next Steps**:
1. Review and approve PIA (service owner, privacy officer, security lead, SRO)
2. {If OAIC engagement planned/directed: provide next steps}
3. Implement recommended mitigations
4. Establish 12-month review cycle
5. {If children's data: Implement age verification and parental consent}

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
🔗 Traceability
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

**Source Artifacts**:
- ✅ Data Model: projects/{project_id}/ARC-*-DATA-*.md
- ✅ Requirements: projects/{project_id}/ARC-*-REQ-*.md
- ✅ Stakeholders: projects/{project_id}/ARC-*-STKE-*.md
- ✅ Architecture Principles: projects/000-global/ARC-000-PRIN-*.md

**Related Artifacts**:
- Risk Register: projects/{project_id}/ARC-*-RISK-*.md ({added/updated})
- Secure by Design: projects/{project_id}/ARC-*-SECD-*.md
- {If AI: AU AI governance assessment: projects/{project_id}/ARC-*-AIGA-*.md}
- {If AI: AITS: projects/{project_id}/ARC-*-AITS-*.md}

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
📚 References
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

- OAIC Guide to undertaking privacy impact assessments (PIAs)
- OAIC APP Guidelines (APP 8/11/12/13)
- OAIC Notifiable Data Breaches (NDB) scheme guidance
- Privacy Act 1988 (s 33D; definitions where relevant)

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

## Important Notes

1. **Policy expectation**: The OAIC strongly encourages PIAs for projects involving personal information. APP 1 supports privacy-by-design practices; agencies may also be directed to provide a PIA under the Privacy Act (s 33D).

2. **Use Write Tool**: PIAs are large documents. You MUST use the Write tool to create the file. Do NOT output the full PIA in the chat.

3. **Risk focus**: PIA risks focus on **impact on individuals** (privacy harm, discrimination, physical harm, financial loss, reputational damage), not only organisational risk. This is different from the project risk register.

4. **Threshold assessment first**: Always perform an OAIC-style threshold assessment first to decide whether a targeted vs comprehensive PIA is needed.

5. **Data model dependency**: A PIA cannot be generated without a data model. The data model is the source of truth for what personal information is being handled.

6. **Bidirectional risk links**: PIA risks should be added to the project risk register (category “Privacy”), and existing privacy risks in the risk register should be referenced in the PIA.

7. **Mitigation sources**: Extract controls from the Secure by Design assessment as PIA mitigations. This creates traceability from risks → mitigations → security controls.

8. **High residual risk escalation**: If residual privacy risk remains high after mitigations, escalate to privacy/legal governance and document the decision and conditions (especially for agencies).

9. **Classification**: PIAs often contain sensitive details about information flows, controls, and vulnerabilities. Default classification should be **OFFICIAL:Sensitive** unless a different protective marking is justified by the entity’s policy.

10. **Review cycle**: PIAs should be revisited and updated when:
    - New processing activities are added
    - Data protection risks change
    - OAIC guidance is updated
    - A data breach occurs

## Success Criteria

- ✅ PIA document created at `projects/{project_id}/ARC-{PROJECT_ID}-PIA-v${VERSION}.md`
- ✅ OAIC-style threshold assessment performed and documented
- ✅ OAIC 10-step PIA flow followed in the report structure
- ✅ All personal information and sensitive information from data model included
- ✅ Processing purposes extracted from requirements
- ✅ Data subjects and vulnerable groups identified from stakeholders
- ✅ Risk assessment completed with likelihood, severity, and overall risk scores
- ✅ Mitigations proposed for all high and medium risks
- ✅ Access and correction pathways assessed (APP 12/13)
- ✅ Cross-border disclosures assessed (APP 8) including accountability considerations (s 16C)
- ✅ NDB readiness addressed (assessment within 30 days; notify as soon as practicable if eligible)
- ✅ Traceability links to data model, requirements, stakeholders, principles, risk register
- ✅ Summary output shows key metrics, risks, and next steps
- ✅ Document classification set and justified (default OFFICIAL:Sensitive)
- ✅ 12-month review cycle established

## Example Usage

```
/arckit.pia Generate PIA for public health appointment system

/arckit.pia Create privacy impact assessment for benefits eligibility decision support tool

/arckit.pia Assess PIA scope for Windows 11 deployment (employee data only)
```
