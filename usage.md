# Usage Guide

This document describes how to use the VS Code Copilot customizations in this workspace: agents, prompts, and workflows.

**Prerequisites:** VS Code 1.106+ with Copilot enabled.

---

## Table of Contents

- [Requirements Gathering Agent](#requirements-gathering-agent)
- [Deployment Strategy Agent](#deployment-strategy-agent)
- [Database & Data Management Agent](#database--data-management-agent)
- [Security & Compliance Agent](#security--compliance-agent)
- [Technology Selection Agent](#technology-selection-agent)
- [Slash Commands (Prompts)](#slash-commands-prompts)
- [Adding Future Usage Details](#adding-future-usage-details)

---

## Requirements Gathering Agent

**Purpose:** Interactively gather Section 1 (Application Functionality and User Experience) from the playbook.

### How to Start

1. Open the Chat view in VS Code.
2. Select **Requirements Gathering** from the agents dropdown, **or**
3. Type `/requirements-start` and press Enter.

### Session Flow

1. **Introduction** — The agent greets you and asks the first questions from 1.1 Core Features.
2. **1.1 Core Features** — Primary functions and critical vs. future feature prioritization.
3. **1.2 User Flows** — User types, interactions, and automation candidates.
4. **1.3 UX/UI Considerations** — Design tools, design system, branding, accessibility, localization, devices.

### Key Behaviors

- **Interactive** — The agent waits for your answers before moving on. You can skip sections or go deeper as needed.
- **Confirmation before fetch/diagram** — If you ask for documentation or diagrams, the agent will ask: *"Would you like me to [fetch X / create a diagram]? Or do you have your own to reference?"* It only proceeds after you confirm.
- **Diagrams** — When approved, the agent generates Mermaid diagrams (user flows, persona matrices, device matrices).
- **Summary** — Run `/requirements-summary` anytime to get a consolidated markdown summary.

### Handoff

When Section 1 is complete, handoff buttons appear: **Continue to Deployment Strategy**, **Continue to Database & Data Management**, **Continue to Security & Compliance**, or **Continue to Technology Selection**.

---

## Deployment Strategy Agent

**Purpose:** Interactively gather Section 2 (Deployment Strategy) from the playbook.

### How to Start

1. Select **Deployment Strategy** from the agents dropdown, **or**
2. Type `/deployment-start` and press Enter, **or**
3. Complete the Requirements Gathering flow and click **Continue to Deployment Strategy**.

### Session Flow

1. **Introduction** — The agent greets you and asks the first questions from 2.1 Environment Approach.
2. **2.1 Environment Approach** — Container vs VM, regulatory/organizational constraints, hybrid feasibility.
3. **2.2 Infrastructure and Scaling** — Scaling under load, hosting requirements, number of environments (dev, test, staging, production).

### Key Behaviors

- **Interactive** — The agent waits for your answers before moving on. You can skip sections or go deeper as needed.
- **Confirmation before fetch/diagram** — If you ask for documentation or diagrams, the agent will ask: *"Would you like me to [fetch X / create a diagram]? Or do you have your own to reference?"* It only proceeds after you confirm.
- **Diagrams** — When approved, the agent generates Mermaid diagrams (environment topology, container vs VM flowchart, scaling architecture, hybrid approach).
- **Summary** — Run `/deployment-summary` anytime to get a consolidated markdown summary.

### Handoff

When Section 2 is complete, handoff buttons appear: **Continue to Technology Selection**, **Continue to Database & Data Management**, **Continue to Security & Compliance**, or **Back to Requirements Gathering**.

---

## Database & Data Management Agent

**Purpose:** Interactively gather Section 3 (Database and Data Management) from the playbook.

### How to Start

1. Select **Database & Data Management** from the agents dropdown, **or**
2. Type `/database-start` and press Enter, **or**
3. Complete the Requirements Gathering or Deployment Strategy flow and click **Continue to Database & Data Management**.

### Session Flow

1. **Introduction** — The agent greets you and asks the first questions from 3.1 Database Requirements.
2. **3.1 Database Requirements** — Database type (relational, NoSQL), data volume and transactions, retention and compliance.
3. **3.2 Caching** — Data to cache, invalidation/consistency, dedicated caching service.
4. **3.3 Messaging and Integration** — Messages/events between services, message broker (RabbitMQ, Kafka, etc.), protocols and standards.

### Key Behaviors

- **Interactive** — The agent waits for your answers before moving on. You can skip sections or go deeper as needed.
- **Confirmation before fetch/diagram** — If you ask for documentation or diagrams, the agent will ask: *"Would you like me to [fetch X / create a diagram]? Or do you have your own to reference?"* It only proceeds after you confirm.
- **Diagrams** — When approved, the agent generates Mermaid diagrams (database topology, caching architecture, message flow, integration diagrams).
- **Summary** — Run `/database-summary` anytime to get a consolidated markdown summary.

### Handoff

When Section 3 is complete, handoff buttons appear: **Continue to Technology Selection**, **Continue to Security & Compliance**, **Back to Requirements Gathering**, or **Back to Deployment Strategy**.

---

## Security & Compliance Agent

**Purpose:** Interactively gather Section 4 (Security and Compliance) from the playbook.

### How to Start

1. Select **Security & Compliance** from the agents dropdown, **or**
2. Type `/security-start` and press Enter, **or**
3. Complete the Requirements Gathering, Deployment Strategy, or Database & Data Management flow and click **Continue to Security & Compliance**.

### Session Flow

1. **Introduction** — The agent greets you and asks the first questions from 4.1 Authentication and Authorization.
2. **4.1 Authentication and Authorization** — Identity provider (SSO, IAM, Entra ID), MFA, RBAC/ABAC, token protocols (OAuth2, SAML).
3. **4.2 Regulatory and Compliance** — Standards (GDPR, HIPAA, PCI), audit logging, retention, who accesses audit logs.
4. **4.3 Data Encryption** — Encryption at rest and in transit, standards (AES-256, TLS 1.2+), key management (KMS, Key Vault, rotation).

### Key Behaviors

- **Interactive** — The agent waits for your answers before moving on. You can skip sections or go deeper as needed.
- **Confirmation before fetch/diagram** — If you ask for documentation or diagrams, the agent will ask: *"Would you like me to [fetch X / create a diagram]? Or do you have your own to reference?"* It only proceeds after you confirm.
- **Diagrams** — When approved, the agent generates Mermaid diagrams (authentication flow, compliance matrix, encryption architecture).
- **Summary** — Run `/security-summary` anytime to get a consolidated markdown summary.

### Handoff

When Section 4 is complete, handoff buttons appear: **Continue to Technology Selection**, **Back to Requirements Gathering**, **Back to Deployment Strategy**, or **Back to Database & Data Management**.

---

## Technology Selection Agent

**Purpose:** Guide through Technology Selection & Proof of Concept planning (playbook Section 2).

### How to Start

1. Select **Technology Selection** from the agents dropdown, **or**
2. Complete the Requirements Gathering, Deployment Strategy, Database & Data Management, or Security & Compliance flow and click **Continue to Technology Selection**.

### Scope

- Build vs. Buy analysis
- Technology stack selection
- Proof of concept / vertical slice
- Decision log

### Handoff

You can click **Back to Database & Data Management** to return to Section 3, or **Back to Security & Compliance** to return to Section 4.

---

## Slash Commands (Prompts)

Type `/` in the Chat input to see available prompts.

| Command | Purpose |
|---------|---------|
| `/requirements-start` | Start an interactive requirements session; asks first 1.1 questions. |
| `/requirements-core` | Jump to 1.1 Core Features questions. |
| `/requirements-flows` | Jump to 1.2 User Flows questions. |
| `/requirements-ux` | Jump to 1.3 UX/UI Considerations questions. |
| `/requirements-summary` | Request a consolidated summary of captured requirements. |
| `/deployment-start` | Start an interactive deployment strategy session; asks first 2.1 questions. |
| `/deployment-env` | Jump to 2.1 Environment Approach questions. |
| `/deployment-scaling` | Jump to 2.2 Infrastructure and Scaling questions. |
| `/deployment-summary` | Request a consolidated summary of captured deployment strategy. |
| `/database-start` | Start an interactive database and data management session; asks first 3.1 questions. |
| `/database-requirements` | Jump to 3.1 Database Requirements questions. |
| `/database-caching` | Jump to 3.2 Caching questions. |
| `/database-messaging` | Jump to 3.3 Messaging and Integration questions. |
| `/database-summary` | Request a consolidated summary of captured database and data management requirements. |
| `/security-start` | Start an interactive security and compliance session; asks first 4.1 questions. |
| `/security-auth` | Jump to 4.1 Authentication and Authorization questions. |
| `/security-compliance` | Jump to 4.2 Regulatory and Compliance questions. |
| `/security-encryption` | Jump to 4.3 Data Encryption questions. |
| `/security-summary` | Request a consolidated summary of captured security and compliance requirements. |

---

## Adding Future Usage Details

When adding new agents, prompts, or workflows:

1. Add a new section under this document (e.g., `## New Agent Name`).
2. Include: **Purpose**, **How to Start**, **Key Behaviors**, and any slash commands.
3. Update the [Table of Contents](#table-of-contents).
4. Add the new slash command to the [Slash Commands](#slash-commands-prompts) table if applicable.

---

**[← Back to README](README.md)** | **[Documentation Index](docs/00-documentation_index.md)**
