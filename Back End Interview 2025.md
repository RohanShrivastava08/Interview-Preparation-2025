
## ✅ **BEGINNER LEVEL (0–1 YOE)**

### 1. **What is a REST API?**

**Answer:**  
A REST (Representational State Transfer) API is an architectural style for building web services that use HTTP methods like GET, POST, PUT, DELETE. It's stateless, uses URIs to access resources, and typically returns data in JSON or XML.

---

### 2. **What is the difference between PUT and POST?**

**Answer:**

- **POST** creates a new resource.
    
- **PUT** updates an existing resource or creates it if it doesn’t exist (idempotent).
    

---

### 3. **What is the purpose of middleware in Express.js?**

**Answer:**  
Middleware functions are functions that have access to `req`, `res`, and `next`. They’re used for logging, authentication, error handling, etc. They execute in order before the request reaches the final route handler.

---

### 4. **What is CORS? Why is it important?**

**Answer:**  
CORS (Cross-Origin Resource Sharing) is a security feature implemented by browsers that restricts cross-origin HTTP requests. It prevents malicious sites from accessing APIs on other domains without permission.

---

### 5. **Explain the MVC architecture.**

**Answer:**  
MVC stands for Model-View-Controller:

- **Model:** Data logic (e.g., DB schema).
    
- **View:** UI layer (frontend or template).
    
- **Controller:** Business logic and request/response handling.
    

---

### 6. **What is the difference between SQL and NoSQL databases?**

**Answer:**

- **SQL (e.g., MySQL, PostgreSQL):** Structured schema, relational data, joins.
    
- **NoSQL (e.g., MongoDB):** Schema-less, document/graph-based, flexible.
    

---

### 7. **What are status codes like 200, 400, 401, 403, 404, 500?**

**Answer:**

- **200:** OK
    
- **400:** Bad Request
    
- **401:** Unauthorized
    
- **403:** Forbidden
    
- **404:** Not Found
    
- **500:** Internal Server Error
    

---

### 8. **What is JWT? How does it work?**

**Answer:**  
JWT (JSON Web Token) is used for authentication. A token is signed and sent to the client. The client sends it with every request. The server verifies the token to allow access.

---
---

## ✅ **INTERMEDIATE LEVEL (1–3 YOE)**

### 9. **Explain the event loop in Node.js.**

**Answer:**  
Node.js is single-threaded but handles async operations using the event loop and callback queue. It enables non-blocking I/O operations, making Node efficient for I/O-heavy tasks.

---

### 10. **What is the difference between synchronous and asynchronous programming?**

**Answer:**

- **Synchronous:** Code runs line by line, blocking the thread.
    
- **Asynchronous:** Allows non-blocking code execution using callbacks, promises, or async/await.
    

---

### 11. **How do you handle error handling in Node.js?**

**Answer:**

- Use `try/catch` with async/await.
    
- Use `.catch()` for Promises.
    
- Implement global error middleware in Express.
    

---

### 12. **What is database indexing and why is it important?**

**Answer:**  
Indexing improves database query performance by allowing faster data retrieval. It’s like a table of contents in a book.

---

### 13. **Explain SQL joins.**

**Answer:**

- **INNER JOIN:** Matches rows in both tables.
    
- **LEFT JOIN:** All rows from left, matched from right.
    
- **RIGHT JOIN:** All rows from right, matched from left.
    
- **FULL OUTER JOIN:** All rows from both tables.
    

---

### 14. **How do you prevent SQL injection?**

**Answer:**

- Use parameterized queries or ORM.
    
- Avoid directly inserting user input into SQL queries.
    

---

### 15. **What is normalization?**

**Answer:**  
It’s the process of structuring a relational database to reduce redundancy and improve data integrity by dividing large tables into smaller related tables.

---

### 16. **What are transactions in databases?**

**Answer:**  
A transaction is a sequence of DB operations that are executed as a single unit. It follows ACID properties:

- **A**tomicity
    
- **C**onsistency
    
- **I**solation
    
- **D**urability

---
---

## ✅ **ADVANCED LEVEL (3+ YOE)**

### 17. **How do you scale a backend application?**

**Answer:**

- **Vertical Scaling:** Increase hardware.
    
- **Horizontal Scaling:** Add more instances.
    
- Use load balancers, caching (Redis), database sharding, microservices, message queues.
    

---

### 18. **What is a message queue? Why use it?**

**Answer:**  
A message queue (like RabbitMQ, Kafka) decouples services and helps in asynchronous communication. Useful for tasks like sending emails, notifications, background processing.

---

### 19. **What is the difference between monolithic and microservices architecture?**

**Answer:**

- **Monolithic:** All code in one deployable unit.
    
- **Microservices:** Split into independent services with clear boundaries and APIs.
    

---

### 20. **What is rate limiting? How do you implement it?**

**Answer:**  
Rate limiting restricts the number of requests a client can make. You can use libraries like `express-rate-limit` or middleware with Redis for distributed rate limiting.

---

### 21. **Explain CAP theorem.**

**Answer:**  
In distributed systems:

- **C**onsistency: All nodes see same data.
    
- **A**vailability: System is always responsive.
    
- **P**artition tolerance: System continues despite network failures.
    

You can choose **only two** at a time.

---

### 22. **How do you ensure security in a backend application?**

**Answer:**

- Use HTTPS
    
- Validate input
    
- Use JWT for auth
    
- Sanitize data
    
- Apply rate limiting
    
- Use Helmet for HTTP headers
    
- Store passwords securely (bcrypt, argon2)
    

---

### 23. **What are design patterns used in backend dev?**

**Answer:**

- Singleton
    
- Factory
    
- Repository
    
- Dependency Injection
    
- Observer
    
- Strategy
    

---

### 24. **How does authentication differ from authorization?**

**Answer:**

- **Authentication:** Verifies user identity.
    
- **Authorization:** Determines access level and permissions.
    

---

### 25. **What is an ORM? Pros and Cons?**

**Answer:**  
An ORM (e.g., Sequelize, TypeORM, Prisma) maps objects to DB rows.

- **Pros:** Faster dev, abstraction, cross-DB support.
    
- **Cons:** Less control, can generate inefficient queries.

---
---

## ✅ **INTERMEDIATE to ADVANCED LEVEL (continued)**

### 26. **What is middleware in Express.js? Give an example.**

**Answer:**  
Middleware is a function that has access to `req`, `res`, and `next` objects in the request-response cycle. It can execute code, modify req/res, end the req-res cycle, or call next middleware.

Example:

js

CopyEdit

`app.use((req, res, next) => {   console.log('Request URL:', req.url);   next(); });`

---

### 27. **How does Node.js handle child processes?**

**Answer:**  
Node.js can spawn child processes using the `child_process` module. It allows running external processes asynchronously, useful for CPU-intensive tasks or running shell commands.

---

### 28. **What are Promises and async/await in Node.js?**

**Answer:**  
Promises represent future completion or failure of async operations. `async/await` is syntactic sugar over Promises for writing asynchronous code in a more synchronous style.

---

### 29. **Explain connection pooling. Why is it used?**

**Answer:**  
Connection pooling reuses database connections to avoid overhead of opening/closing connections for each request, improving performance and scalability.

---

### 30. **What is the difference between synchronous and asynchronous I/O?**

**Answer:**  
Synchronous I/O blocks the execution until the operation completes. Asynchronous I/O allows other tasks to run before completion, improving throughput and responsiveness.

---

### 31. **What is the use of environment variables in backend applications?**

**Answer:**  
Environment variables store configuration such as DB credentials, API keys, and secrets outside code for security and flexibility across environments (development, production).

---

### 32. **How do you secure sensitive data like passwords?**

**Answer:**  
Passwords are hashed with algorithms like bcrypt or argon2, often salted, so stored passwords are not plain text and can't be reversed.

---

### 33. **What is a reverse proxy? Name an example.**

**Answer:**  
A reverse proxy sits between clients and servers, forwarding requests and providing security, load balancing, and caching. Example: NGINX.

---

### 34. **How do you implement pagination in APIs?**

**Answer:**  
Pagination splits data into chunks. Common methods:

- Offset-based (e.g., `?page=2&limit=10`)
    
- Cursor-based (using a unique id or timestamp for better performance on large datasets)
    

---

### 35. **What is database sharding?**

**Answer:**  
Sharding splits a large database into smaller, faster, more manageable parts called shards, each holding a subset of the data.

---

### 36. **What are webhooks?**

**Answer:**  
Webhooks are user-defined HTTP callbacks triggered by events. They allow communication between applications in real-time.

---

### 37. **Explain how to implement file upload in a Node.js backend.**

**Answer:**  
Use middleware like `multer` to handle multipart/form-data. Files can be stored locally or uploaded to cloud storage (AWS S3, Google Cloud).

---

### 38. **How do you debug Node.js applications?**

**Answer:**  
Use `console.log`, Node.js debugger (`node inspect`), Chrome DevTools, or VSCode debugger extensions.

---

### 39. **What is eventual consistency?**

**Answer:**  
In distributed systems, eventual consistency means updates will propagate to all nodes eventually, but immediate consistency isn't guaranteed.

---

### 40. **What is an API gateway?**

**Answer:**  
An API gateway manages, routes, and secures API calls between clients and backend services. It can provide rate limiting, caching, and authentication.

---

### 41. **How would you implement logging in a backend system?**

**Answer:**  
Use logging libraries like `winston` or `bunyan` to capture info, warning, error logs. Logs can be stored in files or sent to monitoring tools (ELK stack).

---

### 42. **What is dependency injection?**

**Answer:**  
A design pattern where an object receives its dependencies from an external source rather than creating them itself, improving testability and modularity.

---

### 43. **What are GraphQL advantages over REST?**

**Answer:**  
GraphQL allows clients to request only needed data, supports complex queries in a single request, and has a strongly typed schema.

---

### 44. **What is the difference between horizontal and vertical scaling?**

**Answer:**

- **Vertical scaling:** Adding more resources (CPU, RAM) to a single server.
    
- **Horizontal scaling:** Adding more machines to distribute load.
    

---

### 45. **What is rate limiting and throttling? How are they different?**

**Answer:**

- **Rate limiting:** Restricts number of requests in a fixed window.
    
- **Throttling:** Limits request rate dynamically to prevent overload.
    

---

### 46. **Explain JWT structure.**

**Answer:**  
JWT consists of three parts:

- Header (algorithm, type)
    
- Payload (claims/data)
    
- Signature (verifies token integrity)
    

---

### 47. **How do you prevent Cross-Site Scripting (XSS)?**

**Answer:**  
Sanitize user inputs, use HTTP headers like Content Security Policy (CSP), and escape output in views.

---

### 48. **Explain the concept of middleware chaining in Express.**

**Answer:**  
Middleware functions are executed in sequence, calling `next()` to pass control to the next middleware until the response is sent.

---

### 49. **What are microservices and how do they communicate?**

**Answer:**  
Microservices are small, independent services. They communicate via REST, gRPC, or messaging queues.

---

### 50. **How do you handle database migrations in production?**

**Answer:**  
Use migration tools (e.g., Sequelize migrations, Flyway) to apply schema changes in a controlled, versioned manner ensuring backward compatibility.