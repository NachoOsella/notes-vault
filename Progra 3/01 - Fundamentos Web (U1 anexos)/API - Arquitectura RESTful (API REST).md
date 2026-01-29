# API - Arquitectura RESTful (API REST)

## Definición
REST (Representational State Transfer) es un estilo de arquitectura para diseñar servicios web de forma sencilla y estandarizada, que aprovecha el protocolo HTTP para intercambiar datos de forma intuitiva, eficiente y escalable.

## Explicación
- *Qué problema resuelve*
    Estandariza la comunicación entre cliente y servidor usando las mismas reglas que gobiernan la Web, permitiendo que sistemas desarrollados en distintas tecnologías interactúen fácilmente.
- *Cómo funciona por arriba*
    Se basa en recursos identificados por URLs y acciones definidas por verbos HTTP (GET, POST, PUT, DELETE). El cliente realiza una petición y el servidor devuelve una representación del recurso, usualmente en JSON.
- *Qué implica / qué permite*
    Permite la separación clara entre cliente y servidor, ausencia de estado (stateless) para mejorar escalabilidad, y uso de formatos ligeros para transmisión rápida.

## Características clave de REST

### Cliente/Servidor
La API REST sigue un modelo cliente-servidor puro donde cliente y servidor están separados. Esto permite que evolucionen independientemente: el cliente solo necesita saber cómo pedir datos, y el servidor cómo entregarlos.

### Sin estado (Stateless)
Cada petición HTTP debe contener toda la información necesaria. El servidor no guarda estado de interacciones previas con el cliente. Esto mejora la escalabilidad, aunque el cliente debe enviar información adicional (como tokens) en cada solicitud.

### Uso de HTTP y uniformidad
Se utilizan los verbos HTTP estándar para operar sobre datos:

| Verbo | Acción | Ejemplo |
|-------|--------|---------|
| **GET** | Leer/consultar recursos | `GET /libros/123` |
| **POST** | Crear nuevos recursos | `POST /libros` |
| **PUT** | Reemplazar recurso completo | `PUT /libros/123` |
| **PATCH** | Modificar parcialmente | `PATCH /libros/123` |
| **DELETE** | Eliminar recurso | `DELETE /libros/123` |

### Formato de datos ligero
Aunque REST puede trabajar con XML o texto plano, lo más común hoy es **JSON** (JavaScript Object Notation) por su ligereza y legibilidad.

```json
{
  "titulo": "El Principito",
  "autor": "Antoine de Saint-Exupéry",
  "anio": 1943
}
```

## Ejemplo de flujo REST
1. Cliente solicita: `GET https://api.ejemplo.com/usuarios/42`
2. Servidor procesa la petición
3. Servidor responde con JSON:
```json
{
  "id": 42,
  "nombre": "Juan",
  "email": "juan@ejemplo.com"
}
```

## Palabras clave
- REST (Representational State Transfer)
- Stateless (Sin estado)
- Recursos (Resources)
- Endpoints
- Verbos HTTP
- JSON
- URL

## Comparaciones típicas
- vs [[API - REST vs SOAP]]: REST es un estilo arquitectónico más ligero/flexible; SOAP es un protocolo más rígido basado en XML y contrato.
- vs [[HTTP - Métodos de solicitud]]: REST se apoya en los verbos HTTP para modelar operaciones sobre recursos.
- vs [[HTTP - Características clave]]: REST hereda de HTTP ideas como stateless y uso de headers/representaciones.

## Preguntas de examen
- ¿Qué significa REST?
- ¿Cuáles son los verbos HTTP principales usados en REST?
- ¿Qué implica que REST sea "stateless"?
- ¿Por qué se prefiere JSON en las APIs REST?
- ¿Qué es un endpoint en REST?

## Errores comunes
- Creer que REST es un protocolo (es un estilo de arquitectura).
- Pensar que el servidor guarda información de la sesión entre peticiones.
- No usar los verbos HTTP correctamente (ej. usar GET para crear datos).
- Confundir PUT (reemplaza todo) con PATCH (modifica parcialmente).

## Mini-ejemplo (mental)
Una librería online: Accedes a `GET /libros/123` para ver detalles de un libro, usas `POST /libros` para agregar uno nuevo, o `DELETE /libros/123` para quitarlo del catálogo. El servidor responde con un objeto JSON con el título y autor. Como es stateless, cada petición debe incluir tu token de autenticación.
