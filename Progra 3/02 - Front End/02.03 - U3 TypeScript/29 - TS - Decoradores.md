# TS - Decoradores

## Definición

Un decorador es una función especial que se aplica con `@...` a clases, métodos, propiedades o parámetros para alterar/extender comportamiento de forma declarativa.

## Explicación

- *Qué problema resuelve*
    Permite aplicar patrones transversales (logging, validación, metadatos) sin ensuciar la lógica principal repetida en muchos lugares.

- *Cómo funciona por arriba*
    - Se coloca `@Decorador` encima de la declaración a decorar
    - TypeScript llama al decorador con información sobre lo decorado
    - Son una característica experimental en TS (requieren configuración)

- *Qué implica / qué permite*
    - Meta-programación y APIs declarativas
    - Mayor “magia” implícita: conviene documentar y usar con moderación

## Tipos de decoradores (lista)

- Decoradores de clase (reciben el constructor)
- Decoradores de método (prototipo, nombre y descriptor)
- Decoradores de accesor (getter/setter)
- Decoradores de propiedad (prototipo y nombre)
- Decoradores de parámetro (función/método e índice)

## Ejemplo mínimo (clase)

```ts
function MostrarFechaCreacion(constructor: Function) {
  console.log("Fecha de creación:", new Date().toLocaleDateString());
}

@MostrarFechaCreacion
class Persona {
  constructor(public nombre: string, public edad: number) {}
}
```

## Configuración necesaria

Para usarlos, se habilita `experimentalDecorators` en `tsconfig.json`. Ver: [[30 - TS - tsconfig.json]]

## Palabras clave

- Decorador
- `@`
- `experimentalDecorators`
- Metadatos
- Meta-programación

## Comparaciones típicas

- vs [[30 - TS - tsconfig.json]]: sin configurar `experimentalDecorators`, el compilador no acepta la sintaxis.
- vs [[31 - TS - Comparación entre JavaScript y TypeScript]]: decoradores son una “sintaxis extra” de TS (no estándar JS final en muchos entornos).

## Preguntas de examen

- ¿Qué es un decorador en TypeScript?
- ¿A qué cosas se puede aplicar un decorador?
- ¿Qué opción de `tsconfig` habilita decoradores?
- ¿Por qué se considera una característica experimental?
- ¿Qué framework frontend usa decoradores intensivamente?

## Errores comunes

- Usar decoradores sin entender qué ejecuta y cuándo (pueden correr al cargar el módulo).
- Introducir lógica “oculta” sin documentación ni pruebas.

## Mini-ejemplo (mental)

Un decorador es como una etiqueta que le agrega comportamiento extra a una declaración sin tocar su cuerpo directamente.
