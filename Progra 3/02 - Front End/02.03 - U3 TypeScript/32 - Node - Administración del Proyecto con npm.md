# Node - Administración del Proyecto con npm

## Definición

npm (Node Package Manager) es la herramienta estándar del ecosistema Node.js para **gestionar dependencias** y **ejecutar comandos/scripts** de un proyecto.

## Explicación

- *Qué problema resuelve*
    Centraliza qué paquetes usa un proyecto y cómo se construye/ejecuta, evitando el “a mí me funciona” por diferencias de entorno.

- *Cómo funciona por arriba*
    - Inicializas un proyecto con `package.json`
    - Instalás dependencias (producción) y devDependencies (desarrollo)
    - Definís scripts (`build`, `start`, `test`) para correr tareas

- *Qué implica / qué permite*
    - Instalar TypeScript local al proyecto
    - Compilar TS con `npx tsc` o `npm run build`
    - Reproducibilidad mediante `package-lock.json`

## Ejemplos comunes

- Inicializar proyecto: `npm init -y`
- Instalar TS para desarrollo: `npm install typescript --save-dev`
- Compilar según `tsconfig.json`: `npx tsc`

## Palabras clave

- npm
- Dependencias
- `devDependencies`
- Scripts
- `package-lock.json`
- Reproducibilidad

## Comparaciones típicas

- vs [[33 - Node - package.json (por qué importa)]]: `package.json` es el archivo central que npm lee.
- vs [[34 - Node - npm (comandos útiles con TS)]]: esa nota lista comandos típicos del flujo de trabajo.
- vs [[30 - TS - tsconfig.json]]: `tsconfig` y `package.json` juntos documentan cómo compilar/ejecutar.

## Preguntas de examen

- ¿Qué es npm y para qué se usa en un proyecto TS?
- ¿Cuál es la diferencia entre `dependencies` y `devDependencies`?
- ¿Para qué sirven los `scripts` en `package.json`?
- ¿Qué problema resuelve `package-lock.json`?

## Errores comunes

- Instalar herramientas globalmente y no declararlas en `devDependencies`.
- No versionar el lockfile (cuando el equipo lo necesita para reproducibilidad).

## Mini-ejemplo (mental)

npm es como una lista de compras y recetas: define qué ingredientes (paquetes) necesitás y cómo cocinar (scripts) para que cualquiera lo replique.

