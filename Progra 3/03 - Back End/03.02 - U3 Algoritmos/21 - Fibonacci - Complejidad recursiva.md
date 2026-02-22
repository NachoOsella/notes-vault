# Fibonacci - Complejidad recursiva

## Definición
Analiza por qué Fibonacci recursivo naive crece de forma exponencial por subproblemas repetidos.

## Explicación

- *Qué problema resuelve*
    Explica por qué la solución recursiva naive de Fibonacci, aunque correcta, es prácticamente inusable para valores medianos de n
- *Cómo funciona por arriba*
    - Cada llamada genera dos nuevas llamadas (F(n-1) y F(n-2))
    - Esto genera una estructura de árbol binario de llamadas
    - La cantidad de llamadas crece exponencialmente
    - **Complejidad temporal**: O(2ⁿ)
    - **Ejemplos concretos**:
        - Para `fibonacci(5)` → ~15 llamadas
        - Para `fibonacci(40)` → más de 300 millones de llamadas
    - Muchos valores se recalculan múltiples veces (ej: fibonacci(2) se calcula varias veces)
- *Qué implica / qué permite*
    - Es un claro ejemplo de algoritmo mal diseñado si se usa sin optimización
    - El tiempo crece exponencialmente, haciendo inviable calcular valores grandes
    - Evidencia la necesidad de técnicas como memoización o programación dinámica para evitar recálculos

## Comparaciones típicas
- vs [[20 - Fibonacci - Recursivo]]: análisis de complejidad vs implementación del código
- vs [[14 - Big-O - O(n^2) cuadrática]]: complejidad exponencial O(2^n) es aún peor que cuadrática
- vs [[22 - Fibonacci - Programación dinámica]]: complejidad exponencial sin memo vs lineal con memo

## Palabras clave
- complejidad exponencial
- subproblemas repetidos
- árbol recursivo
- ineficiencia
- O(2^n)

## Preguntas de examen
- ¿Qué evidencia muestra que Fibonacci recursivo no escala?
- ¿Qué técnica cambia su complejidad a lineal?

## Errores comunes
- Pensar que recursivo implica necesariamente eficiencia.
- No detectar recálculo de estados idénticos.

## Mini-ejemplo (mental)
- Rehacer el mismo ejercicio muchas veces porque no guardaste resultados anteriores.

