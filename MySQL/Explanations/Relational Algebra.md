## Relational Algebra
1. **Selection** : (Sigma Symbol) When we want to select a particular set of attritbutes or tuples from a table.
2. **Projection** : (Pi Symbol) When we want to project or show a selected set of attributes or tuples from a table. We can also use projection directly when we want to showcase full table. However, incase we want to specific features, then first selection and then projection.
3. **Union** : (U Symbol) When we want to find a set of unique records from multiple tables such that the duplicate records will only appear once and will contain all the records.(Sum)
4. **Intersection** : (n Symbol) When we want to find those Records that are common in multiple tables.
5. **Set Intersection** : (- Symbol) When we want to find only those records that exists in a particular table but does not exists in other tables. For ex: A-B Means Give me those records that exists in A and exclude those records that exists in B as well. Exists means have in common.
6. **Cartesian Product** : (X Symbol) When we want to create a table with all the permutations of multiple tables. For ex: AXB means I want a table which can map a particular record to all the set of records from table B. If we have 2x2 A and 2x2 B then final table will be 4x4 which will contain those records
7. Rename Operator : (p Symbol) When we want to rename a particular attribute.