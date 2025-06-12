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

---
---


## 🧠 Intermediate Level (31–70)

### 31. **What is aggregation in MongoDB?**

Aggregation processes data records and returns computed results. It’s similar to SQL’s `GROUP BY`.

---

### 32. **What are the main stages of an aggregation pipeline?**

- `$match`: Filters data
    
- `$group`: Groups data
    
- `$sort`: Sorts data
    
- `$project`: Reshapes documents
    
- `$limit`: Limits output
    
- `$skip`: Skips documents
    
- `$lookup`: Joins collections
    

---

### 33. **Example of an aggregation pipeline:**

js

CopyEdit

`db.orders.aggregate([   { $match: { status: "delivered" } },   { $group: { _id: "$customerId", total: { $sum: "$amount" } } } ]);`

---

### 34. **What is `$project` used for?**

To include, exclude, or rename fields:

js

CopyEdit

`db.users.aggregate([   { $project: { name: 1, email: 1, _id: 0 } } ]);`

---

### 35. **What is `$lookup`?**

Performs a left outer join with another collection:

js

CopyEdit

`{   $lookup: {     from: "orders",     localField: "_id",     foreignField: "userId",     as: "orders"   } }`

---

### 36. **What is a capped collection?**

A fixed-size collection that automatically overwrites its oldest entries when it reaches size limit.

---

### 37. **How to create a capped collection?**

js

CopyEdit

`db.createCollection("logs", { capped: true, size: 100000 });`

---

### 38. **What is sharding in MongoDB?**

Horizontal partitioning of data across multiple machines (shards) for scalability.

---

### 39. **What is a replica set in MongoDB?**

A group of mongod instances that maintain the same data set for high availability and redundancy.

---

### 40. **What are the roles in a replica set?**

- **Primary**: Accepts writes
    
- **Secondary**: Replicates data
    
- **Arbiter**: Votes in elections but holds no data
    

---

### 41. **How does MongoDB ensure high availability?**

Using **replica sets**—if primary fails, a secondary is promoted.

---

### 42. **What is write concern?**

Specifies the level of acknowledgment requested from MongoDB when performing write operations (e.g., 1, majority, etc.).

---

### 43. **What is read concern?**

Determines the level of isolation for read operations. E.g., `local`, `majority`, `linearizable`.

---

### 44. **How do transactions work in MongoDB?**

MongoDB supports multi-document ACID transactions since v4.0 (for replica sets) and v4.2+ (for sharded clusters).

---

### 45. **How to start a transaction?**

js

CopyEdit

`const session = db.getMongo().startSession(); session.startTransaction();`

---

### 46. **What is schema validation?**

You can enforce schema rules using JSON Schema in collection options.

---

### 47. **How to add a validation rule to a collection?**

js

CopyEdit

`db.createCollection("users", {   validator: {     $jsonSchema: {       bsonType: "object",       required: ["name", "email"],       properties: {         email: { bsonType: "string" }       }     }   } });`

---

### 48. **What are the types of indexes?**

- Single field
    
- Compound
    
- Multikey (arrays)
    
- Text
    
- Geospatial
    
- Hashed
    

---

### 49. **What is a text index?**

Used to perform full-text searches on string content.

js

CopyEdit

`db.articles.createIndex({ content: "text" });`

---

### 50. **How to search text in MongoDB?**

js

CopyEdit

`db.articles.find({ $text: { $search: "mongodb" } });`

---

### 51. **What is `$in` operator?**

Matches any value in the given array.

js

CopyEdit

`db.users.find({ age: { $in: [25, 30] } });`

---

### 52. **What is `$set` operator?**

Updates the value of a field.

js

CopyEdit

`db.users.updateOne({ name: "Rohan" }, { $set: { age: 26 } });`

---

### 53. **What is `$unset` operator?**

Removes a field.

js

CopyEdit

`db.users.updateOne({ name: "Rohan" }, { $unset: { age: "" } });`

---

### 54. **What is the difference between `updateOne` and `updateMany`?**

- `updateOne`: Updates first match
    
- `updateMany`: Updates all matches
    

---

### 55. **What is the use of `upsert`?**

If no matching document, insert a new one.

js

CopyEdit

`db.users.updateOne({ name: "Sam" }, { $set: { age: 28 } }, { upsert: true });`

---

### 56. **What is `$push` in MongoDB?**

Appends a value to an array field.

js

CopyEdit

`db.users.updateOne({ name: "Rohan" }, { $push: { hobbies: "reading" } });`

---

### 57. **What is `$addToSet` in MongoDB?**

Adds a value to an array only if it doesn’t exist.

js

CopyEdit

`db.users.updateOne({}, { $addToSet: { tags: "new" } });`

---

### 58. **What is `$pull` in MongoDB?**

Removes matching value from an array.

js

CopyEdit

`db.users.updateOne({}, { $pull: { hobbies: "gaming" } });`

---

### 59. **What is `$inc` in MongoDB?**

Increments a numeric field by a given value.

js

CopyEdit

`db.users.updateOne({}, { $inc: { age: 1 } });`

---

### 60. **How to sort results?**

js

CopyEdit

`db.users.find().sort({ age: -1 });`

---

### 61. **How to paginate results?**

js

CopyEdit

`db.users.find().skip(10).limit(5);`

---

### 62. **What is the Aggregation Framework used for?**

Used for complex data processing: grouping, filtering, sorting, transforming, joining, etc.

---

### 63. **Can we enforce relationships like foreign keys in MongoDB?**

Not natively. You can simulate using references and handle manually or with `$lookup`.

---

### 64. **Difference between `save()` and `insert()`?**

- `save()` replaces entire document if `_id` exists
    
- `insert()` fails on duplicate `_id`
    

---

### 65. **What is `db.stats()`?**

Returns statistics about the current database.

---

### 66. **What is `db.collection.stats()`?**

Returns storage size, index info, and other metrics for a collection.

---

### 67. **How to backup and restore MongoDB?**

- Backup: `mongodump`
    
- Restore: `mongorestore`
    

---

### 68. **How to export and import MongoDB collections?**

- Export: `mongoexport`
    
- Import: `mongoimport`
    

---

### 69. **How to monitor performance in MongoDB?**

- `mongostat`, `mongotop`
    
- Atlas monitoring
    
- Profiler
    

---

### 70. **What are best practices for MongoDB schema design?**

- Embed for one-to-few relationships
    
- Reference for one-to-many or large data
    
- Index frequently queried fields
    
- Avoid deeply nested documents