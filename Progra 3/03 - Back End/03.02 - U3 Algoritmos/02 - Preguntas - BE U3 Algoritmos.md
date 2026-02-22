# Preguntas - BE U3 Algoritmos

## Clasificación de algoritmos

- ¿Qué es un algoritmo?
- ¿Qué propiedades debe cumplir un algoritmo correctamente definido (claridad, finitud, efectividad)?
- ¿Cuáles son los tres criterios principales para clasificar algoritmos?
- ¿Qué significa clasificar por tipo de problema?
- ¿Qué significa clasificar por forma de operar?
- ¿Qué significa clasificar por eficiencia esperada?
- ¿Qué características tiene un algoritmo mal diseñado?

## Complejidad algorítmica

- ¿Qué es la complejidad de un algoritmo?
- ¿Por qué no se mide el tiempo en segundos?
- ¿Qué se mide en su lugar (operaciones elementales)?
- ¿Qué diferencia hay entre complejidad temporal y espacial?
- ¿Qué significa el peor caso, mejor caso y caso promedio?

## Notación Big-O

- ¿Qué representa la notación Big-O?
- ¿Qué significa O(1) y qué ejemplos típicos tiene?
- ¿Qué significa O(n) y en qué casos aparece?
- ¿Qué significa O(n²) y qué algoritmos típicos lo tienen?
- ¿Qué significa O(log n) y por qué es eficiente?
- ¿Cómo se ordenan estas complejidades de mejor a peor?

## Búsqueda

- ¿Cómo funciona la búsqueda lineal?
- ¿Cuál es la complejidad de la búsqueda lineal?
- ¿La búsqueda lineal requiere que el array esté ordenado?
- ¿Cómo funciona la búsqueda binaria?
- ¿Cuál es la complejidad de la búsqueda binaria?
- ¿Por qué la búsqueda binaria requiere array ordenado?
- ¿Cuándo conviene usar búsqueda binaria sobre lineal?

## Fibonacci

- ¿Qué es la sucesión de Fibonacci?
- ¿Cómo se implementa Fibonacci recursivo?
- ¿Cuál es la complejidad del Fibonacci recursivo naive?
- ¿Por qué el Fibonacci recursivo es tan lento para valores grandes?
- ¿Qué es la programación dinámica?
- ¿Cómo mejora la programación dinámica el Fibonacci?
- ¿Cuál es la complejidad del Fibonacci con memoización?
- ¿Qué es el bottom-up vs top-down en programación dinámica?

## Estrategias de resolución

- ¿Qué es la estrategia Divide and Conquer y en qué algoritmos se usa?
- ¿Cómo funciona Backtracking y para qué tipo de problemas sirve?
- ¿Cuál es la diferencia entre Divide and Conquer y Backtracking?
- ¿Qué es un algoritmo Greedy y cuándo garantiza optimalidad global?
- ¿Qué es la programación dinámica y cuándo se aplica?
- ¿Cuál es la diferencia entre top-down y bottom-up en programación dinámica?
- ¿Por qué programación dinámica es diferente de Divide and Conquer?

## Respuestas (opcional)

### ¿Qué es la notación Big-O?
Respuesta: Es una notación matemática que describe el comportamiento límite de una función cuando el argumento tiende a un valor particular. En algoritmos, describe la complejidad temporal en el peor caso. Ver: [[11 - Big-O - Notación]]

### ¿Qué es Divide and Conquer?
Respuesta: Estrategia que divide el problema en subproblemas independientes, los resuelve recursivamente y combina soluciones. Ejemplos: Merge Sort, Quick Sort, Búsqueda Binaria. Ver: [[25 - Estrategias - Divide and Conquer]]

### ¿Qué es Backtracking?
Respuesta: Estrategia de exploración que construye soluciones paso a paso y retrocede cuando detecta que un camino no lleva a solución válida. Usado en Sudoku, laberintos, N-Queens. Ver: [[26 - Estrategias - Backtracking]]

### ¿Qué es un algoritmo Greedy?
Respuesta: Estrategia que en cada paso toma la decisión óptima local sin considerar el futuro. No siempre garantiza óptimo global pero es eficiente. Ver: [[27 - Estrategias - Greedy]]

### ¿Cuál es la diferencia entre búsqueda lineal y binaria?
Respuesta: La lineal recorre secuencialmente todos los elementos (O(n)) y no requiere ordenamiento. La binaria divide el espacio de búsqueda a la mitad (O(log n)) pero requiere array ordenado. Ver: [[18 - Búsqueda - Comparación de eficiencia]]

### ¿Por qué el Fibonacci recursivo naive es ineficiente?
Respuesta: Porque recalcula los mismos valores muchas veces, generando un árbol de llamadas exponencial con complejidad O(2^n). Ver: [[21 - Fibonacci - Complejidad recursiva]]

### ¿Qué es la programación dinámica?
Respuesta: Es una técnica que resuelve problemas dividiéndolos en subproblemas más pequeños, almacenando los resultados para evitar recálculos. Ver: [[22 - Fibonacci - Programación dinámica]]

### ¿Qué propiedades debe cumplir un algoritmo correctamente definido?
Respuesta: Debe ser claro y preciso, finito (terminar) y efectivo (pasos ejecutables con recursos razonables). Ver: [[03 - Algoritmos - Clasificación]]
