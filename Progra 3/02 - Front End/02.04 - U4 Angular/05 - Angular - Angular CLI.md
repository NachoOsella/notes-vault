# Angular - Angular CLI

## Definición

Angular CLI (Command Line Interface) es la herramienta oficial de línea de comandos para crear, desarrollar y mantener proyectos Angular.

## Explicación

- *Qué problema resuelve*
    Automatiza tareas repetitivas (crear proyecto, componentes, servicios, build y serve) y reduce errores de configuración.

- *Cómo funciona por arriba*
    Se instala con npm y expone comandos `ng` como `ng new`, `ng generate`, `ng serve` y `ng build`.

- *Qué implica / qué permite*
    Estandariza la estructura del proyecto y acelera el flujo de trabajo del equipo.

## Comandos base

- `npm install -g @angular/cli`
- `ng new nombre-del-proyecto`
- `ng serve`
- `ng g c nombre-componente`
- `ng g s nombre-servicio`

## Palabras clave

- CLI
- `ng`
- `angular.json`
- `package.json`
- Automatización

## Comparaciones típicas

- vs crear estructura manual: CLI evita boilerplate y asegura convenciones.
- vs [[03 - Angular - Introducción]]: Angular define arquitectura; CLI facilita operarla.

## Preguntas de examen

- ¿Qué diferencia hay entre `ng new` y `ng serve`?
- ¿Por qué Angular CLI mejora mantenibilidad en equipos?

## Errores comunes

- Instalar versiones incompatibles de Node/CLI.
- Modificar archivos base sin entender su impacto (`angular.json`, configs).

## Mini-ejemplo (mental)

CLI es como una navaja suiza para Angular: un mismo comando dispara tareas complejas con una sintaxis simple.
