# Clases Abstractas

## Que son las clases y los metodos abstractos?

Las clases abstractas a diferencia de las clases normales estas no se pueden instanciar, o seá no puedes crear objetos a partir de ellas, por ejemplo e una clase normal podríamos hacer lo siguiente:

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
