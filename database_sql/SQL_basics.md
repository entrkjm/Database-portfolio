# SQL Practice Questions
This markdown file is to archive SQL questions for practice.

## Index
- **[Question1](/database_sql/SQL_basics.md#question-1)**
- **[Question2](/database_sql/SQL_basics.md#question-2)**
- **[Question3](/database_sql/SQL_basics.md#question-3)**
- **[Question4](/database_sql/SQL_basics.md#question-4)**
- **[Question5](/database_sql/SQL_basics.md#question-5)**
- **[Question6](/database_sql/SQL_basics.md#question-6)**
- **[Question7](/database_sql/SQL_basics.md#question-7)**
- **[Question8](/database_sql/SQL_basics.md#question-8)**
- **[Question9](/database_sql/SQL_basics.md#question-9)**
- **[Question10](/database_sql/SQL_basics.md#question-10)**
- **[Question11](/database_sql/SQL_basics.md#question-11)** 
- **[Question12](/database_sql/SQL_basics.md#question-12)** 


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
## Result
![image](/database_sql/images/result5.png)

---
## Question 6

### ***Show first name and last name concatinated into one column to show their full name.***

## Answer
```
SELECT
  CONCAT(first_name, ' ',last_name) AS full_name
FROM patients
```
## Result
![image](/database_sql/images/result6.png)

---
## Question 7

### ***Show first name, last name, and the full province name of each patient.***
### *** Example: 'Ontario' instead of 'ON'***

## Answer
```
SELECT
    first_name, 
    last_name, 
    province_name

From patients
    JOIN province_names on province_names.province_id = patients.province_id
```
## Result
![image](/database_sql/images/result7.png)

---
## Question 8

### ***Show how many patients have a birth_date with 2010 as the birth year.***

## Answer
```
SELECT COUNT (patient_id) AS Born_in_2010
FROM patients
WHERE YEAR(birth_date) = 2010
```
## Result
![image](/database_sql/images/result8.png)

---
## Question 9

### ***Show the first_name, last_name, and height of the patient with the greatest height.***

## Answer
```
SELECT first_name, last_name, MAX(height) as height
FROM patients
```
## Result
![image](/database_sql/images/result9.png)

---
## Question 10

### ***Show the total number of admissions***

## Answer
```
SELECT COUNT(*) AS total_admissions
FROM admissions
```
## Result
![image](/database_sql/images/result10.png)

---
## Question 11

### ***Show all the columns from admissions where the patient was admitted and discharged on the same day.***

## Answer
```
SELECT *
FROM admissions
WHERE admission_date = discharge_date
```
## Result
![image](/database_sql/images/result11.png)

---
## Question 12

### ***Show the patient id and the total number of admissions for patient_id 579.***

## Answer
```
SELECT patient_id, COUNT(patient_id) AS total_admissions
FROM admissions
WHERE patient_id = 579
```
## Result
![image](/database_sql/images/result12.png)


---
# Reference
[Link](https://www.sql-practice.com/)




