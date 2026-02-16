# TS - Variantes de import

## Definición

TypeScript (como JavaScript moderno) permite distintas formas de `import` según el tipo de exportación (named, default, namespace).

## Explicación

- *Qué problema resuelve*
    Adapta la importación a la forma en que el módulo expone su API.

- *Cómo funciona por arriba*
    - Named: `import { a, b } from "...";`
    - Default: `import x from "...";`
    - Namespace: `import * as mod from "...";`
    - Renombre: `import { a as alias } from "...";`

- *Qué implica / qué permite*
    - Claridad en el origen y uso de cada símbolo
    - Evitar conflictos de nombres con alias

## Ejemplos comunes

```ts
import * as utils from "./utils";
import { parsear as parse } from "./parser";
```

## Palabras clave

- Named import
- Default import
- Namespace import
- Alias (`as`)

## Comparaciones típicas

- vs [[25 - TS - Export]]: la forma del import depende de cómo se exportó.
- vs [[28 - TS - Export-Import de tipos]]: los tipos se pueden importar de forma especial para no emitir JS.

## Preguntas de examen

- ¿Qué diferencia hay entre `import { x }` e `import x`?
- ¿Para qué sirve `import * as M`?
- ¿Cómo renombrás un import para evitar conflicto?

## Errores comunes

- Usar default import cuando el módulo no tiene export default.
- Importar muchas cosas y terminar con archivos difíciles de leer (conviene agrupar/ordenar).

## Mini-ejemplo (mental)

Es como retirar herramientas: a veces pedís una herramienta específica, a veces te traés toda la caja (namespace).
