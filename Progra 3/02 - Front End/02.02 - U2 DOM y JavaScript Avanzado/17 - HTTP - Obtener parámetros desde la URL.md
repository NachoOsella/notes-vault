# HTTP - Obtener parámetros desde la URL

## Definición

Los query params son pares `clave=valor` que viajan en la URL después de `?`.

## Explicación

- *Qué problema resuelve*
    Permite compartir estado simple (filtros, búsqueda, paginación) sin guardar datos en storage.

- *Cómo funciona por arriba*
    - Formato: `?a=1&b=2`
    - En JS se leen con `URLSearchParams`
    - Son visibles para el usuario

- *Qué implica / qué permite*
    - URLs compartibles con estado
    - Mejor navegación (atrás/adelante)
    - No usar para datos sensibles

## API útil (`URLSearchParams`)

- `get('clave')`
- `has('clave')`
- `getAll('clave')`
- `set('clave', 'valor')`
- `delete('clave')`
- `toString()`

## Mini-flujo

```mermaid
%%{init: {'theme': 'base', 'themeVariables': { 'primaryColor': '#1d2021', 'primaryTextColor': '#ebdbb2', 'primaryBorderColor': '#928374', 'lineColor': '#a89984', 'secondaryColor': '#282828', 'tertiaryColor': '#3c3836'}}}%%
flowchart LR
    A[window.location.search] --> B[URLSearchParams]
    B --> C[get/set params]
    C --> D[URL final]
```

## Palabras clave

- Query string
- URLSearchParams
- GET
- `encodeURIComponent`
- Estado en URL

## Comparaciones típicas

- vs [[13 - Storage - localStorage]]: URL params son visibles y orientados a navegación; localStorage es interno del navegador
- vs [[12 - HTTP - Body]]: query params son cortos/visibles; body se usa para datos más grandes

## Preguntas de examen

- ¿Cómo se leen parámetros de URL en JS moderno?
- ¿Cuándo conviene pasar estado en URL?
- ¿Por qué no se deben enviar datos sensibles por query params?

## Errores comunes

- No codificar valores con caracteres especiales
- Asumir que un parámetro existe sin validar
- Poner tokens/contraseñas en la URL

## Mini-ejemplo (mental)

Es como enviar una carpeta con etiquetas pegadas afuera: todos ven esas etiquetas y se puede compartir exactamente esa vista.
