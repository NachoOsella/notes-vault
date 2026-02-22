# Fibonacci - Recursivo

## Definición
La versión recursiva implementa directamente F(n)=F(n-1)+F(n-2) con casos base.

## Explicación

- *Qué problema resuelve*
    Implementa la definición matemática de Fibonacci de forma directa y elegante usando recursividad
- *Cómo funciona por arriba*
    - **Recursividad**: Una función se llama a sí misma para resolver versiones más pequeñas del mismo problema
    - **Cálculo de Fibonacci(n)**: requiere conocer los dos anteriores: `fibonacci(n) = fibonacci(n-1) + fibonacci(n-2)`
    - **Código**: 
      ```java
      int fibonacci(int n) {
          if (n == 0) return 0;
          if (n == 1) return 1;
          return fibonacci(n-1) + fibonacci(n-2);
      }
      ```
    - **Proceso**: La función se llama recursivamente hasta llegar a los casos base (0 o 1), luego suma los resultados que regresan
- *Qué implica / qué permite*
    - **Ventajas**: Es intuitivo y fácil de implementar; código corto y legible
    - **Problema**: Tiene un gran problema de eficiencia - muchos cálculos se repiten innecesariamente
    - **Ejemplo**: `fibonacci(5)` calcula `fibonacci(2)` varias veces; a medida que n crece, la cantidad de repeticiones se vuelve enorme

## Comparaciones típicas
- vs [[22 - Fibonacci - Programación dinámica]]: implementación naive O(2^n) con recálculos vs optimizada O(n) con memoización
- vs [[05 - Algoritmos - Clasificación por forma de operar]]: ejemplo paradigmático de algoritmo recursivo vs iterativo
- vs [[21 - Fibonacci - Complejidad recursiva]]: código simple vs análisis de por qué es ineficiente

## Palabras clave
- recursión
- árbol de llamadas
- casos base
- recálculo
- O(2^n)

## Preguntas de examen
- ¿Qué hace intuitiva a la versión recursiva de Fibonacci?
- ¿Qué costo oculto aparece cuando n crece?

## Errores comunes
- Omitir casos base y provocar recursión infinita.
- Usarla para n grande sin memoización.

## Mini-ejemplo (mental)
- Resolver una tarea pidiendo dos subtareas por cada paso; el trabajo se multiplica rápido.

