# Big-O - O(1) constante

## Definición
O(1) indica costo constante: la operación tarda prácticamente lo mismo sin importar n.

## Explicación

- *Qué problema resuelve*
    Representa el caso ideal donde el tiempo de ejecución no depende del tamaño de la entrada, permitiendo operaciones inmediatas sin importar la cantidad de datos
- *Cómo funciona por arriba*
    - El tiempo de ejecución no depende del tamaño de los datos
    - Siempre tarda lo mismo, con un solo paso o acceso
    - **Ejemplo**: Atención al primer cliente en fila preferencial - obtener el primer elemento de un arreglo (`return filaPreferencial[0]`)
    - No importa si hay 1, 10 o 1000 personas, el tiempo es el mismo
- *Qué implica / qué permite*
    Es la complejidad más eficiente; garantiza tiempos de respuesta predecibles; ideal para operaciones críticas que deben ser inmediatas

## Comparaciones típicas
- vs [[13 - Big-O - O(n) lineal]]: tiempo fijo independiente de n vs tiempo proporcional a n
- vs [[14 - Big-O - O(n^2) cuadrática]]: eficiencia óptima vs ineficiencia creciente con n grande
- vs [[15 - Big-O - O(log n) logarítmica]]: ambos son muy eficientes pero O(1) es estrictamente mejor

## Palabras clave
- O(1)
- acceso directo
- tiempo constante
- índice
- eficiencia

## Preguntas de examen
- ¿Qué operaciones típicas son O(1)?
- ¿Por qué O(1) es deseable en sistemas de alta demanda?

## Errores comunes
- Creer que rápido en promedio siempre es O(1).
- Confundir acceso por índice con búsqueda en estructura no indexada.

## Mini-ejemplo (mental)
- Abrir el cajón número 3: no importa cuántos cajones existan, vas directo.

