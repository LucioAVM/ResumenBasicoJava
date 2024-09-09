# Principio de Responsabilidad Única (SRP) en Programación Orientada a Objetos

## Definición
El **Principio de Responsabilidad Única (Single Responsibility Principle, SRP)** establece que una clase o módulo debe tener una única razón para cambiar, es decir, debe tener una sola responsabilidad o propósito.

## Conceptos Claves
- **Responsabilidad Única**: Cada clase debe encargarse de una única funcionalidad o tarea.
- **Razón para Cambiar**: Una clase debe tener solo una razón para ser modificada, lo que implica que debe estar enfocada en una única responsabilidad.

## Importancia
- **Mantenibilidad**: Facilita la comprensión y mantenimiento del código, ya que cada clase tiene una única responsabilidad.
- **Reutilización de Código**: Promueve la reutilización de clases en diferentes contextos, ya que están enfocadas en una tarea específica.
- **Testabilidad**: Mejora la testabilidad del código, ya que las clases con una única responsabilidad son más fáciles de probar.

## Ejemplo de Uso
### Clase con Responsabilidad Única
```java
public class Reporte {
    private String contenido;

    public Reporte(String contenido) {
        this.contenido = contenido;
    }

    public String getContenido() {
        return contenido;
    }
}
```

### Clase para Guardar el Reporte
```java
public class ReporteGuardado {
    public void guardar(Reporte reporte, String rutaArchivo) {
        // Lógica para guardar el reporte en un archivo
        System.out.println("Guardando reporte en: " + rutaArchivo);
    }
}
```

### Clase para Imprimir el Reporte
```java
public class ReporteImpresion {
    public void imprimir(Reporte reporte) {
        // Lógica para imprimir el reporte
        System.out.println("Imprimiendo reporte: " + reporte.getContenido());
    }
}
```

### Uso de las Clases con Responsabilidad Única
```java
public class Main {
    public static void main(String[] args) {
        Reporte reporte = new Reporte("Contenido del reporte");
        ReporteGuardado guardado = new ReporteGuardado();
        ReporteImpresion impresion = new ReporteImpresion();

        guardado.guardar(reporte, "ruta/al/archivo.txt");
        impresion.imprimir(reporte);
    }
}
```

## Casos de Uso Comunes
- **Generación de Reportes**: Separar la lógica de generación, almacenamiento e impresión de reportes en diferentes clases.
- **Gestión de Usuarios**: Dividir la lógica de autenticación, autorización y perfil de usuario en clases separadas.
- **Procesamiento de Datos**: Separar la lógica de validación, transformación y almacenamiento de datos en diferentes clases.

## Conclusión
El Principio de Responsabilidad Única es esencial para crear sistemas mantenibles y fáciles de entender. Al asignar una única responsabilidad a cada clase, se mejora la claridad, la reutilización y la testabilidad del código.