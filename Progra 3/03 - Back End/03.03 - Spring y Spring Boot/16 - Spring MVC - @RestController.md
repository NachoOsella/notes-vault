# Spring MVC - @RestController

## Definicion
`@RestController` marca una clase como controlador REST y hace que sus metodos devuelvan datos (JSON/XML) en el body.

## Explicacion
- *Que problema resuelve*
    Evita escribir `@ResponseBody` en cada metodo y simplifica la creacion de APIs.
- *Como funciona por arriba*
    Es equivalente a `@Controller + @ResponseBody`; serializa objetos Java a JSON automaticamente.
- *Que implica / que permite*
    Permite endpoints REST rapidos y consistentes para frontend u otros servicios.

## Palabras clave
- @RestController
- JSON
- serialization
- API REST

## Comparaciones tipicas
- vs `@Controller`: `@Controller` suele devolver vistas; `@RestController` devuelve datos.
- vs [[21 - Spring MVC - DTO (que y por que)]]: `@RestController` expone datos; DTO define el formato de esos datos.

## Preguntas de examen
- Que diferencia hay entre `@Controller` y `@RestController`?
- Que devuelve por defecto un metodo en `@RestController`?

## Errores comunes
- Exponer entidades JPA directamente en lugar de DTOs.
- Creer que `@RestController` reemplaza validacion o manejo de errores.
