1. Filtering Clause : `WHERE`
	1. Where keyword will provide us the filter options on the tables. In case we want to query a certain options from our tables inside our database, we use where clause.
2. Operators
	1. AND
	2. OR
	3. NOT
3. Keywords
	1. IN
	2. NOT IN
	3. IS NULL
4. WildCards : Wildcards needs to be used with `LIKE` Keyword.
	1. % => To find 0 or more characters.
	2. _ => TO find only single occurence.
5. Sorting
	1. ORDER BY => If the ordering criteria is not provided, by default it is taken as ascending order.
	2. ORDER BY DESC => Descending order.

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

3. Use of IN and NOT IN

select
	*
from student
where
	branch_name in ('dom', 'mar', 'and');

4. Use of IS NULL

select
	*
from student
where
	branch_name IS NULL;

5. List out the complete name of all the students who enrolled in CS206 batch 2019 and sort them in ascending order according to their date of birth and lname. 

SELECT
    fname,lname
FROM
    Student
WHERE
    course='CS206'
    AND
    joining_Year=2019
ORDER BY
    DOB, lname;

6. Fetch out all the records but in descending order by ordering time and in case of similar order times sort in ascending order w.r.t. shipping time. 

SELECT
    *
FROM
    e_transactions
ORDER BY
    ordered_time DESC,
    shipping_time ASC;

7. List down the orders ids with their shipping time which were ordered before 30th June 2021 sort them in ascending order w.r.t. cost and in descending order w.r.t. time the purchase was made. 

SELECT
    order_id,shipping_time
FROM
    e_transactions
WHERE
    ordered_time < '2021-06-30'
ORDER BY
    cost ASC,
    ordered_time DESC;

8. List down all the details of the orders made in February 2021 or July 2021, also sort them in ascending order by their price.

SELECT * FROM e_transactions WHERE ordered_time like '%-02-%' OR ordered_time like '%-07-%' ORDER BY cost;
```