# Arrays

Un array en Swift representa una **colleción de valores del mismo tipo**.

```swift
let enteros = [1, 2, 3]
```

En el ejemplo anterior creamos una constante llamada `enteros` y le asignamos un array de enteros usando la notación literal `[1, 2, 3]`. 

Si inspeccionamos la constante `enteros` nos vamos a dar cuenta que su tipo es `Array<Int>`, o sea, array de enteros. 

```bash
1> print(enteros.dynamicType)
Array<Int>
```

Esto significa que el array `enteros` solamente puede contener datos de tipo `Int`. Otra forma de representar el tipo de dato de esta constante es `[Int]`.

Para poder modificar un array después de haber sido creado, es necesario que la declaración del mismo indique que es una varible, no una constante:

```swift
var nombres = ["Oscar", "Marco", "Antonio"]
nombres.append("María") // #=> ["Oscar", "Marco", "Antonio", "Maria"]
nombres.removeFirst()   // #=> ["Marco", "Antonio", "Maria"]
nombres.removeAll()     // #=> []
```

En el listado de código anterior se ejecutaron una serie de métodos sobre el array, modificando su contenido.

Es importante denotar que un array (cualquier variable o constante, realmente) no puede ser manipulada o leída sino hasta después de haber sido inicializado.

```swift
var edades: [Int]   // En este momento, se ha declarado la variable nombres, pero no ha sido inicializada
print(edades.count) // La propiedad count no puede ser usada en este momento
edades = [12, 29, 22, 34]
```

Si intentamos compilar lo anterior, el compilador va a decirnos que estamos intentando usar `edades` antes de haber sido inicializada:

```bash
$ swift array.swift
array.swift:2:1: error: variable 'edades' used before being initialized
edades.count
^
array.swift:1:5: note: variable defined here
var edades: [Int]
    ^
```

Al invertir el orden de las lineas 2 y 3, tenemos el resultado esperado:

```bash
$ swift array.swift
4
```

---

### Referencia:
1. [Documentación oficial de `Array` de Apple](https://developer.apple.com/library/ios/documentation/Swift/Reference/Swift_Array_Structure/index.html)