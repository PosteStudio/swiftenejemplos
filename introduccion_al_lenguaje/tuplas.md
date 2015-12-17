# Tuplas

Las tuplas agrupan datos en un mismo objeto. A diferencia de los arrays, los *miembros* de una tupla **no deben de ser del mismo tipo.**

```swift
let usuario = ("Oscar Swanros", 22) // => (.0 "Oscar Swanros", .1 22)
```

En el ejemplo anterior, declaramos una tupla llamada `usuario` que contiene `"Oscar Swanros"` y `22` como sus miembros. En este caso, diríamos que la tupla sería de tipo `(String, Int)`.

```swift
let (nombre, edad) = usuario
print(nombre)   // #=> Oscar Swanros
print(edad)     // #=> 22
```

El listado anterior muestra un ejemplo de lo que llamamos *pattern matching*. En una misma linea, utilizamos la sintaxis `let (nombre, edad)` para recuperar los datos en la tupla `usuario`. Los contenidos de la tupla se *mapean* a las constantes definidas: el primer miembro de la tupla se asigna a la primera constante, el segundo a la segunda, etc.

Usando un guión bajo, podemos ignorar uno o más miembros de la tupla al momento de recuperarlos:

```swift
let (_, edad) = usuario
print(edad)     // #=> 22
```

Podemos también hacer referencia a miembros de la tupla sin necesidad de recuperarlos y asignarlos a constantes o variables externas:

```swift
print(usuario.0)    // #=> Oscar Swanros
print(usuario.1)    // #=> 22
```

Al igual que con las funciones y sus parámetros etiquetados, podemos poner etiquitas a los miembros de una tupla:

```swift
let usuario = (nombre: "Oscar Swanros", edad: 22) // => (.0 "Oscar Swanros", .1 22)
usuario.nombre      // => Oscar Swanros
usuario.edad        // => 22
```

Aunque una "tupla" no tiene un tipo único en Swift como `Int`, `Array` o `String`, podemos usar las tuplas como cualquier otro tipo de dato en nuestros programas. Incluso como tipo de retorno en funciones:

```swift
func generarUsuario(nombre nombre: String, edad: Int) -> (nombre: String, edad: Int) {
    return (nombre, edad)
}

let usuario = generarUsuario(nombre: "Oscar Swanros", edad: 22)
print(usuario.nombre)   // #=> Oscar Swanros
print(usuario.edad)     // #=> 22
```

Es importante diferenciar las tuplas de los arrays. 

* **Un array tiene elementos**, puede ser manipulado, escrito y leído.
* Una **tupla tiene miembros**, solamente pueden ser leídos y reemplazados de forma individual, siempre y cuando no se afecte el tipo de dato de la tupla.