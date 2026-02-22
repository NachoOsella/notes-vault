# Testing Spring - @SpringBootTest

## Definicion
`@SpringBootTest` carga el contexto completo de Spring Boot para pruebas de integracion.

## Explicacion
- *Que problema resuelve*
    Permite probar interaccion real entre componentes, configuraciones y beans.
- *Como funciona por arriba*
    Inicia el ApplicationContext casi como en runtime real; opcionalmente levanta servidor para tests web.
- *Que implica / que permite*
    Alta fidelidad de prueba, pero mayor costo/tiempo.

## Palabras clave
- @SpringBootTest
- integration test
- ApplicationContext
- contexto completo

## Comparaciones tipicas
- vs [[40 - Testing Spring - Slice tests (@WebMvcTest @DataJpaTest)]]: `@SpringBootTest` prueba todo; slice test aisla una capa.
- vs unit test puro: unit test es mas rapido y aislado.

## Preguntas de examen
- Cuando conviene usar `@SpringBootTest`?
- Que desventaja principal tiene frente a tests unitarios?

## Errores comunes
- Usarlo para todo y volver lenta la suite.
- No aislar dependencias externas en pruebas.
