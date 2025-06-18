1. Major Categories Data Types are String, Numeric, Date , Boolean(Derived from Int)
2. Advanced Category Data Types are Spatial Datatype and JSON Datatype

## Numeric Datatype
1. TINYINT (1 Byte)
	1. 1 Byte means 8 bits which means we can store upto (2^8 - 1) (-255 to 255) 
2. SMALLINT (2 Byte)
3. MEDIUMINT (3 Byte)
4. INT (4 Byte)
5. BIGINT (8 Byte)
6. DECIMAL : Decimal Datatype can be stored in point values. So Before point is called precision that is the integer and after point is scale. So if we had 5000.05 then Precision would 4 and Scale would be 2 . So we have DECIMAL(4, 2). We can increase the scale value and store that much in table.
7. FLOAT
8. DOUBLE
9. BIT
	1. The BIT Datatype can store values in 1 and 0's
	2. Whenever we want to store any bit related information in a particular attribute we need to use b'1' or B'1' specification. The b or B character should be present with the single quotes defining the bit information.
	3. BIT Can store 1-64 bits of information.
10. If we want to have specific SIGN for a Numeric data type in a column it is by default present for all numeric data type except for BIT . However, if we want to restrict a user to only use unsigned data type which means only positive, then we need to mention that constraint to the attribute while creating table. For ex : `CREATE TABLE (COLUMN1 INT , COLUMN2 INT UNSIGNED);`

## Date Data type
1. DATE 
	1. Format for inserting data is `YYYY-MM-DD` 
	2. It occupies 3 Bytes of data
	3. Range for date data type is from `1000-01-01 to 9999-12-31`
2. TIME
	1. Format for inserting data is `HH:MM:SS`
	2. It also occupies 3 Bytes of data
	3. Range for time is from `-838:59:59` to `838:59:59`
3. DATETIME
	1. Format for inserting data is `YYYY-MM-DD HH:MM:SS`
	2. It occupies 5 Bytes of data
	3. Range: `1000-01-01 00:00:00` to `9999-12-31 23:59:59`
4. TIMESTAMP
	1. Format for inserting data is `YYYY-MM-DD HH:MM:SS`
	2. It occupies 4 Bytes of data
	3. Range: `1970-01-01 00:00:01` UTC to `2038-01-19 03:14:07` UTC
	4. It is best useful when we want to add the timestamp during the changes that happened.
5. YEAR
	1. Format is `YYYY`

## String Data Type
1. CHAR
	1. The default values for string data type are fixed. We can only have a fixed length.
	2. If we want to have dynamic values inserted then use `VARCHAR` 
2. BINARY
	1. Dynamic Values: `VARBINARY`
3. BLOB
	1. Binary Large Object (BLOB) is when we want to store large amount of binary data in database.
	2. Dynamic values: `TINYBLOB , MEDIUMBLOB , LONGBLOB`
4. TEXT
	1. Dynamic Values: `MEDIUMTEXT , LONGTEXT`

## Boolean Data Type
1. Derived from TINYINT Data Type
2. `CREATE TABLE sample1 (trans_status BOOLEAN);`
3. The typical range is `-127 to 127`

## Advanced Data Types
1. Spatial Data Type
2. JSON