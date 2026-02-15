# AI-007 — AU AI Requirements Extraction (Paragraph-level)

Scope: AU AI artifact rewrite requirements extracted from official corpus sources.

## Source verification (critical)

| Source | Corpus presence |
|---|---|
| DTA Guidance for the AI impact assessment tool PDF | `docs/policy-sources/au/ai/originals/dta-guidance-ai-impact-assessment-tool.pdf` + provenance checksum `4f7a322b26e4f42e87d5d3003038d91a5205bdf56c923ac62a9a468d9d0f0908` |
| DTA Policy for the responsible use of AI in government 2.0 | Present in corpus + mapped |
| DTA Australian Government AI technical standard | Present in corpus + mapped |

## Extracted requirement set

| Req ID | Requirement | Source evidence |
|---|---|---|
| AU-AI-REQ-001 | Agencies must publish and maintain an AI transparency statement. | `dta-policy-responsible-ai-gov-v2.txt` lines 334-343; `dta-standard-ai-transparency-statements.txt` lines 73-100 |
| AU-AI-REQ-002 | Agencies must develop and communicate a strategic position on AI adoption. | `dta-policy-responsible-ai-gov-v2.txt` lines 347-355 |
| AU-AI-REQ-003 | Agencies must designate accountable official(s) and notify DTA of changes. | `dta-policy-responsible-ai-gov-v2.txt` lines 366-375; `dta-standard-accountability.txt` lines 76-108 |
| AU-AI-REQ-004 | Agencies must designate accountable use case owner(s) for each in-scope AI use case. | `dta-policy-responsible-ai-gov-v2.txt` lines 379-385; `dta-standard-accountability.txt` lines 231-245 |
| AU-AI-REQ-005 | Agencies must maintain an internal in-scope AI use case register and share every 6 months. | `dta-policy-responsible-ai-gov-v2.txt` lines 389-399; `dta-standard-accountability.txt` lines 285-323 |
| AU-AI-REQ-006 | Internal register must include minimum mandatory fields. | `dta-standard-accountability.txt` lines 286-307 |
| AU-AI-REQ-007 | High-risk entries must include last/next review dates. | `dta-standard-accountability.txt` lines 309-312 |
| AU-AI-REQ-008 | Agencies must operationalise responsible AI (incident pathways, public/staff reporting, governance oversight). | `dta-policy-responsible-ai-gov-v2.txt` lines 427-442 |
| AU-AI-REQ-009 | Agencies must implement mandatory staff training on responsible AI use. | `dta-policy-responsible-ai-gov-v2.txt` lines 460-470 |
| AU-AI-REQ-010 | Agencies must assess all new AI use cases against in-scope criteria and document it. | `dta-policy-responsible-ai-gov-v2.txt` lines 537-542; `dta-guidance-ai-impact-assessment-tool.txt` lines 249-280 |
| AU-AI-REQ-011 | In-scope use cases must complete AI impact assessment before deployment with applied risk treatments. | `dta-policy-responsible-ai-gov-v2.txt` lines 538-547 |
| AU-AI-REQ-012 | Internal process variants must preserve AIA tool outcomes and be revisable for tool updates. | `dta-policy-responsible-ai-gov-v2.txt` lines 558-564 |
| AU-AI-REQ-013 | In-scope deployed use cases require ongoing monitoring and re-validation on material change. | `dta-policy-responsible-ai-gov-v2.txt` lines 566-573; `dta-ai-impact-assessment-tool.txt` lines 91-93 |
| AU-AI-REQ-014 | High-risk use cases require AO reporting, governance board/senior executive oversight, DTA reporting and at least annual review. | `dta-policy-responsible-ai-gov-v2.txt` lines 597-614 |
| AU-AI-REQ-015 | Transparency statement must include minimum content set and plain language requirement. | `dta-standard-ai-transparency-statements.txt` lines 73-90 |
| AU-AI-REQ-016 | Transparency statement must be publicly published and reviewed annually/material-change. | `dta-standard-ai-transparency-statements.txt` lines 92-100 |
| AU-AI-REQ-017 | AIA method should use 12-section structure with explicit roles, risk ratings, residual risk, and review logs. | `dta-guidance-ai-impact-assessment-tool.txt` lines 121, 142-201; `dta-ai-impact-assessment-tool.txt` lines 176-186, 548, 839 |
| AU-AI-REQ-018 | Agencies should apply a risk-based lifecycle assurance model with evidence traceability. | `finance-national-framework-assurance-ai.txt` lines 141-149, 362-387 |
| AU-AI-REQ-019 | Technical lifecycle controls should cover output constraints, validation, bias mitigation, monitoring, incident handling, and decommissioning. | `dta-ai-technical-standard.txt` lines 923-947, 1168-1214, 1335-1375 |
| AU-AI-REQ-020 | AI product adoption must include privacy-by-design due diligence and PIA, with APP-aligned handling. | `oaic-guidance-commercial-ai-products.txt` lines 249-309 |
| AU-AI-REQ-021 | OFFICIAL information with GenAI requires PSPF-assessed access, approved provider controls or FOCI assessment, training, and technology authorisation process. | `pspf-policy-advisory-gen-ai-2025.txt` lines 23-60 |
| AU-AI-REQ-022 | DTA policy contains a defence/national-intelligence carveout; defence pathway must not fabricate non-public obligations. | `dta-policy-responsible-ai-gov-v2.txt` lines 197-202 |

## Source-gap log

| Gap ID | Description | Impact |
|---|---|---|
| SG-001 | No public Defence-wide equivalent to UK JSP 936 identified in corpus. | Defence template uses AU public-source baseline + explicit internal-policy TODOs. |
| SG-002 | BuyICT AI procurement page is JS-rendered; detailed static extraction incomplete. | Procurement controls rely on available DTA/Finance/OAIC public evidence, with TODO for organisation-specific procurement implementation detail. |
