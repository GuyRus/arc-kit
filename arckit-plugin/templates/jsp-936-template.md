# AU Defence AI Assurance Pathway (Public-source baseline)

> **Template Status**: Transitional | **Version**: [VERSION] | **Command**: `/arckit.jsp-936`

## Important scope note

No current publicly discoverable Australian Defence-wide equivalent to UK MOD JSP 936 was identified in the AU policy corpus used for this rewrite.

This template therefore provides a **public-source AU baseline pathway** for Defence-adjacent teams and flags explicit source gaps for internal Defence policy overlays.

## 1. Policy context (public sources)

| Topic | Public source anchor | Implication |
|---|---|---|
| AI policy carveout for defence portfolio | DTA AI policy v2.0 – national security carveouts | DTA whole-of-government AI policy does not apply directly to defence use, but can be voluntarily adopted where suitable. |
| OFFICIAL information with GenAI | PSPF Policy Advisory 001-2025 | Defines approved provider pathways, staff training expectations, and PSPF authorisation requirements. |
| Secure AI system development practices | ACSC AI secure design guidance | Provides secure lifecycle controls for design, development, deployment, and operations. |
| Information security baselines | ISM + PSPF references in technical standard | Security controls and authorisation pathways remain mandatory in relevant contexts. |

## 2. Defence-specific assurance tailoring (required internal overlay)

| Required internal input | Public-source status | Action |
|---|---|---|
| Defence AI risk taxonomy and risk appetite | SOURCE_GAP | Obtain current internal Defence policy and map to this template. |
| Defence authority/approval chain for AI capability release | SOURCE_GAP | Define governance route and accountable approvers. |
| Defence-specific ethical review or assurance board process | SOURCE_GAP | Document board TOR, review cadence, and evidence requirements. |
| Defence incident and reporting policy for AI harms | SOURCE_GAP | Align with Defence cyber/operational incident doctrine. |

## 3. Minimum public-source assurance package

- [ ] Use case profile and operational context documented.
- [ ] Data classification and handling rules documented.
- [ ] AI risk assessment completed (adapted from AU AIA method where feasible).
- [ ] Security controls and authorisation evidence captured (PSPF/ISM aligned).
- [ ] Human oversight model documented (intervention/disengagement).
- [ ] Monitoring, incident response, and re-validation plan documented.
- [ ] Decommissioning and records retention approach documented.

## 4. Risk and governance record

| Item | Status | Evidence |
|---|---|---|
| Approval authority identified | [ ] | [ ] |
| Governance board pathway identified | [ ] | [ ] |
| High-risk escalation pathway defined | [ ] | [ ] |
| Internal policy dependencies captured | [ ] | [ ] |

## 5. Source gaps and TODO register

| Gap | Why it matters | Owner | Due date |
|---|---|---|---|
| [SOURCE_GAP] | [Text] | [Name] | [Date] |

## 6. Legacy UK reference (read-only)

If a project explicitly requires historical UK JSP 936 structure for comparison/migration, use:

- `.arckit/templates/legacy-uk/jsp-936-template.md`

This is a **legacy reference only**, not an AU default artifact.
