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

## ⚙️ SECTION 4: Intermediate & Performance Topics (Q61–90)

---

### 61. **How to handle uncaught exceptions?**

js

CopyEdit

`process.on('uncaughtException', err => {   console.error('Unhandled Exception:', err); });`

---

### 62. **How to handle unhandled promise rejections?**

js

CopyEdit

`process.on('unhandledRejection', err => {   console.error('Unhandled Rejection:', err); });`

---

### 63. **How to create a custom module?**

js

CopyEdit

`// math.js module.exports.add = (a, b) => a + b;  // app.js const math = require('./math'); math.add(2, 3);`

---

### 64. **What is a cluster in Node.js?**

`cluster` module allows creation of child processes (workers) to utilize multi-core systems.

---

### 65. **When should you use clustering?**

For CPU-bound tasks or to improve throughput by balancing load across cores.

---

### 66. **What is the difference between fork and spawn in child_process?**

- `fork`: Spawns a new Node.js process and can send messages
    
- `spawn`: Launches any new process
    

---

### 67. **How to use `child_process` module?**

js

CopyEdit

`const { exec } = require('child_process'); exec('ls', (err, stdout) => console.log(stdout));`

---

### 68. **How does Node handle asynchronous code under the hood?**

Via libuv — which uses a thread pool, the event loop, and OS-level non-blocking I/O operations.

---

### 69. **What is `global` in Node.js?**

It’s the global namespace object (like `window` in browsers).

js

CopyEdit

`global.myVar = 5;`

---

### 70. **What are environment variables in Node.js?**

Stored in `process.env`. Used to configure apps without hardcoding secrets or settings.

---

### 71. **How to load `.env` file values?**

Use the `dotenv` package:

js

CopyEdit

`require('dotenv').config(); console.log(process.env.API_KEY);`

---

### 72. **What are template engines?**

They generate HTML pages dynamically. Examples:

- EJS
    
- Pug
    
- Handlebars
    

---

### 73. **What is the role of `res.locals` in Express?**

Stores local variables scoped to the request, accessible in templates.

---

### 74. **What is a memory leak and how to avoid it in Node.js?**

A memory leak occurs when objects are not garbage collected. Use tools like `clinic.js`, `heapdump`, and avoid holding large unused references.

---

### 75. **What is garbage collection in Node.js?**

Automatic process by V8 that reclaims memory used by unreachable objects.

---

### 76. **How to debug a Node.js app?**

- Use `node inspect` or `--inspect` flag
    
- Debug tools like VS Code debugger
    
- Use console logs or `debug` module
    

---

### 77. **What are microservices in Node.js context?**

Independent small services that interact via HTTP, message queues, or events. Ideal for scaling Node apps.

---

### 78. **How to measure performance of a Node.js app?**

- Use built-in `console.time()`
    
- Use profiling tools like `clinic.js`, `node --prof`
    

---

### 79. **What is middleware chaining?**

The sequential execution of multiple middleware functions via `next()` in Express.

---

### 80. **What is an IIFE and why used in Node?**

Immediately Invoked Function Expression to encapsulate variables:

js

CopyEdit

`(function() {   // isolated scope })();`

---

### 81. **What is the default behavior of `require()`?**

- Loads `.js`, `.json`, `.node` files
    
- Caches modules on first load
    

---

### 82. **Can you use ES6 modules in Node?**

Yes, via:

- `"type": "module"` in `package.json`
    
- `.mjs` file extension
    

---

### 83. **What is the difference between `exports` and `module.exports`?**

Both export values, but `module.exports` is the actual object returned. `exports` is a shortcut:

js

CopyEdit

`exports.hello = () => {} // Equivalent to: module.exports.hello = () => {}`

---

### 84. **How does Node.js handle file uploads?**

Via packages like `multer` that parse `multipart/form-data`.

---

### 85. **What is rate limiting?**

Restricting number of requests from a client in a time window to prevent abuse. Use `express-rate-limit`.

---

### 86. **What is throttling vs debouncing in Node.js context?**

- **Throttling**: Limits how often a function is executed.
    
- **Debouncing**: Ensures a function is executed only after a certain delay.
    

---

### 87. **How to prevent callback hell?**

- Use Promises
    
- Use async/await
    
- Modularize code
    

---

### 88. **What is the event queue?**

Queue where async callbacks wait until the call stack is empty and event loop picks them.

---

### 89. **What is libuv?**

A C library that provides Node.js with an event loop and asynchronous I/O.

---

### 90. **What is backpressure in streams?**

When the writable stream cannot consume data as fast as it is being read, causing memory overflow if not managed.

---
---

## 🔐 SECTION 5: Security, Authentication, Deployment & Best Practices (Q91–115)

---

### 91. **What is JWT (JSON Web Token)?**

JWT is a compact, URL-safe way to represent claims between two parties. It is widely used for authentication.

Structure:

css

CopyEdit

`header.payload.signature`

js

CopyEdit

`const jwt = require('jsonwebtoken'); const token = jwt.sign({ userId: 123 }, 'secretKey', { expiresIn: '1h' });`

---

### 92. **How to verify a JWT?**

js

CopyEdit

`jwt.verify(token, 'secretKey', (err, decoded) => {   if (err) return res.sendStatus(403);   console.log(decoded); });`

---

### 93. **Where should JWT be stored on the client?**

- Preferably in **HTTP-only cookies** (for security)
    
- Avoid storing in `localStorage` (vulnerable to XSS)
    

---

### 94. **What is the difference between Authentication and Authorization?**

|Term|Description|
|---|---|
|Authentication|Verifying identity (e.g., login)|
|Authorization|Checking permissions (e.g., access to route)|

---

### 95. **What is Helmet and why use it?**

Helmet is a middleware that sets secure HTTP headers to protect against common vulnerabilities like XSS, clickjacking, etc.

js

CopyEdit

`const helmet = require('helmet'); app.use(helmet());`

---

### 96. **What are some common security threats in Node.js?**

- XSS (Cross-Site Scripting)
    
- CSRF (Cross-Site Request Forgery)
    
- Injection attacks (e.g., MongoDB/SQL)
    
- DDoS (Denial of Service)
    
- Directory traversal
    
- Insecure cookies
    

---

### 97. **How do you prevent NoSQL injection?**

- Validate and sanitize inputs
    
- Use ORM/ODM safely (like Mongoose)
    
- Never use raw inputs directly in queries
    

---

### 98. **How do you secure API routes in Express?**

- Add **JWT authentication**
    
- Rate-limit requests
    
- Use HTTPS
    
- Validate inputs
    
- Sanitize outputs
    

---

### 99. **How to hash passwords in Node.js?**

Use `bcrypt`:

js

CopyEdit

`const bcrypt = require('bcrypt'); const hashed = await bcrypt.hash('password123', 10); const valid = await bcrypt.compare('password123', hashed);`

---

### 100. **What is rate limiting and how to implement it?**

Prevents brute-force and abuse by limiting requests per IP.

js

CopyEdit

`const rateLimit = require('express-rate-limit'); app.use(rateLimit({ windowMs: 15 * 60 * 1000, max: 100 }));`

---

### 101. **What is the best practice for environment configs in Node.js?**

- Use `.env` for storing secrets
    
- Load with `dotenv`
    
- Do not commit `.env` to version control
    

---

### 102. **What are some logging tools in Node.js?**

- `console.log` (basic)
    
- `winston` (advanced, log levels, file output)
    
- `morgan` (HTTP request logger middleware)
    

---

### 103. **How to deploy a Node.js app?**

- **Local**: Run via `node` or `pm2`
    
- **Cloud**:
    
    - Heroku
        
    - Vercel (for serverless)
        
    - AWS EC2, Lambda
        
    - DigitalOcean
        
- Use CI/CD for automated deployment
    

---

### 104. **How to use PM2 in production?**

bash

CopyEdit

`npm install -g pm2 pm2 start app.js pm2 restart app pm2 logs`

PM2 ensures your app runs in the background and restarts on failure or reboot.

---

### 105. **How to enable HTTPS in Node.js?**

js

CopyEdit

`const https = require('https'); const fs = require('fs'); const options = {   key: fs.readFileSync('key.pem'),   cert: fs.readFileSync('cert.pem'), };  https.createServer(options, app).listen(443);`

---

### 106. **What is CORS and how to enable it?**

Cross-Origin Resource Sharing (CORS) allows servers to specify who can access its resources.

js

CopyEdit

`const cors = require('cors'); app.use(cors());`

---

### 107. **How to handle file uploads securely?**

Use `multer`, restrict file types and sizes:

js

CopyEdit

`const multer = require('multer'); const upload = multer({ dest: 'uploads/', limits: { fileSize: 1e6 } });`

---

### 108. **How to scale a Node.js app?**

- Use clustering (`cluster` module)
    
- Use a load balancer (e.g., NGINX)
    
- Containerization with Docker
    
- Auto-scaling on cloud providers
    

---

### 109. **What is the purpose of `.gitignore` in a Node.js project?**

Prevents unwanted files (like `node_modules`, `.env`) from being pushed to Git.

---

### 110. **How to structure a scalable Node.js project?**

Common structure:

bash

CopyEdit

`/controllers /routes /models /services /middleware /utils`

---

### 111. **What is MVC in Node.js context?**

MVC = Model (data) + View (UI) + Controller (logic)

In Node.js (especially Express):

- **Model**: Database layer (e.g., Mongoose)
    
- **View**: Templating engine (optional)
    
- **Controller**: Logic for routes
    

---

### 112. **What are middleware best practices?**

- Keep them modular
    
- Use `next()` wisely
    
- Avoid blocking code
    
- Use try-catch in async middlewares
    
- Centralize error handling
    

---

### 113. **What is API versioning and how is it handled?**

Helps manage breaking changes across app versions:

js

CopyEdit

`app.use('/api/v1/users', userRoutesV1); app.use('/api/v2/users', userRoutesV2);`

---

### 114. **What are some best practices for REST API design?**

- Use nouns for endpoints (`/users`)
    
- Use HTTP methods properly
    
- Return appropriate status codes
    
- Use pagination, filtering, and sorting
    
- Secure with authentication

---
---
