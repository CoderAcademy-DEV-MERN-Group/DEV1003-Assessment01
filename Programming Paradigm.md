# Programming Paradigm

## Hybrid Approach: OOP Backend with Functional Frontend

At this stage of our application's development we are planning to use a hybrid approach of programming paradigms, choosing the most appropriate for different layers of the application:

* **Backend (Node.js, Express, Mongoose):** Object-Oriented Programming
* **Frontend (React):** Functional Programming with Hooks

For the purposes of this assessment, we will provide a thorough explanation of Object-Oriented Programming (OOP) as it is the foundation of our data models and application logic.

---

## Object Oriented Programming

Object Oriented Programming is a paradigm which structures code into objects, associating and bundling related data and methods within these objects. 

### Objects and Classes

Our application uses data which naturally map to objects. On the beckend, we will be using Mongoose Models and Schemas to serve as blueprints for documents in MongoDB. 

**Core Models (Classes):**

* user.js
* movie.js
* director.js
* genre.js
* rating.js
* friendship.js
* reelList.js
* leaderboardEntry.js
* recommendation.js
* reelProgress.js

*Note:* The leaderboardEntry.js file may not be needed in the final production application, as this may be implemented through aggregation of data from the user.js objects and rating.js objects.

### Encapsulation

Integral methods and properties for each object will be stored in their classes, with authorization and validation being the key focus.

### Inheritance

Unclear

### Polymorphism

### Depedencies