# PDO instancia


```php

class Conexion{
  public   $instance;
  private  $user = "root";
  private  $passw = "";
  private  $strConex = "mysql:host:loscalhost; dbname=mvc";
  private  $conn;
  
  // Inicializa la clase Conxion
  public function __construct(){
  
    $this->conn = new PDO($this->strConx, $this->user, $this->passw);
  
  }
  
  // evita que copien la clase
  public function __clone(){  }


  public function getInstance(){
  
    if(!isset(self::instance)){
        
        $con = __CLASS__;
        
        self::instance = new $con;
    
    }
    return $instance
  
  }



}


```
