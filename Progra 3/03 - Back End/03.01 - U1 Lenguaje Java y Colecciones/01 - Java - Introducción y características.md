# Java - Introducción y características

## Definición

Java es un lenguaje **orientado a objetos** y **portable**: se compila a bytecode y se ejecuta en una JVM, lo que permite correr en múltiples plataformas.

## Explicación

- *Qué problema resuelve*
    Resuelve la portabilidad entre sistemas operativos y mejora la robustez al detectar muchos errores en compilación.

- *Cómo funciona por arriba*
    - Código fuente `.java` → `javac` → bytecode `.class`
    - La JVM ejecuta ese bytecode (interpretación/JIT) en cada plataforma

- *Qué implica / qué permite*
    - Multiplataforma (WORA: Write Once, Run Anywhere)
    - Tipado estático (errores antes de ejecutar)
    - Garbage Collector (memoria automática)
    - Biblioteca estándar grande (`java.util`, `java.io`, etc.)

## Proceso de ejecución

```mermaid
%%{init: {'theme': 'base', 'themeVariables': { 'darkMode': true, 'background': '#1d2021', 'primaryColor': '#3c3836', 'primaryTextColor': '#ffffff', 'primaryBorderColor': '#bdae93', 'secondaryColor': '#504945', 'secondaryTextColor': '#ffffff', 'secondaryBorderColor': '#bdae93', 'tertiaryColor': '#282828', 'tertiaryTextColor': '#ffffff', 'tertiaryBorderColor': '#a89984', 'lineColor': '#d5c4a1', 'textColor': '#ffffff', 'mainBkg': '#282828', 'nodeBkg': '#3c3836', 'nodeTextColor': '#ffffff', 'nodeBorder': '#bdae93', 'clusterBkg': '#282828', 'clusterBorder': '#a89984', 'defaultLinkColor': '#d5c4a1', 'titleColor': '#ffffff', 'edgeLabelBackground': '#282828', 'labelBoxBkgColor': '#3c3836', 'labelBoxBorderColor': '#bdae93', 'labelTextColor': '#ffffff', 'loopTextColor': '#ffffff', 'noteBkgColor': '#282828', 'noteTextColor': '#ffffff', 'noteBorderColor': '#83a598', 'actorBkg': '#3c3836', 'actorBorder': '#bdae93', 'actorTextColor': '#ffffff', 'actorLineColor': '#d5c4a1', 'signalColor': '#d5c4a1', 'signalTextColor': '#ffffff', 'activationBkgColor': '#689d6a', 'activationBorderColor': '#8ec07c', 'sequenceNumberColor': '#ffffff'}, 'themeCSS': 'text, tspan { fill: #ffffff !important; color: #ffffff !important; } .messageText, .labelText, .loopText, .noteText, .actor text, .taskText, .sectionTitle text, .nodeLabel, .edgeLabel, .cluster-label text { fill: #ffffff !important; color: #ffffff !important; } .messageLine0, .messageLine1, .actor-line, .edgePath .path { stroke: #d5c4a1 !important; } .note { fill: #282828 !important; stroke: #83a598 !important; } .labelBox, .edgeLabel rect { fill: #3c3836 !important; stroke: #bdae93 !important; }'}}%%
flowchart LR
    A["Código Fuente.java"] -->|"javac Compilación"| B["Bytecode.class"]
    B -->|JVM| C[Windows]
    B -->|JVM| D[Linux]
    B -->|JVM| E[MacOS]
    
    style A fill:#1d2021,stroke:#928374,color:#ebdbb2
    style B fill:#458588,stroke:#83a598,color:#ebdbb2
    style C fill:#3c3836,stroke:#928374,color:#ebdbb2
    style D fill:#3c3836,stroke:#928374,color:#ebdbb2
    style E fill:#3c3836,stroke:#928374,color:#ebdbb2
```

## Palabras clave

- Bytecode
- JVM (Java Virtual Machine)
- WORA (Write Once, Run Anywhere)
- Garbage Collector

## Comparaciones típicas

- vs JavaScript: Java es tipado estáticamente (compile-time); JS es dinámico (runtime).
- vs C/C++: Java gestiona memoria automáticamente y busca portabilidad vía JVM.

## Preguntas de examen

- ¿Qué significa que Java sea "portable" y cómo lo logra?
- ¿Qué es el bytecode y qué ventaja tiene sobre código máquina?
- ¿Cuáles son los cuatro pilares de la POO en Java?
- ¿Qué es la JVM y cuál es su función?
- ¿Qué significa WORA?

## Errores comunes

- Pensar que Java es un lenguaje interpretado puro (es compilado a bytecode y luego interpretado/JIT)
- Confundir clase con objeto (clase es el molde, objeto es la instancia)
- Creer que Java es 100% orientado a objetos (tiene tipos primitivos)
- No entender que la JVM es diferente en cada sistema operativo

## Mini-ejemplo (mental)

Java es como **un traductor universal**: escribes un libro en un idioma neutral (código Java), un compilador lo traduce a un código intermedio universal (bytecode), y luego cada país tiene su propio intérprete (JVM) que lo traduce a su idioma local (código máquina). Así el mismo libro puede leerse en cualquier parte del mundo sin reescribirlo.
