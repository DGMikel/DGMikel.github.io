# OPERADORES BIT A BIT

Estos operadores aplican la logíca de 4 compuertas logias a cada uno de los bits de las variables y valores que conofrman los programas
AND, OR, NOT & XOR, además de manipular el sitio de ubicación de estos bits.

  1. & AND
  2. | OR
  3. ~ NOT
  4. ^ XOR



```php
/*
      Decimal  binario
      6        110
      5        101 
*/

$a = 6;
$b = 5;


echo "6 = 110<br>5 = 101<br>S = 100<br>";
echo "AND == ".($a & $b)."<br>";
/* SALIDA

        6 = 110
        5 = 101
        S = 100
        AND == 4
*/




echo "<br>";

echo "6 = 110<br>5 = 101<br>S = 111<br>";
echo "OR == ".($a | $b)."<br>";
/* SALIDA
        6 = 110
        5 = 101
        S = 111
        OR == 7
*/



echo "<br>";

echo "6 = 110<br>5 = 101<br>S = 011<br>";
echo "XOR == ".($a ^ $b)."<br>";

/* SALIDA
        6 = 110
        5 = 101
        S = 011
        XOR == 3
*/
echo "<br>";

$bin = 2;
$notbin = ~$bin;

echo decbin($bin)."<br>".decbin($notbin);

/* SALIDA
0000000000000000000000000000000000000000000000000000000000000010  (2)
1111111111111111111111111111111111111111111111111111111111111101  (-2)
*/
```

Se pueden recorrer de espacios los bit que conformen los valores de cada uno de ellos.

```php
$espacios = 2;
$valor = 40;
$nuevo_derecha   = $valor>>$espacios;
$nuevo_izquierda = $valor<<$espacios;

echo "DEC - Binario - &nbsp;&nbsp;Espacios a recorrer<br> 40  - &nbsp;&nbsp;&nbsp;101000&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2";
echo "<br>";
echo "$nuevo_izquierda - &nbsp;10100000 - << (izquierda 2)";
echo "<br>";
echo "0$nuevo_derecha - &nbsp;00001010 - >> (derecha 2)";

/* SADLIDA
            DEC - Binario -   Espacios a recorrer
             40 -    101000      2
            160 -  10100000 - << (izquierda 2)
            010 -  00001010 - >> (derecha 2)
*/


```


