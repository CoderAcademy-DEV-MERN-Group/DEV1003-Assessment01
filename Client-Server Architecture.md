# Client-Server Architecture

Client-Server architecture has been a standard of web communication since the late 1980s, when networks moved away from mainframe systems towards interconnected personal computers. This model connects multiple client devices to centralized servers that manage shared data resources and services (ScienceDirect, 2025)[^1].  
In modern web applications, this model operates in a layered approach: a user enters a URL into their device's browser (client), the client contacts a DNS server to convert the URL to an IP, the client sends an HTTP request to the server at that IP address, the server responds (with HTML, CSS, Javascript, media etc), and finally the client renders the response (GeeksForGeeks, 2025)[^2]. That's already two layers of client server architecture in action: DNS resolution, followed by HTTP communication.  
Developers use this model to distribute data and features, allowing for quick execution and display of web content, and for authorisation and validation to ensure data is secure and correct.

[DIAGRAM HERE: client -> network -> server. Reference has a really good example.]

Our application uses a three-tiered client-server architecture model (DataForest, 2025)[^3]:

- **Tier 1 (Presentation):** React is used for the client front-end framework
- **Tier 2 (Application):** Express is used as the server for business logic and database manipulation
- **Tier 3 (Data):** Mongoose and MongoDB act as database and validation layer

Below we will discuss the key features of the client-server architecture model, and how they will be implemented in our application.

---

## Communication

Client-server communication, in general, occurs through the use of standardised HTTP verbs to define the intent of requests. RESTful applications use this approach due to its advantages of stable and predictable behaviour, simple implementation, and high level of support across web platforms (Das S, 2025)[^4]. In web applications the standard verbs are:

- `GET`: Retrieve data
- `POST`: Create new resources
- `PUT`: Updates the entirity of an existing resource
- `PATCH`: Partially updates an existing record
- `DELETE`: Remove resources

Other HTTP verbs which are less often used, or execute advanced tasks are: `HEAD`, `TRACE`, `OPTIONS` and `CONNECT` (Mozilla Developer Network, 2025)[^5].

Headers are also used to carry metadata such as authentication and authorisation, content type, caching, and any other useful information not necessarily included in the request/response body (Postman, 2025)[^6].

Server-side middleware is used to act on requests from the client, and manipulate database records. Responses are then sent back to the client.

In our application:

- React frontend sends requests and user input, and manages UI states (React, 2025)[^7]
- Express middleware handles application logic, routing, and error handling (Express.js, 2025)[^8]
- Mongoose performs MongoDB database operations and manipulation as required by request type
- Express sends a JSON response to the React frontend, which renders components and updates UI states

Examples of HTTB verbs in our application:

```js
// GET - Fetch user's Reel Canon progress and movie data
GET /api/users/123/reel-progress
GET /api/movies?genre=drama

// POST - Create new ratings and friend relationships
POST /api/ratings { movieId: 456, rating: 5 }
POST /api/friends { friendId: 789 }

// PATCH - Update user profile and scratch progress
PATCH /api/users/123 { favoriteGenres: ['drama'] }
PATCH /api/progress/456 { isScratched: true }

// DELETE - Remove friends and user data
DELETE /api/friends/789
```

--> DIAGRAM HERE: <--
shows flow of our application:  
User Action (Clicks drama genre filter) → React (GET /api/movies?genre=drama) → Express (Movie.find({genre: "drama})) → Mongoose (db.movies.find({genre: "drama"})) → MongoDB.  
Back through chain:  
(MongoDB (return drama movies) -> Mongoose (serialized movie data) -> Express (JSON response) → React (UI Update) -> user)

## Data Distribution

[Explanation of data distribution: What data is stored where? Examples of generic data distributions: Client: Forms, UI states, session data, JWT tokens. Server: User credentials, ratings, application state. In our app: Client: JWT tokens held, UI state, cached movie posters, form input values, user's personal scratch progress. Server: User credentials held, ReelProgress (scratch/watch events for Leaderboard calculations), friend relationship status, cached movie metadata from external APIs, ratings]

## Feature Distribution

[Explanation of feature distribution: The why of the data-distribution. Client side: stored for faster cached loading, UI states: temporary states hold no value being persistent in server: what is open, who has what open, these are temporary states. Tokens attached to headers. Server: Server validates headers, persistent data needed for calculations stored server side: server does the maths and aggregations behind the scenes, serverside application state holds all business logic's current state, including what features are available to the user, session data for all concurrent users, and real-time connection data, held due to referring to multiple users. In our project: Credentials stored for security, ReelProgress stored as single source of truth for leaderboard calculations across multiple devices, friend relationship stored for ..., cached movie data stored to ensure faster load times for subsequent users, ratings stored for recommendation and comparison aggregation]

## Authorization

[Explanation of authorization and how it works in our application: JWT auth, refresh tokens, headers. HOW the token validation works. Token created -> refresh token created, password and user verification through hashed comparison, securely stored enve variables.]

## Validation

[Explanation of how validation is applied in our application: Client-side: forms and required fields validates before sending to server. Server: validation of JSON data and error handling, to database validation through strict Mongoose Schema]

---

## References

[^1] ScienceDirect. (2025). _Client-Server Architecture_. Elsevier. Available at: <https://www.sciencedirect.com/topics/computer-science/client-server-architecture> (Accessed: 19 September 2025)  
[^2] GeeksforGeeks. (2025). _Client-Server Model_. Available at: <https://www.geeksforgeeks.org/system-design/client-server-model/> (Accessed: 19 September 2025)  
[^3] DataForest. (2025). _Client-Server Model Glossary_. Available at: <https://dataforest.ai/glossary/client-server-model> (Accessed: 19 September 2025)  
[^4] Das, S. (2025). _Client-Server Communication: A Deep Dive_. LinkedIn. Available at: <https://www.linkedin.com/pulse/client-server-communication-deep-dive-sandip-das-zljcc/> (Accessed: 19 September 2025)
[^5] Mozilla Developer Network. (2025). _Client-Server Overview_. MDN Web Docs. Available at: <https://developer.mozilla.org/en-US/docs/Learn_web_development/Extensions/Server-side/First_steps/Client-Server_overview> (Accessed: 19 September 2025)  
[^6] Postman. (2025). _What are HTTP headers?_. Postman Blog. Available at: <https://blog.postman.com/what-are-http-headers/> (Accessed: 19 September 2025)
[^7] React. (2025). _Reacting to Input with State_. React Documentation. Available at: <https://react.dev/learn/reacting-to-input-with-state> (Accessed: 19 September 2025)
[^8] Express.js. (2025). _Using Middleware_. Express.js Documentation. Available at: <https://expressjs.com/en/guide/using-middleware.html> (Accessed: 19 September 2025)
[^9]
[^10]
[^11]
[^12]
[^13]

Computer Hope. (2025). _Client-Server Model_. Available at: <https://www.computerhope.com/jargon/c/clientse.htm> (Accessed: 19 September 2025)
Mongoose. (2025). _Mongoose Guide_. Available at: <https://mongoosejs.com/docs/guide.html> (Accessed: 19 September 2025)  
Mongoose. (2025). _Validation_. Available at: <https://mongoosejs.com/docs/validation.html> (Accessed: 19 September 2025)  
npm. (2025). _jsonwebtoken package_. Available at: <https://www.npmjs.com/package/jsonwebtoken> (Accessed: 19 September 2025)  
npm. (2025). _bcrypt package_. Available at: <https://www.npmjs.com/package/bcrypt> (Accessed: 19 September 2025)  
TheUdemezue. (2025). _How to Use JWT Token in React.js_. Dev.to. Available at: <https://dev.to/theudemezue/how-to-use-jwt-token-in-react-js-211c> (Accessed: 19 September 2025)  
Sharma, K. (2025). _Server-Side Caching vs Client-Side Caching_. Medium. Available at: <https://medium.com/@kumud.sharma.0206/server-side-caching-vs-client-side-caching-a-system-design-perspective-cf2ebae73c42> (Accessed: 19 September 2025)
