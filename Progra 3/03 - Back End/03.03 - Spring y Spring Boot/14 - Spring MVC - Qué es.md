# Spring MVC - Que es

## Definicion
Spring MVC es el modulo de Spring para construir aplicaciones web y APIs HTTP siguiendo el patron Modelo-Vista-Controlador.

## Explicacion
- *Que problema resuelve*
    Organiza el manejo de requests HTTP para no mezclar rutas, logica de negocio y respuestas en el mismo lugar.
- *Como funciona por arriba*
    `DispatcherServlet` recibe la solicitud, elige un controlador y devuelve una vista o JSON segun corresponda.
- *Que implica / que permite*
    Permite crear endpoints REST limpios, validacion, manejo centralizado de errores y capas bien separadas.

## Palabras clave
- MVC
- DispatcherServlet
- Controller
- request-response

## Comparaciones tipicas
- vs [[16 - Spring MVC - @RestController]]: MVC es el modulo completo; `@RestController` es una anotacion para exponer APIs JSON.
- vs [[03 - Spring - Que es]]: Spring es el framework general; MVC es el bloque web.

## Preguntas de examen
- Que es Spring MVC y que rol cumple en una app web?
- Que componentes intervienen entre request y response?

## Errores comunes
- Pensar que Spring MVC solo sirve para vistas HTML (tambien sirve para APIs REST).
- Poner logica de negocio en el controller.
