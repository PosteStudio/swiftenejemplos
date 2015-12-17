# Enumeraciones

Las enumeraciones en Swift comprenden una de sus características más poderosas. Nos permiten representar información de una manera mucho más clara. Se declaran usando la palabra reservada `enum`:

```swift
enum TipoDeUsuario {
    case Admin
    case Editor
    case Autor
    case Lector
}
```

El listado de código anterior define una enumeración llamada `TipoDeUsuario` que tiene como opciones `.Admin`, `.Editor`, `.Autor` y `.Lector`. En este contexto, nuestro programa ahora cuenta con un nuevo tipo de dato `TipoDeUsuario` y podemos usarlo al igual que usaríamos cualquier `Int` ó `String`.

Podemos crear una *instancia* de una enumeración de la siguiente manera:

```swift
let admin = TipoDeUsuario.Admin
let autor: TipoDeUsuario = .Autor
```

Ambas constantes son de tipo `TipoDeUsuario`.

Las enumeraciones también se pueden crear a partir de datos:
```swift
enum UtencilioDeCocina {
    case Tenedor = "tenedor"
    case Cuchillo = "cuchillo"
    case Cuchara = "cuchara"
}

let cuchara = UtencilioDeCocina(rawValue: "tenedor")
```

