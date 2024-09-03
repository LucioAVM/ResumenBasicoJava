# Variables y Tipos de Datos en Java

## Variables

### Declaración de Variables
En Java, una variable debe ser declarada antes de ser utilizada. La declaración de una variable incluye el tipo de dato y el nombre de la variable.

```java
int edad;
double salario;
String nombre;
```

### Inicialización de Variables
Una variable puede ser inicializada en el momento de su declaración o posteriormente.

```java
int edad = 25;
double salario = 3000.50;
String nombre = "Juan";
```

### Tipos de Variables
- **Variables locales**: Declaradas dentro de un método y solo accesibles dentro de ese método.
- **Variables de instancia**: Declaradas dentro de una clase pero fuera de cualquier método. Son accesibles por todos los métodos de la clase.
- **Variables de clase (estáticas)**: Declaradas con la palabra clave `static` dentro de una clase pero fuera de cualquier método. Son compartidas por todas las instancias de la clase.

## Tipos de Datos

### Tipos de Datos Primitivos
Java tiene ocho tipos de datos primitivos:

- **byte**: 8 bits, rango de -128 a 127.
- **short**: 16 bits, rango de -32,768 a 32,767.
- **int**: 32 bits, rango de -2^31 a 2^31-1.
- **long**: 64 bits, rango de -2^63 a 2^63-1.
- **float**: 32 bits, precisión simple.
- **double**: 64 bits, precisión doble.
- **char**: 16 bits, un solo carácter Unicode.
- **boolean**: true o false.

```java
byte b = 100;
short s = 10000;
int i = 100000;
long l = 100000L;
float f = 10.5f;
double d = 10.5;
char c = 'A';
boolean bool = true;
```

### Tipos de Datos No Primitivos
- **String**: Una secuencia de caracteres.
- **Arrays**: Una colección de elementos del mismo tipo.
- **Clases**: Definidas por el usuario.
- **Interfaces**: Definidas por el usuario.

```java
String saludo = "Hola, Mundo";
int[] numeros = {1, 2, 3, 4, 5};
```

### Conversión de Tipos
- **Conversión implícita**: Automática cuando se asigna un valor de un tipo de dato más pequeño a uno más grande.

```java
int i = 100;
long l = i; // Conversión implícita
```

- **Conversión explícita (casting)**: Necesaria cuando se asigna un valor de un tipo de dato más grande a uno más pequeño.

```java
long l = 100L;
int i = (int) l; // Conversión explícita
```

## Ejemplos

### Ejemplo de Declaración e Inicialización

```java
public class VariablesEjemplo {
    public static void main(String[] args) {
        int edad = 25;
        double salario = 3000.50;
        String nombre = "Juan";

        System.out.println("Nombre: " + nombre);
        System.out.println("Edad: " + edad);
        System.out.println("Salario: " + salario);
    }
}
```

### Ejemplo de Conversión de Tipos

```java
public class ConversionTipos {
    public static void main(String[] args) {
        int i = 100;
        long l = i; // Conversión implícita
        System.out.println("Valor de l: " + l);

        long l2 = 100L;
        int i2 = (int) l2; // Conversión explícita
        System.out.println("Valor de i2: " + i2);
    }
}
```
