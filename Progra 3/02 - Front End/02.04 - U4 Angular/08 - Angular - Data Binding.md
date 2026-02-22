# Angular - Data Binding

## Definición

Data binding es el mecanismo que sincroniza datos entre el componente y la plantilla en Angular.

## Explicación

- *Qué problema resuelve*
    Evita manipular manualmente el DOM para mantener datos y vista en sincronía.

- *Cómo funciona por arriba*
    Angular ofrece one-way binding (componente -> vista) y two-way binding (componente <-> vista).

- *Qué implica / qué permite*
    Interfaces reactivas con menos código imperativo y menor riesgo de inconsistencias.

## Tipos principales

- Interpolación: `{{ valor }}`
- Property binding: `[src]="imageUrl"`
- Event binding: `(input)="onChange($event)"`
- Two-way binding: `[(ngModel)]="propiedad"`

## Palabras clave

- One-way
- Two-way
- Interpolación
- `ngModel`
- Sincronización

## Comparaciones típicas

- vs [[17 - Angular - Template Driven Forms]]: forms usa binding para capturar/validar datos de usuario.
- vs [[15 - Angular - Comunicación entre componentes]]: binding actúa dentro de template; comunicación padre-hijo cruza componentes.

## Preguntas de examen

- ¿Qué diferencia hay entre interpolación y property binding?
- ¿Por qué `ngModel` se asocia al two-way binding?

## Errores comunes

- Intentar two-way binding sin importar el módulo/formato necesario.
- Abusar de lógica compleja directamente en expresiones del template.

## Mini-ejemplo (mental)

Binding es como un espejo inteligente: cuando cambia el dato, cambia la vista; y con two-way también al revés.
