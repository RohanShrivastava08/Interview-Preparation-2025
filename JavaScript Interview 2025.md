Total: **115 Questions**  
Categorized into: Basics, Functions, Scopes & Closures, Objects & Arrays, Advanced Concepts, DOM, Async JS, ES6+, and Tricky/Edge Cases.

---

### 🟢 **Section 1: JavaScript Basics (Q1–Q20)**

1. **What is JavaScript?**
    
    > JavaScript is a high-level, interpreted scripting language used to build interactive websites. It is dynamically typed, prototype-based, and supports OOP, functional, and imperative styles.
    
2. **Is JavaScript single-threaded or multi-threaded?**
    
    > JavaScript is single-threaded, using an event loop and callback queue to handle asynchronous tasks.
    
3. **What are data types in JavaScript?**
    
    > **Primitive:** String, Number, Boolean, BigInt, undefined, null, Symbol  
    > **Non-Primitive:** Objects (arrays, functions, etc.)
    
4. **What is the difference between `null` and `undefined`?**
    
    - `null` = assigned explicitly (absence of value)
        
    - `undefined` = variable declared but not assigned.
        
5. **What are the falsy values in JavaScript?**
    
    > `false`, `0`, `""`, `null`, `undefined`, `NaN`
    
6. **How does type coercion work in JavaScript?**
    
    > JavaScript automatically converts types during operations (`'5' + 1` becomes `'51'`).
    
7. **What’s the difference between `==` and `===`?**
    
    > `==` compares with coercion, `===` compares without coercion (strict equality).
    
8. **What are template literals?**
    
    > Syntax: `` `Hello ${name}` ``; they support interpolation and multiline strings.
    
9. **What is the difference between `var`, `let`, and `const`?**
    
    - `var` = function-scoped, hoisted
        
    - `let` = block-scoped
        
    - `const` = block-scoped + can't be reassigned
        
10. **Explain hoisting.**
    
    > Declarations (`var`, `function`) are moved to the top of their scope during compilation.
    
11. **What is NaN?**
    
    > Not-a-Number — a special value indicating an invalid number operation (`parseInt('abc')`).
    
12. **What is the difference between `typeof` and `instanceof`?**
    
    - `typeof` checks primitive types
        
    - `instanceof` checks prototype chain for object types
        
13. **What is the purpose of `isNaN()`?**
    
    > To check if a value is **NaN** after coercion.
    
14. **What is the use of `typeof null` returning `'object'`?**
    
    > It's a historical bug in JS.
    
15. **How do you check if a variable is an array?**
    
    js
    
    CopyEdit
    
    `Array.isArray(value)`
    
16. **What is the difference between `slice()` and `splice()`?**
    
    - `slice(start, end)` = returns a portion (non-destructive)
        
    - `splice(start, deleteCount)` = modifies original array
        
17. **What is `use strict`?**
    
    > A directive to enforce stricter parsing and error handling.
    
18. **What are higher-order functions?**
    
    > Functions that take other functions as arguments or return functions.
    
19. **What is the output of `typeof NaN`?**
    
    > `'number'` – even though it's Not-a-Number.
    
20. **Explain the event loop in simple terms.**
    
    > JavaScript runs sync code, and async tasks are handled in the background. The event loop puts async results (callbacks, promises) back into the call stack via the queue.
    

---

### 🟡 **Section 2: Functions, Scope, and Closures (Q21–Q40)**

21. **What are closures in JavaScript?**
    
    > A closure is when an inner function has access to the outer function's variables even after the outer function has returned.
    
22. **What is lexical scoping?**
    
    > Scope is defined by the placement of functions and blocks during code writing, not runtime.
    
23. **Explain IIFE (Immediately Invoked Function Expression).**
    
    js
    
    CopyEdit
    
    `(function() {   // Code runs here })();`
    
24. **Difference between function declaration and expression?**
    
    - Declaration: `function foo() {}` (hoisted)
        
    - Expression: `const foo = function() {}` (not hoisted)
        
25. **What is function currying?**
    
    > Transforming a function with multiple arguments into a sequence of functions with one argument each.
    
26. **What is a callback function?**
    
    > A function passed as an argument to another, to be executed later.
    
27. **What is the call stack?**
    
    > A stack data structure where JS keeps track of function calls.
    
28. **What is `this` keyword?**
    
    > Refers to the object from where the function is called. In global scope, `this` is `window`.
    
29. **What are arrow functions and their differences from regular functions?**
    
    - Short syntax
        
    - No `this`, no `arguments`, not constructible (no `new`)
        
30. **What is the difference between `.call()`, `.apply()` and `.bind()`?**
    
    - `call`: `fn.call(obj, a, b)`
        
    - `apply`: `fn.apply(obj, [a, b])`
        
    - `bind`: returns a new function with `this` bound
        
31. **What is the Temporal Dead Zone (TDZ)?**
    
    > The time between entering scope and variable declaration where `let`/`const` cannot be accessed.
    
32. **What is recursion?**
    
    > A function calling itself to solve problems.
    
33. **How is memory managed in JavaScript?**
    
    > JS uses garbage collection; memory is freed for objects no longer reachable.
    
34. **What is the difference between pure and impure functions?**
    
    - Pure: No side effects, returns same output for same input
        
    - Impure: Causes side effects (e.g., modifies global variable)
        
35. **What are generator functions?**
    
    js
    
    CopyEdit
    
    `function* gen() {   yield 1;   yield 2; }`
    
36. **What are arrow function limitations?**
    
    > No `this`, no `arguments`, not suitable for methods or constructors.
    
37. **Explain `.arguments` object.**
    
    > An array-like object in normal functions that holds all passed parameters.
    
38. **Difference between global scope and block scope?**
    
    > Global: Accessible everywhere  
    > Block: `{}` enclosed, e.g. `let` and `const` follow block scope.
    
39. **What is shadowing in JavaScript?**
    
    > A variable declared in a local scope with the same name as one in outer scope.
    
40. **Can you create private variables in JS?**
    
    > Yes, using closures or ES6 classes with `#privateField`.
    

---

### 🔵 **Section 3: Objects, Arrays, and Prototypes (Q41–Q60)**

41. **How do you clone an object?**
    
    js
    
    CopyEdit
    
    `const clone = {...obj}; // shallow`
    
42. **How do you deep clone an object?**
    
    js
    
    CopyEdit
    
    `const deep = JSON.parse(JSON.stringify(obj)); // simple but loses functions`
    
43. **What is the prototype chain?**
    
    > Objects inherit properties from prototypes. The chain continues until `null`.
    
44. **What is `Object.create()`?**
    
    > Creates a new object with the specified prototype object.
    
45. **What are getters and setters?**
    
    js
    
    CopyEdit
    
    `get name() {...} set name(value) {...}`
    
46. **Difference between map() and forEach()?**
    
    - `map()` returns a new array
        
    - `forEach()` executes a function but returns `undefined`
        
47. **What is destructuring?**
    
    js
    
    CopyEdit
    
    `const {name} = obj; const [a, b] = arr;`
    
48. **How do you merge two objects?**
    
    js
    
    CopyEdit
    
    `const merged = {...obj1, ...obj2};`
    
49. **What are Symbols used for?**
    
    > Unique and immutable identifiers often used for private object keys.
    
50. **How do you iterate over object keys?**
    
    js
    
    CopyEdit
    
    `for (let key in obj) // includes inherited Object.keys(obj).forEach(...)`
    
51. **Explain object immutability.**
    
    > Using `Object.freeze(obj)` or patterns like Redux to avoid state mutation.
    
52. **Difference between shallow and deep copy?**
    
    - Shallow: Only top-level references copied
        
    - Deep: Nested objects are also cloned
        
53. **What is the use of `hasOwnProperty()`?**
    
    > Checks if a property exists directly on the object (not inherited).
    
54. **How to prevent object mutation?**
    
    > Use `Object.freeze()` or libraries like Immer.
    
55. **What is the difference between `in` and `hasOwnProperty()`?**
    
    - `in` checks own + inherited
        
    - `hasOwnProperty()` checks only own
        
56. **What is optional chaining (`?.`) in JS?**
    
    js
    
    CopyEdit
    
    `user?.address?.street`
    
57. **Explain rest and spread operators.**
    
    - Rest: collect arguments — `...args`
        
    - Spread: expand values — `{...obj}`
        
58. **What’s the difference between `Object.keys()`, `Object.values()`, and `Object.entries()`?**
    
    - Keys: returns keys
        
    - Values: values
        
    - Entries: [key, value] pairs
        
59. **What is a factory function?**
    
    > A function that returns a new object (used instead of classes sometimes).
    
60. **What is object destructuring with defaults?**
    
    js
    
    CopyEdit
    
    `const { name = 'Guest' } = user;`

## 🧩 **Section 4: Asynchronous JavaScript (Q61–Q80)**

61. **What is asynchronous JavaScript?**
    

> Code that doesn't block execution. JS uses callbacks, promises, and `async/await` to handle async operations like API calls, timers, etc.

62. **What is a callback?**
    

> A function passed into another function to be executed later.

63. **What are Promises in JavaScript?**
    

> An object representing the eventual completion (or failure) of an async operation.

js

CopyEdit

`const p = new Promise((resolve, reject) => {   resolve('Success'); });`

64. **What are the states of a Promise?**
    

- `pending`
    
- `fulfilled`
    
- `rejected`
    

65. **What is `.then()` and `.catch()`?**
    

> `.then()` handles success, `.catch()` handles failure.

66. **What is `finally()` in promises?**
    

> Executes regardless of success or failure.

js

CopyEdit

`promise.then().catch().finally(() => console.log('Done'));`

67. **What is async/await?**
    

> Syntax sugar over Promises to write async code like synchronous code.

js

CopyEdit

`async function fetchData() {   const data = await fetch('url'); }`

68. **What is the event loop in JavaScript?**
    

> A mechanism that allows JS to perform non-blocking I/O by offloading tasks and waiting for results via a queue.

69. **What is the microtask queue?**
    

> Queue for promises (`.then`, `await`) — executes before macrotasks (e.g., `setTimeout`).

70. **Difference between microtasks and macrotasks?**
    

- **Microtasks:** Promises, `queueMicrotask`
    
- **Macrotasks:** `setTimeout`, `setInterval`, DOM events
    

71. **What is callback hell and how to avoid it?**
    

> Nested callbacks leading to unreadable code. Avoid using Promises or `async/await`.

72. **What is the purpose of `Promise.all()`?**
    

> Runs multiple promises in parallel and waits for all to resolve or any to reject.

73. **What is `Promise.race()`?**
    

> Resolves/rejects as soon as the **first** promise resolves/rejects.

74. **What is `Promise.any()`?**
    

> Resolves as soon as **any one** of the promises fulfills (ignores rejections).

75. **What is `Promise.allSettled()`?**
    

> Waits for **all promises to settle** (either fulfilled or rejected).

76. **Can async functions run in parallel?**
    

> Yes, if you use `Promise.all()` to initiate them concurrently.

77. **How does `await` work internally?**
    

> Pauses function execution and resumes it when the awaited promise resolves.

78. **What happens if `await` is used outside an async function?**
    

> Syntax error — must be inside an `async` function.

79. **Can you make a synchronous function wait?**
    

> Not directly — JS is single-threaded. Use Promises or async/await instead.

80. **How do you handle errors in async/await?**
    

js

CopyEdit

`try {   const res = await fetch('url'); } catch (err) {   console.error(err); }`

---

## 💎 **Section 5: ES6+ and Modern JS Features (Q81–Q95)**

81. **What’s new in ES6?**
    

> `let`, `const`, arrow functions, template literals, destructuring, rest/spread, classes, promises, modules.

82. **What are ES modules and how are they imported/exported?**
    

js

CopyEdit

`// file.js export const name = "Rohan";  // main.js import { name } from './file.js';`

83. **What are sets and maps?**
    

- `Set`: stores unique values
    
- `Map`: key-value pairs with any type as key
    

84. **Difference between `Map` and `Object`?**
    

> `Map` allows any keys, maintains insertion order, and has better performance with frequent additions/removals.

85. **What is optional chaining (`?.`) used for?**
    

> To safely access deeply nested properties without error.

js

CopyEdit

`user?.address?.city`

86. **What is the nullish coalescing operator (`??`)?**
    

> Returns right-hand operand **only if** left is `null` or `undefined`.

js

CopyEdit

`let name = userInput ?? "Guest";`

87. **What is destructuring in function parameters?**
    

js

CopyEdit

`function greet({name, age}) {   console.log(name); }`

88. **What is dynamic import?**
    

> ES2020 feature to lazy-load modules.

js

CopyEdit

`const module = await import('./utils.js');`

89. **What is BigInt?**
    

> A numeric primitive that can represent integers with arbitrary precision.

js

CopyEdit

`const big = 123n;`

90. **What are WeakMap and WeakSet?**
    

> Like Map/Set but keys are weakly referenced (not prevented from garbage collection).

91. **What is a tagged template literal?**
    

js

CopyEdit

``function tag(strings, ...values) {   // Custom processing } tag`Hello ${name}`;``

92. **What is the use of `Symbol.iterator`?**
    

> Makes objects iterable in `for...of` loops.

93. **What is tail call optimization?**
    

> A way to optimize recursive calls. Not widely supported yet in all JS engines.

94. **What is `Object.fromEntries()`?**
    

js

CopyEdit

`Object.fromEntries([['name', 'Rohan']]); // {name: 'Rohan'}`

95. **How do you make a function parameter required in ES6?**
    

js

CopyEdit

`function foo(x = throw new Error("x is required")) {}`

---

## ⚠️ **Section 6: Tricky / Edge Case JS Questions (Q96–Q115)**

96. **What’s the result of `[] + []`?**
    

> `""` — Both arrays converted to strings, then concatenated.

97. **What’s the result of `{} + []`?**
    

> `'[object Object]'` — confusing due to parsing ambiguity.

98. **What is the output of `typeof null`?**
    

> `'object'` — a bug in JS.

99. **Can you reassign `const` objects?**
    

> You can mutate them, but not reassign:

js

CopyEdit

`const obj = {}; obj.name = 'Rohan'; // ✅ obj = {}; // ❌`

100. **What is the output of `[1,2,3] == [1,2,3]`?**
    

> `false` — arrays are reference types.

101. **What is the result of `false == '0'`?**
    

> `true` — type coercion

102. **What is the result of `true + false`?**
    

> `1` — `true` is 1, `false` is 0

103. **What does `delete obj.prop` do?**
    

> Removes the property from object if configurable.

104. **What happens if you use `new` with an arrow function?**
    

> Throws error — arrow functions are not constructible.

105. **What’s the difference between `Object.seal()` and `Object.freeze()`?**
    

- `seal`: can't add/remove props, but can modify
    
- `freeze`: can’t modify anything
    

106. **What is the result of `typeof function(){} instanceof Function`?**
    

> `true`

107. **How can you delay execution in JS?**
    

js

CopyEdit

`setTimeout(() => console.log("Hello"), 1000);`

108. **What does `[].length = 0` do?**
    

> Empties the array.

109. **What happens when you do `Math.max()` with no arguments?**
    

> Returns `-Infinity`

110. **What’s the result of `NaN === NaN`?**
    

> `false`

111. **How to check if value is really NaN?**
    

js

CopyEdit

`Number.isNaN(value)`

112. **Can object keys be numbers?**
    

> Technically yes, but they get coerced to strings.

113. **What’s the output of `typeof undefined == typeof NULL`?**
    

> `ReferenceError` — NULL is undefined (uppercase).

114. **What is function memoization?**
    

> Caching results of function calls to improve performance.

115. **Can you override native prototypes? Should you?**
    

> Yes, but it’s **strongly discouraged** due to maintenance and compatibility issues.