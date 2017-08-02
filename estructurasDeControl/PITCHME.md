![](https://kotlinlang.org/assets/images/twitter-card/kotlin_800x320.png)

### Estructuras de Control

---

## Operadores Condicionales

En *Kotlin* tenemos:

| Operador | Significado     | Expresión |
|----------|-----------------|-----------|
| `>`        | Mayor que       | `a > b`     |
| `<`        | Menor que       | `a < b`     |
| `>=`       | Mayor o igual a | `a >= b`    |
| `<=`       | Menor o igual a | `a <= b`    |
| `==`       | Es igual a      | `a == b`    |
| `!=`       | No es igual a   | `a != b`    |

---

## Operadores Lógicos

Tenemos 3 operadores en *Kotlin*:

| Operador | Descripción                              | Expresión        |
|----------|------------------------------------------|------------------|
| `&&`     | `true`si ambas expresiones son `true`    | `(a>b) && (a<c)` |
| `\|\|`   | `false` si ambas expresiones son `false` | `(a>b) \|\| (a<c)` |
| `!`      | `true` si la expresión es false          | `!(a <= b)`      |

---

## El operador `in`

Este operador permite saber si un elemento pertenece o no a una colección o rango


| Operador | Expresión                              | Ejemplo |
|----------|------------------------------------------|------------------|
| `in`     | `a in b` | `numero in 10..99` |
| `!in`    | `a !in b` | `letra !in 'A' .. 'Z'` |

---

## Instrucción `if`

```kotlin
val mayor = a

if (b >= mayor) {
    mayor = b
}
```

---

## Instrucción `if` / `else`

```kotlin
if (a > b) {
    mayor = a
}
else {
    mayor = b
}
```

---

## Expresión `if` 

```kotlin
var numCifras = if (n in 0 .. 9) {
        1
    }
    else if (n in 10 .. 99) {
        2
    }
    else {
        3
     }
```
---

## La instrucción `when`

Permite seleccionar un acción dependiendo de múltiples valores de una variable o valor.

```kotlin
when (dia) {
    0 -> return "domingo"
    1 -> return "lunes"
    2 -> return "martes"
    3 -> return "miércoles"
    4 -> return "jueves"
    5 -> return "viernes"
    6 -> return "sábado"
    else -> return "ERROR
}
```
---

# El operador `when`

`when` también puede usarse en lugar de una expresión aritmética o asignación 
```kotlin
val tipo = when (dia) {
    0, 6 -> "fin de semana"
    in 1..5 -> "día laboral"
    else -> "raro!"
}
```

---

## Instrucciones repetitivas - el `for`

Esta instrucción permite realizar un conjunto de instrucciones un número determinado de veces. *Kotlin* ofrece múltiples
opciones para trabajar con esta instrucción...

```kotlin
for (i in 1..10) { }

for (i in 1 until 10) { }

for (i in 10 downTo 0) { }

for (i in 1..10 step 2) { }

for (i in 10 downTo 1 step 2) { }

for (item in collection) { }
```

---

## La instrucción `while`

El `while` en *Kotlin*  funciona igual que en otros lenguajes de programación. Repetir hasta que la condición sea falsa.

![Instrucción While](https://cdn.programiz.com/sites/tutorial2program/files/kotlin-while-loop-flowchart.jpg)

El siguiente ejemplo halla la raíz cuadrada entera de un número entero

```kotlin
fun raizCuadrada(n: Int): Int {
    val i = 1
    while (i * i <= n) {
        i++
    }
    return if (i * i == n) i else i - 1
}
```

---

## La instrucción `do/while`

Muy parecida a la instrucción `while`, solo que la condición de salida se evalúa después del cuerpo de la instrucción.

![DO..While](https://cdn.programiz.com/sites/tutorial2program/files/kotlin-do-while-loop.jpg)

El siguiente ejemplo lee una serie de números desde teclado y genera la suma hasta que se ingresa un cero.

```kotlin
fun main(args: Array<String>) {

    var suma: Int = 0
    var número: String

    do {
        print("Entre un número entero: ")
        número = readLine()!!
        suma += número.toInt()

    } while (número != "0")

    println("La Suma Es = $suma")
}
```

---

## Operaciones comunes con los números

Sin importar el tipo de datos, todos los tipos numéricos de *Kotlin*  soportan las siguientes operaciones

- `toByte(): Byte`
- `toChar(): Char`
- `toDouble(): Double`
- `toString(): String`
- `fun dec(): Int`: Para decrementar el valor de la variable
- `fun inc(): Int`: Para incrementar el valor de la variable
- `MAX_VALUE`: el número más grande, dependiendo del tipo
- `MIN_VALUE`: el número más pequeño, dependiendo del tipo

