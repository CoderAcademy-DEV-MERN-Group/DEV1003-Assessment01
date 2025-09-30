# Kanban Task Management Methodology

Kanban is a visual workflow management framework that emphasises transparency, limiting work-in-progress (WIP), and continuous flow (Atlassian, 2024).

We chose Kanban as it provides us a clear, shared view of work and this task management methodology complements well with Agile by providing a simple, visible way to manage tasks. We implement Kanban on a Kanban Board in Trello, integrated with our Agile sprints.

We use Kanban via Trello as our task management framework to visualise workflow and manage priorities.

## Kanban Methodology Core Principles

- **Visualise the workflow:** Tasks represented as cards moving across columns.
- **Limit WIP:** Prevent overload and highlight bottlenecks.
- **Continuous improvement:** Evolve the board as project needs shift.
- **Shared ownership:** No single leader — all team members manage the board.

### Implementation of Kanban in Practice

We use Kanban via Trello as our task management framework to visualise workflow and manage priorities.

### Kanban Board Structure:

#### Phase 1 Baseline

We implemented our Kanban board in Trello with the following columns:

- **Backlog** – Ideas & future tasks
- **Sprint Backlog (To Do)** – Tasks planned for the current sprint
- **In Progress** – Active tasks being worked on (WIP limits applied <= 3 pp)
- **Review and Feedback (QA)** – Peer review, feedback and testing
- **Done** – Reviewed and completed tasks (kept visible for accountability), linked and pushed to GitHub central repository for version control.

### Integration with Agile

- Sprint Planning pulls cards from Backlog → Sprint Backlog
- Daily stand-ups reference card status
- Retrospectives to adjust WIP limits/columns if flow stalls.

During later phases, additional columns like Testing and Deployment may be added. Labels (High/Medium/Low) and swimlanes help manage priorities, blockers, and dependencies.

### Board Evolution Across Phases

**Phase 1 - Planning, Design and Documentation:**
- baseline columns (above)
- tasks cards for ERDs, wireframes, methodologies, roles etc.

**Phase 2 - Back-End Development:**
- add Testing and Deployment
- tasks cards/user stories for endpoints, schemas, controllers, error handling, seeds and bug/feature labels.

**Phase 3 - Front-End Development:**
- add Design swimlane and Bug Fix column
- tasks cards/user stories for components, accessibility, responsiveness, integration.

*Figure 2: Example Trello Kanban Board*


**Card Breakdown (MVP)**

- **Title:** user story or task name
- **Description:** concise scope and context
- **Acceptance criteria:** reviewable/testable bullet points
- **Labels:** priority (High/Med/Low) + type (Design/Back-End/Front-End/Docs/Test)
- **Checklist:** subtasks and rubric alignment check off
- **Owner(s): assignee(s)**
- **Attachments/links:** Figma/GitHub/PR/Insomnia workspace

---

#### Examples:

1. Task created in Backlog: “Draft methodologies.md.”
2. Pulled into Sprint Backlog during planning.
3. Moved to In Progress during drafting.
4. Shifted to Review/QA for peer feedback.
5. Finally, moved to Done once approved.

This flow ensures accountability, visibility, and quality checking before finalisation.

Example B: ERD Design (Phase 1)
Backlog → “Design ERD for Shows, Comedians, Venues, Lineups”
In Progress (dbdiagram.io) → Review/QA (Slack feedback)
Done (export PNG + commit)

Example C: CRUD Endpoint (Phase 2)
Backlog → “POST /comedians”
In Progress (schema, controller, route)
Testing (Insomnia/Bruno) → Review/QA (PR)
Done (merge + update API docs)

---
Example Workflow

Scenario: Designing ERD (Phase 1)
Task created in Backlog: Design ERD
Pulled into Sprint Backlog → assigned to Nhi.
In Progress → ERD drafted in dbdiagram.io.
Review/QA → peer-reviewed in Slack, feedback integrated.
Done → final version exported as PNG, uploaded to GitHub repo.
