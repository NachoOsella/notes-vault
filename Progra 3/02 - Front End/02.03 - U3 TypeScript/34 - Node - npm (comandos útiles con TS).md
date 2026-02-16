# Node - npm (comandos útiles con TS)

## Definición

Comandos típicos de npm/npx para inicializar un proyecto, instalar TypeScript y compilar con `tsc`.

## Explicación

- *Qué problema resuelve*
    Establece un flujo de trabajo repetible para construir y ejecutar proyectos TypeScript.

- *Cómo funciona por arriba*
    - `npm` administra paquetes y scripts
    - `npx` ejecuta binarios instalados localmente en `node_modules/.bin`
    - `tsc` compila TS a JS usando `tsconfig.json` si existe

- *Qué implica / qué permite*
    - No depender de instalaciones globales
    - Tener scripts consistentes para el equipo

## Comandos útiles (lista)

- Iniciar proyecto npm: `npm init -y`
- Instalar TypeScript (local): `npm install typescript --save-dev`
- Inicializar tsconfig: `npx tsc --init`
- Compilar proyecto: `npx tsc`
- Compilación continua: `npx tsc -w`
- Ejecutar un script: `npm run <nombre>`
- Instalar dependencia de producción: `npm install <paquete>`
- Instalar dependencia de desarrollo: `npm install <paquete> --save-dev`

## Palabras clave

- `npm`
- `npx`
- `tsc`
- `-w` (watch)
- Scripts

## Comparaciones típicas

- vs [[30 - TS - tsconfig.json]]: `npx tsc` usa las opciones de `tsconfig`.
- vs [[33 - Node - package.json (por qué importa)]]: los scripts se definen en `package.json` y se corren con `npm run`.

## Preguntas de examen

- ¿Qué hace `npm init -y`?
- ¿Cuál es la diferencia entre `npm` y `npx`?
- ¿Qué comando crea un `tsconfig.json` base?
- ¿Cómo se compila en modo watch?

## Errores comunes

- Correr `tsc` global sin fijar versión por proyecto.
- No usar scripts y ejecutar comandos distintos en cada máquina.

## Mini-ejemplo (mental)

`npm` es la caja de herramientas del proyecto; `npx` es la forma de usar herramientas locales sin instalarlas globalmente.
