# Controllers

Los controllers o controladores son clases dentro de un proyecto de spring que enrutan las peticiones que se hacen al sistema desde las vistas.
estas pueden ser desde una ruta del navegador así como peticiones ajax con rutas hacia servicios internos del sistema.

para que una clase sea conciderda Controller debe tener la anotación @Controller a inicio de esta:

```java

@Controller
public class getUsuarios(){

}

```

a un que así como hay distintos tipos de peticiones así hay variantes en esta anotación.

  *. @Controller
  *. @ControllerAdvice
  *. @RestControlrer
  *. @RestControllerAdvice
  
 
 ## @Controller
 Esta anotación además de indcar a JAVA que la clase es un controlador permite la autodeteccion de clases de componentes en el classpath
 
 ## @ControllerAdvice
 

## @RestController
Esta anotación sirve para indicar que la clase funciona como un controlador en el cual sus métodos devuelven un objeto de dominio en lugar de una vista.

## @RestControlerAdvice
Esta anotación que combina las anotaciones @ControllerAdvice y @ResponseBody y se usa junto con la anotación @ExceptionHnadler para manejar las excepciones dentro del controlador.


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
  
  
  
  
  
  
