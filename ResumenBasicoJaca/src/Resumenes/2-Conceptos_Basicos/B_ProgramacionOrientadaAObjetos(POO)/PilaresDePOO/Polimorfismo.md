# Polimorfismo en Java

## Definición
El polimorfismo es uno de los pilares fundamentales de la Programación Orientada a Objetos (POO). Permite que una misma operación se comporte de diferentes maneras en distintas instancias de clases relacionadas por herencia.

## Beneficios del Polimorfismo
- **Flexibilidad**: Permite escribir código más flexible y reutilizable.
- **Mantenimiento**: Facilita el mantenimiento y la extensión del código.
- **Intercambiabilidad**: Permite tratar objetos de diferentes clases de manera uniforme.

## Tipos de Polimorfismo
- **Polimorfismo en tiempo de compilación (Sobrecarga de métodos)**: Permite definir múltiples métodos con el mismo nombre pero diferentes parámetros.
- **Polimorfismo en tiempo de ejecución (Sobrescritura de métodos)**: Permite que una subclase proporcione una implementación específica de un método que ya está definido en su superclase.

## Polimorfismo en Tiempo de Compilación
### Ejemplo de Sobrecarga de Métodos
```java
public class Calculadora {
    // Método sobrecargado para sumar dos enteros
    public int sumar(int a, int b) {
        return a + b;
    }

    // Método sobrecargado para sumar tres enteros
    public int sumar(int a, int b, int c) {
        return a + b + c;
    }
}
```

## Polimorfismo en Tiempo de Ejecución
### Ejemplo de Sobrescritura de Métodos
#### Superclase
```java
public class Animal {
    public void hacerSonido() {
        System.out.println("El animal hace un sonido");
    }
}
```

#### Subclase
```java
public class Perro extends Animal {
    @Override
    public void hacerSonido() {
        System.out.println("El perro ladra");
    }
}
```

### Uso del Polimorfismo
```java
public class Main {
    public static void main(String[] args) {
        Animal miAnimal = new Perro(); // Polimorfismo en acción
        miAnimal.hacerSonido(); // Salida: El perro ladra
    }
}
```

## Interfaces y Polimorfismo
Las interfaces también permiten implementar polimorfismo, ya que una clase puede implementar múltiples interfaces y ser tratada como cualquiera de ellas.

### Ejemplo de Polimorfismo con Interfaces
#### Interface
```java
public interface Volador {
    void volar();
}
```

#### Clase que Implementa la Interface
```java
public class Pajaro implements Volador {
    @Override
    public void volar() {
        System.out.println("El pájaro vuela");
    }
}
```

### Uso del Polimorfismo con Interfaces
```java
public class Main {
    public static void main(String[] args) {
        Volador miVolador = new Pajaro(); // Polimorfismo en acción
        miVolador.volar(); // Salida: El pájaro vuela
    }
}
```

## Conclusión
El polimorfismo es una característica esencial de la POO que permite que una misma operación se comporte de diferentes maneras en distintas instancias de clases relacionadas. Utilizando la sobrecarga y la sobrescritura de métodos, así como interfaces, se puede escribir código más flexible y reutilizable.
