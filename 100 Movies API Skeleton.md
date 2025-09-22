# The Century Screening Room

**The Century Screening Room** is a social movie collection platform built around the foundational goal of completing a curated list of 100 essential films, known as **"The Reel Canon."** Users track their progress via a *Reel Score*, rate films, and mark them as watched (via an interactive display). The platform fosters social interaction through granular friend-list management, personalized recommendations based on viewing similarity, and competitive leaderboards. Future development will empower users to create and share Custom Lists, transforming personal curation into a tool for planning movie nights and social events. Further development is scalable with other media or lists: eg. 100 Books to Read, 100 Albums to Listen To, 100 Places to Visit.

---

## Application Page Overview

### 1. Home/Splash Page

**Purpose:** Convert visitors into users.
**Content:** High-impact visuals showcasing key features: The Reel Canon, the scratch-off interaction, Reel Comparisons, and the Leaderboard. Clear call-to-action buttons for Login and Register.

### 2. Login Page

**Purpose:** Authenticate existing users.  
**Content:** Form for username/email and password. Link to Registration page.

### 3. Register Page

**Purpose:** Create new user accounts.  
**Content:** Form for username, email, and password. A multi-select list for favourite genres (pulled from the DB). This data seeds future recommendations.

### 4. The Reel Canon

**Purpose:** The core user journey - conquering the list of 100 essential films.  
**Content & Interaction:**

- Movies displayed as **colour palette paint-style cards** showing title, year, and genre
- **Clickable coin/reel icon** triggers animation to "scratch off" the colour, revealing the movie poster
- **Hover animations** reveal brief film descriptions
- **Upon scratching off,** a 5-star rating interface appears
- After rating, the card transforms permanently to display the poster with the user's rating badge

### 5. User Profile Page

**Purpose:** A personal dashboard showing progress and identity.  
**Content:**

- User details (username, etc.)
- **Reel Score:** An animated **"Popcorn Box Meter"** - a classic popcorn container graphic that fills up based on completion percentage
- Condensed **Friends List** with links to profiles
- Grid of **Custom Lists** created by the user

### 6. Reel Leaders (Leaderboard)

**Purpose:** Foster healthy competition and discovery.  
**Content:**

- Table ranking users by their Reel Score
- **Filter dropdown** to rank users by score within specific genres
- Clicking a username reveals an **anonymised data card** showing: username, Reel Score, stated favourite genre, highest-rated genre, and most-watched genre

### 7. Friend Search

**Purpose:** Find and connect with other users.  
**Content:** Search form requiring exact username or email match. Results display user with "Add Friend" button (managing stateful friend request status).

### 8. Reel Connections (Friends List)

**Purpose:** Manage social connections.  
**Content:** List of all friends, categorized by status ("Friends," "Pending Requests"). Displays each friend's current Reel Score. Options to remove friends or accept/deny requests.

### 9. Reel Comparisons (Social Core)

**Purpose:** Deeply compare taste with a friend and find common ground.  
**Content:**

- View shared lists (The Reel Canon or Custom Lists)
- **Visual Language:**
  - **Shiny Border:** Movies watched by **both** users
  - **Shadow Effect:** Movies watched by only **one** user
- **"Suggest Our Next Watch" Button:** Runs recommendation algorithm to find highest-rated movie neither user has seen

### 10. About / FAQ / Contact

**Purpose:** Provide context, help, and professional credibility.  
**Content:**

- **About:** Story and purpose of the app, team information
- **FAQ:** Answers to common questions
- **Contact:** Form for user feedback and support
- **GitHub Link:** Codebase showcase

---

## Entities

1. **User**
    - Has many **Ratings**
    - Has many **Friends** (through Friendship)
    - Has many **Lists**
    - Has many **ScratchProgress** records
2. **Movie**
    - Belongs to one **Director**
    - Belongs to many **Genres**
    - Has many **Ratings**
    - Appears in many **Lists**
    - Appears in many **ReelProgress** records
3. **Director**
    - Has many **Movies**
4. **Genre**
    - Has many **Movies**
5. **Rating**
    - Belongs to one **User**
    - Belongs to one **Movie**
6. **Friendship**
    - Connects two **Users** (pending or accepted state)
7. **List**
    - Belongs to one **User**
    - Has many **Movies**
8. **Leaderboard Entry**
    - Belongs to one **User**  
    - Aggregates **Ratings** + **ReelProgress**
9. **Recommendation**
    - Belongs to one **User**
    - References one or more **Movies**
    - May be generated via **Reel Comparisons** between two Users
10. **ReelProgress**
    - Belongs to one **User**
    - Belongs to one **Movie**
    - Tracks whether scratched, rated, and display state

---

## Personas

### The Competitor

- A competitive person who loves movies.  
- Wants to climb leaderboards and compare scores with others.  
- Uses the Reel Leaders leaderboard, Reel Score, and even Custom Lists as new challenges to complete for a higher score.  

### The Collector

- A completionist who wants to conquer the 100 movies of the Reel Canon.  
- Finds satisfaction in visually “scratching off” and collecting every title.  

### The Social Planner

- The one who organizes movie nights with friends or family.  
- Wants to find recommendations based on shared viewing history.  
- Relies on the friends system and Reel Comparisons to suggest the next group watch.  

### The Curator

- A knowledgeable movie lover who enjoys guiding friends toward great films.  
- Wants to create and share Custom Lists (e.g., “Top 10 Neo-Noir Thrillers” or “Best Movies for a Rainy Night”).  
- Uses the platform to help others discover new favorites, not just to show off expertise.  

### User Story Pattern

As a [type of user], I want [some goal], so that [some reason].

### Example (Collector)

As a Collector, I want to scratch off movies from the Reel Canon, so that I can track my progress through the 100 films.

---

### Conclusion

All of these suggestions are purely for the planning stage, if we feel this is too much work for us to complete we can adjust as needed!
