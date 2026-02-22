# Testing Spring - Slice tests (@WebMvcTest @DataJpaTest)

## Definicion
Los slice tests cargan solo una porcion del contexto Spring para probar una capa concreta.

## Explicacion
- *Que problema resuelve*
    Reduce tiempo de ejecucion al evitar levantar toda la app.
- *Como funciona por arriba*
    `@WebMvcTest` aísla capa web; `@DataJpaTest` aísla persistencia/repositories.
- *Que implica / que permite*
    Feedback rapido y pruebas mas enfocadas por capa.

## Palabras clave
- slice test
- @WebMvcTest
- @DataJpaTest
- aislamiento

## Comparaciones tipicas
- vs [[38 - Testing Spring - @SpringBootTest]]: slice = rapido y parcial; boot test = completo y mas lento.
- vs unit test puro: slice incluye infraestructura Spring de una capa.

## Preguntas de examen
- Que diferencia principal hay entre `@WebMvcTest` y `@DataJpaTest`?
- Cuando elegir slice tests?

## Errores comunes
- Intentar probar toda la app con slice tests.
- No mockear colaboradores externos en `@WebMvcTest`.
