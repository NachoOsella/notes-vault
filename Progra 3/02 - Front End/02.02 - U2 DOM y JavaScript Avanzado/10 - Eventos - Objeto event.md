# Eventos - Objeto event

## Definición

El **objeto event** (también llamado `e` o `evt`) es un objeto que el navegador crea automáticamente cuando ocurre un evento. Contiene toda la información sobre el suceso: tipo, ubicación, elemento disparador, y métodos para controlar su comportamiento.

## Explicación

- *Qué problema resuelve*
    Proporciona acceso estandarizado a la información del evento. Sin él, no sabríamos qué elemento fue clickeado, qué tecla se presionó, ni podríamos controlar la propagación o comportamiento por defecto.

- *Cómo funciona por arriba*
    - El navegador instancia automáticamente el objeto cuando ocurre el evento
    - Se pasa como primer argumento a la función manejadora
    - Contiene propiedades específicas según el tipo de evento
    - Incluye métodos para controlar: `preventDefault()`, `stopPropagation()`
    - Viaja a través del event flow (captura → target → bubbling)

- *Qué implica / qué permite*
    - Acceder a información detallada del evento
    - Prevenir comportamientos por defecto del navegador
    - Controlar la propagación del evento
    - Diferenciar entre elemento origen y elemento con listener
    - Obtener datos específicos (coordenadas, teclas, etc.)

## Propiedades fundamentales

| Propiedad | Descripción | Ejemplo de valor |
|-----------|-------------|------------------|
| `type` | Tipo de evento | `"click"`, `"keydown"` |
| `target` | Elemento donde **originariamente** ocurrió | El botón clickeado |
| `currentTarget` | Elemento con el **listener adjunto** | El contenedor |
| `timeStamp` | Tiempo en ms desde carga de página | `1234567890` |

### Target vs CurrentTarget

```mermaid
%%{init: {'theme': 'base', 'themeVariables': { 'darkMode': true, 'background': '#1d2021', 'primaryColor': '#3c3836', 'primaryTextColor': '#ffffff', 'primaryBorderColor': '#bdae93', 'secondaryColor': '#504945', 'secondaryTextColor': '#ffffff', 'secondaryBorderColor': '#bdae93', 'tertiaryColor': '#282828', 'tertiaryTextColor': '#ffffff', 'tertiaryBorderColor': '#a89984', 'lineColor': '#d5c4a1', 'textColor': '#ffffff', 'mainBkg': '#282828', 'nodeBkg': '#3c3836', 'nodeTextColor': '#ffffff', 'nodeBorder': '#bdae93', 'clusterBkg': '#282828', 'clusterBorder': '#a89984', 'defaultLinkColor': '#d5c4a1', 'titleColor': '#ffffff', 'edgeLabelBackground': '#282828', 'labelBoxBkgColor': '#3c3836', 'labelBoxBorderColor': '#bdae93', 'labelTextColor': '#ffffff', 'loopTextColor': '#ffffff', 'noteBkgColor': '#282828', 'noteTextColor': '#ffffff', 'noteBorderColor': '#83a598', 'actorBkg': '#3c3836', 'actorBorder': '#bdae93', 'actorTextColor': '#ffffff', 'actorLineColor': '#d5c4a1', 'signalColor': '#d5c4a1', 'signalTextColor': '#ffffff', 'activationBkgColor': '#689d6a', 'activationBorderColor': '#8ec07c', 'sequenceNumberColor': '#ffffff'}, 'themeCSS': 'text, tspan { fill: #ffffff !important; color: #ffffff !important; } .messageText, .labelText, .loopText, .noteText, .actor text, .taskText, .sectionTitle text, .nodeLabel, .edgeLabel, .cluster-label text { fill: #ffffff !important; color: #ffffff !important; } .messageLine0, .messageLine1, .actor-line, .edgePath .path { stroke: #d5c4a1 !important; } .note { fill: #282828 !important; stroke: #83a598 !important; } .labelBox, .edgeLabel rect { fill: #3c3836 !important; stroke: #bdae93 !important; }'}}%%
graph TD
    A[< ul id="lista" >] -->|addEventListener| B[Listener en UL]
    A --> C[< li >Item 1</li >]
    A --> D[< li >Item 2</li >]
    
    C -->|Click| E[event.target = LI]
    B -->|Maneja| F[event.currentTarget = UL]
    
    style A fill:#458588,stroke:#83a598,color:#ebdbb2
    style B fill:#3c3836,stroke:#928374,color:#ebdbb2
    style C fill:#d79921,stroke:#fabd2f,color:#1d2021
    style D fill:#3c3836,stroke:#928374,color:#ebdbb2
    style E fill:#cc241d,stroke:#fb4934,color:#ebdbb2
    style F fill:#689d6a,stroke:#8ec07c,color:#ebdbb2
```

**Diferencia clave:**
- `target`: Donde **ocurrió** el evento (el LI clickeado)
- `currentTarget`: Donde está el **listener** (el UL contenedor)

## Métodos de control

### preventDefault()
Previene el **comportamiento por defecto** del navegador.

**Casos de uso:**
- Evitar recarga de página en formularios
- Prevenir navegación de enlaces
- Deshabilitar menú contextual (click derecho)
- Bloquear atajos de teclado del navegador

### stopPropagation()
Detiene la **propagación** del evento (captura o bubbling).

**Útil cuando:**
- Un evento en hijo no debe afectar al padre
- Se quiere evitar que múltiples listeners se disparen
- Se implementa comportamiento específico que no debe burbujear

### stopImmediatePropagation()
Detiene propagación **Y** previene otros listeners en el **mismo elemento**.

**Diferencia con stopPropagation:**
- `stopPropagation`: Detiene bubbling/capturing, pero otros listeners en el mismo elemento sí se ejecutan
- `stopImmediatePropagation`: Detiene TODO, incluso listeners posteriores en el mismo elemento

## Propiedades por tipo de evento

### Eventos de mouse

| Propiedad | Qué indica |
|-----------|------------|
| `clientX/Y` | Coordenadas relativas a la ventana visible |
| `pageX/Y` | Coordenadas relativas al documento completo |
| `offsetX/Y` | Coordenadas relativas al elemento clickeado |
| `button` | Botón: 0=izq, 1=medio, 2=der |

### Eventos de teclado

| Propiedad | Qué indica |
|-----------|------------|
| `key` | Valor de la tecla ("Enter", "a") |
| `code` | Código físico ("KeyA", "Enter") |
| `ctrlKey/altKey/shiftKey/metaKey` | true si modifier está presionado |
| `repeat` | true si tecla está mantenida y se repite |

> ⚠️ `keyCode` está **obsoleto**. Usar `key` o `code`.

### Eventos de formulario

| Propiedad | Qué indica |
|-----------|------------|
| `target.value` | Valor actual del input |
| `target.checked` | Estado de checkbox |
| `target.files` | Archivos seleccionados (input file) |
| `submitter` | Elemento que disparó el submit |

## Palabras clave

- Objeto event
- target / currentTarget
- preventDefault
- stopPropagation / stopImmediatePropagation
- type / timeStamp
- clientX/clientY / pageX/pageY
- key / code

## Comparaciones típicas

- vs [[08 - Eventos - Event flow (fases y flujo)]]: el objeto event tiene métodos para controlar el flujo
- vs [[09 - Eventos - Eventos comunes en la web]]: cada tipo de evento genera un objeto con propiedades específicas

## Preguntas de examen

- ¿Cuál es la diferencia entre `event.target` y `event.currentTarget`?
- ¿Para qué sirve `preventDefault()`?
- ¿Qué diferencia hay entre `stopPropagation()` y `stopImmediatePropagation()`?
- ¿Cómo obtener la tecla presionada en un evento de teclado?
- ¿Qué propiedades indican coordenadas del mouse?
- ¿Por qué no usar `keyCode`?

## Errores comunes

- Confundir `target` con `currentTarget`
- Olvidar `preventDefault()` cuando se necesita evitar comportamiento por defecto
- Usar `stopPropagation()` innecesariamente (puede romper funcionalidad de otros)
- Seguir usando `keyCode` en lugar de `key` o `code`
- No declarar el parámetro event en la función (aunque el navegador lo pasa igual)
- Memory leaks manteniendo referencias al evento en closures

## Mini-ejemplo (mental)

El objeto event es como **el parte de accidente policial**: reporte con detalles de qué pasó (tipo), dónde (coordenadas/target), quién estuvo involucrado (elementos), a qué hora (timestamp). Incluye "sellos" de control: `preventDefault()` detiene el tráfico en la escena, `stopPropagation()` evita que la noticia se propague.
