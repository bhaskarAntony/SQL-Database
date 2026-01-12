

# 🔹 PAPER 1 – COMPANY DATABASE

---

## Create Database

```sql
CREATE DATABASE company;
USE company;
```

**CREATE** = create object
**DATABASE** = database name
**USE** = select database

---

## Create Tables

### Client

```sql
CREATE TABLE client(
client_no INT(10),
name VARCHAR(20),
address VARCHAR(20),
city VARCHAR(20),
pincode INT(20),
state VARCHAR(20),
balance_due INT(20)
);
```

---

### Product

```sql
CREATE TABLE product(
product_no INT(5),
description VARCHAR(15),
profit_percent INT(5),
quantity_on_hand INT,
sell_price INT,
cost_price INT
);
```

---

### Salesman

```sql
CREATE TABLE salesman(
salesman_no INT(5),
salesman_name VARCHAR(20),
address VARCHAR(20),
city VARCHAR(20),
pincode INT(8),
state VARCHAR(20),
sales_amt INT(10),
salary INT(10),
remark VARCHAR(20)
);
```

---

## a) Describe tables

```sql
DESC client;
DESC product;
DESC salesman;
```

DESC = shows structure.

---

## b) Insert 5 records

```sql
INSERT INTO client VALUES
(101,'Ravi','MG Road','Bangalore',560001,'KA',2000),
(102,'Anita','BTM','Mysore',570001,'KA',1500),
(103,'Kiran','RR Nagar','Tumkur',572101,'KA',1000),
(104,'Suma','JP Nagar','Hassan',573201,'KA',500),
(105,'Manoj','Whitefield','Chennai',600001,'TN',2500);
```

```sql
INSERT INTO product VALUES
(101,'Pen',10,20,15,10),
(102,'Book',15,8,120,100),
(103,'Bag',20,3,800,650),
(104,'Mouse',10,12,400,350),
(105,'Keyboard',12,4,600,500);
```

```sql
INSERT INTO salesman VALUES
(101,'Ramesh','BTM','Bangalore',560076,'KA',20000,3000,'Good'),
(102,'Suresh','JP','Mysore',570001,'KA',18000,2500,'Nice'),
(103,'Mahesh','RR','Tumkur',572101,'KA',15000,3000,'Good'),
(104,'Kavya','BTM','Hassan',573201,'KA',14000,2800,'Nice'),
(105,'Divya','White','Chennai',600001,'TN',19000,3500,'Best');
```

---

## c) Display all

```sql
SELECT * FROM client;
SELECT * FROM product;
SELECT * FROM salesman;
```

SELECT = fetch

* = all columns

---

## d) Client name and city

```sql
SELECT name, city FROM client;
```

---

## e) Add date_of_joining

```sql
ALTER TABLE salesman ADD date_of_joining DATE;
```

ALTER = change structure
ADD = add column

---

## f) Update sell_price

```sql
UPDATE product SET sell_price=120 WHERE product_no=101;
```

---

## g) Drop remark

```sql
ALTER TABLE salesman DROP remark;
```

DROP = remove column

---

## h) Rename product

```sql
RENAME TABLE product TO prod;
```

---

## i) Add product_name

```sql
ALTER TABLE prod ADD product_name VARCHAR(20);
```

---

## j) Insert product names

```sql
UPDATE prod SET product_name='Pen' WHERE product_no=101;
UPDATE prod SET product_name='Book' WHERE product_no=102;
UPDATE prod SET product_name='Bag' WHERE product_no=103;
UPDATE prod SET product_name='Mouse' WHERE product_no=104;
UPDATE prod SET product_name='Keyboard' WHERE product_no=105;
```

---

## k) Delete quantity < 5

```sql
DELETE FROM prod WHERE quantity_on_hand < 5;
```

---

## l) Salary update

```sql
UPDATE salesman SET salary=10000 WHERE salesman_no=101;
```

---

## m) Change city & pincode

```sql
UPDATE client
SET city='Bombay', pincode=657892
WHERE client_no=105;
```

---

## n) Salary = 3000

```sql
SELECT salesman_name FROM salesman WHERE salary=3000;
```

---

# 🔹 PAPER 2 – UNIVERSITY DATABASE

---

## Create Database

```sql
CREATE DATABASE university;
USE university;
```

---

## Create Tables

```sql
CREATE TABLE student(
R_no INT(10),
name VARCHAR(20),
age INT,
gender VARCHAR(10),
address VARCHAR(20)
);
```

```sql
CREATE TABLE faculty(
fid INT(5),
fname VARCHAR(15),
age INT(5),
salary INT(10),
address VARCHAR(20)
);
```

```sql
CREATE TABLE course(
courseid INT,
course_name VARCHAR(20),
credit INT,
duration INT
);
```

---

## a) Describe

```sql
DESC student;
DESC faculty;
DESC course;
```

---

## b) Insert records

```sql
INSERT INTO student VALUES
(1,'Ravi',18,'Male','Bangalore'),
(2,'Anita',19,'Female','Mysore'),
(3,'Kiran',18,'Male','Tumkur'),
(4,'Suma',20,'Female','Hassan'),
(5,'Manoj',21,'Male','Mandya');
```

```sql
INSERT INTO faculty VALUES
(101,'Ramesh',35,20000,'Bangalore'),
(102,'Suresh',40,30000,'Mysore'),
(103,'Mahesh',45,25000,'Tumkur'),
(104,'Kavya',30,14000,'Hassan'),
(105,'Divya',32,28000,'Mandya');
```

```sql
INSERT INTO course VALUES
(101,'C',3,30),
(102,'Java',4,40),
(103,'Python',3,35),
(104,'Web',2,25),
(105,'SQL',3,20);
```

---

## c) Display all

```sql
SELECT * FROM student;
SELECT * FROM faculty;
SELECT * FROM course;
```

---

## d) Student name & age

```sql
SELECT name, age FROM student;
```

---

## e) Add date

```sql
ALTER TABLE faculty ADD date_of_joining DATE;
```

---

## f) Update courseid

```sql
UPDATE course SET courseid=120 WHERE courseid=101;
```

---

## g) Drop duration

```sql
ALTER TABLE course DROP duration;
```

---

## h) Rename course

```sql
RENAME TABLE course TO course_details;
```

---

## i) Add semester

```sql
ALTER TABLE course_details ADD semester INT;
```

---

## j) Insert semester

```sql
UPDATE course_details SET semester=1 WHERE courseid=120;
UPDATE course_details SET semester=2 WHERE courseid=102;
UPDATE course_details SET semester=3 WHERE courseid=103;
UPDATE course_details SET semester=4 WHERE courseid=104;
UPDATE course_details SET semester=5 WHERE courseid=105;
```

---

## k) Delete salary <15000

```sql
DELETE FROM faculty WHERE salary<15000;
```

---

## l) Salary change

```sql
UPDATE faculty SET salary=20000 WHERE fid=101;
```

---

## m) Change course name

```sql
UPDATE course_details
SET course_name='DBMS', credit=4
WHERE courseid=105;
```

---

## n) Salary = 30000

```sql
SELECT fname FROM faculty WHERE salary=30000;
```

---

## o) Students age 18

```sql
SELECT * FROM student WHERE age=18;
```

---

# 🔹 IMPORTANT KEYWORDS

| Keyword | Meaning          |
| ------- | ---------------- |
| CREATE  | Create           |
| INSERT  | Add              |
| SELECT  | Fetch            |
| UPDATE  | Modify           |
| DELETE  | Remove           |
| ALTER   | Change structure |
| DROP    | Remove           |
| WHERE   | Condition        |
| DESC    | Describe         |
| RENAME  | Rename           |

---

# 🔹 MOST COMMON VIVA QUESTIONS

1. What is SQL?
2. What is primary key?
3. Difference between DELETE and DROP
4. What is VARCHAR?
5. What is WHERE clause?
6. What is ALTER command?

