# Big-O - O(n^2) cuadrática

## Definición
O(n²) aparece cuando por cada elemento se vuelve a recorrer toda la entrada (doble bucle).

## Explicación

- *Qué problema resuelve*
    Surge naturalmente en algoritmos que comparan cada elemento con todos los demás, siendo tolerable solo para conjuntos pequeños de datos
- *Cómo funciona por arriba*
    - Por cada elemento del conjunto, se realiza un recorrido completo sobre todo el conjunto otra vez
    - Dos bucles anidados resultando en n×n iteraciones
    - **Ejemplo**: Organizar entrevistas entre alumnos donde cada uno debe hablar con todos los demás
    - Si hay 10 alumnos, cada uno entrevista a 9 otros
    - Crecimiento cuadrático: con n=10 son ~100 operaciones, con n=100 son ~10.000
- *Qué implica / qué permite*
    Muy costoso para entradas grandes; rápidamente se vuelve inviable; con n=1000 son 1 millón de operaciones; señal de que el algoritmo necesita optimización urgente

## Comparaciones típicas
- vs [[13 - Big-O - O(n) lineal]]: crecimiento cuadrático mucho más lento que lineal para n grande
- vs [[11 - Big-O - Notación]]: O(n^2) es una categoría frecuente en algoritmos simples como burbuja
- vs [[15 - Big-O - O(log n) logarítmica]]: ineficiencia polinómica vs eficiencia logarítmica

## Palabras clave
- O(n²)
- bucles anidados
- costo cuadrático
- comparaciones
- baja escalabilidad

## Preguntas de examen
- ¿Qué patrones de código suelen derivar en O(n²)?
- ¿Por qué O(n²) puede ser inviable en producción?

## Errores comunes
- Usar doble loop por defecto sin evaluar alternativas.
- Subestimar impacto al crecer n (10x datos implica ~100x trabajo).

## Mini-ejemplo (mental)
- Si cada alumno debe hablar con todos, la cantidad de interacciones explota rápidamente.

