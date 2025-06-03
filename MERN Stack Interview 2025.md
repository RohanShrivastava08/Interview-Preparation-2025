## 🟢 **FRESHER LEVEL (0–1 Year) — 30 Questions with Answers**

---

### 🔹 General & JavaScript Basics

**1. What is the MERN Stack?**  
The MERN stack is a set of JavaScript-based technologies used to build full-stack web applications. It includes:

- **M**ongoDB (Database)
    
- **E**xpress.js (Backend framework)
    
- **R**eact.js (Frontend library)
    
- **N**ode.js (JavaScript runtime environment)
    

---

**2. What are the advantages of using JavaScript across the stack?**

- Code reusability (same language for frontend and backend)
    
- Faster development
    
- Large ecosystem of tools and libraries
    
- JSON used throughout (MongoDB, Node.js, React)
    

---

**3. Explain ES6 features like `let`, `const`, arrow functions, and template literals.**

- `let`: block-scoped variable
    
- `const`: block-scoped, immutable variable
    
- Arrow functions: `() => {}` syntax with lexical `this`
    
- Template literals: Use backticks `` `Hello ${name}` `` for string interpolation
    

---

**4. What is the difference between `==` and `===` in JavaScript?**

- `==`: checks for value equality (performs type coercion)
    
- `===`: checks for both value and type (strict equality)
    

---

**5. Explain hoisting in JavaScript.**  
Variables and function declarations are moved to the top of their scope during compilation. Only declarations are hoisted, not initializations.

---

**6. What are Promises and async/await?**

- **Promise**: An object representing eventual completion/failure of an asynchronous task.
    
- **async/await**: Syntactic sugar over Promises that allows writing async code in a synchronous style.
    

---

### ⚛️ React.js Basics

**7. What is JSX?**  
JSX stands for JavaScript XML. It allows us to write HTML in React.  
Example: `<h1>Hello, {name}</h1>`

---

**8. What are components in React?**  
Components are reusable, independent pieces of UI. React apps are made up of components—either functional or class-based.

---

**9. Functional vs Class components?**

- Functional: Simple JavaScript functions using hooks
    
- Class: Use ES6 classes with `render()` and lifecycle methods
    

---

**10. What is `useState` in React?**  
A React Hook that allows you to add state to a functional component.

js

CopyEdit

`const [count, setCount] = useState(0);`

---

**11. What is `useEffect` used for?**  
Used to perform side effects (e.g., API calls, subscriptions) in functional components.

js

CopyEdit

`useEffect(() => { fetchData(); }, []);`

---

**12. How do you pass data from parent to child in React?**  
Using props.

js

CopyEdit

`<ChildComponent name="Rohan" />`

---

**13. What is the virtual DOM?**  
A lightweight in-memory representation of the real DOM. React compares changes in the virtual DOM and updates only the necessary parts.

---

**14. What is the role of keys in lists?**  
Keys help React identify which items have changed, added, or removed in a list. It improves performance during re-renders.

---

### 🟢 Node.js & Express Basics

**15. What is Node.js?**  
Node.js is a JavaScript runtime built on Chrome’s V8 engine. It allows running JS on the server.

---

**16. Difference between Node.js and browser JavaScript?**  
Node.js can access system resources (files, network), while browser JS is sandboxed and can’t directly access the file system.

---

**17. What is Express.js?**  
A minimal and flexible Node.js web application framework that provides tools for handling HTTP requests, middleware, and routing.

---

**18. How do you create a simple Express server?**

js

CopyEdit

`const express = require('express'); const app = express(); app.get('/', (req, res) => res.send('Hello')); app.listen(3000);`

---

**19. What is middleware in Express?**  
Functions that have access to the request, response, and `next()` middleware. Used for logging, auth, error handling.

---

**20. What is `req` and `res`?**

- `req`: represents the HTTP request object
    
- `res`: represents the HTTP response object
    

---

### 🌿 MongoDB Basics

**21. What is MongoDB?**  
A NoSQL document database that stores data in flexible, JSON-like documents (BSON).

---

**22. What is a document in MongoDB?**  
A document is a record in MongoDB, stored in a collection. It's a JSON object:

json

CopyEdit

`{ "name": "Rohan", "age": 25 }`

---

**23. How do you insert a document into a collection?**

js

CopyEdit

`db.users.insertOne({ name: "Rohan", age: 25 });`

---

**24. Difference between `find()` and `findOne()`?**

- `find()`: returns a cursor to all matching documents
    
- `findOne()`: returns the first matching document
    

---

**25. What is a collection?**  
A group of MongoDB documents, similar to a table in relational databases.

---

**26. What is BSON?**  
Binary JSON. MongoDB stores documents in BSON format for efficient storage and traversal.

---

### 🔁 Full Stack Basics

**27. How does data flow in a MERN app?**  
React (frontend) sends HTTP requests to Express (backend), which interacts with MongoDB and returns responses to React.

---

**28. What is CRUD?**  
CRUD stands for Create, Read, Update, Delete—basic operations on a database.

---

**29. How does frontend communicate with backend?**  
Through HTTP requests (usually via `fetch()` or `axios`) to API endpoints.

---

**30. What tools do you use for MERN development?**

- VS Code
    
- Postman
    
- MongoDB Compass
    
- Git/GitHub
    
- npm/yarn
    
- Node.js & React Developer Tools

---
---
---

## 🟡 **INTERMEDIATE LEVEL (1–3 Years) — 40 Questions with Answers**

---

### ⚛️ React.js Intermediate

**31. What are React Hooks?**  
Hooks are functions that let you use state and lifecycle features in functional components. Common hooks: `useState`, `useEffect`, `useContext`, `useMemo`, etc.

---

**32. Explain `useContext` and where you’d use it.**  
`useContext` allows you to access global values in any component without prop drilling.  
Example: managing theme, user login state globally.

---

**33. What is prop drilling and how to avoid it?**  
Prop drilling is passing props through multiple levels unnecessarily.  
Avoid with:

- `useContext`
    
- State management libraries like Redux or Zustand
    

---

**34. What is lifting state up?**  
Moving shared state to a common ancestor component so it can be passed down to children.

---

**35. Difference between controlled and uncontrolled components?**

- **Controlled**: Form elements controlled by React state
    
- **Uncontrolled**: Form elements manage their own state via refs
    

---

**36. What are higher-order components (HOC)?**  
Functions that take a component and return a new component with additional features.  
Example: `withAuth(Component)`

---

**37. How does React handle forms?**  
Using controlled components. Form inputs are bound to component state and updated via `onChange`.

---

**38. What is conditional rendering?**  
Rendering different elements/components based on conditions using JS expressions (`if`, `&&`, `? :`)

---

**39. How to optimize performance in React apps?**

- Use `React.memo`, `useMemo`, and `useCallback`
    
- Code splitting with React.lazy
    
- Avoid unnecessary re-renders
    
- Use virtualization for long lists (e.g., `react-window`)
    

---

**40. What is `useMemo` and `useCallback`?**

- `useMemo`: Memoizes expensive computed values
    
- `useCallback`: Memoizes functions to avoid re-creating them on re-renders
    

---

### 🟢 Node.js & Express Intermediate

**41. Explain the Event Loop in Node.js.**  
It handles non-blocking async operations by offloading them and executing callbacks when ready—enabling single-threaded concurrency.

---

**42. What are streams in Node.js?**  
Streams are objects for reading/writing data in chunks (streaming). Types: Readable, Writable, Duplex, Transform.

---

**43. How do you handle async operations in Node.js?**  
Using callbacks, Promises, and `async/await` syntax.

---

**44. How do you handle routing in Express?**  
Using route methods:

js

CopyEdit

`app.get('/users', handler); app.post('/login', handler);`

---

**45. How do you implement middleware in Express?**  
Middleware functions sit between the request and response.

js

CopyEdit

`app.use((req, res, next) => {   console.log(req.url); next(); });`

---

**46. How do you send JSON responses in Express?**

js

CopyEdit

`res.json({ message: "Success" });`

---

**47. How do you structure a Node/Express project?**

- `/routes` – API route definitions
    
- `/controllers` – logic for requests
    
- `/models` – MongoDB schemas
    
- `/middleware` – auth, error handlers
    
- `/config` – DB, env setup
    

---

**48. How to secure routes using middleware?**  
Create an auth middleware that checks JWT and applies it to protected routes:

js

CopyEdit

`app.get('/profile', verifyToken, handler);`

---

**49. What is CORS and how do you resolve it?**  
CORS (Cross-Origin Resource Sharing) blocks requests from different origins.  
Fix: Use `cors` middleware in Express:

js

CopyEdit

`app.use(require('cors')());`

---

**50. What is an environment variable and how to use `.env` in Node?**  
Environment variables store sensitive/config info.  
Use `dotenv`:

js

CopyEdit

`require('dotenv').config(); const db = process.env.MONGO_URI;`

---

### 🌿 MongoDB Intermediate

**51. What is an index in MongoDB?**  
Indexes improve query performance by allowing faster lookups.  
Example:

js

CopyEdit

`db.users.createIndex({ email: 1 });`

---

**52. What are the advantages of using indexes?**

- Faster queries
    
- Efficient sorting and filtering
    
- Optimized read performance
    

---

**53. How to implement relationships in MongoDB?**

- Embedding: Store related data in a single document
    
- Referencing: Store ObjectId of related document and use `$lookup` to join
    

---

**54. What is the aggregation pipeline?**  
A powerful framework for data transformation using stages like `$match`, `$group`, `$project`, `$sort`.

---

**55. What is `$lookup` in MongoDB?**  
Performs a left outer join on another collection to combine documents.

js

CopyEdit

`{ $lookup: { from: 'orders', localField: '_id', foreignField: 'userId', as: 'orders' } }`

---

**56. How to filter and project data in aggregation?**  
Use `$match` to filter and `$project` to shape the output:

js

CopyEdit

`{ $project: { name: 1, age: 1 } }`

---

**57. How to paginate results in MongoDB?**  
Use `.skip()` and `.limit()`:

js

CopyEdit

`db.users.find().skip(10).limit(10)`

---

**58. What data types does MongoDB support?**  
String, Number, Boolean, Date, ObjectId, Array, Embedded Documents, Null, Binary Data, etc.

---

### 🔁 MERN Integration

**59. How do you connect React frontend to Express backend?**  
Make HTTP requests from React using `axios` or `fetch()` to Express API routes (usually via a proxy).

---

**60. How do you make API calls in React?**

js

CopyEdit

`useEffect(() => {   fetch('/api/users').then(res => res.json()).then(data => setUsers(data)); }, []);`

---

**61. How to implement authentication in MERN?**

- Backend: Validate user, generate JWT
    
- Frontend: Store token, use it for protected requests
    
- Use middleware to protect routes
    

---

**62. How do you store JWT securely on frontend?**  
Best practice: Use **HttpOnly cookies** (more secure). If localStorage is used, be cautious of XSS vulnerabilities.

---

**63. How to handle protected routes in React?**  
Use a higher-order component or conditional rendering to restrict access:

js

CopyEdit

`{isAuthenticated ? <Dashboard /> : <Navigate to="/login" />}`

---

**64. How to upload images in MERN stack?**

- Frontend: Use `FormData` and `fetch/axios`
    
- Backend: Use `multer` middleware
    
- Store in DB, cloud (e.g., Cloudinary), or filesystem
    

---

**65. How to manage CORS in local development?**  
Use `cors` in backend Express app:

js

CopyEdit

`const cors = require('cors'); app.use(cors({ origin: 'http://localhost:3000' }));`

---

### 🧪 Testing & Tools

**66. What is Postman used for?**  
API testing tool to send HTTP requests, view responses, test endpoints during backend development.

---

**67. How do you debug a Node.js application?**

- Use `console.log()`
    
- Use `node --inspect` and Chrome DevTools
    
- Use VS Code debugger
    

---

**68. What is `nodemon`?**  
A tool that automatically restarts the Node server when file changes are detected.

---

**69. What is `axios`?**  
A promise-based HTTP client for the browser and Node.js, used to make API calls.

---

**70. What is the role of Git and GitHub in projects?**

- **Git**: Version control to manage code changes
    
- **GitHub**: Cloud platform for hosting repositories and collaboration

---
---

