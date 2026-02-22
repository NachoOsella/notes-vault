# Java - Sintaxis básica

## Definición

La sintaxis de Java es el conjunto de reglas para escribir código válido y legible.

## Explicación

- *Qué problema resuelve*
    Define una estructura común para que el compilador y otros programadores entiendan el código.

- *Cómo funciona por arriba*
    - Todo programa va dentro de una clase
    - El punto de entrada es `main`
    - Las sentencias terminan con `;`
    - Los bloques usan `{}`

- *Qué implica / qué permite*
    - Menos ambigüedad
    - Errores detectados en compilación
    - Código más mantenible

## Estructura mínima

```mermaid
%%{init: {'theme': 'base', 'themeVariables': { 'darkMode': true, 'background': '#1d2021', 'primaryColor': '#3c3836', 'primaryTextColor': '#ffffff', 'primaryBorderColor': '#bdae93', 'secondaryColor': '#504945', 'secondaryTextColor': '#ffffff', 'secondaryBorderColor': '#bdae93', 'tertiaryColor': '#282828', 'tertiaryTextColor': '#ffffff', 'tertiaryBorderColor': '#a89984', 'lineColor': '#d5c4a1', 'textColor': '#ffffff', 'mainBkg': '#282828', 'nodeBkg': '#3c3836', 'nodeTextColor': '#ffffff', 'nodeBorder': '#bdae93', 'clusterBkg': '#282828', 'clusterBorder': '#a89984', 'defaultLinkColor': '#d5c4a1', 'titleColor': '#ffffff', 'edgeLabelBackground': '#282828', 'labelBoxBkgColor': '#3c3836', 'labelBoxBorderColor': '#bdae93', 'labelTextColor': '#ffffff', 'loopTextColor': '#ffffff', 'noteBkgColor': '#282828', 'noteTextColor': '#ffffff', 'noteBorderColor': '#83a598', 'actorBkg': '#3c3836', 'actorBorder': '#bdae93', 'actorTextColor': '#ffffff', 'actorLineColor': '#d5c4a1', 'signalColor': '#d5c4a1', 'signalTextColor': '#ffffff', 'activationBkgColor': '#689d6a', 'activationBorderColor': '#8ec07c', 'sequenceNumberColor': '#ffffff'}, 'themeCSS': 'text, tspan { fill: #ffffff !important; color: #ffffff !important; } .messageText, .labelText, .loopText, .noteText, .actor text, .taskText, .sectionTitle text, .nodeLabel, .edgeLabel, .cluster-label text { fill: #ffffff !important; color: #ffffff !important; } .messageLine0, .messageLine1, .actor-line, .edgePath .path { stroke: #d5c4a1 !important; } .note { fill: #282828 !important; stroke: #83a598 !important; } .labelBox, .edgeLabel rect { fill: #3c3836 !important; stroke: #bdae93 !important; }'}}%%
flowchart TD
    A[NombreClase.java] --> B[public class NombreClase]
    B --> C[public static void main]
    C --> D[Código]
```

## Reglas rápidas

- Java distingue mayúsculas y minúsculas
- El nombre de la clase pública debe coincidir con el archivo
- Usar convenciones: `CamelCase` en clases y `camelCase` en métodos/variables

## Palabras clave

- Clase
- `main`
- `;`
- `{}`
- Case-sensitive
- Convenciones de nombres

## Comparaciones típicas

- vs [[01 - Java - Introducción y características]]: esta nota baja a reglas concretas de escritura
- vs JavaScript: Java exige estructura de clase/método para arrancar

## Preguntas de examen

- ¿Cuál es el punto de entrada de un programa Java?
- ¿Por qué importa que el archivo coincida con la clase pública?
- ¿Qué diferencia hay entre `CamelCase` y `camelCase`?

## Errores comunes

- Olvidar `;`
- Romper mayúsculas/minúsculas en nombres
- Nombrar mal el archivo respecto de la clase pública

## Mini-ejemplo (mental)

La sintaxis es como la gramática: si rompes reglas básicas, el "corrector" (compilador) no te deja avanzar.
