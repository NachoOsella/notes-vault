# TS - Tipos de objetos

## Definición

TypeScript permite describir la **forma** de un objeto indicando sus propiedades y tipos (tipado estructural).

## Explicación

- *Qué problema resuelve*
    Evita pasar objetos incompletos o con propiedades de tipo incorrecto.

- *Cómo funciona por arriba*
    - Podés tipar un objeto “en línea” con un literal:
      `{ x: number; y: number }`
    - TS valida que el objeto tenga esas propiedades con esos tipos

- *Qué implica / qué permite*
    - Firmas más claras en funciones que reciben objetos
    - Mejor autocompletado de propiedades

## Ejemplos comunes

```ts
function imprimirCoordenadas(p: { x: number; y: number }) {
  console.log(p.x, p.y);
}

imprimirCoordenadas({ x: 3, y: 7 });
```

## Palabras clave

- Tipo de objeto
- Propiedades
- Tipado estructural
- Literal

## Comparaciones típicas

- vs [[14 - TS - Interfaces]]: interfaces nombran formas de objetos para reutilizarlas.
- vs [[13 - TS - Alias de tipo]]: alias también puede nombrar un tipo de objeto complejo.

## Preguntas de examen

- ¿Cómo se describe la forma de un objeto en TypeScript?
- ¿Qué pasa si falta una propiedad requerida?
- ¿Por qué es útil tipar objetos en funciones?

## Errores comunes

- Confundir “forma” con “clase”: en TS importa la estructura, no la clase concreta.
- No contemplar propiedades opcionales cuando el objeto no siempre las trae. Ver: [[11 - TS - Propiedades opcionales]]

## Mini-ejemplo (mental)

Tipar un objeto es como decir “este paquete tiene que traer exactamente estas cosas adentro”.
