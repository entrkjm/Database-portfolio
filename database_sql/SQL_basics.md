# SQL Practice Questions
This markdown file is to archive SQL questions for practice.

## Index
[Question1](/database_sql/SQL_basics.md#question-1)


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
## Question 2

### ***Show first name and last name of patients who does not have allergies.(null)***

## Answer
```
SELECT 
  first_name,
  last_name
FROM patients
WHERE allergies IS null
```
## Result
![image](/database_sql/images/result2.png)

---
## Question 3

### ***Show first name of patients that start with the letter 'C'***

## Answer
```
SELECT
	first_name 
FROM 
	patients
WHERE 
	first_name Like 'C%'
```
## Result
![image](/database_sql/images/result3.png)

---
## Question 4

### ***Show first name and last name of patients that weight within the range of 100 to 120 (inclusive)***

## Answer
```
SELECT 
	first_name, last_name
FROM 
	patients
WHERE
	weight >= 100 and weight <= 120
```
## Result
![image](/database_sql/images/result4.png)

---
## Question 5

### ***Update the patients table for the allergies column. If the patient's allergies is null then replace it with 'NKA'***

## Answer
```
UPDATE patients
SET allergies = 'NKA'
WHERE allergies IS NULL
```

---
## Question 6

### ***Show first name and last name concatinated into one column to show their full name.***

## Answer
```
SELECT
  CONCAT(first_name, ' ',last_name) AS full_name
FROM patients
```
---
## Question 7

### ***Show first name, last name, and the full province name of each patient.***
### *** Example: 'Ontario' instead of 'ON'***

## Answer
```
SELECT
  CONCAT(first_name, ' ',last_name) AS full_name
FROM patients
```



## Result
![image](/database_sql/images/result6.png)




---
# Reference
[Link](https://www.sql-practice.com/)




