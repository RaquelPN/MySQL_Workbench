```Mysql
-- Retirar 10% do valor de uma coluna , criando uma coluna que não está e nem será inserida no banco de dados

USE sakila;

SELECT 
	customer_id,
	amount,
  amount - (amount * 0.10) as 'discont'
FROM payment
WHERE customer_id = 1
 ```
