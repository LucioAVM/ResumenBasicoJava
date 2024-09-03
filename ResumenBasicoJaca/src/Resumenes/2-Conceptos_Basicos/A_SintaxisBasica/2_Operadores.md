# Operadores en Java

## Operadores Aritméticos
Se utilizan para realizar operaciones matemáticas.

- **Suma (`+`)**: Suma dos operandos.
- **Resta (`-`)**: Resta el segundo operando del primero.
- **Multiplicación (`*`)**: Multiplica dos operandos.
- **División (`/`)**: Divide el primer operando por el segundo.
- **Módulo (`%`)**: Devuelve el resto de la división del primer operando por el segundo.

```java
int a = 10;
int b = 5;
int suma = a + b; // 15
int resta = a - b; // 5
int multiplicacion = a * b; // 50
int division = a / b; // 2
int modulo = a % b; // 0
```

## Operadores de Asignación
Se utilizan para asignar valores a las variables.

- **Asignación (`=`)**: Asigna el valor del operando derecho al operando izquierdo.
- **Asignación con suma (`+=`)**: Suma el operando derecho al operando izquierdo y asigna el resultado al operando izquierdo.
- **Asignación con resta (`-=`)**: Resta el operando derecho del operando izquierdo y asigna el resultado al operando izquierdo.
- **Asignación con multiplicación (`*=`)**: Multiplica el operando derecho por el operando izquierdo y asigna el resultado al operando izquierdo.
- **Asignación con división (`/=`)**: Divide el operando izquierdo por el operando derecho y asigna el resultado al operando izquierdo.
- **Asignación con módulo (`%=`)**: Calcula el módulo del operando izquierdo por el operando derecho y asigna el resultado al operando izquierdo.

```java
int c = 10;
c += 5; // c = 15
c -= 3; // c = 12
c *= 2; // c = 24
c /= 4; // c = 6
c %= 3; // c = 0
```

## Operadores Relacionales
Se utilizan para comparar dos valores.

- **Igual a (`==`)**: Devuelve `true` si los operandos son iguales.
- **No igual a (`!=`)**: Devuelve `true` si los operandos no son iguales.
- **Mayor que (`>`)**: Devuelve `true` si el operando izquierdo es mayor que el derecho.
- **Menor que (`<`)**: Devuelve `true` si el operando izquierdo es menor que el derecho.
- **Mayor o igual que (`>=`)**: Devuelve `true` si el operando izquierdo es mayor o igual que el derecho.
- **Menor o igual que (`<=`)**: Devuelve `true` si el operando izquierdo es menor o igual que el derecho.

```java
int d = 10;
int e = 5;
boolean igual = (d == e); // false
boolean noIgual = (d != e); // true
boolean mayor = (d > e); // true
boolean menor = (d < e); // false
boolean mayorIgual = (d >= e); // true
boolean menorIgual = (d <= e); // false
```

## Operadores Lógicos
Se utilizan para combinar expresiones booleanas.

- **AND lógico (`&&`)**: Devuelve `true` si ambas expresiones son `true`.
- **OR lógico (`||`)**: Devuelve `true` si al menos una de las expresiones es `true`.
- **NOT lógico (`!`)**: Invierte el valor de una expresión booleana.

```java
boolean f = true;
boolean g = false;
boolean and = (f && g); // false
boolean or = (f || g); // true
boolean not = !f; // false
```

## Operadores Unarios
Se aplican a un solo operando.

- **Incremento (`++`)**: Incrementa el valor del operando en 1.
- **Decremento (`--`)**: Decrementa el valor del operando en 1.
- **Negación (`-`)**: Invierte el signo del operando.
- **Complemento lógico (`!`)**: Invierte el valor booleano del operando.

```java
int h = 10;
h++; // h = 11
h--; // h = 10
int neg = -h; // neg = -10
boolean i = true;
boolean notI = !i; // notI = false
```

## Operadores de Bits
Se utilizan para realizar operaciones a nivel de bits.

- **AND a nivel de bits (`&`)**: Realiza una operación AND a nivel de bits.
- **OR a nivel de bits (`|`)**: Realiza una operación OR a nivel de bits.
- **XOR a nivel de bits (`^`)**: Realiza una operación XOR a nivel de bits.
- **Complemento a nivel de bits (`~`)**: Invierte todos los bits del operando.
- **Desplazamiento a la izquierda (`<<`)**: Desplaza los bits del operando a la izquierda.
- **Desplazamiento a la derecha (`>>`)**: Desplaza los bits del operando a la derecha.
- **Desplazamiento a la derecha sin signo (`>>>`)**: Desplaza los bits del operando a la derecha sin signo.

```java
int j = 5; // 0101 en binario
int k = 3; // 0011 en binario
int andBits = j & k; // 0001 en binario, 1 en decimal
int orBits = j | k; // 0111 en binario, 7 en decimal
int xorBits = j ^ k; // 0110 en binario, 6 en decimal
int notBits = ~j; // 1010 en binario (complemento a dos), -6 en decimal
int leftShift = j << 1; // 1010 en binario, 10 en decimal
int rightShift = j >> 1; // 0010 en binario, 2 en decimal
int unsignedRightShift = j >>> 1; // 0010 en binario, 2 en decimal
```

## Operador Ternario
Es una forma abreviada de la instrucción `if-else`.

- **Sintaxis**: `condicion ? valor1 : valor2`

```java
int l = 10;
int m = (l > 5) ? 1 : 0; // m = 1
```