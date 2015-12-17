# Variables

Una variable en Swift se declara con la palabra reservada `var`.

```swift
var nombre = "Oscar"
```

Las variables son conocidos como "valores mutables" dentro de Swift, no precisamente "variables."

Una de las ventajas de Swift es su excelente sistema de inferencia de tipos de datos, lo que significa que el compilador automáticamente sabe de qué tipo es tu variable sin la necesidad de expresarlo explícitamente.

El ejemplo anterior declara una variable de tipo `String`, ya que del lado derecho del signo de asignación (`=`) pusimos una representación literal de un `String`.

Si queremos declarar una variable sin asignarle un valor inicial (como en el ejemplo anterior), podemos hacerlo declarando el tipo de dato que espera la variable:

```swift
var nombre: String  // #=> Declarar la variable nombre de tipo String sin asignar un valor inicial
nombre = "Oscar"
```

En ambos casos, la variable `nombre` durante el resto de la ejecución de nuestro programa, sólo podrá contener `String`s.

Una variable en Swift puede ser modificada en tiempo de ejecución, siempre y cuando se respete su tipo.

```swift
print(nombre)       // => Oscar
nombre = "Marco"    // #=> Ahora nombre es igual a "Marco"
print(nombre)       // => Marco
nombre = 2          // #=> Error! 2 no un tipo de dato String
```