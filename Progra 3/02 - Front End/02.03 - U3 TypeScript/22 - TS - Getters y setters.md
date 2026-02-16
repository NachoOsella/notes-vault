# TS - Getters y setters

## Definición

Getters (`get`) y setters (`set`) son métodos especiales para leer o modificar una propiedad de forma controlada.

## Explicación

- *Qué problema resuelve*
    Permiten validar o transformar datos al acceder/modificar, sin exponer el estado interno directamente.

- *Cómo funciona por arriba*
    - Getter: se usa como propiedad de lectura
    - Setter: se asigna como propiedad, pero ejecuta lógica

- *Qué implica / qué permite*
    - Encapsulamiento más fuerte
    - Validaciones (ej: no permitir valores negativos)

## Ejemplos comunes

```ts
class Temperatura {
  private _c: number = 0;

  get celsius() {
    return this._c;
  }

  set celsius(v: number) {
    if (v < -273.15) throw new Error("Valor inválido");
    this._c = v;
  }
}
```

## Palabras clave

- `get`
- `set`
- Encapsulamiento
- Validación

## Comparaciones típicas

- vs [[19 - TS - Modificadores de acceso]]: suelen combinarse con `private` para proteger el estado interno.
- vs [[21 - TS - Métodos de instancia]]: son métodos, pero con sintaxis de propiedad.

## Preguntas de examen

- ¿Para qué sirven getters y setters?
- ¿Qué ventaja tienen sobre exponer un campo público?
- ¿Cómo se define un getter? ¿y un setter?

## Errores comunes

- Poner lógica pesada en getters (puede sorprender al leer).
- No validar en setters y permitir estados inválidos.

## Mini-ejemplo (mental)

Un getter/setter es como una ventanilla: no entrás al depósito (estado interno), pedís lo que necesitás y te lo entregan validado.
