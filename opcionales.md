# Opcionales

Si Swift tiene algo que llama la atención a primera vista, son los signos de interrogación y exclamación que se llegan a ver en el código de vez en vez.

```swift
var nivelDeEstudios: String?
```

A cualquier tipo de dato que sea seguido de un signo de interrogación se le conoce como un valor opcional. 

En el ejemplo anterior, tenemos un `String?` (se lee "String opcional"). Esto significa que la variable `nivelDeEstudios` ***puede*** contener un valor de tipo `String`, pero ***no es seguro que lo contenga.*** Es como si la variable dijera: "tal vez tenga un string dentro, no sé."

Los opcionales en Swift nos ayudan a manejar de mejor manera la información con la que trabaja nuestro programa: en un programa que recabe datos para una encuesta, el encuestado tal vez quiera o no decir su nivel de estudios, es por eso que esa variable está marcada como opcional.

```swift
var nivelDeEstudios: String? = "Secundaria"

func terminarEncuesta() {
    // No sabemos si nivelDeEstudios contiene un valor
    // Si sí contiene un valor, se lo asignamos a
    // la constante nivel.
    if let nivel = nivelDeEstudios { 
        // En este momento, nivel tiene el valor de nivelDeEstudios
        // pero nivel es de tipo String, no de tipo String?
        guardar(nivel) 
    }
}
```

En el listado de código anterior sucede lo siguiente:

1. Declaramos la variable `nivelDeEstudios` como un `String?`
2. El programa sigue su ejecución. 
3. Al momento en que la ejecución del programa llega a la función `terminarEncuesta`, debemos de verificar si esa variable tiene o no datos.
4. Usamos Extracción de Opcionales (u Optional Binding, en Inglés), para que, en caso de que la variable `nivelDeEstudios` **contenga** algún valor, éste sea asignado a la constante `nivel`. 
5. La variable nivel ahora es un valor de tipo `String` que podemos manipular.

Conocer bien los opcionales es importante, puesto que nos protegen de errores en nuestros programas donde podríamos creer que tenemos información para procesar, pero en realidad no es así.

