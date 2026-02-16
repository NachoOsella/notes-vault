# TS - Comparación entre JavaScript y TypeScript

## Definición

JavaScript (JS) es el lenguaje de ejecución en web/Node. TypeScript (TS) agrega **tipos y chequeos** durante desarrollo y luego se **transpila a JS**.

## Explicación

- *Qué problema resuelve*
    Aporta seguridad y escalabilidad en proyectos grandes, detectando errores de tipos temprano y mejorando el tooling del IDE.

- *Cómo funciona por arriba*
    - Escribes TS con tipos opcionales
    - `tsc` verifica consistencia de tipos
    - `tsc` emite JS para ejecución

- *Qué implica / qué permite*
    - Detectar errores antes de ejecutar
    - Mejor autocompletado y refactors más seguros
    - Paso extra de compilación (más configuración)

## Diferencias clave (resumen)

| Aspecto | JavaScript (JS) | TypeScript (TS) |
|---|---|---|
| Tipado | Dinámico (runtime) | Estático opcional (compile-time) |
| Errores | Aparecen al ejecutar | Muchos se detectan al compilar |
| Ejecución | Corre directo | Debe transpilarse a JS |
| Sintaxis extra | ECMAScript estándar | Tipos, interfaces, enums, decoradores, etc. |
| Flujo de trabajo | Sin build obligatorio | Build/transpile integrado a herramientas |

## Palabras clave

- Dinámico vs estático
- Compile-time vs runtime
- Transpilar
- Tooling / IDE
- `.d.ts` (definiciones de tipos)

## Comparaciones típicas

- vs [[03 - TS - Introducción a TypeScript]]: la introducción explica el “por qué”; esta nota resume el “en qué cambia”.
- vs [[30 - TS - tsconfig.json]]: TS normalmente se usa con configuración reproducible en tsconfig.

## Preguntas de examen

- ¿Cuál es la diferencia entre tipado dinámico y tipado estático?
- ¿Qué se ejecuta finalmente: TypeScript o JavaScript?
- ¿Qué tipo de errores detecta TS antes de ejecución?
- ¿Qué costo agrega TS al flujo de trabajo?
- ¿Se puede migrar un proyecto JS a TS de forma gradual?

## Errores comunes

- Creer que TS “reemplaza” a JS: en ejecución sigue siendo JS.
- Confundir “tener tipos” con “no tener bugs”: TS no valida lógica de negocio.

## Mini-ejemplo (mental)

JS es conducir sin tablero de alertas. TS es tener alertas y diagnósticos antes de salir a la ruta: no impide todos los problemas, pero evita muchos.

