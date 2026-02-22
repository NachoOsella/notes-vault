# Big-O - Notación

## Definición
Big-O describe el límite superior del crecimiento del costo de un algoritmo cuando n es grande.

## Explicación

- *Qué problema resuelve*
    Es una herramienta matemática para expresar la tasa de crecimiento, es decir, cuánto crece el tiempo de ejecución de un algoritmo a medida que crece el tamaño de la entrada n
- *Cómo funciona por arriba*
    - Se enfoca en el comportamiento del algoritmo cuando n tiende a ser muy grande (caso asintótico, cuando el tamaño tiende al infinito)
    - Indica el límite superior, es decir, una estimación del peor crecimiento posible del algoritmo, ignorando constantes y términos de menor orden
    - No nos dice exactamente cuánto tarda un algoritmo, sino cómo escala
    - **Ejemplo**: si un algoritmo es O(n), duplicar la entrada duplica el tiempo; si es O(n²), duplicar la entrada puede cuadruplicar el tiempo
    - **Jerarquía**: O(1) < O(log n) < O(n) < O(n log n) < O(n²) < O(2ⁿ), O(n!)
- *Qué implica / qué permite*
    Comparar algoritmos de forma objetiva; predecir comportamiento con entradas grandes; identificar qué algoritmos crecen de forma razonable vs cuáles se vuelven inviables rápidamente

## Diagrama (Mermaid)

```mermaid
%%{init: {'theme': 'base', 'themeVariables': { 'darkMode': true, 'background': '#1d2021', 'primaryColor': '#3c3836', 'primaryTextColor': '#ffffff', 'primaryBorderColor': '#bdae93', 'secondaryColor': '#504945', 'secondaryTextColor': '#ffffff', 'secondaryBorderColor': '#bdae93', 'tertiaryColor': '#282828', 'tertiaryTextColor': '#ffffff', 'tertiaryBorderColor': '#a89984', 'lineColor': '#d5c4a1', 'textColor': '#ffffff', 'mainBkg': '#282828', 'nodeBkg': '#3c3836', 'nodeTextColor': '#ffffff', 'nodeBorder': '#bdae93', 'clusterBkg': '#282828', 'clusterBorder': '#a89984', 'defaultLinkColor': '#d5c4a1', 'titleColor': '#ffffff', 'edgeLabelBackground': '#282828', 'labelBoxBkgColor': '#3c3836', 'labelBoxBorderColor': '#bdae93', 'labelTextColor': '#ffffff', 'loopTextColor': '#ffffff', 'noteBkgColor': '#282828', 'noteTextColor': '#ffffff', 'noteBorderColor': '#83a598', 'actorBkg': '#3c3836', 'actorBorder': '#bdae93', 'actorTextColor': '#ffffff', 'actorLineColor': '#d5c4a1', 'signalColor': '#d5c4a1', 'signalTextColor': '#ffffff', 'activationBkgColor': '#689d6a', 'activationBorderColor': '#8ec07c', 'sequenceNumberColor': '#ffffff'}, 'themeCSS': 'text, tspan { fill: #ffffff !important; color: #ffffff !important; } .messageText, .labelText, .loopText, .noteText, .actor text, .taskText, .sectionTitle text, .nodeLabel, .edgeLabel, .cluster-label text { fill: #ffffff !important; color: #ffffff !important; } .messageLine0, .messageLine1, .actor-line, .edgePath .path { stroke: #d5c4a1 !important; } .note { fill: #282828 !important; stroke: #83a598 !important; } .labelBox, .edgeLabel rect { fill: #3c3836 !important; stroke: #bdae93 !important; }'}}%%
graph LR
    A["O(1)"] --> B["O(log n)"]
    B --> C["O(n)"]
    C --> D["O(n log n)"]
    D --> E["O(n²)"]
    E --> F["O(2ⁿ)"]
    F --> G["O(n!)"]
```

## Comparaciones típicas
- vs [[09 - Complejidad - Cómo se mide]]: notación formal matemática vs conteo informal de operaciones
- vs [[10 - Complejidad - Temporal]]: notación abstracta vs aplicación específica a tiempo
- vs [[06 - Algoritmos - Clasificación por eficiencia esperada]]: herramienta de medición vs categorización cualitativa

## Palabras clave
- Big-O
- asintótico
- límite superior
- crecimiento
- escalabilidad

## Preguntas de examen
- ¿Qué información da Big-O y qué no da?
- ¿Por qué se ignoran constantes en Big-O?

## Errores comunes
- Interpretar Big-O como tiempo exacto en segundos.
- Comparar algoritmos solo por constantes y no por orden.

## Mini-ejemplo (mental)
- Dos autos arrancan distinto, pero en viajes largos importa más consumo por kilómetro que segundos de arranque.
