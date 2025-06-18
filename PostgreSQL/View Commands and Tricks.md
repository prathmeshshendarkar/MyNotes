## To view in which database am I connected to?
- select current_database();
- \c
- check the terminal after you are connected to database, in the left hand side.

## To view all the tables and sequences inside of our database below commands
- \d

## To just view all the tables and not the sequences.
- \dt
```
- SELECT table_name FROM information_schema."tables" WHERE table_schema = 'public';
```

## Data sorting
- ORDER BY  DESCENDING: `SELECT * FROM test_table_2 ORDER BY lname DESC;`

## Distinct Data
- The below query will give me count of distinct lname data from the table where column is lname.
```
SELECT COUNT(*) FROM (SELECT DISTINCT lname FROM test_table_2 ORDER BY lname DESC);
```

## WHERE clause
- Filter the data based on certain criteria.
```
- SELECT * FROM test_table_2 WHERE fname='Prathmesh' AND (lname='S' OR lname='A');
```

## Comparison Operators
- < less than
- > greater than
- <> not equal to
- = equal to

## Limit
- For selecting specific set of records from table
```
SELECT * FROM test_table_2 LIMIT 10;
```

## Offset
- For selecting records after a certain record(offset)
```
SELECT * FROM test_table_2 OFFSET 5 LIMIT 10;
```

## IN Keyword
- For selecting records in array of values.

```
SELECT * FROM test_table_2 WHERE id IN (1, 2, 3);
```

## BETWEEN keyword
- For selecting records in between some values
```
SELECT * FROM test_table_2 WHERE id BETWEEN 1 AND 10;
```

## LIKE keyword
- % means any keyword 
```
SELECT * FROM test_table_2 WHERE fname LIKE 'P%';
```
- _ means single character 
```
SELECT * FROM test_table_2 WHERE fname LIKE 'P__t%';
```

## ILIKE keyword
- ILIKE will ignore the case sensitive nature.

## GROUP BY and HAVING keyword
```
SELECT fname , COUNT(*) FROM test_table_2 GROUP BY fname HAVING fname='Prathmesh';
```

## Aggregate Functions
- COUNT
- MIN
- MAX
- SUM
- AVG
- ... MANY MORE OPERATIONS ARE THERE.
`SELECT make, model, MIN(price) AS price FROM car GROUP BY make,model HAVING price >= 100000;`

## Arithmetic Operators

+, - , *, !(Fibo) , /

## Alias : AS
The above keyword renames a particular column to some other alias name.

## Coalesce
In case some values are not present in the column, we can then use the above keyword to check if the value is present or not. It will get the first value from the row, if any particular value is not present.

We can change the values inside those column where values are not present to some default value using coalesce.

`SELECT COALESCE(email, 'Email not provided') FROM users;`

## NULLIF
This keyword will return NULL if both the values inside him are same. If they are not same then it will return 1st value.

Eg: `SELECT COALESCE (10 / NULLIF(0,0), 0)`

Since 10/0 is error, but 10/NULL is not an error. So NULLIF will provide output as NULL which will handle our errors.

## Normal Functions
- NOW()
- DATE()
- EXTRACT()
- AGE()