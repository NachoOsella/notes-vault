# Fibonacci - Conclusión

## Definición
Resume el aprendizaje central: no alcanza con que un algoritmo funcione, también debe escalar.

## Explicación

- *Qué problema resuelve*
    Síntesis del caso de estudio Fibonacci mostrando cómo un algoritmo puede funcionar bien en teoría pero ser poco práctico en la realidad si no se diseña correctamente
- *Cómo funciona por arriba*
    - **Comparación de soluciones**:
        - **Recursiva (O(2ⁿ))**: Buena para explicar conceptos, pero no es eficiente. Para fibonacci(40) requiere más de 300 millones de llamadas
        - **Programación Dinámica (O(n))**: Transforma la solución ineficiente en una muy rápida con unas pocas operaciones
    - **Trade-off**: Recursión (claridad conceptual) vs Iteración (eficiencia práctica)
- *Qué implica / qué permite*
    - Es fundamental analizar la complejidad de un algoritmo antes de usarlo, especialmente en casos reales donde el tamaño de entrada puede ser muy grande
    - Aprender recursividad está bien para entender cómo se divide un problema, pero también es importante saber cuándo conviene usarla y cuándo no
    - **Conclusión clave**: No alcanza con que el algoritmo funcione, también tiene que hacerlo de forma eficiente
    - Las técnicas aprendidas (memoización, programación dinámica) aplican a problemas reales: caminos mínimos, knapsack, edit distance

## Comparaciones típicas
- vs [[20 - Fibonacci - Recursivo]]: resumen comparativo naive vs optimizado
- vs [[22 - Fibonacci - Programación dinámica]]: síntesis de técnicas aplicadas
- vs [[28 - Estrategias - Programación Dinámica]]: cierre del caso Fibonacci frente a uso general de la técnica

## Palabras clave
- síntesis
- eficiencia
- escalabilidad
- recursión vs DP
- criterio de diseño

## Preguntas de examen
- ¿Qué lección deja el caso Fibonacci para problemas reales de backend?
- ¿Qué señales te indicarían refactorizar una solución recursiva?

## Errores comunes
- Elegir implementación por simplicidad sin validar complejidad.
- No extrapolar el aprendizaje a otros problemas con subproblemas repetidos.

## Mini-ejemplo (mental)
- Una solución simple sirve en clase; en producción gana la que responde a escala.

