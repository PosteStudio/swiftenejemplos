# Cómo usar este libro

Los contenidos de este libro están disponibles completamente gratis en su [repositorio de GitHub](http://github.com/PosteStudio/swiftenejemplos), desde donde puedes descargar todos los contenidos en formato `.zip`.

## Versión de Swift
Todos los ejemplos de este libro están probados con la última versión de Swift disponible a través de los canales finales de Apple. Actualmente: **Swift 2.1.**

## Errores en los artículos y contribuciones
Todos los artículos en este libro están escritos usando la sintaxis Markdown. Si encuentras algún error, o quieres aportar un artículo en específico, siempre puedes [abrir un Pull Request al repositorio](https://github.com/PosteStudio/swiftenejemplos/pulls). Tu contribución será (posiblemente) editada, para posteriormente ser evaluada su inclusión en el libro.


## Comunidad

Como se dijo anteriormente, Swift en Ejemplos es un trabajo de comunidad.

* [GitHub](http://github.com/postestudio/swiftenejemplos)
* [Twitter](http://twitter.com/SwiftEnEjemplo)
* [Equipo en Slack](http://swiftes.slack.com)

## Listados de código
A lo largo del libro encontrarás varios listados de código donde se muestran ejemplos específicos de Swift. Hay varias consideraciones al respecto:


* Cuando el código deba de ser escrito directamente en la terminal (línea de comandos), el primer caracter en la línea será `$`. Ejemplo:
```bash 
$ swift helloworld.swift
```
* Cuando el código deba de ser escrito en el REPL de Swift, la líneas del listado comenzarán con un número de línea. Ejemplo:
```bash
1> let myVar = "Hello world!"
2> print(myVar)
```
* Cuando el código deba de ser escrito en un archivo específico, se especificará el nombre del mismo como un comentario en la primera línea del listado. Ejemplo:
```swift
// helloworld.swift
print("Hello world!")
```
* Si se espera que la línea de código en el listado tenga algún resultado en pantalla, se denotará el mismo usando la notación `// #=>`. Ejemplo:
```swift
print((0...2).count) // #=> 3
```
* Los comentarios generales en las líneas de código específicas serán expresados a través de la sintaxis de comentario de Swift `//`. Ejemplo:
```swift
let array: [String] // Declaramos una constante de tipo Array<String>
```