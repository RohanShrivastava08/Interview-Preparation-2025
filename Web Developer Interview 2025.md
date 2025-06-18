
### 🟠 **HTML (HyperText Markup Language)**

1. **What is HTML?**  
    HTML (HyperText Markup Language) is the standard language used to create and structure content on the web.
    
2. **What are HTML tags?**  
    Tags define elements in HTML, usually with an opening (`<tag>`) and closing (`</tag>`) syntax.
    
3. **What is the difference between HTML4 and HTML5?**  
    HTML5 introduced new semantic elements (`<article>`, `<section>`), multimedia support (`<audio>`, `<video>`), and APIs like localStorage and geolocation.
    
4. **What is semantic HTML?**  
    Semantic HTML uses meaningful tags like `<nav>`, `<main>`, `<footer>` to improve readability and accessibility.
    
5. **What are void (self-closing) elements in HTML?**  
    Tags that don’t need a closing tag, e.g., `<img>`, `<br>`, `<input>`, `<hr>`.
    
6. **What is the purpose of the `alt` attribute on images?**  
    It provides alternative text if the image fails to load and helps with accessibility.
    
7. **What is the difference between `<div>` and `<span>`?**  
    `<div>` is a block-level element, while `<span>` is an inline element.
    
8. **What is the DOCTYPE in HTML?**  
    It tells the browser the version of HTML being used. Example: `<!DOCTYPE html>` for HTML5.
    
9. **Can you nest block-level elements inside inline elements?**  
    No. Block-level elements like `<div>` should not be placed inside inline elements like `<span>`.
    
10. **How do you make a hyperlink open in a new tab?**  
    Use `target="_blank"` in the `<a>` tag:
    `<a href="https://example.com" target="_blank">Visit</a>`

---
---
### 🟣 **CSS (Cascading Style Sheets)**

11. **What is CSS?**  
    CSS is used to style HTML elements, controlling layout, colors, fonts, and spacing.
    
12. **What is the difference between ID and Class in CSS?**  
    `ID` is unique (`#id`) and used once; `Class` (`.class`) can be reused across elements.
    
13. **What is the Box Model in CSS?**  
    It includes:  
    `Content → Padding → Border → Margin`
    
14. **What are pseudo-classes in CSS?**  
    Pseudo-classes define special states:  
    Example: `:hover`, `:first-child`, `:nth-child(n)`
    
15. **Difference between absolute, relative, fixed, and sticky positioning?**
    

- `relative`: Positioned relative to its normal position
    
- `absolute`: Relative to the nearest positioned ancestor
    
- `fixed`: Relative to the viewport
    
- `sticky`: Sticks within a scroll range
    

16. **What is specificity in CSS?**  
    It determines which style is applied when multiple rules match. Inline > ID > Class > Tag
    
17. **How can you apply the same style to multiple elements?**  
    Use a common class name and apply styles using `.classname { ... }`.
    
18. **How to import a CSS file into another?**  
    Use `@import 'style.css';` or link both in HTML.
    
19. **What is the difference between `inline`, `block`, and `inline-block`?**
    

- `inline`: No new line, can’t set width/height
    
- `block`: Starts on new line, can set width/height
    
- `inline-block`: Like inline, but can set dimensions
    

20. **What is a media query in CSS?**  
    Used for responsive design to apply styles conditionally:
    `@media (max-width: 600px) { ... }`

---
---
### 🟡 **JavaScript (JS)**

21. **What is JavaScript?**  
    JavaScript is a high-level, interpreted programming language used to create dynamic and interactive web pages.
    
22. **What is the difference between `var`, `let`, and `const`?**
    

- `var`: Function-scoped, hoisted
    
- `let`: Block-scoped, not hoisted
    
- `const`: Block-scoped, constant value
    

23. **What is hoisting in JavaScript?**  
    Variable and function declarations are moved to the top of their scope before code execution.
    
24. **What are closures in JavaScript?**  
    A closure is a function that remembers variables from its lexical scope even when executed outside that scope.
    
25. **What’s the difference between `==` and `===` in JavaScript?**
    
- `==`: Loose equality, converts types
    
- `===`: Strict equality, checks type and value
---
---
### 🟢 **DOM & Events**

26. **What is the DOM (Document Object Model)?**  
    The DOM is a programming interface that represents the structure of HTML documents as a tree of objects.
    
27. **How do you access elements in the DOM using JavaScript?**  
    Using methods like:
    

- `document.getElementById("id")`
    
- `document.querySelector(".class")`
    
- `document.querySelectorAll("div")`
    

28. **What is event delegation in JavaScript?**  
    Event delegation allows you to add a single event listener to a parent element to handle events from its children using `event.target`.
    
29. **What is event bubbling and capturing?**
    

- **Bubbling**: Event flows from the target element up to the root.
    
- **Capturing**: Event flows from the root down to the target.
    

30. **How to prevent event bubbling?**  
    Use `event.stopPropagation()` to stop the event from propagating further.
    
31. **What is `addEventListener` and its syntax?**  
    Adds an event listener to an element:
    

js

CopyEdit

`element.addEventListener('click', functionName);`

32. **How to remove an event listener?**  
    Use `removeEventListener()` with the same function reference:
    

js

CopyEdit

`element.removeEventListener('click', functionName);`

33. **What are different types of DOM events?**  
    Common events include:
    

- `click`
    
- `keydown`, `keyup`
    
- `submit`
    
- `change`
    
- `mouseover`, `mouseout`
    

34. **What is the difference between `innerHTML` and `textContent`?**
    

- `innerHTML`: Parses and renders HTML
    
- `textContent`: Only gets/sets plain text
    

35. **How to dynamically create an element in JavaScript?**
    `const div = document.createElement('div'); div.textContent = 'Hello'; document.body.appendChild(div);`

---
---
### 🔵 **Git & Version Control**

36. **What is Git?**  
    Git is a distributed version control system for tracking code changes during software development.
    
37. **What is GitHub?**  
    GitHub is a cloud-based hosting service that lets you manage Git repositories and collaborate on projects.
    
38. **What is the difference between `git fetch` and `git pull`?**
    

- `git fetch`: Gets changes from the remote but doesn’t merge
    
- `git pull`: Fetches + merges changes into current branch
    

39. **How do you resolve a merge conflict in Git?**
    

- Edit the conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`)
    
- Save and stage the file
    
- Run `git commit`
    

40. **What is a Git branch?**  
    A branch is a lightweight movable pointer to a commit, used for parallel development.
    
41. **What is the purpose of `.gitignore` file?**  
    It tells Git which files/folders to ignore and not track (e.g., `node_modules/`, `.env`).
    
42. **How do you clone a Git repository?**
    `git clone https://github.com/user/repo.git`

43. **What is the command to initialize a Git repository?**
    `git init`

44. **How to stage and commit files in Git?**
    `git add .   git commit -m "Commit message"`

45. **What is `git status` used for?**  
    It shows the current state of the working directory and staging area.

---
---

### 🟤 **React.js (Frontend Library)**

46. **What is React?**  
    React is a JavaScript library for building component-based user interfaces, developed by Facebook.
    
47. **What is JSX in React?**  
    JSX is a syntax extension that lets you write HTML in JavaScript:
    `const element = <h1>Hello</h1>;`

48. **What are props in React?**  
    Props (short for properties) are used to pass data from parent to child components. They are read-only.
    
49. **What is state in React?**  
    State is local data managed within a component and can change over time using `useState`.
    
50. **What are React Hooks?**  
    Hooks are functions like `useState`, `useEffect`, etc., that let you use state and lifecycle features in functional components.
---
---

### 🔴 **Advanced JavaScript**

51. **What is the difference between synchronous and asynchronous code?**
    

- **Synchronous**: Code runs one line after another.
    
- **Asynchronous**: Code runs in the background and doesn't block execution (e.g., setTimeout, fetch).
    

52. **What are Promises in JavaScript?**  
    Promises handle async operations. They can be:
    
- `Pending`
    
- `Fulfilled`
    
- `Rejected`

53. **What is `async/await` in JavaScript?**  
    Syntax for handling Promises more cleanly. Example:
    `async function fetchData() {   const res = await fetch(url);   const data = await res.json(); }`

54. **What is a callback function?**  
    A function passed as an argument to another function, invoked later.
    
55. **What is a higher-order function?**  
    A function that takes another function as an argument or returns a function.
    
56. **What is the event loop in JavaScript?**  
    The mechanism that handles asynchronous operations and executes callbacks after the stack is clear.
    
57. **What is `this` in JavaScript?**  
    Refers to the context in which a function is called. In objects, it refers to the object.
    
58. **What is the difference between `call()`, `apply()`, and `bind()`?**
    

- `call`: Calls a function with a given `this` and args
    
- `apply`: Same as `call` but args as an array
    
- `bind`: Returns a new function with `this` bound
    

59. **What is currying in JavaScript?**  
    Transforming a function with multiple arguments into a sequence of functions each with a single argument.
    
60. **What is memoization?**  
    Caching the result of a function call for future reuse to improve performance.

---
---

### 🟣 **APIs & RESTful Services**

61. **What is an API?**  
    API (Application Programming Interface) is a way for systems to communicate over the web.
    
62. **What is REST API?**  
    REST (Representational State Transfer) is a design pattern using standard HTTP methods: GET, POST, PUT, DELETE.
    
63. **What is the difference between GET and POST methods?**
    

- **GET**: Retrieves data, visible in URL
    
- **POST**: Sends data, not visible in URL
    

64. **What is JSON?**  
    JSON (JavaScript Object Notation) is a lightweight format to exchange data between a server and client.
    
65. **What is the purpose of `fetch()` in JavaScript?**  
    It is used to make network requests and returns a Promise:
    `fetch(url).then(res => res.json()).then(data => console.log(data));`

66. **What are status codes in HTTP? Give examples.**
    

- 200: OK
    
- 201: Created
    
- 404: Not Found
    
- 500: Server Error
    

67. **What are headers in HTTP requests?**  
    Metadata like `Content-Type`, `Authorization`, etc., sent with requests.
    
68. **How to send data using POST method in fetch?**
    `fetch('/api', {   method: 'POST',   headers: { 'Content-Type': 'application/json' },   body: JSON.stringify(data) });`

69. **What is CORS?**  
    Cross-Origin Resource Sharing allows restricted resources to be requested from another domain.
    
70. **How do you handle API errors in JavaScript?**  
    Using `.catch()` or `try-catch` with `async/await`:
    `try {   const res = await fetch(url);   if (!res.ok) throw new Error('API error'); } catch (err) {   console.error(err); }`

---
---

### 🟡 **Node.js & Express.js**

71. **What is Node.js?**  
    Node.js is a runtime environment that allows you to run JavaScript on the server side.
    
72. **What is NPM?**  
    Node Package Manager — used to install, manage packages/libraries in a Node.js project.
    
73. **What is Express.js?**  
    A fast, minimalist web framework for Node.js to build APIs and web apps.
    
74. **How do you create a simple server using Express?**
    `const express = require('express'); const app = express(); app.get('/', (req, res) => res.send('Hello World')); app.listen(3000);`

75. **What is middleware in Express?**  
    Functions that execute during the request-response cycle. Example:
    `app.use((req, res, next) => {   console.log('Logged');   next(); });`

---
---

### 🟢 **MongoDB (NoSQL Database)**

76. **What is MongoDB?**  
    MongoDB is a NoSQL database that stores data in JSON-like documents with dynamic schemas.
    
77. **What is the difference between SQL and NoSQL?**
    

- **SQL**: Relational, table-based
    
- **NoSQL**: Document-based, schema-less
    

78. **How do you insert data into MongoDB?**  
    Using the `insertOne()` or `insertMany()` methods:
    `db.users.insertOne({ name: "John", age: 25 });`

79. **How do you find data in MongoDB?**
    `db.users.find({ name: "John" });`

80. **What is Mongoose?**  
    Mongoose is an ODM (Object Data Modeling) library for MongoDB and Node.js that provides schema-based solutions.

---
---

### 🔒 **Security**

81. **What is HTTPS?**  
    HTTPS (HyperText Transfer Protocol Secure) encrypts data transferred between browser and server using SSL/TLS.
    
82. **What is XSS (Cross-site Scripting)?**  
    An attack where malicious scripts are injected into web pages viewed by users. Prevent using input sanitization and CSP.
    
83. **What is CSRF (Cross-Site Request Forgery)?**  
    An attack where unauthorized commands are sent from a trusted user. Mitigation includes CSRF tokens and same-site cookies.
    
84. **How to protect passwords in a web app?**
    

- Hash passwords using bcrypt or Argon2
    
- Never store plain-text passwords
    

85. **What is Content Security Policy (CSP)?**  
    CSP is a browser feature that helps prevent XSS attacks by restricting resource loading policies.

---
---

### 🚀 **Deployment & Hosting**

86. **How do you deploy a website?**
    

- Frontend: Use Netlify, Vercel, GitHub Pages
    
- Fullstack: Use services like Render, Railway, Heroku, or VPS with Node.js + Nginx
    

87. **What is the difference between development and production modes?**
    

- **Development**: With debugging, hot reload
    
- **Production**: Optimized, minified, error logging enabled
    

88. **What is a CDN?**  
    Content Delivery Network — delivers content from geographically distributed servers for faster access.
    
89. **How to optimize a website for speed?**
    

- Minify CSS/JS
    
- Compress images
    
- Use lazy loading
    
- Use caching and CDN
    

90. **What is server-side rendering (SSR)?**  
    HTML is rendered on the server and sent to the browser — faster initial load and SEO benefits.

---
---

### ♿ **Web Accessibility (a11y)**

91. **What is Web Accessibility?**  
    Designing websites that can be used by people with disabilities, including those using screen readers.
    
92. **What are ARIA roles?**  
    ARIA (Accessible Rich Internet Applications) roles provide extra accessibility info to assistive technologies.
    
93. **How to improve keyboard navigation in web apps?**
    

- Use semantic tags
    
- Manage focus properly
    
- Provide visible focus indicators
    

94. **What is the purpose of `alt` text in images?**  
    Describes the image content for screen readers and in case the image doesn’t load.
    
95. **Which tools can be used to test accessibility?**
    

- Lighthouse (Chrome DevTools)
    
- Axe
    
- NVDA (Screen reader)

---
---

### 🟡 **Performance & Optimization**

96. **How to reduce website load time?**
    

- Minify assets
    
- Code splitting
    
- Use lazy loading
    
- Cache static assets
    

97. **What is lazy loading?**  
    Images, components, or data are only loaded when they are about to be viewed (e.g., as the user scrolls).
    
98. **What is debouncing and throttling?**
    

- **Debouncing**: Limits function execution until a pause (e.g., search input)
    
- **Throttling**: Ensures a function executes at most once per interval (e.g., scroll events)
    

99. **What is Time to First Byte (TTFB)?**  
    The time taken by the browser to receive the first byte from the server — a key performance metric.
    

---

### 🧑‍💼 **HR & Miscellaneous**

100. **Why should we hire you as a web developer?**  
    “I have strong frontend and backend development skills, hands-on experience with real-world projects, and I’m passionate about clean code, performance, and solving user problems. I’m ready to contribute from day one and grow with the team.”

---
---

