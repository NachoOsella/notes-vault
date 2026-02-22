# Búsqueda - Binaria

## Definición
La búsqueda binaria encuentra un valor en datos ordenados descartando la mitad del espacio en cada paso.

## Explicación

- *Qué problema resuelve*
    Localizar elementos de forma extremadamente eficiente en colecciones ordenadas, reduciendo drásticamente el tiempo respecto a la búsqueda lineal
- *Cómo funciona por arriba*
    - **Requisito importante**: el arreglo debe estar ordenado previamente
    - Reduce el espacio de búsqueda a la mitad en cada paso:
        1. Se toma el índice del medio del arreglo
        2. Se compara ese valor con el buscado
        3. Si es igual, se encontró
        4. Si el valor buscado es menor, se repite en la mitad izquierda
        5. Si es mayor, se repite en la mitad derecha
    - **Ejemplo**: Buscar 13 en lista ordenada [1..20]: Paso 1: mitad=10(valor 11), 13>11 → buscar en [11-20]; Paso 2: mitad=15(valor 16), 13<16 → buscar en [11-15]; Paso 3: mitad=13(valor 14), 13<14 → buscar en [11-13]; Paso 4: encuentra 13
- *Qué implica / qué permite*
    - Cada paso descarta la mitad de los elementos
    - Muy rápido incluso con listas grandes
    - Complejidad O(log n): para n=1.000.000 solo ~20 comparaciones

## Diagrama (Mermaid)

```mermaid
%%{init: {'theme': 'base', 'themeVariables': { 'darkMode': true, 'background': '#1d2021', 'primaryColor': '#3c3836', 'primaryTextColor': '#ffffff', 'primaryBorderColor': '#bdae93', 'secondaryColor': '#504945', 'secondaryTextColor': '#ffffff', 'secondaryBorderColor': '#bdae93', 'tertiaryColor': '#282828', 'tertiaryTextColor': '#ffffff', 'tertiaryBorderColor': '#a89984', 'lineColor': '#d5c4a1', 'textColor': '#ffffff', 'mainBkg': '#282828', 'nodeBkg': '#3c3836', 'nodeTextColor': '#ffffff', 'nodeBorder': '#bdae93', 'clusterBkg': '#282828', 'clusterBorder': '#a89984', 'defaultLinkColor': '#d5c4a1', 'titleColor': '#ffffff', 'edgeLabelBackground': '#282828', 'labelBoxBkgColor': '#3c3836', 'labelBoxBorderColor': '#bdae93', 'labelTextColor': '#ffffff', 'loopTextColor': '#ffffff', 'noteBkgColor': '#282828', 'noteTextColor': '#ffffff', 'noteBorderColor': '#83a598', 'actorBkg': '#3c3836', 'actorBorder': '#bdae93', 'actorTextColor': '#ffffff', 'actorLineColor': '#d5c4a1', 'signalColor': '#d5c4a1', 'signalTextColor': '#ffffff', 'activationBkgColor': '#689d6a', 'activationBorderColor': '#8ec07c', 'sequenceNumberColor': '#ffffff'}, 'themeCSS': 'text, tspan { fill: #ffffff !important; color: #ffffff !important; } .messageText, .labelText, .loopText, .noteText, .actor text, .taskText, .sectionTitle text, .nodeLabel, .edgeLabel, .cluster-label text { fill: #ffffff !important; color: #ffffff !important; } .messageLine0, .messageLine1, .actor-line, .edgePath .path { stroke: #d5c4a1 !important; } .note { fill: #282828 !important; stroke: #83a598 !important; } .labelBox, .edgeLabel rect { fill: #3c3836 !important; stroke: #bdae93 !important; }'}}%%
flowchart TD
    A["Inicio: arreglo ordenado + objetivo"] --> B["Calcular mitad"]
    B --> C{"arr[mitad] == objetivo?"}
    C -- Sí --> D["Encontrado"]
    C -- No --> E{"objetivo < arr[mitad]?"}
    E -- Sí --> F["Buscar en mitad izquierda"]
    E -- No --> G["Buscar en mitad derecha"]
    F --> B
    G --> B
```

## Comparaciones típicas
- vs [[16 - Búsqueda - Lineal]]: O(log n) con requisito de ordenamiento vs O(n) sin requisitos
- vs [[15 - Big-O - O(log n) logarítmica]]: aplicación práctica de complejidad logarítmica
- vs [[25 - Estrategias - Divide and Conquer]]: caso concreto de una estrategia de reducción por mitades

## Palabras clave
- búsqueda binaria
- O(log n)
- arreglo ordenado
- mitad
- comparación

## Preguntas de examen
- ¿Por qué la búsqueda binaria requiere colección ordenada?
- ¿Qué ventaja práctica tiene sobre lineal en n grande?

## Errores comunes
- Aplicarla sobre datos no ordenados.
- Implementar mal límites izquierdo/derecho y caer en bucles infinitos.

## Mini-ejemplo (mental)
- Buscar una palabra en diccionario abriendo por la mitad en cada intento.
