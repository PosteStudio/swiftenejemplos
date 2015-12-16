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

