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
echo date('l')."<br>";                                               // Día con formato Wendays
echo date('Y.m.d')."<br>";                                           // Fecha con formato 2022.04.23
echo date('H:i:s')."<br>";                                           // Hora con formato de 24 horas 23:10:05


```
