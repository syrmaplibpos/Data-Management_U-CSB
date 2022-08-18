# Data-Management-Self-Study-Journey

Based on The Complete Sql Bootcamp on Udemy


- [Data-Management-Self-Study-Journey](#data-management-self-study-journey)
  - [SQL Fundamentals](#sql-fundamentals)
    - [Distinct, no duplicate value in a column](#distinct-no-duplicate-value-in-a-column)
    - [COUNT, return number of row of column](#count-return-number-of-row-of-column)
    - [WHERE, condition](#where-condition)
    - [ORDER BY](#order-by)
    - [LIMIT, select certain limit number of row](#limit-select-certain-limit-number-of-row)
    - [BETWEEN, NOT BETWEEN](#between-not-between)
    - [IN, NOT IN](#in-not-in)
    - [LIKE and ILIKE](#like-and-ilike)


## SQL Fundamentals 

SELECT column FROM table


### Distinct, no duplicate value in a column

SELECT DISTINCT column FROM table

to clarify which column applied to 

SELECT DISTINCT(column) FROM table


### COUNT, return number of row of column

SELECT COUNT(name) FROM table

SELECT COUNT(DISTINCT name) FROM table;

### WHERE, condition

SELECT name,choice FROM table WHERE name = 'David' AND choice = 'red'

### ORDER BY

SELECT comapny, name, sales FROM table ORDER BY company ASC, sales DESC

default ASC

multiple, the second column sorting **within duplicate entries** of the first column

### LIMIT, select certain limit number of row

SELECT * FROM payment 
ORDER BY payment_date DESC
LIMIT 5;


### BETWEEN, NOT BETWEEN

the same as

value >= low AND value <= high
value BETWEEN low AND high

include boundary

value < low OR value > high
value NOT BETWEEN low AND high

dates
YYYY-MM-DD

BETWEEN 2000-02-18 AND 2000-02-20
include any time between 02-18 00:00:00 and 02-20 00:00:00

### IN, NOT IN

include or not include the ( , , )

### LIKE and ILIKE

LIKE is case-sensitive, ILIKE is case-insensitive

using pattern matching

replace the rest with %

all names that begin with an 'A' or end with 'a'

WHERE name LIKE 'A%'

WHERE name LIKE '%a'

replace just a single character with underscore _

get all Mission Impossible Films

WHERE title LIKE 'Mission Impossible _'

Can use multiple underscores 

WHERE value LIKE 'version#__'

