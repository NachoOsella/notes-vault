# TS - Implementación de interfaces

## Definición

`implements` permite que una clase declare que cumple una o más interfaces (contratos de forma).

## Explicación

- *Qué problema resuelve*
    Asegura que distintas clases expongan el mismo conjunto de miembros, facilitando polimorfismo y consistencia.

- *Cómo funciona por arriba*
    - `class X implements I { ... }`
    - TS verifica que la clase tenga las propiedades/métodos requeridos por la interface

- *Qué implica / qué permite*
    - Diseñar APIs basadas en contratos
    - Intercambiar implementaciones sin cambiar el código consumidor

## Ejemplos comunes

```ts
interface Serializa {
  toJSON(): string;
}

class Usuario implements Serializa {
  constructor(public nombre: string) {}
  toJSON() {
    return JSON.stringify({ nombre: this.nombre });
  }
}
```

## Palabras clave

- `implements`
- Contrato
- Interface
- Consistencia

## Comparaciones típicas

- vs [[23 - TS - Herencia (extends)]]: `implements` no hereda implementación, solo exige forma.
- vs [[14 - TS - Interfaces]]: `implements` aplica a interfaces.

## Preguntas de examen

- ¿Qué significa que una clase “implemente” una interface?
- ¿Qué verifica TypeScript cuando usás `implements`?
- ¿Puede una clase implementar más de una interface?

## Errores comunes

- Confundir `implements` con `extends`.
- Declarar una interface y luego no usarla en ningún lado (pierde valor).

## Mini-ejemplo (mental)

Una interface es una lista de requisitos; `implements` es decir “mi clase cumple esta lista”.
