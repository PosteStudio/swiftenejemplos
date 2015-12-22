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

Las estructuras representan unidades de información. A diferencia de las clases (que se discutirán en el capítulo siguiente), lo que importa con las estructuras en Swift es su contenido. Si una estructura (A) tiene los mismos valores en sus propiedades que otra estructura (B), se considera que A y B son iguales, por lo tanto, son intercambiables.

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

Toda estructura con propiedades definidas tiene un constructor por defecto que requiere que se le asigne un valor a cada una de las propiedades. Si alguna de las propiedades tiene valores por defecto, dicha propiedad se omite en el constructor por defecto:

```swift
struct Animal {
    let numeroDePatas: Int = 4
    let familia: FamiliaAnimal
}

let animal = Animal(familia: .Felidae) // => Animal {numeroDePatas: 4, familia: Felidae }
```

