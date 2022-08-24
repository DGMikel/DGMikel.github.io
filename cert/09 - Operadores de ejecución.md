# OPERADORES DE EJECUCIÓN

Se pueden ejecutar instrucciones para consola si se encierran entre comillas invertidas <br>


```php

// `instrucciones`          <----- `  `

// En este ejercicio se crearan archivos y se nombrarán

$book; // variable donde se guarda los titulos de los archivos

for($i = 0; $i<=5; $i++){
  $book = "Libro_$i.txt"; 
  `touch $book`;//            <----- comando de UNIX con el nombre en php
}

$file = `ls -al`;//           <----- comando de UNIX con reultado guardado enphp
echo "<pre>".$file."<pre>";

// SALIDA
/*
total 16
drwxr-xr-x 1 runner runner  214 Aug 24 14:04 .
drwxrwxrwx 1 runner runner  122 Aug 24 13:52 ..
drwxr-xr-x 1 runner runner   12 Nov 11  2021 .cache
-rw-r--r-- 1 runner runner 1391 Aug 24 14:04 index.php
-rw-r--r-- 1 runner runner    0 Aug 24 14:04 Libro_0.txt
-rw-r--r-- 1 runner runner    0 Aug 24 14:04 Libro_1.txt
-rw-r--r-- 1 runner runner    0 Aug 24 14:04 Libro_2.txt
-rw-r--r-- 1 runner runner    0 Aug 24 14:04 Libro_3.txt
-rw-r--r-- 1 runner runner    0 Aug 24 14:04 Libro_4.txt
-rw-r--r-- 1 runner runner    0 Aug 24 14:04 Libro_5.txt
-rw-r--r-- 1 runner runner   60 Jun  6 17:16 .replit
-rw-r--r-- 1 runner runner   53 Aug 24 13:52 replit.nix
-rw-r--r-- 1 runner runner  458 Aug 24 13:25 texto.txt
*/
```
