# Models

Un model es una clase que busca ser persitida en una tabla (que genereralmente lleva el mismo nombre)<br>
en una base de datos.
Cada instanciación esta clase se gurada en un registro.

Para la implementación de un Model se necesitan importar la clase JPA para hacer uso de sus anotaciones así como de la ayuda<br>
de una librería para hacer más facil la redacción del código.

Descripción:

  1. JPA importada en el paquete javax.persistence, para poder acceder a sus anotaciones.
  2. Lombok es una libreía que permite escribir metodos más facilmente, escribiendo código por el desarrollador.
  3. Anotaciones:
    1. @Entity :: Convierte la clase java en una entidad (JPA).<br> 
    2. @Table(name = "nombre_tabla") :: Establece a que tabla estará relacionada la clase (JPA).<br> 
    3. @Column(name == "nombre_columna") :: Establece a que columna estará relacionada la varaiable (JPA).<br> 
    4. @Id :: Indica cual variable de clase es la llave primaria (Primary Key) (JPA).<br> 
    5. @Getter :: Crea los métodos get de las variables que son marcadas con esta (Librería Lombok).<br> 
    6. @Setter :: Crea los métodos set de las variables que son marcadas con esta (Librería Lombok).<br> 
    

```java
package com.nova.boros.controllers.models;

import lombok.Getter;
import lombok.Setter;

import javax.persistence.Column;
import javax.persistence.Entity;
import javax.persistence.Id;
import javax.persistence.Table;

//////////////////////////////////////////////////////////
//                                                      //
// Esta clase será un modelo de la clase Usuario        //
// Por lo cual la clase se debe volver una Entitie      //
//                                                      //
//////////////////////////////////////////////////////////

                          // @Entity marca esta clase como una entitie
@Entity                   // Ahora es una clase en el que su estado es persistido en la BD

@Table(name = "usuarios") // @Table relaciona la clase a una tabla en la base de datos
                          // name = "alumnos" indica a que tabla apunta en la BD
                          // Si no tuviese esta anotación la clase sería relacionada con una tabla
                          // con el mismo nombre que la clase
public class Usuario {

    // OBSERVA::
    // Cada campo de la clase debe ser mapeado con relación a la tabla en la que se quiere hacer persistencia
    //  Para esto se ocupan las anotaciones siguientes en los campos de la clase

    @Id                    // @Id inidca que este campo es Primary Key
    @Getter                // @Getter crea el método getId automáticamente
    @Column(name = "id")   // @Column(name = "id") Relaciona la varaiable id de la clase con la columna id de la tabla
    private int id;        // private int id declara una varaiable privada en la clase Usuarios

    @Column(name="nombre")
    @Getter
    @Setter                // @Seetter crea el método SetNombre que ajusta el valor de la variable privada nombre
    private String nombre;

    @Getter @Setter @Column(name = "paterno")
    private String paterno;

    @Getter @Setter @Column(name = "email")
    private String email;

    @Getter @Setter @Column(name = "telefono")
    private int telefono;

    @Getter @Setter @Column(name = "password")
    private String password;
    
    /* Fin del MODEL USAUARIO */
}
```

