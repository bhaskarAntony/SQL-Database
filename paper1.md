## Q1. Create a database named university.

```sql
CREATE DATABASE university;
```

### Keywords:

| Keyword  | Meaning               |
| -------- | --------------------- |
| CREATE   | Used to create object |
| DATABASE | Database object       |

### Explanation:

This command creates a new database called university.

---

## Q2. Select the database.

```sql
USE university;
```

| Keyword | Meaning         |
| ------- | --------------- |
| USE     | Select database |

---

## Q3. Create student table.

```sql
CREATE TABLE student (
R_no INT(10),
name VARCHAR(20),
age INT,
gender VARCHAR(10),
address VARCHAR(20)
);
```

| Keyword | Meaning       |
| ------- | ------------- |
| TABLE   | Creates table |
| INT     | Number        |
| VARCHAR | Text          |
| (10)    | Size          |

---

## Q4. Display structure of table.

```sql
DESC student;
```

| Keyword | Meaning        |
| ------- | -------------- |
| DESC    | Describe table |

---

## Q5. Insert record into table.

```sql
INSERT INTO student VALUES (1,'Ravi',18,'Male','Bangalore');
```

| Keyword | Meaning      |
| ------- | ------------ |
| INSERT  | Add data     |
| INTO    | Target table |
| VALUES  | Data         |

---

## Q6. Display all records.

```sql
SELECT * FROM student;
```

| Keyword | Meaning     |
| ------- | ----------- |
| SELECT  | Fetch       |
| *       | All columns |
| FROM    | Table name  |

---

## Q7. Display name and age only.

```sql
SELECT name, age FROM student;
```

---

## Q8. Display students age 18.

```sql
SELECT * FROM student WHERE age=18;
```

| Keyword | Meaning   |
| ------- | --------- |
| WHERE   | Condition |

---

## Q9. Add new column.

```sql
ALTER TABLE faculty ADD date_of_joining DATE;
```

| Keyword | Meaning      |
| ------- | ------------ |
| ALTER   | Modify table |
| ADD     | Add column   |
| DATE    | Date type    |

---

## Q10. Delete column.

```sql
ALTER TABLE course DROP duration;
```

| Keyword | Meaning |
| ------- | ------- |
| DROP    | Remove  |

---

## Q11. Update record.

```sql
UPDATE faculty SET salary=20000 WHERE fid=101;
```

| Keyword | Meaning      |
| ------- | ------------ |
| UPDATE  | Change data  |
| SET     | Assign value |

---

## Q12. Delete record.

```sql
DELETE FROM faculty WHERE salary < 15000;
```

| Keyword | Meaning    |
| ------- | ---------- |
| DELETE  | Remove row |

---

## Q13. Rename table.

```sql
RENAME TABLE course TO course_details;
```

---

## Q14. Insert multiple values.

```sql
INSERT INTO student VALUES
(2,'Anita',19,'Female','Mysore'),
(3,'Kiran',18,'Male','Tumkur');
```

---

## Q15. Change course name.

```sql
UPDATE course_details
SET course_name='DBMS', credit=4
WHERE courseid=105;
```

---

## Q16. Display faculty with salary 30000.

```sql
SELECT fname FROM faculty WHERE salary=30000;
```

---

# 🔹 THEORY QUESTIONS WITH ANSWERS

---

### Q17. What is SQL?

SQL is a language used to manage data in databases.

---

### Q18. What is table?

Table stores data in rows and columns.

---

### Q19. What is primary key?

Primary key uniquely identifies each record.

---

### Q20. Difference between DELETE and DROP?

| DELETE          | DROP             |
| --------------- | ---------------- |
| Removes records | Removes table    |
| Data only       | Structure + data |

---

### Q21. What is VARCHAR?

VARCHAR stores text with variable length.

---

### Q22. What is WHERE?

Used to apply condition.

---

### Q23. What is DDL?

DDL is used to define database structure.

Examples: CREATE, ALTER, DROP.

---

### Q24. What is DML?

Used to manipulate data.

Examples: INSERT, UPDATE, DELETE.

---

# 🔹 IMPORTANT KEYWORDS SUMMARY

| Keyword | Use                 |
| ------- | ------------------- |
| CREATE  | Create              |
| INSERT  | Add                 |
| SELECT  | Fetch               |
| UPDATE  | Modify              |
| DELETE  | Remove              |
| ALTER   | Change structure    |
| DROP    | Remove column/table |
| WHERE   | Condition           |
| DESC    | Structure           |
| RENAME  | Rename              |
