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