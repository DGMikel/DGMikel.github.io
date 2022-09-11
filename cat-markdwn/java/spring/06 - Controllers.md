# Controllers

Se usan para dirigir las url a la las aplicaciones solicitadas por ejemplo su el usuario escribe la URL:<br>
URL/pagina_de_registro  este sea dirigido a dicha pagina.

Para indicarle a la clase que va a ser un controlador se le debe indicar con la anotación<br>
<p>  @RestController  <-- es un controller Rest </p>

Luego cada metodo debe de tener una URL que apunte hacia el, esto lo hace la siguiente anotacuión:<br>
<p> @RequestMapping(value = "/prueba") <-- Esta anotación enlaza la url de 'value' al metodo  </p>

```java
  
package com.proyecto.rptor.controllers;

import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RestController;

@RestController // <-- ya es un controller REST
public class UsuarioController {

    
    @RequestMapping(value = "/prueba") // <-- Esta Anotación provee una ruta al metodo '/prueba' en este caso
    public String prueba(){
        return "SALIDA DE TEXTO CON CONTROLLER SPRING";  // <-- Retrono de el motodo prueba
    }

}
```
  
  
  
  
  
  
