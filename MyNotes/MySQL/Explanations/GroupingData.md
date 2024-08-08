# Lets start grouping the data

## Commands
1. GROUP BY
    - Group By Command helps us to group the records from the column into single category of records.
2. DISTINCT
    - The distinct function works the same way as Group by function.
3. HAVING
	1. The having keyword behaves similar to WHERE Clause. The main difference is having does not work on row data it only works for grouped data. Similarly. WHERE Does not work for group data, only works for row data.

## Aggregate Functions
1. COUNT
2. SUM
3. MAX
4. MIN
5. AVG
![[Pasted image 20240805220422.png]]

## Examples
```
1. Write an SQL query to find different years in which the employees join after the year 2010. 

SELECT
    year_of_joining
FROM
    Employee
WHERE
    year_of_joining > 2010
GROUP BY
    year_of_joining;

2. List out the total number of orders made to each address. 
    
SELECT
    Address , SUM(TotalOrdersYet)
FROM
    Customer
GROUP BY
    Address;

3. List out the maximum number of orders made from a particular Pincode. 

SELECT
    Pincode, MAX(TotalOrdersYet)
FROM
    Customer
GROUP BY
    Pincode;

4. List the cities in descending order of the number of customers residing in them.
Note: Name the number of customers residing in them as "Number" using Alias Keyword.

SELECT
    City, COUNT(cust_id) AS Number
FROM
    Customer
GROUP BY
    City
ORDER BY
    Number DESC;

5. List down all the addresses from Jalandhar city with the number of times the address appears.
Note: Name the number of times the address appears as "Address_times" using Alias Keyword

SELECT
    Address, COUNT(Address) AS Address_times
FROM
    Customer
WHERE
    City='Jalandhar'
GROUP BY
    Address;

6. List down the addresses with the city and the pincode which appear more than twice in the table.

SELECT
    Address,city,pincode
FROM
    Customer
GROUP BY
    Address,city,pincode
HAVING
    COUNT(CITY) > 2;

7. For All the Analyst jobs list down the maximum salaries offered to them in different departments and under different managers, list all the details in ascending order based on the combined salary given out by that department.

![[Pasted image 20240806093559.png]]

SELECT
    Job,DeptCode,Manager, MAX(Salary)
FROM
    Employee_data
WHERE
    Job='ANALYST'
GROUP BY
    Job,DeptCode,Manager
ORDER BY
    MAX(Salary);
```