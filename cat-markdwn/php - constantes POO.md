# Constantes (POO)

Una constante es una variable que no puede ser modificada y se encuentra dentro de una clase

Las constantes van en mayusculas y su sintaxis es la siguiente:

```php
  // constante Global
  define("CONSTANTE","ValorDeConstante"); 
  
  // constante dentro de la clase
  const NOMBRE_CONST = "Valor que se le da a la constante";
```

```php
<?php
// constatnte Global
define("MONEDA","Dolares");

class Contador{
  // constantes de clase
  const CANTIDAD = "Miles de millones ha contado";
  const TIME = "Por muchos años"; 

  function get_letreros(){
    // así se hace hace referencia a la constante
    // cunado estamos dentro de la clase que la contiene
    return self::TIME; 
  }
  
  function get_globalConstante(){
    // aquí se hace referencia de la global MONEDA
    return "Y globalmente solo contó en: ".MONEDA;
  }
}

$conta = new Contador();

echo "Remembranza: <br>";

// El operador :: hace referncia a la constante fuera 
// de la clase que la contiene
echo $conta::CANTIDAD;

echo "<br>";
echo $conta->get_letreros();
echo "<br>";
echo "Ha contado muchos dineros en: ".MONEDA;
echo "<br>";
echo $conta->get_globalConstante();

```
El resultado es el siguiente:

```cmd
Remembranza:
Miles de millones ha contado
Por muchos años
Ha contado muchos dineros en: Dolares
Y globalmente solo contó en: Dolares
```
