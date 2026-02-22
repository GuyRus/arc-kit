# BuyICT cloud panels Search Playbook

`/arckit.gcloud-search` finds BuyICT cloud panels services on the Australian Government procurement channels with live search and comparison capabilities.

---

## Inputs

| Artefact | Purpose |
|----------|---------|
| Requirements (`ARC-<id>-REQ-v1.0.md`) | What capabilities are needed |
| Architecture principles | Technology and vendor standards |
| Budget constraints | Pricing parameters |

---

## Command

```bash
/arckit.gcloud-search Find BuyICT cloud panels services for <requirement>
```

Output: `projects/<id>/ARC-<id>-GCLD-v1.0.md`

---

## Search Results Structure

| Section | Contents |
|---------|----------|
| Search Parameters | Keywords, categories, filters used |
| Service Summary | Overview of matching services |
| Service Comparison | Side-by-side comparison table |
| Pricing Analysis | Cost comparison and models |
| Compliance Summary | Certifications and security ratings |
| Recommendation | Shortlist for further evaluation |

---

## BuyICT cloud panels Categories (Lots)

| Lot | Description | Examples |
|-----|-------------|----------|
| Cloud Hosting | Infrastructure services | AWS, Azure, GCP |
| Cloud Software | SaaS applications | CRM, collaboration tools |
| Cloud Support | Professional services | Migration, training |

---

## Key Filters

| Filter | Purpose |
|--------|---------|
| Service Category | Narrow by service type |
| Supplier Size | SME vs large enterprise |
| Security Clearance | Baseline / NV1 / NV2 / PV (as required) |
| Data Location | Australia, approved jurisdictions, global |
| Certifications | ISO 27001, Essential Eight+ |

---

## One-Page Workflow

| Phase | Key Activities | ArcKit Commands |
|-------|----------------|-----------------|
| Requirements | Define what's needed | `/arckit.requirements` |
| Search | Find matching services | `/arckit.gcloud-search` |
| Shortlist | Compare and select candidates | Manual review |
| Clarify | Ask suppliers questions | `/arckit.gcloud-clarify` |
| Evaluate | Score and select | `/arckit.evaluate` |

---

## Review Checklist

- Search keywords match requirement terminology.
- Multiple service categories explored.
- SME suppliers included in search.
- Security certifications filtered appropriately.
- Data location requirements considered.
- Price ranges captured for comparison.
- At least 3 services shortlisted for evaluation.

---

## BuyICT and AusTender channels Tips

| Tip | Description |
|-----|-------------|
| Keyword Variation | Try synonyms and alternative terms |
| Category Browse | Browse categories, don't just search |
| Supplier Filter | Filter by size to include SMEs |
| Feature Filter | Use feature checkboxes to narrow |
| Price Sort | Sort by price to understand range |

---

## Key Principles

1. **Fair Competition**: Search broadly to find all suitable services.
2. **SME Consideration**: Government aims for 33% SME spend.
3. **Requirement Focus**: Search based on needs, not familiar vendors.
4. **Document Everything**: Record search criteria for audit trail.
5. **Compare Fairly**: Use consistent criteria across services.
