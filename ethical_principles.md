# Ethical Web Development Principles

In 1997, [this software engineering code of ethics](https://dl.acm.org/doi/10.1145/265684.265699)[^1] was published by collaboration of IEEE-CS (Institute of Electrical and Electronics Engineers - Computer Society) and ACM (Association for Computer Machinery), becoming the de-facto globally recognized code of ethics for software engineering. Since then, it has remained the global standard, as evidenced by [this wikipedia article](https://en.wikipedia.org/wiki/Programming_ethics)[^2] which still cites this code as the standard in the "Programming Ethical Guidelines" section. Since then, both IEEE-CS and ACM maintain an [updated version of the code](https://www.acm.org/code-of-ethics/software-engineering-code)[^3] (currently version 5.2)

From the above code of ethics (henceforth CoE), as well as ACM's respected separately created [Code of Ethics and Professional Conduct](https://www.acm.org/code-of-ethics)[^4] (henceforth CoEPC), we will identify and explain how our planned project will adhere to some of the relevant codes/principles.

## Approve Only Safe Software

**CoE 1.03. Approve software only if they have a well-founded belief that it is safe, meets specifications, passes appropriate tests, and does not diminish quality of life, diminish privacy or harm the environment. The ultimate effect of the work should be to the public good:**
This principle is most relevant to our project regarding the handling of personal and login information. As our users will be able to register accounts, providing an email address and password for registration, care must be taken to follow industry practices regarding the handling of such data. Users unfortunately often re-use passwords across different sites and applications, so compromising our users data could have potentially devastating effects for them. Our plans for ensuring adherence to this principle will require the following:

- **Hashing Passwords:** We will use the Bcrypt library to salt and hash the password using the Blowfish cipher prior to storing in the database, rather than storing unsecured plain text.[^5]
- **Minimum Password Requirements:** Using input validation upon account creation to ensure passwords meet standard password security requirements (i.e min length, no common patterns, requiring mixed alphanumeric characters)
- **Protect Routes with JWT Middleware:** Generate JWT (JSON Web Token) for each user using the 'jsonwebtoken' library, after validating them on login, and use middleware to authenticate that the request header contains the valid JWT before allowing access to routes containing data unique to the user. In our project, this could be to access their personal information (such as registered email address), as well as other general features specific to the user (such as their personalized movie reviews)[^6]
- **Testing Exposure of Sensitive Information:** Use the external library "Jest" to test routes, JWT generation and validation, and hashing and salting of passwords. Test to ensure that the returned passwords in headers are hashed and salted, and that users cannot access routes without correct authorization through relevant middleware.

## Respect Creative Works

**CoEPC 1.5. Respect the work required to produce new ideas, inventions, creative works, and computing artifacts.**
Our proposed project will revolve around movies, and the depiction of those movies will include movie posters. Almost all movie posters are copyrighted creative works, owned by the studio or the artist that produced them, with strict rules on the use of said works. Additionally, our planned project will make use of many external libraries, including (but not limited to) Express, React, Mongoose, Bcrypt, jsonwebtoken etc. These external libraries each individually have their own licenses detailing terms of use, and adhering to them and the copyright requirements of movie posters can be achieved in the following ways:

## References

[^1]: [Software Engineering Code of Ethics](https://dl.acm.org/doi/10.1145/265684.265699)
[^2]: [Programming Ethics - Wikipedia](https://en.wikipedia.org/wiki/Programming_ethics)
[^3]: [Software Engineering Code of Ethics - ACM](https://www.acm.org/code-of-ethics/software-engineering-code)
[^4]: [Code of Ethics and Professional Conduct - ACM](https://www.acm.org/code-of-ethics)
[^5]: [Understanding Bcrypt - Auth0](https://auth0.com/blog/hashing-in-action-understanding-bcrypt/)
[^6]: [JWT Authentication Step by Step - Dev](https://dev.to/hamzakhan/securing-your-expressjs-app-jwt-authentication-step-by-step-aom)
