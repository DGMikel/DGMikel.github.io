# OPERADOR DE CONTROL DE ERRORES

El operador es **@**
Al anteponer este operador a una expresion y esta genera un error, el mensaje que esta genere se ignorará

```php

$texto = file('url_archivo_no_existe') or die('No se pudo encontrar el archivo');

// SALIDA
// Sin el operador:: 
// Warning: file(url_archivo_no_existe): failed to open stream: No such file or directory in /home/runner/variables-predifinidas/index.php on line 2
// No se pudo encontrar el archivo

$texto = @file('url_archivo_no_existe') or die('No se pudo encontrar el archivo');

//SALIDA
// Con el operador::
// No se pudo encontrar el archivo

```
