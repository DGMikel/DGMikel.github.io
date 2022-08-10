# Metodos estaticos (statics)

Los metodos estaticos se pueden invocar sin instanciar la clase que los contiene.

```php
<?php

class Convertidor{
  
  public static function dollar($dinero){
      return $dinero * 20.51;
  }
  public static function rublo($dinero){
    return $dinero * 0.50;
  }
  public static function yen(){
    return $dinero * 0.5;
  }
  public static function euro($dinero){
    return $dinero * 21.80; 
  }
}

$dinero = 130;
// Convertidor::dollar <- desde la clase sin estanciar
echo "Dolar: ".Convertidor::dollar($dinero);
echo "<br>";
// Convertidor::rublo <- desde la clase sin estanciar
echo "Rublo: ".Convertidor::rublo($dinero);
echo "<br>";
// Convertidor::yen <- desde la clase sin estanciar
echo "Yen: ".Convertidor::yen($dinero);
echo "<br>";
// Convertidor::euro <- desde la clase sin estanciar
echo "Euro: ".Convertidor::euro($dinero);

```
Y el resultado de esta función sera:

```bash
Dolar: 2666.3
Rublo: 65
Yen: 0
Euro: 2834
```
