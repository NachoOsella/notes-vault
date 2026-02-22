# Big-O - O(n) lineal

## Definición
O(n) implica que el costo crece proporcionalmente al tamaño de la entrada.

## Explicación

- *Qué problema resuelve*
    Describe algoritmos donde el tiempo crece proporcionalmente al tamaño de la entrada, siendo aceptable para muchas aplicaciones prácticas
- *Cómo funciona por arriba*
    - El tiempo de ejecución crece en proporción directa al tamaño de los datos
    - Si los datos se duplican, el tiempo también se duplica (más o menos)
    - **Ejemplo**: Buscar el número de ficha de un paciente en la sala de espera - recorrer una lista desde el principio, nombre por nombre, hasta encontrarlo
    - Si hay 10 pacientes, hasta 10 comparaciones; si hay 100, hasta 100
    - A medida que la lista crece, el tiempo de búsqueda crece al mismo ritmo
- *Qué implica / qué permite*
    Escalabilidad lineal y predecible; eficiente para procesamiento secuencial; duplicar la entrada duplica el tiempo; base para algoritmos más complejos

## Comparaciones típicas
- vs [[12 - Big-O - O(1) constante]]: crecimiento proporcional a n vs tiempo fijo
- vs [[14 - Big-O - O(n^2) cuadrática]]: crecimiento lineal vs crecimiento cuadrático (mucho peor)
- vs [[16 - Búsqueda - Lineal]]: ejemplo clásico de algoritmo O(n) aplicado

## Palabras clave
- O(n)
- lineal
- recorrido secuencial
- proporcionalidad
- escalado

## Preguntas de examen
- ¿Qué tipo de tareas suelen ser O(n)?
- ¿En qué casos O(n) sigue siendo una opción razonable?

## Errores comunes
- Usar recorridos lineales repetidos innecesariamente.
- No aprovechar estructuras que permitan mejor complejidad.

## Mini-ejemplo (mental)
- Pasar lista en clase: si hay el doble de alumnos, tardás aprox. el doble.

