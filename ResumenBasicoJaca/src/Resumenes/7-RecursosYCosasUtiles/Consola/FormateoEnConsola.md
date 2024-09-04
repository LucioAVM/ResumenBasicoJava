| Formato | Descripción                                      | Ejemplo de Uso                  | Resultado Ejemplo             |
|---------|--------------------------------------------------|---------------------------------|-------------------------------|
| %d      | Entero decimal                                   | `String.format("%d", 123)`      | 123                           |
| %f      | Número de punto flotante                         | `String.format("%.2f", 123.456)`| 123.46                        |
| %s      | Cadena de caracteres                             | `String.format("%s", "Hola")`   | Hola                          |
| %x      | Entero en formato hexadecimal                    | `String.format("%x", 255)`      | ff                            |
| %o      | Entero en formato octal                          | `String.format("%o", 8)`        | 10                            |
| %c      | Carácter                                         | `String.format("%c", 'A')`      | A                             |
| %b      | Booleano                                         | `String.format("%b", true)`     | true                          |
| %e      | Número de punto flotante en notación científica  | `String.format("%e", 123.456)`  | 1.234560e+02                  |
| %t      | Fecha y hora                                     | `String.format("%tF", new Date())` | 2024-09-03 (por ejemplo)     |
| %%      | Porcentaje literal                               | `String.format("%%")`           | %                             |
| %n      | Salto de línea                                   | `String.format("Hola%nMundo")`  | Hola                          |
