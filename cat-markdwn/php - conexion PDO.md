# Conexion PDO

```php
<?php 
// conexion acon base de datos

class Conexion{

    private $host = "localhost";
    private $user = "root";
    private $password = "";
    private $db = "mvc";
    private $connect;

    public function __construct(){
        $connectionString = "mysql:host=$this->host; dbname=$this->db; charset=utf8";

        try{

            /* Se inicia un objeto con conexion PDO */
            $this->connect = new PDO($connectionString, $this->user, $this->password);
            
            
            /* es para ver los errores más raídos sirve como LOG */
            $this->connect->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);

            /* Mensaje de exito */

            echo "<h3>Conexion Exitosas </h3>";

        } catch( Exception $e ){

            $this->connect = "Error de Conexión";
            echo "ERROR :: ".$e->getMessage();

        }

    }
}
```
