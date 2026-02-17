# Java - Tipos de datos

## Definición

Los tipos de datos en Java definen qué valores puede almacenar una variable y qué operaciones se pueden realizar con ella. Java es un lenguaje **fuertemente tipado**, lo que significa que cada variable debe declararse con un tipo específico.

## Explicación

- *Qué problema resuelve*
    Garantiza la integridad de los datos y permite detectar errores en tiempo de compilación. Al especificar tipos, el compilador puede verificar que las operaciones sean válidas y asignar la memoria adecuada.

- *Cómo funciona por arriba*
    - **Tipos primitivos**: Almacenan valores directamente en memoria (stack)
    - **Tipos de referencia**: Almacenan direcciones de memoria donde están los objetos (heap)
    - Cada tipo tiene un tamaño y rango específico
    - Java maneja automáticamente la conversión entre tipos compatibles

- *Qué implica / qué permite*
    - Seguridad de tipos en tiempo de compilación
    - Optimización de memoria según el tipo
    - Operaciones específicas para cada tipo de dato
    - Conversión entre tipos (casting)

## Categorías de tipos

En Java hay:
- **Primitivos** (valores directos): `int`, `double`, `boolean`, etc.
- **Referencia** (objetos): `String`, `Scanner`, arrays, clases propias, etc.

## Primitivos más usados (repaso)

| Tipo | Para qué se usa | Nota |
|---|---|---|
| `int` | enteros | por defecto para enteros |
| `long` | enteros grandes | literal con `L` |
| `double` | decimales | por defecto en decimales |
| `boolean` | verdadero/falso | `true` o `false` |
| `char` | un carácter | comillas simples `'A'` |

## Tipos de referencia

Ejemplos típicos: `String`, `Scanner`, `List`, `Map`, arrays (`int[]`), clases propias.

## Diferencias: Primitivos vs Referencia

| Característica | Primitivos | Referencia |
|----------------|------------|------------|
| **Qué guardan** | el valor | una referencia a un objeto |
| **Valor “vacío”** | 0/false/etc. | `null` |
| **Métodos** | no | sí |
| **Comparación con ==** | Compara valores | Compara referencias (direcciones) |

## Palabras clave

- Tipos primitivos
- Tipos de referencia
- byte, short, int, long
- float, double
- char, boolean
- String
- Casting
- Stack vs Heap

## Comparaciones típicas

- vs [[03 - Java - Sintaxis básica]]: los tipos de datos son los bloques de construcción de la sintaxis
- vs otros lenguajes: Java tiene tipos primitivos y wrappers; lenguajes como Python solo tienen tipos de referencia

## Preguntas de examen

- ¿Cuál es la diferencia entre tipos primitivos y tipos de referencia?
- ¿Cuántos bits ocupa un `int` y qué rango tiene?
- ¿Por qué usar `double` en lugar de `float`?
- ¿Qué valor por defecto tienen las variables primitivas vs las de referencia?
- ¿Dónde se almacenan los tipos primitivos (stack o heap)?

## Errores comunes

- Pensar que `String` es un tipo primitivo (es una clase/objeto)
- Comparar objetos con `==` en lugar de `.equals()`
- Olvidar que `char` usa comillas simples (`'A'`) y `String` usa dobles (`"A"`)

## Mini-ejemplo (mental)

Los tipos de datos son como **diferentes tamaños de cajas**: `byte` es una cajita pequeña para guardar solo números chicos (-128 a 127), `int` es una caja mediana estándar, y `long` es un contenedor gigante para números enormes. Cada caja tiene su etiqueta (tipo) y solo puedes guardar cosas que quepan en ella. Las cajas primitivas guardan el valor directamente; las de referencia guardan la dirección donde está el objeto real (como guardar la dirección de una bodega en lugar de la bodega misma).
