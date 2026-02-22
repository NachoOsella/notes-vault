# RxJS - Subject y BehaviorSubject

## Definición

`Subject` es un observable que además permite emitir valores manualmente. `BehaviorSubject` extiende esa idea guardando y reemitiendo el último valor a nuevos suscriptores.

## Explicación

- *Qué problema resuelve*
    Permite comunicación reactiva y estado compartido entre componentes/servicios.

- *Cómo funciona por arriba*
    `Subject` multicasting: varios suscriptores reciben emisiones futuras; `BehaviorSubject` también entrega valor actual al suscriptor nuevo.

- *Qué implica / qué permite*
    `Subject` sirve para eventos; `BehaviorSubject` sirve para estado de aplicación (ej. usuario actual).

## Diferencias clave

- `Subject`: no requiere valor inicial, no replay del último valor.
- `BehaviorSubject`: requiere valor inicial y entrega el último valor al suscribirse.

## Palabras clave

- Subject
- BehaviorSubject
- Multicasting
- Estado compartido
- Valor actual

## Comparaciones típicas

- vs [[11 - Angular - Observables y RxJS]]: ambos son tipos concretos dentro del modelo observable.
- vs eventos DOM: Subject permite un bus reactivo controlado por servicios.

## Preguntas de examen

- ¿Qué problema típico resuelve `BehaviorSubject` mejor que `Subject`?
- ¿Por qué se usa `asObservable()` al exponer streams desde un servicio?

## Errores comunes

- Exponer el `Subject` público y permitir `next()` desde cualquier lado.
- Usar `BehaviorSubject` sin un valor inicial significativo.

## Mini-ejemplo (mental)

`Subject` es una radio en vivo; `BehaviorSubject` es la radio que además te repite el último titular al conectarte.
