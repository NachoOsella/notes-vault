# HTTP - Métodos de solicitud

## Definición
Conjunto de verbos o acciones estandarizadas que el protocolo HTTP define para indicar qué operación se desea realizar sobre un recurso.

## Explicación
- *Qué problema resuelve*
    Permite que el servidor entienda la intención semántica de la petición sin necesidad de analizar complejos mensajes, haciendo la comunicación predecible.
- *Cómo funciona por arriba*
    El cliente incluye un método en la línea de solicitud. Los más comunes son GET (leer, sin efectos secundarios), POST (crear), PUT (reemplazar), PATCH (modificar parcialmente) y DELETE (borrar).
- *Qué implica / qué permite*
    Permite construir APIs RESTful donde el mismo endpoint (ej. `/usuario/1`) se comporta diferente según el método utilizado.

## Otros metodos
- HEAD: igual a GET pero sin cuerpo de respuesta.
- OPTIONS: describe opciones de comunicacion del recurso.
- TRACE: prueba de bucle de mensajes hacia el recurso.
- CONNECT: crea un tunel TCP/IP, usado para HTTPS via proxy.

## Palabras clave
- Verbos HTTP
- Idempotencia
- Seguridad (Safe methods)
- Semántica
- Recursos

## Comparaciones típicas
- vs [[13 - HTTP - Request]]: el método es una parte del request; el request completo incluye URL, headers y body.
- vs [[16 - HTTP - Códigos de estado]]: el método indica la intención del cliente; el código de estado indica el resultado que devolvió el servidor.
- vs [[19 - API - Arquitectura RESTful (API REST)]]: REST usa los métodos HTTP como acciones sobre recursos (GET/POST/PUT/PATCH/DELETE).

## Preguntas de examen
- ¿Cuál es la diferencia entre POST y PUT?
- ¿Qué significa que un método sea "seguro" (safe)?
- ¿Para qué sirve el método PATCH?

## Errores comunes
- Usar GET para realizar acciones que modifican datos (como borrar un usuario).
- Confundir PUT con PATCH.

## Mini-ejemplo (mental)
- En una red social: `GET /post/1` para leerlo, `POST /post` para publicar uno nuevo, y `DELETE /post/1` para borrarlo.
