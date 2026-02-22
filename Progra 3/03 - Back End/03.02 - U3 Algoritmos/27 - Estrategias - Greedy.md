# Estrategias - Greedy

## Definición
Greedy toma en cada paso la mejor decisión local buscando un buen resultado global.

## Explicación

- *Qué problema resuelve*
    Problemas de optimización donde tomar decisiones óptimas localmente en cada paso conduce a una solución global óptima o cercana a la óptima
- *Cómo funciona por arriba*
    - Toma decisiones locales óptimas en cada paso con la esperanza de llegar a una solución global óptima
    - En cada paso elige la opción que parece mejor en ese momento sin considerar el futuro
    - No revisa decisiones pasadas
    - **Ejemplo**: Siempre elegir la opción que parece mejor en el momento
- *Qué implica / qué permite*
    Suele aplicarse en problemas de optimización como seleccionar caminos más cortos o distribuir recursos; algoritmos comunes: Prim, Kruskal; no siempre garantiza solución óptima global pero produce buenas aproximaciones; generalmente eficientes O(n log n)

## Comparaciones típicas
- vs [[26 - Estrategias - Backtracking]]: decisiones definitivas sin revisión vs exploración con retroceso
- vs [[22 - Fibonacci - Programación dinámica]]: decisión local sin memoria vs almacenamiento de todas las soluciones parciales
- vs [[25 - Estrategias - Divide and Conquer]]: elección local voraz vs división recursiva sin criterio de optimalidad local

## Palabras clave
- greedy
- decisión local
- heurística
- optimización
- irreversibilidad

## Preguntas de examen
- ¿Cuándo un enfoque Greedy garantiza óptimo global?
- ¿Qué diferencia clave tiene Greedy respecto de Programación Dinámica?

## Errores comunes
- Suponer que toda elección local óptima produce solución global óptima.
- No justificar la propiedad greedy-choice del problema.

## Mini-ejemplo (mental)
- Dar cambio con monedas eligiendo siempre la mayor posible: a veces funciona perfecto, a veces no.

