# Spring Data JPA - Repository

## Definicion
Un Repository en Spring Data JPA es una interfaz que encapsula operaciones de persistencia sobre una entidad.

## Explicacion
- *Que problema resuelve*
    Centraliza acceso a datos sin exponer detalles de base a las capas superiores.
- *Como funciona por arriba*
    Se extiende `JpaRepository<Entidad, ID>` y se heredan metodos como `save`, `findById`, `findAll`, `deleteById`.
- *Que implica / que permite*
    Codigo mas limpio y facil de testear.

## Palabras clave
- repository pattern
- JpaRepository
- persistencia
- abstraccion

## Comparaciones tipicas
- vs DAO clasico: Repository reduce implementacion manual repetitiva.
- vs [[25 - Spring Data JPA - Query methods (derived queries)]]: repository define el contrato; query methods agregan busquedas por nombre.

## Preguntas de examen
- Que ventajas tiene extender `JpaRepository`?
- Donde deberia usarse un repository dentro de la arquitectura por capas?

## Errores comunes
- Llamar repository directamente desde controller.
- Poner logica de negocio compleja en repository.
