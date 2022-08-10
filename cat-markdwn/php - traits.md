# Traits

Trait permite el el uso de sus metodos en varias clases al mismo tiempo, parecido al la clase abstracta los traits se idefrencian por varios movitivos:

  1. Sedefinen con lasintaxis : trait NombreTrairt{ metodos - todos los metodos deben ser publicos - }
  2. Todas las clases que hagan uso de estos deben incorporar todos los metodos del trait
  3. No se permite que tengan más recursos que los metodos que estos contienen.

```php
<?php 
interface Sound{
  public function sound($sonido);
  public function efect($efecto);
}
//-------  Clase que implementa interface Sound -----------------
class Guitar implements Sound{
  public $typeSound;
  public $typeEfect;

  public function sound($sonido){
    $this->typeSound = $sonido;
    return "Su sonido es de: ".$this->typeSound;
  }

  public function efect($efecto){
    $this->typeEfect = $efecto;
    return "Su efecto es de: ".$this->typeEfect;
  }
  
}
//-----------------------------------------------------------------

//-------  Clase que implementa interface Sound -------------------
// Esta clase usa más funciones que las que implemnta la interface
class Violin implements Sound{
  public $typeSound;
  public $typeEfect;
  public $color;
  public $madera;
  
  function __construct($color, $madera){
    $this->color = $color;
    $this->madera = $madera;
  }

  public function mixData(){
    echo "El violin tiene el color: $this->color 
          y es de madera: $this->madera";
  }
  
  public function sound($sonido){
    $this->typeSound = $sonido;
    return "Su sonido es de: ".$this->typeSound;
  }

  public function efect($efecto){
    $this->typeEfect = $efecto;
    return "Su efecto es de: ".$this->typeEfect;
  }
  
}
//--------------------------------------------------------------------------------------

$guitarra = new Guitar();
$violin = new Violin("Cafe","Caoba");

echo $guitarra->sound("Cuerdas");
echo "<br>";
echo $guitarra->efect("Distorcionador");
echo "<br>";
echo $violin->sound("Cuerdas - con tilde");
echo "<br>";
echo $violin->efect("echo - delay");
echo "<br>";
echo $violin->mixData();
```
Teniendo como resultado:
```console
Su sonido es de: Cuerdas
Su efecto es de: Distorcionador
Su sonido es de: Cuerdas - con tilde
Su efecto es de: echo - delay
El violin tiene el color: Cafe y es de madera: Caoba
```
