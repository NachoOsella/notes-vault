# Angular - Comunicación entre componentes

## Definición

La comunicación entre componentes es el intercambio de datos/eventos entre piezas de UI, principalmente con `@Input` y `@Output`, o mediante servicios.

## Explicación

- *Qué problema resuelve*
    Coordina comportamiento entre componentes separados sin acoplarlos en exceso.

- *Cómo funciona por arriba*
    El padre envía datos al hijo con `@Input`; el hijo notifica acciones al padre con `@Output` + `EventEmitter`.

- *Qué implica / qué permite*
    Diseños modulares, con responsabilidades claras y flujo de datos explícito.

## Alternativa con servicios

Para componentes sin relación padre-hijo directa, un servicio compartido con observables permite comunicar estado/eventos.

## Palabras clave

- `@Input`
- `@Output`
- `EventEmitter`
- Padre-hijo
- Servicio compartido

## Comparaciones típicas

- vs [[08 - Angular - Data Binding]]: binding sincroniza componente-template; `@Input/@Output` sincroniza componentes entre sí.
- vs [[09 - Angular - Servicios]]: servicio gana cuando la comunicación no es jerárquica directa.

## Preguntas de examen

- ¿Cómo se implementa un flujo padre -> hijo?
- ¿Cómo se captura en el padre un evento emitido por el hijo?

## Errores comunes

- Usar demasiados eventos encadenados en lugar de estado compartido cuando escala.
- Pasar objetos mutables sin contrato claro y producir efectos colaterales.

## Mini-ejemplo (mental)

`@Input` es “te paso datos”; `@Output` es “te aviso que algo pasó”.
