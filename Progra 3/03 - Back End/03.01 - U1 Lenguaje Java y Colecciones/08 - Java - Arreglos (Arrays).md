# Java - Arreglos (Arrays)

## Definición

Un arreglo es una estructura que guarda elementos del mismo tipo en posiciones indexadas y con tamaño fijo.

## Explicación

- *Qué problema resuelve*
    Permite agrupar muchos valores relacionados bajo un solo nombre.

- *Cómo funciona por arriba*
    - Se accede por índice (`0` a `length - 1`)
    - El tamaño se define al crearlo
    - Puede ser de una o más dimensiones

- *Qué implica / qué permite*
    - Acceso rápido por índice
    - Recorrido simple con bucles
    - Menos flexibilidad que una colección dinámica

## Visualización simple

```mermaid
%%{init: {'theme': 'base', 'themeVariables': { 'darkMode': true, 'background': '#1d2021', 'primaryColor': '#3c3836', 'primaryTextColor': '#ffffff', 'primaryBorderColor': '#bdae93', 'secondaryColor': '#504945', 'secondaryTextColor': '#ffffff', 'secondaryBorderColor': '#bdae93', 'tertiaryColor': '#282828', 'tertiaryTextColor': '#ffffff', 'tertiaryBorderColor': '#a89984', 'lineColor': '#d5c4a1', 'textColor': '#ffffff', 'mainBkg': '#282828', 'nodeBkg': '#3c3836', 'nodeTextColor': '#ffffff', 'nodeBorder': '#bdae93', 'clusterBkg': '#282828', 'clusterBorder': '#a89984', 'defaultLinkColor': '#d5c4a1', 'titleColor': '#ffffff', 'edgeLabelBackground': '#282828', 'labelBoxBkgColor': '#3c3836', 'labelBoxBorderColor': '#bdae93', 'labelTextColor': '#ffffff', 'loopTextColor': '#ffffff', 'noteBkgColor': '#282828', 'noteTextColor': '#ffffff', 'noteBorderColor': '#83a598', 'actorBkg': '#3c3836', 'actorBorder': '#bdae93', 'actorTextColor': '#ffffff', 'actorLineColor': '#d5c4a1', 'signalColor': '#d5c4a1', 'signalTextColor': '#ffffff', 'activationBkgColor': '#689d6a', 'activationBorderColor': '#8ec07c', 'sequenceNumberColor': '#ffffff'}, 'themeCSS': 'text, tspan { fill: #ffffff !important; color: #ffffff !important; } .messageText, .labelText, .loopText, .noteText, .actor text, .taskText, .sectionTitle text, .nodeLabel, .edgeLabel, .cluster-label text { fill: #ffffff !important; color: #ffffff !important; } .messageLine0, .messageLine1, .actor-line, .edgePath .path { stroke: #d5c4a1 !important; } .note { fill: #282828 !important; stroke: #83a598 !important; } .labelBox, .edgeLabel rect { fill: #3c3836 !important; stroke: #bdae93 !important; }'}}%%
graph LR
    A[0] --> B[10]
    C[1] --> D[20]
    E[2] --> F[30]
```

## Arreglos vs colecciones

| Aspecto | Arreglo | ArrayList |
|---|---|---|
| Tamaño | Fijo | Dinámico |
| Acceso por índice | Sí | Sí |
| Flexibilidad | Baja | Alta |

## Palabras clave

- Array
- Índice
- `length`
- Tamaño fijo
- Multidimensional

## Comparaciones típicas

- vs [[09 - Colecciones - Introducción]]: arreglo prioriza simplicidad y tamaño fijo
- vs [[10 - Colecciones - Listas (List)]]: `ArrayList` crece y ofrece más operaciones

## Preguntas de examen

- ¿Cuál es la limitación principal de un array?
- ¿Cuál es el primer índice?
- ¿Qué diferencia clave hay con `ArrayList`?

## Errores comunes

- Acceder fuera de rango (`ArrayIndexOutOfBoundsException`)
- Confundir `length` con `size()`
- Creer que puede crecer automáticamente

## Mini-ejemplo (mental)

Es una fila de casilleros numerados: podés leer rápido por número, pero no agregar casilleros nuevos sin crear otra fila.
