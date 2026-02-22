# Java - Estructuras de control

## Definición

Las estructuras de control deciden cómo avanza el programa: por condición, por repetición o por salto.

## Explicación

- *Qué problema resuelve*
    Permiten tomar decisiones y repetir tareas en lugar de ejecutar todo en línea recta.

- *Cómo funciona por arriba*
    - Condicionales: `if`, `switch`
    - Bucles: `for`, `while`, `do-while`, `for-each`
    - Saltos: `break`, `continue`, `return`

- *Qué implica / qué permite*
    - Lógica de negocio expresiva
    - Automatizar procesos repetitivos
    - Cortar o continuar flujo cuando hace falta

## Flujo condicional básico

```mermaid
%%{init: {'theme': 'base', 'themeVariables': { 'darkMode': true, 'background': '#1d2021', 'primaryColor': '#3c3836', 'primaryTextColor': '#ffffff', 'primaryBorderColor': '#bdae93', 'secondaryColor': '#504945', 'secondaryTextColor': '#ffffff', 'secondaryBorderColor': '#bdae93', 'tertiaryColor': '#282828', 'tertiaryTextColor': '#ffffff', 'tertiaryBorderColor': '#a89984', 'lineColor': '#d5c4a1', 'textColor': '#ffffff', 'mainBkg': '#282828', 'nodeBkg': '#3c3836', 'nodeTextColor': '#ffffff', 'nodeBorder': '#bdae93', 'clusterBkg': '#282828', 'clusterBorder': '#a89984', 'defaultLinkColor': '#d5c4a1', 'titleColor': '#ffffff', 'edgeLabelBackground': '#282828', 'labelBoxBkgColor': '#3c3836', 'labelBoxBorderColor': '#bdae93', 'labelTextColor': '#ffffff', 'loopTextColor': '#ffffff', 'noteBkgColor': '#282828', 'noteTextColor': '#ffffff', 'noteBorderColor': '#83a598', 'actorBkg': '#3c3836', 'actorBorder': '#bdae93', 'actorTextColor': '#ffffff', 'actorLineColor': '#d5c4a1', 'signalColor': '#d5c4a1', 'signalTextColor': '#ffffff', 'activationBkgColor': '#689d6a', 'activationBorderColor': '#8ec07c', 'sequenceNumberColor': '#ffffff'}, 'themeCSS': 'text, tspan { fill: #ffffff !important; color: #ffffff !important; } .messageText, .labelText, .loopText, .noteText, .actor text, .taskText, .sectionTitle text, .nodeLabel, .edgeLabel, .cluster-label text { fill: #ffffff !important; color: #ffffff !important; } .messageLine0, .messageLine1, .actor-line, .edgePath .path { stroke: #d5c4a1 !important; } .note { fill: #282828 !important; stroke: #83a598 !important; } .labelBox, .edgeLabel rect { fill: #3c3836 !important; stroke: #bdae93 !important; }'}}%%
flowchart TD
    A[Inicio] --> B{Condición}
    B -->|true| C[Ejecuta bloque A]
    B -->|false| D[Ejecuta bloque B]
```

## Regla rápida de elección

- `for`: cuando ya conocés cuántas iteraciones habrá
- `while`: cuando depende de una condición
- `do-while`: cuando debe ejecutarse al menos una vez
- `for-each`: para recorrer arrays/colecciones sin índice

## Palabras clave

- if
- switch
- for
- while
- do-while
- break / continue / return

## Comparaciones típicas

- vs [[06 - Java - Operadores]]: operadores construyen condiciones; estructuras ejecutan según esas condiciones
- vs otros lenguajes: Java exige condición booleana explícita

## Preguntas de examen

- ¿Diferencia entre `while` y `do-while`?
- ¿Para qué sirve `break` en un `switch`?
- ¿Cuándo conviene `for-each`?

## Errores comunes

- Olvidar `break` en `switch`
- Crear bucles infinitos por condición mal armada
- Error off-by-one al iterar

## Mini-ejemplo (mental)

Son como desvíos en una ruta: una condición te manda por un camino, un bucle te hace dar vueltas, y `break` es la salida.
