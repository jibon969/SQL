

<img src="image/sql-learning.png" id='header'>
<h1 align="center">Learn SQl</h1>
<div align="center">
<!-- Gmail Account -->
<a href="mailto:jayed.swe@gmail.com">
<img src='https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white'
alt='Jayed Hossain Jibon'
/>
</a>
<a href="tel:+8801987132107">
<img
src='https://img.shields.io/badge/WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white'
alt='Jayed Hossain Jibon'
/>
<a href="#" target="_blank">
<img
src='https://img.shields.io/badge/website-000000?style=for-the-badge&logo=About.me&logoColor=white'
alt='Jayed Hossain Jibon'
/>
</a>
<a href="https://www.facebook.com/jibon969" target="_blank">
<img
src='https://img.shields.io/badge/Facebook-1877F2?style=for-the-badge&logo=facebook&logoColor=white'
alt='Jayed Hossain Jibon'
/>

<a href="https://www.linkedin.com/in/jibon969/" target="_blank">
<img
src='https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white'
alt='Jayed Hossain Jibon'
/>
</a>
<a href="https://github.com/jibon969" target="_blank">
<img
src='https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white'
alt='Jayed Hossain Jibon'
/>
</a>
</div>

<hr/>

#### 01. Create database and drop database 

<details><summary style="cursor:pointer">Solution</summary>

```sql
create database learn_sql;
drop database learn_sql;
```
</details>

#### 02. How to create table

<details><summary style="cursor:pointer">Solution</summary>

```sql
CREATE TABLE Customers (
    CustomerID serial PRIMARY KEY,
    CustomerName VARCHAR ( 100 ) UNIQUE NOT NULL,
    ContactName VARCHAR ( 20 ) NOT NULL,
    Address VARCHAR ( 100 ) NOT NULL,
    City VARCHAR ( 100 ) UNIQUE NOT NULL,
    PostalCode VARCHAR ( 100 ) UNIQUE NOT NULL,
    Country VARCHAR ( 100 ) UNIQUE NOT NULL
);
```
</details>

#### 03. How to drop table 

<details><summary style="cursor:pointer">Solution</summary>

```sql
drop table Customers;
```
</details>

#### 04. Insert data into a table

<details><summary style="cursor:pointer">Solution</summary>

```sql
INSERT INTO Customers (CustomerName, ContactName, Address, City, PostalCode, Country)
VALUES ('Jibon Ahmed', '01987132107', '69/A, Dhaka', 'Dhaka', '1200', 'Bangladesh');

--- Multiple value insert
INSERT INTO Customers (CustomerName, ContactName, Address, City, PostalCode, Country)
VALUES 
('Jibon Ahmed',   '01987132107', '69/A, Dhaka', 'Dhaka', '1200', 'Bangladesh'),
('Jayed Hossain', 'Georg Pipps', 'Geislweg 14', 'Salzburg ', '5020 ', 'Austria');
```
</details>

### SQL Query 

#### Return all the columns from the Customers table
```
Syntax:
SELECT column1, column2, ...
FROM table_name; 
```
<details><summary style="cursor:pointer">Solution</summary>

```sql
select * from customers
```
</details>

#### Return CustomerName, City from the Customers table
<details><summary style="cursor:pointer">Solution</summary>

```sql
select CustomerName, City from customers
```
</details>

#### The SELECT DISTINCT statement is used to return only distinct 
```
Syntax:
SELECT DISTINCT column1, column2, ...
FROM table_name;
```
<details><summary style="cursor:pointer">Solution</summary>

```sql
select count(DISTINCT country) from customers;
```
</details>


#### SQL WHERE Clause
```
Syntax:
SELECT column1, column2, ...
FROM table_name
WHERE condition;
```
</details>

#### Select all customers from Bangladesh:
<details><summary style="cursor:pointer">Solution</summary>

```sql
SELECT * FROM Customers
WHERE Country='Bangladesh';
```
</details>




---
**[⬆ Back to Top](#header)**

