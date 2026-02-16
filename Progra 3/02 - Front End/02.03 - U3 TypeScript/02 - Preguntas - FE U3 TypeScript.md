# Preguntas - FE U3 TypeScript

## Introducción y flujo de compilación

- ¿Qué significa que TypeScript sea un “superconjunto” de JavaScript?
- ¿Por qué TypeScript no se ejecuta directamente en el navegador o Node?
- ¿Qué hace el compilador `tsc`?
- ¿Para qué sirve la opción `--noEmitOnError`?
- ¿Qué ventajas aporta TypeScript al IDE (autocompletado/errores tempranos)?

## Tipos básicos

- ¿Cuáles son los tipos primitivos básicos en TypeScript?
- ¿Qué dos sintaxis existen para tipar un array?
- ¿Qué diferencia hay entre anotación de tipo e inferencia?
- ¿Qué pasa si reasignás un valor de tipo distinto al inferido?
- ¿Qué es `any` y por qué se recomienda evitarlo?

## Funciones

- ¿Cómo se tipan los parámetros de una función?
- ¿Qué verifica TypeScript además del tipo (por ejemplo, cantidad de argumentos)?
- ¿Cómo se anota el tipo de retorno de una función?
- ¿Qué significa que una función retorne `void`?

## Tipos avanzados

- ¿Cómo se describe la forma de un objeto en TypeScript?
- ¿Cómo se declara una propiedad opcional y qué valor suele tener cuando falta?
- ¿Qué es un tipo de unión (`A | B`)?
- ¿Qué es el narrowing y cómo se logra (por ejemplo con `typeof`)?
- ¿Para qué sirve un alias de tipo (`type`)?
- ¿Para qué sirve una interface y qué ventaja aporta en un proyecto?
- ¿Cuál es una diferencia típica entre alias e interfaces?
- ¿Qué diferencia conceptual hay entre `null` y `undefined`?
- ¿Para qué sirve un `enum`?

## Clases y POO

- ¿Qué es una clase y qué es una instancia?
- ¿Qué visibilidad tiene un miembro sin modificador (public/private/protected)?
- ¿Cuál es la diferencia entre `private` y `protected`?
- ¿Cuándo se ejecuta el constructor?
- ¿Para qué sirve `this` dentro de métodos/constructores?
- ¿Para qué sirven getters y setters?
- ¿Qué significa heredar con `extends` y qué hace `super(...)`?
- ¿Qué significa que una clase “implemente” una interface (`implements`)?

## Módulos

- ¿Qué es un módulo y por qué ayuda a organizar un proyecto?
- ¿Cuál es la diferencia entre export nombrado y export default?
- ¿Cuál es la diferencia entre `import { x }` e `import x`?
- ¿Para qué sirve `import * as M from "..."`?
- ¿Qué significa exportar/importar tipos? ¿Por qué no existen en runtime?

## Decoradores y configuración

- ¿Qué es un decorador y a qué cosas se puede aplicar?
- ¿Por qué se considera una característica experimental?
- ¿Qué opción de `tsconfig` habilita decoradores?

## npm y proyecto

- ¿Qué es npm y para qué sirve en proyectos TypeScript?
- ¿Para qué sirve `package.json`?
- ¿Cuál es la diferencia entre `dependencies` y `devDependencies`?
- ¿Qué hace `npx` y por qué es útil con `tsc` local?
- ¿Qué comando crea un `tsconfig.json` base?
- ¿Qué hace `npx tsc -w`?

## Respuestas (opcional)

### ¿Qué es TypeScript?
Respuesta: Es un superconjunto de JavaScript que agrega tipado estático y se transpila a JS para ejecutarse. Ver: [[03 - TS - Introducción a TypeScript]]

### ¿Qué hace `tsc`?
Respuesta: Verifica tipos y transpila archivos `.ts` a `.js` (aplicando `tsconfig.json` si existe). Ver: [[03 - TS - Introducción a TypeScript]] y [[30 - TS - tsconfig.json]]

### ¿Qué es un tipo de unión?
Respuesta: Un tipo que permite más de una alternativa (ej: `number | string`) y requiere narrowing para usar operaciones específicas. Ver: [[12 - TS - Tipos de unión]]

### ¿Qué diferencia hay entre `dependencies` y `devDependencies`?
Respuesta: `dependencies` se necesita en producción; `devDependencies` solo para desarrollo/compilación (ej: TypeScript). Ver: [[33 - Node - package.json (por qué importa)]]

### ¿Para qué sirve `tsconfig.json`?
Respuesta: Centraliza y documenta la configuración de compilación (target, strict, outDir, etc.) para todo el proyecto. Ver: [[30 - TS - tsconfig.json]]

### ¿Qué diferencia hay entre `extends` e `implements`?
Respuesta: `extends` hereda implementación de una clase base; `implements` obliga a cumplir una interface. Ver: [[23 - TS - Herencia (extends)]] y [[24 - TS - Implementación de interfaces]]
