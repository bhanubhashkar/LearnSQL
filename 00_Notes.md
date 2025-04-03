
# SQL Notes
[Checkout my Profile](https://github.com/bhanubhashkar)

## Introduction
```sql
/*
Database :
A database is an electronically stored, systematic collection of data that can include words, numbers, images, videos, 
and other types of files. Databases are managed using specialized software called a Database Management System (DBMS), 
which allows users to store, retrieve, and manipulate data efficiently. 

Key Features of a Database :
Organized Data Storage: Data is stored in structured formats, such as tables, documents, or key-value pairs.
Efficient Access: Advanced search and query capabilities allow for quick data retrieval.
Security and Scalability: Databases provide robust security measures and can scale with growing data needs.
*/

/*
SQL :
SQL is a Structured query language used to access and manipulate data in databases. 
SQL stands for Structured Query Language. 
We can create, update, delete, and retrieve data in databases like MySQL, Oracle, PostgreSQL, etc. 
Overall, SQL is a query language that communicates with databases.
*/
```

## SELECT Statement
```sql
Intro :
The SELECT statement is used to select data from a database.

Syntax :
SELECT column1, column2, ...
FROM table_name;

Example :
SELECT * FROM table_name;
Return all column from a table.

SELECT column1, column2, column3 FROM TableName;
Return selective column from a table.

Keynote:


Exercise :
SELECT address, district FROM address;

SELECT first_name, last_name, email FROM customer;

```

## ORDER BY Clause
```sql
Intro :
The ORDER BY clause is used to sort the result-set in ascending or descending order.

Syntax :
SELECT column1, column2, ...
FROM table_name
ORDER BY column1, column2, ... ASC|DESC;

Example :
SELECT column1, column2
FROM table_name
ORDER BY column1 ASC;
Sort column1 in ascending order.

SELECT column1, column2
FROM table_name
ORDER BY column1 DESC;
Sort column1 in descending order.

SELECT column1, column2
FROM table_name
ORDER BY column1 ASC, column2 ASC;
Sort column1 & column2 in ascending order.

SELECT column1, column2
FROM table_name
ORDER BY column1 ASC, column2 DESC;
Sort column1 in ascending & column2 in descending order.

SELECT column1, column2
FROM table_name
ORDER BY 1 ASC, 2 DESC;
Sort column1 in ascending & column2 in descending order using column no.

Keynote :
Default behavior of the ORDER BY clause is Ascending Order.
To apply sort by, column no of the result set can be used. Not recommended as it decrease readability. 

Exercise :
SELECT * FROM payment ORDER BY customer_id, amount;

SELECT * FROM payment ORDER BY customer_id, amount DESC;

SELECT * FROM books ORDER BY price DESC;

Below two query returns same result.
SELECT first_name, last_name, email FROM customer
ORDER BY first_name DESC, last_name DESC;

SELECT first_name, last_name, email FROM customer
ORDER BY 1 DESC, 2 DESC;

```

## SELECT DISTINCT Statement
```sql
Intro :
The SELECT DISTINCT statement is used to return only distinct (different) values

Syntax :
SELECT DISTINCT column1, column2, ...
FROM table_name;

Example :
SELECT DISTINCT column1
FROM table_name;
Apply distinct on column1 and return result.

SELECT DISTINCT column1, column2, ...
FROM table_name;
Apply distinct on column1, column2 and return result.

SELECT COUNT (DISTINCT column1) FROM table_name;
Returns count of distinct value present in column1.

Keynote :
Distinct in terms of all selected columns.
It applies on all selected column, even if we have two Ram in first_name but with diff last_name, it will be considerd as two unique value hence both with come in result.

Exercise :
SELECT DISTINCT rating FROM film;

SELECT DISTINCT rental_duration FROM film;

SELECT DISTINCT rating, rental_duration FROM film;

SELECT DISTINCT amount FROM payment ORDER BY amount DESC;

SELECT COUNT (DISTINCT customer_id) FROM payment;

```


## LIMIT Clause
```sql
Intro :
The LIMIT clause is used to specify the number of records to return. It always at the end of the query.
The LIMIT clause is useful on large tables with thousands of records. Returning a large number of records can impact performance.

Syntax :
SELECT column1, column2, ...
FROM table_name
LIMIT number;

Example :
SELECT * 
FROM table_name 
LIMIT 10;

SELECT column1, column2, column3
FROM table_name 
ORDER BY column3 DESC
LIMIT 100;

Exercise :
SELECT * FROM rental LIMIT 100;

SELECT rental_id, rental_date FROM rental ORDER BY rental_date DESC LIMIT 100;

SELECT DISTINCT genre FROM books ORDER BY genre LIMIT 5;

Keynote :

```


## COUNT() Function
```sql
Intro :
The COUNT() function returns the number of rows that matches a specified criterion.

Syntax :
SELECT COUNT(column_name)
FROM table_name;

Example :
SELECT COUNT(ProductName)
FROM Products;

SELECT COUNT(ProductID)
FROM Products
WHERE Price > 20;

SELECT COUNT(DISTINCT Price)
FROM Products;

Exercise :
SELECT COUNT(*) FROM customer;

SELECT COUNT(DISTINCT first_name) FROM customer;

SELECT COUNT(id) from employees;

Keynote :
Null values from selected column will not be counted.

```

### Challenge Solution
```sql
01 : SELECT DISTINCT (district) FROM address

02 : SELECT rental_date FROM rental ORDER BY rental_date DESC LIMIT 1;

03 : SELECT COUNT(title) FROM film;

04 : SELECT COUNT(DISTINCT last_name) FROM customer;

05 : 


Syntax :


Example :


Exercise :


Keynote :

```


## Topic Name
```sql
Intro :


Syntax :


Example :


Exercise :


Keynote :

```




## Comments
```sql
/*

*/
```