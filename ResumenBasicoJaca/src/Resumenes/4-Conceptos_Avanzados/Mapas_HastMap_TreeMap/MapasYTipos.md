# Resumen sobre Map, HashMap y TreeMap en Java

## Map en Java
Un **Map** es una interfaz que permite almacenar pares clave-valor, donde cada clave es única. Proporciona:
- Claves únicas.
- Acceso eficiente a valores mediante claves.
- Operaciones comunes como agregar, eliminar y buscar elementos.

### Ejemplo de Uso
```java
import java.util.Map;
import java.util.HashMap;

public class EjemploMap {
    public static void main(String[] args) {
        Map<String, Integer> mapa = new HashMap<>();
        mapa.put("Uno", 1);
        mapa.put("Dos", 2);
        mapa.put("Tres", 3);

        System.out.println("Valor para 'Dos': " + mapa.get("Dos"));
        mapa.remove("Dos");
        System.out.println("Mapa después de eliminar 'Dos': " + mapa);
    }
}
```

## HashMap
**HashMap** es una implementación de la interfaz Map basada en una tabla hash. Características:
- No garantiza ningún orden en las claves.
- Permite claves y valores nulos.
- Ofrece acceso rápido (O(1)) a los elementos.
- Ideal para aplicaciones donde el orden de los elementos no es importante y se necesita un acceso rápido.

### Ejemplo de Uso
```java
import java.util.HashMap;

public class EjemploHashMap {
    public static void main(String[] args) {
        HashMap<String, String> hashMap = new HashMap<>();
        hashMap.put("clave1", "valor1");
        hashMap.put("clave2", "valor2");
        hashMap.put(null, "valorNulo");

        System.out.println("Valor para 'clave1': " + hashMap.get("clave1"));
        System.out.println("Valor para clave nula: " + hashMap.get(null));
    }
}
```

## TreeMap
**TreeMap** es una implementación de la interfaz NavigableMap basada en un árbol rojo-negro. Características:
- Mantiene las claves ordenadas en su orden natural o mediante un comparador.
- No permite claves nulas.
- Tiene un tiempo de acceso de O(log n).
- Adecuado para aplicaciones que requieren un orden específico de los elementos.

### Ejemplo de Uso
```java
import java.util.TreeMap;

public class EjemploTreeMap {
    public static void main(String[] args) {
        TreeMap<String, String> treeMap = new TreeMap<>();
        treeMap.put("clave1", "valor1");
        treeMap.put("clave3", "valor3");
        treeMap.put("clave2", "valor2");

        System.out.println("TreeMap ordenado: " + treeMap);
        System.out.println("Primera clave: " + treeMap.firstKey());
        System.out.println("Última clave: " + treeMap.lastKey());
    }
}
```

## Diferencias entre HashMap y TreeMap
- **Orden**: HashMap no garantiza el orden de los elementos, mientras que TreeMap los ordena.
- **Rendimiento**: HashMap ofrece un acceso más rápido en promedio (O(1)), mientras que TreeMap es más lento debido a la estructura del árbol (O(log n)).
- **Claves nulas**: HashMap permite claves nulas, TreeMap no.

## Ejemplos de Uso
- **HashMap**: Almacenar y acceder a datos de configuración, cachés.
- **TreeMap**: Implementar tablas de búsqueda, diccionarios ordenados.