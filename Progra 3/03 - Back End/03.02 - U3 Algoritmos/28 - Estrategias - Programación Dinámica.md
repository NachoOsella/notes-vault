# Estrategias - Programación Dinámica

## Definición
Programación Dinámica resuelve problemas con subproblemas superpuestos guardando resultados para reutilizarlos.

## Explicación

- *Qué problema resuelve*
    Problemas que pueden dividirse en subproblemas más pequeños con superposición (los mismos subproblemas aparecen múltiples veces), optimizando mediante almacenamiento de resultados
- *Cómo funciona por arriba*
    - Es una técnica de optimización que evita cálculos repetidos almacenando los resultados ya calculados (memorización)
    - **Dos formas**:
        - **Top-down**: recursión + memoización (guarda resultados en array/diccionario antes de retornarlos)
        - **Bottom-up**: iterativa, construye tabla iterativamente (tabulación), reutilizando resultados en lugar de recalcular. Más eficiente porque evita el uso de la pila de llamadas
    - **Ejemplo**: Recordar soluciones anteriores para no repetir trabajo (ya aplicado en Fibonacci)
- *Qué implica / qué permite*
    Reduce complejidad exponencial a polinomial (ej: de O(2ⁿ) a O(n) en Fibonacci); requiere espacio adicional O(n) o más; aplicable cuando hay subestructura óptima y subproblemas superpuestos; ejemplos: Fibonacci, mochila, caminos mínimos

## Comparaciones típicas
- vs [[22 - Fibonacci - Programación dinámica]]: aplicación específica de la estrategia general al problema de Fibonacci
- vs [[25 - Estrategias - Divide and Conquer]]: subproblemas superpuestos con almacenamiento vs subproblemas independientes
- vs [[27 - Estrategias - Greedy]]: explora todas las opciones guardando resultados vs toma decisiones locales sin revisión
- vs [[26 - Estrategias - Backtracking]]: memorización para evitar recálculos vs retroceso para explorar alternativas

## Palabras clave
- programación dinámica
- subproblemas superpuestos
- memoización
- tabulación
- subestructura óptima

## Preguntas de examen
- ¿Qué dos propiedades debe tener un problema para aplicar Programación Dinámica?
- ¿Cuándo conviene top-down y cuándo bottom-up?

## Errores comunes
- Aplicarla en problemas sin superposición de subproblemas.
- Guardar estados incompletos o mal definidos.

## Mini-ejemplo (mental)
- Armar presupuesto mensual reutilizando cálculos ya hechos en vez de recalcular desde cero cada semana.

