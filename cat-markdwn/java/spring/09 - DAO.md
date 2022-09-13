# DAO

La Interfaz DAO es encargada de implementar los métodos necesarios que serán escritos a la clase DAOImplemnet
si se quiere hacer una inserción de registro, borrado, editado etc, de algun registro y no se provee del metodo necesario para ello 
se debe primero registrar en esta clase y despues hacer la parte ligica en la clase DAOImplements.

```java
package com.nova.boros.controllers.dao;
import com.nova.boros.controllers.models.Usuario;

import java.util.List;

public interface UsuariosDao {
    
    List<Usuario> getUsuarios();      // Este método Obtendrá todos los usuarios.
    List<Usuario> getUsuario(int id); // Este método Obtendra el usuario inidcado por el id de metodo

}
```
