# Web - Sitios dinámicos

## Definición

Un sitio web dinámico es aquel cuyo contenido se genera en tiempo real en el servidor, pudiendo variar según el usuario, la hora, datos de una base de datos u otros factores.

## Explicación

- *Qué problema resuelve*
    Permite crear experiencias personalizadas y contenido que cambia constantemente sin necesidad de modificar archivos manualmente.

- *Cómo funciona por arriba*
    1. El cliente hace una petición HTTP
    2. El servidor recibe la petición y ejecuta código backend (PHP, Node.js, Java, Python, etc.)
    3. El código consulta bases de datos, aplica lógica de negocio, etc.
    4. Se genera HTML dinámicamente y se envía como respuesta
    5. El navegador renderiza el resultado

- *Qué implica / qué permite*
    - Autenticación y sesiones de usuario
    - Contenido personalizado (feed de redes sociales, carrito de compras)
    - CRUDs y aplicaciones web completas
    - Integración con bases de datos

## Ejemplos comunes

- Redes sociales (Facebook, Twitter)
- E-commerce (MercadoLibre, Amazon)
- Aplicaciones web (Gmail, Trello)
- CMS como WordPress

## Palabras clave

- Backend
- Base de datos
- Server-side rendering
- Sesiones
- Autenticación

## Comparaciones típicas

- vs [[05 - Web - Sitios estáticos]]: los estáticos sirven archivos fijos; los dinámicos generan contenido en cada petición
- vs [[03 - Web - Qué es un servidor web]]: en sitios dinámicos, el servidor no solo sirve archivos sino que ejecuta código

## Preguntas de examen

- ¿Qué diferencia hay entre un sitio estático y uno dinámico?
- ¿Qué tecnologías se usan comúnmente en el backend de sitios dinámicos?
- ¿Qué rol juega la base de datos en un sitio dinámico?

## Errores comunes

- Pensar que todo sitio con JavaScript es dinámico (JS en el cliente no lo hace dinámico en el sentido server-side)
- Confundir SPA (Single Page Application) con sitio dinámico tradicional
- Olvidar que los sitios dinámicos requieren más recursos y configuración de seguridad

## Mini-ejemplo (mental)

Cuando entrás a tu perfil de Instagram, el servidor consulta la base de datos para traer TUS fotos, TUS seguidores, y genera una página HTML única para vos.
