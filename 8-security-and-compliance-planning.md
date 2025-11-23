# High-Level Security and Compliance Requirements Gathering

## 1. Lock Down Ports and Network Security
- **Prompts**:
  - Which ports are essential for application traffic and which can be closed or restricted?
  - How will Network Security Groups (NSGs) or Security Groups be configured to enforce least-privileged access?
  - Are there specific firewall rules or IP whitelists that need to be considered?

## 2. Data Encryption (At Rest and In Transit)
- **Prompts**:
  - What encryption mechanisms will be used for data at rest (e.g., KMS, Azure Key Vault, Cloud KMS)?
  - Which protocols (TLS/SSL) and certificates will secure data in transit?
  - How will key management and rotation policies be handled?

## 3. Logging and Monitoring for Compliance
- **Prompts**:
  - Which compliance frameworks (e.g., PCI-DSS, HIPAA, GDPR) apply?
  - What tools or services (e.g., AWS CloudTrail, Azure Monitor, GCP Cloud Logging) will be used for logging?
  - How frequently should logs be reviewed and what are the retention requirements?
  - Who will have access to audit logs?

## 4. Zero Trust Principles

### 4.1 Enforce MFA and Strong Identity Verification
- **Prompts**:
  - Which identity provider (IAM, SSO, or other) will manage authentication?
  - Will conditional access policies be required for different user roles?
  - How will MFA be enforced (e.g., SMS, Authenticator apps, hardware tokens)?

### 4.2 Use Short-Lived Credentials/Tokens
- **Prompts**:
  - Which authentication protocols (STS, OAuth2, etc.) are in scope?
  - How frequently should token rotation occur?
  - Will there be an automated mechanism for credential expiration?

### 4.3 Internal Traffic Inspection (East-West) 
- **Prompts**:
  - Which internal traffic paths or microservices need inspection?
  - What tools or methods (e.g., service mesh, deep packet inspection) will be used for internal traffic monitoring?
  - What performance impacts are acceptable for deeper inspection?

### 4.4 Integrate Policy Enforcement
- **Prompts**:
  - How will AWS Verified Access, Azure Private Link, or BeyondCorp principles be integrated?
  - Where do policies reside (in code, in a centralized manager, etc.)?
  - How will exceptions to policies be handled and documented?

### 4.5 Continuous Monitoring and Risk-Based Access
- **Prompts**:
  - Which metrics or events trigger automatic policy adjustments?
  - How is anomalous behavior detected and managed in real-time?
  - Which teams need alerts and escalation paths when a threat is identified?
