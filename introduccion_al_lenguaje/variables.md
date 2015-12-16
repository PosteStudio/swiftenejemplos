# Variables

Una variable en Swift se declara con la palabra reservada `var`.

```swift
var nombre = "Oscar"
```

Una de las ventajas de Swift es su excelente sistema de inferencia de tipos de datos, lo que significa que el compilador automáticamente sabe de qué tipo es tu variable sin la necesidad de expresarlo explícitamente.

El ejemplo anterior declara una variable de tipo `String` (cadena de texto) ya que del lado derecho del signo de asignación (`=`) pusimos una representación literal de un `String`.

Si queremos declarar una variable sin asignarle un valor inicial (como en el ejemplo anterior), podemos hacerlo declarando el tipo de dato que espera la variable:

```swift
var nombre: String
```

En ambos casos, la variable `nombre` durante el resto de la ejecución de nuestro programa, sólo podrá contener `String`s.