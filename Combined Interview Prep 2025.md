## ✅ **HTML & CSS (Frontend Core)**

1. **What is the difference between HTML and HTML5?**  
    HTML5 includes new elements (e.g., `<section>`, `<article>`, `<video>`), supports local storage, and provides better semantics and multimedia support.
    
2. **What are semantic HTML elements?**  
    Elements like `<article>`, `<section>`, and `<nav>` that clearly describe their meaning in human- and machine-readable ways.
    
3. **Difference between id and class in HTML?**  
    `id` is unique and used once; `class` can be reused across multiple elements.
    
4. **What is the Box Model in CSS?**  
    It includes `content`, `padding`, `border`, and `margin` — used to calculate element dimensions.
    
5. **How does CSS specificity work?**  
    Inline > ID selectors > Class selectors > Element selectors. More specific selectors override others.
    
6. **What are pseudo-classes in CSS?**  
    Keywords like `:hover`, `:nth-child()`, and `:focus` that apply styles based on element state.
    
7. **How do you center a div?**  
    Horizontally with `margin: auto;`, or flexbox: `display: flex; justify-content: center; align-items: center;`
    
8. **What is the difference between relative, absolute, and fixed positioning?**
    
    - `relative`: relative to normal position
        
    - `absolute`: relative to nearest positioned ancestor
        
    - `fixed`: relative to the viewport
        
9. **What are media queries in CSS?**  
    CSS rules that apply based on device screen size, e.g., `@media (max-width: 768px) { ... }`
    
10. **What is the difference between `em`, `rem`, `px` in CSS?**
    

- `px`: fixed size
    
- `em`: relative to parent
    
- `rem`: relative to root (`html`) element

---
---

## ✅ **JavaScript (Frontend + Full Stack Core)**

11. **What is hoisting in JavaScript?**  
    Variables and functions are moved to the top of their scope before code execution.
    
12. **Difference between `var`, `let`, and `const`?**
    

- `var`: function-scoped
    
- `let`: block-scoped
    
- `const`: block-scoped, read-only
    

13. **What is a closure?**  
    A function that retains access to its outer scope even after the outer function has finished executing.
    
14. **What is the difference between `==` and `===`?**  
    `==` checks value with type coercion; `===` checks value and type strictly.
    
15. **What is event delegation?**  
    A pattern where a parent element handles events from its child elements via event bubbling.
    
16. **What are promises in JavaScript?**  
    Objects representing the eventual completion or failure of an asynchronous operation.
    
17. **Explain `async/await`.**  
    Syntactic sugar over Promises to write async code in a synchronous style.
    
18. **What is a callback function?**  
    A function passed into another function to be executed later.
    
19. **What is the DOM?**  
    Document Object Model — a tree-like structure representing HTML documents.
    
20. **What is the difference between synchronous and asynchronous JavaScript?**  
    Synchronous blocks code execution; asynchronous runs in the background and doesn’t block the thread.

---
---

## ✅ **React.js (Frontend + MERN + Full Stack)**

21. **What is React?**  
    A JavaScript library for building UI components, using a virtual DOM for efficient rendering.
    
22. **What are components in React?**  
    Reusable UI building blocks. Can be functional or class-based.
    
23. **What are hooks in React?**  
    Functions like `useState`, `useEffect` that allow functional components to manage state and lifecycle.
    
24. **Difference between functional and class components?**  
    Functional: simpler, use hooks. Class: use lifecycle methods and `this`.
    
25. **What is JSX?**  
    A syntax extension that allows writing HTML-like code in JavaScript.
    
26. **What is state in React?**  
    Data managed inside components that influences rendering.
    
27. **What is props in React?**  
    Data passed from parent to child components, read-only.
    
28. **What is useEffect used for?**  
    To perform side effects like data fetching, subscriptions, or DOM manipulation.
    
29. **What is virtual DOM?**  
    An in-memory representation of the real DOM that improves performance by reducing direct manipulations.
    
30. **How does React handle re-rendering?**  
    Via reconciliation and diffing the virtual DOM tree.

---
---

## ✅ **Node.js & Express.js (Backend + MERN + Full Stack)**

31. **What is Node.js?**  
    A runtime environment that allows executing JavaScript on the server side.
    
32. **What is Express.js?**  
    A minimal and flexible Node.js web application framework.
    
33. **How does routing work in Express?**  
    With methods like `app.get()`, `app.post()`, defining handlers for different paths.
    
34. **What is middleware in Express?**  
    Functions that have access to the request and response objects and the next middleware.
    
35. **What is the role of `package.json`?**  
    Contains metadata and dependencies of the Node.js project.
    
36. **What is `nodemon` used for?**  
    A tool that automatically restarts the server when file changes are detected.
    
37. **What is RESTful API?**  
    An architectural style that uses HTTP methods for CRUD operations on resources.
    
38. **What is CORS?**  
    Cross-Origin Resource Sharing — browser security feature that restricts resource sharing between origins.
    
39. **What is the difference between PUT and PATCH?**
    

- `PUT`: replaces the whole resource
    
- `PATCH`: updates only the specified fields
    

40. **How do you handle errors in Express?**  
    Using middleware with 4 arguments: `function (err, req, res, next) {}`

---
---

## ✅ **MongoDB (Backend + MERN + Full Stack)**

41. **What is MongoDB?**  
    A NoSQL, document-oriented database that stores data in BSON format.
    
42. **Difference between SQL and NoSQL?**  
    SQL: structured, relational. NoSQL: unstructured or semi-structured, document/key-value-based.
    
43. **What is a collection in MongoDB?**  
    Equivalent to a table in SQL; it stores multiple documents.
    
44. **What is a document in MongoDB?**  
    A record in a MongoDB collection, stored in JSON/BSON format.
    
45. **How to connect MongoDB with Node.js?**  
    Using `mongoose.connect()` or native MongoDB driver.
    
46. **What is Mongoose?**  
    An ODM (Object Data Modeling) library for MongoDB and Node.js.
    
47. **What is schema in Mongoose?**  
    Defines the structure of a document like field types, validators, etc.
    
48. **How to define relationships in MongoDB?**  
    Via references (ObjectId) or embedded documents.
    
49. **How do you handle indexing in MongoDB?**  
    Use `.createIndex()` or define indexes in Mongoose schema for faster querying.
    
50. **How do you perform CRUD operations in MongoDB?**  
    Using `Model.create()`, `Model.find()`, `Model.updateOne()`, `Model.deleteOne()`

---
---

## ✅ **Advanced JavaScript & ES6+**

51. **What is destructuring in JavaScript?**  
    A syntax to extract values from arrays or objects:
    `const [a, b] = [1, 2];   const {name} = person;`

52. **What is the spread operator?**  
    Used to expand iterable elements:
    `const arr = [...arr1, ...arr2];`

53. **What is the rest parameter?**  
    Collects all remaining elements into an array:
    `function sum(...nums) {}`

54. **What is a higher-order function?**  
    A function that takes other functions as arguments or returns a function.
    
55. **What is the difference between `map()`, `forEach()`, and `filter()`?**
    
- `map`: transforms array
    
- `forEach`: performs side effects
    
- `filter`: returns elements meeting condition
    

56. **What is the difference between shallow copy and deep copy?**
    
- Shallow: copies reference
    
- Deep: copies actual values recursively
    

57. **How does JavaScript handle memory management?**  
    Uses a garbage collector to free memory from unreachable objects.
    
58. **What is a debounce function?**  
    Limits how often a function is executed — runs after delay of inactivity.
    
59. **What is throttling in JavaScript?**  
    Ensures a function runs only once per specified time interval.
    
60. **What is a generator function?**  
    Special function that can pause execution using `yield`.

---
---

## ✅ **Web APIs & Browser**

61. **What is localStorage vs sessionStorage?**
    

- `localStorage`: persists even after tab/browser close
    
- `sessionStorage`: cleared on tab/browser close
    

62. **What is the Fetch API?**  
    A modern way to make network requests:
    `fetch(url).then(res => res.json());`

63. **What is the difference between cookies and localStorage?**  
    Cookies: sent with every HTTP request; localStorage is not.
    
64. **What are service workers?**  
    Background scripts enabling offline support, caching, and push notifications.
    
65. **What is a WebSocket?**  
    A full-duplex communication channel over a single TCP connection.
    
66. **What is a single-page application (SPA)?**  
    A web app that loads once and dynamically updates content without full page reloads.
    
67. **How to optimize performance in front-end apps?**  
    Lazy loading, code splitting, minification, caching, avoiding re-renders, using CDN.
    
68. **What is lazy loading?**  
    Deferring loading of non-critical resources until needed.
    
69. **What is prefetching vs preloading?**

- `preload`: loads resources you’ll definitely need
    
- `prefetch`: hints browser to load resources for future navigation
    

70. **What is SSR and CSR?**

- SSR (Server-Side Rendering): renders on server
    
- CSR (Client-Side Rendering): renders in browser

---
---

