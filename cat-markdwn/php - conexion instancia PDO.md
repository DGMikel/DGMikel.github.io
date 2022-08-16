# PDO instancia


```php
class Conexion{
  
          public $db;
  private static $instance;
  private static $user = "root";
  private static $dns = "mysql:host=localhost; dbname=mvc";
  private static $password = "";
  
  public function __construct(){
    $this->db = new PDO(self::$dns, self::$user, self::$password);
  }
  
  public function __clone(){}
  
  public function getInstance(){
  
    if(!isset(self::$instance)){
      $object = __CLASS__;
      self::$instance = new $object;
    }
      return self::$instance;
  
  }

}

```
