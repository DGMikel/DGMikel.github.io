Modificadores 

Estos controlan el lacnace que tiene el programa para modificar recurso en el programa.

estos son:

  1. public -> Todos pueden accesar y modificar su valor.
  2. protected -> solo se puede modificar desde la clase que lo contiene y las clases que heredan de esta.
  3. private -> Solo laclase que lo contiene puede modificarlo.

```php
<?php 

class Articles{
  // Todos podrían modificar esta variable
  public $title; 

  // Solo las clases que heredan de esta y esta misma pueden modificarla
  protected $date;

  // Solo esta clase que lo contiene puede modificarla
  private $no_pags;

  
  
}
```
