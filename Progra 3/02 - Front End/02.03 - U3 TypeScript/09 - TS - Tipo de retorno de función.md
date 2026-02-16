# TS - Tipo de retorno de función

## Definición

El tipo de retorno de una función se puede anotar con `: Tipo` después de los paréntesis, aunque TypeScript suele inferirlo.

## Explicación

- *Qué problema resuelve*
    Asegura que una función devuelva lo que promete y evita retornos inconsistentes.

- *Cómo funciona por arriba*
    - Anotación: `function f(): number { return 26; }`
    - Inferencia: si retornás un número, TS deduce `number`
    - Si no retornás nada, el retorno es `void`

- *Qué implica / qué permite*
    - “Contrato” claro para quien consume la función
    - Validación de `return` en todas las ramas

## Ejemplos comunes

```ts
function obtenerNumeroFavorito(): number {
  return 26;
}

function imprimir(msg: string): void {
  console.log(msg);
}
```

## Palabras clave

- Retorno
- `void`
- Inferencia
- Contrato

## Comparaciones típicas

- vs [[08 - TS - Parámetros de función]]: parámetros = entrada, retorno = salida.
- vs [[07 - TS - Anotaciones de tipo e inferencia]]: TS puede inferir retornos igual que variables.

## Preguntas de examen

- ¿Dónde se escribe el tipo de retorno de una función?
- ¿Qué significa que una función retorne `void`?
- ¿Por qué podría convenir anotar el retorno aunque TS lo infiera?

## Errores comunes

- Olvidar retornar en todas las ramas cuando se anotó un tipo no-void.
- Anotar retornos incorrectos y “pelear” con el compilador en vez de corregir la lógica.

## Mini-ejemplo (mental)

El tipo de retorno es como la etiqueta del “producto final” que promete una función.
