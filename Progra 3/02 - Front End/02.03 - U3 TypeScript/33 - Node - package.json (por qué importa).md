# Node - package.json (por qué importa)

## Definición

`package.json` es el archivo central de un proyecto npm: describe el proyecto, sus dependencias y los scripts para construir/ejecutar.

## Explicación

- *Qué problema resuelve*
    Documenta cómo instalar, compilar y correr el proyecto, y qué paquetes necesita para funcionar.

- *Cómo funciona por arriba*
    - Contiene metadatos (nombre, versión, etc.)
    - Declara `dependencies` y `devDependencies`
    - Define `scripts` ejecutables con `npm run ...`

- *Qué implica / qué permite*
    - Reproducir el entorno con `npm install`
    - Estandarizar comandos (`build`, `start`, `test`)
    - Colaboración más simple

## Campos típicos (repaso)

- `name`: nombre del proyecto/paquete
- `version`: versión (SemVer)
- `scripts`: comandos (por ejemplo `"build": "tsc"`)
- `dependencies`: paquetes requeridos en producción
- `devDependencies`: paquetes necesarios solo en desarrollo (por ejemplo `typescript`)
- `main`: punto de entrada del paquete/app (en proyectos Node)
- `license`: licencia

## Palabras clave

- npm
- `package.json`
- `dependencies`
- `devDependencies`
- `scripts`
- SemVer

## Comparaciones típicas

- vs [[32 - Node - Administración del Proyecto con npm]]: npm es la herramienta; `package.json` es el contrato del proyecto.
- vs [[30 - TS - tsconfig.json]]: `package.json` define scripts; `tsconfig` define cómo compila TS.

## Preguntas de examen

- ¿Qué información guarda `package.json`?
- ¿Cuál es la diferencia entre `dependencies` y `devDependencies`?
- ¿Cómo se ejecuta un script definido en `scripts`?
- ¿Para qué sirve `main`?

## Errores comunes

- No definir scripts y depender de comandos “de memoria”.
- Instalar dependencias de producción como dev (o al revés) y confundir el despliegue.

## Mini-ejemplo (mental)

`package.json` es el “contrato” del proyecto: dice qué necesita y cómo se usa.
