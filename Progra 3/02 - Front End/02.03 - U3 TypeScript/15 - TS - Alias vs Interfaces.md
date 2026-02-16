# TS - Alias vs Interfaces

## Definición

`type` (alias) e `interface` sirven para describir tipos, especialmente objetos, pero tienen diferencias de uso y alcance.

## Explicación

- *Qué problema resuelve*
    Ayuda a elegir la herramienta correcta para modelar datos con claridad y extensibilidad.

- *Cómo funciona por arriba*
    - `type` puede nombrar primitivos, uniones y objetos
    - `interface` se usa principalmente para describir objetos y extender estructuras

- *Qué implica / qué permite*
    - Mejor consistencia en el modelado de datos del proyecto
    - Decisiones más claras cuando el dominio crece

## Diferencias típicas

| Caso | Mejor opción | Por qué |
|---|---|---|
| Unión (`A | B`) | `type` | interface no modela uniones directamente |
| Primitivo | `type` | alias directo (`type ID = string`) |
| Objeto extendible | `interface` | suele leerse mejor para “modelos” |
| Objeto simple reutilizable | cualquiera | depende del estilo del proyecto |

## Palabras clave

- `type`
- `interface`
- Unión
- Extensibilidad

## Comparaciones típicas

- vs [[13 - TS - Alias de tipo]]: esta nota define `type` en sí.
- vs [[14 - TS - Interfaces]]: esta nota define `interface` en sí.

## Preguntas de examen

- ¿Qué puede modelar `type` que `interface` no?
- ¿Cuándo conviene usar `interface`?
- ¿Por qué es útil tener un criterio consistente en el proyecto?

## Errores comunes

- Elegir al azar y mezclar sin criterio en el mismo módulo.
- Usar `interface` cuando en realidad necesitabas una unión.

## Mini-ejemplo (mental)

`type` es una etiqueta general para “cualquier tipo”. `interface` es más como un “contrato de forma” para objetos.
