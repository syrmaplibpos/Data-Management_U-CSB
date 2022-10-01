584. Find Customer Referee

caution the NULL value, to detect, use IS NULL


183. Customers Who Never Order

Write an SQL query to report all customers who never order anything.

**sub-query**

use WHERE to subquery and quote that result to in the main query

**NOT IN**

Using sub-query and NOT IN clause

SELECT customers.name AS 'Customers'
FROM customers
WHERE customers.id NOT IN
(
    SELECT customerid FROM orders
);


1873. Calculate Special Bonus

*CASE WHEN*

CASE WHEN
    THEN
ELSE
    END

use it like if else

**AS**

AS alias name, only exist in current query, use "" if their is a space in the name


select employee_id,(case 
 when employee_id %2 !=0 AND name NOT LIKE'M%' 
			  THEN salary
 ELSE 0 END
			 ) AS bonus 
			 FROM Employees 
			 ORDER BY employee_id ;


