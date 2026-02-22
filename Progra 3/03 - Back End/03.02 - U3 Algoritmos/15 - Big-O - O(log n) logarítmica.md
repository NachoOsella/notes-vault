# Big-O - O(log n) logarítmica

## Definición
O(log n) reduce el problema por mitades en cada paso, logrando gran eficiencia en entradas grandes.

## Explicación

- *Qué problema resuelve*
    Ofrece eficiencia cercana a constante incluso para entradas masivas, siendo una de las complejidades más eficientes
- *Cómo funciona por arriba*
    - Reduce el tamaño del problema a la mitad en cada paso
    - **Logaritmo**: responde "¿a qué número tengo que elevar la base para obtener un resultado?" (ej: log₂(8)=3 porque 2³=8)
    - Un algoritmo O(log n) divide el espacio de búsqueda a la mitad en cada paso
    - **Ejemplo**: búsqueda binaria - en cada paso se reduce la búsqueda a la mitad
    - **¿Cuántas veces podés dividir n a la mitad hasta que quede 1 elemento?** Eso es log₂(n)
    - Si n=8: 8→4→2→1 (3 pasos) = log₂(8)=3
    - Si n=16: 16→8→4→2→1 (4 pasos) = log₂(16)=4
    - Si n=1.000.000: solo ~20 pasos
- *Qué implica / qué permite*
    Aunque los datos crezcan muchísimo, el número de operaciones crece muy poco; muy eficiente en listas ordenadas; escala increíblemente bien

## Comparaciones típicas
- vs [[12 - Big-O - O(1) constante]]: muy eficiente pero no constante, crece muy lentamente
- vs [[13 - Big-O - O(n) lineal]]: crecimiento logarítmico es mucho mejor que lineal (ej: n=1M, log n ≈ 20)
- vs [[17 - Búsqueda - Binaria]]: ejemplo clásico de algoritmo O(log n)

## Palabras clave
- O(log n)
- reducción por mitades
- búsqueda binaria
- escalado eficiente
- datos ordenados

## Preguntas de examen
- ¿Qué requisito clave necesita la búsqueda binaria para ser O(log n)?
- ¿Por qué O(log n) escala mejor que O(n)?

## Errores comunes
- Aplicar estrategia logarítmica sobre datos desordenados.
- Olvidar costo de ordenar cuando corresponde.

## Mini-ejemplo (mental)
- Adivinar un número preguntando mayor o menor: cada pregunta corta el rango a la mitad.

