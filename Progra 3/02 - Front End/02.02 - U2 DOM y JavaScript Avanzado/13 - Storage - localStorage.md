# Storage - localStorage

## Definición

`localStorage` guarda datos en el navegador de forma persistente (hasta que se borren manualmente).

## Explicación

- *Qué problema resuelve*
    Mantiene estado del lado cliente sin depender de cookies o backend para datos simples.

- *Cómo funciona por arriba*
    - API: `window.localStorage`
    - Guarda pares clave-valor como texto
    - Es por origen (dominio/protocolo/puerto)
    - Se comparte entre pestañas del mismo origen

- *Qué implica / qué permite*
    - Persistencia entre sesiones
    - Preferencias y caché local simple
    - No apto para datos sensibles

## API básica

- `setItem(clave, valor)`
- `getItem(clave)`
- `removeItem(clave)`
- `clear()`
- `length`

## Datos complejos

```mermaid
%%{init: {'theme': 'base', 'themeVariables': { 'darkMode': true, 'background': '#1d2021', 'primaryColor': '#3c3836', 'primaryTextColor': '#ffffff', 'primaryBorderColor': '#bdae93', 'secondaryColor': '#504945', 'secondaryTextColor': '#ffffff', 'secondaryBorderColor': '#bdae93', 'tertiaryColor': '#282828', 'tertiaryTextColor': '#ffffff', 'tertiaryBorderColor': '#a89984', 'lineColor': '#d5c4a1', 'textColor': '#ffffff', 'mainBkg': '#282828', 'nodeBkg': '#3c3836', 'nodeTextColor': '#ffffff', 'nodeBorder': '#bdae93', 'clusterBkg': '#282828', 'clusterBorder': '#a89984', 'defaultLinkColor': '#d5c4a1', 'titleColor': '#ffffff', 'edgeLabelBackground': '#282828', 'labelBoxBkgColor': '#3c3836', 'labelBoxBorderColor': '#bdae93', 'labelTextColor': '#ffffff', 'loopTextColor': '#ffffff', 'noteBkgColor': '#282828', 'noteTextColor': '#ffffff', 'noteBorderColor': '#83a598', 'actorBkg': '#3c3836', 'actorBorder': '#bdae93', 'actorTextColor': '#ffffff', 'actorLineColor': '#d5c4a1', 'signalColor': '#d5c4a1', 'signalTextColor': '#ffffff', 'activationBkgColor': '#689d6a', 'activationBorderColor': '#8ec07c', 'sequenceNumberColor': '#ffffff'}, 'themeCSS': 'text, tspan { fill: #ffffff !important; color: #ffffff !important; } .messageText, .labelText, .loopText, .noteText, .actor text, .taskText, .sectionTitle text, .nodeLabel, .edgeLabel, .cluster-label text { fill: #ffffff !important; color: #ffffff !important; } .messageLine0, .messageLine1, .actor-line, .edgePath .path { stroke: #d5c4a1 !important; } .note { fill: #282828 !important; stroke: #83a598 !important; } .labelBox, .edgeLabel rect { fill: #3c3836 !important; stroke: #bdae93 !important; }'}}%%
flowchart LR
    A[Objeto JS] -->|JSON.stringify| B[String]
    B -->|setItem/getItem| C[localStorage]
    C -->|JSON.parse| A
```

## Palabras clave

- localStorage
- Persistencia
- Web Storage
- JSON.stringify
- JSON.parse
- Origen

## Comparaciones típicas

- vs [[14 - Storage - sessionStorage]]: localStorage persiste y se comparte entre pestañas
- vs [[15 - Cookies - Crear y usar cookies en JS]]: localStorage no se envía automáticamente al servidor

## Preguntas de examen

- ¿Qué diferencia clave hay entre localStorage y sessionStorage?
- ¿Por qué hay que serializar objetos con JSON?
- ¿Por qué no conviene guardar tokens sensibles en localStorage?

## Errores comunes

- Guardar objetos sin serializar
- Guardar información sensible
- Asumir que `getItem` devuelve `undefined` (devuelve `null` si no existe)

## Mini-ejemplo (mental)

Es como un cajón que queda en tu escritorio aunque cierres la oficina: sigue ahí la próxima vez.
