# Web - Sitios estáticos

## Definición

Un sitio web estático es aquel cuyo contenido (HTML, CSS, JS, imágenes) está pre-generado y se sirve idéntico a todos los usuarios, sin procesamiento en el servidor.

## Explicación

- *Qué problema resuelve*
    Provee una forma simple, rápida y segura de publicar contenido que no cambia frecuentemente o no requiere personalización por usuario.

- *Cómo funciona por arriba*
    1. El desarrollador crea archivos HTML/CSS/JS
    2. Los archivos se suben al servidor
    3. Ante cada petición, el servidor simplemente devuelve el archivo solicitado
    4. No hay ejecución de código en el servidor (solo se "sirven" archivos)

- *Qué implica / qué permite*
    - Mayor velocidad de carga (no hay procesamiento)
    - Mayor seguridad (menos superficie de ataque)
    - Hosting más económico (GitHub Pages, Netlify, Vercel)
    - Ideal para portfolios, blogs, documentación

## Ejemplos comunes

- Landing pages
- Documentación técnica (como GitBook o Docusaurus)
- Portfolios personales
- Blogs generados con Jekyll, Hugo, Gatsby

## Palabras clave

- HTML/CSS/JS
- Pre-generado
- Sin backend
- CDN
- JAMstack

## Comparaciones típicas

- vs [[06 - Web - Sitios dinámicos]]: los sitios dinámicos generan contenido en tiempo real según el usuario o contexto; los estáticos sirven siempre lo mismo
- vs [[03 - Web - Qué es un servidor web]]: el servidor solo entrega archivos, no ejecuta lógica

## Preguntas de examen

- ¿Qué caracteriza a un sitio web estático?
- ¿Cuáles son las ventajas de un sitio estático sobre uno dinámico?
- ¿Qué tipo de contenido es más apropiado para un sitio estático?

## Errores comunes

- Pensar que "estático" significa que no puede tener interactividad (puede tener JS del lado del cliente)
- Creer que los sitios estáticos no pueden consumir APIs (sí pueden, vía fetch/AJAX)
- Confundir estático con "simple" o "limitado"

## Mini-ejemplo (mental)

Tu portfolio en GitHub Pages: subís los archivos HTML y CSS, y cuando alguien entra, el servidor le devuelve exactamente esos archivos sin modificarlos.
