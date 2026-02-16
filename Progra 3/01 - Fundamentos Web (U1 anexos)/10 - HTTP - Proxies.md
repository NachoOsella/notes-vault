# HTTP - Proxies

## Definición
Dispositivos o programas intermediarios que operan en la capa de aplicación para gestionar, filtrar o mejorar los mensajes HTTP entre el cliente y el servidor.

## Explicación
- *Qué problema resuelve*
    Añaden funcionalidades de red sin que el cliente o el servidor tengan que cambiar su código, mejorando la seguridad, el rendimiento y el control del tráfico.
- *Cómo funciona por arriba*
    Se sitúan en medio del canal de comunicación. Pueden ser transparentes o modificar las peticiones. Realizan tareas como caché, filtrado de contenido, balanceo de carga o registro de eventos.
- *Qué implica / qué permite*
    Permite ahorrar ancho de banda (caché), proteger a los usuarios (control parental/antivirus) y distribuir el trabajo entre muchos servidores (balanceo de carga).

## Palabras clave
- Gateway
- Caching
- Balanceo de carga
- Anonimato / Filtrado
- Intermediario

## Comparaciones típicas
- vs [[07 - HTTP - Sistemas basados en HTTP]]: el proxy es un componente opcional del sistema; cliente y servidor son obligatorios.
- vs [[09 - HTTP - Servidor Web]]: el proxy intermedia/optimiza; el servidor es el origen que genera la respuesta.
- vs [[08 - HTTP - User Agent (cliente)]]: el user agent pide recursos; el proxy puede filtrar/cachear esas peticiones sin cambiar al cliente.

## Preguntas de examen
- Menciona 3 funciones que puede realizar un proxy.
- ¿Qué diferencia a un proxy de un router en términos de capas? (El proxy opera en la capa de aplicación).
- ¿Qué es el caching en un proxy?

## Errores comunes
- Pensar que un proxy solo sirve para "navegar de incógnito".
- Confundirlo con un Firewall básico de red (el proxy entiende el contenido del mensaje HTTP).

## Mini-ejemplo (mental)
- En una escuela, un proxy puede bloquear sitios de juegos (filtrado) y guardar las páginas de estudio más visitadas para que carguen más rápido para todos (caché).
