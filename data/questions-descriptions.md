# DPIA Questionnaire — Complete Descriptions

This document provides detailed guidance for each question in the 7-step DPIA form. Use this as a reference while completing the assessment.

---

## Step 1: Identify the Need for a DPIA

### Question 1.1: Project Title & Description

**What to enter:**
Provide a clear, concise title and description of your data processing project.

**Guidance:**
- Include the main objectives and goals
- Describe what problem you're solving or what outcome you're trying to achieve
- List key stakeholders and teams involved
- Mention the systems or processes involved
- Be specific enough that someone unfamiliar with the project could understand it

**Example:**
> **Title:** Employee Payroll System Upgrade
> **Description:** We are migrating our legacy payroll system to a modern cloud-based platform to improve processing efficiency and reporting. The new system will handle salary calculations, tax deductions, pension contributions, and payment processing for all 500+ employees. Key stakeholders include HR, Finance, IT Operations, and the Payroll team. The implementation is planned for Q3 2026.

**Why this matters:**
This description forms the foundation of the DPIA, helping DPOs and reviewers understand the scope and context of what you're assessing.

---

### Question 1.2: Why was a DPIA needed?

**Options:**
- **High-risk processing:** Your processing could pose high risks to individuals' rights and freedoms
- **Special category data:** You're processing sensitive personal data (ethnic origin, political opinions, religion, trade union membership, genetic data, health data, sex life/sexual orientation data)
- **Large-scale processing:** You're systematically processing large amounts of personal data
- **Processing involves children:** You're processing personal data of individuals under 16 years old

**Guidance:**
Select the primary reason(s) that triggered the need for a DPIA under GDPR Article 35. Article 35 requires a DPIA when processing is likely to result in high risks.

**Example scenarios:**
- **High-risk:** Implementing automated decision-making based on personal data
- **Special category:** Processing health records or criminal history data
- **Large-scale:** Processing data of thousands of customers for marketing analysis
- **Children:** Deploying a school's online learning platform that collects student data

**Why this matters:**
This helps document your compliance with GDPR Article 35 and ensures you've correctly identified when a DPIA is mandatory.

---

### Question 1.3: Related Documents

**What to enter:**
Links or file references to relevant project documentation.

**Guidance:**
Include:
- Project proposal or business case
- Security assessment or architecture review
- Vendor security questionnaires (if using third-party tools)
- Data classification results from the Classifier tool
- Any regulatory requirements or compliance standards
- Privacy Impact Analysis documents

**Format:**
Use URLs, file paths, or document names that others can easily access.

**Example:**
```
- Project proposal: https://internal.cvglobal.co/projects/payroll-upgrade
- Security review: Internal Drive > Projects > Payroll > SecurityAssessment_v2.pdf
- Vendor security doc: SharePoint > Vendors > CloudPayroll_SOC2_Certification.pdf
```

**Why this matters:**
This creates an audit trail and allows others to review the supporting documentation behind your DPIA.

---

## Step 2: Describe the Processing

### Question 2.1: Data Flow & Description

**What to enter:**
A detailed description of how personal data moves through your system from collection to deletion.

**Guidance:**
Describe each stage:
1. **Collection:** Where does data come from? (employees, customers, third parties)
2. **Input:** How does data enter your system? (manual upload, API, import, web form)
3. **Processing:** What happens to the data? (calculations, analysis, reporting)
4. **Storage:** Where is it stored? (databases, cloud storage, backups)
5. **Access:** Who uses it and how often?
6. **Sharing:** Is it transferred internally or externally?
7. **Deletion/Archival:** How and when is data deleted or archived?

**Example:**
> Employees submit timesheets monthly via a web portal. The data (hours worked, date, employee ID) is stored in our PostgreSQL database. Payroll team accesses it to calculate salaries. Finance team accesses it for reporting. Data is retained for 7 years in a warm backup, then archived to cold storage. After 7 years, it's deleted via automated purge scripts. External auditors access payroll reports monthly via secure API.

**Why this matters:**
This description helps identify where data is most vulnerable and where controls are needed.

---

### Question 2.2: Data Retention Period

**What to enter:**
How long you keep personal data.

**Guidance:**
- Be specific: "7 years" not "a long time"
- Base retention on:
  - Legal requirements (tax, employment law, regulatory requirements)
  - Business necessity
  - Data minimization (shorter is better)
- Distinguish between:
  - Active retention (accessible, regularly used)
  - Archival (inactive, for historical/compliance purposes)
  - Deletion (permanent removal after retention period)

**Examples:**
- "Payroll records: 7 years (required by tax law) then deleted"
- "Customer contact data: 3 years after last transaction, then deleted"
- "System logs: 30 days, then archived to cold storage for 1 year, then deleted"

**Why this matters:**
Overly long retention periods increase risk. This shows you're practicing data minimization.

---

### Question 2.3: Who has access?

**What to enter:**
All parties who can access the personal data.

**Guidance:**
List:
- **Internal:** Specific teams or roles (Payroll team, Finance analysts, HR managers)
- **External processors:** Vendors providing services (cloud hosting, backup, SaaS)
- **Third parties:** Partners, subcontractors, auditors
- **Access level:** Read-only, read-write, admin

Be specific about roles rather than individuals.

**Example:**
> - Payroll team (5 people): Full access to all payroll data for processing
> - Finance team (2 people): Read-only access for reporting
> - HR team (3 people): Read-only access for employee records
> - CloudPayroll vendor: Read-write access to live payroll data via API
> - Backup provider: Automated read-only access for disaster recovery backups
> - External auditors: Read-only access to anonymized payroll reports (annual, with contract)

**Why this matters:**
This helps identify whether access is appropriate and where controls are needed.

---

### Question 2.4: Is data shared with anyone?

**What to enter:**
Whether and how you transfer personal data outside your direct control.

**Guidance:**
Include:
- **International transfers:** If data leaves the UK/EU, how? (Standard Contractual Clauses, adequacy decision, etc.)
- **Third-country processors:** Any vendors operating outside UK/EU
- **Partners/resellers:** Other organizations you work with
- **Public/regulatory:** Data disclosed to authorities or published
- **Legal basis:** Why you're sharing (contract, legal obligation, legitimate interest)

**Example:**
> We share anonymized payroll data with our benefits provider (UK-based) for pension administration. We share employee addresses with the postal service for physical correspondence (legal obligation). We do not share personal data internationally.

**Why this matters:**
Data sharing creates additional risk and requires appropriate safeguards (contracts, data processing agreements).

---

## Step 3: Consultation Process

### Question 3.1: Who did you consult?

**What to enter:**
List of all stakeholders consulted during the DPIA.

**Guidance:**
Consult:
- **Data Protection Officer:** Mandatory, especially for high-risk processing
- **Security & IT team:** Technical controls, infrastructure
- **Legal team:** Lawful basis, compliance requirements
- **Business owner:** Project feasibility, business needs
- **Affected teams:** HR, Finance, operations who use the data
- **External parties:** Vendors, external auditors if relevant
- **Data subjects:** Sometimes, if processing directly affects them

**Example:**
> - Data Protection Officer (jane.smith@cvglobal.co)
> - Information Security team (security@cvglobal.co)
> - HR Director (hr.director@cvglobal.co)
> - Finance Manager (finance.manager@cvglobal.co)
> - IT Operations lead (it.ops@cvglobal.co)
> - CloudPayroll vendor (compliance@cloudpayroll.com)

**Why this matters:**
Consultation ensures diverse perspectives and helps identify risks others might miss.

---

### Question 3.2: How and when?

**What to enter:**
Methods and dates of consultation activities.

**Guidance:**
Describe:
- **Method:** Meeting, email, survey, workshop, call
- **Dates:** When was each party consulted?
- **Format:** One-on-one, group discussion, formal review
- **Duration:** How much time did each person spend?

**Example:**
> - Meeting with DPO: 2026-02-15 (1 hour, reviewed DPIA draft)
> - Email consultation with Security team: 2026-02-10 to 2026-02-14 (exchanged questions via email, 3 back-and-forth messages)
> - Meeting with HR Director: 2026-02-18 (30 mins, discussed employee impact)
> - Vendor security review: 2026-01-20 (received security questionnaire completion)

**Why this matters:**
This documents the consultation process and shows stakeholder engagement.

---

### Question 3.3: Their concerns & recommendations

**What to enter:**
Summary of feedback from stakeholders.

**Guidance:**
For each major stakeholder, note:
- **Concerns:** What risks or issues did they identify?
- **Recommendations:** What did they suggest?
- **How addressed:** Did you implement their suggestions? Why or why not?

**Example:**
> - **DPO concern:** Considered whether the 7-year retention was excessive. Recommendation: Reduce to 6 years where possible, only 7 years where legally required.
>   → **Addressed:** Implemented retention schedules distinguishing between mandatory records (7 years) and operational records (3 years).
>
> - **Security team concern:** Data is currently in an unencrypted backup. Recommendation: Encrypt all backups.
>   → **Addressed:** CloudPayroll vendor will encrypt backups; IT team implementing encryption for local backups by Q3.

**Why this matters:**
This shows how you've integrated feedback and addressed risks identified during consultation.

---

## Step 4: Assess Necessity & Proportionality

### Question 4.1: Lawful basis

**What to enter:**
The legal justification for processing personal data.

**Options:**
1. **Consent:** The data subject has explicitly agreed
2. **Contract:** Processing is necessary to perform a contract with the data subject
3. **Legal Obligation:** A law or regulation requires you to process this data
4. **Legitimate Interests:** Processing serves your (or a third party's) legitimate business interests

**Guidance:**
- Most processing relies on one primary basis
- You can have multiple bases, but identify the primary one
- Document how you meet the requirements of your chosen basis
- For Legitimate Interests, you must perform an LIA (Legitimate Interests Assessment)

**Examples:**
- **Payroll:** Legal obligation (employment law) + Contract (employment contract)
- **Marketing email:** Consent
- **Fraud prevention:** Legitimate interests (protecting your business)
- **Tax compliance:** Legal obligation (tax law)

**Why this matters:**
This is a foundational GDPR requirement. You must identify a lawful basis, and you're required to disclose it to data subjects.

---

### Question 4.2: How are you minimizing data collection?

**What to enter:**
Specific measures you're taking to limit what data you collect and keep.

**Guidance:**
Explain:
- **Purpose limitation:** Only collecting data needed for stated purpose
- **Anonymization/pseudonymization:** Removing identifiers where possible
- **Collection limits:** Not collecting optional data you don't need
- **Retention limits:** Deleting data when no longer needed
- **Access limits:** Restricting who can access what
- **Aggregation:** Using aggregated/summary data instead of individual-level data

**Example:**
> - We only collect name, ID, hours worked, and pay rate — not marital status or address (not needed for payroll).
> - We delete detailed timesheets after 3 months; keep only summary payroll records for 7 years.
> - We pseudonymize payroll data in reports (removing employee names, using ID numbers).
> - Only the Payroll team and Finance team have access; HR doesn't see salary details.

**Why this matters:**
Data minimization is a core GDPR principle. This shows you're limiting risks by not collecting or keeping more data than necessary.

---

### Question 4.3: How will you support individuals' rights?

**What to enter:**
Which data subject rights you will support.

**Common rights to support:**
- **Right to Access:** Individuals can request a copy of their personal data
- **Right to Deletion (Erasure):** Individuals can request deletion (with exceptions for legal obligations)
- **Right to Portability:** Individuals can request their data in a machine-readable format to move it elsewhere
- **Right to Rectification:** Individuals can correct inaccurate data
- **Right to Object:** Individuals can object to certain types of processing

**Guidance:**
For each right you support, describe:
- **How:** What's your process for handling requests?
- **Timeline:** How quickly will you respond? (GDPR requires 1 month)
- **Cost:** Free or paid?

**Example:**
> - **Right to Access:** Employees can request a copy of their payroll data. We respond within 10 business days via email.
> - **Right to Deletion:** After employment ends, we retain payroll records for 7 years (legal requirement), then delete. Employees can request deletion of non-mandatory data earlier.
> - **Right to Portability:** Employees can request data in CSV format from the CloudPayroll portal directly.

**Why this matters:**
Supporting data subject rights builds trust and demonstrates GDPR compliance.

---

## Step 5: Identify & Assess Risks

### Risk Assessment Table

**Columns:**

#### Risk Description
**What to enter:** A concise description of a potential harm or security/privacy incident.

**Guidance:**
- Be specific and concrete
- Consider both intentional threats (hacking, insider abuse) and accidental incidents (configuration errors, data loss)
- Think about impact on data subjects

**Examples:**
- "Unauthorized access to payroll data by external hacker due to weak database credentials"
- "Accidental deletion of payroll data due to system misconfiguration"
- "Data breach due to unencrypted backup file left on shared drive"
- "Employee with access leaves company; credentials not revoked in time"

**Common risk categories to consider:**
- Confidentiality risks (unauthorized access, disclosure)
- Integrity risks (unauthorized modification, corruption)
- Availability risks (loss, deletion, system failure)
- Compliance risks (inability to support rights, regulatory penalties)

---

#### Likelihood
**What to enter:** How probable is this risk?

**Scale:**
- **Remote:** Very unlikely to happen
- **Possible:** Could happen, but not expected
- **Probable:** Likely to happen or happens regularly

**Guidance:**
Consider:
- Historical incidents in your organization
- Industry-wide incidents
- Threat landscape for your sector
- Existing controls
- Complexity of the system

**Examples:**
- Unauthorized access to a publicly exposed database: **Probable**
- Accidental deletion with automated daily backups: **Remote**
- Employee accessing data they shouldn't: **Possible** (depends on access controls)

---

#### Severity
**What to enter:** How severe would the impact be if this occurred?

**Scale:**
- **Minimal:** Minor inconvenience or limited impact on a few individuals
- **Significant:** Moderate impact on multiple individuals, financial loss, legal consequences
- **Severe:** Major impact on many individuals, significant financial loss, regulatory penalties, reputational damage

**Guidance:**
Consider:
- How many individuals are affected?
- Type of data (health, financial, identity)?
- Consequences for data subjects (financial loss, discrimination, emotional distress)?
- Consequences for organization (fines, reputational damage)?

**Examples:**
- Loss of payroll data for 500 employees: **Severe** (impacts many, affects income)
- Exposure of tax IDs: **Severe** (enables identity theft)
- System downtime for 1 day: **Significant** (disrupts payroll processing)
- Read access by unauthorized admin: **Significant** (potential for misuse)

---

#### Overall Risk
**What to enter:** The combined risk level.

**Scale:**
- **Low:** Unlikely or minimal impact (likelihood: Remote + Severity: Minimal)
- **Medium:** Moderately likely or moderately severe (other combinations)
- **High:** Probable or severe, or both (likelihood: Probable + Severity: Severe)

**Guidance:**
Use this formula as a rough guide:
- **High risk:** Probable + any severity, OR Possible + Severe
- **Medium risk:** Possible + Significant, OR Remote + Severe
- **Low risk:** Remote + Minimal/Significant

**Why this matters:**
High and medium risks require mitigation measures (Step 6).

---

## Step 6: Identify Measures to Reduce Risk

### Risk Mitigation Table

**Columns:**

#### Risk
**What to enter:** Reference the risk from Step 5.

**Guidance:**
Use the exact wording from Step 5 so it's clear which risk you're addressing.

---

#### Proposed Measure
**What to enter:** The specific control or safeguard you'll implement.

**Types of measures:**
- **Technical:** Encryption, access controls, monitoring, firewalls, intrusion detection
- **Organizational:** Training, policies, procedures, background checks, segregation of duties
- **Legal:** Data Processing Agreements, contracts, terms and conditions
- **Physical:** Locks, cameras, secure facilities

**Example measures:**
- "Encrypt all databases using AES-256 encryption"
- "Require multi-factor authentication for all payroll system access"
- "Monthly access reviews to remove inactive users"
- "Mandatory data protection training for all staff with access"
- "Data Processing Agreement with CloudPayroll vendor"
- "Regular penetration testing (quarterly)"

---

#### Effect
**What to enter:** How does this measure reduce the risk?

**Guidance:**
Explain the mechanism:
- What threat does it prevent or mitigate?
- How does it reduce likelihood or severity?

**Examples:**
- "Encryption reduces impact of unauthorized access (confidentiality preserved even if hacked)"
- "MFA reduces likelihood of unauthorized access (attacker can't log in with password alone)"
- "Access reviews reduce likelihood of abuse by former employees"

---

#### Residual Risk
**What to enter:** What risk remains after implementing this measure?

**Guidance:**
- Risk is rarely eliminated completely; it's reduced to an acceptable level
- Use same scale as Step 5 (Low, Medium, High)
- Be realistic about what the measure achieves

**Example:**
> Risk: "Unauthorized access to payroll data by external hacker"
> Measures: "Encryption + MFA + monitoring"
> Residual risk: **Low** (encryption prevents confidentiality loss; MFA makes access very difficult; monitoring detects attempts)

---

#### Timeline
**What to enter:** When will this measure be implemented?

**Guidance:**
- Be realistic and specific: "Q3 2026" not "soon"
- Indicate priority (immediate vs. phased implementation)
- Link to project milestones if relevant

**Example:**
> - MFA: Implement by 2026-03-31 (immediate, before go-live)
> - Encryption: Implement by 2026-06-30 (before production data loading)
> - Monitoring: Q4 2026 (after go-live, lower priority)

---

## Step 7: Sign Off & Record Outcomes

### DPO Section

#### DPO Name
**What to enter:** Full name of the Data Protection Officer.

**Guidance:**
- This is the person who reviewed and approved the DPIA
- For audit trail purposes, use their legal name

---

#### DPO Email
**What to enter:** Email address of the DPO.

**Guidance:**
- Ensure it's a monitored, professional email address
- Used for future reference and audit trail

---

#### DPO Advice
**What to enter:** The DPO's formal advice and recommendations.

**Guidance:**
The DPO should address:
- Overall compliance: Does the processing comply with GDPR?
- Risk assessment: Are the identified risks and mitigations adequate?
- Conditions: Any conditions that must be met before processing starts?
- Concerns: Any unresolved issues or escalations?
- Recommendation: Can processing proceed?

**Example:**
> The proposed payroll system upgrade generally complies with GDPR. Data minimization is appropriate. However, we recommend:
> 1. Encrypt all backups before go-live (currently unencrypted)
> 2. Reduce non-mandatory record retention from 7 to 3 years
> 3. Implement quarterly access reviews
> Processing can proceed conditionally upon implementing these measures by 2026-06-30.

---

### Business Owner Section

#### Owner Name
**What to enter:** Full name of the business owner or senior manager responsible for the processing.

**Guidance:**
- This is the person accountable for managing the data and ensuring controls are implemented
- Usually a department head, product owner, or project sponsor

---

#### Owner Email
**What to enter:** Email address of the business owner.

**Guidance:**
- Professional email address for audit trail

---

#### Do you accept the residual risks?
**What to enter:** Yes or No (with potential escalation if No).

**Guidance:**
- After implementing mitigation measures, some residual risk may remain
- The business owner must formally accept these risks
- If they don't accept, it must be escalated to senior leadership

**Example:**
> Yes, we accept the residual medium risk of system downtime (1-day impact, 1-2 month recovery) as reasonable given business benefits of modernization.

---

### Final Decision Section

#### Can processing proceed?
**What to enter:** The final decision: Yes, Conditional, or No.

**Options:**
- **Yes:** Processing can proceed with no further conditions
- **Conditional:** Processing can proceed if specific conditions are met (e.g., measures implemented by certain date)
- **No:** Processing cannot proceed without major changes

**Guidance:**
Typically:
- **Yes:** All high and medium risks have been mitigated to acceptable levels
- **Conditional:** Some measures are pending implementation, but will be done before go-live
- **No:** Unacceptable risks remain; project scope must change or be abandoned

**Example:**
> Conditional: Processing can proceed after encryption is implemented and quarterly access reviews are established (expected by 2026-06-30).

---

#### Next review date
**What to enter:** When you will review and update this DPIA.

**Guidance:**
- Typically annual review
- Also review when:
  - Processing scope significantly changes
  - New risks emerge
  - Regulatory guidance updates
  - A data breach occurs
  - Controls are modified

**Example:**
> Next review: 2027-02-15 (1 year from implementation)

---

## Tips for Completing the DPIA

1. **Be honest about risks:** Don't minimize risks to make them go away; identify them so you can address them.
2. **Consult early:** Don't wait until the DPIA is half-done to involve stakeholders.
3. **Connect to existing controls:** Reference security measures, policies, and procedures you already have in place.
4. **Focus on high/medium risks:** Low risks don't need mitigation measures; focus on the ones that matter.
5. **Use clear language:** Avoid jargon; assume the reader isn't a security expert.
6. **Document decisions:** Record why you chose certain measures, retention periods, or legal bases.
7. **Keep it proportionate:** A DPIA for a simple project shouldn't be 100 pages; a complex one should be comprehensive.
8. **Get DPO input early:** Don't surprise them at the end; involve them in the consultation phase.

---

## GDPR References

- **Article 35:** Data Protection Impact Assessment requirement
- **Article 36:** DPO consultation for high-risk processing
- **Article 5:** Data protection principles (lawfulness, fairness, transparency, etc.)
- **Article 6:** Lawful basis for processing
- **Article 7:** Conditions for consent
- **Recital 75:** Guidelines on DPIA content and methodology

