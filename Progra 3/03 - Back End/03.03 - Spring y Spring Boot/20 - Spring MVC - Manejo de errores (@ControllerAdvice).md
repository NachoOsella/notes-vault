# Spring MVC - Manejo de errores (@ControllerAdvice)

## Definicion
`@ControllerAdvice` centraliza el manejo de excepciones de varios controllers en un solo lugar.

## Explicacion
- *Que problema resuelve*
    Evita repetir `try/catch` y formatos de error en cada endpoint.
- *Como funciona por arriba*
    Metodos con `@ExceptionHandler` capturan excepciones y devuelven respuesta HTTP uniforme.
- *Que implica / que permite*
    APIs mas mantenibles, mensajes consistentes y codigos HTTP correctos.

## Palabras clave
- @ControllerAdvice
- @ExceptionHandler
- error handling
- ResponseEntity

## Comparaciones tipicas
- vs [[19 - Spring MVC - Validacion (Bean Validation)]]: validacion detecta datos invalidos; advice define como responder errores.
- vs manejo local en controller: local es puntual; advice es global.

## Preguntas de examen
- Que ventaja tiene `@ControllerAdvice` frente a manejar errores en cada metodo?
- Para que sirve `@ExceptionHandler`?

## Errores comunes
- Devolver siempre `500` aunque el error sea de cliente.
- Exponer stack traces en produccion.
