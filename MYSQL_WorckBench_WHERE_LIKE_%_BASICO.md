```MYSQL
USE sakila;
-- LIKE (parecido como, contenha)
```
```MYSQL

 SELECT *
 FROM actor
 wHERE first_name LIKE 'penelope'
```

```MYSQL
-- Colocando o % podemos definir letras tanto no começo quanto no final ex:

 SELECT *
FROM actor
wHERE first_name LIKE 'AL%'   -- nome começa com AL


SELECT *
FROM actor
wHERE first_name LIKE '%o'  -- nome finaliza com O

```MYSQL
Cada padrão define um conjunto de cadeias de caracteres.
A expressão LIKE retorna verdade se a cadeia_de_caracteres estiver contida no conjunto de cadeias de caracteres
representado pelo padrão; como esperado,
a expressão NOT LIKE retorna falso quando LIKE retorna verdade, e vice-versa, e a expressão equivalente é NOT.

(cadeia_de_caracteres LIKE padrão).

Quando o padrão não contém os caracteres percentagem ou sublinhado,
o padrão representa apenas a própria cadeia de caracteres;
neste caso LIKE atua como o operador igual.
No padrão o caractere sublinhado (_) representa (corresponde a)qualquer um único caractere;
o caractere percentagem (%) corresponde a qualquer cadeia com zero ou mais caracteres.

Alguns exemplos:

'abc' LIKE 'abc'    verdade
'abc' LIKE 'a%'     verdade
'abc' LIKE '_b_'    verdade
'abc' LIKE 'c'      falso

A correspondência com padrão LIKE sempre abrange toda a cadeia de caracteres.
Para haver correspondência com o padrão em qualquer posição da cadeia de caracteres,
o padrão deve começar e terminar pelo caractere percentagem %.

Para corresponder ao próprio caractere sublinhado ou percentagem, sem corresponder a
 outros caracteres, estes caracteres devem ser precedidos pelo caractere de escape no padrão.

O caractere de escape padrão é a contrabarra, mas pode ser definido um outro caractere através
da cláusula ESCAPE. Para corresponder ao próprio caractere de escape, devem ser escritos dois caracteres de escape.

Deve ser observado que a contrabarra também possui significado especial
nos literais cadeias de caracteres e,
portanto, para escrever em uma constante um padrão contendo uma
contrabarra devem ser escritas duas contrabarras no comando SQL.

 Assim sendo, para escrever um padrão que corresponda ao literal contrabarra é necessário escrever
 quatro contrabarras no comando,
o que pode ser evitado escolhendo um caractere de escape diferente na cláusula ESCAPE;
assim a contrabarra deixa de ser um caractere especial
para o LIKE (Mas continua sendo especial para o analisador de literais cadeias de caracteres e,
por isso, continuam sendo necessárias duas contrabarras).

```
