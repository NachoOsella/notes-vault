# HTTP - User Agent (cliente)

## Definición
Cualquier herramienta o programa que actúa en representación del usuario para iniciar peticiones en un sistema HTTP (generalmente un navegador web).

## Explicación
- *Qué problema resuelve*
    Actúa como la interfaz entre el humano y el protocolo, abstrayendo la complejidad de las peticiones técnicas para presentar la información de forma visual (renderizado).
- *Cómo funciona por arriba*
    Siempre es el que inicia la comunicación. Envía la petición inicial, procesa el HTML recibido, detecta necesidades de recursos adicionales (imágenes, scripts) y ejecuta el código (JS) para actualizar la página.
- *Qué implica / qué permite*
    Permite la navegación mediante hipervínculos, traduciendo clics en peticiones HTTP. También puede ser un robot (crawler) para buscadores o herramientas de desarrollo.

## Palabras clave
- Navegador (Browser)
- Iniciador de petición
- Renderizado
- Robot / Crawler
- Hipertexto

## Comparaciones típicas
- vs [[HTTP - Servidor Web]]: el user agent inicia la comunicación (requests); el servidor espera y responde.
- vs [[Cliente-Servidor - Clientes y servidores]]: el user agent es el cliente en HTTP; el modelo cliente-servidor es el concepto general.
- vs [[HTTP - Proxies]]: el user agent habla con el servidor directamente o a través de intermediarios (proxy), pero sigue iniciando requests.

## Preguntas de examen
- ¿Quién inicia siempre la comunicación en HTTP?
- ¿Qué hace el navegador después de recibir el primer documento HTML?
- ¿Qué otros tipos de User Agent existen además de los navegadores?

## Errores comunes
- Creer que el servidor puede enviar datos al cliente sin que este los haya pedido primero.
- Pensar que "User Agent" solo se refiere a una cadena de texto (es la herramienta completa).

## Mini-ejemplo (mental)
- Chrome es tu User Agent: cuando haces clic en un enlace, él escribe la petición técnica por ti, espera la respuesta y dibuja la página resultante en tu pantalla.
