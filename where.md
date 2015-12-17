# `where`

La palabra reservada `where` nos permite ser aún más precisos al momento de realizar verificaciones en el flujo de nuestro programa.

Un ejemplo claro de esto es:

```swift
let nombres = ["Oscar", "Marco", "Yuri"]

for nombre in nombres where nombre == "Oscar" {
    print(nombre) // #=> Oscar
}
```

En el ejemplo anterior: 

* Iteramos cada elemento del array `nombres`
* El elemento en turno es asignado a `nombre`
* Se ejecutará el código entre llaves solamente si la condición después de `where` se cumple

```swift
var ceros: [Int]? = []  

while let nums = ceros where nums.count < 5 {  
    ceros?.append(0) // [0,0,0,0,0]
}
```

Ahora combinamos un ciclo `while`, donde su condicional incluye un `where`. Otra aplicación bastante útil es en los condicionales `if` y en conjunto con `guard`s:

```swift
func darAcceso(nombreCompleto: String?) -> Bool {
    if let nombre = nombreCompleto where nombre == "Oscar Swanros" {
        return true
    }
    
    return false
}
darAcceso("Oscar Swanros") // #=> true

func verificarMayoriaDeEdad(nombreCompleto: String?, edad: Int) -> String {
    guard let nombre = nombreCompleto where edad >= 18 && nombre == "Oscar Swanros" else {
        return "Lo siento, no puedes entrar."
    }
    
    return "Bienvenido al club, \(nombre)"
}
verificarMayoriaDeEdad("Oscar Swanros", edad: 14) // #=> Lo siento, no puedes entrar
```

### Otros usos de `where`:

#### Switch:

```swift
let tupla = (14, "Gerardo Swanros")

switch tupla {
case let (edad, _) where edad >= 18:
    print("Eres mayor de edad!")
    
case let (_, nombre) where nombre == "Oscar Swanros":
    print("Eres \(nombre)!")
    
default:
    print("No se nada sobre ti")
}

// #=> No se nada sobre ti
```

#### Restricciones de tipo en funciones genéricas
```swift
enum Animal {
    case Perro
}
extension Animal: CustomStringConvertible {
    var description: String {
        switch self {
        case .Perro: return "El mejor amigo del hombre"
        }
    }
}

func obtenerDescripcionDeObjeto<T where T: CustomStringConvertible>(objeto: T) -> String {
    return objeto.description
}

obtenerDescripcionDeObjeto(Animal.Perro) // #=> El mejor amigo del hombre
```