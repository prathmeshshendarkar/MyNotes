## MySQL Internal Databases
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