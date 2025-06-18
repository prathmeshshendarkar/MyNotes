1. Super key : The key that can be formed by using multiple attributes or set of all the attributes is called super key.
2. Primary Key : Primary Key is a unique attribute (single or multiple) that can identify a tuple from a table
	1. Composite Key: Primary keys that consists of at least more than 2 attributes are known as composite key.
	2. Compound Key : Attributes that are foreign keys in another table. Now, From a table, there needs to be atleast 2 attributes which needs to be foreign keys in another table. 
	3. Surrogate Key : If a table has columns which cannot help us to find a tuple then we create a attribute which will contain unique values. These attribute is known as Surrogate Key.
3. Candidate Key : Candidate keys are set of attributes that can uniquely identify a tuple from a table. A table can have multiple candidate keys but it can only have one primary key.
4. Alternate Key: Those attributes other than primary key but comes under candidate key are known as Alternate key.
5. Foreign Key : The attributes from a table that can help us form a relation with another table will form a Foreign key. 

## Primary Key
1. Primary Key should be unique, non null value(0 is allowed it is not a null value).
2. The values in a primary key attribute should not be same.
3. Primary key values cannot be changed.