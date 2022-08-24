# OPERADOR DE TIPO DE INSTANCIA

La instrucción *instanceof* devolverá verdadero si un objeto es instancia de una clase determinada.

```php
// si tenemos lo siguiente:

class Clase_A{  }//                      <--- Clase_A 

$objeto = new Clase_A();//               <--- Instanciación de Clase_A

var_dump($objeto instanceof Clase_A);//  <--- devuleve bool(true)

```
