# Spring - Configuracion (@Configuration @Bean)

## Definicion
`@Configuration` marca una clase como fuente de configuracion de Spring. `@Bean` marca un metodo cuyo retorno debe registrarse como bean en el contenedor.

## Explicacion
- *Que problema resuelve*
    Permite declarar beans de forma explicita (especialmente para librerias externas o cuando no queres usar scanning).
- *Como funciona por arriba*
    Spring procesa la clase `@Configuration` y ejecuta (segun necesidad) los metodos `@Bean` para crear instancias.
- *Que implica / que permite*
    - Definir dependencias con control total.
    - Centralizar configuraciones (clients HTTP, mappers, etc.).

## Palabras clave
- `@Configuration`
- `@Bean`

## Comparaciones tipicas
- vs [[08 - Spring - Component Scanning]]: `@Bean` es declarativo manual; scanning es automatico por anotaciones.

## Preguntas de examen
- Cuando conviene usar `@Bean` en vez de anotar la clase con `@Component`?
