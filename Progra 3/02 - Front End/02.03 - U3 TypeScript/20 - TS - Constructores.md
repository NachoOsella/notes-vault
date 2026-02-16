# TS - Constructores

## Definición

El constructor (`constructor(...)`) es el método especial que inicializa una instancia cuando se crea con `new`.

## Explicación

- *Qué problema resuelve*
    Garantiza que el objeto nazca en un estado válido inicializando propiedades obligatorias.

- *Cómo funciona por arriba*
    - Se ejecuta automáticamente al hacer `new`
    - Recibe parámetros para inicializar propiedades
    - Usa `this` para asignar al objeto actual

- *Qué implica / qué permite*
    - Inicialización centralizada
    - Validaciones o normalizaciones básicas al crear el objeto

## Ejemplos comunes

```ts
class Producto {
  nombre: string;

  constructor(nombre: string) {
    this.nombre = nombre;
  }
}
```

## Palabras clave

- `constructor`
- Inicialización
- `this`
- Instancia

## Comparaciones típicas

- vs [[18 - TS - Clases (definición y propiedades)]]: el constructor es parte clave de la definición de clase.
- vs [[23 - TS - Herencia (extends)]]: en herencia se usa `super(...)` para inicializar la clase base.

## Preguntas de examen

- ¿Cuándo se ejecuta un constructor?
- ¿Para qué sirve `this` dentro del constructor?
- ¿Qué pasa si no definís constructor?

## Errores comunes

- Olvidar inicializar propiedades usadas luego.
- Confundir parámetros del constructor con propiedades (hay que asignarlas).

## Mini-ejemplo (mental)

El constructor es como el “momento de armado” de un mueble: definís piezas iniciales para que funcione.
