---
name: spcc-plan
description: >
  Draft a complete Spill Prevention, Control, and Countermeasure (SPCC) Plan as a Word (.docx)
  document, fully structured to 40 CFR Part 112. Use this skill whenever a user asks to create,
  draft, generate, or update an SPCC plan, Oil Spill Prevention Plan, spill prevention plan, or
  references Part 112 compliance. Also trigger when a user provides facility oil storage
  information and asks for a compliance document, environmental plan, or EPA-required plan.
  The skill interviews the user to collect all site-specific data, determines the correct
  regulatory tier (Tier I QF, Tier II QF, or Full PE-Certified Plan), drafts the complete plan,
  and flags inline any gaps or deficiencies that need to be resolved before finalization.
---

# SPCC Plan Drafter

This skill produces a complete, site-specific SPCC Plan as a Word document conforming to
40 CFR Part 112. It handles all facility types and all storage configurations:
ASTs, drums/portable containers, transformers/electrical equipment, day tanks, bulk transfer
areas, and USTs (if co-located with aboveground storage that triggers SPCC).

---

## How This Skill Works

Execute the following phases in order. Do not skip phases or combine them.

### Phase 1 — Intake: Assess What the User Has Provided

Before asking any questions, check the conversation for existing information:
- Has the user uploaded a document or site survey? Extract all relevant data from it first.
- Has the user pasted notes or described the site? Pull out any facts already stated.
- Only ask for information that is genuinely missing after this extraction.

Tell the user: "I'll gather the site-specific information needed to draft your SPCC plan.
Some of these questions have multiple parts — answer what you know and mark anything
uncertain with a '?' so I can flag it for follow-up."

### Phase 2 — Interview: Collect Site-Specific Data

Ask questions in the groups below. You may ask multiple groups at once to reduce back-and-forth,
but keep each group clearly labeled. For a full reference of all questions with sub-questions and
acceptable answer formats, read: `references/interview-questions.md`

**Group A — Facility Identity** (always ask)
**Group B — Oil Storage Inventory** (always ask; one row per container)
**Group C — Secondary Containment** (always ask)
**Group D — Discharge Pathway & Water Proximity** (always ask)
**Group E — Operations & Transfer** (always ask)
**Group F — Inspection & Maintenance History** (always ask)
**Group G — Security** (always ask)
**Group H — Personnel & Training** (always ask)
**Group I — Spill & Incident History** (always ask — required for tier determination)

### Phase 3 — Tier Determination

After the interview, determine the correct plan tier. Apply this logic exactly:

```
STEP 1 — Does SPCC apply?
  If total aboveground oil storage < 1,320 gal AND no single container > 660 gal:
    → SPCC does NOT apply. Inform user and stop.
  Otherwise → SPCC applies. Continue.

STEP 2 — Check Tier I Qualified Facility eligibility (§112.3(g)(1))
  ALL of the following must be true:
    a) Total aboveground oil storage ≤ 10,000 gallons
    b) No single discharge to navigable waters or adjoining shorelines
       exceeding 1,000 gallons in past 3 years
    c) No two discharges each > 42 gallons in any 12-month period in past 3 years
    d) Facility is not a petroleum refinery, oil production facility, or
       pipeline facility subject to separate Part 112 sections
  If ALL true → Tier I QF (self-certified, streamlined plan)

STEP 3 — Check Tier II Qualified Facility eligibility (§112.3(g)(2))
  ALL of the following must be true:
    a) Total aboveground oil storage ≤ 10,000 gallons
    b) Meets discharge history requirements (b) and (c) above
    c) Facility has implemented one or more deviations from Tier I requirements
       (e.g., impracticability claims, alternative secondary containment)
  If ALL true → Tier II QF (PE not required but must detail deviations)

STEP 4 — Full Plan
  If none of the above → Full PE-Certified Plan required (§112.3(d))
```

Inform the user of the determined tier and explain what it means for certification
and inspection requirements before proceeding.

### Phase 4 — Draft the Plan

Read `references/plan-template.md` for the full section-by-section structure,
required content, and exact regulatory citations for each section.

Draft all sections in order. For each section:
- Use site-specific data collected in Phase 2
- Include the correct 40 CFR Part 112 citation for each requirement
- For Tier I/II, use the streamlined §112.6/§112.7 checklist format where applicable
- For Full Plans, use the complete narrative format

**Inline Gap Flags**: Whenever a required element cannot be completed because data is
missing, uncertain, or inconsistent, insert a clearly visible flag directly in the
draft text using this format:

  ⚠️ GAP [Section X.X]: [Description of what is missing or problematic]
  Required by: [CFR citation]
  Action needed: [Specific step the user must take to resolve]

Read `references/gap-rules.md` for the complete list of required gap checks,
organized by section. Apply every check. Do not skip any.

### Phase 5 — Produce the Word Document

After drafting all sections, produce the final .docx file using the docx skill.
Read `/mnt/skills/public/docx/SKILL.md` for technical instructions on generating
the Word document.

**Formatting requirements for the SPCC plan document:**
- Cover page: Facility name, address, plan date, revision number, preparer name/title
- Table of contents (auto-generated)
- Section numbering matching the plan template exactly
- Footer: "SPCC Plan — [Facility Name] — CONFIDENTIAL — Rev. [X] — [Date]"
- Header: 40 CFR Part 112 citation for the current section
- Page numbers
- Gap flags formatted as highlighted text (yellow highlight, bold) so they stand out
- Certification signature blocks at end (PE block if Full Plan; Owner/Operator block for QF)
- Document properties: title, author, subject = "SPCC Plan"

### Phase 6 — Deliver & Summarize

After producing the .docx file:
1. Present the file to the user
2. Provide a short summary including:
   - Tier determined and why
   - Total number of ⚠️ GAP flags and the most critical ones
   - Next steps (PE review, training records, inspection schedule, etc.)
   - Reminder that SPCC plans must be reviewed/amended every 5 years or after
     any change in facility configuration (§112.5)

---

## Reference Files

| File | When to Read |
|------|-------------|
| `references/interview-questions.md` | Phase 2 — full question list with sub-questions |
| `references/plan-template.md` | Phase 4 — section-by-section plan structure and required content |
| `references/gap-rules.md` | Phase 4 — complete gap-checking rules by section |

---

## Key Regulatory Notes

- **Applicability threshold**: Aboveground storage ≥ 1,320 gal total OR any single container ≥ 660 gal (§112.1(d)(2)(ii))
- **PE certification**: Required for Full Plans; must be a licensed PE in the state where the facility is located (§112.3(d))
- **Amendment trigger**: Any change in facility design, construction, operation, or maintenance that materially affects the potential for discharge (§112.5(a))
- **5-year review**: All plans must be reviewed and re-certified every 5 years (§112.5(b))
- **Record retention**: Inspection logs, discharge reports, training records — minimum 3 years (§112.7(e)(8))
- **USTs**: USTs are generally excluded from SPCC, but if co-located with aboveground storage, the aboveground storage determines applicability; note USTs in the facility description
- **Transformers**: Oil-filled transformers count toward total oil storage volume; include dielectric fluid type and volume