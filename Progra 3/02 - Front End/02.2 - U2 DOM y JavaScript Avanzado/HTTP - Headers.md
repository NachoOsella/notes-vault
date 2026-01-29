# HTTP - Headers

## Definición

Los headers HTTP son metadatos que acompañan las peticiones y respuestas HTTP, proporcionando información adicional sobre la comunicación (tipo de contenido, autenticación, caché, etc.).

## Explicación

- *Qué problema resuelve*
    Permiten transmitir información contextual que no forma parte del contenido principal, como credenciales, formato de datos esperado, instrucciones de caché, etc.

- *Cómo funciona por arriba*
    - Se envían como pares `clave: valor` al inicio de cada mensaje HTTP
    - Existen headers de **request** (los envía el cliente) y de **response** (los envía el servidor)
    - Son case-insensitive (no distinguen mayúsculas/minúsculas)

- *Qué implica / qué permite*
    - Negociación de contenido (Accept, Content-Type)
    - Autenticación (Authorization)
    - Control de caché (Cache-Control, ETag)
    - Manejo de cookies (Cookie, Set-Cookie)
    - Información del cliente (User-Agent)

## Headers comunes

### Request headers
| Header | Descripción |
|--------|-------------|
| `Accept` | Tipos de contenido que acepta el cliente |
| `Authorization` | Credenciales de autenticación |
| `Content-Type` | Tipo de contenido del body enviado |
| `Cookie` | Cookies almacenadas para ese dominio |
| `User-Agent` | Información del navegador/cliente |

### Response headers
| Header | Descripción |
|--------|-------------|
| `Content-Type` | Tipo MIME del contenido devuelto |
| `Set-Cookie` | Instrucción para guardar una cookie |
| `Cache-Control` | Directivas de caché |
| `Location` | URL de redirección (con códigos 3xx) |
| `Access-Control-Allow-Origin` | CORS - orígenes permitidos |

## Palabras clave

- Metadatos
- Content-Type
- Authorization
- CORS
- Cache

## Comparaciones típicas

- vs [[HTTP - Body]]: los headers son metadatos; el body es el contenido principal
- vs [[Web - Protocolos HTTP]]: los headers son una parte del protocolo HTTP

## Preguntas de examen

- ¿Para qué sirve el header `Content-Type`?
- ¿Qué header se usa para enviar tokens de autenticación?
- ¿Cuál es la diferencia entre `Cookie` y `Set-Cookie`?
- ¿Qué header está relacionado con CORS?

## Errores comunes

- Olvidar establecer `Content-Type: application/json` al enviar JSON
- No entender que CORS se controla mediante headers de response
- Confundir headers de request con headers de response

## Mini-ejemplo (mental)

Cuando hacés un fetch con un token JWT, lo enviás así:
```js
fetch(url, {
  headers: {
    'Authorization': 'Bearer mi-token',
    'Content-Type': 'application/json'
  }
})
```
