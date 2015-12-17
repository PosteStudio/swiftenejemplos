# `guard`

Swift 2.0 introdujo la palabra reser vada `guard`. 

```swift
func esPositivo(numero: Int) -> Bool {
    guard numero > 0 else {
        return false
    }
    
    return true
}
```

Un `guard` nos permite realizar chequeos en el flujo de nuestro programa. Es como decir "para que el programa siga su ejecución, necesito que esta condición sea validada, de lo contrario, ejecuta el código en la cláusula `else`."

Es importante notar que el código dentro de la cláusula `else` **debe** de cambiar el flujo de ejecución del programa. Puedes usar cualquiera de estas palabras reservadas para cambiar el flujo del programa desde una cláusula `else` en un `guard`:

* `return`
* `break`
* `continue`
* `throw`

O en su defecto, llamar a una función marcada con el atributo `@noreturn`.

```swift
func imprimir(cadena: String?) {
    guard let cadena = cadena else {
        return
    }
    
    print(cadena)
}
```


En el ejemplo anterior, usamos `guard` para asegurarnos de que el opcional `cadena` tenga un valor. 

* Si esa condición se cumple, el valor de `cadena` se transferirá a la constante `cadena` (que a partir de ahí será de tipo `String`, no `String?`), y continúa la ejecución normal del programa.
* Si no se cumple la condición, se ejecutará el bloque de código en `else`, que en este caso simplemente retorna la función.


### Casos de Uso

Imagina una pieza de código donde se necesita evaluar diferentes condiciones para que el programa pueda continuar. Antes de Swift 2.0, ese código se vería algo así:

```swift
func generarUsuario(nombre: String?, apellido: String?, edad: Int?, dirección: String?) -> Usuario? {
}
```
