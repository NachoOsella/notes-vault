# TS - Propiedades opcionales

## Definición

Una propiedad opcional se marca con `?` (por ejemplo `apellido?: string`) indicando que puede estar presente o no.

## Explicación

- *Qué problema resuelve*
    Modela objetos donde ciertos datos no siempre existen (formularios, APIs, etc.).

- *Cómo funciona por arriba*
    - Se define con `?`
    - Dentro del código suele requerir chequeo antes de usar (para evitar `undefined`)

- *Qué implica / qué permite*
    - Llamar funciones con objetos parciales sin romper el tipado
    - Obliga a tratar el caso “no viene” de forma segura

## Ejemplos comunes

```ts
function imprimirNombre(p: { nombre: string; apellido?: string }) {
  if (p.apellido !== undefined) {
    console.log(p.nombre, p.apellido);
  } else {
    console.log(p.nombre);
  }
}
```

## Palabras clave

- Opcional `?`
- `undefined`
- Chequeo
- Forma de objeto

## Comparaciones típicas

- vs [[16 - TS - null y undefined]]: lo opcional suele terminar siendo `undefined` cuando falta.
- vs [[10 - TS - Tipos de objetos]]: agrega flexibilidad en propiedades.

## Preguntas de examen

- ¿Cómo se declara una propiedad opcional?
- ¿Por qué hay que chequear si existe antes de usarla?
- ¿Qué valor suele tener una propiedad opcional ausente?

## Errores comunes

- Usar una propiedad opcional como si siempre existiera (termina en `undefined`).
- Hacer opcional algo que en realidad es obligatorio (pierde expresividad).

## Mini-ejemplo (mental)

Una propiedad opcional es como “segundo nombre”: a veces está, a veces no.
