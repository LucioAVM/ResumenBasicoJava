# Herencia en Java

## Definición
La herencia es uno de los pilares fundamentales de la Programación Orientada a Objetos (POO). Permite crear nuevas clases basadas en clases existentes, heredando atributos y métodos de la clase base o superclase.

## Beneficios de la Herencia
- **Reutilización de Código**: Permite reutilizar el código existente, reduciendo la redundancia.
- **Mantenimiento**: Facilita el mantenimiento y la extensión del código.
- **Polimorfismo**: Permite que una clase hija sea tratada como una clase padre, facilitando la implementación de métodos polimórficos.

## Terminología
- **Superclase (Clase Padre)**: La clase de la cual se heredan atributos y métodos.
- **Subclase (Clase Hija)**: La clase que hereda de la superclase.

## Sintaxis
Para declarar una subclase que hereda de una superclase, se utiliza la palabra clave `extends`.

```java
public class Superclase {
    // Atributos y métodos de la superclase
}

public class Subclase extends Superclase {
    // Atributos y métodos adicionales de la subclase
}
```

## Ejemplo de Herencia
### Superclase
```java
public class Animal {
    // Atributos
    protected String nombre;

    // Constructor
    public Animal(String nombre) {
        this.nombre = nombre;
    }

    // Método
    public void hacerSonido() {
        System.out.println("El animal hace un sonido");
    }
}
```

### Subclase
```java
public class Perro extends Animal {
    // Constructor
    public Perro(String nombre) {
        super(nombre); // Llamada al constructor de la superclase
    }

    // Método sobrescrito
    @Override
    public void hacerSonido() {
        System.out.println("El perro ladra");
    }
}
```

### Uso de la Herencia
```java
public class Main {
    public static void main(String[] args) {
        // Crear una instancia de Perro
        Perro miPerro = new Perro("Firulais");

        // Llamar a métodos de la subclase y la superclase
        miPerro.hacerSonido(); // Salida: El perro ladra
    }
}
```

## Sobrescritura de Métodos
La sobrescritura permite que una subclase proporcione una implementación específica de un método que ya está definido en su superclase. Se utiliza la anotación `@Override` para indicar que un método está siendo sobrescrito.

### Ejemplo de Sobrescritura
```java
public class Gato extends Animal {
    // Constructor
    public Gato(String nombre) {
        super(nombre);
    }

    // Método sobrescrito
    @Override
    public void hacerSonido() {
        System.out.println("El gato maúlla");
    }
}
```

## Conclusión
La herencia es una característica poderosa de la POO que permite crear jerarquías de clases, reutilizar código y facilitar el mantenimiento y la extensión del software. Utilizando la herencia, se pueden crear clases más específicas basadas en clases más generales, aprovechando al máximo la reutilización de código.