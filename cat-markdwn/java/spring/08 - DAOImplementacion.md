# Implementacion de la interface DAO

El Objeto de Acceso a los datos o DAO es la clase por donde operan las entradas y salidas de información dado que esta clase es marcada con la anotación @Repository.

así pues uan vez marcada esta clase se tienen que poner a su disposición varios elementos para que ejerza tal función .



```java
package com.nova.boros.controllers.dao;

import com.nova.boros.controllers.models.Usuario;
import org.springframework.stereotype.Repository;

import javax.persistence.EntityManager;
import javax.persistence.PersistenceContext;
import javax.transaction.Transactional;
import java.util.List;

//  https://mvitinnovaciontecnologica.wordpress.com/2020/02/06/guia-de-anotaciones-de-spring-framework/
////////////////////////////////////////////////////////////////
// Esta clase se usará como DAO ( DATA ACCESS OBJECT )        //
// Por lo que los datos que entren y salgan hacia la clase    //
// a la cual hace referencia                                  //
////////////////////////////////////////////////////////////////


@Repository     // Esta anotación marca la clase como Objeto de acceso a datos (DAO) u Repositorio
@Transactional  // Provee a la palicaciónla habilidad declarativa de los límites de la transacción
public class UsuariosDaoImp implements UsuariosDao{

    @PersistenceContext                            // Expresa Dependencia a un Entity manager
    EntityManager entityManager;                   // administrado por el contenedor y su contexto

    @Override                                      //  @Overrride indica que el método de la clase hijo UsuariosDaoImpl
    public List<Usuario> getUsuarios(){            //  está sobreescribiendo al método de la clase padre UsuarioDao
                                                   //  En este caso el método getUsuarios.

        String query = "FROM Usuarios";            // String con Query de Hibernate

        return entityManager.createQuery(query).   //El entityManager gestiona el query creado para hecar la
                getResultList();                   // Consulta la BD y el resultado devolverlo en una Lista.
    }

}

```
