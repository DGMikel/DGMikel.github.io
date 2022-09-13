# COntrollers

Es una clase que se usa para enrutar las peticiones del frontend hacia los mtedodos del backend, se usa para procesar las peticiones de los metodos web GET, PUT, PATCH, DELETE etc.

Se denota por la anotación @Controller al inicio de cada clase.
````java
/****************************************************************/
package com.proyecto.rptor.controllers;                         //
import com.proyecto.rptor.dao.UsuarioDao;                       //
import com.proyecto.rptor.models.Usuario;                       //    
import org.springframework.beans.factory.annotation.Autowired;  //
import org.springframework.web.bind.annotation.PathVariable;    //
import org.springframework.web.bind.annotation.RequestMapping;  //
import org.springframework.web.bind.annotation.RestController;  //
import java.util.List;                                          // 
/******* BLOQUE DE IMPORTACIONES ********************************/


// Anotacion que Convierte la clase en un Controller del  tipo Rest |
// O séa que TODOS SUS METODOS DEVOLVERAN OBJETOS DEL TIPO REST     |
                                                                    | 
@RestController                                                     // 
//------------------------------------------------------------------// 
public class UsuarioController {

    // @Autowired Crea un Objeto y lo hace visisble en otras partes del proyecto                   /  
    // para que pueda ser usado en otras partes                                                    /
    @Autowired                                  // HHACE LA INYECCIÓN DE DEPENDENCIAS             //
    private UsuarioDao usuarioDao; // O SÉA QUE CREA UN OBJETO DE OTRA CLASE Y INSTANCIA AQUÍ      /


    // @RequestMapping provee una ruta a la que se puede tener acceso desde la vista        // 
    @RequestMapping(value = "api/usuarios")            // para este ejemplo "api/usuarios"  //
    // -------------------------------------------------------------------------------------//
    
    public List<Usuario> getUsuario(){
        return   usuarioDao.getUsuarios();
    }

    
}

```

@RestControllers
public class UsuariosController{

   // Todoso los metodos de este controlador devolveran puros datos y objetos de ltipo JSON
}



