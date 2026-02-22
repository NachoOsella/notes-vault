# Java - Operadores

## Definición

Los operadores son símbolos que realizan operaciones sobre operandos (variables, valores, expresiones). Java proporciona operadores aritméticos, relacionales, lógicos, de asignación y más.

## Explicación

- *Qué problema resuelve*
    Permite realizar cálculos matemáticos, comparaciones, asignaciones y operaciones lógicas fundamentales para cualquier programa.

- *Cómo funciona por arriba*
    - Los operadores toman uno o dos operandos
    - Realizan la operación definida
    - Devuelven un resultado del tipo correspondiente
    - Precedencia determina orden de evaluación

- *Qué implica / qué permite*
    - Expresiones matemáticas complejas
    - Toma de decisiones (comparaciones)
    - Control de flujo (operadores lógicos)
    - Asignaciones eficientes

## Categorías de operadores

```mermaid
%%{init: {'theme': 'base', 'themeVariables': { 'darkMode': true, 'background': '#1d2021', 'primaryColor': '#3c3836', 'primaryTextColor': '#ffffff', 'primaryBorderColor': '#bdae93', 'secondaryColor': '#504945', 'secondaryTextColor': '#ffffff', 'secondaryBorderColor': '#bdae93', 'tertiaryColor': '#282828', 'tertiaryTextColor': '#ffffff', 'tertiaryBorderColor': '#a89984', 'lineColor': '#d5c4a1', 'textColor': '#ffffff', 'mainBkg': '#282828', 'nodeBkg': '#3c3836', 'nodeTextColor': '#ffffff', 'nodeBorder': '#bdae93', 'clusterBkg': '#282828', 'clusterBorder': '#a89984', 'defaultLinkColor': '#d5c4a1', 'titleColor': '#ffffff', 'edgeLabelBackground': '#282828', 'labelBoxBkgColor': '#3c3836', 'labelBoxBorderColor': '#bdae93', 'labelTextColor': '#ffffff', 'loopTextColor': '#ffffff', 'noteBkgColor': '#282828', 'noteTextColor': '#ffffff', 'noteBorderColor': '#83a598', 'actorBkg': '#3c3836', 'actorBorder': '#bdae93', 'actorTextColor': '#ffffff', 'actorLineColor': '#d5c4a1', 'signalColor': '#d5c4a1', 'signalTextColor': '#ffffff', 'activationBkgColor': '#689d6a', 'activationBorderColor': '#8ec07c', 'sequenceNumberColor': '#ffffff'}, 'themeCSS': 'text, tspan { fill: #ffffff !important; color: #ffffff !important; } .messageText, .labelText, .loopText, .noteText, .actor text, .taskText, .sectionTitle text, .nodeLabel, .edgeLabel, .cluster-label text { fill: #ffffff !important; color: #ffffff !important; } .messageLine0, .messageLine1, .actor-line, .edgePath .path { stroke: #d5c4a1 !important; } .note { fill: #282828 !important; stroke: #83a598 !important; } .labelBox, .edgeLabel rect { fill: #3c3836 !important; stroke: #bdae93 !important; }'}}%%
mindmap
  root((Operadores))
    Aritméticos
      + - * / %
      ++ --
    Relacionales
      == !=
      < > <= >=
    Lógicos
      && || !
    Asignación
      = += -=
      *= /= %=
    Otros
      Ternario ? :
      instanceof
```

## Reglas rápidas

- `=` asigna, `==` compara
- `/` entre enteros trunca (ej: `5/2` = `2`)
- `&&` y `||` cortocircuitan (a veces evita `NullPointerException`)
- Si hay dudas de precedencia, usar paréntesis

## Palabras clave

- Operadores aritméticos
- Operadores relacionales
- Operadores lógicos
- Operadores de asignación
- Precedencia
- Cortocircuito
- Incremento/decremento

## Comparaciones típicas

- vs [[04 - Java - Tipos de datos]]: los operadores trabajan sobre tipos de datos
- vs [[07 - Java - Estructuras de control]]: operadores relacionales y lógicos se usan en condiciones

## Preguntas de examen

- ¿Cuál es la diferencia entre `=` y `==`?
- ¿Qué hace el operador `%` (módulo)?
- ¿Qué es el cortocircuito en operadores lógicos?
- ¿Cuál es la precedencia: `&&` o `||`?
- ¿Qué diferencia hay entre `++x` y `x++`?

## Errores comunes

- Usar `=` en lugar de `==` en comparaciones
- No considerar precedencia (usar paréntesis para claridad)
- Dividir enteros esperando decimales (`5/2` = 2, no 2.5)
- Olvidar que `&&` tiene precedencia sobre `||`
- No usar cortocircuito a favor (ej: verificar null antes de usar)

## Mini-ejemplo (mental)

Los operadores son como **herramientas de una calculadora**: `+ - * /` son las básicas; `%` te dice cuánto sobra de una división; `&& || !` son interruptores lógicos que combinan condiciones; `++ --` son atajos para sumar/restar 1 rápidamente. La **precedencia** es como el orden de operaciones en matemáticas: paréntesis primero, luego multiplicación, luego suma.
