# Estrategias - Backtracking

## Definición
Backtracking explora soluciones parciales y retrocede cuando un camino deja de ser válido.

## Explicación

- *Qué problema resuelve*
    Problemas de exploración o combinatorios donde se debe encontrar una solución entre múltiples posibilidades
- *Cómo funciona por arriba*
    - Consiste en ir construyendo una solución paso a paso
    - Cuando se detecta que no se puede continuar por un camino, se retrocede (backtrack)
    - Se prueba otra alternativa desde el último punto de decisión
    - **Ejemplo**: Probar opciones y volver atrás si no funciona
- *Qué implica / qué permite*
    Es típico en problemas de exploración como laberintos, rompecabezas o combinatorias; ejemplos clásicos: Sudoku, N-Queens, resolver laberinto; complejidad puede ser exponencial pero poda ramas inviables

## Comparaciones típicas
- vs [[25 - Estrategias - Divide and Conquer]]: explora con retroceso vs divide en subproblemas independientes
- vs [[27 - Estrategias - Greedy]]: explora múltiples caminos deshaciendo decisiones vs toma decisiones definitivas locales
- vs [[20 - Fibonacci - Recursivo]]: backtracking explora espacio de soluciones vs recursión simple que calcula valores

## Palabras clave
- backtracking
- exploración
- poda
- retroceso
- combinatoria

## Preguntas de examen
- ¿Qué problemas típicos se resuelven con Backtracking?
- ¿Qué papel cumple la poda para reducir costo?

## Errores comunes
- No definir condición de corte y explorar todo el árbol sin control.
- Confundir backtracking con brute force sin poda.

## Mini-ejemplo (mental)
- Laberinto: avanzás, y si llegás a un callejón sin salida, volvés al último cruce.

