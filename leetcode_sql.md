584. Find Customer Referee

caution the NULL value, to detect, use IS NULL

183. Customers Who Never Order

Write an SQL query to report all customers who never order anything.

Using sub-query and NOT IN clause

select customers.name as 'Customers'
from customers
where customers.id not in
(
    select customerid from orders
);



