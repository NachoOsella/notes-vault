# TS - Export

## Definición

`export` se usa para exponer funciones, variables, clases o tipos desde un archivo (módulo) para que otros puedan importarlos.

## Explicación

- *Qué problema resuelve*
    Permite organizar el proyecto en módulos y controlar qué queda público y qué queda encapsulado.

- *Cómo funciona por arriba*
    - Exportación nombrada: `export const x = ...`
    - Exportación por lista: `export { a, b }`
    - Exportación default: `export default ...` (uno por módulo)

- *Qué implica / qué permite*
    - Código dividido en piezas más pequeñas
    - Dependencias claras entre archivos

## Ejemplos comunes

```ts
export function suma(a: number, b: number) {
  return a + b;
}
```

## Palabras clave

- Módulos
- `export`
- Named export
- Default export

## Comparaciones típicas

- vs [[26 - TS - Import]]: `export` expone; `import` consume.
- vs [[28 - TS - Export-Import de tipos]]: los tipos también se exportan, pero no existen en runtime.

## Preguntas de examen

- ¿Qué es un módulo en TypeScript/JavaScript moderno?
- ¿Qué diferencia hay entre export nombrado y default?
- ¿Para qué sirve `export { ... }`?

## Errores comunes

- Mezclar default y named exports sin un criterio claro.
- Exportar cosas internas que no deberían ser parte de la API del módulo.

## Mini-ejemplo (mental)

Exportar es “poner algo en la vidriera” del archivo para que otros lo puedan usar.
