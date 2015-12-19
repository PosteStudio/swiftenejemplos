# `if`/`else`

La forma más básica de poder decidir hacer algo o no en Swift es usando los bloques `if` y `else`.

```swift
if numeroDeInvitados > 10 { 
    print("No caben en mi casa!")
} else {
    print("Bienvenidos")
}
```

Las llaves **requeridas** en cada uno de estos bloques. Puedes escribir un `if` sin un `else`, pero no un `else` sin un `if`.

Inmediatamente después el `if`, escribe una expresión que retorne un valor `Bool`. Si el resultado de esta expresión es `true`, se ejecutará el bloque `if`. De lo contrario, se ejecutará el bloque `else`, en caso de existir.

```swift
if true { 
    print("Siempre se ejecutará")
}
```

En caso de que necesites hacer más de una validación, puedes incluir un bloque `else if`:

```swift
if esSabado {
    comprarDespensa()
} else if esDomingo {
    noLevantarseDeCama()
} else {
    trabajar()
}
```

En listado de código anterior nos dice qué deberíamos hacer dependiendo del día de la semana. En sábado, iremos a comprar la despensa, en domingo no nos levantaremos de la cama. Desafortunadamente, cualquier otro día de la semana debemos ir a trabajar.