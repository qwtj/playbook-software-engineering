# Project Structure Requirements Gathering

> **Navigation:** [Home](README.md) | Previous: [Architecture Planning](2-architecture_planning.md) | Next: [Infrastructure Guidelines](4-infrastructure-guidelines.md)
>
> **Prerequisites:** Complete [Architecture Planning](2-architecture_planning.md) first
>
> **Related Documents:**
> - [Architecture Planning](2-architecture_planning.md) - High-level decisions affecting structure
> - [CI/CD Planning](10-cicd-planning.md) - Pipeline integration with project structure
> - [Infrastructure Guidelines](4-infrastructure-guidelines.md) - IaC implementation details

---

## Directory Layout for Source Code
### Purpose
- What languages or frameworks must be supported?
- How should the code be organized to facilitate modular development?
- Are there any established conventions or existing structures to follow?

### Repository Structure
- Is a monorepo approach needed or separate repos per component?
- How will common libraries or shared code be managed?
- What is the expected growth or scale of the project’s codebase?

### Build and Deployment
- How will build artifacts be handled?
- Are there specific branching or versioning strategies in place?

## Infrastructure-as-Code Templates
### Template Type Selection
- Which IaC tooling (Terraform, CloudFormation, ARM) is required or preferred?
- Will multiple cloud providers or environments be involved?

### Structure and Organization
- How should IaC files be structured within the repository?
- Are there requirements for modular or reusable IaC components?
- How will environment-specific configurations be handled?

### Provisioning and Deployment
- Will resources be provisioned in multiple stages (dev, staging, prod)?
- Are there any compliance or security constraints that affect IaC?

## Naming Conventions for Resources
### Naming Schema
- Are there existing naming conventions that must be followed?
- What information must be included in resource names (app name, environment, region)?

### Constraints
- Do length or character restrictions apply for certain resources?
- Are there guidelines for tagging resources (metadata, ownership, cost center)?

### Consistency and Governance
- How will naming standards be enforced?
- Who is responsible for maintaining the naming convention documentation?
