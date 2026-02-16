# TS - enum

## Definición

Un `enum` (enumeración) define un conjunto de constantes con nombre para representar opciones finitas (por ejemplo, estados o roles).

## Explicación

- *Qué problema resuelve*
    Evita “strings mágicos” repetidos y reduce errores por typos al usar valores constantes.

- *Cómo funciona por arriba*
    - Se declara con `enum Nombre { ... }`
    - Se usa como un tipo y como un conjunto de valores

- *Qué implica / qué permite*
    - Código más expresivo: `Estado.Activo` en vez de `"activo"`
    - Menos inconsistencias en valores repetidos

## Ejemplos comunes

```ts
enum Estado {
  Activo,
  Inactivo,
}

let e: Estado = Estado.Activo;
```

## Palabras clave

- `enum`
- Constantes
- Opciones finitas

## Comparaciones típicas

- vs [[13 - TS - Alias de tipo]]: a veces un alias de unión de strings puede reemplazar un enum (según estilo).
- vs [[31 - TS - Comparación entre JavaScript y TypeScript]]: `enum` es una de las “sintaxis extra” de TS.

## Preguntas de examen

- ¿Para qué sirve un `enum`?
- ¿Qué ventaja tiene frente a usar strings sueltos?
- ¿Cómo se declara y se usa un enum?

## Errores comunes

- Usar enums para todo cuando bastan constantes simples.
- No mantener consistencia entre frontend/backend (si comparten estados/roles).

## Mini-ejemplo (mental)

Un enum es como un menú con opciones fijas: en vez de escribir lo que querés “a mano”, elegís una opción válida.
