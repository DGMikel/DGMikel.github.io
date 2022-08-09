## CLASE 

**Propiamente una clase se define con:

	1. Icinicia con la palabra class.
	2. Seguido por el Nombre de la Clase.
	3. Dos llaves encierran el contenido.
		1. Definiciones de clase
		2. Variables
		3. Metodos




```

class Persona{

  public $nombre;
  public $puesto;

  /* ajusta el nombre que ingresa
  en la función $nom*/
  function set_nombre($nom){
    
    /* el 'this' es para hacer referencia a
       public $nombre de la clase */
    $this->$nombre = $nom;
  }
  
  function get_nombre(){
    $this->puesto = "Programador";
    return $this->$nombre;
  }
 
}

```
