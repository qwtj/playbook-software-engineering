# Data Governance & Strategy

> **Navigation:** [Home](README.md)
>
> **Prerequisites:** [Database & Storage Planning](10-database_and_storage_planning.md)
>
> **Related Documents:**
> - [Security & Compliance](4-security_and_compliance_planning.md)
> - [Launch Checklist](20-launch_checklist.md)

---

## 1. Data Classification
categorize data to apply appropriate controls.

### 1.1 Data Types
- **Public:** Marketing data, generic content.
- **Internal:** Operational metrics, non-sensitive docs.
- **Confidential:** User emails, proprietary code.
- **Restricted (PII/PHI):** SSNs, Payment info, Health records.

### 1.2 Handling Requirements
- [ ] Encryption at rest required for: [Prompt]
- [ ] Data residency requirements (e.g., Must stay in EU): [Prompt]

---

## 2. Master Data Management (MDM)
Ensure a single source of truth for critical data entities.

### 2.1 Entities
- **Customer Master:** Where does the "Golden Record" for a user live?
- **Product Master:** Source of truth for product catalog?

### 2.2 Data Lineage
- Map upstream sources and downstream consumers for critical data.
- Tooling for cataloging: [Prompt]

---

## 3. Data Lifecycle Policy
Avoid "data swamps" by defining lifecycle rules.

### 3.1 Retention
- How long must specific data types be kept? (Legal/Compliance)
    - Logs: [Prompt]
    - User Records: [Prompt]
    - Transaction History: [Prompt]

### 3.2 Deletion & Archiving
- Process for "Right to be Forgotten" (GDPR/CCPA requests): [Prompt]
- Archival strategy for cold data (e.g., move to S3 Glacier): [Prompt]

---

## 4. Data Quality
- Who are the Data Stewards responsible for quality?
- Automated quality checks (schema validation, null checks): [Prompt]
