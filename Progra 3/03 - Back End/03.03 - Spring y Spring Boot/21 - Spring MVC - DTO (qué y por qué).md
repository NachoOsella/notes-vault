# Spring MVC - DTO (que y por que)

## Definicion
Un DTO (Data Transfer Object) es un objeto usado para transportar datos entre capas o entre cliente y servidor.

## Explicacion
- *Que problema resuelve*
    Evita exponer entidades internas y separa contrato de API de modelo persistente.
- *Como funciona por arriba*
    Se crean DTOs de entrada/salida y se convierten desde/hacia entidades.
- *Que implica / que permite*
    Mayor seguridad, versionado mas simple y APIs mas estables.

## Palabras clave
- DTO
- contrato
- serializacion
- desacople

## Comparaciones tipicas
- vs entidad JPA: DTO representa intercambio; entidad representa persistencia.
- vs [[16 - Spring MVC - @RestController]]: controller expone endpoints; DTO define payload.

## Preguntas de examen
- Por que conviene usar DTOs en APIs REST?
- Que riesgo hay al devolver entidades directamente?

## Errores comunes
- Crear DTOs identicos a entidades sin necesidad.
- Mezclar logica de negocio dentro de DTOs.
