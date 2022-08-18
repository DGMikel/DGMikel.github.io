# PHP Funciones

```php
<?php

$string = "PHP es un lunguaje para SERVIDORES";
$strReplc = ["El Inglés","PEROSNAS"];

echo strtolower($string)."<br>";                                    // a minusculas
echo strlen($string)."<br>";                                        // longitud del str 
echo strtoupper($string)."<br>";                                    // a mayusculas
echo strrev($string)."<br>";                                        // invierte el orden de un str 
echo str_replace(["PHP","SERVIDORES"], $strReplc, $string )."<br>"; // Remplaza (palabras, con estas, en este texto)
```
