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

-- *	Corresponde a zero ou mais instâncias da String anterior
-- +	Corresponde a uma ou mais instâncias da String anterior
-- .	Corresponde a qualquer caractere único
-- ?	Corresponde a zero ou uma instância das Strings anteriores
-- ^	^ corresponde ao início de uma String
-- $	$ corresponde ao final de uma String
-- [abc]	Corresponde a qualquer caractere listado entre colchetes
-- [^abc]	Corresponde a qualquer caractere não listado entre colchetes
-- [AZ]	Corresponde a qualquer letra maiúscula
-- [az]	Corresponde a qualquer letra minúscula
-- [0-9]	Corresponde a qualquer dígito entre 0-9
-- [[:<:]]	Corresponde ao início das palavras
-- [[:>:]]	Corresponde ao final das palavras
-- [:aula:]	Corresponde a qualquer classe de personagem
-- p1|p2|p3	Matemática qualquer um dos padrões especificados
-- {n}	Corresponde a n instâncias do elemento anterior
-- {m,n}	Corresponde de m a ninstâncias do elemento anterior

Corresponder à String especificada
1
SELECT * FROM `learnerdetails` WHERE `course_name` REGEXP 'SQL';
Corresponder ao início da string(^23)
1
SELECT * FROM `learnerdetails` WHERE `course_Id` REGEXP '^23';
Corresponde a zero ou uma instância das strings anteriores(Ja?)
1
SELECT * FROM learnerdetails WHERE course_name REGEXP 'Ja?';
Corresponde a qualquer um dos padrões 'w|ja'
1
SELECT learner_name FROM learnerdetails WHERE course_name REGEXP 'w|ja' ;
Corresponder ao final de uma string (yahoo.com $)
1
SELECT learner_name FROM learnerdetails WHERE learner_email REGEXP 'yahoo.com$';

```
