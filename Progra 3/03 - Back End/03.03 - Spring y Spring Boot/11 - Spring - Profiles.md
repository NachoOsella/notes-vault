# Spring - Profiles

## Definicion
Un profile es una "variacion de configuracion" para un entorno (dev/test/prod). Permite habilitar beans y propiedades segun el ambiente.

## Explicacion
- *Que problema resuelve*
    Evita tener configuraciones mezcladas (por ejemplo DB local vs DB productiva) y reduce riesgo de desplegar mal.
- *Como funciona por arriba*
    - Activacion via `spring.profiles.active` (properties, env var, argumento CLI).
    - Beans condicionados con `@Profile("dev")`.
    - Properties por archivo (p. ej. `application-dev.yml`).
- *Que implica / que permite*
    Cambiar comportamiento sin recompilar.

## Palabras clave
- `spring.profiles.active`
- `@Profile`

## Comparaciones tipicas
- vs [[12 - Spring - Properties y Environment]]: profiles son un caso especifico de configuracion por ambiente.

## Preguntas de examen
- Como activas un profile en Spring Boot?
- Para que sirve `@Profile`?
