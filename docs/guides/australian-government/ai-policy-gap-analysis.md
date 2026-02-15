# AU AI Policy Gap Analysis (vs UK AI Policy Surfaces)

Scope: AI-only policy corpus and UK→AU mapping for backlog items **AI-003 to AI-006**.

## 1) Confirmed No-Equivalent Gaps

These items were **not identified as direct AU federal equivalents** in the collected official corpus.

1. **Single UK-style AI Playbook artefact**
   - UK has one named AI Playbook; AU equivalent is distributed across DTA policy, DTA technical standard, Finance assurance framework, OAIC privacy guidance, and ACSC/PSPF security sources.

2. **ATRS central hub equivalent**
   - AU has a transparency standard (DTA Standard for AI transparency statements 2.0), but no equivalent central whole-of-government ATRS-hub publication model was identified in collected sources.

3. **Cyber Essentials certification equivalent**
   - AU baseline controls are ISM/Essential Eight/PSPF-based. A direct certification analogue to UK Cyber Essentials for this use was not identified in collected policy corpus.

4. **NCSC CAF direct equivalent**
   - Control intent can be covered by ISM + PSPF + assurance processes, but a direct CAF-equivalent AU framework was not identified in this corpus.

5. **Federal EqIA-style process equivalent**
   - Fairness/contestability are covered in AU AI policy/assessment materials, but a direct UK-style equality impact assessment process equivalent was not found.

6. **Mandatory model-card/datasheet requirement**
   - Not identified as an explicit mandatory whole-of-government requirement in collected AU official sources.

7. **Defence-wide current AI policy equivalent to UK MOD JSP 936** (optional/sector-specific)
   - No current, publicly discoverable Defence-wide policy equivalent was found in official Defence sitemap-discoverable paths during this pass.

## 2) Material Differences (AU ≠ UK Even Where Functionally Similar)

1. **Privacy law baseline differs materially**
   - UK references GDPR/DPIA language; AU uses Privacy Act 1988 + APP Guidelines + OAIC guidance.

2. **Transparency artefact shape differs**
   - UK naming: ATRS.
   - AU naming: AI transparency statement standard and agency transparency statements.

3. **AI assurance architecture differs**
   - UK practice often combines AI Playbook + spend/service controls.
   - AU structure combines DTA policy/technical controls + Finance AI assurance framework + procurement/assurance process guidance.

4. **Security architecture differs**
   - UK secure-by-design references (NCSC/Cyber Essentials/CAF) do not map 1:1.
   - AU stack is ACSC AI guidance + ISM + PSPF directions/advisories.

5. **Procurement route mechanics differ**
   - UK Digital Marketplace route names (G-Cloud/DOS) are UK-specific.
   - AU routeing is CPR + BuyICT + WofG procurement mechanisms.

## 3) Source Availability / Access Gaps (Evidence Limitations)

1. **BuyICT AI procurement guidance page is JS-rendered**
   - URL captured: `https://www.buyict.gov.au/sp?id=resources_and_policies&kb=KB0010685`
   - Static retrieval produced a minimal shell page only; full content may require interactive/browser rendering or authenticated context.

2. **Defence AI policy discovery limitation**
   - Defence sitemap and common canonical paths did not reveal a current Defence-wide policy counterpart during this pass.
   - Marked as unresolved optional/sector-specific gap pending Defence-specific pathway requirements.

## 4) Practical Rewrite Implications for Later Phases

- Treat UK references to **ATRS, AI Playbook, GDPR DPIA, NCSC CAF, Cyber Essentials, JSP 936** as:
  - **Replace** where AU equivalent exists,
  - **Delete** where UK-specific and no AU requirement exists,
  - **No-equivalent** where only partial AU analogues exist.
- Add AU-specific mandatory anchors:
  - DTA AI policy suite,
  - Finance national AI assurance framework + CPR,
  - OAIC APP/PIA/NDB guidance,
  - Legislation anchors (Privacy Act + administrative law acts + FOI Act),
  - ACSC/ISM + PSPF AI advisory controls.
