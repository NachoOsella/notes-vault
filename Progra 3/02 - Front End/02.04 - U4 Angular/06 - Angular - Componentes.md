# Angular - Componentes

## Definición

Un componente es la unidad básica de UI en Angular: encapsula plantilla (HTML), lógica (TypeScript) y estilos en una pieza reutilizable.

## Explicación

- *Qué problema resuelve*
    Permite dividir la interfaz en bloques pequeños y mantenibles, evitando vistas monolíticas.

- *Cómo funciona por arriba*
    Cada componente tiene un selector y Angular lo renderiza en templates según su declaración/importación.

- *Qué implica / qué permite*
    Favorece reutilización, encapsulamiento y mantenimiento por partes de la aplicación.

## Estructura típica

- `nombre.component.ts`
- `nombre.component.html`
- `nombre.component.css`
- `nombre.component.spec.ts`

## Palabras clave

- Selector
- Plantilla
- Encapsulamiento
- Reutilización
- UI modular

## Comparaciones típicas

- vs [[07 - Angular - Standalone Components]]: standalone elimina dependencia obligatoria de módulos para declarar el componente.
- vs [[09 - Angular - Servicios]]: componente maneja vista/interacción; servicio centraliza lógica compartida.

## Preguntas de examen

- ¿Qué partes conforman un componente Angular?
- ¿Qué ventajas aporta dividir la app en componentes?

## Errores comunes

- Colocar lógica de negocio pesada dentro del componente.
- Duplicar componentes casi iguales en lugar de parametrizar.

## Mini-ejemplo (mental)

Un componente es como una pieza LEGO: tiene forma propia y se combina con otras para armar toda la app.
