# TS - Tipos de unión

## Definición

Un tipo de unión (`A | B`) indica que un valor puede ser de más de un tipo, por ejemplo `number | string`.

## Explicación

- *Qué problema resuelve*
    Permite modelar datos que vienen en distintos formatos (IDs numéricos o alfanuméricos, inputs, APIs).

- *Cómo funciona por arriba*
    - Se declara con `|`
    - Dentro de la función, TS solo permite operaciones válidas para todos los tipos
    - Para usar operaciones específicas, se hace *narrowing* (acotación) con chequeos como `typeof`

- *Qué implica / qué permite*
    - Flexibilidad con seguridad: aceptás varios tipos pero los tratás con cuidado
    - Código más expresivo que “cualquier cosa” (`any`)

## Ejemplos comunes

```ts
function imprimirId(id: number | string) {
  if (typeof id === "string") {
    console.log(id.toUpperCase());
  } else {
    console.log(id);
  }
}
```

## Narrowing (idea)

| Técnica | Ejemplo | Resultado |
|---|---|---|
| `typeof` | `typeof x === "string"` | TS trata `x` como `string` en esa rama |
| Propiedad común | `x.length` | válido si ambos tipos la tienen |

## Palabras clave

- Unión `|`
- Narrowing
- `typeof`
- Seguridad

## Comparaciones típicas

- vs [[06 - TS - Tipo any]]: `any` no obliga a chequear; la unión sí.
- vs [[13 - TS - Alias de tipo]]: un alias puede nombrar una unión para reutilizarla.

## Preguntas de examen

- ¿Qué significa `number | string`?
- ¿Por qué TS no permite `id.toUpperCase()` sin chequear primero?
- ¿Qué es el narrowing y cómo se logra?
- ¿Qué pasa si ambos tipos comparten un método o propiedad?

## Errores comunes

- Olvidar el narrowing y forzar con casts (se pierde seguridad).
- Confundir unión con array: `A | B` no es lo mismo que `(A | B)[]`.

## Mini-ejemplo (mental)

Una unión es como un paquete que puede ser de dos marcas: antes de usarlo, mirás la etiqueta para saber qué instrucciones aplicar.
