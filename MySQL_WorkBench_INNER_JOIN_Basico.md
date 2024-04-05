```MYSQL
USE sakila;
-- INNER JOIN seleciona items de 2 ou mais tabelas 
-- ON serve para dar o match nas informações

SELECT 
	customer.customer_id ,
	customer.first_name,
	customer.last_name,
	payment.amount,
    payment.rental_id
FROM customer 
	JOIN payment ON customer.customer_id = payment.payment_id
```
