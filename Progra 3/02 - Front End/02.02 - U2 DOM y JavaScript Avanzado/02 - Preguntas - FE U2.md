# Preguntas - FE U2

## Arquitectura Web y HTTP

- ¿Qué es el modelo cliente-servidor y cuáles son sus componentes principales?
- ¿Qué función cumple un servidor web?
- ¿Qué significa que HTTP sea un protocolo stateless?
- ¿Cuál es la diferencia entre los métodos GET y POST en HTTP?
- ¿Qué indica un código de estado HTTP 404? ¿Y un 500?
- ¿Qué es una API REST y qué verbos HTTP utiliza?
- ¿Cuál es la diferencia entre un sitio web estático y uno dinámico?
- ¿Qué ventajas tiene un sitio estático sobre uno dinámico?
- ¿Qué tecnologías se usan comúnmente en el backend de sitios dinámicos?

## HTTP - Headers y Body

- ¿Para qué sirve el header `Content-Type`?
- ¿Qué header se usa para enviar tokens de autenticación?
- ¿Cuál es la diferencia entre los headers `Cookie` y `Set-Cookie`?
- ¿Qué métodos HTTP suelen llevar body en la petición?
- ¿Qué `Content-Type` usarías para enviar un objeto JSON?
- ¿Cómo se accede a los parámetros de la URL en JavaScript?
- ¿Por qué es importante usar `encodeURIComponent()` al construir URLs?

## DOM y Eventos

- ¿Qué es el DOM y para qué sirve?
- ¿Cómo se representa la estructura de un documento en el DOM?
- ¿Cuál es la diferencia entre `getElementById`, `querySelector` y `querySelectorAll`?
- ¿Qué ventajas tiene usar `querySelector` sobre `getElementsByClassName`?
- ¿Cuáles son las tres fases del event flow en JavaScript?
- ¿Qué es la fase de bubbling y cómo se puede detener?
- ¿Qué es la delegación de eventos y cuáles son sus ventajas?
- ¿Cuál es la diferencia entre `event.target` y `event.currentTarget`?
- ¿Qué es el objeto event y qué información contiene?
- ¿Para qué sirve `event.preventDefault()` y `event.stopPropagation()`?

## JavaScript Avanzado - Fetch y Promesas

- ¿Qué es Fetch API y qué ventajas tiene sobre XMLHttpRequest?
- ¿Qué devuelve la función `fetch()`?
- ¿Por qué es necesario llamar a `.json()` en la respuesta de fetch?
- ¿Cuáles son los tres estados de una promesa?
- ¿Qué diferencia hay entre `.then()` y `.catch()`?
- ¿Para qué sirve `Promise.all()` y cuándo es útil usarlo?
- ¿Qué ventajas tiene usar async/await sobre promesas con `.then()`?
- ¿Qué es CORS y por qué puede causar errores al usar fetch?

## Almacenamiento en el Cliente

- ¿Cuál es la diferencia principal entre localStorage y sessionStorage?
- ¿Cuál es la capacidad típica de almacenamiento de localStorage?
- ¿Por qué no es recomendable usar localStorage para almacenar información sensible?
- ¿Cuándo se borran los datos de sessionStorage?
- ¿Las cookies se envían automáticamente al servidor en cada petición?
- ¿Qué diferencia hay entre una cookie de sesión y una persistente?
- ¿Para qué sirven los atributos Secure, HttpOnly y SameSite en las cookies?
- ¿Cuál es el tamaño máximo aproximado de una cookie vs localStorage?

## Respuestas (opcional)

### ¿Qué es el modelo cliente-servidor y cuáles son sus componentes principales?
Respuesta: Es una arquitectura donde un cliente (navegador/app) pide recursos a un servidor, que procesa y responde. Componentes: cliente, servidor, red y protocolo (HTTP).

### ¿Qué función cumple un servidor web?
Respuesta: Recibe solicitudes HTTP, busca o genera el recurso solicitado y lo devuelve al cliente (HTML, CSS, JS, JSON, etc.).

### ¿Qué significa que HTTP sea un protocolo stateless?
Respuesta: Cada request es independiente y no guarda estado entre peticiones; para recordar sesiones se usan cookies, tokens o almacenamiento.

### ¿Cuál es la diferencia entre los métodos GET y POST en HTTP?
Respuesta: `GET` se usa para leer datos y suele enviar parámetros en la URL; `POST` se usa para crear/enviar datos en el body.

### ¿Qué indica un código de estado HTTP 404? ¿Y un 500?
Respuesta: `404` indica recurso no encontrado; `500` indica error interno del servidor al procesar la solicitud.

### ¿Qué es una API REST y qué verbos HTTP utiliza?
Respuesta: Es una API orientada a recursos, identificados por URLs, que usa HTTP de forma estándar. Verbos comunes: `GET`, `POST`, `PUT`, `PATCH`, `DELETE`.

### ¿Cuál es la diferencia entre un sitio web estático y uno dinámico?
Respuesta: El estático entrega archivos fijos iguales para todos; el dinámico genera contenido en tiempo real según usuario, datos o lógica del servidor.

### ¿Qué ventajas tiene un sitio estático sobre uno dinámico?
Respuesta: Es más rápido, barato y simple de desplegar, con menor superficie de ataque y mejor escalabilidad usando CDN.

### ¿Qué tecnologías se usan comúnmente en el backend de sitios dinámicos?
Respuesta: Frameworks/entornos como Node.js (Express/Nest), Java (Spring), Python (Django/FastAPI), PHP (Laravel) y bases SQL/NoSQL.

### ¿Para qué sirve el header `Content-Type`?
Respuesta: Indica el tipo de dato del body (MIME type), para que el receptor sepa cómo interpretarlo.

### ¿Qué header se usa para enviar tokens de autenticación?
Respuesta: Normalmente `Authorization`, por ejemplo `Authorization: Bearer <token>`.

### ¿Cuál es la diferencia entre los headers `Cookie` y `Set-Cookie`?
Respuesta: `Set-Cookie` lo envía el servidor para crear/actualizar cookies; `Cookie` lo envía el cliente devolviendo esas cookies al servidor.

### ¿Qué métodos HTTP suelen llevar body en la petición?
Respuesta: Principalmente `POST`, `PUT` y `PATCH`; en algunos casos `DELETE` también puede incluir body.

### ¿Qué `Content-Type` usarías para enviar un objeto JSON?
Respuesta: `application/json`.

### ¿Cómo se accede a los parámetros de la URL en JavaScript?
Respuesta: Con `URLSearchParams`, por ejemplo: `new URLSearchParams(window.location.search).get('id')`.

### ¿Por qué es importante usar `encodeURIComponent()` al construir URLs?
Respuesta: Porque escapa caracteres especiales (`?`, `&`, espacios, etc.) y evita URLs inválidas o parámetros mal interpretados.

### ¿Qué es el DOM y para qué sirve?
Respuesta: Es la representación en objetos del documento HTML; permite leer y modificar estructura, contenido, estilos y eventos desde JavaScript.

### ¿Cómo se representa la estructura de un documento en el DOM?
Respuesta: Como un árbol de nodos jerárquico, con `document` como raíz y elementos/texto/atributos como nodos hijos.

### ¿Cuál es la diferencia entre `getElementById`, `querySelector` y `querySelectorAll`?
Respuesta: `getElementById` busca por id y devuelve un elemento; `querySelector` devuelve el primer match CSS; `querySelectorAll` devuelve todos en un `NodeList`.

### ¿Qué ventajas tiene usar `querySelector` sobre `getElementsByClassName`?
Respuesta: Permite selectores CSS más expresivos (combinadores, atributos, pseudo-clases) y devuelve un único elemento fácil de manejar.

### ¿Cuáles son las tres fases del event flow en JavaScript?
Respuesta: Capturing (baja desde la raíz), Target (llega al objetivo) y Bubbling (sube desde el objetivo hacia arriba).

### ¿Qué es la fase de bubbling y cómo se puede detener?
Respuesta: Es la propagación del evento desde el elemento objetivo a sus ancestros; se detiene con `event.stopPropagation()`.

### ¿Qué es la delegación de eventos y cuáles son sus ventajas?
Respuesta: Es escuchar eventos en un contenedor padre y manejar hijos usando `event.target`; reduce listeners y funciona con elementos dinámicos.

### ¿Cuál es la diferencia entre `event.target` y `event.currentTarget`?
Respuesta: `target` es el elemento que disparó el evento; `currentTarget` es el elemento donde está registrado el listener que se está ejecutando.

### ¿Qué es el objeto event y qué información contiene?
Respuesta: Es el objeto que describe el evento ocurrido; incluye tipo, objetivo, posición del cursor, teclas, timestamp y métodos de control.

### ¿Para qué sirve `event.preventDefault()` y `event.stopPropagation()`?
Respuesta: `preventDefault()` cancela la acción por defecto (ej. enviar form); `stopPropagation()` evita que el evento siga propagándose.

### ¿Qué es Fetch API y qué ventajas tiene sobre XMLHttpRequest?
Respuesta: Es una API moderna basada en promesas para hacer requests HTTP; tiene sintaxis más limpia y mejor integración con `async/await`.

### ¿Qué devuelve la función `fetch()`?
Respuesta: Devuelve una `Promise` que resuelve a un objeto `Response`.

### ¿Por qué es necesario llamar a `.json()` en la respuesta de fetch?
Respuesta: Porque el body llega como stream/texto crudo y `.json()` lo parsea a objeto JavaScript utilizable.

### ¿Cuáles son los tres estados de una promesa?
Respuesta: `pending`, `fulfilled` y `rejected`.

### ¿Qué diferencia hay entre `.then()` y `.catch()`?
Respuesta: `.then()` maneja éxito (y puede encadenar transformaciones); `.catch()` maneja errores/rechazos de la cadena.

### ¿Para qué sirve `Promise.all()` y cuándo es útil usarlo?
Respuesta: Ejecuta varias promesas en paralelo y espera a que todas cumplan; útil cuando necesitás todos los resultados juntos.

### ¿Qué ventajas tiene usar async/await sobre promesas con `.then()`?
Respuesta: Hace el código asíncrono más legible y lineal, facilitando manejo de errores con `try/catch`.

### ¿Qué es CORS y por qué puede causar errores al usar fetch?
Respuesta: Es la política de origen cruzado del navegador; falla si el servidor no habilita explícitamente el origen/métodos/headers permitidos.

### ¿Cuál es la diferencia principal entre localStorage y sessionStorage?
Respuesta: `localStorage` persiste entre sesiones; `sessionStorage` dura solo mientras la pestaña esté abierta.

### ¿Cuál es la capacidad típica de almacenamiento de localStorage?
Respuesta: Aproximadamente 5 MB por origen (puede variar según navegador).

### ¿Por qué no es recomendable usar localStorage para almacenar información sensible?
Respuesta: Porque es accesible desde JavaScript y vulnerable a robo ante XSS; no tiene cifrado ni protección `HttpOnly`.

### ¿Cuándo se borran los datos de sessionStorage?
Respuesta: Se eliminan al cerrar la pestaña o ventana donde se creó la sesión.

### ¿Las cookies se envían automáticamente al servidor en cada petición?
Respuesta: Sí, para el dominio/ruta que coincidan y según políticas como `Secure`, `SameSite` y expiración.

### ¿Qué diferencia hay entre una cookie de sesión y una persistente?
Respuesta: La de sesión se borra al cerrar el navegador; la persistente se guarda hasta su fecha de expiración o eliminación manual.

### ¿Para qué sirven los atributos Secure, HttpOnly y SameSite en las cookies?
Respuesta: `Secure` solo por HTTPS, `HttpOnly` bloquea acceso desde JS y `SameSite` reduce envío cross-site para mitigar CSRF.

### ¿Cuál es el tamaño máximo aproximado de una cookie vs localStorage?
Respuesta: Cookie: ~4 KB por cookie; `localStorage`: ~5 MB por origen (aprox., depende del navegador).
