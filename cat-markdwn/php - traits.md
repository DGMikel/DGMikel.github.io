# Traits

Los traits a diferencia de las interfaces estos permiten implementar en lasclases que los usan metodos normales y abstractos
losque significa que estosmetodos siguen las reglas que a cada uno atañe.

  1. Los metodos abstractos - no tendran código en su interior y seran forzosamente usados por las clases que usan el trait -
  2. Los metodos normales - deberán llevar un cuerpo de funcionamiento -
  3. La clase que usa el trait podrá heredar todo su funcionameinto del trait

```php
<?php 
trait MultiFuncion{

  // metodo normal
  public function libre($funcion){
    return "El numnero de función es: ".$funcion;
  }
  
  // metodo abstracto
  abstract function abstracto($abs);
}

class TestCpu{
  use MultiFuncion; // invocación del trait

  function start(){
    return "<span style='color:red'>ON</span>";
  }
  
  // metodo abstracto forzado a aparecer gracias al trait
  function abstracto($abs){
    return "El absoluto de $abs es: ". abs($abs);
  }
  
}

$cpu1 = new TestCpu();
echo $cpu1->start();
echo "<br>";

// aquí se invoca una función abstracta
// desde la clase - forzado a aparecer por el uso del trait
echo $cpu1->abstracto(-125);
echo "<br>";

// Aquí se invoca una función del Trait
// que no esta declarado en la clase
echo $cpu1->libre(2);
```
Teniendo como resultado:
```html
ON
El absoluto de -125 es 125
El numnero de función es: 2
```
