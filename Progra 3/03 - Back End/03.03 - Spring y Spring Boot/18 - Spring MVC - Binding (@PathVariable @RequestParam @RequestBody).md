# Spring MVC - Binding (@PathVariable @RequestParam @RequestBody)

## Definicion
El binding convierte datos de la request HTTP en parametros Java del metodo del controller.

## Explicacion
- *Que problema resuelve*
    Evita parsear manualmente URL, query params o body.
- *Como funciona por arriba*
    `@PathVariable` toma valores de la ruta, `@RequestParam` de query string, `@RequestBody` del cuerpo (normalmente JSON).
- *Que implica / que permite*
    Endpoints mas claros y menos codigo repetitivo.

## Ejemplos comunes
- `GET /users/10` -> `@PathVariable Long id`
- `GET /users?page=2` -> `@RequestParam int page`
- `POST /users` con JSON -> `@RequestBody UserCreateDTO dto`

## Palabras clave
- binding
- @PathVariable
- @RequestParam
- @RequestBody

## Comparaciones tipicas
- vs [[17 - Spring MVC - Mapping (@RequestMapping @GetMapping etc)]]: mapping decide adonde va la request; binding decide que datos extrae.
- vs [[19 - Spring MVC - Validacion (Bean Validation)]]: binding carga datos; validacion verifica que sean correctos.

## Preguntas de examen
- Diferencia entre `@PathVariable`, `@RequestParam` y `@RequestBody`.
- En que casos usar cada uno?

## Errores comunes
- Usar `@RequestBody` en GET sin necesidad.
- No validar datos luego del binding.
