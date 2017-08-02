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
