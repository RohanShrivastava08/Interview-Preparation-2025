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

---
---

## 🚀 SECTION 2: Express.js & REST APIs (Q21–40)

### 21. **What is Express.js?**

Express is a minimal and flexible Node.js web application framework that simplifies routing and middleware.

---

### 22. **How do you create a basic Express server?**

js

CopyEdit

`const express = require('express'); const app = express(); app.get('/', (req, res) => res.send('Hello World!')); app.listen(3000);`

---

### 23. **What is middleware in Express?**

Middleware are functions executed in sequence on request/response cycle. E.g., logging, auth, parsing JSON.

---

### 24. **What is body-parser?**

`body-parser` parses incoming request bodies. Now built into Express via `express.json()` and `express.urlencoded()`.

---

### 25. **Difference between `res.send()` and `res.json()`?**

- `res.send()`: Sends any type of response
    
- `res.json()`: Sends JSON with appropriate headers
    

---

### 26. **How to define routes in Express?**

js

CopyEdit

`app.get('/route', handler); app.post('/route', handler);`

---

### 27. **What is the use of `next()` in middleware?**

It passes control to the next middleware function.

---

### 28. **What are route parameters in Express?**

js

CopyEdit

`app.get('/user/:id', (req, res) => res.send(req.params.id));`

---

### 29. **How do you handle errors in Express?**

Use an error-handling middleware:

js

CopyEdit

`app.use((err, req, res, next) => {   res.status(500).send('Something broke!'); });`

---

### 30. **What is CORS and how do you enable it?**

CORS allows cross-origin requests.

js

CopyEdit

`const cors = require('cors'); app.use(cors());`

---

### 31. **How do you handle JSON request data in Express?**

js

CopyEdit

`app.use(express.json());`

---

### 32. **What is the difference between PUT and PATCH?**

- `PUT`: Replaces the entire resource
    
- `PATCH`: Updates part of the resource
    

---

### 33. **What are status codes in HTTP?**

- 200: OK
    
- 201: Created
    
- 400: Bad Request
    
- 401: Unauthorized
    
- 500: Internal Server Error
    

---

### 34. **How do you redirect a route in Express?**

js

CopyEdit

`res.redirect('/new-url');`

---

### 35. **How to serve static files in Express?**

js

CopyEdit

`app.use(express.static('public'));`

---

### 36. **How do you read query parameters in Express?**

js

CopyEdit

`req.query // { search: 'nodejs' }`

---

### 37. **What is helmet in Express?**

`helmet` adds security headers to protect your app.

---

### 38. **What is morgan in Express?**

`morgan` is an HTTP request logger middleware.

---

### 39. **How to send a file using Express?**

js

CopyEdit

`res.sendFile(__dirname + '/file.pdf');`

---

### 40. **How to handle 404 in Express?**

js

CopyEdit

`app.use((req, res) => res.status(404).send('Not Found'));`

---
---

## 📁 SECTION 3: File System, Events & Utilities (Q41–60)

---

### 41. **What is the `fs` module in Node.js?**

The `fs` (File System) module allows you to work with the file system — reading, writing, updating, and deleting files.

js

CopyEdit

`const fs = require('fs'); fs.readFile('file.txt', 'utf8', (err, data) => {   if (err) throw err;   console.log(data); });`

---

### 42. **Difference between synchronous and asynchronous file operations?**

- **Sync**: Blocks execution until operation completes.
    
- **Async**: Non-blocking, uses callback or Promise.
    

js

CopyEdit

`fs.readFileSync() // Blocking fs.readFile()     // Non-blocking`

---

### 43. **How to write a file asynchronously?**

js

CopyEdit

`fs.writeFile('output.txt', 'Hello!', err => {   if (err) throw err; });`

---

### 44. **How to append data to a file?**

js

CopyEdit

`fs.appendFile('log.txt', 'New log\n', err => {   if (err) throw err; });`

---

### 45. **How to delete a file using Node.js?**

js

CopyEdit

`fs.unlink('delete-me.txt', err => {   if (err) throw err; });`

---

### 46. **What are events in Node.js?**

Node.js has an **EventEmitter** class that allows event-driven programming. You can emit and listen to events.

---

### 47. **How to use EventEmitter?**

js

CopyEdit

`const EventEmitter = require('events'); const emitter = new EventEmitter();  emitter.on('start', () => console.log('Started')); emitter.emit('start');`

---

### 48. **What are some core Node.js events?**

- `data` (streams)
    
- `end`
    
- `error`
    
- `connection` (servers)
    
- Custom events via `EventEmitter`
    

---

### 49. **What is a stream?**

Streams are used to handle large chunks of data efficiently by processing it in smaller pieces.

---

### 50. **Types of Streams in Node.js:**

- **Readable**: Read data (e.g., `fs.createReadStream`)
    
- **Writable**: Write data
    
- **Duplex**: Both readable and writable
    
- **Transform**: Modify data while streaming
    

---

### 51. **How to create a readable stream?**

js

CopyEdit

`const rs = fs.createReadStream('file.txt'); rs.on('data', chunk => console.log(chunk));`

---

### 52. **How to pipe streams?**

js

CopyEdit

`const rs = fs.createReadStream('file.txt'); const ws = fs.createWriteStream('copy.txt'); rs.pipe(ws);`

---

### 53. **What is `path` module?**

`path` provides utilities to work with file and directory paths.

js

CopyEdit

`const path = require('path'); console.log(path.basename('/dir/file.txt')); // file.txt`

---

### 54. **What is `os` module?**

It provides info about the system — CPU, memory, hostname, platform.

js

CopyEdit

`const os = require('os'); console.log(os.platform(), os.cpus().length);`

---

### 55. **How to create directories in Node.js?**

js

CopyEdit

`fs.mkdir('newFolder', err => {   if (err) throw err; });`

---

### 56. **How to read all files in a directory?**

js

CopyEdit

`fs.readdir('./folder', (err, files) => {   if (err) throw err;   console.log(files); });`

---

### 57. **What is `util.promisify`?**

It converts callback-based functions into Promise-based ones.

js

CopyEdit

`const util = require('util'); const readFile = util.promisify(fs.readFile);`

---

### 58. **What is `process` object?**

Gives info and control over the current Node.js process.

js

CopyEdit

`process.argv // CLI arguments process.env  // Environment variables process.exit() // Exit process`

---

### 59. **How to read command-line arguments?**

js

CopyEdit

`console.log(process.argv); // ['node', 'app.js', 'arg1', 'arg2']`

---

### 60. **What is the difference between `__dirname` and `__filename`?**

- `__dirname`: Directory of current module
    
- `__filename`: Full path of the current file

---
---

