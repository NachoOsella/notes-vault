# Java - JDK y JVM

## Definición

El **JDK** es el kit para *desarrollar* (incluye `javac`). La **JVM** es lo que *ejecuta* bytecode `.class`. El **JRE** es el entorno de ejecución (JVM + bibliotecas).

## Explicación

- *Qué problema resuelve*
    Separa desarrollo de ejecución y permite portabilidad: el bytecode se ejecuta sobre una JVM específica de cada sistema.

- *Cómo funciona por arriba*
    - Escribís `.java`
    - Compilás con `javac` (del JDK) a `.class`
    - Ejecutás con `java` (sobre la JVM) en tu sistema operativo

- *Qué implica / qué permite*
    - Para programar Java necesitás JDK
    - Para ejecutar programas Java, alcanza con JRE/JDK
    - Portabilidad: el mismo `.class` se ejecuta en distintas JVM

```mermaid
%%{init: {'theme': 'base', 'themeVariables': { 'primaryColor': '#1d2021', 'primaryTextColor': '#ebdbb2', 'primaryBorderColor': '#928374', 'lineColor': '#a89984', 'secondaryColor': '#282828', 'tertiaryColor': '#3c3836'}}}%%
flowchart LR
    A[".java"] -->|javac (JDK)| B[".class (bytecode)"]
    B -->|JVM| C["Ejecución (Windows/Linux/Mac)"]
    
    style A fill:#1d2021,stroke:#928374,color:#ebdbb2
    style B fill:#d79921,stroke:#fabd2f,color:#1d2021
    style C fill:#689d6a,stroke:#8ec07c,color:#ebdbb2
```

## JRE vs JDK

| Aspecto | JRE | JDK |
|---------|-----|-----|
| **Significado** | Java Runtime Environment | Java Development Kit |
| **Contiene** | JVM + Bibliotecas | JRE + Herramientas de desarrollo |
| **Para** | Ejecutar programas Java | Desarrollar programas Java |
| **Incluye compilador** | ❌ No | ✅ Sí (javac) |
| **Incluye debugger** | ❌ No | ✅ Sí (jdb) |

> **Relación**: JDK = JRE + Herramientas de desarrollo

## Palabras clave

- JDK (Java Development Kit)
- JRE (Java Runtime Environment)
- JVM (Java Virtual Machine)
- Bytecode
- javac

## Comparaciones típicas

- vs [[01 - Java - Introducción y características]]: JDK es el kit completo; JVM es el componente de ejecución

## Preguntas de examen

- ¿Cuál es la diferencia entre JDK, JRE y JVM?
- ¿Qué componente del JDK convierte .java a .class?
- ¿Por qué el bytecode permite portabilidad?

## Errores comunes

- Confundir JDK con JRE (JRE solo ejecuta, JDK también compila)
- No entender que necesitas JDK para desarrollar, pero JRE es suficiente para ejecutar

## Mini-ejemplo (mental)

El **JDK es como un kit de carpintería completo**: incluye herramientas para cortar (javac), lijar (debugger), y el manual (javadoc). La **JVM es como el taller**: es donde realmente se construye y ensambla (ejecuta). El **bytecode son los planos universales**: cualquier taller (JVM) en cualquier ciudad (sistema operativo) puede seguirlos para construir el mismo mueble (programa).
