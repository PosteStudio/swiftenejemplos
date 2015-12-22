# Estructuras

Las estructuras (`struct`) son uno de los pilares principales de Swift como lenguaje.

```swift
struct Vaso {
    let contenido: String
    let capacidad: Float
}
```

El listado de código anterior define una estructura llamada `Vaso` que tiene dos *propiedades:* 

1. `contenido`, de tipo `String`
2. `capacidad`, de tipo `Float`

Las estructuras representan unidades de información. A diferencia de las clases (que se discutirán en el capítulo siguiente), lo que importa con las estructuras en Swift es su contenido. 

**Si una estructura (A) tiene los mismos valores en sus propiedades que otra estructura (B), se considera que A y B son iguales.** Por lo tanto, son intercambiables.

```swift
let vaso1 = Vaso(contenido: "Agua", capacidad: 350)
let vaso2 = Vaso(contenido: "Leche", capacidad: 350)
let vaso3 = Vaso(contenido: "Agua", capacidad: 350)

if vaso1 == vaso2 {
    print("El primer y el segundo vaso no son iguales")
} else if vaso1 == vaso3 {
    print("El primer y el tercer vaso son iguales")
}else {
    print("Nope")
}
```

Si ejecutáramos el código anterior veríamos impresa en pantalla la leyenda "El primer y el tercer vaso son iguales."

Aunque realmente el espacio de memoria que ocupan `vaso1` y `vaso2` son diferentes, se considera que son iguales puesto que su contenido es idéntico.

### Constructores

Toda estructura con propiedades definidas tiene un constructor por defecto que requiere que se le asigne un valor a cada una de las propiedades. Si alguna de las propiedades tiene un valor inicial, dicha propiedad se omite en el constructor por defecto:

```swift
struct Animal {
    let numeroDePatas = 4
    let familia: FamiliaAnimal
}

let animal = Animal(familia: .Felidae) // => Animal {numeroDePatas: 4, familia: Felidae }
```

### Modificando una estructura

Las estructuras con propiedades declaradas como valores inmutables `let` es por defecto inmutable por si misma.

```swift
struct Billete {
    let valor: Float
    let color: String
}

let miBillete = Billete(valor: 200, color: "#68C3A3")
miBillete.valor         // #=> 200
miBillete.valor = 500   // #=> Error!
```

Si intentas compilar lo anterior, encontrarás el error:

```bash
$ swift struct.swift
struct.swift:8:17: error: cannot assign to property: 'valor' is a 'let' constant
miBillete.valor = 500   // #=> Error!
~~~~~~~~~~~~~~~ ^
struct.swift:2:5: note: change 'let' to 'var' to make it mutable
    let valor: Float
    ^~~
    var
```

Cambiar la declaración de una propiedad de `let` a `var` en la definición de una estructura hará que esa propiedad pueda ser modificada en tiempo de ejecución.

Puesto que las estructuras en Swift son consideradas como entidades *de valor*, si deseas modificar una instancia de una estructura, tendrás que declarar que el valor es mutable al momento de crear la misma.

**Las propiedades declaradas como valores mutables (`var`) serán parte del constructor por defecto aún cuando tengan un valor inicial declarado.**

```swift
struct Billete {
    var valor: Float = 200
    var color: String
}

var miBillete = Billete(valor: 200, color: "#68C3A3")
miBillete.valor         // #=> 200
miBillete.valor = 500   // #=> 500
```

Observa cómo ahora `miBillete` es un valor mutable (`var`), lo que significa que podemos modificar su contenido.

Aunque el precio de tener una estructura mutable puede parecer mínimo, el punto general de las estructuras en Swift es que sean valores inmutables. Es ampliamente recomendado que se respete este principio.

Ejemplo práctico: un billete no puede cambiar su valor después de haber sido impreso. Puedes tener dos billetes iguales, del mismo valor, del mismo color, y puedes intercambiarlos por otros billetes del mismo valor. Al final de cuenta, te importa cuánto vale, no un billete en específico. 


### Métodos

Hasta ahora hemos visto solamente cómo una estructura puede representar un valor, pero no hemos hablado de cómo una estructura puede interactuar con nuestro programa.

```swift
struct Persona {
    let nombre: String
    let apellido: String
    
    func nombreCompleto() -> String {
        return nombre + " " + apellido
    }
}

let oscar = Persona(nombre: "Oscar", apellido: "Swanros")
oscar.nombreCompleto()  // #=> "Oscar Swanros"
```

En el ejemplo pasado, definimos una estructura llamada `Persona` con dos propiedades y un método. (Se llama "método" y no "función" puesto que se encuentra declarado como parte de la definición de un tipo de dato nuevo.)

Dentro de nuestro método podemos usar las propiedades de nuestra estructura. Por ahora, sólo estamos leyendo los valores `nombre` y `apellido` y los estamos concatenando. Pero ¿qué pasaría si quisiéramos un método que modifique los valores en nuestra estructura? Hay que especificarlo:

```swift
struct Persona {
    var nombre: String
    let apellido: String
    
    func nombreCompleto() -> String {
        return nombre + " " + apellido
    }
    
    mutating func actualizarNombre(nuevoNombre: String) {
        nombre = nuevoNombre
    }
}

var oscar = Persona(nombre: "Oscar", apellido: "Swanros")
oscar.nombreCompleto()              // #=> "Oscar Swanros"
oscar.actualizarNombre("Oscar E.")  // #=> "Oscar E. Swanros"
```

Llamar un método en una estructura basta con solo poner un punto después de la instancia y llamar al método con los parámetros requeridos.