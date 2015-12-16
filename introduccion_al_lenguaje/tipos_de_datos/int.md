# `Int`

Un valor de tipo `Int` representa un número entero, que puede tener un signo positivo o negativo. Hay una variante de este tipo de dato que solamente representa números positivos: `UInt`.

`Int` también tiene variaciones específicas para representar enteros en plataformas con diferentes arquitecturas: `Int32`/`UInt32` para plataformas de 32 bits, y `Int64`/`UInt64` para plataformas de 64 bits. 

Sin embargo, no debes de preocuparte por esto, ya que:

* En plataformas de 32 bits, `Int` tendrá el mismo tamaño que `Int32`
* En plataformas de 64 bits, `Int` tendrá el mismo tamaño que `UInt64`

Lo anterior es cierto tambíen para `UInt` y sus variantes.


### Representación literal
```swift
let dedosEnLaMano = 5
let autosEnLaCochera = 2
let estrellasEnElCielo = 1_000_000 // Puedes usar _ entre números para mejorar la legibilidad
```