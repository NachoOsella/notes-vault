# Angular - Nuevas directivas (@if, @for, @switch)

## Definición

Las nuevas directivas de control de flujo (`@if`, `@else`, `@for`, `@switch`, `@case`, `@default`) modernizan la sintaxis de templates en Angular y mejoran su legibilidad.

## Explicación

- *Qué problema resuelve*
    Reduce verbosidad y dispersión de lógica condicional/iterativa en templates.

- *Cómo funciona por arriba*
    Expresan condiciones, loops y selección múltiple con un estilo más cercano a estructuras de control del lenguaje.

- *Qué implica / qué permite*
    Templates más claros y mantenibles, especialmente en bloques con condiciones anidadas.

## Reglas clave

- `@if (...) { ... } @else { ... }`
- `@for (item of items; track item.id) { ... }`
- `@switch (valor) { @case (...) { ... } @default { ... } }`

## Palabras clave

- Control flow
- `@if`
- `@for`
- `@switch`
- Legibilidad

## Comparaciones típicas

- vs [[13 - Angular - Directivas]]: estas directivas reemplazan/modernizan casos típicos de `*ngIf`, `*ngFor`, `*ngSwitch`.
- vs `ng-template`: muchas ramas simples pueden resolverse inline sin bloques externos.

## Preguntas de examen

- ¿Qué ventaja de mantenimiento aportan `@if` y `@for` frente a la sintaxis clásica?
- ¿Qué rol cumple `@default` en `@switch`?

## Errores comunes

- Migrar sintaxis sin revisar comportamiento equivalente.
- Omitir estrategias de tracking en listas y perder rendimiento.

## Mini-ejemplo (mental)

Es como escribir control de flujo “de programación” directamente en el template, pero orientado a renderizado.
