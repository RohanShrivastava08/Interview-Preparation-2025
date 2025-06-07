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

