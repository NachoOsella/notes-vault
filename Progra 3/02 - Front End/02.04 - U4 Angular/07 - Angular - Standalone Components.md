# Angular - Standalone Components

## Definición

Los Standalone Components (Angular 17+) son componentes autónomos que no requieren estar declarados en un `NgModule` para funcionar.

## Explicación

- *Qué problema resuelve*
    Reduce boilerplate de módulos y simplifica arquitectura y lazy loading.

- *Cómo funciona por arriba*
    Se generan con `--standalone`, declaran `standalone: true` e importan directamente sus dependencias.

- *Qué implica / qué permite*
    Código más limpio, migración progresiva y rutas más simples en aplicaciones nuevas.

## Ventajas clave

- Menos configuración
- Mejor legibilidad
- Lazy loading más directo
- Reuso más simple de componentes

## Palabras clave

- `standalone: true`
- Angular 17+
- Lazy loading
- Migración gradual

## Comparaciones típicas

- vs [[06 - Angular - Componentes]]: el modelo tradicional depende de módulos para declaración.
- vs [[05 - Angular - Angular CLI]]: CLI provee el flag `--standalone`, pero no define el concepto.

## Preguntas de examen

- ¿Qué problema de arquitectura atacan los standalone?
- ¿Cuándo conviene usarlos en proyectos existentes?

## Errores comunes

- Mezclar imports/dependencias sin revisar alcance del componente.
- Creer que migrar a standalone obliga a reescribir toda la app de una vez.

## Mini-ejemplo (mental)

Standalone es como pasar de necesitar una “carpeta contenedora” para todo, a usar archivos autocontenidos listos para enchufar.
