# Estrategias - Introducción

## Definición
Las estrategias de resolución son patrones para diseñar algoritmos según la estructura del problema.

## Explicación

- *Qué problema resuelve*
    Proporciona un marco conceptual para abordar diferentes tipos de problemas algorítmicos según sus características, permitiendo seleccionar el enfoque más adecuado
- *Cómo funciona por arriba*
    - No todos los problemas se resuelven igual; existen estrategias comunes que se aplican según la naturaleza del problema
    - Las estrategias son patrones de diseño algorítmico que los programadores usan todo el tiempo para resolver problemas reales
    - **Principales estrategias**:
        - Divide and Conquer: problemas que pueden dividirse recursivamente
        - Backtracking: problemas de exploración o combinatorios
        - Greedy: cuando se puede tomar decisiones óptimas locales
        - Programación Dinámica: cuando hay subproblemas repetidos con superposición
- *Qué implica / qué permite*
    Reconocer problemas similares y aplicar soluciones probadas; evitar reinventar la rueda; saber qué estrategia usar puede marcar la diferencia entre encontrar una solución rápidamente o quedarse atascado; identificarlas cuando aparezcan en problemas reales

## Diagrama (Mermaid)

```mermaid
%%{init: {'theme': 'base', 'themeVariables': { 'darkMode': true, 'background': '#1d2021', 'primaryColor': '#3c3836', 'primaryTextColor': '#ffffff', 'primaryBorderColor': '#bdae93', 'secondaryColor': '#504945', 'secondaryTextColor': '#ffffff', 'secondaryBorderColor': '#bdae93', 'tertiaryColor': '#282828', 'tertiaryTextColor': '#ffffff', 'tertiaryBorderColor': '#a89984', 'lineColor': '#d5c4a1', 'textColor': '#ffffff', 'mainBkg': '#282828', 'nodeBkg': '#3c3836', 'nodeTextColor': '#ffffff', 'nodeBorder': '#bdae93', 'clusterBkg': '#282828', 'clusterBorder': '#a89984', 'defaultLinkColor': '#d5c4a1', 'titleColor': '#ffffff', 'edgeLabelBackground': '#282828', 'labelBoxBkgColor': '#3c3836', 'labelBoxBorderColor': '#bdae93', 'labelTextColor': '#ffffff', 'loopTextColor': '#ffffff', 'noteBkgColor': '#282828', 'noteTextColor': '#ffffff', 'noteBorderColor': '#83a598', 'actorBkg': '#3c3836', 'actorBorder': '#bdae93', 'actorTextColor': '#ffffff', 'actorLineColor': '#d5c4a1', 'signalColor': '#d5c4a1', 'signalTextColor': '#ffffff', 'activationBkgColor': '#689d6a', 'activationBorderColor': '#8ec07c', 'sequenceNumberColor': '#ffffff'}, 'themeCSS': 'text, tspan { fill: #ffffff !important; color: #ffffff !important; } .messageText, .labelText, .loopText, .noteText, .actor text, .taskText, .sectionTitle text, .nodeLabel, .edgeLabel, .cluster-label text { fill: #ffffff !important; color: #ffffff !important; } .messageLine0, .messageLine1, .actor-line, .edgePath .path { stroke: #d5c4a1 !important; } .note { fill: #282828 !important; stroke: #83a598 !important; } .labelBox, .edgeLabel rect { fill: #3c3836 !important; stroke: #bdae93 !important; }'}}%%
flowchart TD
    A["Nuevo problema"] --> B{"¿Subproblemas independientes?"}
    B -- Sí --> C["Divide and Conquer"]
    B -- No --> D{"¿Subproblemas superpuestos?"}
    D -- Sí --> E["Programación Dinámica"]
    D -- No --> F{"¿Explorar opciones y deshacer?"}
    F -- Sí --> G["Backtracking"]
    F -- No --> H["Greedy (si hay criterio local válido)"]
```

## Comparaciones típicas
- vs [[03 - Algoritmos - Clasificación]]: estrategias de diseño algorítmico vs categorización general de algoritmos
- vs [[05 - Algoritmos - Clasificación por forma de operar]]: estrategias específicas de resolución vs clasificación amplia por mecanismo

## Palabras clave
- estrategia
- diseño algorítmico
- patrón
- selección de enfoque
- resolución de problemas

## Preguntas de examen
- ¿Por qué identificar el tipo de problema acelera el diseño de solución?
- ¿Qué señales orientan a Greedy, Backtracking o Programación Dinámica?

## Errores comunes
- Intentar resolver todo con una sola técnica conocida.
- Elegir estrategia sin validar precondiciones del problema.

## Mini-ejemplo (mental)
- Antes de construir, decidís si conviene martillo, destornillador o taladro; en algoritmos pasa igual.
