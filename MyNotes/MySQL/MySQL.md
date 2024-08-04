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

## Execution Contexts
1. Whenever we write any command using select operator and fetch something from a table the order of execution is from right side.
2. For ex: If we have a query like `SELECT column1 FROM TABLE1`
	1. First `FROM TABLE1` will execute then
	2. `SELECT column1` will be executed.
## Just some terms
1. INFORMATION_SCHEMA
	1. Information schema database in Mysql is a metadata storage that will provide information about all the databases that is present in your mysql rdbms.
	2. `SELECT table_name FROM INFORMATION_SCHEMA.tables where table_schema='sakila';`
	3. This tells us that there is a global INFORMATION_SCHEMA available in our mysql rdbms. Inside that schema we have tables object which gives us all the information about tables.
	4. We can fetch that using : `SELECT * FROM INFORMATION_SCHEMA.TABLES;`
	5. Now, what we want is lets say, list down all the tables from a specific schema or a dataabase.
	6. We can say, select table_name column which will give me the result of all the table names however there is a clause(where) which says that I need results from `sakila` database/tableschema.
	7. Just like we accesses `INFORMATION_SCHEMA.TABLES` from information_schema we can also access multiple other tables. 
```
	TABLES: Contains information about tables in databases.
	COLUMNS: Contains information about columns in tables.
	SCHEMATA: Contains information about databases (schemas).
	STATISTICS: Contains information about table indexes.
	VIEWS: Contains information about views.
	TRIGGERS: Contains information about triggers.
	ROUTINES: Contains information about stored procedures and functions.
	TABLE_CONSTRAINTS: Contains information about table constraints.
	KEY_COLUMN_USAGE: Contains information about which key columns have constraints.
	REFERENTIAL_CONSTRAINTS: Contains information about foreign key constraints.
	EVENTS: Contains information about scheduled events.
	PARTITIONS: Contains information about table partitions.
```
2. DUAL
	1. This is a dummy table consists of 1 row and 1 column. Whenever we want to execute any expressions for ex: 1+1 or just return 1 using select command, we can use this table
	2. For ex: `SELECT 1;` will output just 1 and the column name will also be 1.
	3. From one of the stack overflow answers, it seems that this select 1 command is used in order to check the connectivity.

## Filtering in MYSQL
1. Please check : 