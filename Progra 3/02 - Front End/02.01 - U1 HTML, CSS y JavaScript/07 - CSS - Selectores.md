# CSS - Selectores

## Definición
Son patrones utilizados para seleccionar los elementos del HTML a los que se le aplicarán estilos CSS.
Existen varios tipos de selectores, como selectores de tipo, clase, ID, atributo, pseudo-clases y pseudo-elementos.

## Explicación
- *Qué problema resuelve*
    Permiten apuntar a elementos específicos del HTML para aplicarles estilos de manera precisa y eficiente.
- *Cómo funciona por arriba*
    Los selectores se escriben al inicio de una regla CSS y definen a qué elementos del HTML se aplicarán las propiedades y valores especificados en esa regla.
- *Qué implica / qué permite*
    Permiten una gran flexibilidad y control sobre el diseño y la apariencia de una página web, facilitando la personalización y adaptación del estilo según diferentes criterios.

## Tipos de selectores (mapa)

```mermaid
%%{init: {'theme': 'base', 'themeVariables': { 'darkMode': true, 'background': '#1d2021', 'primaryColor': '#3c3836', 'primaryTextColor': '#ffffff', 'primaryBorderColor': '#bdae93', 'secondaryColor': '#504945', 'secondaryTextColor': '#ffffff', 'secondaryBorderColor': '#bdae93', 'tertiaryColor': '#282828', 'tertiaryTextColor': '#ffffff', 'tertiaryBorderColor': '#a89984', 'lineColor': '#d5c4a1', 'textColor': '#ffffff', 'mainBkg': '#282828', 'nodeBkg': '#3c3836', 'nodeTextColor': '#ffffff', 'nodeBorder': '#bdae93', 'clusterBkg': '#282828', 'clusterBorder': '#a89984', 'defaultLinkColor': '#d5c4a1', 'titleColor': '#ffffff', 'edgeLabelBackground': '#282828', 'labelBoxBkgColor': '#3c3836', 'labelBoxBorderColor': '#bdae93', 'labelTextColor': '#ffffff', 'loopTextColor': '#ffffff', 'noteBkgColor': '#282828', 'noteTextColor': '#ffffff', 'noteBorderColor': '#83a598', 'actorBkg': '#3c3836', 'actorBorder': '#bdae93', 'actorTextColor': '#ffffff', 'actorLineColor': '#d5c4a1', 'signalColor': '#d5c4a1', 'signalTextColor': '#ffffff', 'activationBkgColor': '#689d6a', 'activationBorderColor': '#8ec07c', 'sequenceNumberColor': '#ffffff'}, 'themeCSS': 'text, tspan { fill: #ffffff !important; color: #ffffff !important; } .messageText, .labelText, .loopText, .noteText, .actor text, .taskText, .sectionTitle text, .nodeLabel, .edgeLabel, .cluster-label text { fill: #ffffff !important; color: #ffffff !important; } .messageLine0, .messageLine1, .actor-line, .edgePath .path { stroke: #d5c4a1 !important; } .note { fill: #282828 !important; stroke: #83a598 !important; } .labelBox, .edgeLabel rect { fill: #3c3836 !important; stroke: #bdae93 !important; }'}}%%
mindmap
  root((Selectores CSS))
    Tipo
      div
      p
      button
    Clase
      .card
      .btn-primary
    ID
      #header
      #app
    Atributo
      input[type=\"text\"]
      a[href]
    Pseudo-clase
      :hover
      :focus
      :nth-child()
    Pseudo-elemento
      ::before
      ::after

```

## Palabras clave
- Selector
- Regla CSS
- Especificidad
- Herencia

## Comparaciones típicas
- vs [[04 - HTML - Principales etiquetas]]: HTML define los elementos; los selectores son la forma de apuntar a esos elementos para estilarlos.
- vs [[08 - CSS - Propiedades comunes]]: selectores apuntan a elementos; propiedades aplican el estilo.

## Preguntas de examen
- ¿Qué es un selector en CSS?
- ¿Para qué sirve un selector?
- ¿Cuál es la diferencia entre un selector de clase y un selector de ID?
- ¿Qué pasa si varios selectores apuntan al mismo elemento con diferentes estilos?

## Errores comunes
- Confundir selectores de clase (.) con selectores de ID (#).
- No entender la especificidad y el orden de los selectores, lo que puede llevar a resultados inesperados.
- Olvidar que los selectores deben coincidir exactamente con los elementos HTML.

## Mini-ejemplo (mental)
- Es como tener un mapa (HTML) y usar una lupa (selector) para encontrar un lugar específico (elemento) donde quieres pintar (aplicar estilos).
