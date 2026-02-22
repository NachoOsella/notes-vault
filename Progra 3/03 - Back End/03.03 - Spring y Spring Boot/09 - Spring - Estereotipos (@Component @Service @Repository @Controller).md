# Spring - Estereotipos (@Component @Service @Repository @Controller)

## Definicion
Los estereotipos son anotaciones que marcan una clase como componente administrado por Spring y expresan su rol (capa) dentro de la aplicacion.

## Explicacion
- *Que problema resuelve*
    Permite que Spring detecte y registre beans automaticamente (component scanning) y ayuda a comunicar intencion.
- *Como funciona por arriba*
    Todas son variantes de `@Component` (directa o indirectamente) y por eso se detectan por scanning.
- *Que implica / que permite*
    Algunas agregan comportamiento:
    - `@Repository`: traduce excepciones de persistencia a la jerarquia de Spring.
    - `@Controller`: controlador MVC.
    - `@RestController`: `@Controller` + `@ResponseBody`.

## Palabras clave
- `@Component`
- `@Service`
- `@Repository`
- `@Controller`
- `@RestController`

## Comparaciones tipicas
- vs [[41 - Arquitectura - Capas (Controller-Service-Repository)]]: los estereotipos suelen mapearse 1:1 con esas capas.

## Preguntas de examen
- Diferencias entre `@Component`, `@Service` y `@Repository`.
- Diferencia entre `@Controller` y `@RestController`.
