```MYSQL

USE sakila;
-- REGEXP  Expressões regulares 

-- EX: ^ puxar todo primeiro nome que começa com  a letra "a"
 SELECT *
FROM actor
WHERE first_name REGEXP '^A' 

-- EX: |(pipe) puxar todo primeiro nome que começa com  a letra "a" e CONTÉM  "B" 
SELECT *
FROM actor
WHERE first_name REGEXP '^a|b' 

-- EX: |(pipe) puxar todo primeiro nome que começa com  a letra "a" e começa com  "B" 
SELECT *
FROM actor
WHERE first_name REGEXP '^a|^b' 

-- EX: Filtrar uma REGEXP que o a contenha antes um g ou e ou r
-- independente da posição  contenha combiações GA e EA e RA
SELECT *
FROM actor
WHERE first_name REGEXP '[ger]a' 

-- inicie com a  posição que  contenha combiações GA e EA e RA
SELECT *
FROM actor
WHERE first_name REGEXP '^[ger]a' 

```
