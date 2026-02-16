# TS - null y undefined

## Definición

`undefined` suele significar “no existe valor” (por ejemplo, propiedad ausente) y `null` “valor intencionalmente vacío”.

## Explicación

- *Qué problema resuelve*
    Modela ausencia de datos de forma explícita y obliga a tratar casos que podrían romper en runtime.

- *Cómo funciona por arriba*
    - Un valor puede ser `string | undefined` o `string | null`
    - Con configuración estricta (por ejemplo `strictNullChecks` dentro de `strict`), TS exige chequear antes de usar

- *Qué implica / qué permite*
    - Menos errores por acceder a algo que no existe
    - Mejor modelado de APIs/formularios

## Ejemplos comunes

```ts
function imprimir(x: string | undefined) {
  if (x !== undefined) console.log(x.toUpperCase());
}
```

## Palabras clave

- `null`
- `undefined`
- `strict` / `strictNullChecks`
- Chequeo

## Comparaciones típicas

- vs [[11 - TS - Propiedades opcionales]]: lo opcional suele ser `undefined` cuando falta.
- vs [[12 - TS - Tipos de unión]]: `null`/`undefined` suelen modelarse con uniones.

## Preguntas de examen

- ¿Qué diferencia conceptual hay entre `null` y `undefined`?
- ¿Por qué conviene chequear antes de usar un valor opcional?
- ¿Qué configuración hace más estricto el manejo de null/undefined?

## Errores comunes

- Asumir que una propiedad opcional siempre viene.
- Resolver con `any` en vez de modelar el caso faltante.

## Mini-ejemplo (mental)

`undefined` es “no está en la caja”. `null` es “la caja está, pero está vacía a propósito”.
