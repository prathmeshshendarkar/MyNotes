1. First and most important thing is to create a ER Model of your objective.


## Relational Databases
1. Terms: [Terms Link](https://www.upi.pr.it/docs/easfg/easvrfgp7.htm)
2. ![[Pasted image 20240801211513.png]]
3. A database is a storage of information in a structured manner.
4. A database has Tables of specific relations, for ex: We have users table or Products table.
5. Each table has Attributes or Fields that provides a feature to every row or record.
6. Each record in a table is also known as Tuples.

## Properties of a Table
1. Each column or attributes values should be unique.
2. There should not be multiple rows with same values so as to avoid redundancy.
3. The values in a tuple or row should be atomic. That means, they should only hold one data. The data should not be breakable. For ex, if one user has 2 Products in his cart, then we cannot have 2 Product Id in one row. That violates the law of DBMS and we should separate that column(Product ID) into another table.
4. If a particular column is given a specific domain, then it should only have values from that domain. For ex: If it is integer then only integer value is required.
5. The sequence of columns and row is insignificance(Does not matter).
6. Integrity Constraints
## More Terms
1. **Degree**: The Degree in a relational database means the number of columns that a table contains.
2. **Cardinality**: Cardinality is the number of records or tuples that exists at a particular database instance.
3. Example: For above image: Degree is 4 for user and 3 for Products. Cardinality at that particular instance is 3 for both the tables.
4. Cardinality changes as we insert or remove the records from the table.

## More Extra Terms
1. **Relational Keys**: Each row in a specific table has some relation like a user has a name, age and sex. These attributes has specific Keys that are assigned to them. These Keys are origin to a particular table or is linked to another table. Check : [[Relational Keys]]
2. **Attribute Domain**: Each attribute in a table has a constraint or domain associated to it. And that domain values should only be present in that column. For ex: If I have a attribute of age set to Integer which is the attribute Domain, then only integer values should be present in that column.
3. Integrity Constraints: The types of data that can be stored in a database is known as integrity constraints.
## Some More Terms
1. Projection
2. Restriction
3. Join