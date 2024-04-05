```MySQL

--- AND | NOT | OR | OR NOT | AND NOT 

 SELECT * FROM customer
 WHERE store_id = 1 AND  active = 0
```
```MySQL
SELECT * FROM payment
 WHERE staff_id = 1 OR amount = 0.99 AND customer_id < 10

```
```MySQL
 SELECT * FROM payment
WHERE NOT staff_id = 1 AND amount = 0.99 AND customer_id < 10

```
```MySQL
 SELECT * FROM payment
 WHERE NOT staff_id = 1 AND NOT amount = 0.99 AND customer_id < 10 -- amount != 0.99  outra forma NOT

```
