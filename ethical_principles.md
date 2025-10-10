# Ethical Web Development Principles

In 1997, [this software engineering code of ethics (Gotterbarn, D., Miller, K. and Rogerson, S., 1997)](https://dl.acm.org/doi/10.1145/265684.265699) was published by collaboration of IEEE-CS (Institute of Electrical and Electronics Engineers - Computer Society) and ACM (Association for Computer Machinery), becoming the de-facto globally recognized code of ethics for software engineering. Since then, it has remained the global standard, as evidenced by [this wikipedia article (Wikipedia contributors, 2019)](https://en.wikipedia.org/wiki/Programming_ethics) which still cites this code as the standard in the "Programming Ethical Guidelines" section. Since then, both IEEE-CS and ACM maintain an [updated version of the code (Association for Computing Machinery, 2024)](https://www.acm.org/code-of-ethics/software-engineering-code) (currently version 5.2)

From the above code of ethics (henceforth CoE), as well as ACM's respected separately created [Code of Ethics and Professional Conduct (Association for Computing Machinery, 2018)](https://www.acm.org/code-of-ethics) (henceforth CoEPC), we will identify and explain how our planned project will adhere to some of the relevant codes/principles.

---

## Approve Only Safe Software

**CoE 1.03. Approve software only if they have a well-founded belief that it is safe, meets specifications, passes appropriate tests, and does not diminish quality of life, diminish privacy or harm the environment. The ultimate effect of the work should be to the public good:**

This principle is most relevant to our project regarding the handling of personal and login information. As our users will be able to register accounts, providing an email address and password for registration, care must be taken to follow industry practices regarding the handling of such data. Users unfortunately often re-use passwords across different sites and applications, so compromising our users data could have potentially devastating effects for them. Our plans for ensuring adherence to this principle will require the following:

- **Hashing Passwords:**
  We will use the Bcrypt library to salt and hash the password using the Blowfish cipher prior to storing in the database, rather than storing unsecured plain text.[(Dan Arias, 2021)](https://auth0.com/blog/hashing-in-action-understanding-bcrypt/)
- **Minimum Password Requirements:**
  Using input validation upon account creation to ensure passwords meet standard password security requirements (i.e min length, no common patterns, requiring mixed alphanumeric characters)
- **Protect Routes with JWT Middleware:**
  Generate JWT (JSON Web Token) for each user using the 'jsonwebtoken' library, after validating them on login, and use middleware to authenticate that the request header contains the valid JWT before allowing access to routes containing data unique to the user. In our project, this could be to access their personal information (such as registered email address), as well as other general features specific to the user (such as their personalized movie reviews)[(Khan, H., 2024)](https://dev.to/hamzakhan/securing-your-expressjs-app-jwt-authentication-step-by-step-aom)
- **Testing Exposure of Sensitive Information:**
  Use the external library "Jest" to test routes, JWT generation and validation, and hashing and salting of passwords. Test to ensure that the returned passwords in headers are hashed and salted, and that users cannot access routes without correct authorization through relevant middleware.

---

## Respect Creative Works

**CoEPC 1.5. Respect the work required to produce new ideas, inventions, creative works, and computing artifacts.**

Our proposed project will revolve around movies, and the depiction of those movies will include movie posters. Almost all movie posters are copyrighted creative works, owned by the studio or the artist that produced them, with strict rules on the use of said works. Additionally, our planned project will make use of many external libraries, including (but not limited to) Express, React, Mongoose, Bcrypt, jsonwebtoken etc. These external libraries each individually have their own licenses detailing terms of use, and adhering to them and the copyright requirements of movie posters can be achieved in the following ways:

- **Following Copyright Requirements:**
  Since this project will be created in Australia, I will be referencing Australian copyright law as outlined by the Australian Copyright Council. The Copyright Act 1968 "allows people to use copyright material without the copyright owner's permission in certain situations, including fair dealing for specific purposes". The Fair Dealings Fact Sheet [(Australian Copyright Council, 2025)](https://s3-ap-southeast-2.amazonaws.com/dimoacc/factsheets/INFO079.pdf?t=2508130836) states: "Under the fair dealing exceptions... copyright material may be used without permission... for one of the specified purposes." Included in the list is "Criticism or review", and expanding on that it is noted "criticism or review... will not be considered to be an infringement... provided that there is sufficient acknowledgement... If the person has other motives... using the material to make a profit or... to divert customers from the competitor – the fact that they have also engaged in a form of criticism or review is not enough to prevent the use from infringing copyright."
  \
  From the above, it is clear that our proposed project meets the copyright requirements around fair use as we will be acknowledging the ownership of the promotional material, not using the material to make a profit, and not diverting customers from competitors using the material. It is important to note that if hosting of the project was to occur in any other country (i.e. hosting our database in New Zealand) we would need to consult the relevant copyright laws of that country and adhere to them. For further legal advice, a request can be submitted to the Copyright Council of Australia or assistance can be provided from the other organizations referenced in their legal advice help page [(Australian Copyright Council, 2025)](https://www.copyright.org.au/legal-advice/)

- **Use Only Licensed External Libraries:**
  Public licensed javascript libraries can be found on the npm website [(npm, 2019)](https://www.npmjs.com/), and list the license used by the package. The relevant license for each package used must be adhered to within the project.
- **Acknowledge Libraries:**
  In the project documentation, we will provide acknowledgement and credit to any external libraries used, as well as listing their licenses, versions and any modifications made. An example of this can be seen in the 'DEPENDENCIES' documentation [(truth-josstice, 2025)](https://github.com/truth-josstice/dev1001_assignment2/blob/main/DEPENDENCIES.md#custom-modified-libraries-used) created by this team for our previous group project.

---

## Consider the Needs of All

**CoE 1.07. Consider issues of physical disabilities, allocation of resources, economic disadvantage and other factors that can diminish access to the benefits of software:**

Our project should strive to be inclusive for all people using it where possible, accounting for differences of physical capabilities and access to software/hardware. This can be achieved in the following ways:

- **Cater for Visually Impaired:**
  The Virtual Screen Reader external library [(guidepup, 2025)](https://www.npmjs.com/package/@guidepup/virtual-screen-reader) allows for tests to be written to test what screen readers will say when accessing the site. In combination with unit testing, writing semantic HTML, and adhering to the guiding principles of [this guide on building a screen reader friendly site (Jaggi, T., 2017)](https://www.accessibility-developer-guide.com/knowledge/screen-readers/how-to-implement/), we can successfully build a site that caters to the visually impaired.
- **Cater for Legacy Hardware and Browsers:** As developers, we are often fortunate to have relatively advanced and powerful hardware, using regularly updated browsers to view content, however it's important to note that many users will be using legacy hardware and browsers. Babel is a transpiler that takes our modern JavaScript code and outputs a set of files with browser compatible syntax, without effecting functionality. Although it can be used online, for our project it would be best installed by following the CLI installation instructions [found here (Babel, 2015)](https://babeljs.io/setup#installation). Additionally, the TinyBench package [(Mohammad Bagher, 2025)](https://www.npmjs.com/package/tinybench) is a simple, lightweight and easy to use benchmarking package we can incorporate into our project to verify performance, referring to the MDN WebDocs section on performance optimization [(MDN Contributors, 2024)](https://developer.mozilla.org/en-US/docs/Learn_web_development/Extensions/Performance/JavaScript). This will ensure our website can run with minimal performance overhead, improving compatibility with low performance hardware.

---

## Respect Privacy

**CoEPC 1.6. Respect privacy:**

Since our project will be collecting and storing some personal data (i.e. email addresses, passwords, friend lists, preferences etc.), we need to ensure we are storing and using this data legitimately, collecting the minimum amount of data needed, and staying informed of the rights and responsibilities of collecting personal data. The Australian Privacy Principles [(OAIC, 2024)](https://www.oaic.gov.au/privacy/australian-privacy-principles/australian-privacy-principles-quick-reference) provide a useful guide for how we can achieve that, and here are some of the ways our project will be adhering to them:

- **Open and transparent management of personal information:**
  Our project will include a privacy policy in its documentation, outlining the types of data collected and how its stored, how we will use it, how it can be accessed, and any other requirements outlined by OAIC [(OAIC, 2023)](https://www.oaic.gov.au/privacy/your-privacy-rights/your-personal-information/what-is-a-privacy-policy). An example of a previously created privacy policy by our team [(truth-josstice, 2025)](https://github.com/truth-josstice/dev1001_assignment2?tab=readme-ov-file#privacy-policy).
- **Security of personal information:**
  As mentioned in the [Approve Only Safe Software](#approve-only-safe-software) section, the use of hashing and salting to secure passwords, JWT middleware to secure routes, and Jest testing to test exposure of sensitive information will all be used to maintain security of personal information.
- **Allow Changing and Deletion of Data:**
  To remain aligned with APP requirements, routes will be created to allow users to update or delete their personal information on the site, including deletion of their account.

## References

| References                                                                                                                                                                                                                                                            |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Gotterbarn, D., Miller, K. and Rogerson, S. (1997). _Software engineering code of ethics._ Available at: <https://dl.acm.org/doi/10.1145/265684.265699> (Accessed: 26 Sep. 2025).                                                                                     |
| Wikipedia contributors (2019). _Programming ethics. Wikipedia._ Available at: <https://en.wikipedia.org/wiki/Programming_ethics> (Accessed: 26 Sep. 2025).                                                                                                            |
| Association for Computing Machinery (2024). _The Software Engineering Code of Ethics and Professional Practice._ Acm.org. Available at: <https://www.acm.org/code-of-ethics/software-engineering-code> (Accessed 26 Sep. 2025).                                       |
| Association for Computing Machinery (2018). _ACM Code of Ethics and Professional Conduct._ Association for Computing Machinery. Available at: <https://www.acm.org/code-of-ethics> (Accessed 26 Sep. 2025).                                                           |
| Dan Arias (2021). _Hashing in Action: Understanding bcrypt._ Auth0 - Blog. Available at: <https://auth0.com/blog/hashing-in-action-understanding-bcrypt/> (Accessed 27 Sep. 2025).                                                                                    |
| Khan, H. (2024). _Securing Your Express.js App: JWT Authentication Step-by-Step._ DEV Community. Available at: <https://dev.to/hamzakhan/securing-your-expressjs-app-jwt-authentication-step-by-step-aom> (Accessed 27 Sep. 2025).                                    |
| Australian Copyright Council (2025). _Fair Dealing: What Can I Use?_ Amazonaws.com. Available at: <https://s3-ap-southeast-2.amazonaws.com/dimoacc/factsheets/INFO079.pdf?t=2508130836> (Accessed 27 Sep. 2025).                                                      |
| Australian Copyright Council (n.d.). _Legal Advice Service._ Australian Copyright Council. Available at: <https://www.copyright.org.au/legal-advice/> (Accessed 27 Sep. 2025).                                                                                        |
| npm (2019). _npm \| build amazing things._ Npmjs.com. Available at: <https://www.npmjs.com/> (Accessed 27 Sep. 2025).                                                                                                                                                 |
| truth-josstice (2025). _dev1001 assignment2 dependencies_ GitHub. Available at: <https://github.com/truth-josstice/dev1001_assignment2/blob/main/DEPENDENCIES.md#custom-modified-libraries-used> (Accessed 28 Sep. 2025).                                             |
| guidepup (2025). _@guidepup/virtual-screen-reader._ npm. Available at: <https://www.npmjs.com/package/@guidepup/virtual-screen-reader> (Accessed 28 Sep. 2025).                                                                                                       |
| Jaggi, T. (2017). _How to implement websites that are ready for screen reader usage._ Accessibility Developer Guide. Available at: <https://www.accessibility-developer-guide.com/knowledge/screen-readers/how-to-implement/> (Accessed 28 Sep. 2025).                |
| Babel (2015). _Using Babel._ Babeljs.io. Available at: <https://babeljs.io/setup#installation> (Accessed 29 Sep. 2025).                                                                                                                                               |
| Mohammad Bagher (2025). _tinybench._ npm. Available at: <https://www.npmjs.com/package/tinybench> (Accessed 29 Sep. 2025).                                                                                                                                            |
| MDN contributors (2024). _JavaScript performance optimization._ MDN Web Docs. Available at: <https://developer.mozilla.org/en-US/docs/Learn_web_development/Extensions/Performance/JavaScript> (Accessed 29 Sep. 2025).                                               |
| OAIC (2024). _Australian Privacy Principles Quick Reference._ Office of the Australian Information Commissioner. Available at: <https://www.oaic.gov.au/privacy/australian-privacy-principles/australian-privacy-principles-quick-reference> (Accessed 29 Sep. 2025). |
| OAIC (2023). _What is a privacy policy?_ OAIC. Available at: <https://www.oaic.gov.au/privacy/your-privacy-rights/your-personal-information/what-is-a-privacy-policy> (Accessed 30 Sep. 2025).                                                                        |
| truth-josstice (2025). _dev1001 assignment2 Privacy Policy_ GitHub. Available at: <https://github.com/truth-josstice/dev1001_assignment2?tab=readme-ov-file#privacy-policy> (Accessed 28 Sep. 2025).                                                                  |
