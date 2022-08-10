# Interfaces

Permiten especificar que metodos se deben implementar en una clase

  1. Las interfaces no tienen argumentos, solo los metodos
  2. Todos los metodos son publicos
  3. Todos los metodos son abstractos (No tienen fucnionalidad esta se establece en la clase que implementa)
  4. Pueden ser implementadas y heredadas. 

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
echo $violin->efect("eco - delay");
echo "<br>";
echo $violin->mixData();

```
Tiene por salida: 
```cmd
Su sonido es de: Cuerdas
Su efecto es de: Distorcionador
Su sonido es de: Cuerdas - con tilde
Su efecto es de: eco - delay
El violin tiene el color: Cafe y es de madera: Caoba
```
