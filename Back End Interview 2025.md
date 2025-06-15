
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

---
---

## ✅ **ADVANCED LEVEL (Q51 – Q100)**

### 51. **What is a circuit breaker pattern?**

**Answer:**  
It prevents an application from repeatedly trying to execute an operation that is likely to fail, by "breaking" the circuit after failures and retrying after a timeout.

---

### 52. **How do you implement caching in a backend?**

**Answer:**  
Use in-memory stores like Redis or Memcached to cache frequent DB queries or API responses, reducing latency and load.

---

### 53. **What is the difference between REST and SOAP?**

**Answer:**  
REST is lightweight, uses HTTP, and supports multiple formats (JSON, XML). SOAP is protocol-based, uses XML, with built-in standards for security and transactions.

---

### 54. **What is the difference between stateless and stateful applications?**

**Answer:**

- **Stateless:** No client session data stored on server (e.g., REST APIs).
    
- **Stateful:** Server keeps session info (e.g., WebSocket connections).
    

---

### 55. **How do you secure REST APIs?**

**Answer:**  
Use HTTPS, authentication tokens (JWT, OAuth), validate and sanitize input, rate limiting, and use API gateways.

---

### 56. **What is OAuth? How is it different from OpenID Connect?**

**Answer:**  
OAuth is an authorization framework to grant limited access. OpenID Connect builds on OAuth for user authentication and identity.

---

### 57. **What is a deadlock? How can you prevent it?**

**Answer:**  
Deadlock is a situation where two or more processes wait indefinitely for each other’s resources. Prevent by using resource ordering, timeouts, or deadlock detection algorithms.

---

### 58. **Explain eventual consistency vs strong consistency.**

**Answer:**

- **Strong consistency:** All nodes see the same data instantly.
    
- **Eventual consistency:** Data updates propagate asynchronously; nodes converge over time.
    

---

### 59. **What is CAP theorem?**

**Answer:**  
It states that a distributed system can guarantee only two of these three at the same time: Consistency, Availability, and Partition tolerance.

---

### 60. **Explain the concept of idempotency in APIs.**

**Answer:**  
An operation is idempotent if repeating it produces the same effect as a single request. Example: PUT and DELETE are idempotent; POST is not.

---

### 61. **What is a saga pattern?**

**Answer:**  
Saga manages distributed transactions by breaking them into smaller transactions with compensating actions for failure rollback.

---

### 62. **How would you implement rate limiting in a distributed system?**

**Answer:**  
Use centralized stores like Redis or API gateways to maintain counters and apply limits across instances.

---

### 63. **What is a service registry?**

**Answer:**  
A service registry keeps track of microservices instances and locations to enable service discovery (e.g., Eureka, Consul).

---

### 64. **What is a circuit breaker?**

**Answer:**  
(Repeated for reinforcement) It detects failures and prevents a system from trying operations that are likely to fail, improving stability.

---

### 65. **Explain Docker and its benefits for backend development.**

**Answer:**  
Docker containers package applications and dependencies in isolated environments for consistent deployment, easy scaling, and portability.

---

### 66. **What is Kubernetes?**

**Answer:**  
An orchestration platform to automate deployment, scaling, and management of containerized applications.

---

### 67. **What is horizontal pod autoscaling?**

**Answer:**  
In Kubernetes, it automatically scales the number of pods based on CPU/memory usage or custom metrics.

---

### 68. **Explain how JWT tokens are validated.**

**Answer:**  
The server verifies the token’s signature using a secret key/public key, checks expiration and claims before granting access.

---

### 69. **What is a schema migration? Why is it important?**

**Answer:**  
Schema migration updates the database schema safely, tracking versions to apply or rollback changes without data loss.

---

### 70. **What is the difference between synchronous and asynchronous messaging?**

**Answer:**

- **Synchronous:** Sender waits for response immediately.
    
- **Asynchronous:** Sender sends message and continues, response received later.
    

---

### 71. **What is eventual consistency in distributed caches?**

**Answer:**  
Cached data may not immediately reflect DB updates but will sync over time, optimizing performance.

---

### 72. **Explain ACID properties in databases.**

**Answer:**

- **Atomicity:** All or nothing.
    
- **Consistency:** Valid state transitions.
    
- **Isolation:** Concurrent transactions don’t interfere.
    
- **Durability:** Once committed, data persists.
    

---

### 73. **What is a CDN and why use it?**

**Answer:**  
Content Delivery Network caches static content geographically close to users for faster delivery and reduced server load.

---

### 74. **How do you handle API versioning?**

**Answer:**  
Use URL versioning (`/v1/users`), header versioning, or query parameters to manage breaking API changes.

---

### 75. **What is Cross-Site Request Forgery (CSRF)? How do you prevent it?**

**Answer:**  
CSRF tricks users into submitting unauthorized requests. Prevent with anti-CSRF tokens, same-site cookies, and checking origin headers.

---

### 76. **What is a token blacklist?**

**Answer:**  
A list of JWT tokens that are revoked or invalid before expiration, to prevent unauthorized use.

---

### 77. **What is the difference between a process and a thread?**

**Answer:**  
A process is an independent execution unit with its own memory space. Threads run within processes sharing memory.

---

### 78. **How do you handle CORS errors in development?**

**Answer:**  
Configure CORS headers on the server or use proxy setups in dev environments.

---

### 79. **What are the advantages of using NoSQL databases?**

**Answer:**  
Schema flexibility, horizontal scaling, fast writes, and handling large volumes of unstructured data.

---

### 80. **Explain eventual consistency and conflict resolution in distributed DBs.**

**Answer:**  
Conflicts arise from concurrent updates; resolved using vector clocks, last-write wins, or application-specific logic.

---

### 81. **What is a health check endpoint?**

**Answer:**  
A lightweight API endpoint (e.g., `/health`) to check service availability, used by load balancers or orchestrators.

---

### 82. **What is the difference between a monolithic app and microservices?**

**Answer:**  
(Repeat) Monolithic is a single deployable unit, microservices are loosely coupled services managed independently.

---

### 83. **What is the principle of least privilege?**

**Answer:**  
Users/applications should have only the minimum access necessary to perform their tasks, improving security.

---

### 84. **How do you implement background jobs in Node.js?**

**Answer:**  
Use job queues like Bull or Agenda with Redis for delayed, retried, or scheduled tasks.

---

### 85. **What is the difference between blocking and non-blocking code?**

**Answer:**  
Blocking code waits until operation finishes; non-blocking code allows other tasks to run concurrently.

---

### 86. **What is a webhook? How is it different from polling?**

**Answer:**  
Webhook pushes event notifications to clients instantly, polling regularly checks for updates.

---

### 87. **What is the role of an API Gateway?**

**Answer:**  
Manages API requests, enforces security, rate limits, routing, caching, and aggregates services.

---

### 88. **Explain distributed tracing.**

**Answer:**  
Tracks a request as it flows through multiple microservices to diagnose performance bottlenecks and errors.

---

### 89. **How do you monitor backend applications?**

**Answer:**  
Use tools like Prometheus, Grafana, ELK stack for logging, metrics, alerting, and performance tracking.

---

### 90. **What are environment variables?**

**Answer:**  
Configurations stored outside code, like API keys and DB credentials, to keep secrets secure and environments flexible.

---

### 91. **Explain JWT refresh tokens and access tokens.**

**Answer:**  
Access tokens are short-lived tokens for resource access. Refresh tokens are long-lived and used to get new access tokens.

---

### 92. **How do you prevent SQL injection?**

**Answer:**  
Use parameterized queries, input validation, ORM, and avoid dynamic SQL string concatenation.

---

### 93. **What are common HTTP methods and their uses?**

**Answer:**  
GET (retrieve), POST (create), PUT (update), PATCH (partial update), DELETE (delete), OPTIONS (communication options).

---

### 94. **Explain the difference between PUT and PATCH.**

**Answer:**  
PUT replaces the entire resource; PATCH updates parts of a resource.

---

### 95. **What is the difference between clustered and non-clustered indexes?**

**Answer:**  
Clustered index determines the physical order of data; non-clustered index is a separate structure pointing to data.

---

### 96. **What is the difference between a cold start and warm start in serverless?**

**Answer:**  
Cold start happens when a serverless function initializes after inactivity, causing latency. Warm start is a reused instance with faster response.

---

### 97. **How do you implement logging best practices?**

**Answer:**  
Structured logs, log levels (info, warn, error), correlation IDs, centralized logging, and log rotation.

---

### 98. **What is idempotency key?**

**Answer:**  
A unique key clients send to ensure repeated requests don’t cause duplicated operations (especially for POST requests).

---

### 99. **What is a rate limiter? How does it protect APIs?**

**Answer:**  
It limits the number of requests per client in a time window to prevent abuse and DoS attacks.

---

### 100. **How do you design a scalable backend system?**

**Answer:**  
Use microservices, load balancing, caching, asynchronous processing, database sharding, CDNs, and proper monitoring.

---
---

