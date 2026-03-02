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

### ¿Qué significa que TypeScript sea un “superconjunto” de JavaScript?
Respuesta: Que todo JavaScript válido también es TypeScript, y además TS agrega tipos y herramientas de análisis estático.

### ¿Por qué TypeScript no se ejecuta directamente en el navegador o Node?
Respuesta: Porque navegadores y Node ejecutan JavaScript; TypeScript primero debe transpilarse a `.js`.

### ¿Qué hace el compilador `tsc`?
Respuesta: Verifica tipos y transpila archivos `.ts` a `.js` según la configuración del proyecto.

### ¿Para qué sirve la opción `--noEmitOnError`?
Respuesta: Evita generar archivos `.js` si hay errores de tipos, para no compilar código inválido.

### ¿Qué ventajas aporta TypeScript al IDE (autocompletado/errores tempranos)?
Respuesta: Mejora autocompletado, navegación y detección temprana de errores antes de ejecutar.

### ¿Cuáles son los tipos primitivos básicos en TypeScript?
Respuesta: `string`, `number`, `boolean`, `null`, `undefined`, `bigint` y `symbol`.

### ¿Qué dos sintaxis existen para tipar un array?
Respuesta: `Tipo[]` (por ejemplo `number[]`) y `Array<Tipo>` (por ejemplo `Array<number>`).

### ¿Qué diferencia hay entre anotación de tipo e inferencia?
Respuesta: En anotación declarás el tipo explícitamente; en inferencia TypeScript lo deduce por el valor.

### ¿Qué pasa si reasignás un valor de tipo distinto al inferido?
Respuesta: TypeScript marca error de tipo, salvo que uses `any` o un tipo compatible.

### ¿Qué es `any` y por qué se recomienda evitarlo?
Respuesta: Es un tipo que desactiva chequeos de tipos; se evita porque pierde seguridad y autoguía del IDE.

### ¿Cómo se tipan los parámetros de una función?
Respuesta: Indicando `nombre: tipo` en cada parámetro, por ejemplo `function f(x: number)`.

### ¿Qué verifica TypeScript además del tipo (por ejemplo, cantidad de argumentos)?
Respuesta: Controla aridad, opcionales, parámetros por defecto y compatibilidad de firmas.

### ¿Cómo se anota el tipo de retorno de una función?
Respuesta: Se agrega después de los paréntesis: `function f(): string { ... }`.

### ¿Qué significa que una función retorne `void`?
Respuesta: Que la función no devuelve un valor útil; solo ejecuta una acción.

### ¿Cómo se describe la forma de un objeto en TypeScript?
Respuesta: Con un tipo literal de objeto, un `type` o una `interface` que define sus propiedades.

### ¿Cómo se declara una propiedad opcional y qué valor suele tener cuando falta?
Respuesta: Se usa `?` (`prop?: tipo`); si no está presente, su valor es `undefined`.

### ¿Qué es un tipo de unión (`A | B`)?
Respuesta: Un tipo que acepta varias alternativas, como `string | number`, según el valor en runtime.

### ¿Qué es el narrowing y cómo se logra (por ejemplo con `typeof`)?
Respuesta: Es refinar un tipo unión a uno más específico usando guardas como `typeof`, `in` o `instanceof`.

### ¿Para qué sirve un alias de tipo (`type`)?
Respuesta: Para nombrar tipos complejos y reutilizarlos de forma clara en varias partes del código.

### ¿Para qué sirve una interface y qué ventaja aporta en un proyecto?
Respuesta: Define contratos de forma de objetos/clases; mejora consistencia y mantenibilidad del código.

### ¿Cuál es una diferencia típica entre alias e interfaces?
Respuesta: `interface` se puede fusionar por declaración; `type` es más flexible para uniones e intersecciones.

### ¿Qué diferencia conceptual hay entre `null` y `undefined`?
Respuesta: `undefined` suele significar “no definido/no asignado”; `null`, “ausencia intencional de valor”.

### ¿Para qué sirve un `enum`?
Respuesta: Para agrupar constantes con nombres semánticos y evitar “valores mágicos” sueltos.

### ¿Qué es una clase y qué es una instancia?
Respuesta: La clase es el molde; la instancia es un objeto concreto creado con `new`.

### ¿Qué visibilidad tiene un miembro sin modificador (public/private/protected)?
Respuesta: Por defecto es `public`, accesible desde cualquier parte donde se vea la instancia.

### ¿Cuál es la diferencia entre `private` y `protected`?
Respuesta: `private` solo dentro de la clase; `protected` también permite acceso desde clases hijas.

### ¿Cuándo se ejecuta el constructor?
Respuesta: Al crear una instancia con `new`, antes de usar el objeto.

### ¿Para qué sirve `this` dentro de métodos/constructores?
Respuesta: Referencia a la instancia actual para leer o modificar sus propiedades y métodos.

### ¿Para qué sirven getters y setters?
Respuesta: Permiten controlar lectura/escritura de propiedades, validando o transformando valores.

### ¿Qué significa heredar con `extends` y qué hace `super(...)`?
Respuesta: `extends` crea una subclase con comportamiento de la base; `super(...)` llama al constructor padre.

### ¿Qué significa que una clase “implemente” una interface (`implements`)?
Respuesta: Que la clase debe cumplir todas las propiedades y métodos definidos por ese contrato.

### ¿Qué es un módulo y por qué ayuda a organizar un proyecto?
Respuesta: Es un archivo con su propio scope y exports/imports; separa responsabilidades y evita acoplamiento.

### ¿Cuál es la diferencia entre export nombrado y export default?
Respuesta: Nombrado exporta varios miembros con nombre; `default` exporta uno principal sin llaves al importar.

### ¿Cuál es la diferencia entre `import { x }` e `import x`?
Respuesta: `import { x }` trae un export nombrado; `import x` trae el `default` exportado.

### ¿Para qué sirve `import * as M from "..."`?
Respuesta: Importa todo el módulo en un objeto namespace (`M`) para acceder como `M.algo`.

### ¿Qué significa exportar/importar tipos? ¿Por qué no existen en runtime?
Respuesta: Son contratos para compilación; TypeScript los elimina al transpilar, por eso no están en runtime.

### ¿Qué es un decorador y a qué cosas se puede aplicar?
Respuesta: Es una función/metadato que anota o modifica comportamiento de clases, métodos, propiedades o parámetros.

### ¿Por qué se considera una característica experimental?
Respuesta: Porque su especificación no estuvo totalmente estabilizada y puede tener cambios entre versiones.

### ¿Qué opción de `tsconfig` habilita decoradores?
Respuesta: `experimentalDecorators: true` en `compilerOptions`.

### ¿Qué es npm y para qué sirve en proyectos TypeScript?
Respuesta: Es el gestor de paquetes de Node; instala dependencias y ejecuta scripts del proyecto.

### ¿Para qué sirve `package.json`?
Respuesta: Define metadatos, scripts y dependencias, y funciona como manifiesto del proyecto.

### ¿Cuál es la diferencia entre `dependencies` y `devDependencies`?
Respuesta: `dependencies` se usan en ejecución; `devDependencies` en desarrollo/build/testing.

### ¿Qué hace `npx` y por qué es útil con `tsc` local?
Respuesta: Ejecuta binarios de paquetes sin instalación global; permite usar el `tsc` de la versión del proyecto.

### ¿Qué comando crea un `tsconfig.json` base?
Respuesta: `npx tsc --init`.

### ¿Qué hace `npx tsc -w`?
Respuesta: Activa modo watch: recompila automáticamente al detectar cambios en archivos TypeScript.
