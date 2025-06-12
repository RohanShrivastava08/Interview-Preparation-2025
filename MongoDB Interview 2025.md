## 🔰 Basic Level (1–30)

### 1. **What is MongoDB?**

MongoDB is a NoSQL, open-source, document-oriented database that stores data in flexible, JSON-like BSON format. It allows horizontal scaling and high performance.

---

### 2. **What are the key features of MongoDB?**

- Document-oriented (BSON)
    
- Schema-less
    
- High availability with replication
    
- Horizontal scaling with sharding
    
- Powerful querying with aggregation
    
- Indexing support
    

---

### 3. **How is MongoDB different from RDBMS?**

|Feature|RDBMS|MongoDB|
|---|---|---|
|Structure|Tables, Rows|Collections, Documents|
|Schema|Fixed|Dynamic|
|Joins|Supported|Limited (via $lookup)|
|Scalability|Vertical|Horizontal (Sharding)|

---

### 4. **What is a document in MongoDB?**

A document is a JSON-like structure (BSON) that stores data as key-value pairs. Example:

json

CopyEdit

`{   "_id": 1,   "name": "Rohan",   "age": 25 }`

---

### 5. **What is a collection in MongoDB?**

A collection is a group of MongoDB documents, similar to a table in RDBMS. It is schema-less.

---

### 6. **What is BSON?**

Binary JSON — a binary-encoded format of JSON used by MongoDB to store data efficiently.

---

### 7. **What is the default port of MongoDB?**

`27017`

---

### 8. **What are CRUD operations in MongoDB?**

- Create → `insertOne`, `insertMany`
    
- Read → `find`, `findOne`
    
- Update → `updateOne`, `updateMany`
    
- Delete → `deleteOne`, `deleteMany`
    

---

### 9. **How do you insert data into a collection?**

js

CopyEdit

`db.users.insertOne({ name: "Rohan", age: 25 });`

---

### 10. **How do you retrieve all documents from a collection?**

js

CopyEdit

`db.users.find();`

---

### 11. **How do you update a document?**

js

CopyEdit

`db.users.updateOne({ name: "Rohan" }, { $set: { age: 26 } });`

---

### 12. **How do you delete a document?**

js

CopyEdit

`db.users.deleteOne({ name: "Rohan" });`

---

### 13. **What is the `_id` field in MongoDB?**

A unique identifier for each document. MongoDB creates it automatically if not provided.

---

### 14. **Is MongoDB schema-less?**

Yes. Collections don’t require a predefined schema, allowing different documents in a collection to have different fields.

---

### 15. **What is the command to list databases?**

js

CopyEdit

`show dbs;`

---

### 16. **How do you switch to a specific database?**

js

CopyEdit

`use databaseName;`

---

### 17. **How to list collections in a DB?**

js

CopyEdit

`show collections;`

---

### 18. **How do you drop a collection?**

js

CopyEdit

`db.collectionName.drop();`

---

### 19. **How do you drop a database?**

js

CopyEdit

`db.dropDatabase();`

---

### 20. **What is the difference between `find()` and `findOne()`?**

- `find()` returns a cursor (can return many documents)
    
- `findOne()` returns the first matching document
    

---

### 21. **How do you perform a query with a condition?**

js

CopyEdit

`db.users.find({ age: { $gt: 25 } });`

---

### 22. **What are comparison operators in MongoDB?**

- `$eq`, `$ne`, `$gt`, `$gte`, `$lt`, `$lte`, `$in`, `$nin`
    

---

### 23. **What is an index in MongoDB?**

A data structure that improves query performance. Like an index in books.

---

### 24. **How do you create an index?**

js

CopyEdit

`db.users.createIndex({ name: 1 });`

---

### 25. **What is a compound index?**

An index on multiple fields:

js

CopyEdit

`db.users.createIndex({ name: 1, age: -1 });`

---

### 26. **What is the use of `explain()`?**

It shows how MongoDB executes a query, useful for performance tuning.

---

### 27. **What are the data types in MongoDB?**

- String, Number, Boolean, Date, Array, Object, Null, ObjectId, Binary, etc.
    

---

### 28. **What is ObjectId?**

A 12-byte unique identifier for documents:

- 4 bytes timestamp
    
- 5 bytes machine + process ID
    
- 3 bytes incrementing counter
    

---

### 29. **Can you join documents in MongoDB?**

Yes, using `$lookup` in aggregation.

---

### 30. **What is the size limit of a MongoDB document?**

16 MB