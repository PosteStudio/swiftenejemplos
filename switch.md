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

`switch` es una de las características más poderosas de Swift, puesto que podemos trabajar con mucho más que números.