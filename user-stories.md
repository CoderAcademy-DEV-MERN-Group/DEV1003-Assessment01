# User Stories

## Personas (Wants/Stories)

### 1. The Competitor

- **Persona:**

  - A competitive person who loves movies.
  - Wants to climb leaderboards and compare scores with others.
  - Uses the Reel Leaders leaderboard, Reel Score and even Custom Lists as new challenges to complete for a higher score.

- **Leaderboard Motivation:**

  - As a Competitor, I want to see where I rank on the Reel Leaders leaderboard, so that I can measure my progress against other movie fans.

- **Genre-Based Challenges:**

  - As a Competitor, I want to filter leaderboards by genre, so that I can challenge myself in specific categories I enjoy or want to improve in.

- **Reel Score Tracking:**
  - As a Competitor, I want my Reel Score to update automatically as I watch and rate movies, so that I feel rewarded for every step of progress.

---

### 2. The Collector

- **Persona:**

  - A completionist who wants to conquer the 100 movies of the Reel Canon.
  - Finds satisfaction in visually “scratching off” and collecting every title.

- **Scratch-Off Progress:**

  - As a Collector, I want to scratch off movies from the Reel Canon, so that I can visually track my progress toward completing the full list of 100 films.

- **Rating as a Milestone:**

  - As a Collector, I want to rate each movie as I scratch it off, so that I can reflect on my personal journey through the Canon.

- **Completion Satisfaction:**
  - As a Collector, I want to see my Popcorn Box Meter fill up, so that I get a clear sense of achievement as I approach 100% completion.

---

### 3. The Social Planner

- **Persona:**

  - The one who organises movie nights with friends or family.
  - Wants to find recommendations based on shared viewing history.
  - Relies on the friends system and Reel Comparisons to suggest the next group watch.

- **Friend Comparisons:**

  - As a Social Planner, I want to compare my movie list with my friends, so that I can find films we’ve all watched or ones we’re both missing.

- **Smart Recommendations:**

  - As a Social Planner, I want the app to suggest movies that neither of us has seen, so that I can easily pick the next movie night choice.

- **Shared Events:**
  - As a Social Planner, I want to invite friends through the platform, so that planning group movie sessions feels connected and fun.

---

### 4. The Curator

- **Persona:**

  - A knowledgeable movie lover who enjoys guiding friends toward great films.
  - Wants to create and share Custom Lists (eg., “Top 10 Thrillers” or “Best Movies for a Girls Night”).
  - Uses the platform to help others discover new favorites, not just to show off expertise.

- **List Creation:**

  - As a Curator, I want to create custom lists of movies (eg “Top 10 Thrillers”), so that I can share my taste with others.

- **List Sharing:**

  - As a Curator, I want to publish my custom lists for friends to explore, so that they can discover films I think are worth watching.

- **Discovery Through Curation:**
  - As a Curator, I want to see how others interact with my lists, so that I know I’m helping people discover new favorites.

---

## Epics and User Stories (Goals/Stories)

### Epic #1: Competition and Leaderboards

- **Persona**: The "Competitor"
- **Goal:** Motivate competitive users by comparing thei leaderboards scores and progress.
- **User Stories:**
  - As a Competitor, I want to view my ranking on the Reel Leaders leaderboard, so that I can measure my progress against others.
  - As a Competitor, I want to filter leaderboards by genre, so that I can challenge myself in specific areas.
  - As a Competitor, I want my Reel Score to update automatically when I complete or rate a movie, so that I feel rewarded instantly.

---

### Epic #2: Movie Progress and Watched Completion

- **Persona:** The "Collector"
- **Goal:** Help users track, rate and complete the Century Screening Room **Movie Canon.**
- **User Stories:**
  - As a Collector, I want to scratch off movies from the Movie Canon, so that I can visually track my progress.
  - As a Collector, I want to rate each movie I complete, so that I can reflect on my personal journey through the canon.
  - As a Collector, I want to see my “Popcorn Meter” fill up as I progress, so that I feel a sense of achievement.

---

### Epic #3: Social Viewing and Planning

- **Goal:** Make it easy for groups of friends to plan and share experiences.
- **User Stories:**
  - As a Social Planner, I want to compare my movie list with my friends, so that I can find films we’ve all watched or are missing.
  - As a Social Planner, I want the app to suggest movies that neither of us has seen, so that I can easily choose a movie for the next group night.
  - As a Social Planner, I want to invite friends to shared events, so that group movie nights are easier to organise.

---

### Epic #4: Curated Lists and Discovery

- **Goal:** Enable knowledgeable users to create, share, and promote movie lists.
- **Persona**: The "Curator"
- **User Stories:**
  - As a Curator, I want to create custom lists (eg. “Top 10 Thrillers”), so that I can share my recommendations.
  - As a Curator, I want to publish lists for others to explore, so that they can discover films I recommend.
  - As a Curator, I want to see how others interact with my lists, so that I know I’m helping people find new favourites.

---

## User Story Mapping Across Phases

| Persona            | User Story / Feature Example                             | Phase Alignment                                                                                                        |
| ------------------ | -------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| **Collector**      | Scratch-off movies from the Reel Canon to track progress | **Back-End**: CRUD endpoints for movies & progress tracking <br> **Front-End**: UI to visually mark/scratch-off movies |
| **Collector**      | Rate each movie watched to reflect on progress           | **Back-End**: Ratings schema & API routes <br> **Front-End**: Rating input & display                                   |
| **Competitor**     | View ranking on Reel Leaders leaderboard                 | **Back-End**: Leaderboard logic, Reel Score updates <br> **Front-End**: Leaderboard display component                  |
| **Competitor**     | Filter leaderboards by genre for challenges              | **Back-End**: Query/filter endpoints <br> **Front-End**: Leaderboard filter controls                                   |
| **Social Planner** | Compare movie lists with friends                         | **Front-End**: Friend comparison UI <br> **Back-End**: Shared user data queries                                        |
| **Social Planner** | Smart recommendations for next group watch               | **Back-End**: Recommendation logic <br> **Front-End**: Suggested movies display                                        |
| **Social Planner** | Invite friends to shared events                          | **Front-End**: Friend invite & event feature (stretch goal)                                                            |
| **Curator**        | Create & publish custom movie lists                      | **Back-End**: Custom List schema & endpoints <br> **Front-End**: List builder UI                                       |
| **Curator**        | Share lists & track interactions                         | **Back-End**: Tracking engagement data <br> **Front-End**: Interaction analytics UI (stretch goal)                     |

---
