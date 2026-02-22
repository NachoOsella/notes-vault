# Transacciones - @Transactional

## Definicion
`@Transactional` indica que un metodo o clase se ejecuta dentro de una transaccion.

## Explicacion
- *Que problema resuelve*
    Garantiza consistencia: o se confirman todos los cambios, o se revierten (rollback).
- *Como funciona por arriba*
    Spring abre/cierra transaccion alrededor del metodo, normalmente via proxies/AOP.
- *Que implica / que permite*
    Operaciones de negocio atomicas y seguras ante errores.

## Palabras clave
- @Transactional
- commit
- rollback
- atomicidad

## Comparaciones tipicas
- vs [[13 - Spring - AOP (concepto)]]: `@Transactional` se implementa internamente con AOP/proxy.
- vs manejo manual: declarativo reduce codigo y errores.

## Preguntas de examen
- Que pasa cuando una excepcion rompe un metodo transaccional?
- Donde conviene ubicar `@Transactional` en arquitectura por capas?

## Errores comunes
- Marcar controllers en vez de services sin criterio.
- Suponer que cualquier excepcion siempre hace rollback (depende del tipo).
