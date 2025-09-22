# Planning and Design Documentation

This project is focussed on planning larger scaled MERN stack development project. The ideas and plans made in this document pertain to the remainder of the term's assesments (all those related to MERN) but do not necessarily have to be commited to once production begins.  

## MVP & Assessment Brief (HD Requirement Alignment)

These MUST be included in some form:

1. **Explanation of the planned software architecture of the project**
    - **Programming paradigm:** Object-Oriented (MERN stack example: Mongoose schemas as “classes”).  
    - **Requirements for HD:** MULTIPLE programming examples + AT LEAST ONE diagram.  
    - **App architecture:** Model-View-Controller.  
    - **Requirements for HD:** THROUGH explanation, MULTIPLE diagrams, AT LEAST ONE programming example.

2. **Explanation of software development methodologies used in the project**
    - **Project management method:** Agile.  
      - **Requirements for HD:** MULTIPLE diagrams + AT LEAST ONE example/scenario of Agile in practice (e.g., sprints, standups).  
    - **Task management method:** Kanban (Trello).  
      - **Requirements for HD:** MULTIPLE diagrams (e.g., board screenshots) + AT LEAST ONE example/scenario of how tasks flow across the board.

3. **Explanation of client-server architecture**  
    - React (Client) & Express (Server) with MongoDB.  
    - **Requirements for HD:** THROUGH explanation of ALL FIVE areas (communication, data distribution, feature distribution, authorization, validation). MULTIPLE diagrams + MULTIPLE references.

4. **Plan for implementing the client-server architecture in the project**  
    - Explains how the project specifically applies the above (JWT auth, validation, what runs client-side vs. server-side).  
    - **Requirements for HD:** DETAILED plan covering ALL FIVE areas, with MULTIPLE diagrams + MULTIPLE references.

5. **Entity Relationship Diagram (ERD)**  
    - Optimised to standard format (crow’s foot notation).  
    - **Requirements for HD:** Draft + optimised version, showing all entities and relationships.

6. **User Stories**  
    - Must address AT LEAST THREE personas.  
    - Must include AT LEAST THREE different reasons/justifications.  
    - Must cover AT LEAST FOUR different wants/features/functionalities.  
    - **Requirements for HD:** Valid, sensible, and clear user stories at a professional level.

7. **Ethical Web Development Principles**  
    - Must cover AT LEAST FOUR principles (e.g., Privacy, Security, Accessibility, Transparency).  
    - **Requirements for HD:** GREAT DETAIL + references to tools or systems used to enforce them.

8. **Wireframes**  
    - Representing the intended application across THREE devices (Desktop, Tablet, Mobile).  
    - Must include MORE THAN FIVE detailed, well-designed wireframes.  
    - Low-fidelity OR high-fidelity acceptable.

## Rubrics

1. Explains a programming paradigm (5%) - Priority Low
    - Provide a thorough explanation of a programming paradigm with MULTIPLE programming examples and AT LEAST ONE diagram.
2. Explains a software architecture pattern (10%) - Priority Medium
    - Provides a THROUGH explanation of a software architecture pattern, with AT LEAST ONE programming example and MULTIPLE diagrams.
3. Explains a management methodology (5%) - Priority Low
    - Provides a THOROUGH explanation of a project management methodology, with MULTIPLE diagrams and AT LEAST ONE example or scenario of how that methodology would be used.
4. Explains a task management methodology (10%) - Priority Medium
    - Provides a THOROUGH explanation of a task management methodology, with MULTIPLE diagrams, and AT LEAST ONE example or scenario of how that methodology *would* be used.
5. Explains the fundamentals of software client/server architecture (10%) - Priority Medium
    - Provides a THOROUGH explanation on client/server architecture, including ALL of the topics listed: client/server communication, data distribution, feature distribution, authorization, validation. Explanation includes MULTIPLE diagrams and MULTIPLE references.
6. Explains a plan for implementing client server architecture in a software project (5%) - Priority Low
    - Provides a DETAILED plan on implementing client/server architecture in a project, including ALL of the topics listed: client/server communication, data distribution, feature distribution, authorization, validation. Explanation includes MULTIPLE diagrams and MULTIPLE references.
7. Optimises an entity relationship diagram to a standard format (5%) - Priority Low
8. Designs user stories appropriate to a web development project to a professional level (10%) - Priority Medium
    - Valid, sensible and *clear* user stories for AT LEAST THREE different users or personas, using AT LEAST THREE different reasons or justifications, for AT LEAST FOUR different wants/features/functionalities.
9. Explains how ethical web development principles will be applied to a project (5%) - Priority Low
    - Explanation of how AT LEAST FOUR ethical web development principles will be adhered to is provided with GREAT DETAIL, including references to tools or systems to help adhere to those principles.
10. Designs a set of wireframes appropriate for a responsive website (10%) - Priority Medium
    - MORE THAN FIVE DETAILED AND WELL DESIGNED (low fidelity OR high fidelity is fine) wireframes provided, for SEVERAL different device types (as required by the app).
11. Collaborates professionally and efficiently with a team during a project (20%) - Priority High
    - Project work performed EXCEPTIONALLY within a team, contributing to the work to a HIGH degree and communicating with the team to solve problems EXTREMELY EFFICIENTLY.

## Time Investment Estimate per Rubric

### 1. Explains a Programming Paradigm (Object-Oriented) (5%) - Priority Low

- **Estimate:** 2–3 hours  
- **Tasks:**
  - Research OOP principles (encapsulation, inheritance, polymorphism) as they apply to MERN.  
  - Create a diagram (e.g., class diagram for a `User` or `Movie` model).  
  - Write explanation with code snippets (e.g., a Mongoose schema as an example of a class).  

---

### 2. Explains a Software Architecture Pattern (MVC) (10%) - Priority Medium

- **Estimate:** 3–4 hours  
- **Tasks:**
  - Research the MVC pattern in the context of Express.js:  
    - **Models:** Mongoose schemas  
    - **Views:** React components  
    - **Controllers:** Express route handlers  
  - Create multiple diagrams:  
    - High-level flow diagram of a request.  
    - Specific diagram for a feature (e.g., rating a movie).  
  - Provide detailed code example (e.g., controller function handling `POST /api/movies/:id/rate`).  

---

### 3. Explains a Management Methodology (Agile) (5%) - Priority Low

- **Estimate:** 1–2 hours  
- **Tasks:**
  - Define Agile principles.  
  - Create a diagram of the Agile lifecycle.  
  - Provide a project scenario (e.g., 2-week sprints with planning, backlog prioritization, daily standups).  

---

### 4. Explains a Task Management Methodology (Kanban) (10%) - Priority Medium

- **Estimate:** 2–3 hours  
- **Tasks:**
  - Explain Kanban concepts (visualizing work, limiting WIP, managing flow).  
  - Create diagrams (e.g., Trello board template with columns like *Backlog, To Do, In Progress, Review, Done*).  
  - Provide a project scenario (e.g., bug reports moving through board stages).  

---

### 5. Explains the Fundamentals of Software Client/Server Architecture (10%) - Priority Medium

- **Estimate:** 4–5 hours  
- **Tasks:**
  - Explain core topics:  
    - **Client/Server Communication:** RESTful APIs, HTTP requests (GET, POST), JSON.  
    - **Data Distribution:** Client vs server storage (JWT on client, hashed passwords on server).  
    - **Feature Distribution:** UI rendering in React, business logic & database access in Express.  
    - **Authorization:** JWTs for API route protection.  
    - **Validation:** Client-side UX checks vs server-side security checks (e.g., Joi/Mongoose validation).  
  - Create multiple diagrams:  
    - Sequence diagram of login flow.  
    - Architecture diagram (client, server, database).  

---

### 6. Explains a Plan for Implementing Client/Server Architecture (5%) - Priority Low

- **Estimate:** 1–2 hours (can be done alongside #5)  
- **Tasks:**
  - Apply fundamentals (from #5) to the project context.  
  - Example:  
    - React client stores JWT in local storage.  
    - Sends JWT in API request headers to protected routes (e.g., `POST /api/friends`).  
    - Express server uses middleware to validate token before controller executes.  
  - Reuse diagrams from #5, annotated for the app.  

---

### 7. Optimises an Entity Relationship Diagram (5%) - Priority Low

- **Estimate:** 1–2 hours  
- **Tasks:**
  - Draft a basic ERD (entities: User, Movie, List, etc.).  
  - Create optimized version with crow’s foot notation.  
  - Define relationships clearly (e.g., User has many Movies through `WatchedMovies` join table).  

---

### 8. Designs User Stories (10%) - Priority Medium

- **Estimate:** 2–3 hours  
- **Tasks:**
  - Define 3–4 personas (e.g., The Competitor, The Social Planner, The Curator).  
  - Write 2–3 user stories per persona, following format:  
    - *As a [type of user], I want [goal], so that [reason].*  

---

### 9. Explains Ethical Web Development Principles (5%) - Priority Low

- **Estimate:** 1–2 hours  
- **Tasks:**
  - Choose 4 key principles:  
    - Privacy  
    - Security  
    - Accessibility  
    - Transparency  
  - Write one paragraph per principle, applied to project.  
  - Example: *For Privacy, collect only essential data (username, email, hashed password), store securely in MongoDB, use JWT for stateless authentication.*  

---

### 10. Designs a Set of Wireframes (10%) - Priority Medium

- **Estimate:** 6–8 hours  
- **Tasks:**
  - Create low-fidelity wireframes (Figma/Adobe XD).  
  - Design at least 5–6 core pages:  
    - Splash  
    - Login  
    - Reel Canon  
    - Profile  
    - Comparisons  
    - Leaderboard  
  - Produce versions for Desktop, Tablet, Mobile.  
  - Focus on layout and interaction changes (e.g., scratch-off mechanic on mobile).  

---

### 11. Collaborates Professionally (20%) - Priority High

- **Estimate:** 0 hours (naturally occurs during project)  
- **Tasks:**
  - Communicate regularly within team.  
  - Use version control (Git) effectively.  
  - Document processes and decisions.  
  - Contribute fairly to team tasks and peer collaboration.
