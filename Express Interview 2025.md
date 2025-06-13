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

