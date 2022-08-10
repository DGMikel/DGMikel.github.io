# Clases Abstractas

## Que son las clases abstractas?

Las clases abstractas a diferencia de las clases normales estas no se pueden instanciar, o seá no se pueden crear objetos a partir de ellas, por ejemplo en una clase normal podríamos hacer lo siguiente:

```php

<?php
// Esta clase será llamda padre
class Vehiculo{
  public $llantas;
  public $tipo;
  
  function __construct($no_llantas, $tipo_car){
  
    $this->llantas = $no_llantas;
    $this->tipo = $tipo_car;
  }
  
  function get_data(){
  return "Los datos de este vehiculo es: <br> Tipo: ".$this->tipo."<br>No de llantas: ".$this->llantas; 
  }
}

$vehiculo = new Vehiculo(4, "tsuru");
echo $vehiculo->get_data(); 

```
Pues en una clase abstracta no se puede hacer esto, su función es obligar a las clases que heredan de ella a seguir un comportamiento estbalecido por ellas.
aquí el resultado de instanciar un clase abstracta:

```php

abstract class VehiculoAbstracto{
  public $matricula;
  public $color;
  
  function set_color($color){
    return "El color es $color";
  }
  
  abstract function set_cilindro($cilindros);

}

$vehiculo = new VehiculoAbstracto();
$vehiculo->set_color("RED");


```
Teniendo por salida:
```cmd
Fatal error: Uncaught Error: Cannot instantiate abstract class VehiculoAbstracto
```

Para un funcionamineto correcto se tendrá que implementar de la siguiente manera:

```php

// Clase que no se puede instanciar solo heredar
abstract class VehiculoAbstracto{
  public $matricula;
  public $color;
  
  function set_color($color){
    return "El color es $color";
  }
  
  // metodo abstracto obligado a aparecer en clases que extiende
  abstract function set_cilindro($cilindros);

}

// clase que hereda de la clase abstracta
class Auto extends VehiculoAbstracto{
  public $ciudad;
  public $tenecia;
  
  function __constrcut($ciudad, $tenencia){
      $this->ciudad = $ciudad;
      $this->tenencia = $tenencia;
  }
  
  // función que es obligado desde la clase abstracta
  function set_cilindro($cilindros){
    return "El auto tienen $cilindros";
  }
  function get_informe(){
    return "El informe muestra todo en regla";
  }
}

$auto = new Auto("CDMX", "2022");
echo $auto->set_color("RED");
echo "<br>";
echo $auto->set_cilindro(12); // abstracto
```
Teniendo por resultado:
```cmd
El color es RED
El auto tienen 12

```
Entonces se sigue un flujo de trabajo de la siguiente forma:
```cmd
Clase abstracta => clase extiende => objeto que implementa de la clase que extiende 
                                     (con datos que obligadamente debe de contener de la clase abstracta)
```
