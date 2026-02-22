# Angular - Directivas

## Definición

Las directivas son instrucciones en templates que modifican estructura, comportamiento o estilos de elementos HTML en Angular.

## Explicación

- *Qué problema resuelve*
    Permite aplicar lógica declarativa al DOM sin manipulación manual directa.

- *Cómo funciona por arriba*
    Se clasifican en estructurales (`ngIf`, `ngFor`, `ngSwitch`), de atributo (`ngClass`, `ngStyle`) y personalizadas.

- *Qué implica / qué permite*
    Hace templates más expresivos y reutilizables, con reglas de renderizado claras.

## Otras directivas útiles

- `ng-content` (proyección de contenido)
- `ng-template` (bloques de template reutilizables/condicionales)
- `ng-container` (agrupar sin nodo extra en DOM)

## Palabras clave

- Estructural
- Atributo
- `ngIf`
- `ngFor`
- `ngClass`

## Comparaciones típicas

- vs [[14 - Angular - Nuevas directivas (@if, @for, @switch)]]: Angular moderno ofrece sintaxis más legible para condicionales/iteración.
- vs [[16 - Angular - Pipes]]: directiva controla render/comportamiento; pipe transforma datos mostrados.

## Preguntas de examen

- ¿Qué diferencia hay entre directiva estructural y de atributo?
- ¿Para qué se usa `ng-container`?

## Errores comunes

- Usar directivas complejas cuando conviene mover lógica al componente.
- Generar DOM innecesario por no usar `ng-container` donde corresponde.

## Mini-ejemplo (mental)

Una directiva es como una regla adherida al HTML que le dice al elemento cómo comportarse.
