# Testing Spring - MockMvc

## Definicion
`MockMvc` permite probar controllers HTTP sin levantar un servidor real.

## Explicacion
- *Que problema resuelve*
    Verifica rutas, status y payloads de API de forma rapida.
- *Como funciona por arriba*
    Simula requests (`get`, `post`, etc.) y valida respuestas (`status`, `jsonPath`, headers).
- *Que implica / que permite*
    Tests web confiables con bajo costo.

## Palabras clave
- MockMvc
- test web
- status code
- jsonPath

## Comparaciones tipicas
- vs cliente HTTP real: MockMvc es mas rapido al evitar red/servidor real.
- vs [[38 - Testing Spring - @SpringBootTest]]: MockMvc puede usarse en contexto parcial o completo.

## Preguntas de examen
- Que valida tipicamente un test con MockMvc?
- Que ventaja tiene frente a test manual de endpoints?

## Errores comunes
- Probar solo `200 OK` sin validar contenido.
- Acoplar tests a detalles internos del controller.
