# SQL Practice Questions
This markdown file is to practice and organize practice examples by commands

## Index
- **[Create](/database_sql/SQL_practice.md.#Create)**

## Create & Alter

### ***Table 'students' creation and ALTER, INSERT***

## Code
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
## Result
![image](/database_sql/images/result1.png)

## Create & Alter

### ***Table 'students' creation and ALTER, INSERT***

## Code
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
## Result
![image](/database_sql/images/output2.png)

---
# Reference
[Link](https://www.sql-practice.com/)
