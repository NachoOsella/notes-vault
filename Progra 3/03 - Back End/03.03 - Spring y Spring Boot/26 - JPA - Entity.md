# JPA - Entity

## Definicion
Una entidad (`@Entity`) es una clase Java que representa una tabla de base de datos.

## Explicacion
- *Que problema resuelve*
    Permite trabajar con objetos en lugar de manipular filas SQL manualmente.
- *Como funciona por arriba*
    Campos de la clase se mapean a columnas; `@Id` define la clave primaria.
- *Que implica / que permite*
    Persistencia orientada a objetos y uso de repositorios JPA.

## Palabras clave
- @Entity
- @Id
- @Table
- ORM

## Comparaciones tipicas
- vs [[21 - Spring MVC - DTO (que y por que)]]: entidad modela persistencia; DTO modela intercambio de datos.
- vs POJO comun: una entidad tiene ciclo de vida administrado por JPA.

## Preguntas de examen
- Que requisitos basicos tiene una entidad JPA?
- Para que sirve `@Id`?

## Errores comunes
- Exponer entidades directamente en API.
- Ignorar igualdad/hashCode en entidades con identidad.
