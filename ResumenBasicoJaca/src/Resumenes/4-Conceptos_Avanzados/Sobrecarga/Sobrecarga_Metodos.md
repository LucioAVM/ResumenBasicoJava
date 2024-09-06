# Sobrecarga de Métodos en Java

## Definición
La sobrecarga de métodos en Java permite definir múltiples métodos con el mismo nombre pero diferentes parámetros en una clase. Esto proporciona flexibilidad para realizar la misma operación de diferentes maneras.

## Conceptos Claves
- **Método**: Bloque de código que realiza una tarea específica.
- **Sobrecarga**: Definir múltiples métodos con el mismo nombre pero diferentes parámetros.
- **Parámetros**: Los argumentos que se pasan al método para realizar la operación.

## Beneficios de la Sobrecarga de Métodos
- **Flexibilidad**: Permite realizar la misma operación con diferentes tipos o cantidades de datos.
- **Reutilización de Código**: Facilita la reutilización de código al permitir diferentes implementaciones en una sola clase.
- **Claridad**: Mejora la claridad del código al proporcionar métodos específicos para diferentes escenarios.

## Ejemplo de Uso
### Clase con Sobrecarga de Métodos
```java
public class Calculadora {
    // Método para sumar dos enteros
    public int sumar(int a, int b) {
        return a + b;
    }

    // Método para sumar tres enteros
    public int sumar(int a, int b, int c) {
        return a + b + c;
    }

    // Método para sumar dos números de punto flotante
    public double sumar(double a, double b) {
        return a + b;
    }
}
```

### Uso de los Métodos Sobrecargados
```java
public class Main {
    public static void main(String[] args) {
        Calculadora calc = new Calculadora();

        System.out.println(calc.sumar(2, 3)); // Salida: 5
        System.out.println(calc.sumar(2, 3, 4)); // Salida: 9
        System.out.println(calc.sumar(2.5, 3.5)); // Salida: 6.0
    }
}
```

## Casos de Uso Comunes
- **Operaciones Matemáticas**: Realizar operaciones matemáticas con diferentes tipos o cantidades de datos.
- **Conversión de Datos**: Convertir datos de un tipo a otro con diferentes parámetros.
- **Procesamiento de Datos**: Procesar datos de diferentes maneras según los parámetros proporcionados.

## Conclusión
La sobrecarga de métodos en Java es una técnica poderosa que proporciona flexibilidad y claridad al realizar operaciones. Permite definir múltiples formas de realizar una operación, adaptándose a diferentes necesidades y escenarios.