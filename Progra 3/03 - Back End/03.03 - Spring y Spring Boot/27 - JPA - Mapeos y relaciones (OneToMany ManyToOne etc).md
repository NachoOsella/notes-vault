# JPA - Mapeos y relaciones (OneToMany ManyToOne etc)

## Definicion
Los mapeos JPA describen como se relacionan entidades entre si en la base de datos.

## Explicacion
- *Que problema resuelve*
    Representa relaciones reales (1-1, 1-N, N-M) en modelo orientado a objetos.
- *Como funciona por arriba*
    `@OneToMany`, `@ManyToOne`, `@OneToOne`, `@ManyToMany` y anotaciones de join (`@JoinColumn`, `@JoinTable`).
- *Que implica / que permite*
    Navegar datos relacionados sin escribir joins en cada caso.

## Palabras clave
- @OneToMany
- @ManyToOne
- @JoinColumn
- @JoinTable

## Comparaciones tipicas
- vs [[26 - JPA - Entity]]: Entity define tabla/objeto; mapeos definen relaciones entre entidades.
- vs [[28 - JPA - FetchType y Cascade]]: mapeo define la relacion; fetch/cascade define comportamiento.

## Preguntas de examen
- Diferencia entre `@OneToMany` y `@ManyToOne`.
- Cuando se usa `@JoinTable`?

## Errores comunes
- Configurar relaciones bidireccionales sin controlar recursion en JSON.
- Ignorar propietario de la relacion (`mappedBy`).
