
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
