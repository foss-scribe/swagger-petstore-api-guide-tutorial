# README

This readme contains my notes and explains some of my thought processes regarding the exercise.

A brief introduction outlines the purpose, establishes some assumptions about the reader's abilities and notes the use of vanilla JavaScript in the code examples. I opted not to use a front-end framework or third-party library (i.e. Axios) because the goal is straightforward, and I wanted the output file to be self-contained and lean.

In the `About the Petstore API`, I introduce the API and identify critical technical points that a consumer of an API would find helpful. Had the task required one of the authenticated endpoints, I would have added an authentication guide too.

This section also includes a detailed guide on using the findByStatus. It describes the query parameters and provides example request and response examples. I like separating endpoint descriptions from tutorials so they can serve as a standalone, language-agnostic reference. You'll note I included cURL in my request because cURL is the lowest common denominator (everyone has it) and has no levels of abstraction. Similarly, I included the raw JSON response to illustrate what a developer can expect to receive upon a successful request. I would have documented those for completeness if the API included error responses.

In the `Building the HTML pet store` section, I walk the reader through building a basic page, querying the data and rendering out the list.

This section puts into practice what they've learnt in the API guide (`About the Petstore API`) and combines this with their assumed HTML/JavaScript and REST API knowledge. Because of their assumed knowledge, I didn't go into tremendous detail, only highlighting essential information like the requirement to handle the Promises returned by Fetch, which might throw developers used to working in Axios or a front-end framework that abstracts them away.

Note that I haven't styled the output as CSS wasn't a listed requirement, and I didn't think it necessary. I only rendered the `name` field because it was the API's only consistently helpful bit of data.

I've kept the tone deliberately conversational and informal, per the brief and my preferred style, because I think it improves a reader's retention and makes the document more approachable.

For the sake of completeness, I've added a `Next steps` section to serve as a concluding statement, call to action and a pointer to further reading.


**NOTE**: I made an additional code update the day after yesterday's (Friday) commit to handle null name values. I didn't appreciate how much this API would change with lots of people using it publicly with little in the way of field validation.

In case the API proves unreliable, I've created an alternative endpoint using a Cloud Function (written in Python, and deployed to DigitalOcean) that returns a dozen pets matching the scheme. It's commented out in petstore.html JavaScript.