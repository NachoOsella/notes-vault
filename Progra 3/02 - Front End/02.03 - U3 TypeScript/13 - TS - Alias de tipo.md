# TS - Alias de tipo

## Definición

Un alias de tipo (`type`) permite crear un nombre para un tipo existente (primitivo, unión u objeto complejo).

## Explicación

- *Qué problema resuelve*
    Mejora la legibilidad y reutilización: evita repetir tipos largos o complejos.

- *Cómo funciona por arriba*
    - Se declara con `type Nombre = ...`
    - Luego se usa como cualquier otro tipo

- *Qué implica / qué permite*
    - Nombres más semánticos (ej: `Identificador`)
    - Composición de tipos (uniones, objetos)

## Ejemplos comunes

```ts
type Identificador = number | string;

type Punto = {
  x: number;
  y: number;
};
```

## Palabras clave

- `type`
- Alias
- Reutilización
- Legibilidad

## Comparaciones típicas

- vs [[14 - TS - Interfaces]]: interfaces son otra forma de describir objetos; los alias pueden cubrir más casos (uniones, primitivos).
- vs [[12 - TS - Tipos de unión]]: un alias puede nombrar una unión para usarla en todo el proyecto.

## Preguntas de examen

- ¿Para qué sirve `type` en TypeScript?
- ¿Podés crear un alias para una unión?
- ¿Qué ventaja aporta un alias de tipo en un proyecto grande?

## Errores comunes

- Usar alias e interfaces sin criterio; conviene saber cuándo usar cada uno. Ver: [[15 - TS - Alias vs Interfaces]]

## Mini-ejemplo (mental)

Un alias es como ponerle un apodo a una definición larga para no repetirla siempre.
