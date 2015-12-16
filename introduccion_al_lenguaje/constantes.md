# Constantes

Una constante en Swift se declara usando la palabra reservada `let`. 

```swift
let numeroDeDiasEnLaSemana = 7
```

Las constantes son conocidos como "valores inmutables" dentro de Swift, no precisamente "constantes."

Al igual que las variables, no es necesario declarar explícitamente el tipo de dato de la constante si se le asignará un valor inicial en la misma declaración. Podemos declarar una constante sin valor inicial, de la siguiente forma:

```swift
let numeroDeDiasEnLaSemana: Int // #=> Declaramos la constante tipo Int sin asignar un valor inicial
numeroDeDiasEnLaSemana = 7 // #=> Asignamos el valor a la constante
```

La característica de las constantes en Swift, es que una vez que se les asigna un primer valor, éste ya no puede ser cambiado, solamente leído.

```swift
numeroDeDiasEnLaSemana = 9      // Error! numeroDeDiasEnLaSemana es inmutable y ya no se puede incializar de nuevo
```

El compilador será inteligente y te sugerirá que cambies la declaración de tu constante para que ahora sea una variable (mutable) y puedas asignar ese nuevo valor.

```bash
$ swift constantes.swift
constantes.swift:4:24: error: immutable value 'numeroDeDiasEnLaSemana' may only be initialized once
numeroDeDiasEnLaSemana = 9
                       ^
constantes.swift:1:1: note: change 'let' to 'var' to make it mutable
let numeroDeDiasEnLaSemana: Int
^~~
var
```