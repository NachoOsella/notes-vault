# Spring MVC - Mapping (@RequestMapping @GetMapping etc)

## Definicion
Los mappings vinculan URLs y metodos HTTP con metodos Java en un controller.

## Explicacion
- *Que problema resuelve*
    Define de forma declarativa que endpoint atiende cada accion.
- *Como funciona por arriba*
    `@RequestMapping` mapea de forma general; `@GetMapping`, `@PostMapping`, `@PutMapping` y `@DeleteMapping` son atajos por verbo HTTP.
- *Que implica / que permite*
    API mas legible, consistente y alineada a REST.

## Palabras clave
- endpoint
- routing
- @RequestMapping
- @GetMapping

## Comparaciones tipicas
- vs [[18 - Spring MVC - Binding (@PathVariable @RequestParam @RequestBody)]]: mapping define la ruta; binding define como leer datos de la request.
- vs [[15 - Spring MVC - DispatcherServlet]]: mappings declaran reglas; `DispatcherServlet` las aplica.

## Preguntas de examen
- Para que sirve `@RequestMapping`?
- Cuando conviene usar `@GetMapping` en vez de `@RequestMapping`?

## Errores comunes
- Usar el verbo HTTP incorrecto para la operacion.
- Crear rutas ambiguas entre controllers.
