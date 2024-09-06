# Iteradores en Java

## Definición
Un iterador es un objeto que permite recorrer una colección, accediendo a sus elementos uno a uno. Los iteradores proporcionan una manera uniforme de iterar sobre diferentes tipos de colecciones sin exponer su estructura interna.

## Conceptos Claves
- **Iterador**: Objeto que permite recorrer una colección.
- **Métodos Principales**:
  - `hasNext()`: Devuelve `true` si hay más elementos en la colección.
  - `next()`: Devuelve el siguiente elemento de la colección.
  - `remove()`: Elimina el último elemento devuelto por el iterador (opcional).

## Beneficios de Usar Iteradores
- **Uniformidad**: Proporcionan una manera uniforme de recorrer diferentes tipos de colecciones.
- **Encapsulamiento**: Ocultan la estructura interna de la colección, permitiendo cambios en la implementación sin afectar el código que la recorre.
- **Flexibilidad**: Permiten eliminar elementos de la colección durante la iteración de manera segura.

## Ejemplo de Uso
### Iterador con List
```java
import java.util.ArrayList;
import java.util.Iterator;
import java.util.List;

public class Main {
    public static void main(String[] args) {
        List<String> lista = new ArrayList<>();
        lista.add("Elemento 1");
        lista.add("Elemento 2");
        lista.add("Elemento 3");

        Iterator<String> iterador = lista.iterator();
        while (iterador.hasNext()) {
            String elemento = iterador.next();
            System.out.println(elemento);
        }
    }
}
```

### Iterador con Set
```java
import java.util.HashSet;
import java.util.Iterator;
import java.util.Set;

public class Main {
    public static void main(String[] args) {
        Set<String> conjunto = new HashSet<>();
        conjunto.add("Elemento 1");
        conjunto.add("Elemento 2");
        conjunto.add("Elemento 3");

        Iterator<String> iterador = conjunto.iterator();
        while (iterador.hasNext()) {
            String elemento = iterador.next();
            System.out.println(elemento);
        }
    }
}
```

## Conclusión
Los iteradores son una herramienta esencial en Java para recorrer colecciones de manera uniforme y segura. Proporcionan una abstracción que oculta la estructura interna de la colección, mejorando la flexibilidad y la mantenibilidad del código.