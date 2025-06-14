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
