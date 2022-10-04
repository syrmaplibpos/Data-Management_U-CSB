584. Find Customer Referee

caution the NULL value, to detect, use IS NULL


183. Customers Who Never Order

Write an SQL query to report all customers who never order anything.

**sub-query**

use WHERE to subquery and quote that result to in the main query

**NOT IN**

Using sub-query and NOT IN clause

```
SELECT customers.name AS 'Customers'
FROM customers
WHERE customers.id NOT IN
(
    SELECT customerid FROM orders
);
```

1873. Calculate Special Bonus

*CASE WHEN*

```
CASE WHEN
    THEN
ELSE
    END

CASE WHEN condition THEN result
     [WHEN ...]
     [ELSE result]
END
```

use it like if else

**AS**

AS alias name, only exist in current query, use "" if their is a space in the name

```
SELECT employee_id,(CASE 
 WHEN employee_id %2 !=0 AND name NOT LIKE'M%' 
			  THEN salary
 ELSE 0 END
			 ) AS bonus 
			 FROM Employees 
			 ORDER BY employee_id ;
```

627. Swap Salary

Write an SQL query to swap all 'f' and 'm' values (i.e., change all 'f' values to 'm' and vice versa) with a single update statement and no intermediate temporary tables.

Note that you must write a single update statement, do not write any select statement for this problem.

**IF(condition_1, operation, else_operation)**

UPDATE salary set sex = if(sex = 'm','f','m');

**CASE WHEN condition THEN result [WHEN ...][ELSE result]END**

UPDATE salary SET sex = CASE sex WHEN 'm' THEN 'f' ELSE 'm' END;


196. Delete Duplicate Emails

Write an SQL query to delete all the duplicate emails, keeping only one unique email with the smallest id. Note that you are supposed to write a DELETE statement and not a SELECT one.

After running your script, the answer shown is the Person table. The driver will first compile and run your piece of code and then show the Person table. The final order of the Person table does not matter.

```
DELETE p1 FROM Person p1,
    Person p2
WHERE
    p1.Email = p2.Email AND p1.Id > p2.Id

SELECT p1.*
FROM Person p1,
    Person p2
WHERE
    p1.Email = p2.Email
;

SELECT p1.*
FROM Person p1,
    Person p2
WHERE
    p1.Email = p2.Email AND p1.Id > p2.Id
;
```

**UPDATE**

```
UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition;
```

**DELETE**

```
DELETE FROM table_name WHERE condition;
```


196. Delete Duplicate Emails

Write an SQL query to delete all the duplicate emails, keeping only one unique email with the smallest id. Note that you are supposed to write a DELETE statement and not a SELECT one.

After running your script, the answer shown is the Person table. The driver will first compile and run your piece of code and then show the Person table. The final order of the Person table does not matter.

```
DELETE p1 FROM Person p1,
    Person p2
WHERE
    p1.Email = p2.Email AND p1.Id > p2.Id
```


**self join**


**SUBSTRING**


`SUBSTRING(string, start, length)`

string	Required. The string to extract from

start	Required. The start position. The first position in string is 1

length	Required. The number of characters to extract. Must be a positive number


**SUBSTR**

`SUBSTR(string, start, length)`

```
SELECT Users.user_id , CONCAT(UPPER(SUBSTR(Users.name,1,1)),LOWER(SUBSTR(Users.name,2))) AS name 
FROM Users
ORDER BY
Users.user_id ASC
```

SUBSTR(Users.name,1,1)

extract from the string starting from position 1 and the length of the extracted one is 1

SUBSTR(Users.name,2)

extract from the string starting from position 2 and the length of the extracted one is to the end

**CONCAT**

```
CONCAT(A,B)
concat two strings A+B
```

