# Spring Boot - ConfigurationProperties

## Definicion
`@ConfigurationProperties` enlaza bloques de configuracion externa a objetos tipados.

## Explicacion
- *Que problema resuelve*
    Evita usar muchos `@Value` sueltos y mejora validacion/mantenibilidad.
- *Como funciona por arriba*
    Se define prefijo, Boot mapea propiedades a campos y opcionalmente valida.
- *Que implica / que permite*
    Configuracion centralizada, tipada y facil de testear.

## Palabras clave
- @ConfigurationProperties
- binding
- prefijo
- configuracion tipada

## Comparaciones tipicas
- vs `@Value`: `@Value` sirve para casos simples; `@ConfigurationProperties` para grupos de propiedades.
- vs [[33 - Spring Boot - application.properties vs application.yml]]: esos archivos son fuente; esta anotacion es mecanismo de mapeo.

## Preguntas de examen
- Que ventaja tiene `@ConfigurationProperties` frente a `@Value`?
- Que rol cumple el prefijo?

## Errores comunes
- No habilitar escaneo/registro de la clase de propiedades.
- Dejar propiedades obligatorias sin validacion.
