# Principio de Inversión de Dependencias (DIP) en Programación Orientada a Objetos

## Definición
El Principio de Inversión de Dependencias (Dependency Inversion Principle, DIP) establece que:
1. Los módulos de alto nivel no deben depender de los módulos de bajo nivel. Ambos deben depender de abstracciones.
2. Las abstracciones no deben depender de los detalles. Los detalles deben depender de las abstracciones.

## Conceptos Claves
- **Módulos de Alto Nivel**: Componentes que contienen la lógica de negocio y las reglas del dominio.
- **Módulos de Bajo Nivel**: Componentes que implementan detalles específicos, como acceso a bases de datos o servicios externos.
- **Abstracciones**: Interfaces o clases abstractas que definen contratos sin implementar detalles específicos.

## Importancia
- **Desacoplamiento**: Reduce la dependencia entre módulos, facilitando cambios y mejoras en el sistema.
- **Flexibilidad**: Permite cambiar implementaciones de bajo nivel sin afectar los módulos de alto nivel.
- **Testabilidad**: Facilita la creación de pruebas unitarias al permitir el uso de mocks o stubs.

## Ejemplo de Uso
### Definición de Interfaces y Clases
```java
// Interfaz que define el contrato
public interface ServicioNotificacion {
    void enviarMensaje(String mensaje);
}

// Implementación concreta del servicio de notificación
public class EmailNotificacion implements ServicioNotificacion {
    @Override
    public void enviarMensaje(String mensaje) {
        System.out.println("Enviando email: " + mensaje);
    }
}

// Clase de alto nivel que depende de la abstracción
public class GestorPedidos {
    private ServicioNotificacion servicioNotificacion;

    public GestorPedidos(ServicioNotificacion servicioNotificacion) {
        this.servicioNotificacion = servicioNotificacion;
    }

    public void procesarPedido(String pedido) {
        // Lógica de procesamiento del pedido
        servicioNotificacion.enviarMensaje("Pedido procesado: " + pedido);
    }
}
```

### Uso de las Clases con Inversión de Dependencias
```java
public class Main {
    public static void main(String[] args) {
        ServicioNotificacion notificacion = new EmailNotificacion();
        GestorPedidos gestor = new GestorPedidos(notificacion);

        gestor.procesarPedido("12345");
    }
}
```

## Casos de Uso Comunes
- **Sistemas de Notificación**: Permitir diferentes métodos de notificación (email, SMS, push) sin cambiar la lógica de negocio.
- **Acceso a Datos**: Cambiar la fuente de datos (base de datos, archivos, servicios web) sin modificar los módulos de alto nivel.
- **Inyección de Dependencias**: Utilizar frameworks de inyección de dependencias para gestionar las dependencias entre componentes.

## Conclusión
El Principio de Inversión de Dependencias es crucial para crear sistemas desacoplados y flexibles. Al depender de abstracciones en lugar de implementaciones concretas, se facilita el mantenimiento, la escalabilidad y la testabilidad del código.