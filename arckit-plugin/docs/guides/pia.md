# Privacy Impact Assessment (PIA) Guide (via `/arckit.pia`)

`/arckit.pia` produces an OAIC-aligned **Privacy Impact Assessment (PIA)** report for projects that handle personal information under the **Privacy Act 1988** and the **Australian Privacy Principles (APPs)**.

ArcKit’s PIA structure follows the OAIC PIA Guide’s 10-step flow (threshold → plan → describe → consult → flows → compliance → risks → recommendations → report → respond/review) and is designed to surface concrete design actions (not just headings).

## Inputs (What You Need Before You Run It)

| Artefact | Why it matters |
|----------|----------------|
| `ARC-<id>-DATA-v*.md` (data model) | Source of truth for *what* personal/sensitive information is handled, where it flows, retention/disposal approach (APP 11.3), and overseas disclosure/access patterns (APP 8). |
| `ARC-<id>-REQ-v*.md` (requirements) | Purposes and decision impacts (including eligibility/entitlements/sanctions), disclosure needs, and constraints that drive privacy risk. |
| `ARC-<id>-STKE-v*.md` (stakeholders) | Identifies individuals affected, vulnerable groups, power imbalance, and who must be consulted/sign off. |
| `ARC-<id>-SECD-v*.md` (secure by design) | Seeds APP 11 security controls and operational safeguards. |
| `ARC-<id>-RISK-v*.md` (risk register) | Existing risks/controls; helps trace privacy risks into the broader project risk posture. |
| Vendor/contract artefacts (if outsourcing) | Needed to evidence “reasonable steps” for cross-border disclosure controls (APP 8) and supplier privacy/security controls. |

## When to Run a PIA (Threshold Assessment)

PIAs are strongly recommended whenever a project handles personal information. Prioritise a PIA (and expect it to be comprehensive) when the project includes:
- Sensitive information (Privacy Act s 6(1)) or high-consequence domains (health, benefits, law enforcement, etc.)
- Large volume, aggregation, or a new central dataset
- Cross-entity sharing, matching, or unexpected secondary uses
- Outsourcing (including overseas hosting/support) or novel technology (AI/ML, biometrics, pervasive monitoring)
- Compulsory provision of information, or decisions that can materially affect individuals
- Power imbalance (government–citizen, employer–employee) or vulnerable groups

## Command

```bash
/arckit.pia Generate PIA for <project>
```

Output: `projects/<id>/ARC-<id>-PIA-vX.Y.md`

## What the Output Covers (At a Glance)

The generated PIA report includes:
- Threshold assessment and scope
- PIA plan (roles, evidence, milestones)
- Project description and affected individuals
- Consultation record (internal/external, proportionate to risk)
- End-to-end information flows (collection → storage → use → disclosure → retention → disposal/de-identification)
- APP compliance matrix (including APP 8 cross-border disclosure and APP 11 security/disposal)
- Notifiable Data Breaches (NDB) readiness (including the 30-day assessment window and notification “as soon as practicable” if eligible)
- Privacy risks framed as impacts on individuals (with `PIA-###` risk IDs), mitigations, and residual risk
- Recommendations/action plan, sign-off, and review triggers

## How to Use It (Practical Flow)

```text
1. Ensure prerequisites exist (data model + requirements + stakeholders; security and vendor artefacts where relevant)
2. Run /arckit.pia
3. Validate the content with privacy, security, records/IM, legal/policy, and the service owner:
   - Are purposes, data categories, and disclosures correct?
   - Are APP gaps explicit and turned into actions with owners?
   - Are cross-border disclosures (APP 8) and retention/disposal (APP 11.3) evidence-based?
4. Push actions into delivery tracking (backlog/assurance tracker) and link them to risks
5. Re-run after major design changes, new vendors, new data flows, or incidents
```

## Linkages

- Feed recommendation actions into `/arckit.risk` and (if used) `/arckit.servicenow`.
- If AI is in scope, cross-reference `/arckit.ai-playbook` and ensure any agency AI impact assessment requirements are met.
- Store signed PIAs with an explicit review cadence and update the PIA when processing changes.
