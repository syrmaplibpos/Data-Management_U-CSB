# Database-Self-Study-Journey

Based on [The Complete Sql Bootcamp](https://concordia.udemy.com/course/the-complete-sql-bootcamp/)


## SQL Fundamentals 

SELECT column FROM table


* Distinct, no duplicate value in a column

SELECT DISTINCT column FROM table

to clarify which column applied to 

SELECT DISTINCT(column) FROM table


* COUNT, return number of row of column

SELECT COUNT(name) FROM table

SELECT COUNT(DISTINCT name) FROM table;

* WHERE, condition

SELECT name,choice FROM table WHERE name = 'David' AND choice = 'red'

* ORDER BY

SELECT comapny, name, sales FROM table ORDER BY company ASC, sales DESC

default ASC

multiple, the second column sorting **within duplicate entries** of the first column

* LIMIT, select certain limit number of row

SELECT * FROM payment 
ORDER BY payment_date DESC
LIMIT 5;


