# Preguntas - Fundamentos Web

## Cliente-Servidor

### Que es la arquitectura cliente-servidor?
Respuesta: Modelo donde un cliente solicita servicios a un servidor a traves de una red, separando roles y responsabilidades. Ver: [[03 - Cliente-Servidor - Características y componentes]]

### Cuales son los componentes basicos del modelo?
Respuesta: Cliente, servidor, red, protocolo, servicio y base de datos como soporte de la comunicacion. Ver: [[04 - Cliente-Servidor - Componentes]]

### En que se diferencian cliente y servidor?
Respuesta: El cliente demanda servicios y el servidor los provee; el servidor suele tener mas capacidad y maneja multiples solicitudes. Ver: [[05 - Cliente-Servidor - Clientes y servidores]]

### Menciona ventajas y desventajas del modelo
Respuesta: Ventajas: escalabilidad, integracion, flexibilidad. Desventajas: punto unico de falla, costos altos, complejidad de mantenimiento. Ver: [[06 - Cliente-Servidor - Ventajas y desventajas]]

### Que ejemplos cotidianos usan cliente-servidor?
Respuesta: Navegar web, FTP, SSH, correo electronico, juegos en red.

---

## HTTP

### Que es HTTP y por que es stateless?
Respuesta: Protocolo base de la Web que no guarda estado entre solicitudes; el contexto se maneja con cookies o tokens. Ver: [[11 - HTTP - Características clave]]

### Quien inicia la comunicacion en HTTP?
Respuesta: El user agent (cliente) inicia las peticiones y el servidor solo responde. Ver: [[08 - HTTP - User Agent (cliente)]]

### Cuales son los pasos del flujo de mensajes HTTP?
Respuesta: Abrir conexion TCP, enviar request, recibir response y cerrar o reusar la conexion. Ver: [[12 - HTTP - Flujo de mensajes]]

### Que partes componen un request HTTP?
Respuesta: Metodo, URL, version, cabeceras y cuerpo opcional. Ver: [[13 - HTTP - Request]]

### Que partes componen un response HTTP?
Respuesta: Version, codigo y mensaje de estado, cabeceras y cuerpo con el recurso. Ver: [[14 - HTTP - Response]]

### Para que sirven los metodos HTTP?
Respuesta: Indican la accion sobre un recurso (GET, POST, PUT, PATCH, DELETE, etc.) y definen su semantica. Ver: [[15 - HTTP - Métodos de solicitud]]

### Que indican los codigos de estado 2xx, 4xx y 5xx?
Respuesta: 2xx = exito, 4xx = error del cliente, 5xx = error del servidor. Ver: [[16 - HTTP - Códigos de estado]]

### Que es un proxy en HTTP?
Respuesta: Intermediario que puede cachear, filtrar o balancear trafico entre cliente y servidor. Ver: [[10 - HTTP - Proxies]]

### Que cambio entre HTTP/1.1 y HTTP/2?
Respuesta: HTTP/2 usa formato binario con tramas y permite multiplexacion; HTTP/1.1 usa texto plano legible.

---

## APIs y Servicios Web

### Que es una API?
Respuesta: Conjunto de reglas y protocolos para que aplicaciones se comuniquen sin conocer detalles internos. Ver: [[17 - API - Qué es una API]]

### Cual es la analogia tipica para explicar una API?
Respuesta: El mesero de un restaurante: recibe el pedido del cliente, lo lleva a la cocina y trae el resultado.

### En que se diferencia una API de un servicio web?
Respuesta: Un servicio web es una API que opera sobre la red con protocolos web (HTTP); no todas las APIs son servicios web. Ver: [[18 - API - Qué es un Servicio Web]]

### Que es REST y que implica ser stateless?
Respuesta: Estilo arquitectonico basado en recursos y verbos HTTP; stateless implica que cada request lleva todo el contexto. Ver: [[19 - API - Arquitectura RESTful (API REST)]]

### Cuales son las caracteristicas clave de REST?
Respuesta: Cliente/servidor separados, stateless, uso de verbos HTTP, recursos con URLs, formato JSON.

### Cual es la diferencia clave entre REST y SOAP?
Respuesta: REST es ligero y orientado a recursos con JSON/HTTP; SOAP es un protocolo rigido basado en XML y WSDL. Ver: [[20 - API - REST vs SOAP]]

### Que tipos de APIs existen segun su alcance?
Respuesta: Locales (mismo dispositivo), remotas (en red) y web (remotas basadas en HTTP). Ver: [[21 - API - Tipos de APIs (locales vs remotas vs web)]]

---

## Respuestas rapidas

| Pregunta | Respuesta corta |
|----------|-----------------|
| Cliente vs Servidor | Cliente pide, servidor provee |
| HTTP stateless | No guarda estado entre peticiones |
| Metodos HTTP principales | GET, POST, PUT, PATCH, DELETE |
| Codigo 200 | Exito |
| Codigo 404 | Recurso no encontrado |
| Codigo 500 | Error del servidor |
| API vs Servicio Web | API puede ser local; servicio web siempre usa red |
| REST vs SOAP | REST = ligero/JSON; SOAP = rigido/XML |
