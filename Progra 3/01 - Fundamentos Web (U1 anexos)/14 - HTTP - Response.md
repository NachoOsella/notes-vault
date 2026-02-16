# HTTP - Response

## Definición
Mensaje enviado por el servidor al cliente como contestación a una petición previa, conteniendo el resultado de la operación y, opcionalmente, el recurso pedido.

## Explicación
- *Qué problema resuelve*
    Informa al cliente si su petición fue entendida, si fue exitosa o si ocurrió un error, entregando los datos de forma estructurada para su procesamiento.
- *Cómo funciona por arriba*
    Se compone de: 1. **Versión** del protocolo. 2. **Código de estado** (número). 3. **Mensaje de estado** (texto breve). 4. **Cabeceras**. 5. **Cuerpo** (el recurso solicitado, ej. el HTML).
- *Qué implica / qué permite*
    Permite al navegador saber qué hacer a continuación (renderizar la página, mostrar un error 404, o redirigir a otra URL).

## Palabras clave
- Status Code (Código de estado)
- MIME Type (en cabeceras)
- Content-Length
- Body (Cuerpo)
- Respuesta exitosa vs Error

## Comparaciones típicas
- vs [[13 - HTTP - Request]]: la response es la contestación del servidor a un request (misma interacción, distinto sentido).
- vs [[16 - HTTP - Códigos de estado]]: el status code es una parte de la response; la response además incluye headers y body.
- vs [[12 - HTTP - Flujo de mensajes]]: response es el mensaje de vuelta; el flujo describe el proceso completo (conexión, ida y vuelta).

## Preguntas de examen
- ¿Qué elementos forman una respuesta HTTP?
- ¿Qué indica el mensaje de estado?
- ¿Dónde viaja el código HTML de una página solicitada? (En el cuerpo de la respuesta).

## Errores comunes
- Pensar que si no hay cuerpo (body), la respuesta falló (algunas respuestas exitosas como 204 No Content no tienen cuerpo).
- Confundir el código 200 con el único código de éxito posible.

## Mini-ejemplo (mental)
- La entrega del mozo: "Aquí tiene (200 OK), es una hamburguesa (Cuerpo), provecho (Mensaje de estado)".
