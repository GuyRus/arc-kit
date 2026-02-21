# Data Model Quick Guide

`/arckit.data-model` transforms Data Requirements (DR-xxx) into an ERD, governance catalogue, and Privacy Act 1988 / APPs compliance pack.

---

## Inputs Checklist

| Artefact | Purpose |
|----------|---------|
| `ARC-<id>-REQ-v1.0.md` with DR-xxx entries | Defines entities and attributes |
| Up-to-date stakeholders & risk register | Drives governance roles and retention risk |
| Latest architecture diagrams | Populate CRUD matrix and integrations |

---

## Command

```bash
/arckit.data-model Create data model for <project name>
```

Output: `projects/<id>/ARC-<id>-DATA-v1.0.md`

---

## Deliverable Snapshot

| Section | Highlights | Next Action |
|---------|------------|-------------|
| Mermaid ERD | Normalised entity diagram ready for mermaid.live | Share with architects for validation |
| Entity catalogue | Attributes, data types, keys, derived fields | Flag unknown data types for modelling session |
| Privacy/APP pack | Personal/sensitive info inventory, APP 8/11/12/13 mapping, retention/disposal, NDB readiness | Review with privacy officer; schedule PIA if high risk |
| Governance matrix | Owner, steward, custodian, classification | Update RACI and onboarding materials |
| CRUD & integrations | Component ↔ entity access + upstream/downstream feeds | Align with API contracts and ETL plans |
| Data quality | KPIs, controls, monitoring cadence | Feed into ServiceNow service design |

---

## Compliance Focus

- **Identify PII** – mark direct/indirect PII in the catalogue.
- **Retention** – confirm duration against organisation policy.
- **Security** – ensure encryption/segmentation controls align with risk appetite.
- **Access & correction** – validate mechanism for APP 12/13 (and FOI for agencies).
- **Disposal** – validate APP 11.3 destruction/de-identification workflow (and Archives/records constraints).

Use the output to enrich `/arckit.dpia` (privacy impact assessment pack).

---

## Review Tips

- Run the command whenever requirements change materially.
- Ask data stewards to sign off catalogue rows before build.
- Store diagrams alongside other architecture artefacts for audit trails.

---

## Related Commands

- `/arckit.dpia` - Generate privacy impact assessment (PIA) pack (auto-references data model)
- `/arckit.data-mesh-contract` - Create federated data product contracts from entities (mesh architecture)
- `/arckit.traceability` - Link entities to requirements and test cases
