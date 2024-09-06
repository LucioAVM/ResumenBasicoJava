# Clases Y Objetos en Java

## Clases
Una clase es una plantilla para crear objetos. Define atributos y métodos que los objetos creados a partir de la clase tendrán.

### Sintaxis

```java
public class NombreDeLaClase {
    // Atributos
    tipo atributo1;
    tipo atributo2;

    // Constructor
    public NombreDeLaClase(tipo parametro1, tipo parametro2) {
        this.atributo1 = parametro1;
        this.atributo2 = parametro2;
    }

    // Métodos
    public void metodo1() {
        // Código del método
    }

    public tipo metodo2() {
        // Código del método
        return valor;
    }
}
```

### Ejemplo
```java
public class Persona {
    // Atributos
    String nombre;
    int edad;

    // Constructor
    public Persona(String nombre, int edad) {
        this.nombre = nombre;
        this.edad = edad;
    }

    // Métodos
    public void mostrarInformacion() {
        System.out.println("Nombre: " + nombre);
        System.out.println("Edad: " + edad);
    }
}
```

## Objetos
Un objeto es una instancia de una clase. Se crea utilizando la palabra clave `new`.

### Sintaxis
```java
NombreDeLaClase objeto = new NombreDeLaClase(parametro1, parametro2);
```

### Ejemplo
```java
public class Main {
    public static void main(String[] args) {
        // Crear un objeto de la clase Persona
        Persona persona1 = new Persona("Juan", 25);

        // Llamar a un método del objeto
        persona1.mostrarInformacion();
    }
}
```

## Métodos
Un método es un bloque de código que realiza una tarea específica y puede ser llamado desde otras partes del programa.

### Sintaxis
```java
public class NombreDeLaClase {
    // Método sin valor de retorno
    public void nombreDelMetodo() {
        // Código del método
    }

    // Método con valor de retorno
    public tipo nombreDelMetodoConRetorno() {
        // Código del método
        return valor;
    }

    // Método con parámetros
    public void nombreDelMetodoConParametros(tipo parametro1, tipo parametro2) {
        // Código del método
    }
}
```

### Ejemplo
```java
public class Calculadora {
    // Método sin valor de retorno
    public void saludar() {
        System.out.println("Hola, bienvenido a la calculadora!");
    }

    // Método con valor de retorno
    public int sumar(int a, int b) {
        return a + b;
    }

    // Método con parámetros
    public void imprimirSuma(int a, int b) {
        int suma = a + b;
        System.out.println("La suma de " + a + " y " + b + " es: " + suma);
    }
}
```

### Llamada a Métodos
```java
public class Main {
    public static void main(String[] args) {
        // Crear un objeto de la clase Calculadora
        Calculadora calc = new Calculadora();

        // Llamar a un método sin valor de retorno
        calc.saludar();

        // Llamar a un método con valor de retorno
        int resultado = calc.sumar(5, 3);
        System.out.println("Resultado de la suma: " + resultado);

        // Llamar a un método con parámetros
        calc.imprimirSuma(5, 3);
    }
}
```

# Conceptos
> - **Clase**: Plantilla para crear objetos.
> - **Objeto**: Instancia de una clase.
> - **Atributo**: Variables de una clase.
> - **Método**: Funciones de una clase.
> - **Constructor**: Método especial para inicializar objetos.
> - **Palabra clave `this`**: Hace referencia al objeto actual.