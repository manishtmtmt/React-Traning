## 1. Why do we use Git?

**Ans:** _Git is a tool for managing projects with ease (track files and their changes)_

**Explanation:** Git is a tool that allows to track all changes to the project folder. It keeps different copies of the project at any stage of the devepopment and allows you to efficiently manipulate file updates. Git is use by every developer in the world.

## 2. Why use Promise.all?

**Ans:** _To process multiple independent promises concurrently instead of one by one_

**Explanation:** Promise.all is used when there are multiple independent promises that must be resolved/executed all at once. With Promise.all promises are processed concurrently instead of one by one.

## 3. What is a javascript module?

**Ans:** _javaScript module is self-contained .js file that does not rely on the global scope_

**Explanation:** JavaScript module is a self-contained .js file that does not rely on outer global scope. To share data between modules data must be imported and exported in order to use it.

## 4. If one says: that website is written in React. How will you understand this statement?

**Ans:** _a) relies on React as its front-end technology; b) uses components; c) most probably behaves as a Single Page Application_

**Explanation:** If a website is written in React, it means that the website a) uses components; b) relies on React as its core front-end library; c) most probably behaves as a SPA (Single Page App). Term "most probably" is used because React != SPA. With modern technologies, React can be used for server-side rendering too. And the gotcha here is that server-side rendered apps can also behave as SPAs (no need for page refresh).

## 5. What is JSON?

**Ans:** _JSON is a file format used to transfer data on the web_

**Explanation:** JSON is a file format and extension that is used to transfer data on the internet. It resembles a javascript object and indeed because JSON stands for JavaScript Object Notation.

## 6. Is React library or framework?

**Ans:** _Library_

**Explanation:** React is only a library. You can find different frameworks on the web that use React as its core technology, but these are tools built arount React.

## 7. What is NodeJS?

**Ans:** _NodeJS is javascript runtime environment for executing JavaScript outside of browsers_

**Explanation:** NodeJS is a javascript runtime environment that allows to execute javascript basically anywhere outside of the browser (servers, mobile phones, IoT, desktop)

## 8. Choose on correct statement

**Ans:** _GraphQL has single endpoint while REST has multiple endpoints_

**Explanation:** REST servers have multiple endpoints and return data model defined by the requested endpoint. (GET request to "/user/15" will return user fields defined on the server).
GraphQL servers have single endpoint /graphql. Returns to that endpoint must have a query written in GraphQL query language. What fields and what data to receive from the server is written in the query.
REST uses multi-entrypoint approach where every endpoint dictates what it will do.
GraphQL uses single-entrypoint approach where user dictates what data he manipulates in form GraphQL query language.

## 9. What is a SPA (Single Page App)?

**Ans:** _SPAs are websites managed by JavaScript and they behave more like native appss_

**Explanation:** SPA is a website fully managed by javascript. From the server only bare bones "index.html" skeleton is received. DOM manipulation and page transitions are done by JS that runs in browser. SPA are intended to look more like native mobile apps.

## 10. Name two types of React components

**Ans:** _Function-based and class-based_

**Explanation:** Thare are two types of component you can create: function-based and class-based.
Class-based components, by some people, have been comsidered "old syntax" since React hooks release. React hooks solved problems that class-based components had. Hooks can be used only in function-based components.

## 11. Can NodeJS be used in a browser?

**Ans:** _No, that's not the point of NodeJS_

**Explanation:** NodeJs is a javascript runtime environment that allows to execute javascript basically anywhere outside of the browser (servers, mobile phones, IoT, desktop). It can't be used inside browser environment.

## 12. What is the main advantage of SPA?

**Ans:** _Behaves as a native mobile app_

**Explanation:** SPAs are intended to look and behave more like native mobile apps. That's basically all.

## 13. Imagine you create an arrow function at line 5. Then you try to call this function at line 2. What is going to happen?

**Ans:** _JS will produce a reference error_

**Explanation:** JavaScript will produce a reference error because you try to call an arrow function (line 2) before it was defined (line 5). Arrow functions are javascript expressions and are processed one by one as they appear in the code.

## 14. Which one is a primitive GIT workflow to create new local commit

**Ans:** _git add -> git commit_

**Explanation:** git add -> git commit is the only correct option.
When there are new changes that must be recognized by Git. You first make all new changes recognized by Git (git add) and once new changes are ready to be saved to Git (git commit).

## 15. Are Github and Git same things?

**Ans:** _No. Git is a tool for project management. Github is a service that hosts git projects online_

**Explanation:** Git is a tool for project management. Github is a service that hosts git projects online. Git project can be hosted on other services too (e.g., GitLab)

## 16. What is NPM?

**Ans:** _NPM is a tool for managing packages in NodeJS projects_

**Explanation:** NPM stands for node package manager. NPM is a tool for managing packages (dependencies) in NodeJS projects

## 17. How many ways exist to install an npm package?

**Ans:** _3_

**Explanation:** NPM package can installed in 3 different ways: globally (npm i -g), as a project dependency (npm i), as a developer dependency in a project (npm i --save-dev)

## 18. Why components are useful?

**Ans:** _1) Allow to reuse HTML logic multiple time 2) Consistent 3) Isolated_

**Explanation:**

-> Components allow to reuse and share logic.

-> Reusability involves consistency, meaning that one component reused multiple times will produce the same result.

-> A component doesn't need to know what happens outside (e.g. <Table /> is not aware of h1 tag title outside of it)

## 19. Name three features that are part of React

**Ans:** _Virtual DOM, React Fiber, Flux_

**Explanation:**

Flux - react's architecture pattern, it decribes how data flows in React

React Fiber - a set of core React algorithms

Virtual DOM - in-memory representation of real DOM that internally used by React

## 20. What is async/await syntax?

**Ans:** _Async/await is built on top of Promises. Its intention is to make Promise look more synchronous and readable_

**Explanation:** Async/await is syntax built on top of Promises to make Promises (async code) look more synchronous

## 21. A promise can be either ...?

**Ans:** _Resolved or Rejected_

**Explanation:** A Promise can be either 1) Resolved or 2) Rejected. When in one of these states, a promise is considered to be settled.

## 22. Is it correct that Virtual DOM == DOM?

**Ans:** _No. Virtual DOM resides in-memory and used only internally by React while DOM is part of every web document (webpage)_

**Explanation:** Virtual DOM is NOT real DOM (document object model). Virtual DOM resides in memory and used only internally by React to reduce number of real DOM operations.
