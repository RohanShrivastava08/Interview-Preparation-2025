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