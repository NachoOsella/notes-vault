# API - Servicios Web

## Definición
Un servicio web es un tipo de API que permite la comunicación entre aplicaciones siguiendo protocolos web entre equipos a través de una red, generalmente Internet. Se maneja mediante request y response.

## Explicación
- *Qué problema resuelve*
    Permite que diferentes aplicaciones/sistemas se comuniquen e intercambien informacion de manera estandarizada, independientemente de la ubicación o la plataforma en la que se ejecuten siempre y cuando tengan acceso a la red.
- *Cómo funciona por arriba*
    Un cliente envia una solicitud (request) generalmente mediante una URL a un servidor que exponse sus endpoints a traves de protocolos web (HTTP/HTTPS). El servidor procesa la solicitud y devuelve una respuesta(response) con los datos solicitados, generalmente en formatos como JSON o XML.
- *Qué implica / qué permite*
    Permite la integracion entre sistemas desarrollados en diferentes plataformas o lenguajes de programacion, facilitando la interoperabilidad y la escalabilidad de aplicaciones distribuidas.

## Estilos principales
- SOAP: protocolo estructurado con mensajes XML y contrato WSDL.
- REST: estilo arquitectonico basado en HTTP y recursos.


## Palabras clave
- Red
- HTTP/HTTPS
- Protocolos

## Comparaciones típicas
- vs [[17 - API - Qué es una API]]: todo servicio web es una API; no toda API es servicio web (puede ser local o no usar HTTP).
- vs [[13 - HTTP - Request]] / [[14 - HTTP - Response]]: un servicio web se consume via request/response sobre HTTP/HTTPS.
- vs [[20 - API - REST vs SOAP]]: REST y SOAP son estilos/protocolos comunes para implementar servicios web.

## Preguntas de examen
- ¿Qué es un servicio web?
- ¿Para qué sirven los servicios web?
- ¿Cuál es la diferencia entre una API y un servicio web?
- ¿Qué pasa si un servicio web no tiene acceso a Internet?

## Errores comunes
- Confundir servicios web con APIs en general.
- Pensar que todos los servicios web usan el mismo protocolo o formato de datos.
- Asumir que un servicio web solo puede ser consumido por aplicaciones web.

## Mini-ejemplo (mental)
- Una aplicación móvil que consume datos de un servicio web RESTful para mostrar el clima actual en una ciudad específica. La app envía una solicitud HTTP al servicio web y recibe una respuesta en formato JSON con la información del clima.
