# TS - Modificadores de acceso

## Definición

Los modificadores `public`, `private` y `protected` controlan la visibilidad de propiedades y métodos en una clase.

## Explicación

- *Qué problema resuelve*
    Permite encapsular detalles internos y exponer solo lo necesario, evitando uso incorrecto de la clase.

- *Cómo funciona por arriba*
    - `public`: accesible desde cualquier lugar (por defecto)
    - `private`: accesible solo dentro de la clase
    - `protected`: accesible dentro de la clase y sus subclases

- *Qué implica / qué permite*
    - Mejor diseño de APIs internas
    - Menos acoplamiento y menos “manoseo” del estado

## Ejemplos comunes

```ts
class Cuenta {
  public titular: string;
  private saldo: number;

  constructor(titular: string, saldo: number) {
    this.titular = titular;
    this.saldo = saldo;
  }
}
```

## Palabras clave

- `public`
- `private`
- `protected`
- Encapsulamiento

## Comparaciones típicas

- vs [[22 - TS - Getters y setters]]: getters/setters son una forma controlada de exponer datos.
- vs [[23 - TS - Herencia (extends)]]: `protected` cobra sentido cuando hay herencia.

## Preguntas de examen

- ¿Qué diferencia hay entre `private` y `protected`?
- ¿Qué visibilidad tiene un miembro sin modificador en TS?
- ¿Por qué usar encapsulamiento?

## Errores comunes

- Poner todo `public` por defecto y perder control.
- Exponer estado que debería ser interno y luego depender de él desde afuera.

## Mini-ejemplo (mental)

`private` es como una caja fuerte: solo se abre desde adentro. `protected` es una caja que también pueden abrir “los hijos” (subclases).
