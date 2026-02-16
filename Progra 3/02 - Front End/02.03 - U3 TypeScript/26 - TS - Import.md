# TS - Import

## Definición

`import` trae funciones, variables, clases o tipos exportados desde otro módulo.

## Explicación

- *Qué problema resuelve*
    Permite reutilizar código y mantener archivos pequeños con responsabilidades claras.

- *Cómo funciona por arriba*
    - Import nombrado: `import { a } from "./mod";`
    - Import default: `import X from "./mod";`
    - Import namespace: `import * as M from "./mod";`

- *Qué implica / qué permite*
    - Dependencias explícitas
    - Mejor organización de proyecto

## Ejemplos comunes

```ts
import { suma } from "./math";

console.log(suma(2, 3));
```

## Palabras clave

- `import`
- Dependencias
- Módulos

## Comparaciones típicas

- vs [[25 - TS - Export]]: import consume lo que otro archivo exporta.
- vs [[27 - TS - Variantes de import]]: hay varias sintaxis según lo exportado.

## Preguntas de examen

- ¿Cómo importás una exportación nombrada?
- ¿Cómo importás una exportación default?
- ¿Qué ventaja aporta modularizar con imports/exports?

## Errores comunes

- Importar por defecto algo que fue exportado como nombrado (o al revés).
- Tener imports circulares por mala organización.

## Mini-ejemplo (mental)

Importar es “traer una herramienta” de otra caja (módulo) para usarla acá.
