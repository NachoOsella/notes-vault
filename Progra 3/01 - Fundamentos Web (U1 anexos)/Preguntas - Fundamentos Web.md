# Preguntas - Fundamentos Web

## Cliente-Servidor
- ¿Qué es la arquitectura cliente-servidor y cuál es su propósito?
- ¿Cuáles son los componentes del modelo (red, cliente, servidor, protocolo, servicios, base de datos)?
- ¿Cuál es la diferencia entre un cliente y un servidor?
- ¿Qué ejemplos cotidianos usan arquitectura cliente-servidor (web, FTP, SSH, correo)?
- Menciona ventajas clave del modelo cliente-servidor.
- Menciona desventajas clave del modelo cliente-servidor.

## HTTP
- ¿Qué es HTTP y por qué es un protocolo cliente-servidor?
- ¿Qué significa que HTTP sea stateless y cómo se maneja el estado?
- ¿Qué es el user agent y qué tareas realiza al cargar una página?
- ¿Qué es un servidor web y por qué puede estar compuesto por varios elementos?
- ¿Qué funciones puede cumplir un proxy HTTP?
- ¿Cuáles son los pasos del flujo de mensajes HTTP?
- ¿Qué partes componen un request HTTP?
- ¿Qué partes componen un response HTTP?
- ¿Cuáles son los métodos HTTP principales y qué hace cada uno?
- ¿Qué clases de códigos de estado existen y qué indican?
- ¿Qué significan los códigos 200, 201, 301, 404 y 503?
- ¿Qué cambió en el formato de mensajes entre HTTP/1.1 y HTTP/2?

## APIs y Servicios Web
- ¿Qué es una API y cuál es la analogía del "mesero"?
- Da ejemplos de APIs que usas en la vida real.
- ¿Qué es un servicio web y en qué se diferencia de una API local?
- ¿Qué estilos principales de servicios web existen (REST y SOAP)?
- ¿Qué es REST y cuáles son sus características clave?
- ¿Qué verbos HTTP se usan típicamente en una API REST?
- ¿Qué diferencias hay entre REST y SOAP en formato, transporte y complejidad?
- ¿Qué tipos de APIs existen (local, remota, web) y cómo se relacionan?
# Preguntas - Fundamentos Web

## Cliente-Servidor

### Que es la arquitectura cliente-servidor?
Respuesta: Modelo donde un cliente solicita servicios a un servidor a traves de una red, separando roles y responsabilidades. Ver: [[Cliente-Servidor - Características y componentes]]

### Cuales son los componentes basicos del modelo?
Respuesta: Cliente, servidor, red, protocolo, servicio y base de datos como soporte de la comunicacion. Ver: [[Cliente-Servidor - Componentes]]

### En que se diferencian cliente y servidor?
Respuesta: El cliente demanda servicios y el servidor los provee; el servidor suele tener mas capacidad y maneja multiples solicitudes. Ver: [[Cliente-Servidor - Clientes y servidores]]

### Menciona dos ventajas y dos desventajas del modelo
Respuesta: Ventajas como escalabilidad e integracion; desventajas como punto unico de falla y costos altos de infraestructura. Ver: [[Cliente-Servidor - Ventajas y desventajas]]

## HTTP

### Que es HTTP y por que es stateless?
Respuesta: Es el protocolo base de la Web y no guarda estado entre solicitudes; el contexto se maneja con cookies o tokens. Ver: [[HTTP - Características clave]]

### Quien inicia la comunicacion en HTTP?
Respuesta: El user agent (cliente) inicia las peticiones y el servidor solo responde. Ver: [[HTTP - User Agent (cliente)]]

### Cuales son los pasos del flujo de mensajes HTTP?
Respuesta: Abrir conexion TCP, enviar request, recibir response y cerrar o reusar la conexion. Ver: [[HTTP - Flujo de mensajes]]

### Que partes componen un request HTTP?
Respuesta: Metodo, URL, version, cabeceras y cuerpo opcional. Ver: [[HTTP - Request]]

### Que partes componen un response HTTP?
Respuesta: Version, codigo y mensaje de estado, cabeceras y cuerpo con el recurso. Ver: [[HTTP - Response]]

### Para que sirven los metodos HTTP?
Respuesta: Indican la accion sobre un recurso (GET, POST, PUT, PATCH, DELETE, etc.) y definen su semantica. Ver: [[HTTP - Métodos de solicitud]]

### Que indican los codigos de estado 2xx y 4xx?
Respuesta: 2xx indica exito y 4xx errores del cliente (por ejemplo 404). Ver: [[HTTP - Códigos de estado]]

### Que es un proxy en HTTP?
Respuesta: Intermediario que puede cachear, filtrar o balancear trafico entre cliente y servidor. Ver: [[HTTP - Proxies]]

## APIs y servicios web

### Que es una API?
Respuesta: Conjunto de reglas y protocolos para que aplicaciones se comuniquen sin conocer detalles internos. Ver: [[API - Qué es una API]]

### En que se diferencia una API de un servicio web?
Respuesta: Un servicio web es una API que opera sobre la red con protocolos web; no todas las APIs son servicios web. Ver: [[API - Qué es un Servicio Web]]

### Que es REST y que implica ser stateless?
Respuesta: Es un estilo arquitectonico basado en recursos y verbos HTTP; stateless implica que cada request lleva todo el contexto. Ver: [[API - Arquitectura RESTful (API REST)]]

### Cual es la diferencia clave entre REST y SOAP?
Respuesta: REST es ligero y orientado a recursos con JSON/HTTP; SOAP es un protocolo rigido basado en XML y WSDL. Ver: [[API - REST vs SOAP]]

### Que tipos de APIs existen segun su alcance?
Respuesta: Locales (mismo dispositivo), remotas (en red) y web (remotas basadas en HTTP). Ver: [[API - Tipos de APIs (locales vs remotas vs web)]]
