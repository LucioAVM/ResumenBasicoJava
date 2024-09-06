# Sobrecarga de Constructores en Java

## Definición
La sobrecarga de constructores en Java permite definir múltiples constructores en una clase, cada uno con diferentes parámetros. Esto proporciona flexibilidad para crear objetos de diferentes maneras.

## Conceptos Claves
- **Constructor**: Método especial que se llama al crear un objeto.
- **Sobrecarga**: Definir múltiples métodos con el mismo nombre pero diferentes parámetros.
- **Parámetros**: Los argumentos que se pasan al constructor para inicializar el objeto.

## Beneficios de la Sobrecarga de Constructores
- **Flexibilidad**: Permite crear objetos de diferentes maneras según las necesidades.
- **Reutilización de Código**: Facilita la reutilización de código al permitir diferentes inicializaciones en una sola clase.
- **Claridad**: Mejora la claridad del código al proporcionar constructores específicos para diferentes escenarios.

## Ejemplo de Uso
### Clase con Sobrecarga de Constructores
```java
public class Persona {
    String nombre;
    int edad;
    String direccion;

    // Constructor sin parámetros
    public Persona() {
        this.nombre = "Desconocido";
        this.edad = 0;
        this.direccion = "Desconocida";
    }

    // Constructor con un parámetro
    public Persona(String nombre) {
        this.nombre = nombre;
        this.edad = 0;
        this.direccion = "Desconocida";
    }

    // Constructor con dos parámetros
    public Persona(String nombre, int edad) {
        this.nombre = nombre;
        this.edad = edad;
        this.direccion = "Desconocida";
    }

    // Constructor con tres parámetros
    public Persona(String nombre, int edad, String direccion) {
        this.nombre = nombre;
        this.edad = edad;
        this.direccion = direccion;
    }
}
```

### Uso de los Constructores Sobrecargados
```java
public class Main {
    public static void main(String[] args) {
        Persona p1 = new Persona();
        Persona p2 = new Persona("Juan");
        Persona p3 = new Persona("Ana", 25);
        Persona p4 = new Persona("Luis", 30, "Calle Falsa 123");

        System.out.println(p1.nombre); // Salida: Desconocido
        System.out.println(p2.nombre); // Salida: Juan
        System.out.println(p3.nombre + ", " + p3.edad); // Salida: Ana, 25
        System.out.println(p4.nombre + ", " + p4.edad + ", " + p4.direccion); // Salida: Luis, 30, Calle Falsa 123
    }
}
```

## Casos de Uso Comunes
- **Inicialización por Defecto**: Proporcionar valores por defecto cuando no se pasan parámetros.
- **Inicialización Parcial**: Permitir la creación de objetos con solo algunos de los atributos inicializados.
- **Inicialización Completa**: Proporcionar un constructor que inicialice todos los atributos del objeto.

## Conclusión
La sobrecarga de constructores en Java es una técnica poderosa que proporciona flexibilidad y claridad al crear objetos. Permite definir múltiples formas de inicializar un objeto, adaptándose a diferentes necesidades y escenarios.