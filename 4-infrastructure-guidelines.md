## 1. Project Overview
- Describe the overall purpose of the project.
- Define success criteria and expected outcomes.
- Identify key stakeholders and sponsors.
- **Prompt**: What are the primary objectives and how do they align with business goals?
- **Prompt**: Who will be involved and what are their roles?

## 2. Infrastructure Requirements
### 2.1 Cloud Platform and Region
- Confirm AWS, Azure, or GCP as the primary provider.
- Select appropriate regions based on latency, compliance, or cost.
- **Prompt**: Which cloud provider will be used and why?
- **Prompt**: Are there specific region-based compliance needs?

### 2.2 VPC/Virtual Network/Subnet Configuration
- Determine IP address ranges.
- Decide on public vs. private subnets for security and access control.
- **Prompt**: How should traffic flow between subnets?
- **Prompt**: Any requirements for on-premises connectivity (VPN, Direct Connect/ExpressRoute/Interconnect)?

## 3. Identity and Access Management
- Define roles and associated permissions.
- Use service accounts for application-level access.
- **Prompt**: Which users, groups, or services need access?
- **Prompt**: What level of permissions is required (read, write, admin)?

## 4. Security Considerations
- Determine network security group/firewall configurations.
- Define encryption needs for data at rest and in transit.
- **Prompt**: Are there specific compliance or audit requirements?
- **Prompt**: Any additional security measures like intrusion detection or DDoS protection?

## 5. Scalability and Availability
- Identify expected workload and capacity planning.
- Plan for autoscaling, load balancing, and redundancy.
- **Prompt**: What are peak usage times and resource usage patterns?
- **Prompt**: Is high availability or disaster recovery required?

## 6. Monitoring and Logging
- Decide on logging and monitoring platforms or services.
- Define alerting and incident response processes.
- **Prompt**: Which metrics are most critical to track?
- **Prompt**: Who is responsible for handling alerts?

## 7. Governance and Compliance
- Establish policies for resource naming, tagging, cost management.
- Review relevant compliance frameworks (HIPAA, PCI, etc.).
- **Prompt**: Are there specific reporting or auditing requirements?
- **Prompt**: How will cost and resource governance be tracked?

## 8. Testing and Validation
- Define test environments (dev, staging, production).
- Validate subnet and routing configurations.
- **Prompt**: What types of testing will be done (functional, performance, security)?
- **Prompt**: Which QA processes or tools will be used?

## 9. Documentation and Handover
- Outline required architectural diagrams, support docs, and runbooks.
- Plan for knowledge transfer to operations teams.
- **Prompt**: Which teams or individuals will maintain the documentation?
- **Prompt**: How often should the documentation be updated?

## 10. Timeline and Next Steps
- Establish milestones for each phase of provisioning.
- Assign responsibilities and track progress.
- **Prompt**: What is the overall project schedule and who is accountable for deliverables?
- **Prompt**: Are there any major dependencies or risks that might impact the timeline?
