# TS - Interfaces

## Definición

Una `interface` describe la **forma** de un objeto: qué propiedades tiene y de qué tipo son.

## Explicación

- *Qué problema resuelve*
    Estandariza estructuras de datos (por ejemplo, objetos que vienen de una API) y mejora la comunicación entre partes del código.

- *Cómo funciona por arriba*
    - Se define con `interface Nombre { ... }`
    - Un objeto es compatible si “tiene esa forma” (tipado estructural)

- *Qué implica / qué permite*
    - Reutilizar tipos de objetos en muchos lugares
    - Extender interfaces para construir modelos más grandes

## Ejemplos comunes

```ts
interface Usuario {
  id: number;
  nombre: string;
}

function imprimirUsuario(u: Usuario) {
  console.log(u.id, u.nombre);
}
```

## Palabras clave

- `interface`
- Forma
- Propiedades
- Tipado estructural

## Comparaciones típicas

- vs [[13 - TS - Alias de tipo]]: ambas describen objetos, pero `interface` está orientada a estructuras extensibles.
- vs [[23 - TS - Implementación de interfaces]]: `implements` en clases obliga a cumplir la forma de la interface.

## Preguntas de examen

- ¿Qué es una interface y para qué se usa?
- ¿Qué significa que TS sea “estructural”?
- ¿Cómo ayuda una interface en mantenibilidad?

## Errores comunes

- Confundir interface con clase: una interface no genera código en runtime, solo sirve para tipos.
- Definir interfaces demasiado grandes (difíciles de reutilizar).

## Mini-ejemplo (mental)

Una interface es como un “molde de propiedades”: no crea objetos, solo define cómo deben verse.
