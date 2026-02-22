# Búsqueda - Lineal

## Definición
La búsqueda lineal revisa elementos uno por uno hasta encontrar el objetivo o agotar la colección.

## Explicación

- *Qué problema resuelve*
    Encontrar un elemento en una colección cuando no se sabe nada sobre el ordenamiento de los datos o cuando la colección es muy pequeña
- *Cómo funciona por arriba*
    - Recorre los elementos uno por uno desde el comienzo hasta el final
    - En cada paso, compara el elemento actual con el valor buscado
    - Si lo encuentra, devuelve su posición; si llega al final sin encontrarlo, indica que no está presente
    - **Código**: `for (int i = 0; i < arr.length; i++) { if (arr[i] == objetivo) return i; } return -1;`
- *Qué implica / qué permite*
    - **Características**: No necesita que el arreglo esté ordenado; es simple de implementar; sirve para cualquier tipo de datos
    - **Complejidad**: Mejor caso O(1) (si está al principio), Peor caso O(n) (si está al final o no está)
    - No escala bien, su rendimiento empeora linealmente con el tamaño de la entrada

## Comparaciones típicas
- vs [[17 - Búsqueda - Binaria]]: recorre todos los elementos O(n) vs divide y vence O(log n); no requiere orden vs requiere orden
- vs [[13 - Big-O - O(n) lineal]]: ejemplo práctico de complejidad lineal aplicada a búsqueda
- vs [[18 - Búsqueda - Comparación de eficiencia]]: algoritmo individual vs análisis cuantitativo frente a binaria

## Palabras clave
- búsqueda lineal
- recorrido secuencial
- O(n)
- sin orden previo
- peor caso

## Preguntas de examen
- ¿Cuál es el mejor y peor caso de la búsqueda lineal?
- ¿Cuándo conviene usarla aunque sea O(n)?

## Errores comunes
- Usarla en colecciones enormes con muchas consultas repetidas.
- Olvidar cortar el ciclo al encontrar el elemento.

## Mini-ejemplo (mental)
- Buscar una llave en un cajón desordenado revisando objeto por objeto.

