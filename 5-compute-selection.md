# Compute Selection

> **Navigation:** [Home](README.md) | Previous: [Infrastructure Guidelines](4-infrastructure-guidelines.md) | Next: [Database & Storage Planning](6-database-and-storage-planning.md)
>
> **Prerequisites:** Complete [Architecture Planning](2-architecture_planning.md) (section 2.2 Serverless vs Compute)
>
> **Related Documents:**
> - [Architecture Planning](2-architecture_planning.md) - High-level compute architecture decisions
> - [Infrastructure Guidelines](4-infrastructure-guidelines.md) - VPC and networking context
> - [Performance & Optimization](11-performance-and-optimization-planning.md) - Compute sizing and scaling
> - [CI/CD Planning](10-cicd-planning.md) - Deployment target configuration

---

## 1. Project Context
- [Prompt] What is the overall goal or purpose of the project?
- [Prompt] Any business or technical constraints?

## 2. Compute Platform Options

### 2.1 Container Services (ECS/Fargate, AKS, GKE)
- [Prompt] What container orchestration tools or platforms are already in use?
- [Prompt] Are microservices or monolithic architectures in play?
- [Prompt] What level of control over infrastructure is needed?

### 2.2 Serverless (Lambda, Azure Functions, Cloud Functions)
- [Prompt] Is an event-driven architecture suitable or required?
- [Prompt] What are the expected traffic patterns (spiky, constant, unpredictable)?
- [Prompt] Any latency or cold-start constraints?

### 2.3 Classic VMs (EC2, Azure VMs, Compute Engine)
- [Prompt] Are there legacy apps or specialized workloads that need full OS control?
- [Prompt] Are custom configurations or third-party software dependencies a factor?
- [Prompt] Is VM-level isolation a security requirement?

## 3. Scaling Requirements

### 3.1 Automatic Scaling
- [Prompt] What metrics (CPU, memory, queue length) will trigger scaling?
- [Prompt] How quickly must scaling react to load changes?
- [Prompt] Does the application require predictive or scheduled scaling?

### 3.2 Manual Scaling
- [Prompt] Are there scenarios where manual capacity adjustments are preferred?
- [Prompt] Any change management process or regulations that limit auto-scaling?

## 4. OS Base Images

### 4.1 Linux
- [Prompt] Specific distributions preferred (Ubuntu, Amazon Linux, Alpine)?
- [Prompt] Any security or compliance requirements for the OS?
- [Prompt] Existing automation or tools (e.g., Chef, Ansible) that favor certain distros?

### 4.2 Windows
- [Prompt] Do applications rely on .NET or Windows-specific services?
- [Prompt] Any specific licensing or support constraints?
- [Prompt] Are there toolchains or existing expertise for Windows?

## 5. Additional Considerations

### 5.1 Cost and Budget
- [Prompt] Are there cost targets or restrictions?
- [Prompt] Preferred billing models (pay-as-you-go, reserved instances, etc.)?

### 5.2 Security and Compliance
- [Prompt] What data protection or regulatory standards apply (HIPAA, GDPR, etc.)?
- [Prompt] Authentication and authorization mechanisms?
- [Prompt] Are there encryption or key management requirements?

### 5.3 Networking and Connectivity
- [Prompt] Inbound/outbound traffic patterns or integration with other systems?
- [Prompt] Do existing VPCs, subnets, or on-prem connectivity influence design?

### 5.4 Monitoring and Logging
- [Prompt] Which tools (CloudWatch, Prometheus, Splunk, etc.) are preferred?
- [Prompt] Key metrics or logs to track for system health?
- [Prompt] Any requirements for audits or historical data retention?

### 5.5 Roadmap and Future Growth
- [Prompt] How might requirements evolve over time?
- [Prompt] Upcoming features or new service integrations?
- [Prompt] Migration or version upgrade strategies?

## 6. Decision Points and Next Steps
- [Prompt] Summarize priorities and constraints.
- [Prompt] Identify critical trade-offs or open questions.
- [Prompt] Outline actions for finalizing compute selection.
