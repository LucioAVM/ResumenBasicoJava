# Principio de Sustitución de Liskov (LSP) en Programación Orientada a Objetos

## Definición
El **Principio de Sustitución de Liskov (Liskov Substitution Principle, LSP)** establece que los objetos de una clase derivada deben ser sustituibles por objetos de la clase base sin alterar el correcto funcionamiento del programa. En otras palabras, una subclase debe ser reemplazable por su superclase sin que el comportamiento del sistema se vea afectado.

## Conceptos Claves
- **Sustitución**: Las instancias de una subclase deben poder reemplazar a las instancias de la clase base.
- **Herencia**: Las subclases deben heredar de manera coherente y respetar el contrato de la clase base.
- **Contrato**: Las subclases deben cumplir con las expectativas y comportamientos definidos por la clase base.

## Importancia
- **Correctitud**: Garantiza que el sistema funcione correctamente cuando se utilizan subclases en lugar de la clase base.
- **Reutilización de Código**: Facilita la reutilización de código al permitir que las subclases se utilicen de manera intercambiable con la clase base.
- **Mantenibilidad**: Mejora la mantenibilidad del código al asegurar que las subclases no introduzcan comportamientos inesperados.

## Ejemplo de Uso
### Clase Base y Subclases
```java
public class Vehiculo {
    public void acelerar() {
        System.out.println("El vehículo está acelerando");
    }
}

public class Coche extends Vehiculo {
    @Override
    public void acelerar() {
        System.out.println("El coche está acelerando");
    }
}

public class Bicicleta extends Vehiculo {
    @Override
    public void acelerar() {
        System.out.println("La bicicleta está acelerando");
    }
}
```

### Uso de las Clases con Sustitución de Liskov
```java
public class Main {
    public static void main(String[] args) {
        Vehiculo vehiculo1 = new Coche();
        Vehiculo vehiculo2 = new Bicicleta();

        vehiculo1.acelerar(); // Salida: El coche está acelerando
        vehiculo2.acelerar(); // Salida: La bicicleta está acelerando
    }
}
```

## Casos de Uso Comunes
- **Jerarquías de Clases**: Asegurar que las subclases puedan sustituir a las clases base en jerarquías de herencia.
- **Polimorfismo**: Utilizar el polimorfismo de manera efectiva, permitiendo que las subclases se comporten como la clase base.
- **Diseño de APIs**: Crear APIs que permitan la extensión mediante subclases sin romper el comportamiento esperado.

## Conclusión
El Principio de Sustitución de Liskov es crucial para mantener la correctitud y coherencia en sistemas orientados a objetos. Al asegurar que las subclases puedan sustituir a las clases base sin alterar el comportamiento del sistema, se mejora la reutilización, mantenibilidad y robustez del código.