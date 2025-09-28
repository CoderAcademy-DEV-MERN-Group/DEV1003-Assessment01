# Software Development Methodologies

This section explains the **Software Development Methodologies** and how we apply them in our MERN Full-Stack project - *The Century Screening Room*. During the Planning Phase, we considered project scope, team size, and the need for flexibility throughout the lifecycle. We chose to apply the methodologies of **Agile** for **Project Management** and **Kanban** for **Task Management**, to provide us a balance of a structured yet flexible workflow for our project.

## Agile Project Management Methodology

Agile is an iterative project management methodology that emphasises on adaptability, collaboration, continuous delivery and working in incremental progress (Atlassian, 2024). It's core principles include working in short development cycles, continuous feedback, and responding to change rather than rigid planning. Agile practices include sprints (short work cycles), daily stand ups (quick team check-ins), and retrospectives (reviewing what worked and what to improve).

For our group project on the MERN Full Stack Application, we chose Agile as our overarching project management methodology because it's core principles aligned with our allows us to work in short, flexible cycles,collaborate closely, and adjust when plans change and evolve.

- Flexibility and adaptability to change
- Collaboration and transparency among team members
- Continuous delivery and improvement
- Working in short development cycles with regular retrospectives

The application of how we plan to use Agile Methodology in our project include the practices of:

- **Sprints**: Short weekly cycles to deliver incremental progress.
- **Daily Stand-ups**: Quick updates covering yesterday’s work, today’s goals, and low and high priority blockers.
- **Retrospectives**: End of sprint reviews to reflect on what worked well and what we can improve on.
- **Task Prioritisation**: Tasks that include MVP requirements or features and those with dependencies are prioritised first.

*Figure 1: Agile Methodology Cycle Diagram (iteration, feedback, improvement) - need to add*

---

### Example: Agile in Practice

**Phase 1 (Week 1) - Planning, Design & Documentation:**

1. We defined sprint goals aligned with the rubric aligned MVPs.
2. Daily stand-ups were held in Slack (#daily-standups). Example stand-up format:
    - **Work Undertaken Yesterday:** A brief description of what you worked on yesterday
    - **Time Per Unit - Yesterday:** A rough estimate of how much time you spent on each unit of work yesterday (e.g. 2.30hrs working on wireframes, 15 minutes general admin)
    - **Time Per Unit - Total:** Add the above to yesterdays total
    - **Todays Work:** A brief overview of the work planned for today
    - **Phase 1 Completion Tracker:** A rough percentage of how much of phase 1 you have completed. I don't expect this to be initially accurate
    - **Low Priority Blockers:** Any blockers that would prevent you from completing phase 1
    - **High Priority Blockers:** Any blockers that are preventing you from completing your planned tasks today
3. At the end of the sprint, we hold a retrospective to reflect on the cycle progress (what worked well and what we could improve on). Following this collaborative discussion, we consider any changes required and then plan for the next Sprint Cycle.
4. We then repeat our workflow cycle including planning, assigning next workload of tasks, implemenation, review and feedback, and complete end of spring retrospective.

---

## Kanban Task Management Methodology

Kanban is a visual workflow management methodology provides structure and visibility for tasks, emphasing transparency and visualisation of workflow that helps teams organise and track tasks as they move through defined stages. It uses **columns and task cards** to represent stages of work as task cards usually as user stories. It helps teams to monitor workload and if often implemented with limiting work in progress (WIP) to reduce bottlenecks (overload) and support continuous improvement flow.

We chose to use Kanban as our Task Management Methodology as our project and small team group aligned with the workflow and the Kanban Core Principles (Atlassian, 2024) of:**

- **Start with what you do now** - visualise our current tasks before optimising.
- **Pursue incremental change** - evolve the board gradually (e.g., adding *Testing* or *Deployment* later).
- **Respect current roles** - no need for a Scrum Master; all members can update the board.
- **Leadership at all levels** - anyone can suggest improvements to the workflow.

In our project, we implement our Kanban Board on [Trello](https://trello.com/), where tasks are represented as cards that move across columns (Backlog → To Do → In Progress → Review/Feedback → Done). Each task is represented as a card containing description of task, acceptance criteria, useful labels to help with prioritisation and assigned members to own/share tasks.

One of the advantages of using Kanban is that it is not fixed and the board structure can evolve as the project progresses. While our initial setup uses columns such as Backlog, Sprint Backlog (To Do), In Progress, Review/QA, and Done, we plan to refine this workflow as we move into different project phases.

Examples of how we plan to implement this in our project workflow:

- During development, we may add dedicated columns like Testing or Deployment
- As features expand, we may use epic cards that break down into smaller user stories or tasks
- WIP limits may be adjusted based on team capacity
- Additional labels or swimlanes may be introduced to track priorities, ownership, or dependencies

This flexibility ensures that our Kanban board continues to support our team’s workflow without becoming a constraint, aligning with Agile principles of adaptability and continuous improvement.

*Figure 2: Example of our Kanban Board on Trello*
[Insert screenshot of Trello board here]

---

## Quick Overview

### Kanban Methodology

- A framework focused on continuous flow and visualisation.
- Often considered both an Agile methodology and a task management framework.

### Kanban Principles

- Visualise work to increase transparency
- Limit work-in-progress (WIP) to reduce overload
- Improve flow continuously

### Kanban Approach

- Using a Kanban board (columns: Backlog → In Progress → Done) to represent workflow.
- Deciding whether you use Kanban standalone or blended with Agile (e.g., “Scrumban”).

### Kanban Practices

- Moving task cards across Trello as work progresses.
- Applying WIP limits (eg max 3 tasks cards in “In Progress” each).
- Using labels for priorities (High/Medium/Low).

### Our Kanban Board Structure

Columns in our board during Phase 1 of Planning, Design & Documentation:

- **Backlog** – Ideas & future tasks
- **Sprint Backlog (To Do)** – Tasks planned for the current sprint
- **In Progress** – Tasks actively being worked on (WIP limits applied)
- **Review/QA** – Peer review, feedback, and testing
- **Done** – Completed tasks (kept visible for accountability)

*Technical Diagram here*

---


OLD DRAFT NOTES TO REVIEW
### Example: Kanban Task Management Flow in Practice

**Scenario:** Writing this methodologies document
**Phase:** Planning, Designing, and Documentation

1. Task created in **Backlog**: “Draft `methodologies.md` (Agile & Kanban explanation).”
2. Pulled into **Sprint Backlog** during sprint planning.
3. Moved to **In Progress** once actively drafted.
4. Shifted to **Review/QA** for peer feedback.
5. Once approved, moved to **Done** (kept visible for transparency).

This flow ensures accountability, visibility, and quality checking before final completion.

Throughout our project lifecycle, we will continously adjust and refine our Kanban board structure and workflow based on team feedback and project needs. For example, during early development phase, we may add relevant columns such as for "Testing" and "Deployment", adjust WIP limits based on team capacity, create epic stories which are then broken down into user stories/tasks/features, and reprioritise tasks as requirements evolve. We continue to adopt the Agile Methodologies and its principles to ensure we remain flexible and adaptive to change.

---


Atlassian outlines six practices that support the principles and make Kanban work in software projects (Atlassian, 2024). Below is how we plan to use these practices in our project:

1. **Visualise the workflow:** Using a Trello board with columns representing workflow stages.
- **Transparency:** Everyone sees the current status of work.
- **Flexibility:** Tasks can be reprioritised mid-sprint if requirements change.
- **Collaboration:** Daily stand-ups and reviews encourage communication.
- **Focus:** WIP limits and sprint goals prevent overload.

### Our Practices

- **Limits on WIP:**
    - Prevents overload and highlights bottlenecks.
    - *As students working at different paces, this helps us avoid over-polishing and rework.*
- **Board Ownership:**
    - Shared by all team members, not one leader.
    - *This supports equal collaboration and shifting priorities.*
- **Task Responsibility:**
    - Individuals own tasks but can step in to help unblock others.
    - *This suits our varied skill levels and allows flexible support.*
- **Continuous Updates:**
    - New tasks can be added any time.
    - *This flexibility keeps progress flowing even with changing availability.*
- **Urgency Handling:**
    - Swim lane for critical blockers.
    - *Helps us address unpredictable issues in our first MERN app quickly.*
- **Backlog Management:**
    - Mix of descriptive tasks (rubric-aligned) and user stories where appropriate.
    - *Ensures clarity while leaving room for development features.*
- **Prioritisation:**
    - Real-time, based on MVP alignment and dependencies, supported by Trello labels.
- **Continuous Flow:**
    - No reset periods, work evolves continuously.
    - *Supports balancing study commitments with project tasks.*

The Agile Project Management Methodologies and Kanban Task Management Framework is well suited to the project's lifecycle and its principles, concepts and tools help us to manage our Full-Stack MERN Project effectively.

---

## Task Management Methodology

For task management, we used Kanban board which provides structure and visibility across the workflow. This method is effective for visualising tasks on a shared board, limiting work in progress to avoid bottlenecks (overload), and managing the flow of work until completion.

We set a Kanban board up via Trello with columns to represent the statuses of the phase's workflow. For our initial setup to keep it simple and clear for the planning and documentation phase, we used clear rubric aligned titles for the task cards, so that this helps us easily check off what our MVP requirements are. As we evolve into the development stage, we will create epic stories (key milestones) and break them down into user stories as task cards. This will also include the acceptance criteria, subtasks (checklists), priority labels, and ownership.

- Backlog (Ideas & Future Tasks)
- Sprint Backlog (To Do for current sprint cycle)
- In Progress (Actively working on and with WIP limits to prevent overload)
- Review/QA (Peer review and Feedback)
- Done (Completed tasks that have been reviewed against acceptance criteria)
[Include Kanban Board screenshot here for initial setup here]

This structured, visual approach ensures every team member can see progress at a glance and accountability is shared across the team. Together, Agile and Kanban give us a framework that balances flexibility with accountability. Agile helps us manage the project in short cycles, while Kanban ensures tasks are visible, organised, and moving forward in a transparent way.

**An example of how we applied Kanban with Agile methodologies:**

1. Weekly meetings planned to collaborate and discuss specific goals and tasks to complete.
2. Create tasks represented as a card on the Trello board with details like description, acceptance criteria, subtasks, priority labels, and ownership.
3. Assign tasks and decide who will work on what based on skills and interests and team capacity.
4. Tasks start in the Backlog column, then are pulled into To Do (for the current sprint cycle) when ready to be worked on, moved to In Progress when actively being worked on, then to Review for peer feedback, and finally to Done when following approved review being completed.
5. Daily stand ups on Slack to share progress, discuss blockers, and adjust priorities as needed.

To embed Agile practice, we started with an initial team meeting to collaboratively explore and understand the project idea's scope, set goals and expectations, and decide on the core implementation plans for the planning, design and documentation phase.

For our initial setup to keep it simple and clear for the planning and documentation phase, We used clear rubric aligned titles for the task cards, so that this helps us easily check off what our MVP requirements are. As we evolve into the development stage, we will create epic stories (key milestones) and break them down into user stories as task cards. This will also include the acceptance criteria, subtasks (checklists), priority labels, and ownership.

- Backlog → Ideas & Future Tasks
- Sprint Backlog → To Do
- In Progress → Actively working on (with WIP limits to prevent overload)
- Review/QA → Peer review and Feedback
- Testing → Bug fixing and Validation
- Done → Completed tasks


This included coverage for:

- Defining roles and responsibilities
- Designing the ERD and wireframes
- Setting up the Trello board with epics, user stories, and tasks
- Creating a shared Slack channel for communication
- Planning for future sprints covering backend (Assessment 2) and frontend (Assessment 3) development.
- Establishing a Definition of Done for task completion criteria.
- Creating a shared documentation repository for all project files.
- Implementing a feedback loop for continuous improvement.
- Holding sprint planning meetings to review backlogs, define goals and tasks.
- Complete weekly sprint retrospectives to reflect on the process and outcomes.

We agreed on a regular schedule for daily stand ups on Slack to share progress, discuss blockers, and adjust priorities as needed. Each sprint cycle (weekly) focused on delivering specific features or documentation components, with regular reviews and retrospectives to reflect on what went well and what could be improved. We plan to adapt to make changes in scope or requirements based on feedback from peers and throughout the development and testing phases as we progress, then regularly revise our task priorities as needed.

This Agile approach allows us to stay flexible, collaborate effectively, and maintain visibility across the project planning and task management which we will extend on as we approach the development and implementation phases of the project's lifecycle.

The use of a Kanban Board (using Trello) provides a clear visual tool aligned with Agile workflow practices. This task management tool is considered a Kanban framework, which also falls under the Agile methodology umbrella. The Kanban board is used to organise and track our task cards so that it is accessible and transparent to help us manage and track workflow items and features including:

- **Task statuses:**
    - These are columns representing different stages of the workflow, such as Backlog, To Do, In Progress, Review, Testing, and Done (Refer to example of Trello Kanban Board screenshot).
    - The key here is to keep the columns minimal and focused on the main workflow stages of the project phases.
    - As we progress into development, we may add more specific columns like Testing or Deployment to reflect the requirements and full life cycle of our project.

- **Task ownership:**
    - Who is responsible for each task
    - Assigned roles and labels such as Research, Planning, Design, Documentation, Backend, Frontend, Testing, Deployment etc.

- **Prioritisation of Tasks using priority labels:**
    - **High Priority**
        - Blocks progress in other tasks or dependencies
        - High importance or requirement for assessment criteria
    - **Medium Priority:**
        - Adds value but not blocking
        - Needed for quality or completeness
    - **Low Priority:**
        - Enhancements or polish
        - Optional features, diagrams etc.

- **Task deadlines:**
    - Due dates for time sensitive items
    - Sprint cycle dates

- **Task details:**
    - Title/User stories
    - Descriptions
    - Rubric aligned requirements
    - Checklists used for Tasks, Subtasks, Acceptance Criteria and QA
    - Task comments (for updates and collaboration)
    - Task labels (for categorisation and filtering)
    - Other relevant notes and attachments

The Kanban board and columns enable a clear visualisation to also help us identify any blockers or dependencies, and manage accountability across the team. The work in progress (WIP) limits help us avoid overload and identify potential bottlenecks early. Daily stand-ups on Slack facilitate quick communication and updates, while retrospectives allow us to reflect and improve our workflow continuously. Overall, the Agile methodology was chosen for its flexibility, focus on collaboration, and ability to deliver value incrementally, which aligns well with our project goals and team dynamics. This approach will help us manage the complexities of a full-stack MERN application project in a structured yet adaptable way.

---

## Tools Used

| Tool/Platform     | Link | Purpose |
|-------------------|------|---------|
| **Kanban Board**  | [Trello](https://trello.com/) | Task management using Kanban. Visualises backlog, sprint tasks, progress, and completed items with clear accountability. |
| **Communication** | [Slack](https://slack.com/) | Team collaboration and daily stand-ups. Used for quick updates, flexible communication, and sharing blockers. |
| **Documentation & Version Control** | [GitHub Repository](https://github.com/CoderAcademy-DEV-MERN-Group/DEV1003-Assessment01) | Central hub for documentation, codebase, and version control. Ensures files are reviewed, tracked, and accessible. |
| **Design/Wireframes** | [Figma](https://figma.com/) | Used to create low/high-fidelity wireframes. Provides a shared visual reference for planning UI/UX across devices. |
| **API Testing**   | [Insomnia](https://insomnia.rest/) / [Bruno](https://www.usebruno.com/) | Helps us test endpoints during backend development. Supports validation of requests, responses, and authentication workflows. |

---

## References

| Site Title & Link  | Purpose |
|-----------------------|---------|
| [Atlassian Agile Coach](https://www.atlassian.com/agile) | Resource for Agile principles, sprints, stand-ups, and Kanban best practices. Ensures our approach aligns with industry standards. |
| [Atlassian: Kanban Principles](https://www.atlassian.com/agile/project-management/kanban-principles) | Explains the 4 core Kanban principles and 6 supporting practices. Informs how we apply Kanban incrementally, respect current roles, and encourage team-wide leadership. |
| [Miro Blog: Scrum vs. Kanban Boards](https://miro.com/blog/scrum-kanban-boards-differences) | Compares Scrum and Kanban boards, clarifying their differences in WIP limits, ownership, backlog management, and flow. Helped us justify why Kanban was more suitable for our group project. |
| [Trello Guide](https://trello.com/guide) | Official Trello documentation for setting up and optimising Kanban boards. Helps us structure our workflow effectively. |
