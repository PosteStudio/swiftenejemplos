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

### `enums` con tipos de dato de respaldo

Ambas constantes son de tipo `TipoDeUsuario`.

Las enumeraciones también se pueden crear a partir de datos. A continuación declaramos una enumeración que tiene `String` como tipo de dato de respaldo para cada caso:

```swift
enum UtencilioDeCocina: String {
    case Tenedor = "tenedor"
    case Cuchillo = "cuchillo"
    case Cuchara = "cuchara"
}

let tenedor = UtencilioDeCocina(rawValue: "tenedor") // => Tenedor
let cuchillo = UtencilioDeCocina(rawValue: "cuchara sopera") // => nil, "cuchara sopera" no está declarada como miembro de respaldo de la enumeración
```

Usando el constructor `rawValue:` podemos pasar un argumento del tipo de dato que respalda a la enumeración. Si el dato que pasamos al constructor es igual a uno de los declarados en la enumeración, se generará una instancia de la enumeración.

Del mismo modo, podemos obtener el valor de respaldo de una instancia de una enumeración usando la propiedad `rawValue`:

```swift
print(UtencilioDeCocina.Cuchillo.rawValue) // #=> "cuchillo"
```

### `enums` con tipos de datos asociados

Las enumeraciones, además poder tener tipos de dato de respalo, pueden, por así decirlo, transportar datos.

```swift
enum Resultado {
    case Error(Int, String)
    case Valor(AnyObject)
}
```

En el listado de código anterior definimos una enumeración con dos *cases* que pueden transportar datos: `.Error` que tiene asociados un `Int` y un `String`, y `.Valor`, que puede transportar cualquier objeto.

```swift
let error = Resultado.Error(404, "Página no encontrada")

switch error {
case .Error(let codigo, let descripcion):
    print("Código \(codigo): " + descripcion)
    
case .Valor(let valor):
    print(valor)
}

// #=> "Código 404: Página no encontrada"
```

El listado anterior muestra cómo podemos trabajar cuando tenemos enumeraciones con datos asociados. 