# Web - Modelo Cliente-Servidor

## Definición

El modelo cliente-servidor es una arquitectura de red donde los clientes (dispositivos que realizan solicitudes) interactúan con servidores (sistemas que proporcionan recursos o servicios). El cliente envía solicitudes HTTP y el servidor procesa la petición y devuelve una respuesta.

## Explicación

- *Qué problema resuelve*
    Permite distribuir la carga de procesamiento y separar claramente las responsabilidades: el cliente se encarga de la presentación y la interacción con el usuario, mientras que el servidor gestiona los datos, la lógica de negocio y el almacenamiento persistente. Esta separación facilita el mantenimiento, la escalabilidad y la seguridad de las aplicaciones.

- *Cómo funciona por arriba*
    1. El cliente (navegador o app) envía una solicitud HTTP (GET, POST, etc.) a una URL específica
    2. La solicitud viaja a través de Internet hasta llegar al servidor destino
    3. El servidor recibe la petición, la valida, busca o genera el recurso solicitado
    4. El servidor devuelve una respuesta HTTP con el contenido y un código de estado
    5. El cliente recibe la respuesta y renderiza el contenido o procesa los datos

- *Qué implica / qué permite*
    - Acceso centralizado a recursos compartidos (bases de datos, archivos, servicios)
    - Múltiples clientes pueden conectarse simultáneamente al mismo servidor
    - Actualizaciones independientes: se puede modificar el servidor sin afectar a los clientes
    - Seguridad centralizada: el servidor controla el acceso a los datos sensibles
    - Escalabilidad: se pueden agregar más servidores para manejar más carga

## Componentes

| Rol | Ejemplos | Funciones principales |
|-----|----------|----------------------|
| **Cliente** | Navegadores (Chrome, Firefox), apps móviles | Enviar solicitudes HTTP, renderizar HTML/CSS, ejecutar JavaScript, interactuar con el usuario |
| **Servidor** | Apache, Nginx, servicios en la nube (AWS, Azure) | Almacenar archivos y bases de datos, procesar solicitudes, ejecutar lógica de negocio, enviar respuestas |

## Ejemplos comunes

- Navegador web solicitando una página HTML
- App móvil pidiendo datos de una API REST
- Cliente de correo electrónico conectándose al servidor de correo
- Videojuego online donde el cliente se conecta al servidor del juego

## Palabras clave

- Cliente
- Servidor
- Solicitud (Request)
- Respuesta (Response)
- HTTP/HTTPS
- Arquitectura distribuida
- Stateless

## Comparaciones típicas

- vs [[05 - Web - Sitios estáticos]]: en sitios estáticos el servidor solo entrega archivos; en aplicaciones cliente-servidor complejas hay procesamiento en ambos lados
- vs [[06 - Web - Sitios dinámicos]]: los sitios dinámicos implementan el modelo cliente-servidor con generación de contenido en tiempo real
- vs [[03 - Web - Qué es un servidor web]]: el servidor web es la pieza software/hardware que implementa el lado servidor del modelo

## Preguntas de examen

- ¿Cuáles son los dos roles principales en el modelo cliente-servidor?
- ¿Qué ventajas tiene separar el cliente del servidor?
- ¿Por qué se dice que HTTP es un protocolo "stateless"?
- ¿Qué sucede cuando un cliente hace una solicitud a un servidor?

## Errores comunes

- Confundir "cliente" (software) con "usuario" (persona)
- Pensar que el modelo cliente-servidor solo aplica a la web (también se usa en bases de datos, correo, juegos, etc.)
- Creer que el servidor siempre debe estar en la nube; puede ser local (localhost)
- Olvidar que el cliente también puede procesar datos, no solo mostrarlos

## Mini-ejemplo (mental)

Es como ir a un restaurante: **tú eres el cliente**, pides al **mesero (servidor intermediario)** que te traiga comida, y la **cocina (servidor)** prepara tu pedido y te lo envía. Tú no necesitas saber cómo se cocina, solo recibes el resultado. Al mismo tiempo, otros clientes pueden pedir sin interferir con tu orden.
