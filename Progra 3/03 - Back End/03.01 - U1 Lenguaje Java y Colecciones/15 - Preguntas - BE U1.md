# Preguntas - BE U1

## Introducción a Java

- ¿Qué significa que Java sea "portable" y cómo lo logra?
- ¿Qué es el bytecode y qué ventaja tiene sobre el código máquina?
- ¿Cuáles son los cuatro pilares de la Programación Orientada a Objetos?
- ¿Qué es la JVM y cuál es su función principal?
- ¿Qué significa WORA (Write Once, Run Anywhere)?

## JDK y JVM

- ¿Cuál es la diferencia entre JDK, JRE y JVM?
- ¿Qué componente convierte archivos .java a .class?
- ¿Qué es el JIT Compiler y para qué sirve?
- ¿Qué hace el Garbage Collector?
- ¿Para qué sirve el Bytecode Verifier?

## Sintaxis Básica

- ¿Cuál es el método de entrada (punto de inicio) de un programa Java?
- ¿Por qué el nombre del archivo debe coincidir con la clase pública?
- ¿Qué diferencia hay entre CamelCase y camelCase?
- ¿Cuándo usar `//` vs `/* */` vs `/** */`?
- ¿Java distingue mayúsculas de minúsculas?

## Tipos de Datos

- ¿Cuál es la diferencia entre tipos primitivos y tipos de referencia?
- ¿Cuántos bits ocupa un `int` y qué rango tiene?
- ¿Por qué usar `double` en lugar de `float`?
- ¿Qué valor por defecto tienen las variables primitivas vs las de referencia?
- ¿Dónde se almacenan los tipos primitivos (stack o heap)?

## Variables y Ámbito

- ¿Cuál es la diferencia entre variable de instancia y variable local?
- ¿Las variables locales se inicializan automáticamente?
- ¿Qué tipo de variable se comparte entre todas las instancias de una clase?
- ¿Cuál es el ámbito de una variable declarada dentro de un bucle `for`?
- ¿Cuándo se destruye una variable local?

## Operadores

- ¿Cuál es la diferencia entre `=` y `==`?
- ¿Qué hace el operador `%` (módulo)?
- ¿Qué es el cortocircuito en operadores lógicos?
- ¿Cuál es la precedencia: `&&` o `||`?
- ¿Qué diferencia hay entre `++x` y `x++`?

## Estructuras de Control

- ¿Cuál es la diferencia entre `while` y `do-while`?
- ¿Qué hace `break` en un switch?
- ¿Cuándo es más apropiado usar `for-each`?
- ¿Qué es el "fall-through" en un switch?
- ¿Para qué sirve `continue` en un bucle?

## Arreglos

- ¿Cuál es la principal limitación de los arreglos en Java?
- ¿Qué valor tiene el primer índice de un arreglo?
- ¿Cómo se accede a un elemento en un arreglo bidimensional?
- ¿Cuál es la diferencia entre arreglos y ArrayList?
- ¿Qué propiedad devuelve el tamaño de un arreglo?

## Colecciones - Introducción

- ¿Cuál es la diferencia principal entre arreglos y colecciones?
- ¿Qué es una interfaz y qué es una implementación?
- ¿Qué interfaz usarías para almacenar elementos sin duplicados?
- ¿Qué característica distingue a Map de las demás colecciones?
- ¿Qué son los Generics?

## Listas (List)

- ¿Cuál es la diferencia entre ArrayList y LinkedList?
- ¿Por qué LinkedList es mejor para inserciones frecuentes?
- ¿Qué significa que Vector sea "sincronizado"?
- ¿Cuál es la complejidad O(?) de get(index) en ArrayList?
- ¿Cuándo debería usar Vector sobre ArrayList?

## Mapas (Map)

- ¿Qué es una función hash y para qué sirve en HashMap?
- ¿Cuál es la diferencia entre HashMap y TreeMap?
- ¿Por qué LinkedHashMap mantiene orden de inserción?
- ¿Qué ventaja tiene ConcurrentHashMap sobre Hashtable?
- ¿Las claves en un Map pueden repetirse? ¿Y los valores?

## Conjuntos (Set)

- ¿Qué diferencia principal tiene un Set respecto a un List?
- ¿Cómo determina HashSet si un elemento está duplicado?
- ¿Cuál implementación de Set mantiene orden de inserción?
- ¿Por qué TreeSet no permite elementos null?
- ¿Cuándo usarías LinkedHashSet sobre HashSet?

## Elección de Estructuras

- ¿Qué estructura usarías para almacenar usuarios con acceso rápido por DNI?
- ¿Cuál es mejor para una lista de tareas donde solo importa el orden de llegada?
- ¿Qué implementación de Map elegirías para una aplicación multihilo?
- ¿Cuándo usarías LinkedList sobre ArrayList?
- ¿Qué estructura permite elementos duplicados y acceso por índice?

## Respuestas (opcional)

### ¿Qué significa que Java sea "portable" y cómo lo logra?
Respuesta: Que el mismo programa corre en distintos SO sin recompilar; se logra compilando a bytecode que ejecuta la JVM de cada plataforma.

### ¿Qué es el bytecode y qué ventaja tiene sobre el código máquina?
Respuesta: Es un código intermedio generado por `javac`; su ventaja es ser independiente del hardware y ejecutable en cualquier JVM compatible.

### ¿Cuáles son los cuatro pilares de la Programación Orientada a Objetos?
Respuesta: Encapsulamiento, abstracción, herencia y polimorfismo.

### ¿Qué es la JVM y cuál es su función principal?
Respuesta: Es la Máquina Virtual de Java; carga, verifica y ejecuta bytecode, gestionando memoria y recursos de ejecución.

### ¿Qué significa WORA (Write Once, Run Anywhere)?
Respuesta: "Escribir una vez, ejecutar en cualquier lado": un mismo bytecode corre en cualquier plataforma con JVM.

### ¿Cuál es la diferencia entre JDK, JRE y JVM?
Respuesta: JDK = herramientas de desarrollo + JRE; JRE = entorno para ejecutar apps; JVM = motor que ejecuta el bytecode.

### ¿Qué componente convierte archivos .java a .class?
Respuesta: El compilador `javac`.

### ¿Qué es el JIT Compiler y para qué sirve?
Respuesta: Es un compilador en tiempo de ejecución que traduce bytecode caliente a código nativo para mejorar rendimiento.

### ¿Qué hace el Garbage Collector?
Respuesta: Libera memoria automáticamente eliminando objetos que ya no tienen referencias alcanzables.

### ¿Para qué sirve el Bytecode Verifier?
Respuesta: Verifica seguridad y validez del bytecode antes de ejecutarlo (tipos, accesos, stack y formato).

### ¿Cuál es el método de entrada (punto de inicio) de un programa Java?
Respuesta: `public static void main(String[] args)`.

### ¿Por qué el nombre del archivo debe coincidir con la clase pública?
Respuesta: Porque Java exige que la clase `public` esté en un archivo con el mismo nombre para resolverla correctamente al compilar.

### ¿Qué diferencia hay entre CamelCase y camelCase?
Respuesta: CamelCase (PascalCase) inicia con mayúscula, se usa en clases; camelCase inicia con minúscula, se usa en variables y métodos.

### ¿Cuándo usar `//` vs `/* */` vs `/** */`?
Respuesta: `//` para una línea, `/* */` para bloque/multilínea, `/** */` para documentación Javadoc.

### ¿Java distingue mayúsculas de minúsculas?
Respuesta: Sí, Java es case-sensitive (`Nombre` y `nombre` son identificadores distintos).

### ¿Cuál es la diferencia entre tipos primitivos y tipos de referencia?
Respuesta: Primitivos guardan el valor directamente; referencias guardan la dirección de un objeto en memoria.

### ¿Cuántos bits ocupa un `int` y qué rango tiene?
Respuesta: 32 bits; desde -2,147,483,648 hasta 2,147,483,647.

### ¿Por qué usar `double` en lugar de `float`?
Respuesta: Porque tiene mayor precisión (64 bits vs 32 bits) y reduce errores de redondeo en la mayoría de cálculos.

### ¿Qué valor por defecto tienen las variables primitivas vs las de referencia?
Respuesta: En atributos de clase: primitivas tienen 0/false/'\u0000' según tipo y referencias `null`; las locales no tienen valor por defecto.

### ¿Dónde se almacenan los tipos primitivos (stack o heap)?
Respuesta: Si son variables locales, usualmente en stack; si son campos de objeto, viven dentro del objeto en heap.

### ¿Cuál es la diferencia entre variable de instancia y variable local?
Respuesta: La de instancia pertenece al objeto y existe mientras el objeto viva; la local existe solo dentro del bloque o método.

### ¿Las variables locales se inicializan automáticamente?
Respuesta: No, deben inicializarse explícitamente antes de usarse.

### ¿Qué tipo de variable se comparte entre todas las instancias de una clase?
Respuesta: La variable `static` (de clase).

### ¿Cuál es el ámbito de una variable declarada dentro de un bucle `for`?
Respuesta: Solo dentro del `for` (cabecera y bloque del bucle).

### ¿Cuándo se destruye una variable local?
Respuesta: Al salir del bloque/método donde fue declarada (fin de su alcance).

### ¿Cuál es la diferencia entre `=` y `==`?
Respuesta: `=` asigna un valor; `==` compara igualdad (en objetos compara referencias, no contenido).

### ¿Qué hace el operador `%` (módulo)?
Respuesta: Devuelve el resto de una división entera o decimal.

### ¿Qué es el cortocircuito en operadores lógicos?
Respuesta: Que en `&&` y `||` se evita evaluar la segunda condición si la primera ya determina el resultado.

### ¿Cuál es la precedencia: `&&` o `||`?
Respuesta: `&&` tiene mayor precedencia que `||`.

### ¿Qué diferencia hay entre `++x` y `x++`?
Respuesta: `++x` incrementa y luego devuelve; `x++` devuelve primero y luego incrementa.

### ¿Cuál es la diferencia entre `while` y `do-while`?
Respuesta: `while` evalúa antes de entrar; `do-while` ejecuta al menos una vez y evalúa al final.

### ¿Qué hace `break` en un switch?
Respuesta: Corta la ejecución del `switch` y evita seguir a los siguientes `case`.

### ¿Cuándo es más apropiado usar `for-each`?
Respuesta: Cuando solo necesitás recorrer todos los elementos sin usar índice ni modificar estructura durante la iteración.

### ¿Qué es el "fall-through" en un switch?
Respuesta: Es continuar al siguiente `case` por no usar `break` en el `case` actual.

### ¿Para qué sirve `continue` en un bucle?
Respuesta: Salta la iteración actual y pasa a evaluar la siguiente.

### ¿Cuál es la principal limitación de los arreglos en Java?
Respuesta: Su tamaño es fijo: no pueden crecer ni reducirse luego de crearse.

### ¿Qué valor tiene el primer índice de un arreglo?
Respuesta: 0.

### ¿Cómo se accede a un elemento en un arreglo bidimensional?
Respuesta: Con dos índices: `matriz[fila][columna]`.

### ¿Cuál es la diferencia entre arreglos y ArrayList?
Respuesta: El arreglo tiene tamaño fijo y puede guardar primitivos; `ArrayList` es dinámico y guarda objetos (o wrappers).

### ¿Qué propiedad devuelve el tamaño de un arreglo?
Respuesta: `length`.

### ¿Cuál es la diferencia principal entre arreglos y colecciones?
Respuesta: Los arreglos son de tamaño fijo; las colecciones son estructuras dinámicas con API más rica.

### ¿Qué es una interfaz y qué es una implementación?
Respuesta: Interfaz define contrato de métodos; implementación es la clase concreta que cumple ese contrato.

### ¿Qué interfaz usarías para almacenar elementos sin duplicados?
Respuesta: `Set`.

### ¿Qué característica distingue a Map de las demás colecciones?
Respuesta: Almacena pares clave-valor y accedés por clave, no por posición.

### ¿Qué son los Generics?
Respuesta: Son parámetros de tipo (`<T>`) que dan seguridad de tipos en compilación y evitan casts innecesarios.

### ¿Cuál es la diferencia entre ArrayList y LinkedList?
Respuesta: `ArrayList` ofrece acceso por índice muy rápido; `LinkedList` inserta/elimina mejor en extremos o con iterador.

### ¿Por qué LinkedList es mejor para inserciones frecuentes?
Respuesta: Porque al tener nodos enlazados evita mover muchos elementos al insertar en posiciones intermedias.

### ¿Qué significa que Vector sea "sincronizado"?
Respuesta: Que sus métodos están protegidos para acceso concurrente, haciéndolo thread-safe pero con más costo.

### ¿Cuál es la complejidad O(?) de get(index) en ArrayList?
Respuesta: O(1).

### ¿Cuándo debería usar Vector sobre ArrayList?
Respuesta: Casi nunca en código nuevo; solo por compatibilidad legacy o cuando necesitás su sincronización intrínseca.

### ¿Qué es una función hash y para qué sirve en HashMap?
Respuesta: Convierte una clave en un entero para ubicarla en buckets, acelerando búsquedas e inserciones promedio O(1).

### ¿Cuál es la diferencia entre HashMap y TreeMap?
Respuesta: `HashMap` no mantiene orden y suele ser O(1); `TreeMap` mantiene claves ordenadas y opera en O(log n).

### ¿Por qué LinkedHashMap mantiene orden de inserción?
Respuesta: Porque además de tabla hash enlaza las entradas en una lista doble en el orden en que se insertan.

### ¿Qué ventaja tiene ConcurrentHashMap sobre Hashtable?
Respuesta: Permite mayor concurrencia y mejor rendimiento, bloqueando por segmentos/operaciones y no toda la tabla.

### ¿Las claves en un Map pueden repetirse? ¿Y los valores?
Respuesta: Las claves no se repiten (una nueva pisa la anterior); los valores sí pueden repetirse.

### ¿Qué diferencia principal tiene un Set respecto a un List?
Respuesta: `Set` no admite duplicados; `List` sí y además mantiene orden por índice.

### ¿Cómo determina HashSet si un elemento está duplicado?
Respuesta: Usando `hashCode()` para ubicar bucket y `equals()` para confirmar igualdad.

### ¿Cuál implementación de Set mantiene orden de inserción?
Respuesta: `LinkedHashSet`.

### ¿Por qué TreeSet no permite elementos null?
Respuesta: Porque necesita comparar elementos para ordenarlos y `null` no es comparable en ese contexto.

### ¿Cuándo usarías LinkedHashSet sobre HashSet?
Respuesta: Cuando querés evitar duplicados pero también conservar el orden de inserción.

### ¿Qué estructura usarías para almacenar usuarios con acceso rápido por DNI?
Respuesta: Un `HashMap<DNI, Usuario>` para búsqueda por clave en tiempo promedio O(1).

### ¿Cuál es mejor para una lista de tareas donde solo importa el orden de llegada?
Respuesta: Una cola (`Queue`, por ejemplo `ArrayDeque`) para procesar en FIFO.

### ¿Qué implementación de Map elegirías para una aplicación multihilo?
Respuesta: `ConcurrentHashMap`.

### ¿Cuándo usarías LinkedList sobre ArrayList?
Respuesta: Cuando predominan inserciones/eliminaciones frecuentes en medio o extremos y el acceso aleatorio no es prioritario.

### ¿Qué estructura permite elementos duplicados y acceso por índice?
Respuesta: `List` (por ejemplo, `ArrayList`).
