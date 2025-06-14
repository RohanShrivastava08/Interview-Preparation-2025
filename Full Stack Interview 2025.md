## 🔷 **SECTION 1: HTML, CSS, Browser (Q1–10)**

### **1. What is the difference between HTML and XHTML?**

**Answer:**

- **HTML (HyperText Markup Language)** is forgiving of syntax errors (e.g., missing end tags).
    
- **XHTML (Extensible HTML)** follows stricter XML rules: all tags must be closed, lowercase, properly nested.
    
- XHTML is stricter and better for data interchange; HTML is better supported by browsers.
    

---

### **2. Explain the CSS Box Model.**

**Answer:**  
Every HTML element is a box made of:

- **Content**: The actual text/image.
    
- **Padding**: Space inside the border.
    
- **Border**: Edge of the box.
    
- **Margin**: Space outside the box.
    

---

### **3. What is the difference between `display: none` and `visibility: hidden`?**

**Answer:**

- `display: none`: Hides the element completely — no layout space is reserved.
    
- `visibility: hidden`: Hides the element **but still reserves its space** in layout.
    

---

### **4. What are semantic HTML tags?**

**Answer:**  
Semantic tags like `<article>`, `<nav>`, `<header>`, `<section>` define the **meaning** of the content.  
They:

- Improve accessibility
    
- Aid SEO
    
- Help developers understand structure
    

---

### **5. How does `position: absolute` work in CSS?**

**Answer:**  
`position: absolute` positions the element **relative to its nearest positioned ancestor** (`relative`, `absolute`, or `fixed`). If no ancestor is positioned, it's relative to the document body.

---

### **6. What are media queries?**

**Answer:**  
Media queries apply CSS rules based on **device characteristics** (e.g., width).

css

CopyEdit

`@media (max-width: 768px) {   .container { flex-direction: column; } }`

Used for **responsive design**.

---

### **7. What is the difference between SSR and CSR?**

**Answer:**

- **Server-Side Rendering (SSR):** HTML is generated on the server (e.g., Next.js).
    
- **Client-Side Rendering (CSR):** JavaScript runs in the browser and builds HTML dynamically (e.g., React SPA).
    
- SSR is better for SEO; CSR is better for interactive apps.
    

---

### **8. What is CORS?**

**Answer:**  
CORS (Cross-Origin Resource Sharing) is a **security feature** that controls how one domain can access resources on another.  
Handled via response headers like:

http

CopyEdit

`Access-Control-Allow-Origin: https://example.com`

---

### **9. What is the DOM and how does it relate to JavaScript?**

**Answer:**  
DOM (Document Object Model) is a **tree-like structure** representing HTML in the browser.  
JavaScript can use it to:

- Modify structure (`createElement`, `removeChild`)
    
- Update styles
    
- Handle events
    

---

### **10. Explain Critical Rendering Path.**

**Answer:**  
The Critical Rendering Path is the sequence of steps the browser performs to render a page:

1. HTML → DOM
    
2. CSS → CSSOM
    
3. DOM + CSSOM → Render Tree
    
4. Layout
    
5. Paint
    
6. Composite

---
---
## 🟦 **SECTION 2: JavaScript & ES6+ Concepts (Q11–30)**

---

### **11. What is the difference between `var`, `let`, and `const`?**

**Answer:**

- `var`: Function-scoped, hoisted, can be redeclared.
    
- `let`: Block-scoped, not hoisted in the same way, can't be redeclared in the same scope.
    
- `const`: Block-scoped, must be initialized, cannot be reassigned (but objects/arrays can be mutated).
    

---

### **12. What are closures in JavaScript?**

**Answer:**  
A closure is a function that **remembers its outer scope** even after the outer function has returned.

js

CopyEdit

`function outer() {   let count = 0;   return function inner() {     return ++count;   }; } const counter = outer(); counter(); // 1 counter(); // 2`

---

### **13. What is event delegation?**

**Answer:**  
Event delegation allows you to **attach a single event listener to a parent**, and handle events from child elements via event bubbling.

js

CopyEdit

`document.getElementById('list').addEventListener('click', function(e) {   if (e.target.tagName === 'LI') {     console.log(e.target.textContent);   } });`

---

### **14. What is the difference between synchronous and asynchronous code?**

**Answer:**

- **Synchronous**: Executes line-by-line, blocking.
    
- **Asynchronous**: Uses callbacks/promises/`async/await` to run non-blocking code (e.g., HTTP calls, timers).
    

---

### **15. How does JavaScript’s event loop work?**

**Answer:**

1. JS runs single-threaded.
    
2. The **call stack** executes synchronous code.
    
3. **Web APIs** handle async tasks (e.g., `fetch`, `setTimeout`).
    
4. Callback/promise resolutions go into the **task/microtask queue**.
    
5. Event loop pushes them back into the call stack when it's empty.
    

---

### **16. What is hoisting in JavaScript?**

**Answer:**  
Hoisting moves **variable and function declarations** to the top of their scope during compilation.

js

CopyEdit

`console.log(a); // undefined (hoisted var) var a = 5;  sayHi(); // works (function hoisted) function sayHi() { console.log('Hi'); }`

---

### **17. Difference between `==` and `===` in JS?**

**Answer:**

- `==`: Loose equality. Converts types if needed.
    
- `===`: Strict equality. **No type coercion**.
    

js

CopyEdit

`'5' == 5   // true '5' === 5  // false`

---

### **18. What are Promises and `async/await`?**

**Answer:**

- Promises handle asynchronous results:
    

js

CopyEdit

`fetch('/api').then(res => res.json());`

- `async/await` is syntactic sugar for promises:
    

js

CopyEdit

`async function getData() {   const res = await fetch('/api');   const data = await res.json(); }`

---

### **19. What are arrow functions and how are they different?**

**Answer:**

- **No `this` binding**: Arrow functions capture `this` from their lexical scope.
    
- More concise syntax.
    

js

CopyEdit

`const add = (a, b) => a + b;`

---

### **20. Difference between `map()`, `forEach()`, `filter()`?**

**Answer:**

- `map()`: Transforms array, returns new array.
    
- `forEach()`: Iterates, doesn't return.
    
- `filter()`: Returns array of items passing the condition.
    

---

### **21. Explain prototypal inheritance.**

**Answer:**  
In JS, objects can inherit from other objects using the prototype chain.

js

CopyEdit

``function Person(name) {   this.name = name; } Person.prototype.greet = function () {   return `Hello ${this.name}`; };``

---

### **22. What is `this` in JavaScript?**

**Answer:**  
`this` refers to the execution context.

- In global scope: `window` (browser).
    
- Inside function: depends on how it's called.
    
- In arrow functions: inherited from parent.
    

---

### **23. What are pure functions?**

**Answer:**  
Functions that:

- Always return the same output for the same input.
    
- Cause **no side effects** (no mutation of external data).
    

---

### **24. What is debouncing and throttling?**

**Answer:**

- **Debounce**: Delay function call until X ms after last call (e.g., input search).
    
- **Throttle**: Call function once every X ms, no matter how often triggered (e.g., scroll handler).
    

---

### **25. Difference between shallow and deep copy?**

**Answer:**

- **Shallow copy**: Top-level cloned, nested objects still share reference.
    

js

CopyEdit

`const a = { x: 1, y: { z: 2 } }; const b = { ...a }; // shallow`

- **Deep copy**: All levels cloned (use `structuredClone()` or `lodash`).
    

---

### **26. How to avoid memory leaks in JavaScript?**

**Answer:**

- Remove event listeners when no longer needed.
    
- Avoid global variables.
    
- Clear intervals and timeouts.
    
- Avoid closures capturing large objects.
    

---

### **27. What is an IIFE (Immediately Invoked Function Expression)?**

**Answer:**  
A function that runs as soon as it’s defined.

js

CopyEdit

`(function() {   console.log('Run once!'); })();`

Used to avoid polluting global scope.

---

### **28. What is the Temporal Dead Zone (TDZ)?**

**Answer:**  
The time between entering a block and declaring a `let`/`const` variable, where accessing the variable will throw a ReferenceError.

---

### **29. What are modules in JavaScript?**

**Answer:**  
ES Modules (`import`/`export`) allow JS code to be split into reusable pieces.

js

CopyEdit

`// math.js export function add(a, b) { return a + b; }  // main.js import { add } from './math.js';`

---

### **30. Explain immutability in JavaScript.**

**Answer:**  
Immutability means **data cannot be changed** once created.  
Use `Object.freeze()`, or create new objects instead of modifying old ones.

js

CopyEdit

`const newArr = [...oldArr, newItem];`

---
---
## 🟩 **SECTION 3: React.js & Frontend Frameworks (Q31–50)**

---

### **31. What is React and why is it used?**

**Answer:**  
React is a **JavaScript library for building user interfaces**, especially single-page applications.  
Key features:

- Component-based architecture
    
- Virtual DOM for faster updates
    
- JSX for writing HTML in JS
    
- Unidirectional data flow
    

---

### **32. What is the Virtual DOM in React?**

**Answer:**  
The Virtual DOM is a **lightweight in-memory representation** of the real DOM.  
When state changes, React:

1. Creates a new virtual DOM.
    
2. Diffs it with the previous one.
    
3. Efficiently updates the real DOM (reconciliation).
    

---

### **33. What are React Hooks? Name a few.**

**Answer:**  
Hooks are **functions that let you use state and other React features in functional components**.  
Common hooks:

- `useState()` – manage state
    
- `useEffect()` – side effects
    
- `useContext()` – context API
    
- `useRef()`, `useMemo()`, `useCallback()`
    

---

### **34. Difference between useEffect and useLayoutEffect?**

**Answer:**

- `useEffect()`: Runs **after** the DOM has been painted.
    
- `useLayoutEffect()`: Runs **before paint**, blocking rendering. Use carefully for layout measurements.
    

---

### **35. What is JSX?**

**Answer:**  
JSX stands for **JavaScript XML**.  
It lets you write HTML-like syntax inside JavaScript.

js

CopyEdit

`const element = <h1>Hello, React</h1>;`

JSX gets transpiled to `React.createElement(...)`.

---

### **36. Explain the component lifecycle in React.**

**Answer:**  
In function components with Hooks:

- `useEffect(() => {}, [])` = componentDidMount
    
- `useEffect(() => { return () => {} })` = componentWillUnmount
    
- `useEffect(() => {}, [dep])` = componentDidUpdate for `dep`
    

Class-based:

- `constructor`
    
- `render`
    
- `componentDidMount`
    
- `componentDidUpdate`
    
- `componentWillUnmount`
    

---

### **37. Controlled vs Uncontrolled components in React?**

**Answer:**

- **Controlled**: Form elements controlled via React state.
    

js

CopyEdit

`<input value={name} onChange={e => setName(e.target.value)} />`

- **Uncontrolled**: Use `ref` to access DOM value directly.
    

---

### **38. What is the Context API?**

**Answer:**  
Context API allows **global state sharing** without prop drilling.

js

CopyEdit

`const ThemeContext = React.createContext(); <ThemeContext.Provider value="dark">   <App /> </ThemeContext.Provider>`

Consume via `useContext(ThemeContext)`.

---

### **39. How do keys work in React?**

**Answer:**  
`key` prop helps React identify which items changed, added, or removed.  
They must be **unique and stable**.

js

CopyEdit

`{items.map(item => <li key={item.id}>{item.name}</li>)}`

---

### **40. What causes performance issues in React and how to optimize?**

**Answer:**  
Causes:

- Re-renders due to unnecessary state/prop changes
    
- Heavy computations
    

Optimizations:

- `React.memo` to memoize components
    
- `useMemo`, `useCallback`
    
- Virtualization (e.g., react-window)
    
- Splitting code with `React.lazy()`
    

---

### **41. Difference between props and state?**

**Answer:**

- **Props**: Passed from parent, read-only.
    
- **State**: Managed inside the component, can be updated.
    

---

### **42. What is prop drilling?**

**Answer:**  
When data is passed through multiple layers of components just to reach a deeply nested component.  
**Solution:** Context API or state management libraries (Redux/Zustand).

---

### **43. How do you handle side effects in React?**

**Answer:**  
Using the `useEffect()` hook.

js

CopyEdit

`useEffect(() => {   fetchData(); }, []);`

Also used for:

- DOM manipulation
    
- Event listeners
    
- Timers
    

---

### **44. What is Redux and how does it work?**

**Answer:**  
Redux is a **state management library** for JS apps.  
Flow:

- Actions → Reducers → Store → Components
    
- Store is a **single source of truth**
    
- Uses pure functions (reducers) to update state
    

---

### **45. What is the difference between `useReducer` and Redux?**

**Answer:**

- `useReducer`: Local state management inside a component.
    
- Redux: Global state management across the app.
    

---

### **46. What are Higher Order Components (HOC)?**

**Answer:**  
A **HOC is a function that takes a component and returns a new component**.

js

CopyEdit

`const withLogger = (Wrapped) => (props) => {   console.log('Render:', props);   return <Wrapped {...props} />; };`

Used for reuse, abstraction.

---

### **47. What is React Router?**

**Answer:**  
A library for **navigating between components** in SPAs.

- `<BrowserRouter>`, `<Route>`, `<Link>`, `useNavigate`, `useParams`
    

---

### **48. Difference between `useEffect` and `useMemo`?**

**Answer:**

- `useEffect`: Runs **side effects** after render.
    
- `useMemo`: **Memoizes a value** to avoid recomputation unless dependencies change.
    

---

### **49. What is SSR in React (Next.js)?**

**Answer:**  
Server-Side Rendering: HTML is generated on the server.  
Next.js supports:

- `getServerSideProps()` for SSR
    
- `getStaticProps()` for SSG
    
- Great for SEO and initial load speed
    

---

### **50. What is reconciliation in React?**

**Answer:**  
The process React uses to **diff the new Virtual DOM with the previous one** and update the real DOM with minimal changes.

---
---
## 🟥 **SECTION 4: Backend (Node.js + Express), REST APIs, Middleware (Q51–70)**

---

### **51. What is Node.js and why is it used?**

**Answer:**  
Node.js is a **JavaScript runtime built on Chrome’s V8 engine**. It lets you run JS on the server side.  
Used for:

- Building scalable network applications
    
- Real-time apps (chat, live dashboards)
    
- APIs (REST/GraphQL)
    

---

### **52. What is the difference between CommonJS and ES Modules?**

**Answer:**

- **CommonJS (CJS)**: `require()`, `module.exports` (default in Node.js)
    
- **ES Modules (ESM)**: `import`, `export` (modern JS standard)
    

Node supports both:

js

CopyEdit

`// CJS const fs = require('fs');  // ESM import fs from 'fs';`

---

### **53. What is the event-driven model in Node.js?**

**Answer:**  
Node.js uses an **event loop** to handle asynchronous operations (non-blocking I/O).  
It processes:

- Events (like HTTP requests)
    
- Timers
    
- I/O callbacks
    

This allows high concurrency with a single thread.

---

### **54. What is Express.js?**

**Answer:**  
Express is a **minimal and flexible Node.js web framework** for building RESTful APIs and web apps.  
Features:

- Routing
    
- Middleware support
    
- Error handling
    
- Request/response abstraction
    

---

### **55. How does routing work in Express?**

**Answer:**  
Routing is how an application responds to a request.

js

CopyEdit

``app.get('/user/:id', (req, res) => {   res.send(`User ${req.params.id}`); });``

---

### **56. What is middleware in Express?**

**Answer:**  
Middleware functions are functions that have access to the **request**, **response**, and `next()` function.

js

CopyEdit

`app.use((req, res, next) => {   console.log('Request URL:', req.url);   next(); });`

Types:

- Application-level
    
- Router-level
    
- Error-handling
    

---

### **57. How do you create RESTful APIs in Express?**

**Answer:**  
Using CRUD endpoints:

js

CopyEdit

`app.get('/items', ...); app.post('/items', ...); app.put('/items/:id', ...); app.delete('/items/:id', ...);`

Each route maps to an HTTP method and resource.

---

### **58. What is the difference between `res.send()`, `res.json()`, and `res.end()`?**

**Answer:**

- `res.send()`: Sends a response of any type (auto-detects).
    
- `res.json()`: Sends a JSON response (adds `Content-Type: application/json`)
    
- `res.end()`: Ends the response without data.
    

---

### **59. What is body-parser and why is it used?**

**Answer:**  
Body-parser is middleware to **parse incoming request bodies** (like JSON or URL-encoded).

js

CopyEdit

`app.use(express.json()); app.use(express.urlencoded({ extended: true }));`

---

### **60. How do you handle errors in Express?**

**Answer:**  
Use middleware with 4 params:

js

CopyEdit

`app.use((err, req, res, next) => {   console.error(err.stack);   res.status(500).send('Something broke!'); });`

---

### **61. What is CORS and how do you enable it in Express?**

**Answer:**  
CORS = Cross-Origin Resource Sharing  
Enable using middleware:

js

CopyEdit

`const cors = require('cors'); app.use(cors());`

Or configure it manually via headers.

---

### **62. How do you secure Express apps?**

**Answer:**

- Use `helmet` for security headers
    
- Sanitize user input
    
- Use rate limiting (`express-rate-limit`)
    
- Validate all inputs
    
- Use HTTPS and tokens
    

---

### **63. What are environment variables and how do you use them?**

**Answer:**  
Store secrets/config outside code (e.g., API keys, DB strings).  
Use `.env` file + `dotenv`:

js

CopyEdit

`require('dotenv').config(); console.log(process.env.DB_URL);`

---

### **64. How do you connect Node.js to MongoDB?**

**Answer:**  
Using `mongoose` or `mongodb` driver.

js

CopyEdit

`const mongoose = require('mongoose'); mongoose.connect(process.env.MONGO_URI);`

Then define schemas and models.

---

### **65. What are HTTP status codes you often use in REST APIs?**

**Answer:**

- 200 – OK
    
- 201 – Created
    
- 400 – Bad Request
    
- 401 – Unauthorized
    
- 403 – Forbidden
    
- 404 – Not Found
    
- 500 – Internal Server Error
    

---

### **66. What is JSON Web Token (JWT)?**

**Answer:**  
JWT is a token format used for **authentication**.  
Structure: `header.payload.signature`

js

CopyEdit

`const token = jwt.sign({ id: user._id }, process.env.JWT_SECRET);`

Sent in headers, verified on protected routes.

---

### **67. What is the difference between authentication and authorization?**

**Answer:**

- **Authentication**: Who are you? (login)
    
- **Authorization**: Are you allowed to do this? (roles/permissions)
    

---

### **68. What is a middleware chain in Express?**

**Answer:**  
A series of middleware functions called in sequence for a request.  
Each must call `next()` to continue.

js

CopyEdit

`app.use(authMiddleware); app.use(logMiddleware); app.get('/dashboard', handler);`

---

### **69. What is the purpose of `next()` in Express?**

**Answer:**  
It passes control to the **next middleware** or route handler.  
Without it, the request **hangs**.

---

### **70. How do you structure a scalable Express app?**

**Answer:**  
Use modular structure:

bash

CopyEdit

`/controllers /routes /models /middleware /config`

Example:

js

CopyEdit

`router.get('/users', userController.getAllUsers);`

---
---
## 🟨 **SECTION 5: MongoDB, Database Design, Mongoose, Aggregation (Q71–85)**

---

### **71. What is MongoDB?**

**Answer:**  
MongoDB is a **NoSQL, document-oriented database** that stores data in flexible, JSON-like **BSON** documents.  
Features:

- Schema-less
    
- High performance and scalability
    
- Document-based (not rows and columns)
    

---

### **72. Difference between SQL and NoSQL?**

|Feature|SQL (Relational)|NoSQL (MongoDB)|
|---|---|---|
|Data format|Tables & rows|Documents (JSON-like)|
|Schema|Fixed schema|Dynamic schema|
|Joins|Supported|Limited (via `$lookup`)|
|Scaling|Vertical (scale up)|Horizontal (scale out)|

---

### **73. What is a collection and a document in MongoDB?**

**Answer:**

- **Collection** = table (group of related documents)
    
- **Document** = individual JSON-like record
    

Example:

json

CopyEdit

`{   "_id": "123",   "name": "Rohan",   "age": 25 }`

---

### **74. What is Mongoose and why use it?**

**Answer:**  
Mongoose is an **ODM (Object Data Modeling)** library for MongoDB and Node.js.  
It provides:

- Schema definition
    
- Model methods
    
- Validations
    
- Middleware (pre/post hooks)
    

---

### **75. How do you define a Mongoose model?**

**Answer:**

js

CopyEdit

`const mongoose = require('mongoose');  const userSchema = new mongoose.Schema({   name: String,   email: String,   age: Number, });  const User = mongoose.model('User', userSchema);`

---

### **76. Common Mongoose methods for CRUD?**

**Answer:**

js

CopyEdit

`User.create(data);         // Create User.find();               // Read all User.findById(id);         // Read one User.findByIdAndUpdate();  // Update User.findByIdAndDelete();  // Delete`

---

### **77. How do you validate data in Mongoose?**

**Answer:**  
Using built-in validation rules in the schema:

js

CopyEdit

`age: {   type: Number,   required: true,   min: 0,   max: 120 }`

Or custom validators:

js

CopyEdit

`email: {   type: String,   validate: [validator.isEmail, 'Invalid email'] }`

---

### **78. What are MongoDB indexes? Why are they important?**

**Answer:**  
Indexes **improve query performance**.  
Without indexes, MongoDB performs a full collection scan.

Create an index:

js

CopyEdit

`db.users.createIndex({ email: 1 })`

---

### **79. What is the Aggregation Framework in MongoDB?**

**Answer:**  
Used for advanced data processing (grouping, filtering, transforming).

Example:

js

CopyEdit

`db.orders.aggregate([   { $match: { status: "delivered" } },   { $group: { _id: "$userId", total: { $sum: "$amount" } } } ]);`

---

### **80. What are the stages in an aggregation pipeline?**

**Answer:**  
Common stages:

- `$match` – filter
    
- `$group` – aggregate
    
- `$project` – reshape
    
- `$sort`, `$limit`, `$skip`
    
- `$lookup` – join
    
- `$unwind` – flatten arrays
    

---

### **81. What is the use of `$lookup` in MongoDB?**

**Answer:**  
It performs a **left outer join** between collections.

Example:

js

CopyEdit

`{   $lookup: {     from: "orders",     localField: "_id",     foreignField: "userId",     as: "orders"   } }`

---

### **82. Difference between `find()` and `aggregate()` in MongoDB?**

|Feature|`find()`|`aggregate()`|
|---|---|---|
|Use case|Simple queries|Complex data transformation|
|Returns|Documents directly|Pipeline results|
|Features|Basic filters|Grouping, lookup, computed fields|

---

### **83. How do you implement pagination in MongoDB?**

**Answer:**  
Use `.skip()` and `.limit()`:

js

CopyEdit

`db.users.find().skip(20).limit(10);`

In Mongoose:

js

CopyEdit

`User.find().skip((page-1)*limit).limit(limit);`

---

### **84. How do you handle relations in MongoDB (1:1, 1:N)?**

**Answer:**

- **1:1**: Embed or reference
    
- **1:N**: Either embed an array or use references
    

Example (referencing):

js

CopyEdit

`userSchema = { posts: [{ type: mongoose.Schema.Types.ObjectId, ref: "Post" }] }`

Populate:

js

CopyEdit

`User.find().populate("posts");`

---

### **85. How to handle schema-less flexibility in MongoDB projects?**

**Answer:**

- Use **Mongoose validation** and schemas
    
- Use schema migration tools or add versioning (`__v`)
    
- Define clear model contracts even if MongoDB is flexible

---
---
## 🟦 **SECTION 6: Full Stack Integration, Deployment, Git, CI/CD, System Design (Q86–100)**

---

### **86. How does the MERN stack work together?**

**Answer:**

- **MongoDB**: NoSQL database to store data.
    
- **Express.js**: Backend framework on top of Node.js to handle routes & API logic.
    
- **React.js**: Frontend library to build UI.
    
- **Node.js**: Server runtime for running JavaScript.
    

**Flow**:  
React → API Calls → Express (Node.js) → MongoDB → Response → React UI

---

### **87. How do you connect frontend to backend in MERN?**

**Answer:**

- Use `fetch()` or `axios` from React to call backend APIs.
    
- Example:
    

js

CopyEdit

`axios.post("/api/login", { email, password });`

Ensure CORS is handled properly on the backend.

---

### **88. How do you structure a full stack project?**

**Answer:**

bash

CopyEdit

`/client   → React frontend /server   → Express backend .env      → Shared configs`

Backend handles routes, controllers, DB logic.  
Frontend handles UI and state using context/hooks.

---

### **89. How do you deploy a MERN app?**

**Answer:**

- **Frontend**: Vercel, Netlify, or static site on Nginx/S3.
    
- **Backend**: Render, Railway, or VPS (like EC2).
    
- **DB**: MongoDB Atlas (cloud DB).
    

Can also deploy all in one using services like Render or DigitalOcean.

---

### **90. How do you manage environment variables in full stack apps?**

**Answer:**

- Use `.env` files in both frontend and backend.
    
- Frontend: Variables must start with `REACT_APP_` or `VITE_`.
    

**Security tip**: Never expose secrets in frontend code.

---

### **91. What is Git and why is it used?**

**Answer:**  
Git is a **version control system** that helps track changes in code over time.  
Benefits:

- Collaboration via branches
    
- Revert history
    
- Merge features safely
    

---

### **92. Common Git commands you use?**

**Answer:**

bash

CopyEdit

`git init             # initialize repo git clone <url>      # clone remote git status           # check status git add .            # stage changes git commit -m ""     # commit git push origin main # push to branch`

---

### **93. What are branches in Git and why use them?**

**Answer:**  
Branches are used to work on features independently without affecting the main codebase.

Example:

bash

CopyEdit

`git checkout -b feature/login`

---

### **94. What is pull request (PR) and how does it work?**

**Answer:**  
PR is a request to merge your feature branch into the main branch on platforms like GitHub.  
Team members review code before merging (code review, CI checks).

---

### **95. What is CI/CD and why is it important?**

**Answer:**  
CI/CD = Continuous Integration & Continuous Deployment

- CI: Automatically runs tests on every push (e.g., GitHub Actions)
    
- CD: Automatically deploys code when merged
    

Tools: GitHub Actions, Jenkins, CircleCI, Vercel

---

### **96. What is Webpack / Vite and why are they used?**

**Answer:**  
They are **build tools** that bundle frontend assets (JS, CSS, etc.).

- **Webpack**: Older but highly configurable.
    
- **Vite**: Modern, fast dev server with hot reloading and ES Module support.
    

---

### **97. What are service workers and why are they used?**

**Answer:**  
Service workers are scripts that run in the background and:

- Enable offline support (via caching)
    
- Push notifications
    
- Background sync
    

Used in Progressive Web Apps (PWAs).

---

### **98. What is lazy loading and how do you implement it in React?**

**Answer:**  
Lazy loading delays loading a component until it’s needed.

js

CopyEdit

`const LazyComp = React.lazy(() => import('./LazyComp'));`

Used with `<Suspense fallback={<Loader />}>`.

---

### **99. Explain a basic system design of a URL shortener.**

**Answer:**

- **Frontend**: Input URL, display short URL
    
- **Backend**:
    
    - Store long URL with short code in MongoDB
        
    - GET `/short/:code` → redirect
        
    - POST `/shorten` → generate & save code
        

**Optional Features**:

- Expiry
    
- Analytics
    
- Rate limiting
    

---

### **100. How would you design a scalable full stack application?**

**Answer:**  
**Frontend:**

- React + lazy loading + state management
    

**Backend:**

- Node.js + Express with layered architecture
    
    - `routes`, `controllers`, `services`, `models`
        

**Database:**

- MongoDB with indexing, validation, schema design
    

**Deployment:**

- Vercel (frontend), Render (backend), MongoDB Atlas
    
- Environment-based configs
    
- CI/CD pipeline via GitHub Actions
    

**Best Practices:**

- Error handling
    
- Input validation
    
- Security (JWT, Helmet, CORS, rate-limiting)
    
- Logging & monitoring
---
---

