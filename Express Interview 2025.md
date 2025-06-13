## 🔹 Section 1: Basics of Express.js (1–15)

**1. What is Express.js?**  
Express.js is a minimal and flexible Node.js web application framework that provides robust features to build web and mobile applications. It simplifies server creation and route handling.

**2. How do you install Express.js in a Node.js project?**

bash

CopyEdit

`npm install express`

**3. What are the key features of Express.js?**

- Middleware support
    
- Routing
    
- Template engines support
    
- HTTP utility methods
    
- Error handling
    

**4. How do you create a simple Express server?**

js

CopyEdit

`const express = require('express'); const app = express();  app.get('/', (req, res) => res.send('Hello World!'));  app.listen(3000, () => console.log('Server running on port 3000'));`

**5. What is middleware in Express.js?**  
Middleware functions have access to `req`, `res`, and `next()`. They modify the request/response or end the request cycle.

**6. Explain the `next()` function in middleware.**  
`next()` passes control to the next middleware function in the stack.

**7. What is the difference between `app.use()` and `app.get()`?**

- `app.use()` applies middleware functions for all routes.
    
- `app.get()` defines a handler for HTTP GET requests to a specific route.
    

**8. What is `req.params` vs `req.query` vs `req.body`?**

- `req.params`: Route parameters (`/user/:id`)
    
- `req.query`: URL query string (`/user?id=1`)
    
- `req.body`: Data sent via POST/PUT (requires body-parser)
    

**9. What is the default HTTP method supported by Express routes?**  
All standard methods like GET, POST, PUT, DELETE, PATCH, etc.

**10. How do you serve static files in Express.js?**

js

CopyEdit

`app.use(express.static('public'));`

**11. What are route handlers and routers?**

- Route handlers: Define what to do on a specific route.
    
- Routers: Allow modular route definitions.
    

**12. What is the order of middleware execution?**  
It’s based on the order you define them in your code.

**13. How can you handle 404 errors in Express?**

js

CopyEdit

`app.use((req, res) => {   res.status(404).send('Page Not Found'); });`

**14. How do you export and import routers?**

js

CopyEdit

`// userRoutes.js const router = require('express').Router(); router.get('/', ...); module.exports = router;`

**15. What is the role of `express.json()` and `express.urlencoded()`?**  
They parse incoming JSON and URL-encoded payloads.

---
---

## 🔹 Section 2: Routing (16–30)

**16. What is Express routing?**  
Routing defines how an application responds to client requests to specific endpoints.

**17. How do you define route parameters?**

js

CopyEdit

``app.get('/user/:id', (req, res) => {   res.send(`User ID: ${req.params.id}`); });``

**18. What is the use of `Router()` in Express?**  
Modularizes routes into separate files for better scalability.

**19. Can you chain multiple route handlers?**  
Yes:

js

CopyEdit

`app.get('/route', middleware1, middleware2, handler);`

**20. What is route grouping in Express?**  
Using `express.Router()` to group routes under a common prefix.

**21. How do you implement route-level middleware?**  
Attach it to a specific route:

js

CopyEdit

`router.get('/user', authMiddleware, controller);`

**22. What is the difference between `app.route()` and `router.route()`?**  
Both allow chaining route handlers for the same path. `router.route()` is used in modular routers.

**23. What are wildcards in routing?**  
`*` can match any path, like `app.get('*', handler)`.

**24. How do you redirect in Express.js?**

js

CopyEdit

`res.redirect('/new-path');`

**25. How do you handle optional route parameters?**

js

CopyEdit

`app.get('/user/:id?', handler);`

**26. Can routes be case-sensitive in Express?**  
Yes, with `case sensitive routing` setting:

js

CopyEdit

`app.set('case sensitive routing', true);`

**27. What is the difference between `req.baseUrl` and `req.originalUrl`?**

- `baseUrl`: Mounted route’s path.
    
- `originalUrl`: Full URL requested by the client.
    

**28. How can you handle routes for all HTTP methods?**

js

CopyEdit

`app.all('/example', handler);`

**29. How do you define nested routes using `express.Router()`?**  
By mounting routers within routers.

**30. What is the difference between `req.route` and `req.path`?**

- `req.route`: The matched route info.
    
- `req.path`: The request path string.

---
---

## 🔹 Section 3: Middleware & Error Handling (31–45)

**31. What are different types of middleware in Express?**

- Application-level
    
- Router-level
    
- Error-handling
    
- Built-in
    
- Third-party
    

**32. How do you define an error-handling middleware?**

js

CopyEdit

`app.use((err, req, res, next) => {   res.status(500).send(err.message); });`

**33. What is third-party middleware?**  
Middleware not built into Express, e.g., `cors`, `helmet`, `morgan`.

**34. How do you use `cors` in Express?**

js

CopyEdit

`const cors = require('cors'); app.use(cors());`

**35. How does Express handle async errors?**  
You must catch them in `try/catch` or use a package like `express-async-handler`.

**36. Can you skip middleware?**  
Yes, by not calling `next()` or conditionally branching logic.

**37. How do you log HTTP requests?**  
Using middleware like `morgan`.

**38. What is the difference between global and route-level middleware?**

- Global: Runs for all requests.
    
- Route-level: Only for specific paths.
    

**39. What is `helmet` middleware?**  
Helps secure Express apps by setting HTTP headers.

**40. How do you handle invalid JSON errors in requests?**  
Use error-handling middleware to catch JSON parsing errors.

**41. What is the significance of `next(err)`?**  
It passes errors to the next error-handling middleware.

**42. How to set headers using middleware?**

js

CopyEdit

`res.setHeader('X-Custom-Header', 'value');`

**43. What is `res.locals` used for?**  
To pass data to views or later middleware in the request-response cycle.

**44. What are some common use cases for middleware?**

- Authentication
    
- Logging
    
- Parsing
    
- CORS
    
- Input validation
    

**45. Can middleware be async?**  
Yes, use `async/await` with proper error handling.

---
---

## 🔹 Section 4: Request & Response (46–60)

**46. How to get headers from a request?**

js

CopyEdit

`req.headers['header-name']`

**47. How do you set response status code?**

js

CopyEdit

`res.status(201).send('Created');`

**48. How to send JSON response?**

js

CopyEdit

`res.json({ msg: 'Success' });`

**49. What’s the difference between `res.send()`, `res.json()`, and `res.end()`?**

- `res.send()`: Sends string/buffer/object.
    
- `res.json()`: Sends JSON with correct content-type.
    
- `res.end()`: Ends the response without data.
    

**50. How to append cookies to the response?**  
Using `res.cookie('name', 'value')` (requires `cookie-parser`).

**51. How to read POST data?**  
Use `express.json()` or `express.urlencoded()` middleware.

**52. How to send file as response?**

js

CopyEdit

`res.sendFile(path.join(__dirname, 'file.txt'));`

**53. How to handle file uploads?**  
Use middleware like `multer`.

**54. How to handle redirect responses?**

js

CopyEdit

`res.redirect('/new-url');`

**55. How to get IP address of client?**

js

CopyEdit

`req.ip`

**56. What does `res.set()` do?**  
Sets HTTP response headers.

**57. How do you handle different content types in Express?**  
Use middleware and check `req.headers['content-type']`.

**58. How to implement rate-limiting?**  
Use middleware like `express-rate-limit`.

**59. What is the use of `res.format()`?**  
It responds with different formats based on `Accept` headers.

**60. How do you prevent caching?**

`res.set('Cache-Control', 'no-store');`

---
---

## 🔹 Section 5: Security and Authentication (61–75)

**61. How do you secure Express apps against common web vulnerabilities?**  
Use packages like:

- `helmet` – secure HTTP headers
    
- `cors` – handle cross-origin requests
    
- `express-rate-limit` – prevent brute-force attacks
    
- Input validation – prevent injection attacks
    

**62. What is CORS and how do you handle it in Express?**  
CORS (Cross-Origin Resource Sharing) allows or restricts requested resources on a web server.

js

CopyEdit

`const cors = require('cors'); app.use(cors());`

**63. How do you implement JWT authentication in Express?**  
Use `jsonwebtoken`:

js

CopyEdit

`const jwt = require('jsonwebtoken');  app.post('/login', (req, res) => {   const token = jwt.sign({ id: user.id }, 'secret', { expiresIn: '1h' });   res.json({ token }); });  app.get('/protected', verifyToken, (req, res) => {   res.send('Protected Route'); });`

**64. How do you create a middleware to verify JWT?**

js

CopyEdit

`const verifyToken = (req, res, next) => {   const token = req.headers['authorization'];   if (!token) return res.sendStatus(403);   jwt.verify(token, 'secret', (err, decoded) => {     if (err) return res.sendStatus(401);     req.user = decoded;     next();   }); };`

**65. What are CSRF attacks and how to prevent them?**  
CSRF (Cross-Site Request Forgery) tricks users into making unintended requests. Prevent it using:

js

CopyEdit

`const csrf = require('csurf'); app.use(csrf({ cookie: true }));`

**66. What are HTTP headers you can set to increase security?**

- `X-Frame-Options`
    
- `Content-Security-Policy`
    
- `X-XSS-Protection`
    
- `Strict-Transport-Security`
    
- Set via `helmet`
    

**67. How do you hash passwords before storing?**  
Use `bcrypt`:

js

CopyEdit

`const bcrypt = require('bcrypt'); const hashed = await bcrypt.hash(password, 10);`

**68. How do you protect routes with authentication middleware?**  
Wrap routes:

js

CopyEdit

`app.get('/dashboard', isAuthenticated, controllerFn);`

**69. How do you invalidate JWT tokens (logout)?**  
JWTs are stateless, so logout is handled on the client. Alternatively, store blacklisted tokens server-side.

**70. What is session-based authentication in Express?**  
Use `express-session` to store sessions server-side or in-memory:

js

CopyEdit

`app.use(session({ secret: 'secret', resave: false, saveUninitialized: true }));`

**71. What are cookies, and how do you manage them in Express?**  
Cookies store client data. Use `cookie-parser`:

js

CopyEdit

`const cookieParser = require('cookie-parser'); app.use(cookieParser());`

**72. What is the difference between cookies and sessions?**

- Cookies: stored on client, less secure
    
- Sessions: server-side storage, more secure
    

**73. How do you restrict CORS to specific domains?**

js

CopyEdit

`app.use(cors({ origin: ['https://mydomain.com'] }));`

**74. How to validate incoming request data in Express?**  
Use `express-validator` or `Joi`.

**75. Why is it risky to trust client-side authentication alone?**  
Client-side auth can be manipulated. Always validate tokens/server-sessions on backend.

---
---
## 🔹 Section 6: Performance & Optimization (76–85)

**76. How can you optimize performance in Express apps?**

- Use compression
    
- Limit middleware
    
- Cache responses
    
- Optimize database queries
    
- Use load balancers
    

**77. How to enable GZIP compression in Express?**

js

CopyEdit

`const compression = require('compression'); app.use(compression());`

**78. What is request throttling and how is it implemented?**  
Prevent spamming with `express-rate-limit`:

js

CopyEdit

`const rateLimit = require('express-rate-limit'); app.use(rateLimit({ windowMs: 1 * 60 * 1000, max: 100 }));`

**79. How to implement response caching?**  
Use `apicache` or Redis to cache frequent responses.

**80. What are best practices to structure a large Express app?**

- Modular routing
    
- Use controllers/services
    
- Layered architecture (routes → controllers → services → models)
    

**81. How do you profile performance bottlenecks in Express apps?**

- Use Node's built-in profiler
    
- Tools like `clinic.js`, `PM2`, or `New Relic`
    

**82. What is clustering in Node.js and how can it help Express?**  
Clusters use multiple CPU cores:

js

CopyEdit

`const cluster = require('cluster');`

**83. How to prevent memory leaks in Express apps?**

- Avoid global variables
    
- Properly close DB connections
    
- Monitor memory usage
    

**84. When should you use async handlers in Express?**  
When performing I/O operations like DB calls, file reads, API calls.

**85. What are the benefits of using a reverse proxy like Nginx with Express?**

- SSL termination
    
- Load balancing
    
- Better static file handling
    
- Security headers

---
---
## 🔹 Section 7: Advanced Topics (86–95)

**86. How do you create a custom middleware in Express?**

js

CopyEdit

``function logger(req, res, next) {   console.log(`${req.method} ${req.url}`);   next(); } app.use(logger);``

**87. How do you mount multiple apps in Express?**

js

CopyEdit

`const subApp = express(); app.use('/sub', subApp);`

**88. What is the use of `app.locals` and `res.locals`?**

- `app.locals`: app-wide variables
    
- `res.locals`: request-scoped variables
    

**89. What is the purpose of `app.set()` and `app.get()`?**  
Configure and retrieve app settings like views, environment, etc.

**90. What is `app.disable()` used for?**  
To turn off Express settings like `x-powered-by`.

**91. How to handle async errors globally in Express?**  
Wrap routes in `try/catch` or use packages like `express-async-errors`.

**92. What is the difference between Express and Koa?**

- Express: middleware chaining via callbacks
    
- Koa: uses async/await, more modular
    

**93. How to generate an Express project boilerplate quickly?**  
Use `express-generator`:

bash

CopyEdit

`npx express-generator`

**94. What is `trust proxy` in Express?**  
Tells Express to trust proxy headers (`X-Forwarded-*`) for IP, protocol.

**95. Can Express be used in serverless environments (e.g., AWS Lambda)?**  
Yes, using `serverless-http` adapter.

---
---
## 🔹 Section 8: Testing & Deployment (96–100)

**96. How do you test Express APIs?**  
Use:

- `supertest`
    
- `jest` or `mocha`
    

js

CopyEdit

`const request = require('supertest'); request(app).get('/api').expect(200);`

**97. How to write unit tests for Express routes?**  
Mock services and test handlers independently using test frameworks like Jest.

**98. How to deploy an Express app to production?**

- Use services like Render, Railway, Vercel, or AWS
    
- Serve via Nginx + PM2 or Docker
    

**99. How to handle environment variables in Express?**  
Use `dotenv`:

js

CopyEdit

`require('dotenv').config(); console.log(process.env.PORT);`

**100. What are common deployment issues with Express apps?**

- CORS issues
    
- Port binding
    
- Incorrect environment variables
    
- Improper async error handling
    
- Uncaught exceptions
---
---
