# Software Engineering Playbook - Workspace Context

This workspace follows the Software Engineering Playbook SDLC. Key references:

- **Documentation structure:** The `docs/` folder contains 22 guides covering the full lifecycle. See [docs/00-documentation_index.md](docs/00-documentation_index.md).
- **Requirements gathering:** Section 1 (Application Functionality and User Experience) is defined in [docs/01-requirements_gathering.md](docs/01-requirements_gathering.md) and covers:
  - 1.1 Core Features
  - 1.2 User Flows
  - 1.3 UX/UI Considerations
- **Deployment strategy:** Section 2 (Environment Approach and Infrastructure/Scaling) covers container vs VM, regulatory constraints, hybrid feasibility, scaling, and environment count. Use the **Deployment Strategy** agent or `/deployment-start` prompt.
- **Database and data management:** Section 3 in [docs/01-requirements_gathering.md](docs/01-requirements_gathering.md) covers 3.1 Database Requirements, 3.2 Caching, 3.3 Messaging and Integration. Use the **Database & Data Management** agent or `/database-start` prompt.
- **Next phase:** After requirements, proceed to [docs/02-technology_selection_and_poc.md](docs/02-technology_selection_and_poc.md).

For interactive requirements gathering, use the **Requirements Gathering** agent or `/requirements-start` prompt. For deployment strategy, use the **Deployment Strategy** agent or `/deployment-start` prompt. For database and data management, use the **Database & Data Management** agent or `/database-start` prompt. Sections 1, 2, and 3 can be run in any order.
