# Algoritmos - Clasificación por forma de operar

## Definición
Clasifica algoritmos por su mecánica interna, principalmente iterativos o recursivos.

## Explicación

- *Qué problema resuelve*
    Ayuda a entender las diferentes estrategias de implementación disponibles para resolver un mismo problema según cómo opera internamente el algoritmo
- *Cómo funciona por arriba*
    Clasifica según el mecanismo de ejecución:
    - **Algoritmos iterativos**: Repiten instrucciones usando estructuras de control como bucles (for, while). Son muy comunes y suelen ser más eficientes en consumo de memoria que su versión recursiva
    - **Algoritmos recursivos**: Se llaman a sí mismos para resolver subproblemas más pequeños. Son elegantes y naturales para ciertos problemas como Fibonacci o recorridos de árboles. La recursión puede ser más costosa en memoria si no se optimiza
- *Qué implica / qué permite*
    Permite elegir entre claridad de código vs eficiencia; facilidad de implementación vs optimización; algunos problemas se expresan más naturales recursivamente; la iteración generalmente consume menos memoria que la recursión

## Comparaciones típicas
- vs [[04 - Algoritmos - Clasificación por tipo de problema]]: clasificación por estrategia de solución vs por categoría funcional
- vs [[20 - Fibonacci - Recursivo]]: ejemplos concretos de algoritmos recursivos vs iterativos aplicados a un mismo problema

## Palabras clave
- iterativo
- recursivo
- bucles
- pila de llamadas
- consumo de memoria

## Preguntas de examen
- ¿Cuándo conviene preferir una versión iterativa sobre una recursiva?
- ¿Qué costo adicional puede introducir la recursión?

## Errores comunes
- Usar recursión sin casos base correctos.
- Asumir que recursivo siempre es más elegante y también más eficiente.

## Mini-ejemplo (mental)
- Subir escaleras: podés contar peldaños con un loop (iterativo) o definir peldaño n en función de n-1 (recursivo).

