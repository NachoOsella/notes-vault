# TS - Tipos primitivos

## Definición

Los tipos primitivos básicos en TypeScript (igual que en JavaScript) son `string`, `number` y `boolean`.

## Explicación

- *Qué problema resuelve*
    Permite describir qué tipo de dato se espera y detectar asignaciones incorrectas en compilación.

- *Cómo funciona por arriba*
    - Anotás el tipo: `let nombre: string = "Juan";`
    - O dejás que TS lo infiera: `let ciudad = "Rosario";` (infiere `string`)

- *Qué implica / qué permite*
    - Evitar mezclar tipos por error (ej: sumar número con string sin querer)
    - Mejor autocompletado y chequeo de operaciones válidas

## Ejemplos comunes

```ts
let nombre: string = "Ana";
let edad: number = 26;
let activo: boolean = true;
```

## Palabras clave

- `string`
- `number`
- `boolean`
- Inferencia
- Anotación de tipo

## Comparaciones típicas

- vs [[07 - TS - Anotaciones de tipo e inferencia]]: esa nota explica cuándo conviene anotar vs inferir.
- vs [[06 - TS - Tipo any]]: `any` desactiva el chequeo; los primitivos lo aprovechan.

## Preguntas de examen

- ¿Cuáles son los tipos primitivos básicos en TypeScript?
- ¿Qué significa que TypeScript “infiera” el tipo?
- ¿Qué ventaja tiene anotar un tipo explícitamente?
- ¿Qué pasa si intentás asignar un `number` a una variable `string`?

## Errores comunes

- Asumir que existen tipos separados para enteros y flotantes (en JS/TS todo es `number`).
- Anotar tipos redundantes siempre (a veces la inferencia alcanza).

## Mini-ejemplo (mental)

Los tipos primitivos son como etiquetas en cajas: si una caja dice “string”, no deberías meter un número ahí.
