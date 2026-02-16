# HTTP - Flujo de mensajes

## Definición
Secuencia de pasos técnicos que ocurren desde que un cliente decide solicitar un recurso hasta que recibe y procesa la respuesta del servidor.

## Explicación
- *Qué problema resuelve*
    Establece un orden lógico y predecible para que dos sistemas que no se conocen puedan intercambiar datos de forma fiable.
- *Cómo funciona por arriba*
    1. El cliente abre una conexión (TCP). 2. Envía la **Petición** (Request) en texto plano o binario. 3. El servidor procesa y envía la **Respuesta** (Response). 4. Se cierra o reutiliza la conexión.
- *Qué implica / qué permite*
    Implica una comunicación de "parada y espera" (aunque se puede optimizar con multiplexación). Permite la depuración humana (en HTTP/1.1) ya que los mensajes son legibles.

## Palabras clave
- TCP Handshake
- Request / Response
- Texto plano vs Binario (HTTP/2)
- Reuso de conexión
- Multiplexación

## Comparaciones típicas
- vs [[13 - HTTP - Request]] / [[14 - HTTP - Response]]: el flujo es el proceso completo; request/response son las unidades de mensaje que viajan dentro.
- vs [[11 - HTTP - Características clave]]: flujo describe pasos; características describe propiedades del protocolo (stateless, extensible).

## Preguntas de examen
- ¿Cuáles son los 4 pasos principales del flujo de mensajes HTTP?
- ¿Qué cambió en el formato de los mensajes de HTTP/1.1 a HTTP/2?
- ¿Por qué es importante el paso de abrir una conexión TCP?

## Errores comunes
- Pensar que el mensaje viaja por arte de magia sin abrir primero una conexión de transporte (TCP).
- Creer que HTTP/2 cambió la semántica (solo cambió el formato de envío, la lógica sigue igual).

## Mini-ejemplo (mental)
- Es como una llamada telefónica: 1. Marcas y esperas que atiendan (TCP). 2. Dices qué quieres (Request). 3. Te contestan (Response). 4. Cortas o sigues hablando (Cierre/Reuso).
