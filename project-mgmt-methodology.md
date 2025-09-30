# Software Development Methodologies

This section explains the Software Development Methodologies and how we plan to implement them in our MERN Full-Stack project: **The Century Screening Room**.

During the planning phase, we considered our project scope, team size and the need for flexibility across the lifecycle. We chose Agile as our Project Management Methodology and Kanban as our Task Management Methodology. While Agile guides our sprints and retrospectives, Kanban provides the task visualisation framework we use to manage these Agile practices in Trello.

The combination of these methodologies enables us with a structured yet flexible workflow that can evolve across all three phases of the project lifecycle.

## Agile Project Management Methodology

Agile is an iterative methodology that emphasises adaptability, collaboration and incremental progress (Atlassian, 2024).

### Core Principles We Apply

- Short development cycles (sprints) to deliver incremental value and continuous delivery.
- Continuous feedback via daily stand-ups, reviews and retrospectives enabling us to continuously reflect and improve.
- Responding and adapting quickly to change over rather than rigid planning.
- Transparency and collaboration across the team.

## Implementation of Agile Practices

Working in an Agile approach helps us maintain progress while adapting to changes. It fits our small team and evolving scope by enabling short feedback loops and continuous improvement. Implementation plan of Agile practices include:

- **Sprints:** Weekly cycles delivering incremental outcomes aligned with MVP requirements.
- **Daily Stand-ups** (Slack): Quick posts covering yesterday’s work, today’s plan, and low/high priority blockers.
- **Sprint Planning:** At the start of each sprint: prioritise tasks, assign ownership, define acceptance criteria.
- **Retrospectives:** End of each sprint reviews to evaluate what worked and what needs adjustment. We reflect on successes, challenges and improvements.
- **Definition of Done (DoD):** Each task card requires acceptance criteria and peer review before moving to “Done”.
Any tests/docs updated.
- **Task Prioritisation:** Dependencies and MVP-aligned tasks prioritised and addressed.
- **Backlog Hygiene:** Regular refinement of epics/stories, keeping scope realistic.
- **Pipeline management:** Regular review against projection of keeping on track with our roadmap timeline throughout the project development phases.

**How Agile and Kanban integrate:**

Agile gives us the cadence (sprints, planning, retros). Kanban (in Trello) provides the visual flow to execute those practices day-to-day.

*Figure 1: Agile Methodology Cycle (iteration, feedback, improvement)*

---

## Agile Application Across Phases

We adopted Agile as our overarching methodology because it was suitable for our team size working on a full-stack project that would require flexibility and regular adjustments.

### Phase 1 (Planning, Design and Documentation)

**Sprint goals:** Software architecture and paradigms, ERDs, wireframes, methodology docs, initial backlog, and DoD.
**Retrospective focus:** clarity of scope, rubric alignment, task progress update on team alignments, estimation to manage tasks/workload/prioritisation and timeline projections.

### Phase 2 (Back-End Development)

**Sprint goals:** CRUD endpoints, validation, error handling, seed data, API docs.
**Retrospective focus:** code quality, debugging and testing coverage, PR review quality, CI checks.

### Phase 3 (Front-End Development)

**Sprint goals:** UI components, state/data flows, responsiveness, accessibility, testing.
**Retrospective focus:** usability feedback, user testing, integration issues, ensure responsiveness and accessibility, polish.

---

### Examples of Agile in Practice

#### Phase 1 – Planning, Design & Documentation (Week 1)

**Example 1: Sprint Planning**

1. Define sprint goals aligned with rubric MVPs.
2. Select tasks cards/user stories into sprint and add acceptance criteria and ownership.
3. Run daily Slack stand-ups. Example of our standup format:
    - Yesterday’s work and time spent
    - Today’s plan
    - Completion % toward phase goal
    - Low vs high-priority blockers
4. Closed sprint with a retrospective and adjusted for the next cycle.
5. Repeated the cycle of planning → implementing → reviewing → reflecting.

---

**Example 2: Wireframes Designing in Practice**

**Task:** Create wireframes for the ReelCanon movie list page (desktop, tablet, and mobile views).

- **Sprint Planning:**

    - In our sprint planning session, we created a backlog task card in Trello: “Design ReelCanon Wireframes (Desktop + Tablet + Mobile).”
    - The card included acceptance criteria:
        - Desktop: []
        - Tablet: []
        - Mobile: []
    - Task assigned to a team member with a checklist for each device layout.
    - Outcome: Drafts in Figma → peer feedback → export PNGs → push to GitHub.

- **Kanban Workflow:**

    - Card moved from Backlog → Sprint Backlog → In Progress during Sprint 2.
    - Daily Slack stand-up example: *“Yesterday I sketched the mobile layout; today I’ll start on tablet responsive design; no blockers so far.”*

- **Review and Feedback (QA):**

    - Once initial drafts were done in Figma, the card was moved to Review column.
    - Other team members provided peer feedback (eg. Make hover effect on desktop and consider alternative options on Tablet and Mobile as 'hover' may not work on these devices).

- **Done:**

    - Meeting held to collaborate and reflect and provide feedback for adjustments
    - Final wireframes were exported and uploaded to GitHub repo.
    - The card was moved to Done, with the acceptance criteria checked off.

- **Retrospective:**

    - In the sprint retrospective, we noted that defining acceptance criteria at the start made peer review smoother and reduced rework.

---

## Tools/Technologies Used

| Tools/Platforms     | Source             | Purpose                       |
|-------------------|--------------------|---------|
| **Kanban Board**  | [Trello](https://trello.com/) | Kanban board for task management and visualisation of workflow |
| **Communication** | [Slack](https://slack.com/) | Communication for team collaboration, quick communications, daily standups and retrorespectives |
| **Documentation & Version Control** | [GitHub Repository](https://github.com/CoderAcademy-DEV-MERN-Group/DEV1003-Assessment01) | Central repository for documentation, codebase and version control. Working off individual feature branches and Pull Requests to review documentation and codebase. Tracked changes and accessible for our whole team. |
| **Design/Wireframes** | [Figma](https://figma.com/) | Designing wireframes and UX/UI design for across difference devices (responsive for Mobile + Tablet + Desktop) |
| **API Testing**   | [Insomnia](https://insomnia.rest/) / [Bruno](https://www.usebruno.com/) | API Endpoint Testing |
| **Deployment** | [Render??] | Deployment platform and services |

## References

| Source                | Purpose                                    |
|-----------------------|--------------------------------------------|
| [Atlassian: What is Agile Project Management](https://www.atlassian.com/agile/project-management) | Detailed overview and guidance on Agile Project Management |
| [Atlassian: Agile Coach](https://www.atlassian.com/agile) | Agile principles, sprints, stand-ups and guide to align our approach with industry standards and best practices. |
| [Atlassian: Kanban Principles](https://www.atlassian.com/agile/project-management/kanban-principles) | Explains the core Kanban principles and supporting practices |
| [Miro Blog: Scrum vs. Kanban Boards](https://miro.com/blog/scrum-kanban-boards-differences) | Comparison of Scrum vs Kanban boards |
| [Trello Guide](https://trello.com/guide) | Trello documentation for setting up and optimising Kanban board setup. |
