# Testing - Introducción

## Definición
El testing es el proceso de evaluar y verificar el comportamiento de un sistema, aplicación o módulo de software para asegurarse de que funciona correctamente y cumple con los requerimientos especificados.

## Explicación
- *Qué problema resuelve*
    Permite identificar errores, bugs o problemas de rendimiento antes de que el software sea entregado al usuario final, mejorando la calidad del producto.
- *Cómo funciona por arriba*
    Se crean casos de prueba que ejecutan el código bajo diferentes condiciones y se verifican los resultados contra valores esperados. Puede ser manual o automatizado.
- *Qué implica / qué permite*
    Mejora la calidad y eficiencia del desarrollo. Reduce costos al detectar errores temprano. Facilita la colaboración en equipos al garantizar que los cambios no rompan funcionalidades existentes.

## Pirámide de testing (idea)

```mermaid
%%{init: {'theme': 'base', 'themeVariables': { 'darkMode': true, 'background': '#1d2021', 'primaryColor': '#3c3836', 'primaryTextColor': '#ffffff', 'primaryBorderColor': '#bdae93', 'secondaryColor': '#504945', 'secondaryTextColor': '#ffffff', 'secondaryBorderColor': '#bdae93', 'tertiaryColor': '#282828', 'tertiaryTextColor': '#ffffff', 'tertiaryBorderColor': '#a89984', 'lineColor': '#d5c4a1', 'textColor': '#ffffff', 'mainBkg': '#282828', 'nodeBkg': '#3c3836', 'nodeTextColor': '#ffffff', 'nodeBorder': '#bdae93', 'clusterBkg': '#282828', 'clusterBorder': '#a89984', 'defaultLinkColor': '#d5c4a1', 'titleColor': '#ffffff', 'edgeLabelBackground': '#282828', 'labelBoxBkgColor': '#3c3836', 'labelBoxBorderColor': '#bdae93', 'labelTextColor': '#ffffff', 'loopTextColor': '#ffffff', 'noteBkgColor': '#282828', 'noteTextColor': '#ffffff', 'noteBorderColor': '#83a598', 'actorBkg': '#3c3836', 'actorBorder': '#bdae93', 'actorTextColor': '#ffffff', 'actorLineColor': '#d5c4a1', 'signalColor': '#d5c4a1', 'signalTextColor': '#ffffff', 'activationBkgColor': '#689d6a', 'activationBorderColor': '#8ec07c', 'sequenceNumberColor': '#ffffff'}, 'themeCSS': 'text, tspan { fill: #ffffff !important; color: #ffffff !important; } .messageText, .labelText, .loopText, .noteText, .actor text, .taskText, .sectionTitle text, .nodeLabel, .edgeLabel, .cluster-label text { fill: #ffffff !important; color: #ffffff !important; } .messageLine0, .messageLine1, .actor-line, .edgePath .path { stroke: #d5c4a1 !important; } .note { fill: #282828 !important; stroke: #83a598 !important; } .labelBox, .edgeLabel rect { fill: #3c3836 !important; stroke: #bdae93 !important; }'}}%%
flowchart TD
  A[Unit tests: muchos, rápidos] --> B[Integration tests: menos, más lentos]
  B --> C[E2E/Acceptance: pocos, más costosos]

  style A fill:#689d6a,stroke:#8ec07c,color:#ebdbb2
  style B fill:#458588,stroke:#83a598,color:#ebdbb2
  style C fill:#d79921,stroke:#fabd2f,color:#1d2021

```

## Herramientas principales en Java
- **JUnit**: Framework de pruebas unitarias para crear y ejecutar tests automatizados.
- **TestNG**: Alternativa a JUnit con funcionalidades adicionales.
- **Mockito**: Framework para crear objetos simulados (mocks) y aislar dependencias.

## Palabras clave
- Testing
- Calidad de software
- Bugs
- Casos de prueba
- Automatización
- JUnit
- Mockito

## Comparaciones típicas
- vs [[11 - Testing - Fundamentos]]: introducción = panorama general y por qué testear; fundamentos = conceptos y principios que sostienen la práctica.
- vs [[12 - Testing - Tests unitarios]]: intro es general; unit tests son el tipo de test más "chico" y rápido.

## Preguntas de examen
- ¿Qué es el testing y cuál es su objetivo principal?
- ¿Cuáles son las herramientas de testing más populares en Java?
- ¿Por qué es importante realizar testing en el desarrollo de software?

## Errores comunes
- Pensar que el testing solo es necesario en proyectos grandes (todo proyecto se beneficia del testing).
- Confundir testing manual con automatizado: ambos son válidos pero tienen diferentes propósitos.
- Creer que el testing garantiza software sin errores (reduce bugs, pero no los elimina al 100%).

## Mini-ejemplo (mental)
El testing es como revisar un ensayo antes de entregarlo. Lees cada párrafo (unidad) buscando errores de ortografía (bugs), verificas que las ideas fluyan correctamente (integración) y finalmente te aseguras de que el ensayo responde la pregunta original (aceptación). Cuanto antes encuentres un error, más fácil es corregirlo.
