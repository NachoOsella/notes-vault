# Colecciones - Listas (List)

## Definición

Las **Listas** son colecciones ordenadas que permiten elementos duplicados y acceso por índice. La interfaz `List` extiende `Collection` y define el comportamiento de listas secuenciales.

## Explicación

- *Qué problema resuelve*
    Proporciona estructuras de datos dinámicas que mantienen el orden de inserción, permiten acceso posicional y manejan duplicados. A diferencia de los arreglos, crecen automáticamente.

- *Cómo funciona por arriba*
    - Interface `List` define operaciones: add, get, remove, set, indexOf
    - Implementaciones usan diferentes estructuras internas
    - ArrayList: arreglo dinámico
    - LinkedList: lista doblemente enlazada
    - Vector: similar a ArrayList pero sincronizado (thread-safe)

- *Qué implica / qué permite*
    - Acceso por índice (posición)
    - Mantenimiento del orden de inserción
    - Permitir elementos duplicados
    - Diferentes implementaciones según necesidades de rendimiento

## Jerarquía y estructura

```mermaid
%%{init: {'theme': 'base', 'themeVariables': { 'darkMode': true, 'background': '#1d2021', 'primaryColor': '#3c3836', 'primaryTextColor': '#ffffff', 'primaryBorderColor': '#bdae93', 'secondaryColor': '#504945', 'secondaryTextColor': '#ffffff', 'secondaryBorderColor': '#bdae93', 'tertiaryColor': '#282828', 'tertiaryTextColor': '#ffffff', 'tertiaryBorderColor': '#a89984', 'lineColor': '#d5c4a1', 'textColor': '#ffffff', 'mainBkg': '#282828', 'nodeBkg': '#3c3836', 'nodeTextColor': '#ffffff', 'nodeBorder': '#bdae93', 'clusterBkg': '#282828', 'clusterBorder': '#a89984', 'defaultLinkColor': '#d5c4a1', 'titleColor': '#ffffff', 'edgeLabelBackground': '#282828', 'labelBoxBkgColor': '#3c3836', 'labelBoxBorderColor': '#bdae93', 'labelTextColor': '#ffffff', 'loopTextColor': '#ffffff', 'noteBkgColor': '#282828', 'noteTextColor': '#ffffff', 'noteBorderColor': '#83a598', 'actorBkg': '#3c3836', 'actorBorder': '#bdae93', 'actorTextColor': '#ffffff', 'actorLineColor': '#d5c4a1', 'signalColor': '#d5c4a1', 'signalTextColor': '#ffffff', 'activationBkgColor': '#689d6a', 'activationBorderColor': '#8ec07c', 'sequenceNumberColor': '#ffffff'}, 'themeCSS': 'text, tspan { fill: #ffffff !important; color: #ffffff !important; } .messageText, .labelText, .loopText, .noteText, .actor text, .taskText, .sectionTitle text, .nodeLabel, .edgeLabel, .cluster-label text { fill: #ffffff !important; color: #ffffff !important; } .messageLine0, .messageLine1, .actor-line, .edgePath .path { stroke: #d5c4a1 !important; } .note { fill: #282828 !important; stroke: #83a598 !important; } .labelBox, .edgeLabel rect { fill: #3c3836 !important; stroke: #bdae93 !important; }'}}%%
graph TD
    A[Collection] --> B[List]
    B --> C[ArrayList]
    B --> D[LinkedList]
    B --> E[Vector]
    
    C --> C1["Arreglo dinámico"]
    C1 --> C2["Acceso rápido O1"]
    C1 --> C3["Inserción lenta On"]
    
    D --> D1["Lista enlazada"]
    D1 --> D2["Acceso lento On"]
    D1 --> D3["Inserción rápida O1"]
    
    E --> E1["Arreglo sincronizado"]
    E1 --> E2["Thread-safe"]
    E1 --> E3["Más lento"]
    
    style A fill:#3c3836,stroke:#928374,color:#ebdbb2
    style B fill:#d79921,stroke:#fabd2f,color:#1d2021
    style C fill:#689d6a,stroke:#8ec07c,color:#ebdbb2
    style D fill:#458588,stroke:#83a598,color:#ebdbb2
    style E fill:#cc241d,stroke:#fb4934,color:#ebdbb2
```

## ArrayList

### Características
- Basado en **arreglo dinámico** que se redimensiona automáticamente
- Acceso por índice muy rápido: **O(1)**
- Inserción/eliminación en medio: **O(n)** (debe mover elementos)
- **No sincronizado** (no thread-safe)
- Cuando se llena, crea nuevo arreglo 50% más grande y copia elementos

### Cuándo usar
- Acceso frecuente por índice
- Recorrido secuencial
- Pocas inserciones/eliminaciones en medio

## LinkedList

### Características
- Basada en **nodos enlazados** (doble enlace)
- Cada nodo tiene: dato + referencia al siguiente + referencia al anterior
- Acceso por índice lento: **O(n)** (debe recorrer)
- Inserción/eliminación rápida: **O(1)** (solo cambia referencias)
- **No sincronizada**

### Cuándo usar
- Muchas inserciones/eliminaciones
- Poco acceso por índice
- Implementación de colas o pilas

## Vector

### Características
- Similar a ArrayList pero **sincronizado** (thread-safe)
- Métodos son `synchronized`
- Cuando se llena, crea arreglo con capacidad fija de incremento (diferente de ArrayList)
- **Más lento** que ArrayList por el overhead de sincronización
- Legado de Java 1.0

### Cuándo usar
- Aplicaciones multihilo donde múltiples threads acceden a la lista
- En general, se prefiere `ArrayList` + `Collections.synchronizedList()`

## Comparativa de implementaciones

| Operación | ArrayList | LinkedList | Vector |
|-----------|-----------|------------|--------|
| **get(index)** | 🚀 O(1) - Directo | 🐢 O(n) - Recorre | 🚀 O(1) |
| **add(ultimo)** | ⚡ O(1)* | 🚀 O(1) | ⚡ O(1)* |
| **add(inicio)** | ❌ O(n) - Mueve todos | 🚀 O(1) | ❌ O(n) |
| **add(medio)** | 🐢 O(n) | 🚀 O(1) cerca de extremos | 🐢 O(n) |
| **remove** | 🐢 O(n) | 🚀 O(1) | 🐢 O(n) |
| **Memoria** | ✅ Menor | ❌ Mayor (referencias) | ✅ Menor |
| **Thread-safe** | ❌ No | ❌ No | ✅ Sí |
| **Overhead sync** | Ninguno | Ninguno | Alto |

*Amortizado, puede ser O(n) si necesita redimensionar

## Estructura interna visual

### ArrayList
```mermaid
%%{init: {'theme': 'base', 'themeVariables': { 'darkMode': true, 'background': '#1d2021', 'primaryColor': '#3c3836', 'primaryTextColor': '#ffffff', 'primaryBorderColor': '#bdae93', 'secondaryColor': '#504945', 'secondaryTextColor': '#ffffff', 'secondaryBorderColor': '#bdae93', 'tertiaryColor': '#282828', 'tertiaryTextColor': '#ffffff', 'tertiaryBorderColor': '#a89984', 'lineColor': '#d5c4a1', 'textColor': '#ffffff', 'mainBkg': '#282828', 'nodeBkg': '#3c3836', 'nodeTextColor': '#ffffff', 'nodeBorder': '#bdae93', 'clusterBkg': '#282828', 'clusterBorder': '#a89984', 'defaultLinkColor': '#d5c4a1', 'titleColor': '#ffffff', 'edgeLabelBackground': '#282828', 'labelBoxBkgColor': '#3c3836', 'labelBoxBorderColor': '#bdae93', 'labelTextColor': '#ffffff', 'loopTextColor': '#ffffff', 'noteBkgColor': '#282828', 'noteTextColor': '#ffffff', 'noteBorderColor': '#83a598', 'actorBkg': '#3c3836', 'actorBorder': '#bdae93', 'actorTextColor': '#ffffff', 'actorLineColor': '#d5c4a1', 'signalColor': '#d5c4a1', 'signalTextColor': '#ffffff', 'activationBkgColor': '#689d6a', 'activationBorderColor': '#8ec07c', 'sequenceNumberColor': '#ffffff'}, 'themeCSS': 'text, tspan { fill: #ffffff !important; color: #ffffff !important; } .messageText, .labelText, .loopText, .noteText, .actor text, .taskText, .sectionTitle text, .nodeLabel, .edgeLabel, .cluster-label text { fill: #ffffff !important; color: #ffffff !important; } .messageLine0, .messageLine1, .actor-line, .edgePath .path { stroke: #d5c4a1 !important; } .note { fill: #282828 !important; stroke: #83a598 !important; } .labelBox, .edgeLabel rect { fill: #3c3836 !important; stroke: #bdae93 !important; }'}}%%
graph LR
    A[Índice 0] -->|→| B[Índice 1]
    B -->|→| C[Índice 2]
    C -->|→| D[Índice 3]
    D -->|→| E[Índice 4]
    
    style A fill:#689d6a,stroke:#8ec07c,color:#ebdbb2
    style B fill:#689d6a,stroke:#8ec07c,color:#ebdbb2
    style C fill:#689d6a,stroke:#8ec07c,color:#ebdbb2
    style D fill:#689d6a,stroke:#8ec07c,color:#ebdbb2
    style E fill:#689d6a,stroke:#8ec07c,color:#ebdbb2
```

### LinkedList
```mermaid
%%{init: {'theme': 'base', 'themeVariables': { 'darkMode': true, 'background': '#1d2021', 'primaryColor': '#3c3836', 'primaryTextColor': '#ffffff', 'primaryBorderColor': '#bdae93', 'secondaryColor': '#504945', 'secondaryTextColor': '#ffffff', 'secondaryBorderColor': '#bdae93', 'tertiaryColor': '#282828', 'tertiaryTextColor': '#ffffff', 'tertiaryBorderColor': '#a89984', 'lineColor': '#d5c4a1', 'textColor': '#ffffff', 'mainBkg': '#282828', 'nodeBkg': '#3c3836', 'nodeTextColor': '#ffffff', 'nodeBorder': '#bdae93', 'clusterBkg': '#282828', 'clusterBorder': '#a89984', 'defaultLinkColor': '#d5c4a1', 'titleColor': '#ffffff', 'edgeLabelBackground': '#282828', 'labelBoxBkgColor': '#3c3836', 'labelBoxBorderColor': '#bdae93', 'labelTextColor': '#ffffff', 'loopTextColor': '#ffffff', 'noteBkgColor': '#282828', 'noteTextColor': '#ffffff', 'noteBorderColor': '#83a598', 'actorBkg': '#3c3836', 'actorBorder': '#bdae93', 'actorTextColor': '#ffffff', 'actorLineColor': '#d5c4a1', 'signalColor': '#d5c4a1', 'signalTextColor': '#ffffff', 'activationBkgColor': '#689d6a', 'activationBorderColor': '#8ec07c', 'sequenceNumberColor': '#ffffff'}, 'themeCSS': 'text, tspan { fill: #ffffff !important; color: #ffffff !important; } .messageText, .labelText, .loopText, .noteText, .actor text, .taskText, .sectionTitle text, .nodeLabel, .edgeLabel, .cluster-label text { fill: #ffffff !important; color: #ffffff !important; } .messageLine0, .messageLine1, .actor-line, .edgePath .path { stroke: #d5c4a1 !important; } .note { fill: #282828 !important; stroke: #83a598 !important; } .labelBox, .edgeLabel rect { fill: #3c3836 !important; stroke: #bdae93 !important; }'}}%%
graph LR
    A[Nodo 1] <-->|←→| B[Nodo 2]
    B <-->|←→| C[Nodo 3]
    C <-->|←→| D[Nodo 4]
    
    style A fill:#458588,stroke:#83a598,color:#ebdbb2
    style B fill:#458588,stroke:#83a598,color:#ebdbb2
    style C fill:#458588,stroke:#83a598,color:#ebdbb2
    style D fill:#458588,stroke:#83a598,color:#ebdbb2
```

## Palabras clave

- List / ArrayList / LinkedList / Vector
- Acceso por índice
- Arreglo dinámico
- Lista enlazada (nodos)
- Sincronización (thread-safe)
- O(1) vs O(n)
- Redimensionamiento

## Comparaciones típicas

- vs [[09 - Colecciones - Introducción]]: List es la interfaz; ArrayList/LinkedList/Vector son implementaciones
- vs [[08 - Java - Arreglos (Arrays)]]: ArrayList es un arreglo dinámico; los arreglos son estáticos
- vs [[11 - Colecciones - Mapas (Map)]]: List usa índices numéricos; Map usa claves arbitrarias

## Preguntas de examen

- ¿Cuál es la diferencia entre ArrayList y LinkedList?
- ¿Por qué LinkedList es mejor para inserciones frecuentes?
- ¿Qué significa que Vector sea "sincronizado"?
- ¿Cuál es la complejidad O(?) de get(index) en ArrayList?
- ¿Cuándo debería usar Vector sobre ArrayList?

## Errores comunes

- Usar LinkedList cuando se necesita acceso frecuente por índice (muy lento)
- Usar Vector en aplicaciones no concurrentes (overhead innecesario)
- No considerar el costo de redimensionamiento en ArrayList
- Pensar que todas las operaciones son igual de rápidas en todas las implementaciones
- Modificar la lista mientras se itera (ConcurrentModificationException)

## Mini-ejemplo (mental)

**ArrayList** es como **una fila de sillas numeradas en el cine**: llegas directo a tu asiento (acceso rápido), pero si alguien se sienta en medio, todos los demás deben moverse (inserción lenta).

**LinkedList** es como **el juego del teléfono**: para llegar al final debes pasar por todos los participantes (acceso lento), pero insertar a alguien es solo tomar las manos de dos personas (inserción rápida).

**Vector** es como **una fila de sillas con un guardia de seguridad**: solo una persona puede moverse a la vez (thread-safe), lo que hace todo más lento pero seguro en multitudes (multihilo).
