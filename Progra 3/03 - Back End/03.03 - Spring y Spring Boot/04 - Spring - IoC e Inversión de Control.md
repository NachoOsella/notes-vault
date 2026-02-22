# Spring - IoC e Inversion de Control

## Definicion
IoC (Inversion de Control) es un principio donde la creacion y el armado de objetos (y sus dependencias) deja de estar en el codigo de la aplicacion y pasa a un contenedor (Spring).

## Explicacion
- *Que problema resuelve*
    Reduce acoplamiento: las clases no "deciden" que dependencias instanciar; solo declaran lo que necesitan.
- *Como funciona por arriba*
    Spring registra definiciones de beans (por anotaciones o configuracion) y, cuando se necesita un objeto, lo construye e inyecta sus dependencias.
- *Que implica / que permite*
    - Reemplazar implementaciones (por config) sin tocar la logica.
    - Testear mas facil (inyectando dobles/mocks).
    - Centralizar configuracion y ciclo de vida.

## Palabras clave
- Contenedor IoC
- Bean
- Wiring

## Comparaciones tipicas
- vs [[05 - Spring - DI e Inyeccion de Dependencias]]: IoC es el principio; DI es el mecanismo mas comun para implementarlo.

## Preguntas de examen
- Que es IoC y por que mejora el diseno?
- Como se implementa IoC en Spring?

## Errores comunes
- Confundir IoC con DI como sinonimos perfectos.
