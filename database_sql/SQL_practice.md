# SQL Practice Questions
This markdown file is to practice and organize practice examples by commands

## Index
- **[Create](/database_sql/SQL_practice.md.#create)**
- **[Create & Alter](/database_sql/SQL_practice.md.#create--alter)**
- **[Insert & Update & Delete](/database_sql/SQL_practice.md.#insert--update--delete)**

## Create
**Table 'students' creation and ALTER, INSERT**

**Code**

---

```
-- create a table
CREATE TABLE students (
  id INTEGER,
  name TEXT NOT NULL,
  gender CHAR(1) NOT NULL,
  PRIMARY KEY(id)
);

-- alter table
ALTER TABLE students ADD score FLOAT;

insert some values
INSERT INTO students VALUES (1, 'Ryan', 'M', '32.9');
INSERT INTO students VALUES (2, 'Joanna', 'F', '44.9');
-- fetch some values
SELECT * FROM students
```
---

**Result**
![image](/database_sql/images/result1.png)

---

## Create & Alter

**Table 'students' creation and ALTER, INSERT**

**Code**

---

```
-- create a table
CREATE TABLE students (
  id INTEGER,
  name TEXT NOT NULL,
  gender CHAR(1) NOT NULL,
  PRIMARY KEY(id)
);

-- alter table
ALTER TABLE students ADD score FLOAT;

-- insert
INSERT INTO students VALUES (1, 'Ryan', 'M', 32.9);
INSERT INTO students VALUES (2, 'Joanna', 'F', 44.9);
INSERT INTO students VALUES (3, 'Jin', 'M', 33.6);

-- ALTER TABLE students DROP COLUMN gender;

UPDATE students SET score = 47.1
WHERE name = 'Jin';

-- fetch some values
SELECT * FROM students
```
---

## Insert & Update & Delete

**Table 'students' creation and ALTER, INSERT, UPDATE, DELETE**

**Code**

---

```
-- create a table
CREATE TABLE students (
  id INTEGER PRIMARY KEY,
  name TEXT NOT NULL,
  gender TEXT NOT NULL
);

ALTER TABLE students ADD score INTEGER NOT NULL;

INSERT INTO students VALUES(234, 'Pam', 'F', 44);
INSERT INTO students VALUES(235, 'Jim', 'M', 33);
INSERT INTO students VALUES(236, 'Dwight', 'M', 22);
INSERT INTO students VALUES(237, 'Michael', 'M', 27);

--ALTER TABLE students DROP COLUMN gender;

DELETE FROM students
  WHERE name = 'Dwight'; 

UPDATE students SET score = 32
  WHERE name = 'Micheal';

SELECT * FROM students;
```
---


**Result**

![image](/database_sql/images/output3.png)

---


---
# Reference
[Link](https://www.sql-practice.com/)
