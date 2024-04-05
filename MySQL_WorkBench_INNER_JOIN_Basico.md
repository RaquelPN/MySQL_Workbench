```MYSQL
USE sakila;
-- INNER JOIN seleciona items de 2 ou mais tabelas 
-- ON serve para dar o match nas informações

SELECT 
	c.customer_id ,
	c.first_name,
	c.last_name,
	p.amount,
    p.rental_id
FROM customer c
	JOIN payment p ON c.customer_id = p.payment_id
    
```
