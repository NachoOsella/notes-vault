# HTTP - Códigos de estado

## Definición
Valores numéricos estandarizados que el servidor incluye en su respuesta para indicar el resultado de una petición HTTP.

## Explicación
- *Qué problema resuelve*
    Permite que las aplicaciones (navegadores, bots, scripts) entiendan rápidamente el destino de su petición sin tener que leer y analizar todo el contenido de la respuesta.
- *Cómo funciona por arriba*
    Se agrupan en 5 clases: **1xx** (Informativos), **2xx** (Éxito), **3xx** (Redirección), **4xx** (Error del Cliente), **5xx** (Error del Servidor).
- *Qué implica / qué permite*
    Permite la automatización y el manejo de errores. Por ejemplo, un navegador sabe que debe pedir otra URL si recibe un 301, o dejar de intentar si recibe un 404.

## Codigos frecuentes
- 100 Continue: respuesta provisional para continuar la solicitud.
- 101 Switching Protocols: acepta cambio de protocolo.
- 200 OK: solicitud exitosa.
- 201 Created: se creo un recurso nuevo.
- 202 Accepted: solicitud recibida pero aun sin procesar.
- 301 Moved Permanently: recurso movido a otra URI.
- 308 Permanent Redirect: redireccion permanente sin cambiar metodo.
- 400 Bad Request: sintaxis invalida en la solicitud.
- 401 Unauthorized: se requiere autenticacion.
- 403 Forbidden: el cliente no tiene permisos.
- 404 Not Found: recurso inexistente.
- 500 Internal Server Error: fallo interno del servidor.
- 503 Service Unavailable: servidor no disponible o sobrecargado.

## Palabras clave
- 200 OK
- 404 Not Found
- 500 Internal Server Error
- Familias de códigos
- Semántica de respuesta
- 301 Moved Permanently
- 401 Unauthorized
- 503 Service Unavailable

## Comparaciones típicas
- vs [[14 - HTTP - Response]]: el status code es el indicador de resultado dentro de la response completa.
- vs [[13 - HTTP - Request]]: el request no tiene códigos de estado; los códigos aparecen en la respuesta del servidor.
- vs [[15 - HTTP - Métodos de solicitud]]: método = qué querés hacer; status = qué pasó cuando se intentó.

## Preguntas de examen
- ¿Qué indican los códigos que empiezan con 4? ¿Y los que empiezan con 5?
- ¿Cuál es la diferencia entre un 200 y un 201?
- ¿Qué significa un código 301?

## Errores comunes
- Pensar que 404 es un error del servidor (es error del cliente por pedir algo que no existe).
- Creer que el mensaje de texto (ej. "Not Found") es lo que procesa la máquina (la máquina procesa el número 404).

## Mini-ejemplo (mental)
- Es como un semáforo: Verde (2xx), Amarillo/Desvío (3xx), Rojo porque vos te mandaste mal (4xx), Rojo porque se rompió el semáforo (5xx).
