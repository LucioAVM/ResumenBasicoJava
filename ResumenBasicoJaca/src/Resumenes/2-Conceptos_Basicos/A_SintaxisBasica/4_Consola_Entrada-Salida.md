# Entrada y Salida en Java

## Salida con `System.out`
`System.out` se utiliza para imprimir texto en la consola.

### Métodos Comunes
- **`System.out.print()`**: Imprime texto sin un salto de línea al final.
- **`System.out.println()`**: Imprime texto con un salto de línea al final.
- **`System.out.printf()`**: Imprime texto formateado.

### Ejemplos
```java
System.out.print("Hola, ");
System.out.print("Mundo!"); // Salida: Hola, Mundo!

System.out.println("Hola, Mundo!"); // Salida: Hola, Mundo! (con salto de línea)

int edad = 25;
System.out.printf("Tengo %d años.", edad); // Salida: Tengo 25 años.
```

--- Agregar todos los posibles formateos

## Entrada con `Scanner`
`Scanner` se utiliza para leer datos de entrada del usuario.

### Importar la Clase `Scanner`
```java
import java.util.Scanner;
```

### Crear un Objeto `Scanner`
```java
Scanner scanner = new Scanner(System.in);
```

### Métodos Comunes
- **`nextLine()`**: Lee una línea completa de texto.
- **`nextInt()`**: Lee un entero.
- **`nextDouble()`**: Lee un número de punto flotante.
- **`nextBoolean()`**: Lee un valor booleano.

### Ejemplos
```java
import java.util.Scanner;

public class EntradaEjemplo {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Leer una línea de texto
        System.out.print("Ingresa tu nombre: ");
        String nombre = scanner.nextLine();
        System.out.println("Hola, " + nombre);

        // Leer un entero
        System.out.print("Ingresa tu edad: ");
        int edad = scanner.nextInt();
        System.out.println("Tienes " + edad + " años.");

        // Leer un número de punto flotante
        System.out.print("Ingresa tu salario: ");
        double salario = scanner.nextDouble();
        System.out.println("Tu salario es " + salario);

        // Leer un valor booleano
        System.out.print("¿Eres estudiante? (true/false): ");
        boolean esEstudiante = scanner.nextBoolean();
        System.out.println("Eres estudiante: " + esEstudiante);
    }
}
```

### Cerrar el `Scanner`
Es una buena práctica cerrar el `Scanner` después de usarlo para liberar recursos.

```java
scanner.close();
```