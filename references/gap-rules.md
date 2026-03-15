# SPCC Plan Gap Rules

Reference for Phase 4 of the SPCC Plan Drafter skill.
Apply EVERY check below. Insert a ⚠️ GAP flag inline in the draft wherever a check fails.

**Gap flag format:**
```
⚠️ GAP [Section X.X]: [What is missing or non-compliant]
Required by: [40 CFR §XXX]
Action needed: [Specific step to resolve before plan is finalized]
```

Severity levels (include in each flag):
- 🔴 CRITICAL — Plan cannot be certified until resolved; regulatory violation
- 🟡 IMPORTANT — Must be resolved before plan is operational; may not be a current violation
- 🔵 RECOMMENDED — Best practice; not strictly required but strongly advisable

---

## Section 1 — Facility Description Gaps

| Check | Condition | Severity |
|-------|-----------|----------|
| Missing SPCC coordinator | No designated coordinator named | 🔴 CRITICAL |
| Missing owner/operator contact | Phone or email not provided | 🟡 IMPORTANT |
| Tier determination not documented | Tier was inferred but not formally stated with capacity figures | 🟡 IMPORTANT |
| Plan history unknown | Prior plans existed but date/certification status unknown | 🟡 IMPORTANT |
| No SIC code or business description | Cannot assess facility type-specific requirements | 🔵 RECOMMENDED |

---

## Section 2 — Oil Storage Inventory Gaps

| Check | Condition | Severity |
|-------|-----------|----------|
| Container capacity unknown | Any container listed with unknown or estimated capacity | 🔴 CRITICAL |
| Oil type unspecified | Contents listed as "oil" without specificity | 🟡 IMPORTANT |
| Container age unknown for ASTs | Age unknown and no integrity test on record | 🟡 IMPORTANT |
| Mobile containers not bounded | Portable drums/totes stored without defined max quantity or location | 🟡 IMPORTANT |
| Transformer dielectric fluid type unknown | Cannot assess PCB status or volume | 🔴 CRITICAL |
| PCB status unconfirmed for transformers | Dielectric fluid not confirmed as non-PCB | 🔴 CRITICAL |
| No site map to verify inventory | No map provided or referenced | 🟡 IMPORTANT |

---

## Section 3 — Drainage and Discharge Prediction Gaps

| Check | Condition | Severity |
|-------|-----------|----------|
| Nearest water body not identified | User unable to name nearby water body | 🔴 CRITICAL |
| Distance to water body unknown | Cannot assess discharge risk | 🟡 IMPORTANT |
| Drainage pathway not described | Unknown where site runoff flows | 🔴 CRITICAL |
| No worst-case discharge calculation | Volume and direction of worst-case spill not estimated | 🔴 CRITICAL |
| Site map not available | Cannot confirm discharge pathways | 🟡 IMPORTANT |
| Floor drains exist with unknown destination | Drain outlet not identified | 🔴 CRITICAL |

---

## Section 4 — Secondary Containment Gaps

| Check | Condition | Severity |
|-------|-----------|----------|
| Containment capacity < 110% of largest container | Fails §112.7(c) minimum standard | 🔴 CRITICAL |
| No secondary containment and no impracticability claim | Container has no containment and no documented basis for exception | 🔴 CRITICAL |
| Impracticability claim without documentation | Claim made but basis not described | 🔴 CRITICAL |
| Impracticability claim without equivalent measures | No alternate protection described | 🔴 CRITICAL |
| Containment drain valve normally open | Valve left open allows uncontrolled discharge | 🔴 CRITICAL |
| Containment condition unknown or poor | Material condition not assessed | 🟡 IMPORTANT |
| Open containment with no stormwater management | Precipitation accumulates with no removal procedure | 🟡 IMPORTANT |
| Portable containment for fixed operations | Temporary drip trays used instead of permanent containment without justification | 🟡 IMPORTANT |

---

## Section 5 — Container Inspection and Integrity Gaps

| Check | Condition | Severity |
|-------|-----------|----------|
| No integrity test on record for ASTs ≥ 660 gal | No API 653 or equivalent test documented | 🔴 CRITICAL |
| Integrity test overdue | Last test > 10 years ago (or per API 653 interval) without justification | 🔴 CRITICAL |
| No overfill protection on ASTs | No high-level alarm, automatic shutoff, or equivalent | 🔴 CRITICAL |
| No inspection frequency established | Containers not being inspected on a schedule | 🔴 CRITICAL |
| Inspection records not maintained | No log or records system described | 🟡 IMPORTANT |
| Known leaks or staining not addressed | Visual evidence of prior leaks without corrective action documented | 🔴 CRITICAL |
| No leak detection for buried piping | Underground transfer lines have no monitoring | 🔴 CRITICAL |
| No cathodic protection on buried metallic piping | Corrosion risk not mitigated | 🔴 CRITICAL |
| Brittle fracture evaluation not performed | Field-constructed or relocated AST with no evaluation on record | 🟡 IMPORTANT |
| Container material incompatible with product | Compatibility concern noted (e.g., fiberglass with certain solvents) | 🔴 CRITICAL |

---

## Section 6 — Transfer Operations Gaps

| Check | Condition | Severity |
|-------|-----------|----------|
| No drip containment at transfer points | Transfers performed without any catch capability | 🔴 CRITICAL |
| Transfer procedures not documented | No written procedure for loading/unloading | 🟡 IMPORTANT |
| Hoses and fittings not inspected before use | No pre-transfer inspection step | 🟡 IMPORTANT |
| Valves unlabeled | Shutoff valves not clearly identified | 🟡 IMPORTANT |
| Cathodic protection not tested | CP system present but test date unknown | 🟡 IMPORTANT |
| Buried piping age > 20 years without assessment | High corrosion risk with no documented evaluation | 🔴 CRITICAL |

---

## Section 7 — Drainage Management Gaps

| Check | Condition | Severity |
|-------|-----------|----------|
| No procedure for testing contained liquid before draining | Contaminated stormwater could be released | 🔴 CRITICAL |
| Oil-water separator present but not maintained | No maintenance record or frequency | 🟡 IMPORTANT |
| Retention pond capacity unknown | Cannot confirm it handles design storm | 🟡 IMPORTANT |
| Contaminated water disposal method unknown | No procedure for removing oil-contaminated water | 🔴 CRITICAL |

---

## Section 8 — Security Gaps

| Check | Condition | Severity |
|-------|-----------|----------|
| Facility not fenced or perimeter security absent | No physical barrier preventing unauthorized access | 🟡 IMPORTANT |
| Pump starters not secured | Equipment can be activated by unauthorized persons | 🟡 IMPORTANT |
| No warning signs at storage areas | Required signage absent | 🔵 RECOMMENDED |
| No protocol for unattended facility | No documented procedure for securing site when unstaffed | 🟡 IMPORTANT |

---

## Section 9 — Personnel and Training Gaps

| Check | Condition | Severity |
|-------|-----------|----------|
| No designated SPCC coordinator | Required role not assigned | 🔴 CRITICAL |
| No training program | Personnel handling oil receive no spill prevention training | 🔴 CRITICAL |
| Training records not maintained | Cannot demonstrate compliance | 🟡 IMPORTANT |
| National Response Center number not posted | Key emergency contact not available at point of need | 🟡 IMPORTANT |
| No spill response contractor under agreement | No pre-arranged cleanup capability | 🟡 IMPORTANT |
| No spill response equipment on site | Nothing to deploy in a spill event | 🟡 IMPORTANT |
| Emergency contact list not posted at storage areas | Information not accessible when needed | 🟡 IMPORTANT |

---

## Section 10 — Spill Response Gaps

| Check | Condition | Severity |
|-------|-----------|----------|
| Response procedures not documented in writing | Verbal procedures only | 🟡 IMPORTANT |
| Reporting thresholds not communicated to staff | Employees unsure when to report | 🔴 CRITICAL |
| No spill incident report form | No formal record-keeping mechanism | 🟡 IMPORTANT |
| No post-spill amendment procedure | Plan does not address how discharges trigger plan review | 🟡 IMPORTANT |

---

## Section 11 — Spill History Gaps

| Check | Condition | Severity |
|-------|-----------|----------|
| Spill history unknown or unverified | Cannot complete tier determination or compliance history | 🔴 CRITICAL |
| Past qualifying discharge not reported | Discharge to navigable waters was not reported to NRC | 🔴 CRITICAL |
| Past discharge not incorporated into plan | Corrective actions not described | 🟡 IMPORTANT |

---

## Section 12 — Amendment and Review Gaps

| Check | Condition | Severity |
|-------|-----------|----------|
| Plan has never been reviewed | Existing plan with unknown review history | 🟡 IMPORTANT |
| Last PE certification > 5 years ago | Plan overdue for re-certification (§112.5(b)) | 🔴 CRITICAL |
| Recent facility changes not reflected in plan | Known changes made without amending plan | 🔴 CRITICAL |
| No amendment log | Cannot track plan history | 🔵 RECOMMENDED |

---

## Section 13 — Certification Gaps

| Check | Condition | Severity |
|-------|-----------|----------|
| PE not identified for Full Plan | Plan ready for PE review but no PE named | 🟡 IMPORTANT |
| Qualified Facility eligibility uncertain | Spill history data incomplete — tier may be wrong | 🔴 CRITICAL |
| Owner/operator signatory not identified | Cannot complete certification block | 🟡 IMPORTANT |

---

## Appendix Gaps

| Check | Condition | Severity |
|-------|-----------|----------|
| No site map provided or referenced | Cannot verify layout, containment, or drainage claims | 🟡 IMPORTANT |
| Site map present but storage areas not labeled | Map is not plan-specific | 🟡 IMPORTANT |
| No inspection log template | Inspection program has no recording tool | 🔵 RECOMMENDED |
| No training record template | Training compliance cannot be documented | 🔵 RECOMMENDED |

---

## End-of-Draft Gap Summary

After completing all sections, generate a summary table at the end of the document:

**Title: COMPLIANCE GAP SUMMARY — Action Required Before Plan Finalization**

| # | Section | Gap Description | Severity | Status |
|---|---------|----------------|----------|--------|
| 1 | [X.X] | [Description] | 🔴/🟡/🔵 | Open |

Count totals:
- 🔴 CRITICAL gaps: ___
- 🟡 IMPORTANT gaps: ___
- 🔵 RECOMMENDED gaps: ___

Include a note: "This plan draft contains [N] critical gaps that must be resolved before
this plan can be certified and implemented. Items marked 🔴 CRITICAL represent potential
regulatory violations under 40 CFR Part 112 if left unresolved."