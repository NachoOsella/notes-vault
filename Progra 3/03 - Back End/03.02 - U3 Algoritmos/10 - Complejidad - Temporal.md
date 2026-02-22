# Complejidad - Temporal

## Definición
La complejidad temporal expresa cómo crece el tiempo de ejecución cuando crece n.

## Explicación

- *Qué problema resuelve*
    Analiza cuánto tiempo tarda un algoritmo en ejecutarse de forma independiente del hardware específico
- *Cómo funciona por arriba*
    En lugar de medir tiempo con un reloj (que depende de la computadora), se mide en función de la cantidad de operaciones elementales que realiza:
    - Comparaciones, asignaciones, ciclos, llamadas a funciones
    - Se analiza el número de iteraciones y operaciones clave
    - Se considera cómo cambia ese número cuando el tamaño de entrada n crece
    - **Ejemplo O(n)**: Revisar una lista de clientes - si hay 10 clientes se hacen 10 envíos, si hay 1000 se hacen 1000 envíos (crece proporcionalmente)
    - **Ejemplo O(n²)**: Comparar pares de productos - si hay 10 productos se hacen ~100 comparaciones (10×10), si hay 100 se hacen 10.000 (100×100)
- *Qué implica / qué permite*
    Permite comparar algoritmos de forma objetiva sin importar la máquina; identificar cuellos de botella; decidir si un algoritmo es viable para producción con ciertos volúmenes de datos; diferenciar entre crecimiento lineal, cuadrático, logarítmico, etc.

## Comparaciones típicas
- vs [[08 - Complejidad - Qué es]]: complejidad específica de tiempo vs complejidad general (que incluye espacial)
- vs [[11 - Big-O - Notación]]: análisis de tiempo sin notación formal vs con notación Big-O
- vs complejidad espacial: recursos de tiempo vs recursos de memoria

## Palabras clave
- tiempo de ejecución
- operaciones
- iteraciones
- costo temporal
- rendimiento

## Preguntas de examen
- ¿Qué operaciones suelen contarse para estimar complejidad temporal?
- ¿Por qué O(n²) se vuelve crítico con n grande?

## Errores comunes
- Optimizar microdetalles sin revisar el orden de complejidad.
- Ignorar cuellos de botella en bucles anidados.

## Mini-ejemplo (mental)
- Revisar una fila una vez (lineal) vs comparar cada persona con todas (cuadrática).

