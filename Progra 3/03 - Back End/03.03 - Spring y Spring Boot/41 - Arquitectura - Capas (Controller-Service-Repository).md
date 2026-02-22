# Arquitectura - Capas (Controller-Service-Repository)

## Definicion
Es un modelo de separacion de responsabilidades en 3 capas: controller (entrada HTTP), service (logica) y repository (datos).

## Explicacion
- *Que problema resuelve*
    Evita acoplar web, negocio y persistencia en una sola clase.
- *Como funciona por arriba*
    `Controller` recibe request -> delega a `Service` -> `Service` usa `Repository` -> retorna respuesta.
- *Que implica / que permite*
    Codigo mas mantenible, testeable y escalable.

## Palabras clave
- Controller
- Service
- Repository
- separacion de responsabilidades

## Comparaciones tipicas
- vs arquitectura en una sola capa: capas reducen caos y duplicacion.
- vs [[05 - Spring - DI e Inyeccion de Dependencias]]: DI conecta capas sin acoplamiento fuerte.

## Preguntas de examen
- Que responsabilidad tiene cada capa?
- Por que no deberia un controller acceder directo a la base?

## Errores comunes
- Poner reglas de negocio complejas en controller.
- Usar service como "pasamanos" sin valor.
