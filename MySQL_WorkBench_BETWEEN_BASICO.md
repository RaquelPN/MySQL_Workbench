```MySQL

USE sakila;

-- BETWEEN   entre um valor e o outro . ex: utilizado para puxar uma range dentro de um inicio e um fim
-- ( pode usar AND  > OU < . PORÉM BETWEEN DEIXA O CODIGO MAIS LIMPO pois ELE INCLUI => e =< 


SELECT *
FROM Payment
WHERE amount BETWEEN 1.99 AND 3.99

```
