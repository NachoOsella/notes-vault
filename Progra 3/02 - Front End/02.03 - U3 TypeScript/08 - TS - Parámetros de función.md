# TS - Parámetros de función

## Definición

TypeScript permite tipar los **parámetros** de una función para garantizar que se la llame con argumentos del tipo correcto.

## Explicación

- *Qué problema resuelve*
    Evita llamadas incorrectas (por ejemplo, pasar un número donde se esperaba un string).

- *Cómo funciona por arriba*
    - Se anota cada parámetro: `function saludar(nombre: string) { ... }`
    - TS verifica el tipo y también la cantidad de argumentos

- *Qué implica / qué permite*
    - Menos errores al usar métodos propios del tipo (ej: `toUpperCase()` en strings)
    - Firma de función más clara para quien la usa

## Ejemplos comunes

```ts
function saludar(nombre: string) {
  console.log(nombre.toUpperCase());
}
```

## Palabras clave

- Parámetros
- Firma
- Anotación
- Argumentos

## Comparaciones típicas

- vs [[09 - TS - Tipo de retorno de función]]: parámetros son entrada; retorno es salida.
- vs [[12 - TS - Tipos de unión]]: un parámetro puede aceptar más de un tipo con uniones.

## Preguntas de examen

- ¿Cómo se tipa un parámetro en TypeScript?
- ¿Qué verifica TS además del tipo (en llamadas a funciones)?
- ¿Por qué ayuda tipar parámetros en tiempo de compilación?

## Errores comunes

- Tipar parámetros como `any` por comodidad. Ver: [[06 - TS - Tipo any]]
- No considerar que una función puede ser llamada con menos argumentos (TS lo advierte).

## Mini-ejemplo (mental)

Tipar parámetros es como poner el formato exacto en un formulario: si te piden “string”, no podés mandar “number”.
