## Constraints in MySQL Table Creation

1. NOT NULL
2. PRIMARY KEY
3. FOREIGN KEY
4. UNIQUE
5. CHECK
6. DEFAULT

## Commands
1. DESCRIBE TABLE_NAME => Will provide in depth details of a table.
2. SHOW COLUMNS FROM TABLE_NAME => SAME AS ABOVE
3. COMMAND
    - `SELECT COLUMN_NAME FROM INFORMATION_SCHEMA.COLUMNS WHERE TABLE_SCHEMA='SAMPLEDATABASE1' AND TABLE_NAME='TABLE1';`
4. 

## Primary Key
1. There are three properties that needs to be followed for a primary key in a table
- NOT NULL
- Unique
- Only one primary key should exists in a table.

### It is recommended to have INT attribute as the primary key. As MYSQL is fast when fetching records using INT attribute.
- The stackover flow answer for the question "Which datatype is preffered as a primary key for database" says that there is no benchmark for any particular type. All have same performance.
- However, there are many reasons to choose a INT type Primary key over string, reasons: Storage is less(8 Bytes for more than billion storage records), Does not have real meaning with the real world data which states that overtime this cannot be changed, Will always be unique in nature if we use UUID for 8 Bytes allowing good performance, And many other reasons are there.


## Foreign Keys
1. Each foreign key should refer to the primary key of the table that we want to have relationship.
2. There can be multiple foreign keys in the table, however the first condition for each foreign key should be satisfied.

```
CREATE TABLE table3 (
    id INT,
    customer_id INT,
    address VARCHAR(50),
    branch VARCHAR(50),
    PRIMARY KEY(id),
    FOREIGN KEY(cutomer_id) REFERENCES CUSTOMER(id)
);
```

1. Unique
- The properties of unique key are they can be null.
- The unique also behaves same as primary key with some differences like can be null, can be multiple unique keys.

2. CHECK
- Check is a constraint which is applied on the attribute with some conditions. Whenever we are inserting any record in the table, that constraint should be followed by that column.

3. DEFAULT
- Default is the constraint that is applied to the attribute when we want to initialize a attribute with a default value.
	
Remember to have NOT NULL Constraint for every attribute whenever we are using Unique, Check and Default.
	
```
UNIQUE
	CREATE TABLE TABLE1 (stud_id INT UNIQUE, stud_addr INT UNIQUE);
	
CHECK
	CREATE TABLE placement (
		placement_id INT PRIMARY KEY,
		stud_id INT NOT NULL,
		stud_college VARCHAR(50) NOT NULL,
		CONSTRAINT stud_college CHECK(stud_id == "IIT")
	);
```

Examples
```
CREATE TABLE customer (
    ID INT PRIMARY KEY NOT NULL,
    Name VARCHAR(50) NOT NULL,
    City VARCHAR(50) NOT NULL
);

CREATE TABLE contacts (
    ID INT PRIMARY KEY,
    Customer_Id INT,
    Customer_Info VARCHAR(50) NOT NULL,
    Type VARCHAR(50) NOT NULL,
    FOREIGN KEY(Customer_Id) REFERENCES customer(ID)
);

DESC customer;
DESC contacts;
```