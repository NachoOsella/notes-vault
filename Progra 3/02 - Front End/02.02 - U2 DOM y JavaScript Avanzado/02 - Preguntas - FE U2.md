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

### ¿Qué es el modelo cliente-servidor?
Es una arquitectura donde el cliente (navegador/app) envía solicitudes HTTP a un servidor, que procesa la petición y devuelve una respuesta. Ver: [[16 - Web - Modelo Cliente-Servidor]]

### ¿Qué es el DOM?
El Document Object Model es una interfaz de programación que representa la página web como un árbol de objetos, permitiendo manipular el contenido, estructura y estilo mediante JavaScript. Ver: [[07 - DOM - Manipulación del DOM]]

### ¿Cuáles son las tres fases del event flow?
1. **Capturing**: el evento desciende desde la raíz al elemento objetivo
2. **Target**: el evento llega al elemento donde ocurrió
3. **Bubbling**: el evento asciende desde el elemento objetivo hacia la raíz
Ver: [[08 - Eventos - Event flow (fases y flujo)]]

### ¿Cuál es la diferencia entre localStorage y sessionStorage?
- **localStorage**: Persistente, sobrevive al cerrar el navegador, compartido entre pestañas del mismo dominio
- **sessionStorage**: Temporal, se borra al cerrar la pestaña, aislado por pestaña
Ver: [[13 - Storage - localStorage]] y [[14 - Storage - sessionStorage]]

### ¿Qué es una promesa?
Un objeto que representa el resultado eventual (éxito o fracaso) de una operación asíncrona, permitiendo encadenar operaciones y manejar errores de forma más limpia que los callbacks. Ver: [[19 - JS - Promesas (Promises)]]
