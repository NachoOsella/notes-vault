# HTTP - Request

## Definición
Mensaje enviado por el cliente para iniciar una acción en el servidor o solicitar un recurso específico.

## Explicación
- *Qué problema resuelve*
    Proporciona una estructura estandarizada para que el cliente pueda especificar no solo qué quiere, sino bajo qué condiciones y con qué datos adicionales.
- *Cómo funciona por arriba*
    Se compone de: 1. **Método** (verbo como GET/POST). 2. **URL** (dirección del recurso). 3. **Versión** del protocolo. 4. **Cabeceras** (metadatos). 5. **Cuerpo** (opcional, para enviar datos).
- *Qué implica / qué permite*
    Permite enviar información compleja al servidor (ej. un formulario de registro en el cuerpo de un POST) y configurar la respuesta deseada (ej. pedirla en un idioma específico mediante cabeceras).

## Palabras clave
- Verbo HTTP
- Endpoint (URL)
- Headers (Cabeceras)
- Payload / Body
- Línea de solicitud

## Comparaciones típicas
- vs [[14 - HTTP - Response]]: request es la solicitud (qué querés y cómo); response es el resultado (qué pasó y qué te devuelven).
- vs [[15 - HTTP - Métodos de solicitud]]: el método (GET/POST/...) es solo una parte del request; el request incluye también URL, headers y body.
- vs [[12 - HTTP - Flujo de mensajes]]: el request es un mensaje; el flujo describe cuándo y cómo se envía dentro de la interacción.

## Preguntas de examen
- ¿Qué partes componen una petición HTTP?
- ¿En qué parte del request viajarían los datos de un login? (En el Body/Cuerpo).
- ¿Para qué sirven las cabeceras en un request?

## Errores comunes
- Olvidar que no todos los Requests tienen cuerpo (los GET usualmente no lo tienen).
- Confundir la URL del recurso con el dominio del servidor (la URL en el request suele ser relativa).

## Mini-ejemplo (mental)
- Una orden de pedido: "Traeme (Método) una hamburguesa (URL) rápido y sin cebolla (Cabeceras)".
