# OPERADORES DE COMPARACIÓN

Se usan para hacer comparaciones (MAYOR, MENOR, IGUAL. IDENTICO) etc.

    1. < MENOR que.                           6. <=   MENOR e IGUAL que. 
    2. > MAYOR que.                           7. >=   MAYOR e IGUAL que.
    3. ==   IGUAL que.                        8. !=   DISNTO que.
    4. ===  IGUAL y del mismo TIPO que        9. !==  DISTINTO hasta del TIPO
    5. <>   DISTINTO                         10. A??B SI A no existe o es NULL  entra B


```php

$a = 10;
$b = 5;

//  MAYOR que:
echo ($a > $b)?'MAYOR':'MENOR';   // SALIDA MAYOR

echo "<br>";

//  MENOR que:
echo ($a < $b)?'MAYOR'?'MENOR';   // SALIDA MENOR

echo "<br>";

//  IUGAL que:
echo ($a == $b)?'IGUAL'?'NO IGUAL';   // SALIDA NO IGUAL

echo "<br>";

//  ?? opcion:
echo $x ?? $b?    // SALIDA 5 


```

