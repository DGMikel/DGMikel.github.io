#OPERADORES DE INCREMENTO DECREMENTO

los simbolos ++ ó -- sumará o restará una unidad a la variable que las usen.
lo que cambia es el orden de usma y retorno de resultado. 

++$var  : sumará a $var uno y devolverá el valor de $var
$var++  : devolverá el valor de $var y despues le sumará uno.

--$var  : restará a $var uno y devolverá el valor de $var
$var--  : devolverá el valor de $var y despues le restará uno.

```php

$a = 10;
echo "Retornará 10: ".$a++; // notese ++
echo "<br>";
echo "El valor final: ".$a; // ya se aplico el operador ++

/* SALIDA
    Retornará 10: 10
    El valor final: 11
*/
```
