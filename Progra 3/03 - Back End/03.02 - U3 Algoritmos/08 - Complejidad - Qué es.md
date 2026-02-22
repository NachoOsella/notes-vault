# Complejidad - Qué es

## Definición
La complejidad describe cuántos recursos (tiempo y memoria) requiere un algoritmo según el tamaño de entrada.

## Explicación

- *Qué problema resuelve*
    Caracteriza cuántos recursos computacionales (tiempo y espacio) necesita un algoritmo para resolver un problema, permitiendo comparar algoritmos independientemente del hardware
- *Cómo funciona por arriba*
    Se refiere a la cantidad de recursos que necesita el algoritmo:
    - **Tiempo**: Cuánto tarda el algoritmo en ejecutarse y cómo evoluciona este tiempo según el tamaño de las entradas
    - **Espacio**: Cuánta memoria requiere
    Se analiza estimando cómo crecen estos recursos en función del tamaño del problema de entrada (denotado como n)
- *Qué implica / qué permite*
    Un algoritmo que funciona bien con 10 elementos puede volverse muy lento con 1000 o más; es importante pensar no solo en que el algoritmo funcione, s también en cómo escala; permite identificar algoritmos que se vuelven impracticables cuando el tamaño de la entrada crece

## Comparaciones típicas
- vs [[09 - Complejidad - Cómo se mide]]: concepto abstracto vs metodología de medición concreta
- vs [[10 - Complejidad - Temporal]]: complejidad general vs específicamente temporal (tiempo)

## Palabras clave
- complejidad
- recursos
- tiempo
- espacio
- escalado

## Preguntas de examen
- ¿Por qué la complejidad importa incluso cuando el algoritmo da el resultado correcto?
- ¿Qué diferencia conceptual hay entre complejidad temporal y espacial?

## Errores comunes
- Medir solo en computadora local y generalizar.
- No distinguir entre costo para casos pequeños y grandes.

## Mini-ejemplo (mental)
- Cocinar para 2 personas vs 200: misma receta, distinto costo operativo.

