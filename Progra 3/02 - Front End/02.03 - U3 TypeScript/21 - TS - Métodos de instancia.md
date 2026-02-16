# TS - Métodos de instancia

## Definición

Los métodos de instancia son funciones definidas en una clase que operan sobre los datos de cada objeto (usando `this`).

## Explicación

- *Qué problema resuelve*
    Organiza el comportamiento asociado a una entidad junto con sus datos.

- *Cómo funciona por arriba*
    - Se definen dentro de la clase
    - Se invocan sobre una instancia: `obj.metodo()`
    - Acceden a propiedades con `this`

- *Qué implica / qué permite*
    - Encapsular lógica en el objeto
    - Reutilizar comportamiento en muchas instancias

## Ejemplos comunes

```ts
class Contador {
  valor: number = 0;

  incrementar() {
    this.valor++;
  }
}
```

## Palabras clave

- Método
- Instancia
- `this`
- Comportamiento

## Comparaciones típicas

- vs [[22 - TS - Getters y setters]]: getters/setters son métodos especiales para acceder/modificar propiedades.
- vs [[19 - TS - Modificadores de acceso]]: métodos también pueden ser public/private/protected.

## Preguntas de examen

- ¿Qué es un método de instancia?
- ¿Cómo se invoca un método de instancia?
- ¿Para qué sirve `this` en un método?

## Errores comunes

- Perder el contexto de `this` al pasar métodos como callbacks sin bind.

## Mini-ejemplo (mental)

Un método de instancia es una acción que puede hacer cada objeto, como “incrementar” en un contador.
