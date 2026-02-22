# Spring Data JPA - Query methods (derived queries)

## Definicion
Las derived queries son metodos en el Repository cuyo nombre define automaticamente la consulta.

## Explicacion
- *Que problema resuelve*
    Evita escribir JPQL/SQL para consultas comunes.
- *Como funciona por arriba*
    Spring interpreta nombres como `findByEmail`, `findByStatusAndDateAfter`, `existsByUsername`.
- *Que implica / que permite*
    Rapidez para casos simples y codigo expresivo.

## Palabras clave
- derived query
- naming convention
- findBy
- existsBy

## Comparaciones tipicas
- vs `@Query`: derived query sirve para casos comunes; `@Query` para consultas mas complejas.
- vs [[24 - Spring Data JPA - Repository]]: repository es la interfaz base; derived queries son metodos extra.

## Preguntas de examen
- Como se construye una derived query en Spring Data JPA?
- Cuando conviene pasar a `@Query`?

## Errores comunes
- Crear nombres de metodos demasiado largos y dificiles de mantener.
- Suponer que toda consulta compleja puede resolverse bien con naming.
