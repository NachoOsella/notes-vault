# Spring MVC - DispatcherServlet

## Definicion
`DispatcherServlet` es el Front Controller de Spring MVC: punto de entrada unico para las solicitudes HTTP.

## Explicacion
- *Que problema resuelve*
    Centraliza el enrutamiento para evitar logica duplicada de despacho en cada controlador.
- *Como funciona por arriba*
    Recibe request, consulta mappings, invoca el metodo del controller y delega la construccion de la respuesta.
- *Que implica / que permite*
    Facilita validacion, interceptores, manejo de excepciones y resolucion uniforme de respuestas.

## Palabras clave
- Front Controller
- routing
- HandlerMapping
- HandlerAdapter

## Comparaciones tipicas
- vs [[14 - Spring MVC - Que es]]: MVC es la arquitectura; `DispatcherServlet` es su coordinador central.
- vs [[17 - Spring MVC - Mapping (@RequestMapping @GetMapping etc)]]: mapping define rutas; `DispatcherServlet` las ejecuta.

## Preguntas de examen
- Por que `DispatcherServlet` se considera Front Controller?
- Que etapas basicas recorre una request en Spring MVC?

## Errores comunes
- Confundirlo con un controller de negocio.
- Ignorar que toda la cadena de MVC pasa por este servlet.
