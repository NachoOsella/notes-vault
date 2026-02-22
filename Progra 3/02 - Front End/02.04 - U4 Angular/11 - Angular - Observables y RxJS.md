# Angular - Observables y RxJS

## Definición

Un observable representa una secuencia de datos en el tiempo. RxJS es la librería que Angular usa para crear, transformar y combinar esos flujos reactivos.

## Explicación

- *Qué problema resuelve*
    Modela asincronía (HTTP, eventos, timers, streams) de forma uniforme y componible.

- *Cómo funciona por arriba*
    Te suscribís con `subscribe()` para recibir emisiones (`next`), errores (`error`) y finalización (`complete`).

- *Qué implica / qué permite*
    Permite construir UI reactiva, controlar suscripciones y transformar datos con operadores en `.pipe()`.

## Suscripción y desuscripción

- Observables de `HttpClient` suelen completar solos.
- Streams como `interval`, eventos, `Subject` o sockets no completan solos.
- Para limpiar suscripciones: `unsubscribe()` o `takeUntil`.

## Palabras clave

- Observable
- `subscribe`
- `pipe`
- `takeUntil`
- Memory leak

## Comparaciones típicas

- vs Promesas: promesa emite un único resultado; observable puede emitir múltiples valores.
- vs [[10 - Angular - HttpClient]]: HttpClient es un caso concreto de uso de observables.

## Preguntas de examen

- ¿Qué diferencia hay entre `next`, `error` y `complete`?
- ¿Cuándo corresponde desuscribirse manualmente?

## Errores comunes

- No desuscribirse de streams infinitos en `ngOnDestroy`.
- Tratar un observable como si fuera un valor inmediato/síncrono.

## Mini-ejemplo (mental)

Observable es como una radio en vivo: te suscribís para escuchar emisiones a medida que llegan.
