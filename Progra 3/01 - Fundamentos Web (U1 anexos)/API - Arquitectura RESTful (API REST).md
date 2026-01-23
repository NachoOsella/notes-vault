# Arquitectura RESTful (API REST)

## Definición
Estilo de arquitectura para diseñar servicios web de forma sencilla y estandarizada, que aprovecha el protocolo HTTP para intercambiar datos de forma intuitiva, eficiente y escalable.

## Explicación
- *Qué problema resuelve*
    Estandariza la comunicación entre cliente y servidor usando las mismas reglas que gobiernan la Web, permitiendo que sistemas desarrollados en distintas tecnologías interactúen fácilmente.
- *Cómo funciona por arriba*
    Se basa en recursos identificados por URLs y acciones definidas por verbos HTTP (GET, POST, PUT, DELETE). El cliente realiza una petición y el servidor devuelve una representación del recurso, usualmente en JSON.
- *Qué implica / qué permite*
    Permite la separación clara entre cliente y servidor, la ausencia de estado (stateless) para mejorar la escalabilidad, y el uso de formatos ligeros para una transmisión rápida.

## Palabras clave
- REST (Representational State Transfer)
- Stateless (Sin estado)
- Recursos (Resources)
- Verbos HTTP
- JSON

## Comparaciones típicas
- vs [[API - REST vs SOAP]]: REST es un estilo arquitectónico más ligero/flexible; SOAP es un protocolo más rígido basado en XML y contrato.
- vs [[HTTP - Métodos de solicitud]]: REST se apoya en los verbos HTTP para modelar operaciones sobre recursos.
- vs [[HTTP - Características clave]]: REST hereda de HTTP ideas como stateless y uso de headers/representaciones.

## Preguntas de examen
- ¿Qué significa REST?
- ¿Cuáles son los verbos HTTP principales usados en REST?
- ¿Qué implica que REST sea "stateless"?
- ¿Por qué se prefiere JSON en las APIs REST?

## Errores comunes
- Creer que REST es un protocolo (es un estilo de arquitectura).
- Pensar que el servidor guarda información de la sesión entre peticiones.
- No usar los verbos HTTP correctamente (ej. usar GET para crear datos).

## Mini-ejemplo (mental)
- Una librería online: Accedes a `GET /libros/123` para ver detalles de un libro, o usas `DELETE /libros/123` para quitarlo del catálogo. El servidor responde con un objeto JSON con el título y autor.
