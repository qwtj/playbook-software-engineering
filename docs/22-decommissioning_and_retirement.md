# Decommissioning & Retirement (End of Life)

> **Navigation:** [Home](../README.md)
>
> **Prerequisites:** New system operational (if replacing) or Product Decision to Sunset
>
> **Related Documents:**
> - [Data Governance & Strategy](3-data_governance_and_strategy.md)

---

## 1. Retirement Planning
Plan the orderly shutdown of the application.

### 1.1 Trigger Conditions
When should this application be retired?
- [ ] Replacement system is 100% operational
- [ ] User base drops below threshold X
- [ ] Dependency End-of-Support reached

### 1.2 Timeline
- **Announcement Date:**
- **Read-Only Mode Date:**
- **hard Shutdown Date:**

---

## 2. Data Strategy (End of Life)
Refer to Data Governance policy.

### 2.1 Archiving
- What data must be retained for legal/compliance?
- Where will the archive live? (e.g., S3 Glacier, Tape)
- How will it be accessed if needed during audits?

### 2.2 Sanitization
- [ ] Securely wipe ephemeral storage / caches.
- [ ] Delete backup snapshots (after final archive created).
- [ ] PII deletion validation.

---

## 3. Resource Termination
Stop paying for what you don't use.

- [ ] Terminate Compute instances / Containers.
- [ ] Delete Load Balancers & DNS records.
- [ ] Release Static IPs.
- [ ] Cancel SaaS licenses / Add-ons.

## 4. Final Compliance Check
- [ ] Legal Hold released?
- [ ] Contracts with 3rd party consumers terminated?
