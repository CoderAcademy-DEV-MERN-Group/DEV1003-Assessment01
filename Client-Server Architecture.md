# Client-Server Architecture

[Introduction paragraph: How client server architecture works, what the main components are (listed below in subheadings), what our client is (React) and what our server is (Express). Include references (MDN Docs, JS docs, React docs, Express Docs at least)]

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

[Explanation of communication and how it works in our application: HTTP verbs, middleware, request/response]

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
[^4]
[^5]
[^6]
[^7]
[^8]
[^9]
[^10]
[^11]
[^12]
[^13]

Mozilla Developer Network. (2025). _Client-Server Overview_. MDN Web Docs. Available at: <https://developer.mozilla.org/en-US/docs/Learn_web_development/Extensions/Server-side/First_steps/Client-Server_overview> (Accessed: 19 September 2025)  

Computer Hope. (2025). _Client-Server Model_. Available at: <https://www.computerhope.com/jargon/c/clientse.htm> (Accessed: 19 September 2025)

Mongoose. (2025). _Mongoose Guide_. Available at: <https://mongoosejs.com/docs/guide.html> (Accessed: 19 September 2025)  
Mongoose. (2025). _Validation_. Available at: <https://mongoosejs.com/docs/validation.html> (Accessed: 19 September 2025)  
npm. (2025). _jsonwebtoken package_. Available at: <https://www.npmjs.com/package/jsonwebtoken> (Accessed: 19 September 2025)  
npm. (2025). _bcrypt package_. Available at: <https://www.npmjs.com/package/bcrypt> (Accessed: 19 September 2025)  
TheUdemezue. (2025). _How to Use JWT Token in React.js_. Dev.to. Available at: <https://dev.to/theudemezue/how-to-use-jwt-token-in-react-js-211c> (Accessed: 19 September 2025)  
Sharma, K. (2025). _Server-Side Caching vs Client-Side Caching_. Medium. Available at: <https://medium.com/@kumud.sharma.0206/server-side-caching-vs-client-side-caching-a-system-design-perspective-cf2ebae73c42> (Accessed: 19 September 2025)  
Das, S. (2025). _Client-Server Communication: A Deep Dive_. LinkedIn. Available at: <https://www.linkedin.com/pulse/client-server-communication-deep-dive-sandip-das-zljcc/> (Accessed: 19 September 2025)
