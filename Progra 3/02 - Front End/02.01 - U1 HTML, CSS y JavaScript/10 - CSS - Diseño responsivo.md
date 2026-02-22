# CSS - Diseño responsivo

## Definición
Es una técnica que permite que las páginas web se adapten a los diferentes tamaños y resoluciones de diferentes dispositivos, como computadoras de escritorio, tabletas y teléfonos móviles, haciendo que el contenido sea legible y accesible en todos ellos.

## Explicación
- *Qué problema resuelve*
    Permite que una misma página web se vea bien y funcione correctamente en una variedad de dispositivos con diferentes tamaños de pantalla y resoluciones, mejorando la experiencia del usuario.
- *Cómo funciona por arriba*
    Utiliza técnicas como media queries en CSS para aplicar diferentes estilos según las características del dispositivo, como el ancho de la pantalla, la orientación y la resolución.
- *Qué implica / qué permite*
    Permite diseñar sitios web que son flexibles y adaptables, mejorando la accesibilidad y usabilidad en múltiples dispositivos.

## Herramientas típicas (mapa)

```mermaid
%%{init: {'theme': 'base', 'themeVariables': { 'darkMode': true, 'background': '#1d2021', 'primaryColor': '#3c3836', 'primaryTextColor': '#ffffff', 'primaryBorderColor': '#bdae93', 'secondaryColor': '#504945', 'secondaryTextColor': '#ffffff', 'secondaryBorderColor': '#bdae93', 'tertiaryColor': '#282828', 'tertiaryTextColor': '#ffffff', 'tertiaryBorderColor': '#a89984', 'lineColor': '#d5c4a1', 'textColor': '#ffffff', 'mainBkg': '#282828', 'nodeBkg': '#3c3836', 'nodeTextColor': '#ffffff', 'nodeBorder': '#bdae93', 'clusterBkg': '#282828', 'clusterBorder': '#a89984', 'defaultLinkColor': '#d5c4a1', 'titleColor': '#ffffff', 'edgeLabelBackground': '#282828', 'labelBoxBkgColor': '#3c3836', 'labelBoxBorderColor': '#bdae93', 'labelTextColor': '#ffffff', 'loopTextColor': '#ffffff', 'noteBkgColor': '#282828', 'noteTextColor': '#ffffff', 'noteBorderColor': '#83a598', 'actorBkg': '#3c3836', 'actorBorder': '#bdae93', 'actorTextColor': '#ffffff', 'actorLineColor': '#d5c4a1', 'signalColor': '#d5c4a1', 'signalTextColor': '#ffffff', 'activationBkgColor': '#689d6a', 'activationBorderColor': '#8ec07c', 'sequenceNumberColor': '#ffffff'}, 'themeCSS': 'text, tspan { fill: #ffffff !important; color: #ffffff !important; } .messageText, .labelText, .loopText, .noteText, .actor text, .taskText, .sectionTitle text, .nodeLabel, .edgeLabel, .cluster-label text { fill: #ffffff !important; color: #ffffff !important; } .messageLine0, .messageLine1, .actor-line, .edgePath .path { stroke: #d5c4a1 !important; } .note { fill: #282828 !important; stroke: #83a598 !important; } .labelBox, .edgeLabel rect { fill: #3c3836 !important; stroke: #bdae93 !important; }'}}%%
mindmap
  root((Responsivo))
    Media queries
      breakpoints
      orientación
    Layout
      Flexbox
      Grid
    Unidades
      %
      rem/em
      vw/vh
    Imágenes
      max-width: 100%
      object-fit

```

## Palabras clave
- Media queries
- Breakpoints
- Flexbox
- Grid layout

## Comparaciones típicas
- vs [[11 - Tailwind - Conceptos clave]]: responsivo en CSS usa media queries; en Tailwind se aplica con prefijos de breakpoints.
- vs [[08 - CSS - Propiedades comunes]]: el responsivo combina propiedades con reglas condicionales; las propiedades son los bloques base.

## Preguntas de examen
- ¿Cómo se utilizan los breakpoints en diseño responsivo?
- ¿Para qué sirve una media query en CSS?
- ¿Cuál es la diferencia entre diseño fijo y diseño responsivo?
- ¿Qué pasa si no se implementa diseño responsivo en un sitio web?

## Errores comunes
- No definir breakpoints adecuados para los dispositivos más comunes.
- No probar el diseño en múltiples dispositivos y resoluciones.
- Usar unidades fijas (px) en lugar de unidades relativas (%, em, rem).

## Mini-ejemplo (mental)
- Es como diseñar una casa que se ajusta automáticamente al tamaño de la familia que vive en ella, asegurando que todos tengan suficiente espacio y comodidad sin importar cuántas personas haya.
