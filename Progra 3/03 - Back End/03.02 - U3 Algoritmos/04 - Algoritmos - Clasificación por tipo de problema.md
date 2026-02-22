# Algoritmos - Clasificación por tipo de problema

## Definición
Clasifica algoritmos según la tarea que resuelven: búsqueda, ordenamiento, optimización o recorrido.

## Explicación

- *Qué problema resuelve*
    Permite identificar qué algoritmo usar según la naturaleza del problema a resolver (búsqueda, ordenamiento, grafos, optimización, etc.)
- *Cómo funciona por arriba*
    Agrupa algoritmos según el tipo de tarea que realizan:
    - **Algoritmos de búsqueda**: encuentran un elemento dentro de una estructura de datos (arreglo, lista). Ejemplos: Búsqueda lineal O(n), Búsqueda binaria O(log n) (requiere orden)
    - **Algoritmos de ordenamiento**: reorganizan elementos según algún criterio (menor a mayor). Ejemplos: Bubble sort (simple pero poco eficiente), Merge sort (más eficiente, basado en divide y conquistar), Quick sort (muy usado en la práctica)
    - **Algoritmos de optimización**: buscan la mejor solución posible (óptima) entre muchas alternativas según una medida. Ejemplos: Problema de la mochila (knapsack), Caminos mínimos (Dijkstra), Algoritmos de asignación de tareas
    - **Algoritmos de recorrido**: exploran estructuras de datos (listas enlazadas, árboles, grafos). Ejemplos: Recorridos en profundidad (DFS), Recorridos en anchura (BFS), Recorridos en árboles binarios (inorden, preorden, postorden)
- *Qué implica / qué permite*
    Simplifica la búsqueda de soluciones en bibliotecas y frameworks; ayuda a comprender que problemas similares pueden tener soluciones similares; facilita la comunicación entre programadores al usar un vocabulario común

## Comparaciones típicas
- vs [[05 - Algoritmos - Clasificación por forma de operar]]: clasificación por "qué resuelve" vs "cómo lo resuelve"
- vs [[06 - Algoritmos - Clasificación por eficiencia esperada]]: clasificación por dominio del problema vs por rendimiento medible

## Palabras clave
- búsqueda
- ordenamiento
- optimización
- recorrido
- dominio del problema

## Preguntas de examen
- ¿Qué diferencia hay entre un algoritmo de búsqueda y uno de recorrido?
- ¿Qué ejemplos de optimización aparecen en la unidad?

## Errores comunes
- Pensar que un algoritmo de una categoría sirve igual de bien para cualquier problema.
- Ignorar restricciones del dominio (datos ordenados, estructura, costo).

## Mini-ejemplo (mental)
- Si querés encontrar un libro en biblioteca, usás un algoritmo de búsqueda; si querés reubicar todos por autor, usás ordenamiento.

