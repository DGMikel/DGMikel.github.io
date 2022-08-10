
# Propiedades Estáticas

Dichas propiedaes se pueden invocar sin necesidad de instanciar la clase que las contiene;

```php
<?php

class Figuras{
  public static $cuadrado = 4;
  public static $triangulo = 3;
  public static $circulo = 0;
  public static $hexagono = 6;
 
}
// Figuras::$cuadrado <- traido desde la clase sin estanciar 
echo "Número de lados de un cuadrado es: ".Figuras::$cuadrado;
echo "<br>";

// Figuras::$triangulo <- traido desde la clase sin estanciar 
echo "Número de lados de un triangulo es: ".Figuras::$triangulo;
echo "<br>";

// Figuras::$circulo <- traido desde la clase sin estanciar 
echo "Número de lados de un circulo es: ".Figuras::$circulo;
echo "<br>";

// Figuras::$hexaxgono <- traido desde la clase sin estanciar 
echo "Número de lados de un hexagono es: ".Figuras::$hexagono;

```

Y se trndrá de resultado:

```cmd
Número de lados de un cuadrado es: 4
Número de lados de un triangulo es: 3
Número de lados de un circulo es: 0
Número de lados de un hexagono es: 6
```
