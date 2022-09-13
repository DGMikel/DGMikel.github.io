# Anotaciones

Dan funcionalidad a Calses y metodos estas inician con @.

Dependeiendo de la necesidad Spring porovee de muchas anotaciones:

<table>
  <tr>
    <td>Anotación</td><td>Función</td>
  </tr>
  <tr>
    <td>
      @Component<br>(Spring - Stereotype Annotation)
    </td>
    <td> <ul>
           <li>
             Registra la clase como un bean dentro del framework para usarla en otros lados del proyecto Para que el explorador de componenetes pueda agregarla al contexto de la aplicación.
           </li>
           <li>
             Es la principal anotación del paquete de anotaciones de Spring *** Stereotype Annotation *** ya que de ella derivan otras como son: <br> @Service, @Repository, @Controller 
          </li>
  </tr>
  <tr>
    <td>
      @Service<br>(Spring - Stereotype Annotation)
    </td>
    <td>
      <ul>
        <li>
          Usada en las clases, @Service marca una clase que realiza algún servicio, como puede ser Logica de negocios, cálculos ó llamar APIS externas
        </li>
        <li>
          Las clases marcadas con esta anotación estn destinadas a usarse en la capa de servicio.
        </il>
        <li>
          Se encarga de registrar el componente y permitir que se inyecten otras clases.
      </ul>
    </td>
  </tr>
  <tr>
    <td>
      @Repository<br>(Spring - Stereotype Annotation)
    </td>
    <td>
      <ul>
        <li>
          <b>Accede directamenet a la Base deatos</b> funciona como marcador para cualquier clase que cumpla la fucnión de repositorio u Objeto de acceso a datos.
        </li>
        <li>
          Registra un componente a nivel del motor de iniyección de dependenciasy traduce de forma automática las excepeciones que produzcan de accesos de datos *** haciendo que no sea necesario un bloque Try-catch ***.
        </li>
        <li>
          Las clases marcadas con esta anotación estn destinadas a usarse en la capa de servicio.
        </il>
      </ul>
    </td>
  </tr>
  <tr>
    <td>
      @Controller<br>(Spring - Stereotype Annotation)
    </td>
    <td>
      <ul>
        <li>
          <b>Registra los controladores</b> que son los encargados de enlazarnos con la capa de presentación del modelo MVC.
        </li>
        <li>
          <b>Registra las URLs</b> a las que el componente responde a través de los diferentes @RequestMapping
        </li>
      </ul>
    </td>
  </tr>
  
  <tr>
    <td>
      @RestController<br>(Spring - Stereotype Annotation)
    </td>
    <td>
      <ul>
        <li>Se usa a nivel de clase</li>
        <li>
          Cada uno de los metodos de la clase marcada con esta anotación devolvera un objeto de dominio en lugar de una vista.
        </li>
        <li>
          Estos Objetos son del tipo HTTP y pueden ser por ejemplo JSON pero no HTMLs
        </li>
      </ul>
    </td>
  </tr>
  
  
  <tr>
    <td>
      @RequestMApping
    </td>
    <td>
      <ul>
        <li>Se usa a nivel de clase y de metodo</li>
        <li>
          Si se usa a nivel de clase establece una URL para todo el Controlador ejemplo:<br>
          @RequestMApping(value = "autos") <-- 'prefijo autos' <br> 
          navedaor = autos/beatle, autos/monza, autos/ibiza 
        </li>
        <li>
          Cuando se usa en un metodo se ajusta una URL al metodo y mediante la petición se accede a el y a su respuesta.<br>
          ejemplo: @RequestMApping(value = "beatle")<br> 
          navedaor = autos/beatle <- para acceder a la pagina del carro beatle.
        </li>
      </ul>
    </td>
  </tr>
  
  <tr>
    <td>
      @Entity
    </td>
    <td>
      <ul>
        <li>Marca la clase como una entidad que se maperará a un tabla de la base de datos</li>
        <li>Cada variable de clase se mapeará con las columnas de la tabla asignada o diseñada para esta clase</li>
      </ul>
    </td>
  </tr>
  
  <tr>
    <td>
      @Table
    </td>
    <td>
      <ul>
        <li>Indica caraecteristicas de esquema, como el nombre</li>
        <li>Si no se indica esta anotación la entidad se mapeará con un atbal en la Base de Datos con el mismo nobre de la clase</li>
      </ul>
    </td>
  </tr>
  
   <tr>
    <td>
      @Id
    </td>
    <td>
      <ul>
        <li>Indica el campo que va a ser identificador de la entidad (Primary Key)</li>
      </ul>
    </td>
  </tr>
  
  
   <tr>
    <td>
      @GeneratedValue
    </td>
    <td>
      <ul>
        <li>Es el Identificador que se genera automáticamente por parte de la base de datos cuna do la entidad se hace persistente</li>
      </ul>
    </td>
  </tr>
  
  <tr>
    <td>
      @Column
    </td>
    <td>
      <ul>
        <li>Se usa para indicar caracteristacas del esquema en la que se mapea el campo</li>
        <li>Inidca el nombre de la columna con la que relacionará la variable y la columna de la entidad</li>
        <li>Si no se hace uso de estas anotaciones la entidad relacionara las variables que tengan el mismo nobre con la tabla en la base de datos</li>
      </ul>
    </td>
  </tr>
  
  <tr>
    <td>
      @OneToMany
    </td>
    <td>
      <ul>
        <li>Sirve para relacionar uno a muchos en entre tablas</li>
        <li></li>
      </ul>
    </td>
  </tr>
  <tr>
    <td>
      @mappedBy.
    </td>
    <td>
      <ul>
        <li><h3>EN COSNTRUCCION</h3></li>
        <li></li>
      </ul>
    </td>
  </tr>
  
</table>


@OneToMany: Sirve para definir una relación uno-a-muchos entre Autor y Mensaje. La anotación cascade indica que las acciones de borrado, persist y merge se propagan en cascada a los mensajes. Más adelante explicaremos la anotación @mappedBy.


@Column: Sirve para indicar características del esquema de la columna en la que se mapea el campo. En este caso, su nombre. Si no estuviera esta anotación, el nombre de la columna en la base de datos sería el nombre del campo.

@GeneratedValue: El identificador se genera automáticamente por parte de la base de datos cuando la entidad se hace persistente.

@Id: indica que el campo anotado (en nuestro caso Long id) va a ser el identificador de la entidad. La columna con la que se mapea en la base de datos es la clave primaria de la tabla.







@Entity: La clase es una entidad que se va a mapear con una tabla de la base de datos. Los campos de la clase se mapearán con columnas de la base de datos.

@Table: Sirve para indicar características del esquema de la tabla, en nuestro caso su nombre. Si no estuviera esta anotación, la entidad se mapearía con un una tabla con el nombre de la clase Java.




- ----------------------

JPA :  Java Persistence API
Es una API de java para manejar los datos --relacionales-- en un aplicación JAVA
para invocarla se importa:
    java.persistence



@Entity: indica que la clase decorada es una entidad
@MappedSuperClass: aplicado sobre una clase, indica que se mapeará como cualquier otra clase, pero que se aplicará únicamente a sus subclases, puesto que esta entidad no tiene una tabla asociada.
@Table: especifica el nombre de la tabla relacionada con la entidad. Admite el parámetro:
name: nombre de la tabla
PROPIEDAD
@Column: indica el nombre de la columna en base de datos. Admite el parámetro:
name: especifica el nombre de la columna
@Enumerated: indica que los valores de la propiedad van a estar dentro del rango de un objeto enumerador. Admite el parámetro:
value: indica el tipo valor que se va a utilizar en la persistencia en Base de Datos. Puede utilizarse el enumerador EnumType.
@Id: aplicado sobre una propiedad, indica que es la clave primaria de una entidad. La propiedad a la que hace referencia puede ser de los siguientes tipos: cualquier tipo primitivo, String, java.util.Date, java.sql.Date, java.math.BigDecimal, java.math.BigInteger
@GeneratedValue: especifica la estrategia de generación de la clave primaria. Admite el parámetro:
strategy: indica la estrategia a seguir para la obtención de un nuevo identificador. Permite utilizar el enum GenerationType.
@Lob: aplicado sobre una propiedad, indica que es un objeto grande (Large OBject). Por ejemplo, en el caso de String, si no se especifica @Lob, se le asigna un tamaño máximo de 255 caracteres.
@NotEmpty: validación de restricción, indica que la propiedad no puede tener un valor vacío.
TIPOS DE RELACIÓN
@OneToOne especifica un valor único que contiene una relación uno-a-uno con otro objeto. Dispone de los parámetros:
cascade: indica el tipo de operación de cascada a realizar. Permite utilizar el enumerador CascadeType.
fetch: indica la forma en que se consultarán las entidades asociadas. Permite utilizar el enumerador FetchType.
@OneToMany: especifica una relación uno-a-muchos. Dispone de los parámetros:
cascade: especifica el tipo de cascada. Permite utilizar el enumerador CascadeType.
mappedBy: especifica la propiedad de la entidad hija (en el extremo muchos) que sirve para enlazar con la entidad principal (en el extremo uno)
@ManyToOne: especifica una relación muchos-a-uno
@ManyToMany especifica una relación muchos-a-muchos en la propiedad decorada. Si la relación es bidireccional, se debe especificar el extremo propietario (el que posee la clave principal) mediante el parámetro mappedBy. En casos de relación bidireccional, JPA creará una tabla relacional por cada sentido. Para evitar esto, se usa el decorador @JoinTable.
@JoinTable especifica datos relativos a la tabla de unión en la relación. Este decorador se añade en el extremo propietario
Parámetros disponibles
name, indica el nombre de la tabla
joinColumns, indica cómo se llamará la columna que contendrá la clave correspondiente a la tabla en el extremo que es propietario. Se utiliza el decorador @JoinColumn para ello.
inverseJoinColumns, especifica cómo se llama la columna de clave ajena correspondiente al extremo propietario. Se utiliza el decorador @JoinColumns para ello.
Decoradores disponibles
@JoinColumn especifica la columna de unión. Dispone del parámetro
name, indica el nombre de la columna.
Ejemplo: imaginemos que en la entidad Receta tenemos la propiedad categorias, que correspondería a una unión muchos-a-muchos con la entidad Categoria, que a su vez tiene la propiedad recetas. En este caso, la propiedad categorias de Receta quedaría decorada de la siguiente forma:
@ManyToMany
@JoinTable(name = "receta_categoria",
      joinColumns = @JoinColumn(name = "receta_id"),
      inverseJoinColumns = @JoinColumn(name = "categoria_id"))
private Set<Categoria> categorias;
En la entidad Categoria, tendríamos una propiedad llamada recetas que decoraríamos de la siguiente forma:
@ManyToMany(mappedBy = "categorias")
private Set<Receta> recetas;
ENUMERADORES UTILIZADOS
CascadeType. Tipos de operación de cascada:
REMOVE
REFRESH
PERSIST
MERGE
DETACH
ALL
GenerationType. Tipos de estrategia para la generación de identificadores:
AUTO: el proveedor de persistencia escoge el método más adecuado según el modelo de base de datos
IDENTITY: el proveedor de persistencia escoge un identificador basándose en una columna identity de la tabla
SEQUENCE: utiliza una secuencia de la base de datos
TABLE: utiliza una tabla auxiliar para asegurarse de que la clave es verdaderamente única
FetchType. Tipos de obtención de entidades relacionadas:
LAZY
EAGER
EnumType. Tipo de enumerador. Indica cómo va a ser el tipo de persistencia en la base de datos:
ORDINAL: formato predeterminado. En base de datos, se almacenará el ordinal correspondiente al valor del enum.
STRING: en base de datos, se almacenará el valor String correspondiente al enum. Usando este tipo de persistencia, se evitan errores en caso de que los valores del enum cambien o se intercalen valores nuevos, que puedan alterar el ordinal asignado.





## SEGUIR CON 
importados de:
java.lang.annotation: @Retention, @Documented, @Target, y @Inherited<br>
            java.lang: @Override, @Deprecated, @SafeVarargs, @FunctionalInterface, y @SuppressWarnings



