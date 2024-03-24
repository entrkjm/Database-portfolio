# SQL Practice Questions
This markdown file is to practice and organize practice examples by commands

## Index
- **[Create](/database_sql/SQL_practice.md.#Create)**

## Create 

### ***Table 'students' creation and ALTER, INSERT ***

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

---
# Reference
[Link](https://www.sql-practice.com/)
