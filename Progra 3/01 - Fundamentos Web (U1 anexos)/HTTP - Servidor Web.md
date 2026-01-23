# HTTP - Servidor Web

## Definición
Entidad en la red que "sirve" los datos solicitados por el cliente, gestionando las peticiones y devolviendo los recursos correspondientes.

## Explicación
- *Qué problema resuelve*
    Provee un punto centralizado de acceso a recursos (archivos, datos, aplicaciones) para múltiples clientes de forma simultánea.
- *Cómo funciona por arriba*
    Es una entidad conceptual que puede estar formada por varios elementos físicos (load balancing) o programas (caché, bases de datos) que colaboran para generar la respuesta.
- *Qué implica / qué permite*
    Permite alojar sitios web y servicios. No tiene que ser un único equipo físico; varios servidores lógicos pueden convivir en un mismo computador compartiendo una IP.

## Palabras clave
- Host
- Load Balancing (Balanceo de carga)
- Recursos
- Request handling
- Entidad lógica

## Comparaciones típicas
- vs [[HTTP - User Agent (cliente)]]: el servidor espera requests y responde; el cliente (user agent) inicia la acción.
- vs [[Cliente-Servidor - Clientes y servidores]]: el servidor web es el rol "servidor" aplicado a HTTP.
- vs [[HTTP - Proxies]]: un proxy puede intermediar y hasta cachear respuestas; el servidor web es el origen del recurso.

## Preguntas de examen
- ¿Un servidor web debe ser siempre una única máquina física?
- ¿Qué funciones puede delegar un servidor principal a otros componentes?
- ¿Cómo comparten varios servidores la misma IP en HTTP/1.1?

## Errores comunes
- Confundir el hardware (la computadora) con el software servidor (el programa que responde).
- Pensar que el servidor "llama" a los usuarios (solo responde a sus llamadas).

## Mini-ejemplo (mental)
- El servidor de Wikipedia: recibe miles de peticiones por segundo, las reparte entre muchas computadoras internas y todas te devuelven el artículo que pediste como si fueran una sola.
