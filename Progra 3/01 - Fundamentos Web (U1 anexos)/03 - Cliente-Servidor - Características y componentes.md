# Cliente-Servidor - Características y componentes

## Definición
Conjunto de elementos y rasgos que definen el funcionamiento del modelo donde un cliente solicita un servicio a un servidor con hardware/software especifico a traves de una red.

## Explicación
- *Qué problema resuelve*
    Mantiene la comunicacion de informacion entre entidades de una red usando protocolos y almacenamiento adecuados, separando visualizacion y procesamiento.
- *Cómo funciona por arriba*
    Se basa en el intercambio de mensajes (solicitud/respuesta). Los componentes principales son el cliente, el servidor, el medio (red) y el protocolo (reglas de comunicacion). En Internet, los clientes se conectan a servidores via su ISP para acceder a los servicios requeridos.
- *Qué implica / qué permite*
    Implica una comunicacion asimetrica (el cliente pide, el servidor sirve) y permite conectar varios clientes a los servicios de un mismo servidor en simultaneo.

## Ejemplos de uso
- Navegar sitios web
- Usar protocolos FTP o SSH
- Juegos en red
- Servidores de correo

## Palabras clave
- Asimetría
- Protocolo
- Red (Network)
- Middleware
- Recursos compartidos

## Comparaciones típicas
- vs [[04 - Cliente-Servidor - Componentes]]: acá se describen rasgos/ideas (asimetría, request/response); el otro lista las piezas concretas del modelo.
- vs [[05 - Cliente-Servidor - Clientes y servidores]]: acá se describen características del modelo; el otro baja al detalle de roles (quién pide vs quién responde).
- vs [[07 - HTTP - Sistemas basados en HTTP]]: cliente-servidor es el modelo general; HTTP es un caso concreto aplicado a la Web.

## Preguntas de examen
- ¿Cuáles son los 4 componentes básicos del modelo cliente-servidor?
- ¿Qué significa que la relación sea asimétrica?
- ¿Por qué es necesario un protocolo?

## Errores comunes
- Olvidar que la red es un componente esencial.
- Pensar que cliente y servidor deben estar en máquinas diferentes (pueden ser procesos en la misma PC).

## Mini-ejemplo (mental)
- Navegar por la web: Tu navegador (cliente) usa el cable o Wi-Fi (medio) siguiendo reglas (protocolo HTTP) para pedir una página a una computadora en otro lugar (servidor).
