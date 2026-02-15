# MLOps Strategy (AU AI Governance Integrated)

> **Template Status**: Experimental | **Version**: [VERSION] | **Command**: `/arckit.mlops`

## Document Control

| Field | Value |
|---|---|
| Document ID | ARC-[PROJECT_ID]-MLOP-v[VERSION] |
| Project | [PROJECT_NAME] |
| Owner | [OWNER_NAME_AND_ROLE] |
| Last Modified | [YYYY-MM-DD] |
| Review Date | [YYYY-MM-DD] |

## 1. ML System Overview

- Business outcome and service context
- Model inventory (classification/regression/LLM etc.)
- Operational criticality and user impact

## 2. Data and Feature Lifecycle

- Source systems and data contracts
- Data quality controls and lineage
- Privacy and classification controls
- Feature engineering and versioning

## 3. Model Development and Evaluation

- Training pipelines and experiment tracking
- Model validation criteria (accuracy + robustness + fairness)
- Output safety constraints and exclusion conditions

## 4. Release and Deployment

- Promotion gates (dev/stage/prod)
- Release controls, rollback, and approvals
- Human oversight model in production

## 5. Monitoring and Operations

| Monitoring domain | Minimum control | Evidence |
|---|---|---|
| Performance and drift | Thresholds + alerting + retraining trigger | [Link] |
| Safety | Harmful/unreliable outputs monitored | [Link] |
| Security | DLP, access controls, anomaly monitoring | [Link] |
| Transparency | Explanation and disclosure quality checks | [Link] |
| Compliance | Policy and legal control checks | [Link] |

## 6. Responsible AI and AU Compliance Integration

Link this strategy to AU AI artifacts:

- `ARC-[PROJECT_ID]-AIGA-v[VERSION].md` (governance assessment)
- `ARC-[PROJECT_ID]-AIIA-v[VERSION].md` (impact assessment)
- `ARC-[PROJECT_ID]-AITS-v[VERSION].md` (transparency statement)
- `ARC-[PROJECT_ID]-AIUR-v[VERSION].md` (use case register)
- `ARC-[PROJECT_ID]-AIGC-v[VERSION].md` (governance checklist)

## 7. Incident Management and Re-validation

- AI incident severity model
- Escalation pathways
- Re-validation triggers (material scope/usage/operation changes)

## 8. Decommissioning

- Retirement criteria and stakeholder communications
- Data/model/infrastructure shutdown and retention controls
- Lessons learned and final compliance record

## 9. Delivery Roadmap

| Milestone | Owner | Date | Dependency |
|---|---|---|---|
| [Milestone] | [Owner] | [Date] | [Dependency] |
