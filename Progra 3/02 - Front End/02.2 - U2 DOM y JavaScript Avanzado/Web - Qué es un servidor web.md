# Web - Qué es un servidor web

## Definición

Un servidor web es un software (y por extensión, el hardware que lo ejecuta) que recibe peticiones HTTP de clientes (navegadores) y responde con recursos como páginas HTML, imágenes, o datos.

## Explicación

- *Qué problema resuelve*
    Centraliza y distribuye contenido web, permitiendo que múltiples usuarios accedan a los mismos recursos desde cualquier lugar con conexión a Internet.

- *Cómo funciona por arriba*
    1. El cliente (navegador) envía una petición HTTP a una URL
    2. El servidor recibe la petición y la procesa
    3. Busca o genera el recurso solicitado
    4. Devuelve una respuesta HTTP con el contenido y un código de estado

- *Qué implica / qué permite*
    - Hosting de sitios web (estáticos y dinámicos)
    - APIs REST para comunicación cliente-servidor
    - Servir archivos multimedia, scripts, hojas de estilo

## Ejemplos comunes

- Apache HTTP Server
- Nginx
- Microsoft IIS
- Node.js con Express
- Tomcat (para aplicaciones Java)

## Palabras clave

- HTTP
- Request/Response
- Puerto 80/443
- Hosting
- URL

## Comparaciones típicas

- vs [[Web - Sitios estáticos]]: el servidor puede servir contenido estático (archivos fijos) o dinámico (generado en tiempo real)
- vs [[Web - Sitios dinámicos]]: los sitios dinámicos requieren que el servidor ejecute código backend

## Preguntas de examen

- ¿Qué función cumple un servidor web?
- ¿Cuál es la diferencia entre un servidor web y un servidor de aplicaciones?
- ¿Qué protocolo usan los navegadores para comunicarse con servidores web?

## Errores comunes

- Confundir servidor web (software) con servidor físico (hardware)
- Pensar que todos los servidores web solo sirven páginas HTML estáticas
- Olvidar que HTTPS usa el puerto 443, no el 80

## Mini-ejemplo (mental)

Cuando escribís `www.google.com` en el navegador, tu petición viaja hasta un servidor web de Google que procesa tu solicitud y te devuelve la página de búsqueda.
