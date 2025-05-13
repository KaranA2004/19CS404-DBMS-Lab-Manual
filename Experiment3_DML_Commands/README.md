# Experiment 3: DML Commands
## Name : Karan A
## Reg No : 212222060113
## AIM
To study and implement DML (Data Manipulation Language) commands.

## THEORY

### 1. INSERT INTO
Used to add records into a relation.
These are three type of INSERT INTO queries which are as
A)Inserting a single record
**Syntax (Single Row):**
```sql
INSERT INTO table_name (field_1, field_2, ...) VALUES (value_1, value_2, ...);
```
**Syntax (Multiple Rows):**
```sql
INSERT INTO table_name (field_1, field_2, ...) VALUES
(value_1, value_2, ...),
(value_3, value_4, ...);
```
**Syntax (Insert from another table):**
```sql
INSERT INTO table_name SELECT * FROM other_table WHERE condition;
```
### 2. UPDATE
Used to modify records in a relation.
Syntax:
```sql
UPDATE table_name SET column1 = value1, column2 = value2 WHERE condition;
```
### 3. DELETE
Used to delete records from a relation.
**Syntax (All rows):**
```sql
DELETE FROM table_name;
```
**Syntax (Specific condition):**
```sql
DELETE FROM table_name WHERE condition;
```
### 4. SELECT
Used to retrieve records from a table.
**Syntax:**
```sql
SELECT column1, column2 FROM table_name WHERE condition;
```
**Question 1**

Write a SQL statement to update the product_name as 'Grapefruit' whose product_id is 4 in the products table.
```
update products
set product_name='Grapefruit'
where product_id=4;
```

**Output:**

![image](https://github.com/user-attachments/assets/2079a8c9-3ba4-4d6e-84b6-5c53bfeb112c)

**Question 2**

Write a SQL query to reduce the reorder level by 30% where cost price is more than 50 and quantity in stock is less than 100 in the products table.
```
update Products
set reorder_lvl=reorder_lvl*0.7
where cost_price>50 and quantity<100;
```
**Output:**

![image](https://github.com/user-attachments/assets/ce8578d2-4a6a-46e6-9d7b-500b56467d79)

**Question 3**

Write a SQL query to Delete a Specific Surgery which was made on 28th Feb 2024.
```
delete from Surgeries 
where surgery_date='2024-02-28';
```
**Output:**

![image](https://github.com/user-attachments/assets/4cf2e546-f59f-408d-b7c9-ca449e95262c)

**Question 4**
Write a SQL query to Delete customers from 'customer' table where 'GRADE' is not equal to 3.
```
delete from customer
where GRADE!=3;
```
**Output:**

![image](https://github.com/user-attachments/assets/62d778bb-cdc3-45a4-a2ef-58d913f0beac)

**Question 5**

Write a query to fetch details of employees whose EmpLname ends with an alphabet ‘A’ and contains five alphabets.
```
select * from EmployeeInfo 
where EmpLname like '%A' and length(EmpLname)=5;
```

**Output:**

![image](https://github.com/user-attachments/assets/20faf609-e393-4458-9c56-da2692919e12)

**Question 6**

Write a SQL query to classify base in the Calculations table as 'Provided' if it is not NULL, otherwise 'Not Provided'.
```
select id,base,
case when base is not NULL then 'Provided'
else 'Not Provided'
end as base_status
from Calculations;
```

**Output:**

![image](https://github.com/user-attachments/assets/a2667fc1-fde5-4fcc-9527-63b2cb3ab032)

**Question 7**

Write a SQL query to calculate the final price after applying both the discount and the tax. Return product_id, original_price, discount_percentage, tax_rate, and final_price.
```
select product_id,original_price,discount_percentage,tax_rate,(original_price*(1-discount_percentage))*(1+tax_rate) as final_price
from products;
```

**Output:**

![image](https://github.com/user-attachments/assets/502345b9-8064-4903-8d1a-27235b07bcab)

**Question 8**

Create a report that shows the capitalized FirstName and capitalized LastName renamed as FirstName and Lastname respectively and EmployeeId from the employees table sorted by EmployeeId in descending order.
```
select upper(FirstName) AS FirstName,upper(LastName) AS LastName,EmployeeId
from employees
order by EmployeeID desc;
```

**Output:**

![image](https://github.com/user-attachments/assets/65284a61-9a56-47d5-b41f-201a52575825)

**Question 9**

Write a SQL statement to retrieve city(column name) of all customers from customers table without any repeats.
```
select distinct city from customers;
```

**Output:**

![image](https://github.com/user-attachments/assets/20e5b8ee-89e3-4f33-80a2-beb5e03876d2)

**Question 10**

Write a SQL statement to Double the salary for employees in department 20 who have a job_id ending with 'MAN'
```
update EMPLOYEES
SET SALARY= SALARY *2
WHERE JOB_ID like'%MAN';
```

**Output:**

![image](https://github.com/user-attachments/assets/9ec40e7e-50a6-4a7b-a732-d1bca272ed13)

## RESULT
Thus, the SQL queries to implement DML commands have been executed successfully.
