# RxJS - Operadores

## Definición

Los operadores RxJS son funciones que se encadenan con `.pipe()` para transformar, filtrar, combinar o controlar observables.

## Explicación

- *Qué problema resuelve*
    Evita lógica asíncrona dispersa y permite describir procesamiento de datos en pasos declarativos.

- *Cómo funciona por arriba*
    Cada operador recibe emisiones del observable anterior y entrega un nuevo stream al siguiente operador.

- *Qué implica / qué permite*
    Permite construir pipelines legibles para casos reales: filtrado, mapeo, cancelación, combinación y debugging.

## Operadores frecuentes

- Transformación: `map`, `scan`
- Filtrado/control: `filter`, `take`, `takeUntil`
- Combinación: `merge`, `forkJoin`, `combineLatest`
- Cambio de stream: `switchMap`
- Efectos secundarios: `tap`

## Palabras clave

- `.pipe()`
- Transformación
- Filtrado
- Combinación
- Cancelación

## Comparaciones típicas

- vs `async/await`: async/await modela secuencia de promesas; RxJS modela flujos múltiples en el tiempo.
- vs [[11 - Angular - Observables y RxJS]]: esta nota profundiza en “cómo manipular” observables.

## Preguntas de examen

- ¿Qué diferencia hay entre `map` y `tap`?
- ¿Por qué `switchMap` es útil en búsquedas/peticiones sucesivas?
- ¿Qué hace `takeUntil` en componentes Angular?

## Errores comunes

- Encadenar muchos operadores sin nombrar intenciones y perder legibilidad.
- Usar `forkJoin` con streams que no completan y bloquear resultado final.

## Mini-ejemplo (mental)

Los operadores son como estaciones de una línea de montaje: cada una procesa el dato antes de pasarlo a la siguiente.
