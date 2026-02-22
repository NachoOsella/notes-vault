# Búsqueda - Comparación de eficiencia

## Definición
Compara lineal y binaria para decidir cuál conviene según tamaño de datos y precondiciones.

## Explicación

- *Qué problema resuelve*
    Ayuda a decidir qué algoritmo de búsqueda usar según las características del problema (tamaño de datos, ordenamiento, frecuencia de búsquedas)
- *Cómo funciona por arriba*
    - **Comparación para n = 1.000.000**:
        - Búsqueda lineal: hasta 1.000.000 comparaciones en el peor caso
        - Búsqueda binaria: hasta log₂(1.000.000) ≈ 20 comparaciones
    - La búsqueda binaria es muchísimo más eficiente en arreglos grandes
    - Mientras la lineal puede requerir revisar cada uno de los elementos (un millón), la binaria lo hace en alrededor de 20 pasos
    - **Trade-offs**: Lineal no requiere ordenamiento previo; Binaria requiere datos ordenados (costo de preparación)
- *Qué implica / qué permite*
    Tomar decisiones informadas: para pocas búsquedas en datos desordenados puede ser mejor lineal; para muchas búsquedas, ordenar y usar binaria compensa; permite análisis de break-even point

## Comparaciones típicas
- vs [[16 - Búsqueda - Lineal]]: análisis comparativo vs descripción del algoritmo individual
- vs [[17 - Búsqueda - Binaria]]: análisis comparativo vs descripción del algoritmo individual
- vs [[11 - Big-O - Notación]]: comparación aplicada entre O(n) y O(log n)

## Palabras clave
- comparación
- trade-off
- costo de ordenamiento
- lineal vs binaria
- decisión algorítmica

## Preguntas de examen
- ¿Cuándo compensa ordenar para luego buscar con binaria?
- ¿Qué métrica usarías para justificar una elección en backend?

## Errores comunes
- Evaluar solo complejidad de búsqueda sin incluir costo de preparación de datos.
- Generalizar una elección sin considerar frecuencia de consultas.

## Mini-ejemplo (mental)
- Si buscás una sola vez, revisar lista puede bastar; si buscás miles de veces, conviene ordenar e indexar.

