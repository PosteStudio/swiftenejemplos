# `switch`

Una directiva `switch` nos puede ahorrar mucho tiempo y código cuando escribamos Swift.

```swift
switch numero {
    case 1:
        print("Es uno!")
    
    case 2:
        print("Es dos!")
        
    case 3: 
        print("Es tres!")
        
    default:
        print("Es cualquier otro número!")
}
```

Dentro de cada uno de los `case` que se deben incluir dentro del `switch` podemos definir el comportamiento que nuestro código debe tomar.

La sintáxis es muy parecida a la que encontramos en otros lenguajes de programación. La peculiaridad de `switch`en Swift es que no necesitamos romper el ciclo de ejecución al final de cada rama del mismo (es decir, no es necesario incluir la palabra `break`).

`switch` es una de las características más poderosas de Swift, puesto que podemos trabajar con mucho más que números. Por ejemplo...

Enumeraciones:

```swift
switch TipoDeUsuario {
    case .Usuario:
        irAlPerfilDeUsuario() 
        
    case .Admin:
        irAlPanelDeControl()
        
    case .Editor:
        irAlPanelDeArticulosPendientes()
}
```

Cadenas:

```swift
switch Nombre {
    case "Oscar":
        mostrarContenidoParaOscar()
        
    case "Nancy":
        mostrarContenidoParaNancy()
    
    default:
        mostrarContenidoGeneral()
```

... y muchos más, que veremos en capítulos siguientes.

Algo que debes de tomar en cuenta cuando trabajes con `switch` es que debe ser exhaustivo. Lo que significa, que en los `case`s debes cubrir todas las posibles opciones de ejecución.

En el ejemplo anterior, donde trabajamos con enumeraciones, asumimos que `TipoDeUsuario` tiene sólo 3 posibles miembros: `.Usuario`, `.Admin`, y `.Editor`. 

Cuando trabajemos con `Int`s o con `String`s, como en el ejemplo 1 y 3, debido a que son innumerables las posibles combinaciones que podemos analizar (los números son infinitos y las posibles cadenas, bueno... también), debemos incluid un `case default` — si nungún otro case satisface nuestro `switch`, se ejecutará el código en `default`.