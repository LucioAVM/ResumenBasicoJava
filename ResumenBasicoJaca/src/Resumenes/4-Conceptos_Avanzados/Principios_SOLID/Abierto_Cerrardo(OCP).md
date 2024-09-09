# Principio Abierto/Cerrado (OCP) en Programación Orientada a Objetos

## Definición
El Principio Abierto/Cerrado (Open/Closed Principle, OCP) establece que las entidades de software (clases, módulos, funciones, etc.) deben estar abiertas para la extensión, pero cerradas para la modificación. Esto significa que el comportamiento de una entidad puede extenderse sin modificar su código fuente.

## Conceptos Claves
- **Extensión**: Añadir nuevas funcionalidades sin alterar el código existente.
- **Modificación**: Cambiar el código existente, lo cual puede introducir errores y afectar la estabilidad del sistema.
- **Polimorfismo**: Utilizar interfaces y clases abstractas para permitir la extensión del comportamiento.

## Importancia
- **Mantenibilidad**: Facilita la adición de nuevas funcionalidades sin riesgo de introducir errores en el código existente.
- **Escalabilidad**: Permite que el sistema crezca de manera ordenada y controlada.
- **Reutilización de Código**: Promueve la reutilización de componentes existentes mediante la extensión.

## Ejemplo de Uso
### Clase Base y Extensiones
```java
// Clase base cerrada para modificación
public abstract class Empleado {
    protected String nombre;
    protected double salario;

    public Empleado(String nombre, double salario) {
        this.nombre = nombre;
        this.salario = salario;
    }

    public abstract double calcularBonificacion();
}

// Clase que extiende la funcionalidad
public class EmpleadoTiempoCompleto extends Empleado {
    public EmpleadoTiempoCompleto(String nombre, double salario) {
        super(nombre, salario);
    }

    @Override
    public double calcularBonificacion() {
        return this.salario * 0.1;
    }
}

// Otra clase que extiende la funcionalidad
public class EmpleadoMedioTiempo extends Empleado {
    public EmpleadoMedioTiempo(String nombre, double salario) {
        super(nombre, salario);
    }

    @Override
    public double calcularBonificacion() {
        return this.salario * 0.05;
    }
}
```

### Uso de las Clases Extensibles
```java
public class Main {
    public static void main(String[] args) {
        Empleado emp1 = new EmpleadoTiempoCompleto("Juan", 50000);
        Empleado emp2 = new EmpleadoMedioTiempo("Ana", 25000);

        System.out.println(emp1.calcularBonificacion()); // Salida: 5000.0
        System.out.println(emp2.calcularBonificacion()); // Salida: 1250.0
    }
}
```

## Casos de Uso Comunes
- **Sistemas de Pago**: Extender el cálculo de bonificaciones o descuentos sin modificar el código base.
- **Procesamiento de Datos**: Añadir nuevos tipos de procesamiento sin alterar el código existente.
- **Desarrollo de Plugins**: Permitir la adición de nuevas funcionalidades mediante plugins o módulos externos.

## Conclusión
El Principio Abierto/Cerrado es fundamental para crear sistemas flexibles y mantenibles. Permite extender el comportamiento de las entidades de software sin modificar su código fuente, lo que reduce el riesgo de errores y facilita la evolución del sistema.