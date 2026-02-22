# Angular - Template Driven Forms

## Definición

Template Driven Forms es el enfoque de Angular para construir formularios definiendo gran parte de la lógica directamente en la plantilla HTML con directivas.

## Explicación

- *Qué problema resuelve*
    Permite crear formularios simples de forma rápida con menos código TypeScript.

- *Cómo funciona por arriba*
    Usa `ngForm` para el formulario, `ngModel` para binding de controles, `ngSubmit` para envío y validaciones HTML5/Angular.

- *Qué implica / qué permite*
    Desarrollo ágil en formularios básicos y feedback de estado (`valid`, `dirty`, `touched`) sin infraestructura compleja.

## Directivas y estados clave

- `ngForm`
- `ngModel`
- `ngSubmit`
- `ngModelGroup`
- Estados: `valid/invalid`, `pristine/dirty`, `touched/untouched`

## Palabras clave

- Formularios
- `ngForm`
- `ngModel`
- Validación
- `ngModelGroup`

## Comparaciones típicas

- vs Reactive Forms: template-driven prioriza simplicidad; reactive prioriza control fino y escalabilidad.
- vs [[08 - Angular - Data Binding]]: forms reutiliza two-way binding como base de captura de datos.

## Preguntas de examen

- ¿Qué rol cumple `name` en controles con `ngModel`?
- ¿Qué diferencia hay entre `dirty` y `touched`?
- ¿Para qué sirve `ngModelGroup`?

## Errores comunes

- Olvidar el atributo `name` en controles y romper el registro del formulario.
- Forzar template-driven en formularios complejos que piden validación avanzada.

## Mini-ejemplo (mental)

Es como diseñar un formulario “desde el HTML”, dejando que Angular conecte datos y estado automáticamente.
