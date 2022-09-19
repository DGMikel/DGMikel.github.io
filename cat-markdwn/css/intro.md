# Datos

```cmd
css : lenguaje de estilos para paginas web
css :: capa de estilos en cascada

css sintaxis : selector { propiedad:valor, propiedad:valor }
css sintaxis ejemplo : p { color:red; font-size:12px }

// css selectores tipos
css selectores : son usados para seleccionar elementos html
css selectores simples : selectores basados en (name, id, class)
css selectores combinados : selectores basados en una relación especifica entre ellos
css selectores pseudo-clases : selectores basados en elementos en un cirto caso
css selectores pseudo-elementos : selecciona parte y estilo de un elemento
css atributos de selector : selecciona elementos basados en un atributo o valor de atributo

// css id selector
css selector id : es usado para seleccionar ese elemento en especifico, carácteristica '#'
css selector id ejemplo :  #titulo { color:red: } si <p id="titulo"> texto.. </p>

// css class selector
css selector class : usado para seleccionar elementos que tengan en común una clase,  carácteristica '.'
css selector class ejemplo : .texto { color:red; } si <p class="texto"> texto ... </p>
css selector elemento-clase : selecciona un elemento de una clase
css selector elemento-clase ejemplo : p.texto { color:red; } aquí los elementos <p> de la clase texto

// css universal selector 
css selector universal : selecciona todos los elementos de una página, carácteristica '*'
css selector universal ejemplo : * { text-align:center; color:red;} todos los elementod de la página


// css agrupamiento de selectores
css group selectors : se pueden agrupar selectores que tengan las mismas carácteristicas de estilo.
css group selectors ejemplo : h1, p { color:red } así todos los elemtos h1 y p tendrán texto en color rojo.

// Resumen selectores

selector            Sintaxis css      Html 
#id                 : #input1 { }     <input id="input1" type="text">
.class              : .class  { }     <h1 class = "texto"> texto ...</h1>
elemento.class      : p.texto { }     <p class = "texto"> texto ...  </p>
*                   : * { }           all html document
elemento            : p { }           <p>texto1</p> .... n<p></p>   
elemento, elemento  : h1, h2, p { }   <h1>, <h2>, <p>

// css inserción de código.
css inserción archivo : se puede hacer uso de un archivo con los estilos que deba tener el documento
css inserción archivo ejemplo : <link rel="stylesheet" href="./url_archivo.css">
```
satr
