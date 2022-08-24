# OPERADORES LÓGICOS

funcionando como las compuertas lógicas AND, OR, NOT etc, estos operadores toman el valor que retornan las variables
para hacer operaciones lógicas.

|Operador |Nombre|
|:--------|:-------|
|and      | AND|
|or       | OR|
|xor      | OR(EXCLUSIVO)|
|!        | NOT|
|&&       | OR (INCLUSIVO)|
|\|\|     |OR|

```php

$a = true;
$b = true;
$c = false;

echo "a = true<br>
      b = true<br>
      c = false<br>";

echo "OPERADORES AND y && con a y b<br>";
echo "AND = ";      var_dump($a and $b);
echo "<br>";
echo "&nbsp;&& = "; var_dump($a && $b);

echo "<br>";
echo "<br>";

echo "OPERADORES OR y || con a y c<br>";
echo "OR = ";      var_dump($a or $c);
echo "<br>";
echo "|| = "; var_dump($a || $c);


echo "<br>";
echo "<br>";

echo "OPERADOR ! Not aplicado a c<br>";
echo "! = "; var_dump(!$c);

/* SALIDA

a = true
b = true
c = false
OPERADORES AND y && con a y b
AND = bool(true)
 && = bool(true)

OPERADORES OR y || con a y c
OR = bool(true)
|| = bool(true)

OPERADOR ! Not aplicado a c
! = bool(true)


*/

```
