## Properties of a Table
1. Each column or attributes values should be unique.
2. There should not be multiple rows with same values so as to avoid redundancy.
3. The values in a tuple or row should be atomic. That means, they should only hold one data. The data should not be breakable. For ex, if one user has 2 Products in his cart, then we cannot have 2 Product Id in one row. That violates the law of DBMS and we should separate that column(Product ID) into another table.
4. If a particular column is given a specific domain, then it should only have values from that domain. For ex: If it is integer then only integer value is required.
5. The sequence of columns and row is insignificance(Does not matter).
6. Integrity Constraints