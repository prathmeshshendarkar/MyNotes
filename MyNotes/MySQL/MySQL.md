> SQL stands for Structured Query Language

## Crud Operations in MySQL
1. Create : To create a table or database schema in a database.
2. Read : To Read the records from the table.
3. Update : To update the records or update the attributes.
4. Delete : To delete the records from the table

> SQL is a way to perform operations on a RDBMS whereas MySQL is a software that helps us create a RDBMS Environment with the help of SQL.

## Properties of MySQL
1. MySQL is a opensource and relational DBMS

## Data Types
1. ![[Pasted image 20240802190817.png]]
2. Check Here : [[MySQL Data Types]]

## Commands
1. ![[Pasted image 20240803193638.png]]
2. Check Here for more details: [[MySQL Commands]]

## Just some terms
1. INFORMATION_SCHEMA
	1. `SELECT table_name FROM INFORMATION_SCHEMA.tables where table_schema='sakila';`
	2. This tells us that there is a global INFORMATION_SCHEMA available in our mysql rdbms. Inside that schema we have tables object which gives us all the information about tables.
	3. We can fetch that using : `SELECT * FROM INFORMATION_SCHEMA.TABLES;`
	4. Now, what we want is lets say, list down all the tables from a specific schema or a dataabase.
	5. We can say, select table_name column which will give me the result of all the table names however there is a clause(where) which says that I need results from `sakila` database/tableschema.
2. 