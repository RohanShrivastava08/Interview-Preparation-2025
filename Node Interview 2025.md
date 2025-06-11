## 📘 SECTION 1: Core Node.js Fundamentals (Q1–20)

### 1. **What is Node.js?**

Node.js is an open-source, cross-platform JavaScript runtime built on Chrome's V8 engine. It allows JavaScript to run on the server, enabling backend development using JavaScript.

---

### 2. **Why is Node.js popular?**

- Single-threaded, non-blocking architecture
    
- Uses JavaScript across the stack
    
- Fast I/O operations (thanks to V8)
    
- Scalable for I/O-intensive apps
    
- Rich npm ecosystem
    

---

### 3. **Is Node.js single-threaded? How does it handle concurrency?**

Yes. Node.js uses an event loop and asynchronous I/O to handle many connections simultaneously without multiple threads.

---

### 4. **What is the Event Loop?**

The event loop is a continuous cycle that listens for and processes events (I/O, timers, etc.). It allows Node.js to perform non-blocking I/O on a single thread.

---

### 5. **What are Blocking vs Non-blocking calls?**

- **Blocking**: Waits for an operation to complete before proceeding.
    
- **Non-blocking**: Continues execution and handles result via callbacks or promises.
    

---

### 6. **What is npm?**

npm (Node Package Manager) manages dependencies, installs third-party libraries, and runs scripts in Node.js applications.

---

### 7. **What is package.json?**

`package.json` defines metadata, dependencies, scripts, and entry points of a Node.js project.

---

### 8. **Difference between `dependencies` and `devDependencies`?**

- `dependencies`: Required in production
    
- `devDependencies`: Needed only for development (e.g., testing tools)
    

---

### 9. **How to initialize a project using npm?**

bash

CopyEdit

`npm init # or npm init -y`

---

### 10. **What is `require()` used for?**

`require()` is a CommonJS function used to import modules.

---

### 11. **What is `module.exports`?**

It defines what a module exports and makes available for `require()` in another file.

---

### 12. **Difference between `require` and `import`?**

- `require`: CommonJS (Node default)
    
- `import`: ES Module (used with `"type": "module"` in `package.json` or `.mjs` extension)
    

---

### 13. **What is a callback function?**

A callback is a function passed to another function, to be executed later (especially after async operations).

---

### 14. **What are Promises?**

A Promise is an object representing a value that may be available now, in the future, or never. It has three states: `pending`, `fulfilled`, `rejected`.

---

### 15. **What is async/await?**

It’s syntax sugar over Promises to write async code in a synchronous style.

js

CopyEdit

`async function getData() {   try {     const data = await fetchData();   } catch (err) {     console.error(err);   } }`

---

### 16. **What is a Buffer?**

Buffer is a Node.js class to handle binary data directly in memory, useful when dealing with streams, files, etc.

---

### 17. **What are Streams in Node.js?**

Streams are objects that let you read/write data piece-by-piece.

- Types: Readable, Writable, Duplex, Transform
    

---

### 18. **Difference between `setImmediate()` and `process.nextTick()`?**

- `process.nextTick()`: Executes after the current operation ends, before the event loop continues.
    
- `setImmediate()`: Executes in the next iteration of the event loop.
    

---

### 19. **How does the V8 engine help Node.js?**

It compiles JavaScript to optimized machine code, enabling fast execution.

---

### 20. **What is REPL in Node.js?**

REPL stands for Read–Eval–Print–Loop, a command-line tool for running JavaScript interactively.