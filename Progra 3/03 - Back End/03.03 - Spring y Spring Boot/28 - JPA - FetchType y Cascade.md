# JPA - FetchType y Cascade

## Definicion
`FetchType` define cuando cargar relaciones; `Cascade` define que operaciones propagar a entidades relacionadas.

## Explicacion
- *Que problema resuelve*
    Controla rendimiento y consistencia al trabajar con grafos de entidades.
- *Como funciona por arriba*
    `LAZY` carga bajo demanda, `EAGER` carga inmediato. `CascadeType` propaga `PERSIST`, `MERGE`, `REMOVE`, etc.
- *Que implica / que permite*
    Permite optimizar consultas y simplificar operaciones de guardado/borrado relacionadas.

## Palabras clave
- LAZY
- EAGER
- cascade
- N+1

## Comparaciones tipicas
- vs [[27 - JPA - Mapeos y relaciones (OneToMany ManyToOne etc)]]: relaciones modelan estructura; fetch/cascade modelan comportamiento.
- vs consulta manual: fetch plan bien definido evita sobrecarga innecesaria.

## Preguntas de examen
- Diferencias practicas entre `LAZY` y `EAGER`.
- Que riesgo tiene `CascadeType.ALL`?

## Errores comunes
- Usar `EAGER` por defecto en todo.
- Borrar en cascada sin entender impacto.
