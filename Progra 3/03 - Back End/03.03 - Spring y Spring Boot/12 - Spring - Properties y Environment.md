# Spring - Properties y Environment

## Definicion
En Spring (y especialmente Spring Boot), la configuracion se externaliza en properties/yaml, variables de entorno y argumentos de linea de comandos. `Environment` expone esas propiedades al runtime.

## Explicacion
- *Que problema resuelve*
    Permite cambiar configuracion (puertos, DB, URLs, credenciales) sin modificar codigo.
- *Como funciona por arriba*
    Spring carga propiedades desde multiples fuentes con un orden de precedencia (CLI > env vars > archivos, etc.).
- *Que implica / que permite*
    - Configurar distinto por ambiente.
    - Inyectar valores con `@Value` o bindear grupos con `@ConfigurationProperties`.

## Fuentes tipicas
- `application.properties` / `application.yml`
- `application-<profile>.properties` / `.yml`
- Variables de entorno
- Argumentos: `--server.port=8081`

## Palabras clave
- `Environment`
- `@Value`
- `@ConfigurationProperties`

## Comparaciones tipicas
- vs [[33 - Spring Boot - application.properties vs application.yml]]: formato; ambos terminan siendo propiedades.
- vs [[34 - Spring Boot - ConfigurationProperties]]: `@Value` inyecta valores puntuales; `@ConfigurationProperties` agrupa y valida mejor.

## Preguntas de examen
- Que fuentes de configuracion reconoce Spring Boot?
- Por que se recomienda externalizar configuracion?
