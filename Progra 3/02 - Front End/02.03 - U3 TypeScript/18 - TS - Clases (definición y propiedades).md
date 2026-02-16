# TS - Clases (definición y propiedades)

## Definición

Una clase en TypeScript es una plantilla para crear objetos con **propiedades** y **métodos**, usando sintaxis de POO similar a otros lenguajes.

## Explicación

- *Qué problema resuelve*
    Permite modelar entidades con estado y comportamiento, organizando el código en objetos.

- *Cómo funciona por arriba*
    - Se define con `class`
    - Las propiedades se declaran en la clase
    - Se instancia con `new`

- *Qué implica / qué permite*
    - Encapsular datos y comportamiento
    - Usar herencia e interfaces en TS

## Ejemplos comunes

```ts
class Persona {
  nombre: string;
  edad: number;

  constructor(nombre: string, edad: number) {
    this.nombre = nombre;
    this.edad = edad;
  }
}
```

## Palabras clave

- `class`
- Propiedades
- Instancia
- `new`
- `this`

## Comparaciones típicas

- vs [[23 - TS - Herencia (extends)]]: `extends` permite reutilizar y especializar clases.
- vs [[24 - TS - Implementación de interfaces]]: `implements` obliga a cumplir un contrato de forma.

## Preguntas de examen

- ¿Qué es una clase y para qué se usa?
- ¿Cómo se definen propiedades en una clase TS?
- ¿Qué significa instanciar con `new`?

## Errores comunes

- No inicializar propiedades antes de usarlas.
- Confundir clase (definición) con objeto (instancia).

## Mini-ejemplo (mental)

Una clase es como el plano de una casa; la instancia es la casa construida.
