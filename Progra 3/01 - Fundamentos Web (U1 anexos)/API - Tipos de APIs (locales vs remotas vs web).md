# Tipos de APIs (locales vs remotas vs web)

## Definición
Clasificación de las APIs según el entorno en el que operan y el alcance de su comunicación.

## Explicación
- *Qué problema resuelve*
    Diferencia cómo se accede a las funcionalidades: si están dentro del mismo equipo, en otro servidor de la red, o disponibles a través de protocolos web estándar en Internet.
- *Cómo funciona por arriba*
    Las **Locales** llaman a funciones del SO o librerías instaladas. Las **Remotas** usan la red para conectar dos sistemas. Las **Web** son un subconjunto de las remotas que usan HTTP y estándares web.
- *Qué implica / qué permite*
    Permite elegir la tecnología adecuada según la necesidad: una API de sistema para usar la cámara del móvil, o una API web para integrar mapas de Google en una aplicación.

## Palabras clave
- API Local (Win32, iOS/Android SDK)
- API Remota (RPC, Sockets)
- API Web (Endpoints, HTTP)
- Entorno de ejecución

## Comparaciones típicas
- vs [[API - Qué es una API]]: acá se clasifica por alcance (local/remota/web); el otro da la definición general de API.
- vs [[API - Qué es un Servicio Web]]: una API web suele ser un servicio web cuando expone endpoints por red (HTTP/HTTPS).
- vs [[API - Arquitectura RESTful (API REST)]]: REST es una forma típica de implementar una API web; no aplica a APIs locales.

## Preguntas de examen
- ¿Qué es una API local y dar un ejemplo?
- ¿Toda API web es una API remota?
- ¿Qué protocolo es fundamental en las APIs Web?

## Errores comunes
- Pensar que todas las APIs necesitan Internet (las locales no).
- Confundir una API remota genérica con una API Web específica.

## Mini-ejemplo (mental)
- **Local:** La app de fotos pidiendo permiso al Android para usar la cámara.
- **Remota:** Una aplicación accediendo a una base de datos en el servidor de la empresa.
- **Web:** Tu sitio web obteniendo los últimos tweets mediante la API de Twitter sobre Internet.
