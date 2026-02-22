# Estrategias - Divide and Conquer

## Definición
Divide and Conquer divide el problema en partes independientes, las resuelve y combina resultados.

## Explicación

- *Qué problema resuelve*
    Problemas que pueden descomponerse en subproblemas más pequeños del mismo tipo, donde la solución del problema grande se construye a partir de las soluciones de los pequeños
- *Cómo funciona por arriba*
    - Se basa en dividir un problema en subproblemas más pequeños
    - Resolverlos de manera recursiva
    - Luego combinar las soluciones
    - Típicamente reduce el espacio de búsqueda a la mitad en cada paso
    - **Ejemplo cotidiano**: Buscar una palabra en un diccionario ordenado cortándolo por la mitad cada vez
- *Qué implica / qué permite*
    Es muy eficiente para ciertos tipos de problemas como ordenamientos o búsqueda; algoritmos comunes: Merge Sort, Binary Search, Quick Sort; eficiencia típica O(log n) o O(n log n); permite paralelización

## Comparaciones típicas
- vs [[17 - Búsqueda - Binaria]]: ejemplo paradigmático de divide and conquer aplicado a búsqueda
- vs [[26 - Estrategias - Backtracking]]: divide en subproblemas independientes vs explora caminos con posible vuelta atrás
- vs [[22 - Fibonacci - Programación dinámica]]: subproblemas independientes vs subproblemas superpuestos con solapamiento

## Palabras clave
- divide and conquer
- subproblemas independientes
- recursión
- combinación
- n log n

## Preguntas de examen
- ¿Qué condiciones favorecen usar Divide and Conquer?
- ¿Qué algoritmos clásicos de la unidad siguen este enfoque?

## Errores comunes
- Confundir subproblemas independientes con superpuestos.
- Olvidar la etapa de combinación de resultados.

## Mini-ejemplo (mental)
- Ordenar un mazo: separás en mitades, ordenás cada mitad y luego fusionás.

