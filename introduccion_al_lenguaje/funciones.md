# Funciones

Es muy fácil declarar una función en Swift. Sólo hay que usar la palabra reservada `func`:

```swift
func decirHola() {
    print("hola!")
}
```

El ejemplo en el listado anterior declara una función llamada `decirHola`, que no acepta ningún parámetro, y al ser invocada imprimirá en pantalla el texto `hola!`.

Para invocar una función hay que escribir su nombre seguido de paréntesis:

```swift
decirHola() // #=> hola!
```

Muchas de las funciones que escribas en un futuro trabajarán con algún tipo de información. Esta información puede ser *pasada* a la función como parámetro de la misma:

```swift
func sumar(primerNumero: Int, segundoNumero: Int) -> Int {
    return primerNumero + segundoNumero
}

sumar(2, segundoNumero: 3)  // => 5
```

El listado anterior declara una función que acepta dos parámetros de tipo entero (`primerNumero` y `segundoNumero`) y debe de retornar un tipo de dato entero (`-> Int`).

Primero observemos la declaración de la función.  

Para Swift, dicha función se llama `sumar(_: segundoNumero:)` internamente. Observa el guión bajo en su nombre. Swift omite el nombre del primer parámetro para representar la función internamente. El nombre del segundo parámetro es usado tanto como para representar el nombre de la función internamente, como para el parámetro tal cual (para uso dentro de la función).

Esto puede hacer que el llamar una función resulte algo complicado. Como en el ejemplo anterior. ¿No sería mejor si se pudiera leer más naturalmente? La respuesta es sí:

```swift
func sumar(primerNumero: Int, con segundoNumero: Int) -> Int {
    return primerNumero + segundoNumero
}

sumar(2, con: 3) // => 5
```

Ahora, nuestra función sigue teniendo dos parámetros de tipo entero. El primer parámetro se omitirá en la llamada a la función, y el segundo parámetro será representado externamente usando `con`, pero internamente usando `segundoNumero`. Estamos haciendo uso del etiquetado de parámetros.

Hacer buen uso de esta capacidad de Swift resulta en código mucho más legible, como vimos anteriormente.
