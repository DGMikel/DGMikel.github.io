## Constructor

El constructor permite incializar propiedades de los objetos una vez creados.

```php
class Vehiculo{
  public $nombreV;
  public $no_llantas;

  function __construct($nombre, $llantas){
    $this->nombreV = $nombre;
    $this->no_llantas = $llantas;
  }

  function data_out(){
     $out = "Tipo de vehiculo: ".$this->nombreV."<br> Numero de llantas ".$this->no_llantas;   
     return $out;  
  }
}

$carro = new Vehiculo("Bocho",4);

echo $carro->data_out();
```

tendrá por salida: 
```cmd
Tipo de vehiculo: Bocho
Numero de llantas 4
```
