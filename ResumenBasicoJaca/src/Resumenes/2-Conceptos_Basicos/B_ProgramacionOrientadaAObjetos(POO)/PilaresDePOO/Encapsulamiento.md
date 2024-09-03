# Encapsulamiento en Java

## Definición
El encapsulamiento es uno de los pilares fundamentales de la Programación Orientada a Objetos (POO). Consiste en ocultar los detalles internos de una clase y exponer solo lo necesario a través de métodos públicos. Esto ayuda a proteger los datos y a mantener la integridad del objeto.

## Beneficios del Encapsulamiento
- **Protección de Datos**: Evita el acceso no autorizado y la modificación de los datos internos de un objeto.
- **Mantenimiento**: Facilita la modificación del código sin afectar a otras partes del programa.
- **Reutilización**: Permite reutilizar el código de manera más segura y eficiente.

## Implementación en Java
Para implementar el encapsulamiento en Java, se utilizan modificadores de acceso y métodos de acceso (getters) y modificación (setters).

### Modificadores de Acceso
- **private**: Restringe el acceso a los miembros de la clase solo dentro de la misma clase.
- **public**: Permite el acceso a los miembros de la clase desde cualquier otra clase.
- **protected**: Permite el acceso a los miembros de la clase dentro de la misma clase y en clases derivadas (subclases).
- **default (sin modificador)**: Permite el acceso a los miembros de la clase dentro del mismo paquete.

### Ejemplo de Encapsulamiento
```java
public class CuentaBancaria {
    // Atributos privados
    private double saldo;

    // Constructor
    public CuentaBancaria(double saldoInicial) {
        this.saldo = saldoInicial;
    }

    // Métodos públicos para acceder y modificar el saldo
    public double getSaldo() {
        return saldo;
    }

    public void depositar(double cantidad) {
        if (cantidad > 0) {
            saldo += cantidad;
        }
    }

    public void retirar(double cantidad) {
        if (cantidad > 0 && cantidad <= saldo) {
            saldo -= cantidad;
        }
    }
}
```

### Uso de la Clase Encapsulada
```java
public class Main {
    public static void main(String[] args) {
        // Crear una instancia de CuentaBancaria
        CuentaBancaria cuenta = new CuentaBancaria(1000.0);

        // Acceder al saldo usando el método getter
        System.out.println("Saldo inicial: " + cuenta.getSaldo());

        // Modificar el saldo usando los métodos setter
        cuenta.depositar(500.0);
        System.out.println("Saldo después del depósito: " + cuenta.getSaldo());

        cuenta.retirar(200.0);
        System.out.println("Saldo después del retiro: " + cuenta.getSaldo());
    }
}
```

## Conclusión
El encapsulamiento es una práctica esencial en la POO que ayuda a proteger los datos y a mantener la integridad del objeto. Utilizando modificadores de acceso y métodos de acceso y modificación, se puede controlar cómo se accede y se modifica el estado interno de un objeto.