# TS - Export-Import de tipos

## Definición

En TypeScript podés exportar e importar **tipos** (interfaces, alias, etc.) para compartir definiciones durante compilación.

## Explicación

- *Qué problema resuelve*
    Permite mantener consistencia de tipos entre archivos y evitar duplicación de modelos.

- *Cómo funciona por arriba*
    - Se exportan tipos como cualquier export
    - Al compilar a JS, esas importaciones/exportaciones de tipos no generan código (no existen en runtime)

- *Qué implica / qué permite*
    - Modelos compartidos en todo el proyecto
    - Mejor organización: tipos cerca de la lógica relacionada

## Ejemplos comunes

```ts
// modelos.ts
export interface Usuario {
  id: number;
  nombre: string;
}

// app.ts
import type { Usuario } from "./modelos";
```

## Palabras clave

- `import type`
- Interfaces
- Alias
- Compile-time
- Runtime

## Comparaciones típicas

- vs [[25 - TS - Export]]: export de valores sí existe en runtime; export de tipos se elimina al compilar.
- vs [[14 - TS - Interfaces]]: interfaces son típicamente exportadas/importadas.

## Preguntas de examen

- ¿Por qué los tipos no existen en tiempo de ejecución?
- ¿Qué ventaja tiene compartir tipos entre módulos?
- ¿Qué hace `import type`?

## Errores comunes

- Pensar que un tipo importado se puede “loggear” o usar en runtime.
- Duplicar definiciones de tipos en múltiples archivos y desincronizarlas.

## Mini-ejemplo (mental)

Exportar/importar tipos es compartir “planos” (definiciones) entre archivos, aunque el edificio final (JS) no los incluya.
