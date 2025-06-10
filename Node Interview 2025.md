## 🔰 **Beginner-Level Node.js Questions (1–60)**

### 1. **What is Node.js?**

Node.js is an open-source, cross-platform JavaScript runtime environment that executes JavaScript code outside a browser. It’s built on Chrome's V8 engine and is designed for building scalable network applications.

### 2. **Why use Node.js?**

- Non-blocking I/O
    
- Fast performance (V8 engine)
    
- Single programming language (JavaScript)
    
- Ideal for real-time applications
    
- Large ecosystem (npm)
    

### 3. **What is the V8 engine?**

V8 is Google’s open-source high-performance JavaScript engine used in Chrome and Node.js. It compiles JavaScript to native machine code before execution.

### 4. **Is Node.js single-threaded?**

Yes, Node.js uses a single-threaded event loop architecture, but it can handle concurrent connections efficiently through non-blocking I/O.

### 5. **What is the difference between asynchronous and non-blocking in Node.js?**

- **Asynchronous**: Code runs independently and notifies when complete.
    
- **Non-blocking**: Doesn’t block execution; tasks run in the background.
    

### 6. **What is npm?**

npm (Node Package Manager) is the default package manager for Node.js. It manages dependencies, installs packages, and allows sharing of reusable code.

### 7. **What is the purpose of package.json?**

It stores metadata about the project including scripts, dependencies, version, author, and entry point.

### 8. **How do you install a package globally and locally in npm?**

- **Globally**: `npm install -g package-name`
    
- **Locally**: `npm install package-name`
    

### 9. **What is the difference between dependencies and devDependencies?**

- `dependencies`: Required to run the app.
    
- `devDependencies`: Required only during development/testing.
    

### 10. **How do you initialize a Node.js project?**

bash

CopyEdit

`npm init`
### 11. **What is a callback function?**

A function passed as an argument to another function, to be executed later.

### 12. **What are Promises?**

Objects representing the eventual completion (or failure) of an async operation.

### 13. **What is async/await?**

Syntactic sugar over Promises, making asynchronous code look synchronous.

### 14. **Explain the Event Loop in Node.js.**

The Event Loop is a mechanism that allows Node.js to handle asynchronous tasks using callbacks, promises, etc., in a non-blocking way.

### 15. **What are streams in Node.js?**

Streams are objects that allow reading or writing data piece by piece (streaming), useful for large files.

### 16. **Types of streams?**

- Readable
    
- Writable
    
- Duplex
    
- Transform
    

### 17. **What are buffers in Node.js?**

Raw memory allocations used for binary data (e.g., file streams).

### 18. **What is the use of `require()`?**

It loads modules in Node.js using CommonJS.

### 19. **What is module.exports?**

It allows you to export functions/objects from a module to be used elsewhere.

### 20. **Difference between require and import?**

- `require`: CommonJS
    
- `import`: ES Modules (used with `.mjs` or `"type": "module"` in package.json)