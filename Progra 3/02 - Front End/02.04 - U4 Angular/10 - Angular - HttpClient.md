# Angular - HttpClient

## Definición

`HttpClient` es el servicio de Angular para realizar peticiones HTTP hacia APIs y consumir respuestas de forma reactiva con observables.

## Explicación

- *Qué problema resuelve*
    Centraliza comunicación con backend sin usar `fetch`/XHR manual en cada componente.

- *Cómo funciona por arriba*
    Se configura con `provideHttpClient()`, se inyecta en servicios/componentes y métodos como `get/post/put/delete` retornan observables.

- *Qué implica / qué permite*
    Facilita manejo de asincronía, errores y transformación de respuesta con RxJS.

## Flujo típico

- Inyectar `HttpClient`
- Llamar a un método HTTP
- Suscribirse al observable (`next`, opcional `error`, opcional `complete`)
- Cargar datos en estado del componente

## Palabras clave

- `provideHttpClient()`
- Observable
- `subscribe`
- API REST
- Asincronismo

## Comparaciones típicas

- vs [[11 - Angular - Observables y RxJS]]: HttpClient usa observables; RxJS define el modelo reactivo y operadores.
- vs [[09 - Angular - Servicios]]: HttpClient suele usarse dentro de servicios para aislar acceso a API.

## Preguntas de examen

- ¿Qué devuelve un método de `HttpClient`?
- ¿Qué callbacks puede recibir `subscribe`?
- ¿Por qué conviene manejar errores de red/API explícitamente?

## Errores comunes

- Consumir API directo en muchos componentes en vez de centralizar en servicios.
- No tipar respuestas y perder ayuda de TypeScript.

## Mini-ejemplo (mental)

`HttpClient` es el “mensajero oficial” de Angular para hablar con el backend de forma estándar y reactiva.
