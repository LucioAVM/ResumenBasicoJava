# Principio de Segregación de Interfaces (ISP) en Programación Orientada a Objetos

## Definición
El **Principio de Segregación de Interfaces (Interface Segregation Principle, ISP)** establece que una clase no debe estar obligada a implementar interfaces que no utiliza. En lugar de tener una interfaz grande, es mejor tener varias interfaces específicas y pequeñas.

## Conceptos Claves
- **Interfaces Específicas**: Interfaces que definen métodos relacionados con una única funcionalidad.
- **Desacoplamiento**: Reducir la dependencia entre clases y sus interfaces.
- **Cohesión**: Aumentar la cohesión al tener interfaces que agrupan métodos relacionados.

## Importancia
- **Mantenibilidad**: Facilita la modificación y mantenimiento del código, ya que las clases solo implementan métodos que realmente utilizan.
- **Flexibilidad**: Permite cambiar o extender funcionalidades sin afectar otras partes del sistema.
- **Reutilización de Código**: Promueve la reutilización de interfaces y clases en diferentes contextos.

## Ejemplo de Uso
### Interfaces Específicas
```java
public interface Imprimible {
    void imprimir();
}

public interface Guardable {
    void guardar(String rutaArchivo);
}
```

### Clases que Implementan Interfaces Específicas
```java
public class Reporte implements Imprimible, Guardable {
    private String contenido;

    public Reporte(String contenido) {
        this.contenido = contenido;
    }

    @Override
    public void imprimir() {
        System.out.println("Imprimiendo reporte: " + contenido);
    }

    @Override
    public void guardar(String rutaArchivo) {
        System.out.println("Guardando reporte en: " + rutaArchivo);
    }
}

public class Documento implements Imprimible {
    private String texto;

    public Documento(String texto) {
        this.texto = texto;
    }

    @Override
    public void imprimir() {
        System.out.println("Imprimiendo documento: " + texto);
    }
}
```

### Uso de las Clases con Interfaces Específicas
```java
public class Main {
    public static void main(String[] args) {
        Reporte reporte = new Reporte("Contenido del reporte");
        Documento documento = new Documento("Texto del documento");

        reporte.imprimir();
        reporte.guardar("ruta/al/archivo.txt");
        documento.imprimir();
    }
}
```

## Casos de Uso Comunes
- **Sistemas de Reportes**: Separar la lógica de impresión y almacenamiento en diferentes interfaces.
- **Gestión de Archivos**: Definir interfaces específicas para operaciones de lectura, escritura y eliminación de archivos.
- **Servicios Web**: Crear interfaces específicas para diferentes tipos de operaciones (GET, POST, PUT, DELETE).

## Conclusión
El Principio de Segregación de Interfaces es esencial para crear sistemas flexibles y mantenibles. Al definir interfaces específicas y pequeñas, se reduce el acoplamiento y se aumenta la cohesión, facilitando la evolución y reutilización del código.