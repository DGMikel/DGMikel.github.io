Herencia

La herencia es la capacidad de extender los recursos publicos y protegidos (public y protected) a otras clases llamadas hijas para que estas puedan hacer uso de estos recursos.

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
// Esta clase será llamada hija y extiende de Vehiculo (Extends)
class Moto extends Vehiculo{
  public $matricula;

  
  function set_nombre(){
    return "<br>Tipo: Moto";
  }
  
  function set_placa($placa){
    $this->matricula = $placa;
    return "<br>La placa es: ".$this->matricula;    
  }
}

$moto = new Moto(2, "RTX-200"); // Inicio del objeto Moto que hereda de Vehiculo

echo $moto->get_data();   // funcion propia de la clase Vehiculo
echo $moto->set_nombre(); // funcion propia de la clase Moto
echo $moto->set_placa("CDMX-987"); // funcion propia de la clase Moto
```
tiene por salida:

```cmd
Los datos de este vehiculo es:
Tipo: RTX-200
No de llantas: 2
Tipo: Moto
La placa es: CDMX-987
```
