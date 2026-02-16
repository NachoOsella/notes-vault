# HTTP - Body

## Definición

El body HTTP es la parte del mensaje que contiene los datos principales de la petición o respuesta, como el contenido de un formulario, un objeto JSON, o el HTML de una página.

## Explicación

- *Qué problema resuelve*
    Permite transmitir el contenido real de la comunicación: los datos que queremos enviar (en requests) o recibir (en responses).

- *Cómo funciona por arriba*
    - El body viene después de los headers, separado por una línea en blanco
    - El header `Content-Type` indica el formato del body (JSON, HTML, form-data, etc.)
    - El header `Content-Length` indica el tamaño del body en bytes
    - **GET y DELETE** generalmente no llevan body; **POST, PUT, PATCH** sí

- *Qué implica / qué permite*
    - Enviar datos de formularios al servidor
    - Transmitir objetos JSON en APIs REST
    - Recibir HTML, imágenes, archivos como respuesta
    - Upload de archivos (multipart/form-data)

## Formatos comunes del body

| Content-Type | Descripción | Uso típico |
|--------------|-------------|------------|
| `application/json` | Objeto JSON | APIs REST |
| `application/x-www-form-urlencoded` | Datos de formulario codificados | Forms HTML tradicionales |
| `multipart/form-data` | Datos binarios/archivos | Upload de archivos |
| `text/html` | Documento HTML | Respuestas de páginas web |
| `text/plain` | Texto plano | Logs, datos simples |

## Palabras clave

- Content-Type
- JSON
- Form data
- Payload
- Multipart

## Comparaciones típicas

- vs [[11 - HTTP - Headers]]: los headers son metadatos; el body es el contenido en sí
- vs [[04 - Web - Protocolos HTTP]]: el body es una parte opcional del mensaje HTTP

## Preguntas de examen

- ¿Qué métodos HTTP suelen llevar body?
- ¿Qué Content-Type usarías para enviar un objeto JSON?
- ¿Cuál es la diferencia entre `application/json` y `application/x-www-form-urlencoded`?
- ¿Cómo se envían archivos en el body de una petición HTTP?

## Errores comunes

- Olvidar parsear el body JSON en el servidor (`JSON.parse()` o middleware)
- No coincidir el Content-Type con el formato real del body
- Intentar enviar body en peticiones GET

## Mini-ejemplo (mental)

```js
// Enviando JSON en el body
fetch('/api/usuarios', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify({ nombre: 'Juan', edad: 25 })
})
```

El servidor recibe el body y lo parsea para obtener el objeto `{ nombre: 'Juan', edad: 25 }`.
