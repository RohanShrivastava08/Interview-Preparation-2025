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