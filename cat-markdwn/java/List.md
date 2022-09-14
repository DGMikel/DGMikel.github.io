List  ArrayList

Es un Array que puede cambiar de tamaño, la cual puede ser encontrada en el paquete java.util

algunos método de manipulacón que tiene son los siguientes :: 

```console
  1. .add(valor) ::::::::::::::::: Adiciona un valor a la pila de valores que guarda.
  2. .get(indice) :::::::::::::::: Obtien el valor del indice inidcado en su interior.
  3. .remove(indice) ::::::::::::: Remueve el valor guardado en el indice inidcado.
  4. .set(indice, nuevo_valor) ::: Remplaza en el indice indicado el nuevo valor.
  5. .clear() :::::::::::::::::::: Limpia toda la lista de valores 
  6. .size() ::::::::::::::::::::: Retorna la cantidad de valores guardados.
  7. .isEmpty() :::::::::::::::::: Retorna un booleano indicando s esta vacia ó no el array.
  8. .indexOf(valor) ::::::::::::: Devuelve el indice donde se encuentra el valor parametrizado.
  9. .addAll(indice, Array) :::::: Guarda en el indice indicado otro objeto de la clase Array.
  10 .clone() :::::::::::::::::::: Se inicia como un objeto de la primera lista 
                                   Array<E> segudoArray = (Array<E>)primerArray.clone();
```

```java
import java.util.ArrayList;
import java.util.Collections;

class Main {
  public static void main(String[] args) {

    ArrayList<String> carros = new ArrayList<String>();
    ArrayList<String> carrosSort = new ArrayList<String>();

    // Adicionar  elementos
    carros.add("volvo");
    carros.add("bmw");
    carros.add("ford");
    carros.add("mazda");
    System.out.println("carros : "+carros);
    System.out.println("\n--Obtener un item---");
    //obtener un item
    System.out.print("carros.get(2) :"+carros.get(2));

    // modificar un elemento metodo set(indice, valor)
    carros.set(1,"VolksWagen");
    System.out.print("\n"+carros);

    //Remover un item método .remove(indice)
    carros.remove(2);
    System.out.print("\nUn item se ha removido :: "+carros);

    //Remover todos los item métdo .clear()
    carros.clear();
    System.out.print("\n Se ha limpiado la lista :: "+carros);

    // obtener la longitud del Array método .size()
    carros.add("volvo");
    carros.add("bmw");
    carros.add("tzuru");
    carros.add("beatle");
    carros.add("aztech");
    System.out.print("\nLa lista de carros :: "+carros);
    System.out.print("\nLa longitud de la lista :: "+carros.size()+"\n");

    // ordenar una lista método sort()
    Collections.sort(carros);
    for (String i : carros) {
      System.out.println(i);
    }
    
  }
}
```
