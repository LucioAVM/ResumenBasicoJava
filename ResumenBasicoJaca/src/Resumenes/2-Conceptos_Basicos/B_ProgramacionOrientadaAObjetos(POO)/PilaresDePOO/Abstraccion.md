# Abstracción en Java

## Definición
Consiste en ocultar los detalles de implementación y mostrar solo la funcionalidad esencial de un objeto. La abstracción permite centrarse en lo que hace un objeto en lugar de cómo lo hace.

## Beneficios de la Abstracción
- **Simplicidad**: Reduce la complejidad al ocultar los detalles de implementación.
- **Mantenimiento**: Facilita el mantenimiento y la modificación del código.
- **Reutilización**: Permite reutilizar el código de manera más eficiente.

## Implementación en Java
En Java, la abstracción se puede lograr utilizando clases abstractas e interfaces.

### Clases Abstractas
Una clase abstracta no puede ser instanciada y puede contener métodos abstractos (sin implementación) y métodos concretos (con implementación).

#### Sintaxis
```java
public abstract class NombreDeLaClase {
    // Método abstracto
    public abstract void metodoAbstracto();

    // Método concreto
    public void metodoConcreto() {
        // Implementación del método
    }
}
```

#### Ejemplo de Clase Abstracta
```java
public abstract class Figura {
    // Método abstracto
    public abstract double calcularArea();

    // Método concreto
    public void mostrarTipo() {
        System.out.println("Esta es una figura");
    }
}
```

### Subclase que Extiende una Clase Abstracta
```java
public class Circulo extends Figura {
    private double radio;

    public Circulo(double radio) {
        this.radio = radio;
    }

    @Override
    public double calcularArea() {
        return Math.PI * radio * radio;
    }
}
```

### Uso de la Clase Abstracta
```java
public class Main {
    public static void main(String[] args) {
        Figura miFigura = new Circulo(5.0);
        System.out.println("Área del círculo: " + miFigura.calcularArea());
        miFigura.mostrarTipo();
    }
}
```

### Interfaces
Una interfaz es una colección de métodos abstractos que una clase puede implementar. Las interfaces permiten definir un contrato que las clases deben cumplir.

#### Sintaxis
```java
public interface NombreDeLaInterfaz {
    void metodoAbstracto();
}
```

#### Ejemplo de Interfaz
```java
public interface Dibujable {
    void dibujar();
}
```

### Clase que Implementa una Interfaz
```java
public class Cuadrado implements Dibujable {
    @Override
    public void dibujar() {
        System.out.println("Dibujando un cuadrado");
    }
}
```

### Uso de la Interfaz
```java
public class Main {
    public static void main(String[] args) {
        Dibujable miDibujo = new Cuadrado();
        miDibujo.dibujar();
    }
}
```

## Conclusión
La abstracción es una característica esencial de la POO que permite ocultar los detalles de implementación y centrarse en la funcionalidad esencial. Utilizando clases abstractas e interfaces, se puede escribir código más simple, mantenible y reutilizable.
