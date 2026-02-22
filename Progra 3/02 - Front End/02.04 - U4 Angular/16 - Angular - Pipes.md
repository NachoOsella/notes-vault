# Angular - Pipes

## Definición

Los pipes transforman valores en templates Angular para mostrarlos con un formato deseado sin mover esa lógica al componente.

## Explicación

- *Qué problema resuelve*
    Evita mezclar lógica de presentación con lógica de negocio en TypeScript.

- *Cómo funciona por arriba*
    Se aplica con `{{ valor | pipe }}` y opcionalmente parámetros (por ejemplo `number`, `date`, `currency`).

- *Qué implica / qué permite*
    Templates más legibles y consistentes para formato de texto, números y fechas.

## Pipes comunes

- `uppercase` / `lowercase`
- `date`
- `currency`
- `number` (decimal)
- `slice`

## Pipes personalizados

Se generan con `ng generate pipe nombre-del-pipe` para encapsular formatos de negocio repetidos.

## Palabras clave

- Transformación
- Formato
- `date`
- `currency`
- Pipe personalizado

## Comparaciones típicas

- vs [[13 - Angular - Directivas]]: pipe transforma datos; directiva altera estructura/comportamiento del DOM.
- vs lógica en componente: pipe evita duplicación de formateo en múltiples vistas.

## Preguntas de examen

- ¿Qué ventaja aporta usar `pipe` en vez de formatear todo en TS?
- ¿Qué parámetros recibe típicamente `number`/`decimal` pipe?

## Errores comunes

- Colocar lógica de negocio compleja dentro de pipes de presentación.
- Abusar de pipes costosos en listas grandes sin evaluar rendimiento.

## Mini-ejemplo (mental)

Un pipe es como un filtro visual: el dato base no cambia, cambia cómo lo mostrás.
