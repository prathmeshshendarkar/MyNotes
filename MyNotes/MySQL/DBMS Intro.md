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
3. Integrity Constraints: The types of data that can be stored in a database is known as integrity constraints. Check: [[Integrity Constraints]]
## Some More Terms
1. Projection : Project a set from the table.
2. Restriction
3. Join

Relational Algebra
1. **Selection** : (Sigma Symbol) When we want to select a particular set of attritbutes or tuples from a table.
2. **Projection** : (Pi Symbol) When we want to project or show a selected set of attributes or tuples from a table. We can also use projection directly when we want to showcase full table. However, incase we want to specific features, then first selection and then projection.
3. **Union** : (U Symbol) When we want to find a set of unique records from multiple tables such that the duplicate records will only appear once and will contain all the records.(Sum)
4. **Intersection** : (n Symbol) When we want to find those Records that are common in multiple tables.
5. **Set Intersection** : (- Symbol) When we want to find only those records that exists in a particular table but does not exists in other tables. For ex: A-B Means Give me those records that exists in A and exclude those records that exists in B as well. Exists means have in common.
6. **Cartesian Product** : (X Symbol) When we want to create a table with all the permutations of multiple tables. For ex: AXB means I want a table which can map a particular record to all the set of records from table B. If we have 2x2 A and 2x2 B then final table will be 4x4 which will contain those records
7. Rename Operator : (p Symbol) When we want to rename a particular attribute.