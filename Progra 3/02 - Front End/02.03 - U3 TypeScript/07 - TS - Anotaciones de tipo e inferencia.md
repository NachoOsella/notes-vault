# TS - Anotaciones de tipo e inferencia

## Definición

En TypeScript podés **anotar** tipos explícitamente (`: Tipo`) o dejar que el compilador los **infiera** a partir del valor inicial.

## Explicación

- *Qué problema resuelve*
    Reduce errores por asignaciones incompatibles y mejora la legibilidad del código.

- *Cómo funciona por arriba*
    - Anotación explícita: `let nombre: string = "Juan";`
    - Inferencia: `let ciudad = "Rosario";` (TS deduce `string`)
    - Si luego intentás asignar otro tipo, TS marca error

- *Qué implica / qué permite*
    - Menos redundancia: la inferencia suele alcanzar
    - Anotar ayuda cuando el contexto no es suficiente o como “documentación”

## Ejemplos comunes

```ts
let miNombre: string = "Juan";
let miCiudad = "Rosario"; // TS infiere string
// miCiudad = 123; // error de tipos
```

## Palabras clave

- Anotación `: Tipo`
- Inferencia
- Redundancia
- Legibilidad

## Comparaciones típicas

- vs [[04 - TS - Tipos primitivos]]: la inferencia se apoya en valores primitivos iniciales.
- vs [[30 - TS - tsconfig.json]]: `strict`/`noImplicitAny` cambian qué tanto TS exige tipos.

## Preguntas de examen

- ¿Qué es la inferencia de tipos?
- ¿Cómo se anota un tipo en una variable?
- ¿Cuándo conviene anotar explícitamente?
- ¿Qué pasa si reasignás un tipo distinto al inferido?

## Errores comunes

- Anotar todo incluso cuando es obvio (ruido).
- Confiar en la inferencia cuando el valor inicial es `null`/`undefined` y falta contexto. Ver: [[16 - TS - null y undefined]]

## Mini-ejemplo (mental)

La inferencia es como un profesor que deduce de tu primera respuesta qué tema estás usando; la anotación es decirlo explícitamente.
