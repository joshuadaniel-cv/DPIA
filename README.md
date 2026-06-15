# CV DPIA Tool — Data Protection Impact Assessment

## Introduction

A **Data Protection Impact Assessment (DPIA)** is a systematic process for identifying and minimizing data protection risks before you process personal data at scale. It's a legal requirement under **GDPR Article 35** for high-risk processing activities.

CV Global is committed to protecting personal privacy and data security. This tool helps teams at CV Global (and partner organizations) systematically analyze their data processing activities and embed privacy and security controls **from the start** — not as an afterthought.

### Why DPIA Matters

- **Legal requirement**: GDPR Article 35 mandates DPIAs for certain processing activities
- **Risk mitigation**: Identifies threats to confidentiality, integrity, and availability early
- **Better decisions**: Integrates privacy and security findings back into project planning
- **Ongoing process**: Not a one-time box-tick; should be reviewed and updated as processing evolves

---

## The Data Governance Workflow

DPIA is one critical step in CV Global's integrated data governance process:

```
┌─────────────┐    ┌──────────────┐    ┌──────────────┐    ┌──────────────┐
│  Add Source │ ─→ │  Classifier  │ ─→ │    DPIA      │ ─→ │    ROPA      │
│   (Metadata)│    │ (CIA + GDPR) │    │  (7 Steps)   │    │   (Records)  │
└─────────────┘    └──────────────┘    └──────────────┘    └──────────────┘
```

- **Add Source**: Register your data source and basic metadata
- **Classifier**: Assess confidentiality, integrity, availability, and GDPR categories
- **DPIA** (this tool): Work through the 7-step impact assessment
- **ROPA**: Record the outcome in your Record of Processing Activities

---

## What This Tool Does

The DPIA tool is a **semi-automated, guided form** that:

1. **Pre-fills** relevant data from your Add Source submission and Classifier results
2. **Guides you** through the 7-step ICO DPIA template aligned to GDPR Article 35
3. **Allows editing** at every step — your circumstances may require adjustments
4. **Tracks progress** visually so you know where you are in the assessment
5. **Facilitates sign-off** with clear approval workflows for Data Protection Officers (DPOs) and business owners

No coding required. No special software. Just a modern web browser.

---

## Before You Start: Add Source & Run Classifier

The DPIA tool works best when you've already completed two upstream steps:

### 1. Add Source Form

This separate form captures metadata about your data source:

| Field | Example | Used in DPIA |
|-------|---------|-------------|
| **Managing Group** | Data & Insights, Privacy | Step 1: Controller details |
| **Source Name** | Employee Payroll System | Step 2: Processing description |
| **Type of Source** | Database, API, File Share | Step 2: Processing description |
| **Unique Source ID** | SRC-2024-0042 | Step 7: Audit trail |
| **Source URL** | https://payroll.internal | Step 2: Technical details |
| **Source Owner / SPoC Email** | john.doe@cvglobal.co | Step 1: Responsible person |
| **Permission Granted?** | Yes / No | Step 4: Lawful basis |
| **Contains PII?** | Yes / No | Step 2: Data categories |
| **T&Cs Consent?** | Yes / No | Step 4: Consent status |
| **Privacy Policy Consent?** | Yes / No | Step 4: Consent status |

These fields will appear as a recap at the start of the DPIA tool.

### 2. Dataset Classifier

After adding the source, you'll run the **Dataset Classifier** tool to assess:

- **Confidentiality**: How sensitive is the data if disclosed?
- **Integrity**: Impact of unauthorized modification?
- **Availability**: Impact if data becomes unavailable?
- **GDPR Categories**: Personal data, special category, criminal offence data?
- **ISO Controls**: Which ISO 27001:2022 controls apply?

Classifier results are **automatically imported** into DPIA Step 2 (Describe the processing).

---

## The 7-Step DPIA Process

The DPIA tool guides you through the ICO template with 7 steps. Each step builds on the previous one.

### Step 1: Identify the Need for a DPIA

**What you're doing**: Explaining why this DPIA matters and who is responsible.

**Pre-filled from Add Source**:
- Managing Group (controller organization)
- Source Owner / SPoC (responsible person)
- Source details

**What you add**:
- Project description and objectives
- Why you identified the need for a DPIA
- Reference documents (project proposal, security review, etc.)

---

### Step 2: Describe the Processing

**What you're doing**: Explaining how you collect, use, store, and delete data.

**Pre-filled from Source + Classifier**:
- Source name, type, and location
- Data categories identified by the Classifier
- PII, special category, and consent flags from Add Source
- Confidentiality, integrity, availability levels from Classifier

**What you add**:
- Technical details (systems involved, data flows)
- Data retention periods
- Who has access?
- Are you sharing data with other organizations?
- Any novel or unusual processing?

---

### Step 3: Consultation Process

**What you're doing**: Identifying who needs to be consulted and documenting their input.

**Guidance**:
- Internal stakeholders: Security, compliance, technical teams
- External stakeholders: Data Protection Officer (DPO), legal team, external processors
- Data subjects: In some cases, you should seek their views

**What you record**:
- Who you consulted
- When and how (meeting, email, survey)
- Their concerns and recommendations
- How you addressed feedback

---

### Step 4: Assess Necessity and Proportionality

**What you're doing**: Ensuring the processing is justified and you're not collecting more data than needed.

**Key questions**:
- What's your lawful basis for processing? (Consent, contract, legal obligation, etc.)
- Does this processing actually achieve your stated purpose?
- Is there a less invasive way to achieve the same outcome?
- Are you minimizing data (not collecting anything you don't need)?
- How will you support individuals' rights? (Access, deletion, portability, objection)
- How will you prevent function creep (using data for unintended purposes)?

---

### Step 5: Identify and Assess Risks

**What you're doing**: Listing potential harms to individuals and assessing likelihood and severity.

**Risk template**:
| Risk | Likelihood | Severity | Overall Risk |
|------|-----------|----------|--------------|
| Unauthorized disclosure | Possible | Severe | High |
| Data loss | Remote | Significant | Medium |
| ... | ... | ... | ... |

**Guidance**:
- Likelihood: Remote, possible, or probable?
- Severity: Minimal, significant, or severe?
- Overall: Low, medium, or high risk?

---

### Step 6: Identify Measures to Reduce Risk

**What you're doing**: For each medium or high risk from Step 5, what controls can you add?

**Mitigation options**:
- Technical controls (encryption, access controls, monitoring)
- Organizational controls (training, policies, procedures)
- Process controls (approval workflows, retention limits)
- Legal controls (contracts, terms and conditions)

**Record the outcome**:
| Risk | Proposed Measure | Effect | Residual Risk | Approved? |
|------|------------------|--------|---------------|-----------|
| Unauthorized disclosure | End-to-end encryption | Reduced | Medium | Yes |
| ... | ... | ... | ... | ... |

---

### Step 7: Sign Off and Record Outcomes

**What you're doing**: Getting formal approval from key stakeholders and documenting the decision.

**Sign-offs required**:
- **DPO approval**: Advice on compliance and whether processing can proceed
- **Business owner approval**: Acceptance of residual risks and planned measures
- **Consultation review**: How you addressed stakeholder concerns

**Key decisions**:
- Can processing proceed? (Yes, with conditions, or needs more work)
- Residual high risks: If you're accepting any high-risk outcomes, DPO consultation is mandatory
- Timeline: When will measures be implemented?
- Review date: When will this DPIA be revisited?

---

## How Auto-Population Works

### From Add Source Form
When you start the DPIA, fields automatically populate with:
- Managing Group
- Source Name, Type, URL
- Source Owner / SPoC Email
- Permission status
- PII flags
- Consent status

**You can edit any field** if circumstances have changed or if you need to provide more detail.

### From Dataset Classifier
The DPIA pulls in:
- Confidentiality, integrity, availability levels
- GDPR data category flags
- Special category indicators
- Applicable ISO 27001 controls

**Again, you can override or add context** if your assessment differs from the Classifier.

### What You Add
All other fields (risk assessment, consultation notes, measures, approvals) are entered directly by you. The tool provides templates and guidance to make this straightforward.

---

## Getting Started

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge — all recent versions)
- JavaScript enabled
- About 1–2 hours to complete a full DPIA

### Step-by-Step

1. **Access the tool**
   - Open: [CV DPIA Tool](https://joshuadaniel-cv.github.io/DPIA/)
   - Dark/light theme toggle in the top-right

2. **Review your source and classification**
   - Confirm the Add Source and Classifier data at the top of the form
   - Make any corrections needed

3. **Work through the 7 steps**
   - One step per page, in order
   - Progress bar shows where you are
   - Go back to review previous steps anytime

4. **Get sign-offs**
   - At Step 7, route for DPO and business owner approval
   - Record their feedback and decision

5. **Save/Export**
   - (Details on saving and export format coming soon)
   - Your DPIA is now ready for ROPA integration

### Data Privacy Note

✓ **Your DPIA form data is processed entirely in your browser**. It is not sent to any server and is not stored by CV Global. If you need to save your work, use your browser's download or print-to-PDF feature. Integration with backend storage systems is planned for a future release.

---

## Design & Accessibility

This tool is built on the **CV Global Design System**, ensuring:

- **Dark and light themes**: Choose your preference; it persists across sessions
- **Responsive design**: Works on desktop, tablet, and mobile
- **WCAG AA accessibility**: High contrast, keyboard navigation, screen reader support
- **Fast and lightweight**: No external dependencies, works offline

---

## For Data Protection Officers

If you're a DPO reviewing or signing off on DPIAs:

### Your Role in the Process

- **Step 3**: Consult with you on the proposed processing
- **Step 6**: Review proposed risk mitigation measures
- **Step 7**: Provide formal advice on:
  - Legal compliance (lawful basis, fairness, necessity)
  - Risk mitigation adequacy
  - Whether processing can proceed

### Escalation Criteria

If the DPIA identifies **residual high risks** that cannot be eliminated:
- You must be consulted before processing starts
- If you advise against processing, the business owner must escalate to senior leadership
- If they override your advice, this decision must be documented

### Ongoing Review

DPIAs are not static. Review the DPIA:
- When processing scope significantly changes
- If new risks emerge
- At least annually as part of your compliance review
- When relevant regulations or guidance update

---

## Documentation & Standards

### Key References

- **GDPR Article 35**: [Conduct of a Data Protection Impact Assessment](https://gdpr-info.eu/art-35-gdpr/)
- **ICO DPIA Guidance**: [Data Protection Impact Assessments](https://ico.org.uk/for-organisations/guidance-index/guides-for-uk-businesses-and-organisations/guide-to-the-general-data-protection-regulation-gdpr/data-protection-impact-assessments/)
- **ISO/IEC 27001:2022**: [Information Security Management](https://www.iso.org/standard/27001)
  - Specifically Section A.8.2 (Information Classification)

### Related Tools

- **Dataset Classifier**: [CV Dataset Classification Tool](https://joshuadaniel-cv.github.io/data-classifier/)
- **Record of Processing Activities (ROPA)**: Coming soon

---

## Feedback & Support

Have questions? Found a bug? Want to suggest improvements?

**Contact**: [uk.privacy@cvglobal.co](mailto:uk.privacy@cvglobal.co)

**For urgent issues**: Reach out to your Data Protection Officer or the CV Global Privacy Team.

---

## License

This tool is maintained by CV Global and is made available for use by CV Global employees and authorized partners.

---

## Version History

| Version | Date | Changes |
|---------|------|---------|
| 1.0 | June 2026 | Initial MVP: 7-step guided DPIA form with auto-population from Add Source and Classifier |

---

**Maintained by**: CV Global Privacy & Data Governance Team  
**Last Updated**: June 2026  
**Next Review**: December 2026
