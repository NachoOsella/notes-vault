# TS - tsconfig.json

## Definición

`tsconfig.json` es el archivo de configuración que le dice a TypeScript **cómo compilar** un proyecto: opciones del compilador, qué incluir/excluir y cómo emitir la salida.

## Explicación

- *Qué problema resuelve*
    Evita repetir flags en la línea de comandos y hace el build reproducible para todo el equipo.

- *Cómo funciona por arriba*
    - Se ubica en la raíz del proyecto TS
    - `tsc` lo detecta y aplica sus opciones por defecto
    - Muchas herramientas (IDEs, bundlers) lo leen automáticamente

- *Qué implica / qué permite*
    - Configuración centralizada
    - Misma compilación para todos
    - Checks estrictos para reducir errores

## Opciones comunes (idea)

Todas viven en `compilerOptions`:

- `target`: versión de JS de salida (ES5, ES2015, ESNext, etc.)
- `module`: sistema de módulos (commonjs, esnext, etc.)
- `strict`: habilita checks estrictos (incluye `noImplicitAny`, `strictNullChecks`, etc.)
- `noImplicitAny`: error si algo queda con `any` implícito
- `outDir`: carpeta de salida (`./dist`, por ejemplo)
- `rootDir`: carpeta raíz del código fuente
- `sourceMap`: genera `.map` para depurar TS en vez de JS emitido
- `noEmitOnError`: no emite `.js` si hay errores
- `experimentalDecorators`: habilita decoradores. Ver: [[29 - TS - Decoradores]]

## Ejemplo mínimo

```json
{
  "compilerOptions": {
    "target": "ES2017",
    "module": "commonjs",
    "strict": true,
    "outDir": "./dist",
    "rootDir": "./src",
    "noEmitOnError": true
  },
  "include": ["src/**/*.ts"],
  "exclude": ["node_modules"]
}
```

## Inicialización rápida

- Crear un `tsconfig` base: `npx tsc --init`

## Palabras clave

- `tsconfig.json`
- `compilerOptions`
- `strict`
- `outDir`
- `target`
- `module`

## Comparaciones típicas

- vs [[34 - Node - npm (comandos útiles con TS)]]: `npx tsc --init` y `npx tsc` se apoyan en `tsconfig`.
- vs [[33 - Node - package.json (por qué importa)]]: `package.json` documenta scripts; `tsconfig` documenta compilación.

## Preguntas de examen

- ¿Para qué sirve `tsconfig.json`?
- ¿Qué hace la opción `strict`?
- ¿Para qué se usa `outDir`?
- ¿Qué diferencia hay entre `target` y `module`?
- ¿Qué opción evita emitir JS si hay errores?

## Errores comunes

- No compartir el `tsconfig` en el repo y compilar cada uno con flags distintos.
- Activar opciones sin entender impacto (por ejemplo, `strict`) y luego “apagar” con `any`.

## Mini-ejemplo (mental)

`tsconfig.json` es la receta del compilador: si todos usan la misma receta, todos obtienen el mismo resultado.
