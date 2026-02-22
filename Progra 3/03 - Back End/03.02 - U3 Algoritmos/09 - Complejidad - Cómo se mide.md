# Complejidad - Cómo se mide

## Definición
Se mide estimando operaciones elementales y su crecimiento para peor, mejor y caso promedio.

## Explicación

- *Qué problema resuelve*
    Establece una forma concreta de estimar cómo crecen los recursos necesarios (tiempo o espacio) en función del tamaño del problema de entrada
- *Cómo funciona por arriba*
    Se analiza el comportamiento del algoritmo cuando el tamaño de entrada n crece:
    - Se estima cómo crecen las operaciones necesarias
    - Se considera que un algoritmo poco eficiente puede funcionar bien para casos pequeños pero volverse impracticable cuando crece la entrada
    - La relación se expresa usando notación matemática que describe el comportamiento en "peor caso", "mejor caso" o "caso promedio"
- *Qué implica / qué permite*
    Comparar algoritmos de forma objetiva sin importar en qué máquina se ejecutan; predecir el comportamiento con entradas grandes; identificar cuándo un algoritmo se vuelve impracticable

## Comparaciones típicas
- vs [[08 - Complejidad - Qué es]]: metodología de medición vs el concepto en sí
- vs [[11 - Big-O - Notación]]: medición informal (contar operaciones) vs notación formal matemática
- vs análisis por casos (peor/mejor/promedio): misma métrica aplicada bajo distintos escenarios de entrada

## Palabras clave
- operaciones elementales
- peor caso
- mejor caso
- caso promedio
- análisis asintótico

## Preguntas de examen
- ¿Por qué no se recomienda medir complejidad en segundos?
- ¿Qué utilidad tiene analizar el peor caso?

## Errores comunes
- Contar microsegundos en vez de crecimiento asintótico.
- Ignorar supuestos del caso promedio.

## Mini-ejemplo (mental)
- Comparar compras por cantidad de productos, no por velocidad del cajero de un día puntual.

