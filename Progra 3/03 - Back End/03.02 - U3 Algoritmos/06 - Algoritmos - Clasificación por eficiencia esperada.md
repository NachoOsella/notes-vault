# Algoritmos - Clasificación por eficiencia esperada

## Definición
Clasifica algoritmos por cómo crece su costo al aumentar n, usando órdenes de complejidad.

## Explicación

- *Qué problema resuelve*
    Permite predecir qué tan bien escalará una solución cuando crezca el tamaño de los datos de entrada observando cómo crece su tiempo de ejecución
- *Cómo funciona por arriba*
    Clasifica algoritmos observando el crecimiento de su tiempo de ejecución según aumenta el tamaño de los datos. Esto se describe usando notación Big O. Ejemplo comparativo:
    - Búsqueda lineal: O(n)
    - Búsqueda binaria: O(log n)
    - Bubble sort: O(n²)
- *Qué implica / qué permite*
    Toma de decisiones informada sobre trade-offs; permite descartar algoritmos que no escalarán para los volúmenes de datos esperados; facilita la comparación objetiva entre diferentes algoritmos independientemente del hardware

## Comparaciones típicas
- vs [[11 - Big-O - Notación]]: clasificación cualitativa (bueno/malo) vs medición formal matemática
- vs [[12 - Big-O - O(1) constante]]|[[13 - Big-O - O(n) lineal]]|[[14 - Big-O - O(n^2) cuadrática]]|[[15 - Big-O - O(log n) logarítmica]]: categorías generales vs órdenes específicos de complejidad

## Palabras clave
- escalabilidad
- crecimiento
- Big-O
- rendimiento
- costo computacional

## Preguntas de examen
- ¿Por qué dos algoritmos correctos pueden diferir mucho en práctica?
- ¿Qué información aporta comparar O(n) contra O(log n)?

## Errores comunes
- Elegir por tiempo de prueba pequeño sin analizar crecimiento.
- Comparar algoritmos sin considerar tamaño esperado de entrada.

## Mini-ejemplo (mental)
- Para 20 datos varios enfoques funcionan; para 1 millón solo sobreviven los que escalan bien.

