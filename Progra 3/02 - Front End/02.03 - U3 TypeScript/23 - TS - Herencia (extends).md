# TS - Herencia (extends)

## Definición

La herencia permite crear una clase hija que reutiliza y extiende una clase base usando `extends`.

## Explicación

- *Qué problema resuelve*
    Evita duplicación cuando varias clases comparten comportamiento y estructura.

- *Cómo funciona por arriba*
    - `class Hija extends Base { ... }`
    - Se puede sobreescribir (override) métodos
    - Se usa `super(...)` para inicializar la clase base en el constructor

- *Qué implica / qué permite*
    - Reutilización y especialización
    - Polimorfismo (tratar una hija como base)

## Ejemplos comunes

```ts
class Animal {
  hablar() {
    console.log("...");
  }
}

class Perro extends Animal {
  hablar() {
    console.log("guau");
  }
}
```

## Palabras clave

- `extends`
- `super`
- Clase base
- Subclase
- Override

## Comparaciones típicas

- vs [[24 - TS - Implementación de interfaces]]: `extends` hereda implementación; `implements` solo obliga a cumplir un contrato.
- vs [[19 - TS - Modificadores de acceso]]: `protected` se usa mucho con herencia.

## Preguntas de examen

- ¿Para qué sirve `extends`?
- ¿Qué hace `super(...)` en un constructor?
- ¿Qué es sobreescritura de métodos?

## Errores comunes

- Abusar de herencia cuando composición sería más simple.
- Olvidar llamar `super(...)` cuando la clase base lo requiere.

## Mini-ejemplo (mental)

Herencia es como partir de un modelo base de auto y crear versiones “deportiva” o “familiar” agregando cambios.
