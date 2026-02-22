# Spring MVC - Validacion (Bean Validation)

## Definicion
Bean Validation permite declarar reglas sobre datos (`@NotNull`, `@Size`, etc.) y validarlas automaticamente con `@Valid`.

## Explicacion
- *Que problema resuelve*
    Evita repetir validaciones manuales en cada endpoint.
- *Como funciona por arriba*
    Se anotan DTOs con restricciones y en el controller se activa con `@Valid`.
- *Que implica / que permite*
    Respuestas consistentes ante datos invalidos y mejor calidad de API.

## Palabras clave
- @Valid
- @NotNull
- @Size
- constraint violations

## Comparaciones tipicas
- vs [[18 - Spring MVC - Binding (@PathVariable @RequestParam @RequestBody)]]: binding asigna valores; validacion comprueba reglas.
- vs [[20 - Spring MVC - Manejo de errores (@ControllerAdvice)]]: validacion detecta errores; `@ControllerAdvice` puede formatear la respuesta de error.

## Preguntas de examen
- Para que sirve `@Valid` en Spring MVC?
- Donde conviene poner reglas de validacion?

## Errores comunes
- Validar entidad persistente en vez de DTO de entrada.
- No devolver mensajes de error claros.
