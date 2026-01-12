## Q1. What is MongoDB?

MongoDB is a **NoSQL database** that stores data in **documents (JSON format)** instead of tables.

---

## Q2. Difference between SQL and MongoDB?

| SQL          | MongoDB         |
| ------------ | --------------- |
| Table        | Collection      |
| Row          | Document        |
| Column       | Field           |
| Schema fixed | Schema flexible |

---

## Q3. Create a database.

```js
use university
```

**Explanation:**
Creates database if not exists and selects it.

Keyword: `use`

---

## Q4. Insert one document.

```js
db.student.insertOne({name:"Ravi",age:18})
```

**Keywords:**

* insertOne → insert single document

---

## Q5. Insert multiple documents.

```js
db.student.insertMany([
{name:"Anita",age:19},
{name:"Kiran",age:18}
])
```

---

## Q6. Display all documents.

```js
db.student.find()
```

find() → fetch records

---

## Q7. Display selected fields.

```js
db.student.find({}, {name:1, age:1, _id:0})
```

| Keyword | Meaning   |
| ------- | --------- |
| {}      | condition |
| 1       | show      |
| 0       | hide      |

---

## Q8. Display age = 18.

```js
db.student.find({age:18})
```

---

## Q9. Update record.

```js
db.student.updateOne(
{name:"Ravi"},
{$set:{age:20}}
)
```

Keywords:

* updateOne
* $set

---

## Q10. Update many.

```js
db.student.updateMany({}, {$set:{city:"Bangalore"}})
```

---

## Q11. Delete one record.

```js
db.student.deleteOne({name:"Ravi"})
```

---

## Q12. Delete many.

```js
db.student.deleteMany({age:{$lt:18}})
```

$lt → less than

---

## Q13. Drop collection.

```js
db.student.drop()
```

---

## Q14. Find with condition operators.

```js
db.student.find({age:{$gt:18}})
```

| Operator | Meaning       |
| -------- | ------------- |
| $gt      | greater than  |
| $lt      | less than     |
| $gte     | greater equal |
| $lte     | less equal    |

---

## Q15. Sort records.

```js
db.student.find().sort({age:1})
```

1 → ascending
-1 → descending

---

## Q16. Count records.

```js
db.student.countDocuments()
```

---

## Q17. Limit records.

```js
db.student.find().limit(2)
```

---

## Q18. What is a document?

A document is a JSON object stored in MongoDB.

---

## Q19. What is a collection?

Collection is group of documents.

---

## Q20. What is NoSQL?

NoSQL means Not Only SQL.

---

# 📘 COMPANY DATABASE EXAM QUESTIONS IN MONGODB

---

### Insert client

```js
db.client.insertOne({client_no:101,name:"Ravi",city:"Bangalore"})
```

---

### Display all clients

```js
db.client.find()
```

---

### Display name and city

```js
db.client.find({}, {name:1,city:1,_id:0})
```

---

### Update city

```js
db.client.updateOne({client_no:101},{$set:{city:"Bombay"}})
```

---

### Delete quantity < 5

```js
db.product.deleteMany({quantity_on_hand:{$lt:5}})
```

---

### Salary = 3000

```js
db.salesman.find({salary:3000},{name:1,_id:0})
```

---

# 📘 UNIVERSITY DATABASE MONGODB

---

### Insert student

```js
db.student.insertOne({R_no:1,name:"Ravi",age:18})
```

---

### Age 18

```js
db.student.find({age:18})
```

---

### Add semester field

```js
db.course.updateMany({},{$set:{semester:1}})
```

---

### Change course name

```js
db.course.updateOne({courseid:105},{$set:{course_name:"DBMS",credit:4}})
```

---

# 📘 IMPORTANT KEYWORDS

| Keyword    | Meaning           |
| ---------- | ----------------- |
| find       | fetch             |
| insertOne  | insert            |
| insertMany | insert multiple   |
| updateOne  | update            |
| updateMany | update many       |
| deleteOne  | delete            |
| deleteMany | delete many       |
| drop       | remove collection |
| $set       | update value      |
| $lt        | less              |
| $gt        | greater           |

---

# 📘 VIVA QUESTIONS

1. What is MongoDB?
2. What is document?
3. What is collection?
4. Difference SQL and MongoDB
5. What is $set?
6. What is NoSQL?
