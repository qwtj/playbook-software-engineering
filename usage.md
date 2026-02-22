# Usage Guide

This document describes how to use the VS Code Copilot customizations in this workspace: agents, prompts, and workflows.

**Prerequisites:** VS Code 1.106+ with Copilot enabled.

---

## Table of Contents

- [Requirements Gathering Agent](#requirements-gathering-agent)
- [Deployment Strategy Agent](#deployment-strategy-agent)
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

When Section 1 is complete, handoff buttons appear: **Continue to Deployment Strategy** or **Continue to Technology Selection**.

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

When Section 2 is complete, handoff buttons appear: **Continue to Technology Selection** or **Back to Requirements Gathering**.

---

## Technology Selection Agent

**Purpose:** Guide through Technology Selection & Proof of Concept planning (playbook Section 2).

### How to Start

1. Select **Technology Selection** from the agents dropdown, **or**
2. Complete the Requirements Gathering or Deployment Strategy flow and click **Continue to Technology Selection**.

### Scope

- Build vs. Buy analysis
- Technology stack selection
- Proof of concept / vertical slice
- Decision log

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

---

## Adding Future Usage Details

When adding new agents, prompts, or workflows:

1. Add a new section under this document (e.g., `## New Agent Name`).
2. Include: **Purpose**, **How to Start**, **Key Behaviors**, and any slash commands.
3. Update the [Table of Contents](#table-of-contents).
4. Add the new slash command to the [Slash Commands](#slash-commands-prompts) table if applicable.

---

**[← Back to README](README.md)** | **[Documentation Index](docs/00-documentation_index.md)**
