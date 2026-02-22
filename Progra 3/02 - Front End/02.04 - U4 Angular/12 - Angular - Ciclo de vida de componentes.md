# Angular - Ciclo de vida de componentes

## Definición

El ciclo de vida de un componente es la secuencia de eventos/hooks desde su creación, inicialización y chequeos de cambios, hasta su destrucción.

## Explicación

- *Qué problema resuelve*
    Permite ejecutar lógica en momentos precisos (inicialización, cambios, limpieza).

- *Cómo funciona por arriba*
    Angular invoca hooks como `ngOnInit`, `ngOnChanges`, `ngAfterViewInit` y `ngOnDestroy` según la fase.

- *Qué implica / qué permite*
    Facilita inicializar datos, reaccionar a cambios de inputs y liberar recursos correctamente.

## Hooks comunes

- `ngOnChanges`
- `ngOnInit`
- `ngDoCheck`
- `ngAfterContentInit`
- `ngAfterContentChecked`
- `ngAfterViewInit`
- `ngAfterViewChecked`
- `ngOnDestroy`

## Palabras clave

- Hook
- Inicialización
- Detección de cambios
- Limpieza
- `ngOnDestroy`

## Comparaciones típicas

- vs [[11 - Angular - Observables y RxJS]]: en `ngOnDestroy` suele limpiarse suscripciones.
- vs [[15 - Angular - Comunicación entre componentes]]: `ngOnChanges` es clave cuando cambian `@Input`.

## Preguntas de examen

- ¿Para qué se usa `ngOnInit` y en qué se diferencia de `ngOnChanges`?
- ¿Qué tipo de tareas van en `ngOnDestroy`?

## Errores comunes

- Hacer lógica pesada en hooks que se disparan muy seguido (`ngDoCheck`, `ngAfterViewChecked`).
- Omitir limpieza de recursos al destruir el componente.

## Mini-ejemplo (mental)

El ciclo de vida es como la vida útil de un objeto: nace, se prepara, trabaja y finalmente se cierra limpiamente.
