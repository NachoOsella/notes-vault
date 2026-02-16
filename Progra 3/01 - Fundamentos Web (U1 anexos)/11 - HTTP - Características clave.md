# HTTP - Características clave

## Definición
Rasgos fundamentales que definen cómo opera el protocolo de transferencia de hipertexto (HTTP) en la web.

## Explicación
- *Qué problema resuelve*
    Proporciona un estándar universal, simple y extensible para que cualquier navegador pueda comunicarse con cualquier servidor web en el mundo.
- *Cómo funciona por arriba*
    Es un protocolo de capa de aplicación, generalmente sobre TCP/IP. Es "sin estado" (stateless), funciona mediante solicitudes/respuestas y es extensible mediante cabeceras (headers).
- *Qué implica / qué permite*
    Implica que cada interacción es independiente. Permite la carga de diversos tipos de contenido (imágenes, scripts, video) gracias a los tipos MIME.

## Caracteristicas principales
- HTTP es sencillo: los mensajes son legibles y facilitan la depuracion.
- HTTP es extensible: las cabeceras permiten agregar funcionalidades nuevas.
- HTTP es stateless: no guarda estado entre peticiones, pero puede usar cookies para mantener contexto.
- HTTP y conexiones: se apoya en TCP por ser confiable; no requiere conexion continua entre solicitudes.

## Palabras clave
- Stateless (Sin estado)
- Basado en texto
- Request/Response
- Extensible
- Capa de Aplicación
- Cookies
- TCP/UDP
- HTTP/2

## Comparaciones típicas
- vs [[07 - HTTP - Sistemas basados en HTTP]]: acá se describen reglas/rasgos del protocolo; el otro describe actores y arquitectura del ecosistema.
- vs [[12 - HTTP - Flujo de mensajes]]: características explica qué es HTTP (stateless, headers, etc.); flujo describe el paso a paso de una interacción.
- vs [[13 - HTTP - Request]] / [[14 - HTTP - Response]]: request/response son mensajes; las características explican las reglas que hacen que esos mensajes funcionen.
- vs [[19 - API - Arquitectura RESTful (API REST)]]: HTTP es el protocolo; REST es un estilo que lo usa (recursos + verbos).

## Preguntas de examen
- ¿Qué significa que HTTP sea "stateless"?
- ¿Sobre qué protocolo de transporte suele correr HTTP?
- ¿Cómo maneja HTTP el estado si es stateless? (Cookies/Tokens).

## Errores comunes
- Confundir HTTP con HTML (uno es el protocolo, otro el formato de archivo).
- Pensar que HTTP mantiene una conexión abierta permanentemente para saber quién eres (el estado se maneja aparte).

## Mini-ejemplo (mental)
- HTTP es como enviar cartas: envías una, te responden, y si envías otra, el cartero no tiene por qué recordar que ya enviaste una antes.
