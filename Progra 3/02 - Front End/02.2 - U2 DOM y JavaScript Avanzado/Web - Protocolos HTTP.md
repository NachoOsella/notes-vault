# Web - Protocolos HTTP

## Definición

HTTP (HyperText Transfer Protocol) es el protocolo de comunicación que define cómo se estructuran y transmiten los mensajes entre clientes y servidores web.

## Explicación

- *Qué problema resuelve*
    Establece un lenguaje común para que navegadores y servidores puedan intercambiar información de manera estandarizada.

- *Cómo funciona por arriba*
    - Es un protocolo **request-response**: el cliente inicia enviando una petición, el servidor responde
    - Es **stateless**: cada petición es independiente (no guarda estado entre peticiones)
    - Usa **métodos** (GET, POST, PUT, DELETE, etc.) para indicar la acción deseada
    - Las respuestas incluyen **códigos de estado** (200 OK, 404 Not Found, 500 Error, etc.)

- *Qué implica / qué permite*
    - Navegación web tradicional
    - Comunicación con APIs REST
    - Transferencia de archivos, imágenes, datos JSON

## Métodos HTTP principales

| Método | Descripción | Idempotente |
|--------|-------------|-------------|
| GET | Obtener recurso | Sí |
| POST | Crear recurso | No |
| PUT | Reemplazar recurso completo | Sí |
| PATCH | Modificar parcialmente | No |
| DELETE | Eliminar recurso | Sí |

## Códigos de estado comunes

- **2xx**: Éxito (200 OK, 201 Created)
- **3xx**: Redirección (301 Moved, 304 Not Modified)
- **4xx**: Error del cliente (400 Bad Request, 401 Unauthorized, 404 Not Found)
- **5xx**: Error del servidor (500 Internal Server Error, 503 Service Unavailable)

## Palabras clave

- Request
- Response
- Stateless
- Métodos HTTP
- Códigos de estado
- REST

## Comparaciones típicas

- vs HTTPS: HTTPS es HTTP + cifrado TLS/SSL para seguridad
- vs [[HTTP - Headers]]: los headers son metadatos que acompañan las peticiones/respuestas HTTP
- vs [[HTTP - Body]]: el body es el contenido principal de la petición o respuesta

## Preguntas de examen

- ¿Qué significa que HTTP sea stateless?
- ¿Cuál es la diferencia entre GET y POST?
- ¿Qué indica un código 404? ¿Y un 500?
- ¿Qué método HTTP usarías para actualizar un recurso existente?

## Errores comunes

- Usar GET para enviar datos sensibles (quedan en la URL)
- Confundir PUT (reemplaza todo) con PATCH (modifica parcialmente)
- No manejar correctamente los códigos de error en el cliente

## Mini-ejemplo (mental)

Cuando hacés click en un link, el navegador envía un GET a esa URL. El servidor responde con código 200 y el HTML de la página en el body.
