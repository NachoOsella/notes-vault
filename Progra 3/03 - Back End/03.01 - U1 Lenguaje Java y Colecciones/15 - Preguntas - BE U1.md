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

### Portabilidad de Java
Respuesta: Java logra portabilidad mediante el bytecode y la JVM. El código fuente se compila a bytecode (independiente de plataforma), y la JVM específica de cada sistema operativo ejecuta ese bytecode. Ver: [[01 - Java - Introducción y características]] y [[02 - Java - JDK y JVM]]

### ArrayList vs LinkedList
**ArrayList**: Acceso rápido O(1), inserción lenta O(n). Basado en arreglo dinámico.
**LinkedList**: Acceso lento O(n), inserción rápida O(1). Basado en nodos enlazados.
Ver: [[10 - Colecciones - Listas (List)]]

### HashMap vs TreeMap
**HashMap**: Tabla hash, acceso O(1), sin orden.
**TreeMap**: Árbol rojo-negro, acceso O(log n), ordenado por clave.
Ver: [[11 - Colecciones - Mapas (Map)]]

### Set vs List
**Set**: No permite duplicados, sin orden específico (generalmente).
**List**: Permite duplicados, mantiene orden, acceso por índice.
Ver: [[12 - Colecciones - Conjuntos (Set)]] y [[10 - Colecciones - Listas (List)]]
