# Introducción al lenguaje
Swift es un lenguaje de programación increíble: su sintáxis es limpia, entendible (casi como pseudocódigo) sin sacrificar rendimiento y/ó velocidad.


## Aplicaciones
Si este es tu primer intento de aprender Swift, hay algo que debes saber: **Swift no solamente funciona para crear aplicaciones para iOS/OS X.** 

Al contrario, Apple ha dicho que el objetivo de Swift es que sea un lenguaje de programación lo suficientemente simple para que sea el lenguaje con el que se enseñen a programar las nuevas generaciones, pero lo suficientemente poderoso para que puedas escribir un sistema operativo completo.

De hecho, gracias al nuevo status de *open source* de Swift, ya incluso tenemos frameworks para [crear servicios web](http://perfect.org) o [aplicaciones de ](github.com/SwiftAndroid/swift)Android. Ambos, usando Swift.


## Tu primer programa con Swift

[Siguiendo la costumbre](https://es.wikipedia.org/wiki/Hola_mundo), el primer programa que escribirás en cualquier lenguaje de programación será el *Hola Mundo.*

Crea un archivo de texto `holamundo.swift` en tu escritorio y escribe lo siguiente dentro:

```swift
print("Hola mundo!")
```

Ahora, desde tu terminal navega a tu escritorio y escribe lo siguiente y presiona `Enter`:

```bash
$ swift holamundo.swift
```

Después de unos momentos verás un texto aparecer debajo de tu instrucción:

```bash
$ swift holamundo.swift
Hola mundo!
```

Swift incluye una función como parte del lenguaje llamada `print` que acepta un *parámetro* de tipo `String`, el cual es impreso en la pantalla cuando dicha función es llamada.

Una vez escrita esa instrucción de forma adecuada en un archivo con extensión `.swift` (la extensión que reconoce el compilador de Swift como código fuente), podemos compilarla y ejecutarla usando el comando `swift` desde nuestra linea de comandos. 