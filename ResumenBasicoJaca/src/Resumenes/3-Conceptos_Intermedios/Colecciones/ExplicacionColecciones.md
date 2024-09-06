# Colecciones en Java

## Definición
Las colecciones en Java son estructuras de datos que permiten almacenar y manipular grupos de objetos. Proporcionan una manera eficiente de manejar conjuntos de datos, facilitando operaciones como búsqueda, inserción, eliminación y ordenación.

## Concepto de Colección
Una colección es un contenedor de objetos, también conocidos como elementos. Las colecciones permiten agrupar múltiples elementos en una sola unidad, proporcionando métodos para operar sobre estos elementos de manera eficiente.

## Beneficios de Usar Colecciones
- **Eficiencia**: Proporcionan métodos optimizados para manipular grandes cantidades de datos.
- **Flexibilidad**: Permiten almacenar diferentes tipos de datos y cambiar el tamaño dinámicamente.

## Casos de Uso Generales
- **Almacenamiento Dinámico**: Cuando se necesita una estructura de datos cuyo tamaño puede cambiar dinámicamente.
- **Agrupación de Datos**: Para agrupar objetos relacionados y operar sobre ellos de manera conjunta.
- **Ordenación y Búsqueda**: Para ordenar elementos y realizar búsquedas eficientes.
- **Eliminación y Filtrado**: Para eliminar elementos específicos o filtrar elementos según ciertos criterios.

## Tipos de Colecciones
- **List**: Almacena elementos en una secuencia ordenada, permite duplicados.
- **Set**: Almacena elementos únicos, no permite duplicados.
- **Queue**: Almacena elementos en el orden en que se insertan, siguiendo el principio FIFO (First In, First Out).
- **Map**: Almacena pares clave-valor, permite buscar valores basados en claves.

## Ejemplo de Uso
### List
```java
import java.util.ArrayList;
import java.util.List;

public class Main {
    public static void main(String[] args) {
        List<String> lista = new ArrayList<>();
        lista.add("Elemento 1");
        lista.add("Elemento 2");
        lista.add("Elemento 3");
        System.out.println(lista);
    }
}
```

### Set
```java
import java.util.HashSet;
import java.util.Set;

public class Main {
    public static void main(String[] args) {
        Set<String> conjunto = new HashSet<>();
        conjunto.add("Elemento 1");
        conjunto.add("Elemento 2");
        conjunto.add("Elemento 1"); // No se añadirá porque ya existe
        System.out.println(conjunto);
    }
}
```

### Queue
```java
import java.util.LinkedList;
import java.util.Queue;

public class Main {
    public static void main(String[] args) {
        Queue<String> cola = new LinkedList<>();
        cola.add("Elemento 1");
        cola.add("Elemento 2");
        System.out.println(cola.poll()); // Elimina y devuelve el primer elemento
        System.out.println(cola);
    }
}
```

### Map
```java
import java.util.HashMap;
import java.util.Map;

public class Main {
    public static void main(String[] args) {
        Map<String, Integer> mapa = new HashMap<>();
        mapa.put("Clave 1", 1);
        mapa.put("Clave 2", 2);
        System.out.println(mapa.get("Clave 1")); // Devuelve el valor asociado a "Clave 1"
    }
}
```

## Conclusión
Las colecciones en Java son herramientas poderosas y flexibles para manejar grupos de objetos. Proporcionan métodos eficientes para realizar operaciones comunes y son esenciales para el desarrollo de aplicaciones robustas y escalables.