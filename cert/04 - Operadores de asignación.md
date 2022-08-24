# OPERADIRES DE ASIGNACIÓN

Son utilizados para asignarle un valor a las variables 

```php

$a = 10;
// = le asigna el valor de 10 a la variable $a

```

 # OPERADORES DE ASIGNACIÓN COMBINADO
 
 Los Operadores de asignación combiando son +,- combinados con el operador =
 esta operación le sumará al valor de la variable que se le anteponga y asignará a la misma variable.
 De la misma forma si anteponemos un . al signo = con una variable con string este operador concatenará el string
 que le prosigue a la varbable que hace uso del .=
 
 ```php
 
 $a = 10;
 $a += 2;
  echo $a;  // El resultado es 12
 
$c = "hello world";
$c .= ", hello live!!";
echo $c; // salida hello world, hello live!!
  
 ```
 
 # OPERADOR DE AIGNACIÓN POR REFERENCIA
 
 Este operador asigna el valor de la variable al que se le antepone con cualquier cambio que esto conlleve.
 ( siempre esta observando dicha variable )
 
 ```php
 $a = 10;
 $b = &$a;
 
 echo "1. $a --- $b";
  
 $a = 21;
 
 echo "2. $a ---- $b";
 
 /* EL resultado es:
 
     1.  10 --- 10
     2.  21 ---- 21
 */
 
 ```
 
 
