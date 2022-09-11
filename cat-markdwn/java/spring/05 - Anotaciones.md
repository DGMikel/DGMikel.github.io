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
</table>
 
  
  









## SEGUIR CON 
importados de:
java.lang.annotation: @Retention, @Documented, @Target, y @Inherited<br>
            java.lang: @Override, @Deprecated, @SafeVarargs, @FunctionalInterface, y @SuppressWarnings



