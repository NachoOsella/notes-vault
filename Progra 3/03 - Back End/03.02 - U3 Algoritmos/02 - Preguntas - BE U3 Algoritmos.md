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

### ¿Qué es un algoritmo?
Respuesta: Es un conjunto finito y ordenado de pasos para resolver un problema o realizar una tarea.

### ¿Qué propiedades debe cumplir un algoritmo correctamente definido (claridad, finitud, efectividad)?
Respuesta: Debe ser claro (sin ambigüedad), finito (termina) y efectivo (cada paso es ejecutable en la práctica).

### ¿Cuáles son los tres criterios principales para clasificar algoritmos?
Respuesta: Se clasifican por tipo de problema, por forma de operar y por eficiencia esperada.

### ¿Qué significa clasificar por tipo de problema?
Respuesta: Agruparlos según lo que resuelven, por ejemplo búsqueda, ordenamiento, optimización o recorrido.

### ¿Qué significa clasificar por forma de operar?
Respuesta: Agruparlos por su estrategia de ejecución, como iterativos, recursivos, divide and conquer, greedy o dinámica.

### ¿Qué significa clasificar por eficiencia esperada?
Respuesta: Compararlos por costo de tiempo y memoria, normalmente usando notación asintótica como Big-O.

### ¿Qué características tiene un algoritmo mal diseñado?
Respuesta: Suele ser ambiguo, ineficiente, difícil de mantener o incluso no terminar para ciertos casos.

### ¿Qué es la complejidad de un algoritmo?
Respuesta: Es una medida de cuánto tiempo y/o memoria requiere un algoritmo según el tamaño de entrada.

### ¿Por qué no se mide el tiempo en segundos?
Respuesta: Porque depende del hardware, lenguaje y entorno; no permite una comparación general entre algoritmos.

### ¿Qué se mide en su lugar (operaciones elementales)?
Respuesta: Se cuentan operaciones básicas en función de n (comparaciones, asignaciones, accesos, etc.).

### ¿Qué diferencia hay entre complejidad temporal y espacial?
Respuesta: La temporal mide pasos/tiempo de ejecución; la espacial mide memoria adicional utilizada.

### ¿Qué significa el peor caso, mejor caso y caso promedio?
Respuesta: Son escenarios de análisis: máximo costo, mínimo costo y costo esperado para entradas típicas.

### ¿Qué representa la notación Big-O?
Respuesta: Representa una cota superior del crecimiento del costo de un algoritmo al aumentar n, usualmente en peor caso.

### ¿Qué significa O(1) y qué ejemplos típicos tiene?
Respuesta: Tiempo constante: no crece con n. Ejemplos: acceder a `array[i]` o hacer push/pop en una pila.

### ¿Qué significa O(n) y en qué casos aparece?
Respuesta: Tiempo lineal: crece proporcionalmente con n. Aparece al recorrer una lista una sola vez.

### ¿Qué significa O(n²) y qué algoritmos típicos lo tienen?
Respuesta: Tiempo cuadrático: suele aparecer con dos bucles anidados, como Bubble Sort o Selection Sort.

### ¿Qué significa O(log n) y por qué es eficiente?
Respuesta: Crece muy lento porque reduce el problema por factores (mitades); ejemplo típico: búsqueda binaria.

### ¿Cómo se ordenan estas complejidades de mejor a peor?
Respuesta: O(1) < O(log n) < O(n) < O(n log n) < O(n²) < O(2^n) < O(n!).

### ¿Cómo funciona la búsqueda lineal?
Respuesta: Recorre los elementos uno por uno hasta encontrar el objetivo o llegar al final.

### ¿Cuál es la complejidad de la búsqueda lineal?
Respuesta: Peor caso O(n), mejor caso O(1) si el elemento está al inicio.

### ¿La búsqueda lineal requiere que el array esté ordenado?
Respuesta: No, funciona tanto en arreglos ordenados como desordenados.

### ¿Cómo funciona la búsqueda binaria?
Respuesta: Compara con el elemento medio y descarta la mitad donde no puede estar el valor, repitiendo el proceso.

### ¿Cuál es la complejidad de la búsqueda binaria?
Respuesta: O(log n) en tiempo y O(1) en espacio si es iterativa.

### ¿Por qué la búsqueda binaria requiere array ordenado?
Respuesta: Porque decide qué mitad descartar usando el orden; sin orden, esa decisión no es válida.

### ¿Cuándo conviene usar búsqueda binaria sobre lineal?
Respuesta: Cuando los datos están ordenados (o se harán muchas búsquedas sobre los mismos datos ordenados).

### ¿Qué es la sucesión de Fibonacci?
Respuesta: Secuencia donde cada término es la suma de los dos anteriores: 0, 1, 1, 2, 3, 5, ...

### ¿Cómo se implementa Fibonacci recursivo?
Respuesta: Con casos base `F(0)=0`, `F(1)=1` y recurrencia `F(n)=F(n-1)+F(n-2)`.

### ¿Cuál es la complejidad del Fibonacci recursivo naive?
Respuesta: Temporal O(2^n) aproximadamente, por la gran repetición de subproblemas.

### ¿Por qué el Fibonacci recursivo es tan lento para valores grandes?
Respuesta: Porque recalcula muchas veces los mismos valores y el árbol de llamadas crece exponencialmente.

### ¿Qué es la programación dinámica?
Respuesta: Técnica que guarda resultados de subproblemas para reutilizarlos y evitar recálculos.

### ¿Cómo mejora la programación dinámica el Fibonacci?
Respuesta: Memoiza o tabula resultados intermedios, reduciendo el tiempo de exponencial a lineal.

### ¿Cuál es la complejidad del Fibonacci con memoización?
Respuesta: O(n) en tiempo y O(n) en espacio.

### ¿Qué es el bottom-up vs top-down en programación dinámica?
Respuesta: Top-down usa recursión + memoización; bottom-up construye soluciones iterativamente desde casos base.

### ¿Qué es la estrategia Divide and Conquer y en qué algoritmos se usa?
Respuesta: Divide en subproblemas independientes, resuelve y combina. Se usa en Merge Sort, Quick Sort y búsqueda binaria.

### ¿Cómo funciona Backtracking y para qué tipo de problemas sirve?
Respuesta: Prueba decisiones paso a paso y retrocede cuando una rama falla; útil en combinatoria y restricciones (N-Queens, Sudoku).

### ¿Cuál es la diferencia entre Divide and Conquer y Backtracking?
Respuesta: Divide and Conquer descompone y combina soluciones de subproblemas; Backtracking explora candidatos y poda ramas inválidas.

### ¿Qué es un algoritmo Greedy y cuándo garantiza optimalidad global?
Respuesta: Toma la mejor decisión local en cada paso; garantiza óptimo global solo si hay subestructura óptima y elección voraz válida.

### ¿Qué es la programación dinámica y cuándo se aplica?
Respuesta: Se aplica cuando hay subproblemas superpuestos y subestructura óptima; evita recomputar resultados.

### ¿Cuál es la diferencia entre top-down y bottom-up en programación dinámica?
Respuesta: Top-down resuelve bajo demanda con recursión; bottom-up llena una tabla iterativa desde lo más simple.

### ¿Por qué programación dinámica es diferente de Divide and Conquer?
Respuesta: En dinámica los subproblemas se repiten y se almacenan resultados; en Divide and Conquer suelen ser independientes.
