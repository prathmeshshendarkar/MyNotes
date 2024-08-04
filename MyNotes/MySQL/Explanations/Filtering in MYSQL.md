1. Filtering Clause : `WHERE`
	1. Where keyword will provide us the filter options on the tables. In case we want to query a certain options from our tables inside our database, we use where clause.
2. Operators
	1. AND
	2. OR
	3. NOT

## Examples
```
1. WHERE and OR

select
	*
from
	category
where
	name = 'Action'
    or
    name = 'Animation';

2. use of BETWEEN and AND : We want to find the result from a sales_by_film_category table that should contain the sales between 0 and 4000
BETWEEN is used when we want to filter from only single column. We can also use conditional operators.

SELECT
	*
FROM
	sales_by_film_category
WHERE
	total_sales BETWEEN 0 AND 4000;


```