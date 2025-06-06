## 🧱 HTML & Semantic Markup

1. **What is HTML?**
    
    > HTML (HyperText Markup Language) is the standard language for creating and structuring web pages and applications.
    
2. **What are semantic HTML elements?**
    
    > Semantic elements clearly describe their meaning to both the browser and the developer. Examples include `<article>`, `<section>`, `<nav>`, and `<footer>`.
    
3. **Difference between `<div>` and `<section>`?**
    
    > `<div>` is a generic container with no semantic meaning, while `<section>` represents a standalone section of content with a specific theme.
    
4. **What is the purpose of the `<!DOCTYPE html>` declaration?**
    
    > It informs the browser about the HTML version used, ensuring proper rendering of the page.
    
5. **How do you create a hyperlink in HTML?**
    
    > Using the `<a>` tag with the `href` attribute: `<a href="https://example.com">Link</a>`.
    
6. **What are meta tags in HTML?**
    
    > Meta tags provide metadata about the HTML document, such as character set, author, and viewport settings.
    
7. **What is the difference between inline and block elements?**
    
    > Inline elements do not start on a new line and only occupy as much width as necessary, while block elements start on a new line and take up the full width available.
    
8. **What is the role of the `alt` attribute in images?**
    
    > It provides alternative text for images, enhancing accessibility and SEO.
    
9. **How do you create a table in HTML?**
    
    > Using `<table>`, `<tr>` for rows, `<th>` for headers, and `<td>` for data cells.
    
10. **What is the difference between `<ul>` and `<ol>`?**
    
    > `<ul>` creates an unordered (bulleted) list, while `<ol>` creates an ordered (numbered) list.
    

---

## 🎨 CSS & Styling

11. **What is CSS?**
    
    > CSS (Cascading Style Sheets) is used to style and layout web pages, including colors, fonts, and spacing.
    
12. **Difference between `id` and `class` selectors in CSS?**
    
    > `id` is unique and used for a single element, while `class` can be applied to multiple elements.
    
13. **What are pseudo-classes in CSS?**
    
    > Pseudo-classes define the special state of an element, such as `:hover`, `:focus`, and `:nth-child()`.
    
14. **What is the CSS box model?**
    
    > It describes the rectangular boxes generated for elements, consisting of margins, borders, padding, and the actual content.
    
15. **How do you center a div horizontally and vertically?**
    
    > Using Flexbox:
    
    css
    
    CopyEdit
    
    `display: flex; justify-content: center; align-items: center;`
    
16. **What is the difference between `relative`, `absolute`, and `fixed` positioning?**
    
    > - `relative`: positions the element relative to its normal position.
    >     
    
    - `absolute`: positions the element relative to its nearest positioned ancestor.
        
    - `fixed`: positions the element relative to the viewport.
        
17. **What are media queries in CSS?**
    
    > Media queries allow the application of different styles based on device characteristics like screen width.
    
18. **What is specificity in CSS?**
    
    > Specificity determines which CSS rule is applied when multiple rules target the same element.
    
19. **What is the difference between `em` and `rem` units?**
    
    > `em` is relative to the font-size of the parent, while `rem` is relative to the root element's font-size.
    
20. **How do you create a responsive layout?**
    
    > Using flexible grids, media queries, and relative units to adapt the layout to various screen sizes.
    

---

## 🧠 JavaScript Fundamentals

21. **What is JavaScript?**
    
    > JavaScript is a scripting language used to create and control dynamic website content.
    
22. **What are the different data types in JavaScript?**
    
    > Primitive types: `string`, `number`, `boolean`, `null`, `undefined`, `symbol`, `bigint`; Non-primitive: `object`.
    
23. **What is the difference between `==` and `===`?**
    
    > `==` compares values after type coercion, while `===` compares both value and type.
    
24. **What is a closure in JavaScript?**
    
    > A closure is a function that retains access to its lexical scope even when executed outside its original scope.
    
25. **What is hoisting in JavaScript?**
    
    > Hoisting is JavaScript's behavior of moving declarations to the top of the current scope before code execution.
    
26. **What are arrow functions?**
    
    > A concise syntax for writing functions using the `=>` notation.
    
27. **What is the difference between `var`, `let`, and `const`?**
    
    > - `var`: function-scoped, can be redeclared and updated.
    >     
    
    - `let`: block-scoped, can be updated but not redeclared.
        
    - `const`: block-scoped, cannot be updated or redeclared.
        
28. **What is the event loop in JavaScript?**
    
    > The event loop handles asynchronous callbacks by placing them in a queue and executing them after the current call stack is empty.
    
29. **What is the difference between synchronous and asynchronous code?**
    
    > Synchronous code is executed sequentially, blocking further execution until completion; asynchronous code allows other operations to continue before completion.
    
30. **What are Promises in JavaScript?**
    
    > Promises represent the eventual completion or failure of an asynchronous operation.
    

---

## ⚙️ Advanced JavaScript Concepts

31. **What is the `this` keyword in JavaScript?**
    
    > `this` refers to the object from which the function was called.
    
32. **What is prototypal inheritance?**
    
    > It's a feature where objects can inherit properties and methods from other objects.
    
33. **What is the difference between `call()`, `apply()`, and `bind()`?**
    
    > - `call()`: invokes a function with a given `this` value and arguments.
    >     
    
    - `apply()`: similar to `call()`, but arguments are provided as an array.
        
    - `bind()`: returns a new function with a bound `this` value.
        
34. **What are IIFEs (Immediately Invoked Function Expressions)?**
    
    > Functions that are executed immediately after their definition.
    
35. **What is event delegation?**
    
    > A technique where a single event listener is added to a parent element to handle events from its child elements.
    
36. **What is the difference between deep and shallow copy?**
    
    > A shallow copy duplicates only the top-level properties, while a deep copy duplicates all nested objects.
    
37. **What is the difference between `null` and `undefined`?**
    
    > `null` is an assignment value indicating no value, while `undefined` means a variable has been declared but not assigned a value.
    
38. **What is the purpose of the `async` and `await` keywords?**
    
    > They simplify working with Promises, allowing asynchronous code to be written in a synchronous style.
    
39. **What is a higher-order function?**
    
    > A function that takes another function as an argument or returns a function as a result.
    
40. **What is the difference between `map()`, `filter()`, and `reduce()`?**
    
    > - `map()`: creates a new array by applying a function to each element.
    >     
    
    - `filter()`: creates a new array with elements that pass a test.
        
    - `reduce()`: applies a function against an accumulator to reduce the array to a single value.
        

---

## 🌐 DOM Manipulation & Events

41. **What is the DOM?**
    
    > The Document Object Model is a programming interface for HTML and XML documents, representing the page so programs can change the document structure, style, and content.
    
42. **How do you select elements in the DOM?**
    
    > Using methods like `getElementById()`, `getElementsByClassName()`, `querySelector()`, and `querySelectorAll()`.
    
43. **How do you add an event listener to an element?**
    
    > Using `element.addEventListener('event', function)`.
    
44. **What is event bubbling and capturing?**
    
    > Event bubbling is the propagation of events from child to parent elements; capturing is the reverse.
    
45. **How do you prevent event propagation?**
    
    > Using `event.stopPropagation()`.
    
46. **How do you prevent the default behavior of an event?**
    
    > Using `event.preventDefault()`.
    
47. **How do you create and dispatch a custom event?**
    
    > Using the `CustomEvent` constructor and `dispatchEvent()` method.
    
48. **What is the difference between `innerHTML` and `textContent`?**
    
    > `innerHTML` parses content as HTML, while `textContent` treats content as plain text.
    
49. **How do you modify the attributes of an element?**
    
    > Using `setAttribute()`, `getAttribute()`, and `removeAttribute()` methods.
    
50. **How do you create a new element and append it to the DOM?**
    
    > Using `document.createElement()` and `appendChild()` methods.
    

---

## 📦 Web APIs & Browser Storage

51. **What is the Fetch API?**
    
    > A modern interface for making HTTP requests in JavaScript.
    
52. **How do you handle JSON data in JavaScript?**
    
    > Using `JSON.parse()` to convert JSON strings to objects and `JSON.stringify()` to convert objects to JSON strings.
    
53. **What is localStorage?**
    
    > A web storage object that allows storing key-value pairs in the browser with no expiration time.
    
54. **What is sessionStorage?**
    
    > Similar to localStorage, but data is cleared when the page session ends.
    
55. **What are cookies?**
    
    > Small pieces of data stored in the browser, sent with every HTTP request to the same domain.
    
56. **What is CORS (Cross-Origin Resource Sharing)?**
    
    > A mechanism that allows restricted resources on a web page to be requested from another domain.
    
57. **What is the purpose of the `navigator` object?**
    
    > Provides information about the browser and the operating system.
    
58. **What is the purpose of the `location` object?**
    
    > Provides information about the current URL and allows redirection.

## ⚛️ React & Component Architecture

### 51. **What is the Virtual DOM, and how does React use it?**

> The Virtual DOM is a lightweight JavaScript representation of the actual DOM. React uses it to optimize UI rendering by updating only the parts of the DOM that have changed, enhancing performance.

### 52. **Differentiate between Class and Functional Components in React.**

> Class components are ES6 classes extending `React.Component` with lifecycle methods. Functional components are plain JavaScript functions that can use hooks to manage state and side effects. Functional components are now preferred due to their simplicity and performance benefits.[dev.to](https://dev.to/ruppysuppy/17-react-interview-questions-you-must-know-as-a-developer-in-2025-1o6f?utm_source=chatgpt.com)

### 53. **What are React Hooks? Name a few commonly used ones.**

> Hooks are functions that let you use state and other React features in functional components. Common hooks include `useState`, `useEffect`, `useContext`, `useReducer`, and `useMemo`.

### 54. **Explain the purpose of `useEffect` hook.**

> `useEffect` allows you to perform side effects in functional components, such as data fetching, subscriptions, or manually changing the DOM. It runs after the render and can be configured to run on specific state or prop changes.

### 55. **What is the significance of keys in React lists?**

> Keys help React identify which items have changed, are added, or are removed. They should be unique and stable to ensure efficient re-rendering of list items.[dev.to](https://dev.to/ruppysuppy/17-react-interview-questions-you-must-know-as-a-developer-in-2025-1o6f?utm_source=chatgpt.com)

---

## 🚀 Performance Optimization

### 56. **How can you optimize React application performance?**

> - Use React's `PureComponent` or `React.memo` to prevent unnecessary re-renders.
>     
> - Implement code-splitting using dynamic `import()` and React.lazy.
>     
> - Utilize virtualization for long lists with libraries like `react-window`.
>     
> - Avoid inline functions and objects in render methods.
>     
> - Debounce or throttle expensive operations.[arxiv.org](https://arxiv.org/abs/2504.03884?utm_source=chatgpt.com)
>     

### 57. **What is code-splitting, and why is it important?**

> Code-splitting is the practice of breaking up your code into smaller chunks that can be loaded on demand. It improves initial load time and performance by loading only the necessary code for the current view.

### 58. **Explain lazy loading in React.**

> Lazy loading is a technique where components or resources are loaded only when needed. In React, `React.lazy()` and `Suspense` are used to load components lazily, enhancing performance by reducing the initial bundle size.

---

## ♿ Accessibility (a11y)

### 59. **What are ARIA roles, and how do they enhance accessibility?**

> ARIA (Accessible Rich Internet Applications) roles provide additional information to assistive technologies about the purpose of elements, improving accessibility for users with disabilities.

### 60. **How do you ensure keyboard accessibility in web applications?**

> - Ensure all interactive elements are focusable using `tabindex`.
>     
> - Use semantic HTML elements like `<button>`, `<a>`, and `<input>`.
>     
> - Manage focus states and visible indicators.
>     
> - Implement keyboard event handlers for custom components.
>     

---

## 🧪 Testing & Debugging

### 61. **What is the difference between unit testing and integration testing?**

> - Unit testing focuses on individual components or functions in isolation.
>     
> - Integration testing verifies the interaction between different components or modules to ensure they work together as expected.
>     

### 62. **Which tools are commonly used for testing React applications?**

> - Jest: A JavaScript testing framework for unit and integration tests.
>     
> - React Testing Library: For testing React components by simulating user interactions.
>     
> - Enzyme (less common now): For shallow rendering and component testing.
>     

---

## 🔐 Security Best Practices

### 63. **What is Cross-Site Scripting (XSS), and how can you prevent it?**

> XSS is a security vulnerability where attackers inject malicious scripts into web pages viewed by others. Prevention includes:
> 
> - Escaping user input.
>     
> - Validating and sanitizing inputs.
>     
> - Using Content Security Policy (CSP) headers.
>     

### 64. **Explain the concept of Cross-Origin Resource Sharing (CORS).**

> CORS is a security feature implemented by browsers to restrict web pages from making requests to a different domain than the one that served the web page. Servers can enable CORS by setting appropriate headers to allow cross-origin requests.

---

## 🧰 Tooling & Build Processes

### 65. **What is Webpack, and why is it used in frontend development?**

> Webpack is a module bundler that compiles JavaScript modules and other assets into a single bundle or multiple bundles, optimizing them for deployment. It handles dependencies, code splitting, and asset management.

### 66. **What is Babel, and how does it work?**

> Babel is a JavaScript compiler that converts modern JavaScript (ES6+) into backward-compatible versions for older browsers. It uses plugins and presets to transform code syntax.

---

## 🧩 Design Patterns & Architecture

### 67. **What is the Flux architecture, and how does Redux implement it?**

> Flux is a unidirectional data flow architecture where data flows from actions to dispatcher to stores and then to views. Redux implements Flux by providing a single store, pure reducer functions, and actions to manage state changes predictably.

### 68. **Explain the concept of Higher-Order Components (HOC) in React.**

> An HOC is a function that takes a component and returns a new component with enhanced behavior. It's used for code reuse, logic abstraction, and manipulating props.

---

## 🌐 Progressive Web Apps (PWA)

### 69. **What are Progressive Web Apps, and what are their key features?**

> PWAs are web applications that provide a native app-like experience. Key features include:
> 
> - Responsive design.
>     
> - Offline capabilities via service workers.
>     
> - Installable on devices.
>     
> - Push notifications.
>     
> - Fast loading and performance.[roadmap.sh](https://roadmap.sh/questions/frontend?utm_source=chatgpt.com)
>     

### 70. **How do service workers enhance PWA functionality?**

> Service workers act as a proxy between the web application and the network, enabling features like offline caching, background sync, and push notifications, thereby improving performance and reliability.

## ⚛️ React & Component Architecture

### 71. **What is the Virtual DOM, and how does React use it?**

> The Virtual DOM is a lightweight JavaScript representation of the actual DOM. React uses it to optimize UI rendering by updating only the parts of the DOM that have changed, enhancing performance.

### 72. **Differentiate between Class and Functional Components in React.**

> Class components are ES6 classes extending `React.Component` with lifecycle methods. Functional components are plain JavaScript functions that can use hooks to manage state and side effects. Functional components are now preferred due to their simplicity and performance benefits.

### 73. **What are React Hooks? Name a few commonly used ones.**

> Hooks are functions that let you use state and other React features in functional components. Common hooks include `useState`, `useEffect`, `useContext`, `useReducer`, and `useMemo`.

### 74. **Explain the purpose of `useEffect` hook.**

> `useEffect` allows you to perform side effects in functional components, such as data fetching, subscriptions, or manually changing the DOM. It runs after the render and can be configured to run on specific state or prop changes.

### 75. **What is the significance of keys in React lists?**

> Keys help React identify which items have changed, are added, or are removed. They should be unique and stable to ensure efficient re-rendering of list items.

---

## 🚀 Performance Optimization

### 76. **How can you optimize React application performance?**

> - Use React's `PureComponent` or `React.memo` to prevent unnecessary re-renders.
>     
> - Implement code-splitting using dynamic `import()` and React.lazy.
>     
> - Utilize virtualization for long lists with libraries like `react-window`.
>     
> - Avoid inline functions and objects in render methods.
>     
> - Debounce or throttle expensive operations.
>     

### 77. **What is code-splitting, and why is it important?**

> Code-splitting is the practice of breaking up your code into smaller chunks that can be loaded on demand. It improves initial load time and performance by loading only the necessary code for the current view.

### 78. **Explain lazy loading in React.**

> Lazy loading is a technique where components or resources are loaded only when needed. In React, `React.lazy()` and `Suspense` are used to load components lazily, enhancing performance by reducing the initial bundle size.

---

## ♿ Accessibility (a11y)

### 79. **What are ARIA roles, and how do they enhance accessibility?**

> ARIA (Accessible Rich Internet Applications) roles provide additional information to assistive technologies about the purpose of elements, improving accessibility for users with disabilities.

### 80. **How do you ensure keyboard accessibility in web applications?**

> - Ensure all interactive elements are focusable using `tabindex`.
>     
> - Use semantic HTML elements like `<button>`, `<a>`, and `<input>`.
>     
> - Manage focus states and visible indicators.
>     
> - Implement keyboard event handlers for custom components.
>     

---

## 🧪 Testing & Debugging

### 81. **What is the difference between unit testing and integration testing?**

> - Unit testing focuses on individual components or functions in isolation.
>     
> - Integration testing verifies the interaction between different components or modules to ensure they work together as expected.
>     

### 82. **Which tools are commonly used for testing React applications?**

> - Jest: A JavaScript testing framework for unit and integration tests.
>     
> - React Testing Library: For testing React components by simulating user interactions.
>     
> - Enzyme (less common now): For shallow rendering and component testing.
>     

---

## 🔐 Security Best Practices

### 83.**What is Cross-Site Scripting (XSS), and how can you prevent it?**

> XSS is a security vulnerability where attackers inject malicious scripts into web pages viewed by others. Prevention includes:
> 
> - Escaping user input.
>     
> - Validating and sanitizing inputs.
>     
> - Using Content Security Policy (CSP) headers.
>     

### 84.**Explain the concept of Cross-Origin Resource Sharing (CORS).**

> CORS is a security feature implemented by browsers to restrict web pages from making requests to a different domain than the one that served the web page. Servers can enable CORS by setting appropriate headers to allow cross-origin requests.

---

## 🧰 Tooling & Build Processes

### 85. **What is Webpack, and why is it used in frontend development?**

> Webpack is a module bundler that compiles JavaScript modules and other assets into a single bundle or multiple bundles, optimizing them for deployment. It handles dependencies, code splitting, and asset management.

### 86. **What is Babel, and how does it work?**

> Babel is a JavaScript compiler that converts modern JavaScript (ES6+) into backward-compatible versions for older browsers. It uses plugins and presets to transform code syntax.

---

## 🧩 Design Patterns & Architecture

### 87. **What is the Flux architecture, and how does Redux implement it?**

> Flux is a unidirectional data flow architecture where data flows from actions to dispatcher to stores and then to views. Redux implements Flux by providing a single store, pure reducer functions, and actions to manage state changes predictably.

### 88. **Explain the concept of Higher-Order Components (HOC) in React.**

> An HOC is a function that takes a component and returns a new component with enhanced behavior. It's used for code reuse, logic abstraction, and manipulating props.

---

## 🌐 Progressive Web Apps (PWA)

### 89. **What are Progressive Web Apps, and what are their key features?**

> PWAs are web applications that provide a native app-like experience. Key features include:
> 
> - Responsive design.
>     
> - Offline capabilities via service workers.
>     
> - Installable on devices.
>     
> - Push notifications.
>     
> - Fast loading and performance.[naukri.com](https://www.naukri.com/code360/library/full-stack--developer-interview-questions?utm_source=chatgpt.com)
>     

### 90. **How do service workers enhance PWA functionality?**

> Service workers act as a proxy between the web application and the network, enabling features like offline caching, background sync, and push notifications, thereby improving performance and reliability.

