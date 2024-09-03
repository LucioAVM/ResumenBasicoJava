# Estructuras de Control en Java

## Estructura de Control `if`
Permite ejecutar un bloque de código si una condición es verdadera.

### Sintaxis
```java
if (condicion) {
    // Bloque de código a ejecutar si la condición es verdadera
} else if (otraCondicion) {
    // Bloque de código a ejecutar si la otra condición es verdadera
} else {
    // Bloque de código a ejecutar si ninguna condición anterior es verdadera
}
```

### Ejemplo
```java
int numero = 10;
if (numero > 0) {
    System.out.println("El número es positivo");
} else if (numero < 0) {
    System.out.println("El número es negativo");
} else {
    System.out.println("El número es cero");
}
```

## Estructura de Control `switch`
Permite seleccionar una de entre múltiples opciones basadas en el valor de una expresión.

### Sintaxis
```java
switch (expresion) {
    case valor1:
        // Bloque de código a ejecutar si expresion == valor1
        break;
    case valor2:
        // Bloque de código a ejecutar si expresion == valor2
        break;
    // Más casos...
    default:
        // Bloque de código a ejecutar si ningún caso anterior coincide
}
```

### Ejemplo
```java
int dia = 3;
switch (dia) {
    case 1:
        System.out.println("Lunes");
        break;
    case 2:
        System.out.println("Martes");
        break;
    case 3:
        System.out.println("Miércoles");
        break;
    case 4:
        System.out.println("Jueves");
        break;
    case 5:
        System.out.println("Viernes");
        break;
    case 6:
        System.out.println("Sábado");
        break;
    case 7:
        System.out.println("Domingo");
        break;
    default:
        System.out.println("Día inválido");
}
```

## Bucles (`loops`)
Permiten ejecutar repetidamente un bloque de código mientras una condición sea verdadera.

### Bucle `for`
Se utiliza para iterar un número específico de veces.

#### Sintaxis
```java
for (inicializacion; condicion; actualizacion) {
    // Bloque de código a ejecutar
}
```

#### Ejemplo
```java
for (int i = 0; i < 5; i++) {
    System.out.println("Iteración: " + i);
}
```

### Bucle `while`
Se utiliza para iterar mientras una condición sea verdadera.

#### Sintaxis
```java
while (condicion) {
    // Bloque de código a ejecutar
}
```

#### Ejemplo
```java
int i = 0;
while (i < 5) {
    System.out.println("Iteración: " + i);
    i++;
}
```

### Bucle `do-while`
Similar al bucle `while`, pero garantiza que el bloque de código se ejecute al menos una vez.

#### Sintaxis
```java
do {
    // Bloque de código a ejecutar
} while (condicion);
```

#### Ejemplo
```java
int i = 0;
do {
    System.out.println("Iteración: " + i);
    i++;
} while (i < 5);
```