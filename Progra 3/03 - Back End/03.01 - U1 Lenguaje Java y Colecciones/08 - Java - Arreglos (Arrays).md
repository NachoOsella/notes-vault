# Java - Arreglos (Arrays)

## Definición

Los arreglos son estructuras de datos que almacenan una **colección de elementos del mismo tipo** en posiciones contiguas de memoria. Tienen **tamaño fijo** definido al momento de creación.

## Explicación

- *Qué problema resuelve*
    Permite almacenar múltiples valores relacionados bajo un solo nombre, accesibles mediante índices numéricos. Útil para listas de datos del mismo tipo.

- *Cómo funciona por arriba*
    - Reserva un bloque contiguo de memoria
    - Cada elemento ocupa una posición indexada (0 a n-1)
    - El índice 0 es el primer elemento
    - El tamaño es inmutable después de crearlo

- *Qué implica / qué permite*
    - Almacenamiento ordenado de datos
    - Acceso rápido por índice (O(1))
    - Iteración secuencial
    - Tamaño fijo (limitación importante)

## Tipos de arreglos

```mermaid
%%{init: {'theme': 'base', 'themeVariables': { 'primaryColor': '#458588', 'primaryTextColor': '#ffffff', 'primaryBorderColor': '#83a598', 'lineColor': '#a89984', 'secondaryColor': '#689d6a', 'tertiaryColor': '#d79921', 'background': '#1d2021'}}}%%
mindmap
  root((Arreglos))
    Unidimensionales
      (Una sola fila)
      ("Sintaxis: tipo[]")
      ("Ej: int[5]")
    Multidimensionales
      Bidimensionales
        (Tabla / filas y columnas)
        ("Sintaxis: tipo[][]")
        ("Ej: int[3][4]")
      Tridimensionales
        (Cubo / capas)
        ("Sintaxis: tipo[][][]")
        ("Ej: int[2][3][4]")

```

## Arreglos unidimensionales

### Características
- Una sola fila de elementos
- Acceso mediante un índice: `array[índice]`
- Índices van de 0 a tamaño-1

### Visualización

```mermaid
%%{init: {'theme': 'base', 'themeVariables': { 'primaryColor': '#1d2021', 'primaryTextColor': '#ebdbb2', 'primaryBorderColor': '#928374', 'lineColor': '#a89984', 'secondaryColor': '#282828', 'tertiaryColor': '#3c3836'}}}%%
graph LR
    A["Índice 0"] -->|Valor| B["10"]
    C["Índice 1"] -->|Valor| D["20"]
    E["Índice 2"] -->|Valor| F["30"]
    G["Índice 3"] -->|Valor| H["40"]
    I["Índice 4"] -->|Valor| J["50"]
    
    style A fill:#458588,stroke:#83a598,color:#ebdbb2
    style B fill:#689d6a,stroke:#8ec07c,color:#ebdbb2
    style C fill:#458588,stroke:#83a598,color:#ebdbb2
    style D fill:#689d6a,stroke:#8ec07c,color:#ebdbb2
    style E fill:#d79921,stroke:#fabd2f,color:#1d2021
    style F fill:#689d6a,stroke:#8ec07c,color:#ebdbb2
    style G fill:#458588,stroke:#83a598,color:#ebdbb2
    style H fill:#689d6a,stroke:#8ec07c,color:#ebdbb2
    style I fill:#458588,stroke:#83a598,color:#ebdbb2
    style J fill:#689d6a,stroke:#8ec07c,color:#ebdbb2
```

### Limitaciones
- **Tamaño fijo**: No puede cambiar después de crearlo
- Si es muy pequeño: datos se pierden
- Si es muy grande: desperdicio de memoria
- Inserción/eliminación en medio es costosa (hay que mover elementos)

## Arreglos multidimensionales

### Bidimensionales (matrices)
- Como una tabla: filas y columnas
- Acceso: `matriz[fila][columna]`
- Útiles para: tableros de juego, matrices matemáticas, datos tabulares

### Tridimensionales
- Como un cubo: capas, filas, columnas
- Acceso: `cubo[capa][fila][columna]`
- Útiles para: juegos 3D (cubo Rubik), datos volumétricos

## Propiedad length

- Todos los arreglos tienen la propiedad `length`
- Devuelve el tamaño del arreglo
- Útil para bucles que recorren todo el arreglo

## Recorrido de arreglos

| Método | Cuándo usar | Características |
|--------|-------------|----------------|
| **for tradicional** | Necesitar índice | Control total del índice |
| **for-each** | Solo leer elementos | Más legible, sin índice |
| **while** | Condición especial | Flexibilidad |

## Arreglos vs Colecciones

| Característica | Arreglos | Colecciones (ArrayList, etc.) |
|----------------|----------|------------------------------|
| **Tamaño** | Fijo | Dinámico (crece automáticamente) |
| **Tipo de elementos** | Primitivos y objetos | Solo objetos (autoboxing para primitivos) |
| **Métodos** | Mínimos (length) | Muchos métodos útiles |
| **Generics** | No | Sí |
| **Rendimiento** | Más rápido acceso directo | Más flexible |

## Palabras clave

- Array / Arreglo
- Índice (index)
- length
- Unidimensional
- Bidimensional
- Multidimensional
- Tamaño fijo
- Elemento

## Comparaciones típicas

- vs [[09 - Colecciones - Introducción]]: arreglos son estáticos (tamaño fijo); colecciones son dinámicas
- vs [[10 - Colecciones - Listas (List)]]: ArrayList es la alternativa dinámica a los arreglos

## Preguntas de examen

- ¿Cuál es la principal limitación de los arreglos en Java?
- ¿Qué valor tiene el primer índice de un arreglo?
- ¿Cómo se accede a un elemento en un arreglo bidimensional?
- ¿Cuál es la diferencia entre arreglos y colecciones como ArrayList?
- ¿Qué propiedad devuelve el tamaño de un arreglo?

## Errores comunes

- ArrayIndexOutOfBoundsException: acceder a índice fuera de rango
- Pensar que arreglos pueden cambiar de tamaño
- Confundir `length` (propiedad de arreglos) con `size()` (método de colecciones)
- Olvidar que el último índice es `length - 1`, no `length`
- No inicializar el arreglo antes de usarlo

## Mini-ejemplo (mental)

Un arreglo es como **una fila de casilleros numerados**: tienes 5 casilleros (tamaño 5) numerados del 0 al 4, y cada uno guarda un valor. Una vez construida la fila, **no puedes agregar más casilleros** (tamaño fijo). Si quieres guardar más cosas, necesitas una estructura diferente (colecciones). Un arreglo bidimensional es como **un estacionamiento**: filas y columnas de espacios.
