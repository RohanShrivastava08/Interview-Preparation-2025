## 🔹 Section 1: React Basics (Q1–Q15)

### 1. What is React?

> React is a **JavaScript library** for building **user interfaces**, especially **single-page applications (SPAs)**. It uses a **component-based** architecture and a **virtual DOM** for efficient UI rendering.

### 2. What are components in React?

> Components are the **building blocks** of a React application. They can be **functional or class-based** and return React elements (UI).

### 3. What is JSX?

> JSX stands for **JavaScript XML**. It allows writing HTML-like syntax inside JavaScript, which gets compiled to `React.createElement()` calls.

### 4. What is the difference between functional and class components?

> Functional components are **stateless** and written as functions. Class components are **stateful** and extend from `React.Component`.

### 5. What is the Virtual DOM?

> The virtual DOM is a **lightweight copy of the real DOM**. React uses it to optimize rendering by updating only changed elements.

## 🔹 Section 2: Props and State (Q16–Q30)

### 16. What are props in React?

> Props (short for **properties**) are used to **pass data** from a parent to child components. Props are **read-only**.

### 17. What is state in React?

> State is **data that changes over time** and determines a component’s behavior and rendering. Managed using `useState` in functional components.

### 18. Can you modify props in a child component?

> ❌ No, props are immutable. You should pass a callback function to the child if it needs to communicate back.

### 19. How do you update the state in React?

> By using the `setState` method in class components or the `setStateFunction` returned by `useState` in functional components.

### 20. What happens when you update the state in React?

> React **schedules a re-render** of the component and **updates the virtual DOM** accordingly.

## 🔹 Section 3: Hooks (Q31–Q50)

### 31. What are hooks in React?

> Hooks are **functions** that let you use **state and lifecycle** features in functional components.

### 32. Name some commonly used hooks.

> `useState`, `useEffect`, `useRef`, `useContext`, `useMemo`, `useCallback`, `useReducer`.

### 33. What is `useState`?

> A hook that lets you add **state** to functional components.

### 34. What is `useEffect`?

> A hook for handling **side effects** like data fetching, subscriptions, or manually changing the DOM. Runs after render.

### 35. Difference between `useEffect` and `useLayoutEffect`?

> `useEffect` runs **after the render is committed** to the screen, while `useLayoutEffect` runs **before painting**. Use the latter for measuring DOM elements.

## 🔹 Section 4: Lifecycle & Events (Q51–Q65)

### 51. What are lifecycle methods in class components?

> Common ones:

- `componentDidMount()`
    
- `componentDidUpdate()`
    
- `componentWillUnmount()`
    

### 52. What is the equivalent of `componentDidMount` in hooks?

> `useEffect(() => { ... }, [])`

### 53. How do you handle events in React?

> By passing functions like `onClick={() => ...}` or `onChange={handleChange}` to JSX elements.

### 54. What are synthetic events?

> React uses **synthetic events**, a wrapper around native events, for cross-browser compatibility.

## 🔹 Section 5: Conditional Rendering (Q66–Q70)

### 66. How do you render conditionally in React?

> Using `if/else`, ternary `condition ? A : B`, logical AND `condition && <Component />`.

### 67. Can you return null from a component?

> ✅ Yes. Returning `null` renders nothing.

---

## 🔹 Section 6: Lists and Keys (Q71–Q75)

### 71. How do you render a list in React?

> Using `Array.map()` to loop over an array and return a component for each item.

### 72. Why is `key` important in React lists?

> Keys help React identify which items have changed, are added, or removed.

---

## 🔹 Section 7: Forms (Q76–Q80)

### 76. How do you handle forms in React?

> Use controlled components by binding form inputs to state.

### 77. What are controlled vs uncontrolled components?

> **Controlled**: Form inputs controlled by React state.  
> **Uncontrolled**: Accessed via refs (`useRef`), not state.

## 🔹 Section 8: Context and State Management (Q81–Q90)

### 81. What is Context API in React?

> A way to pass data deeply through the component tree **without props drilling**.

### 82. When would you use Context?

> For global state like theme, user authentication, language preferences.

### 83. What is Redux?

> Redux is a **state management library**. It uses a single global state and dispatchable actions to update the state.

---

## 🔹 Section 9: Performance Optimization (Q91–Q100)

### 91. What is memoization in React?

> Techniques like `React.memo`, `useMemo`, and `useCallback` prevent **unnecessary re-renders**.

### 92. When to use `React.memo`?

> When you want to **memoize** a component so it doesn’t re-render unless props change.

### 93. What is code splitting in React?

> Using **dynamic `import()`** or tools like `React.lazy` to **load components on demand**.

---

## 🔹 Section 10: Routing & Next.js (Q101–Q110)

### 101. What is React Router?

> A popular library for handling **routing in React SPAs**, allowing navigation between pages/components.

### 102. What is the difference between `<Link>` and `<a>` in React Router?

> `<Link>` prevents full-page reloads and enables **client-side navigation**. `<a>` triggers a full page load.

### 103. How do you define routes in React Router v6?


`<Routes>     <Route path="/home" element={<Home />} />   </Routes>`

## 🔹 Section 11: Error Handling & Testing (Q111–Q115)

### 111. What are Error Boundaries in React?

> Special class components with `componentDidCatch()` used to **catch JavaScript errors in child components**.

### 112. How do you test React components?

> Use **Jest** with **React Testing Library** to test rendering, user interactions, and outputs.

---

## 🔹 Section 12: Miscellaneous (Q116–Q125)

### 116. What is the difference between `useRef` and `createRef`?

> `useRef` is for functional components, `createRef` is for class components. Both reference DOM elements or values without triggering re-renders.

### 117. What is hydration in React?

> The process of attaching event listeners to **server-rendered HTML** when using frameworks like Next.js.

### 118. How do portals work in React?

> With `ReactDOM.createPortal`, you can render components **outside the parent DOM hierarchy**, useful for modals, tooltips.