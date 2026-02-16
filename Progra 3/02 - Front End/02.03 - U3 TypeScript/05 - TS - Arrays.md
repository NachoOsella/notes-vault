# TS - Arrays

## Definición

Un array tipado en TypeScript es una lista de elementos donde cada elemento cumple un tipo (por ejemplo `number[]` o `Array<string>`).

## Explicación

- *Qué problema resuelve*
    Evita mezclar tipos dentro de una colección por accidente (ej: números y strings juntos).

- *Cómo funciona por arriba*
    TypeScript ofrece dos sintaxis equivalentes:
    - `Tipo[]` (corchetes)
    - `Array<Tipo>` (genérica)

- *Qué implica / qué permite*
    - Autocompletado de métodos y chequeo de tipos al hacer `push`, `map`, etc.
    - Errores en compilación si se inserta un elemento del tipo incorrecto

## Ejemplos comunes

```ts
const numeros: number[] = [1, 2, 3];
const palabras: Array<string> = ["hola", "ts"];
```

## Palabras clave

- `Tipo[]`
- `Array<Tipo>`
- Colección
- Inferencia

## Comparaciones típicas

- vs [[04 - TS - Tipos primitivos]]: los arrays son colecciones de primitivos (u otros tipos).
- vs [[12 - TS - Tipos de unión]]: un array puede ser de unión, por ejemplo `(number | string)[]`.

## Preguntas de examen

- ¿Qué dos sintaxis existen para tipar un array en TypeScript?
- ¿Qué error detecta TS si haces `numeros.push("hola")`?
- ¿Cómo tiparías una lista de strings?

## Errores comunes

- Confundir `number[] | string` con `(number | string)[]` (no significan lo mismo).
- Declarar arrays como `any[]` y perder chequeo.

## Mini-ejemplo (mental)

Un array tipado es como una fila donde solo dejan entrar gente con un tipo de credencial específico.
