# Integracion - Consumir APIs REST (RestTemplate vs WebClient)

## Definicion
Spring ofrece clientes HTTP para consumir APIs externas: `RestTemplate` (bloqueante) y `WebClient` (reactivo/no bloqueante).

## Explicacion
- *Que problema resuelve*
    Permite integrar servicios externos (pagos, auth, catalogos, etc.) desde tu backend.
- *Como funciona por arriba*
    Se construye request HTTP, se envia, se mapea respuesta y se maneja error/timeout/reintento.
- *Que implica / que permite*
    Integracion controlada con otros sistemas y arquitectura distribuida.

## Comparaciones tipicas
- `RestTemplate`: simple para casos tradicionales sin reactividad.
- `WebClient`: mejor para alta concurrencia y pipelines reactivos.
- vs [[46 - Microservicios - DevOps y CI-CD]]: consumir APIs es integracion funcional; DevOps resuelve operacion/entrega.

## Palabras clave
- RestTemplate
- WebClient
- timeout
- resiliencia

## Preguntas de examen
- Diferencia principal entre `RestTemplate` y `WebClient`.
- Que aspectos no funcionales hay que cuidar al consumir APIs externas?

## Errores comunes
- No definir timeouts.
- Asumir que servicios externos siempre responden rapido y bien.
