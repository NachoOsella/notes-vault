# TS - Tipo any

## Definición

`any` es un tipo especial que **desactiva** el chequeo de tipos para un valor: el compilador “confía” en vos y no verifica operaciones.

## Explicación

- *Qué problema resuelve*
    Facilita migraciones de JS a TS o casos puntuales donde el tipo es difícil de describir en el momento.

- *Cómo funciona por arriba*
    Si una variable es `any`, podés:
    - Asignarle cualquier valor
    - Llamar métodos que quizás no existen
    - Acceder propiedades sin verificación

- *Qué implica / qué permite*
    - Compila con menos fricción
    - Pero aumenta el riesgo de errores en runtime (perdés la seguridad de TS)

## Ejemplos comunes

```ts
let desconocido: any = "hola";
desconocido = 123;
desconocido.noExiste(); // TS no se queja, pero en runtime puede romper
```

## Palabras clave

- `any`
- Chequeo de tipos
- Runtime
- Migración gradual

## Comparaciones típicas

- vs [[07 - TS - Anotaciones de tipo e inferencia]]: si TS no puede inferir, puede caer en `any` implícito dependiendo de configuración.
- vs [[30 - TS - tsconfig.json]]: `noImplicitAny` ayuda a evitar `any` implícito.

## Preguntas de examen

- ¿Qué efecto tiene usar `any` en una variable?
- ¿Cuándo puede ser útil `any`?
- ¿Por qué se recomienda evitar `any`?
- ¿Qué opción ayuda a detectar `any` implícito?

## Errores comunes

- Usar `any` como solución general (termina siendo “JS sin beneficios”).
- Suponer que si compila entonces es seguro (con `any` puede fallar en ejecución).

## Mini-ejemplo (mental)

`any` es como desactivar el cinturón de seguridad: te deja moverte más rápido, pero te expone a más golpes.
