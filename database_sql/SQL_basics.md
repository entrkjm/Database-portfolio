# SQL Practice Questions
This markdown file is to archive SQL questions for practice.

## Basic Schema for Practice Questions
![image](/database_sql/images/schema.png)

---
## Question 1

### ***Show first name, last name, and gender of patients whose gender is 'M'***

## Answer
```
SELECT 
  first_name,
  last_name,
  gender
FROM patients
WHERE gender = 'M'
```
## Result
![image](/database_sql/images/result1.png)


---

# Reference
[Link](https://www.sql-practice.com/)



