# Microservicios - Patrones comunes

## Definicion
Son soluciones recurrentes para problemas de comunicacion, evolucion y organizacion en sistemas de microservicios.

## Explicacion
- *BFF (Back-end for Front-end)*
    Backend especifico por tipo de cliente (web, mobile, etc.).
- *Entidad y agregado*
    Agrupa datos de negocio con limites consistentes.
- *Descubrimiento de servicios*
    Permite ubicar instancias dinamicas en runtime.
- *Adaptador*
    Traduce contratos incompatibles con terceros.
- *Strangler*
    Migra un monolito gradualmente hacia microservicios.

## Palabras clave
- BFF
- agregado
- service discovery
- adapter
- strangler

## Comparaciones tipicas
- vs [[49 - Microservicios - Antipatrones]]: patrones recomiendan que hacer; antipatrones advierten que evitar.
- vs arquitectura ad-hoc: patrones reducen improvisacion y riesgo.

## Preguntas de examen
- Explica brevemente BFF y Strangler.
- Para que sirve service discovery?

## Errores comunes
- Aplicar un patron sin entender el problema real.
- Querer usar todos los patrones en el mismo proyecto.
