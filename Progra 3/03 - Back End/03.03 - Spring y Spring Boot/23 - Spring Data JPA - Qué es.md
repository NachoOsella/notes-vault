# Spring Data JPA - Que es

## Definicion
Spring Data JPA es un modulo que simplifica el acceso a datos con JPA, reduciendo codigo boilerplate para CRUD y consultas.

## Explicacion
- *Que problema resuelve*
    Evita escribir DAOs repetitivos y gran parte de SQL/manual wiring.
- *Como funciona por arriba*
    Definis repositorios como interfaces y Spring genera implementaciones en runtime.
- *Que implica / que permite*
    Desarrollo mas rapido, consultas derivadas y paginacion con poco codigo.

## Palabras clave
- JPA
- repository
- CRUD
- JpaRepository

## Comparaciones tipicas
- vs JDBC puro: JPA abstrae mapeo objeto-relacional; JDBC trabaja mas cerca de SQL.
- vs [[24 - Spring Data JPA - Repository]]: Spring Data JPA es el modulo; Repository es el contrato principal.

## Preguntas de examen
- Que aporta Spring Data JPA sobre JPA "a mano"?
- Que se obtiene al extender `JpaRepository`?

## Errores comunes
- Pensar que elimina por completo la necesidad de entender SQL.
- Abusar de consultas derivadas complejas.
